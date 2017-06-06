# MkDocs.cn

Project documentation with Markdown.

modified to support search in Chinese.

Idea from **ZhangXin**'s blog: http://wyqbailey.github.io/2015/08/13/make-mkdocs-support-chinese.html

Steps:

1. Change lunr.js to a modified clone from https://github.com/ming300/lunr.js

2. Modify **generate_search_index** in **mkdocs/search.py**, add _ensure_ascii=False_
```
return json.dumps(page_dicts, sort_keys=True,ensure_ascii=False, indent=4)
```

3. some Chinese text changes

4. Make it a pip module

## Installation
Of cource, you need python installed to use mkdocs.
```
# uninstall OFFICIAL MkDocs first
pip uninstall mkdocs

# install from github
pip install git+https://github.com/wusixin/mkdocs.cn

# or, install from github zip archive, faster
pip install https://codeload.github.com/wusixin/mkdocs.cn/zip/master
```

## Usage
see document from http://www.mkdocs.org
