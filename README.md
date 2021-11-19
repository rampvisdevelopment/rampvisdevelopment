## The rampvisdevelopment account
This is an account to host data needed for the development of the RAMP VIS project ([rampvis-api](https://github.com/ScottishCovidResponse/rampvis-api), [rampvis-ui](https://github.com/ScottishCovidResponse/rampvis-ui)).

*There are two ways of hosting data on this account for use in the rampvis project, **gists** and **repositories***.

### Gists

[gist/gists](https://docs.github.com/en/github/writing-on-github/editing-and-sharing-content-with-gists/creating-gists) is a service github offers to upload one or a small number of files rather than an entire project. 

**Advantages to using gists:**
* The url to files are presistent, this is not true if you store a file on a branch of a repo and then merge that branch.
* Gists keep track of changes, like a normal github repository.
* It is easy and quick to upload data as a gist, unlike creating a normal github repository.
* You can acess both public **and** secret gists directly if you have the URL, unlike normal github.
* No need for pull requests and other overhead, unlike normal github. Thus saving team members' time.
* Loading data from gists means it is not neccessary to push data along with code to the other repositories.

To create a gist, log into this account. Then go to https://gist.github.com/ and drag the file into the box, alternatively, explicitly copy the contents of the file into the box. Then, decide if the gist should be public, that is searchable, or private meaning you need the URL to find it. Now the data you uploaded can be seen at https://gist.github.com/rampvisdevelopment, and to get a URL for it, go to the gist, click raw and copy that url. 

To get the latest version of the data, if it is updated, remove the characters between "raw" and the file name.   
Thus, the url ".../raw/123456789/example.txt" would go to ".../raw/example.txt" and so on. Supply this url in `urls.json`, and your file will be downloaded every time the downloader_agent runs.

**Limitations of gists**
* Gist lacks many features of normal github. It is for storing small files needed for development rather a place for development itself.

### Repositories
If you have a larger number of files with a folder structure you would like to preserve you can create a repository on this account, similar to the [example repository](https://github.com/rampvisdevelopment/example_data_respository). This will be downloaded as a zip file and unzipped by the download agent if you provide the appropriate url to the api, for the example repository this is: `https://github.com/rampvisdevelopment/example_data_respository/archive/main.zip`.

Similar to using gists you will need to add the information required by the downloader agent to `url.json`, for the [example repository](https://github.com/rampvisdevelopment/example_data_respository) this might be:

```
    {
        "name": "example_structured_data",
        "url": "https://github.com/rampvisdevelopment/example_data_respository/archive/main.zip",
        "save_to": "example_folder"
    }
```

## ⚠️ Caveats ⚠️
**The file ending of the url is important for the files to be downloaded correctly**, currently the supported formats are: `.csv`,`.json`and `.zip`.
<!--
**rampvisdevelopment/rampvisdevelopment** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
