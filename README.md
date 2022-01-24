Modellbiblioteket's fork of the international openEHR.org CKM mirror, plus some "local" Swedish templates and archetypes
===========================================================================================================
The intention of this experimental "fork" is to make it simple to work with archetype and template tools to create and share local Swedish content based on international archetypes. You can download a zip (or maintain a GIT-clone/fork/link) of this repository in order to access the combination of international and local archetypes and templates in your tools.

Archetypes of international value and Swedish translations of international archetypes should be uploaded to the CKM tool (not here) and will then be semi-automatically be copied here upon next update/sync.

Please note that _operational_ templates (.opt-files) and other downstream openEHR-related artifacts should be maintained elsewhere, not here. (To see an example of how e.g. Region Östergötland plans to do this, look at the https://github.com/regionostergotland/openehr_definitions/ repository.)

Also note the shared ad-hoc work area at https://github.com/modellbibliotek/Arbetsyta-openEHR that can be used when you do not want the entire CKM-mirror content to potentially interfere with your work.

Directory names and content
---------------------------
Warning: the directory names are a bit confusing due to conventions and tools used "upstream"

* `/local`  currently may often contain many locally created archetypes and templates, all in the same directory, no matter what openEHR class they are based on. (This seems to be the default directory for saving new files created in Marand's ADL-designer). Needs regular manual cleanup by moving to suitable subdirectories.
* `/local/archetypes`, `/local/templates` and `/local/templates` contain directories copied straight from openEHR's international online CKM tool http://ckm.openehr.org via https://github.com/openEHR/CKM-mirror
* Potential example: `/local/standin/` a manually created subdirectory intended for (semi-regularly) manually organizing files from the project Standin3. Note that the tools do not save here by default.
* Potential example: `/local/regionostergotland/` example of a manually created subdirectory intended for (semi-regularly) manually organizing Region Östergötland's files. Note that the tools do not save here by default. Further project/topic-specific subdirectories could be created, e.g. `/local/regionostergotland/surgery` - the subdirectories under `/local` seem to be read by several tools.
* `/remote/` contains subdirectories like `no.nasjonalikt/archetypes` that have been copied from "national/regional" CKMs like http://arketyper.no/ckm/ into openEHR's international online CKM tool http://ckm.openehr.org they are thus "remote" with respect to the international CKM as opposed to the `/local/archetypes` considered local with respect to the international CKM. 
* `/` The root directory, containing this readme file and som other files cloned from the ckm-mirror. (It also seems to be where the ADL-designer tool stores archetypes that you "import" (rather than create) using the tool. Needs regular manual cleanup by moving to suitable subdirectories.

Thus, part of the content under `/local` and it's subdirectories is truly local to specific swedish projects/organisations and other content (e.g. `/local/archetypes`) comes from the international space...

Tools, tool settings and behavoiurs
-------------
List of available modelling tools: https://www.openehr.org/downloads/modellingtools

### The online Archetype-designer
Please note the somewhat odd directory choices used for saving new and imported assets described above. Template files created in the tool are by default saved with a ".t.json"-file ending. They can also be exported to several formats.

If you are using openEHRs online Archetype-designer https://tools.openehr.org/designer/#/ and login with a persoonal Github-account (or a group/organization-account) that is new in the tool, then this setting should work to add this repo:

Repositories (top menu bar) --> New repository (button) --> Repository type: GitHub
```
  Repository name: Region/Company Nnnns fork of Modellbibliotek's CKM-mirror (or whatever you want to call it)  
  Owner: modellbibliotek
  Repository: CKM-mirror
  Branch: master (or, if you want to work in a branch, the name of the branch instead of "master" )
```

Important: If you want to save files (and avoid some GitHub rate-limiting-related related "403" errors) you need to be logged in to github with a user account that has write permission to this repository, ideally before opening the ADL designer.

### Local-file-based tools
If you are using Ocean's Template designer or other local-file-based tools it should be possible to either 
* download and unpack the zip-file of this repository, found under the green "Clone or download" button on the https://github.com/modellbibliotek/CKM-mirror page or
* set up GIT client to keep in sync (this has a bit of learning curve...)

Update policy & instructions
----------------------------
We do occasional manual one-way updates from https://github.com/openEHR/CKM-mirror (that most often update the content of the '/local/archetypes' subdirectory tree). The direction is always _from_ the international CKM tool (automatically) to https://github.com/openEHR/CKM-mirror and from there (manually) to this fork https://github.com/modellbibliotek/CKM-mirror.

If we find an error or want to contribute new content to the international repository, then the web-based tools at http://ckm.openehr.org should be used for submitting such content. Files in this fork will _not_ be synced back automatically to the international repository.

Howto-instructions for Modellebibliotek-repo admins to update this repository to get the latest content from the international one: 
* With command-line tools https://help.github.com/articles/syncing-a-fork/ or
* Using the web: https://www.sitepoint.com/quick-tip-sync-your-fork-with-the-original-without-the-cli/

Howto-instructions for Modellebibliotek-repo admins regarding how to move a file uding GitHub's web tools: https://help.github.com/articles/moving-a-file-to-a-new-location/

Local/regional setup?
----------------------
If there is interest, then the chain can be: openEHR --> "modellbibliotek" (maybe later run by SFMI?) --> Your local region (e.g. Region Östergötland) 

If you want a stable local (regional?) repository where you can control when updates should happen, then make a fork of this repository and use that fork in your tools instead of using this shared Swedish repository in your tools. 

Using or forking this repository will give you access to both international assets and a copy of some Swedish local/regional/project-directories, possibly including work in progress (because you want to see what others are working on...).

--------------



### Marand's online ADL-designer
Please note the somewhat odd directory choices used for saving new and imported assets described above. Template files created in the tool are by default saved with a ".t.json"-file ending. They can also be exported to several formats.

If you are using Marand's online ADL-designer https://ehrscape.marand.si/designerv2 and nobody in your organization has yet added this repo, then this setting should work:

Repositories (top menu bar) --> New repository (button) --> Repository type: GitHub
```
  Repository name: Regione Nnnns fork of CKM-mirror (or whatever you want to call it)  
  Owner: modellbibliotek
  Repository: CKM-mirror
  Branch: master
```

If you want to save files (and avoid some GitHub rate-limiting-related related "403" errors) you need to be logged in to github with a user account that has write permission to this repository, ideally before opening the ADL designer.

### Local-file-based tools
If you are using Ocean's Template designer or other local-file-based tools it should be possible to either 
* download and unpack the zip-file of this repository, found under the green "Clone or download" button on the https://github.com/modellbibliotek/CKM-mirror page or
* set up GIT client to keep in sync (this has a bit of learning curve...)

Update policy & instructions
----------------------------
Without warning, we may do manual one-way updates from https://github.com/openEHR/CKM-mirror (that most often update the content of the '/local/archetypes' subdirectory tree). The direction is always _from_ the international CKM tool (automatically) to https://github.com/openEHR/CKM-mirror and from there (manually) to this fork https://github.com/modellbibliotek/CKM-mirror.

If we find an error or want to contribute new content to the international repository, then the web-based tools at http://ckm.openehr.org should be used for submitting such content. Files in this fork will _not_ be synced back automatically to the international repository.

Howto-instructions for repository admins to update this repository to get the latest content from the international one: 
* With command-line tools https://help.github.com/articles/syncing-a-fork/ or
* Using the web: https://www.sitepoint.com/quick-tip-sync-your-fork-with-the-original-without-the-cli/

Howto-instructions for admins regarding how to move a file using GitHub's web tools: https://help.github.com/articles/moving-a-file-to-a-new-location/

Local/regional setup?
----------------------
If there is interest, then the chain can be: openEHR --> "modellbibliotek" (maybe later run by SKL or EHM?) --> Your local region (e.g. Region Östergötland) 

If you want a stable local (regional?) repository where you can control when updates should happen, then make a fork of this repository and use that fork in your tools instead of using this shared Swedish repository in your tools. 

Using or forking this repository will give you access to both international assets and a copy of some Swedish local/regional/project-directories, possibly including work in progress (because you want to see what others are working on...).

--------------

Below you find the original readme content from...

openEHR Foundation International CKM Mirror 
===========================================

This is a mirror of the not-for-profit international openEHR.org Clinical Knowledge Manager (CKM) clinical models repository at www.openehr.org/ckm

It contains archetypes, templates and termsets on the CKM Authoring TRUNK, and will include both published assets and unpublished/unstable assets undergoing active development and review.

All of these assets are licenced under a Creative Commons Attribution-ShareAlike 3.0 licence ![CC-BY-SA License](https://i.creativecommons.org/l/by-sa/3.0/88x31.png) and can be used freely within open source or commercial applications.

This mirror auto-updates whenever the CKM TRUNK changes.

If you would like to contribute to development or review of the models, please register at www.openehr.org/ckm
