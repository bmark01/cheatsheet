<!-- omit in toc -->
# Cheat Sheet

- [Comment out lines of code in Visual Studio Code](#comment-out-lines-of-code-in-visual-studio-code)
- [DocFX](#docfx)
- [DocFxTocGenerator and indexing](#docfxtocgenerator-and-indexing)
- [GitHub Desktop Commit issue](#github-desktop-commit-issue)
- [Image path formatting](#image-path-formatting)
- [Insert TOC in Markdown document](#insert-toc-in-markdown-document)
- [Exclude items from TOC](#exclude-items-from-toc)
- [Markdown tips](#markdown-tips)
- [Relative Paths](#relative-paths)
- [SQL](#sql)
- [Web-Clear cache](#web-clear-cache)


___

### Comment out lines of code in Visual Studio Code
* Comment out: **Command**+**K**+**C**
  
* Uncomment: **Command**+**K**+**U**

___

### DocFX

* cmd to **build**: docfx init  
* To **start site**: docfx /Users/brucemark/shockwavedocfx/docfx.json --serve

* Add index.md to each directory for landing page
* toc.yml files are key in each folder!

___

### DocFxTocGenerator and indexing
1. cd to ShockWaveDocFX directory 
2. DocFxTocGenerator -d shockwave-software/Projects

	* Examples:
		* brucemark@Bruces-MBP-5-2 shockwavetest % DocFxTocGenerator -d 			shockwave-software/Projects
		* brucemark@Bruces-MBP-5-2 shockwavetest % DocFxTocGenerator -d 		shockwave-software/Solutions

3. Exit with return code 0= **success!**
4. In case you want **no help** go here: [Link to DocFXTocGenerator documentation](https://github.com/Ellerbach/docfx-companion-tools/tree/main/src/DocFxTocGenerator)
5. **Commands:**

	* '**-d "docs folder" "-o output folder" [-vsi]**'

	* -d, --docfolder          Required. Folder containing the documents.
	* -o, --outputfolder       Folder to write the resulting toc.yml in.
	* -v, --verbose            Show verbose messages.
	* -s, --sequence           Use the .order files for TOC sequence. Format are raws of: filename-without-extension
	* -r, --override           Use the .override files for TOC file name override. Format are raws of: filename-without-extension;Title you want
	* **-i, --index              Auto-generate a file index in each folder.**
	* -g, --ignore             Use the .ignore files for TOC directory ignore. Format are raws of directory names: directory-to-ignore
	* -m, --multitoc <depth>   Generate multiple toc files for child folders down to a certain child depth, default is 0 (root only generation).
	* --help                   Display this help screen.
	* --version                Display version information.
  
6. Sometimes **deleting the index** then recreating it, can clear up issues.

___

### GitHub Desktop Commit issue
**Error:** "The remote disconnected. Check your Internet connection and try again."  

**Fix:** Run this command from the directory you are trying to publish from (e.g. cheatsheet)
```
git config --global http.postBuffer 157286400

```

___
### Image path formatting
 `![text](~/images/query.png)`

___

### Insert TOC in Markdown document

* **Command**+**shift**+**P**  
* Type/choose:  "**_Markdown All in One: Create Table of Contents_**"  

> 📌 **Note:**  
> Need to install Markdown All in One extension for Visual Studio Code

___

### Exclude items from TOC  
  
```
<!-- omit in toc -->
```  

* Usage example: 
  
```
<!-- omit in toc -->
### Table of Contents  

```  

___

### Markdown tips
* [Handy Site](https://www.codecademy.com/resources/docs/markdown)
* Use two spaces after text to add a space in between lines.
* Footnotes- add \[^1] to doc and it will prompt to create a footnote. (needed plugin)
* To format commands - `JobStatus` WRITE (add job record) Use "`(the character below ~)" before and after command.  
  
___

> ⚠️ **Warning:**
> This is a warning message. Be careful!  

**Format:**
```
> ⚠️ **Warning:**
> This is a warning message. Be careful!  
```
___

> 📌 **Note:**  
> This is a note. Take note of this important information. 
 
**Format:** 
```
> 📌 **Note:**  
> This is a note. Take note of this important information.  
```
___

>  💡 **Tip:**
> This is a helpful tip. Use this advice to improve your workflow.


**Format:**
```
>  💡 **Tip:**
> This is a helpful tip. Use this advice to improve your workflow.
```
___

### Relative Paths
Use relative paths when your documentation and DocFX configuration file (docfx.json) are in the same directory or subdirectories.

Start the path with a dot (.) to indicate the current directory.
Use forward slashes (/) even on Windows for consistency.


Example: "files": [ "./src/**/*.cs" ] references all .cs files in the src subdirectory.

___

### SQL

**Select statements:**
* use three backticks <```> (under the tilde key) before and after the SQL statement - **on separate lines**) 
  * example:  
\`\`\`
select * from vcSubscriberRawCdr(nolock) where cast(EFFECTIVE_DATE as date) between '01/01/2024' and '01/31/2024'
\`\`\`

**Highlight table text:** ``` `attSubscriberRawCdr`.```
  
___

### Web-Clear cache

**To clear cache and reload site (reflect changes) in Chrome**

1. F12 or right click and choose "Insert"
2. Right click on refresh 
3. Click Empty Cash and Hard Reload  




