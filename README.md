# lucky-markdown.vim 

Vim completion of Markdown links with top Google search results

## Introduction

lucky-markdown is a simple plugin that allows you to quickly fetch the top
Google result for a link in a Markdown document.

## Installation

To use lucky-markdown you need Vim to be compiled with Ruby support.

The recommeded installation method is through a Vim plugin manager such as
Pathon or Vundle. For example, to install with Pathogen:

    cd ~/.vim/bundle
    git clone git://github.com/avdgaag/vim-lucky-markdown.git

For more information on how these plugin managers work, please refer to their
documentation.

If you don't want to or cannot use such plugin managers, simply copy the files
from this repository to their respective locations in `~/.vim`:

    cp plugin/lucky-markdown.vim ~/.vim/plugin
    cp doc/lucky-markdown.txt ~/.vim/doc

To generate the helptags for this help file, see |:helptags|.

## Usage

After installing the plugin, an `omnicomplete` function is automatically
configured for Markdown documents. You can invoke it with CTRL-X CTRL-O (see
`i_CTRL-X_CTRL-O`) after your started writing a Markdown link.

For example, you can complete the following two link syntaxes (the | is the
current cursor):

    [Ruby]:|
    [Ruby](

This will result in the following completed text:

    [Ruby]: http://ruby-lang.org
    [Ruby](http://ruby-lang.org)

The text between the brackets will be used as the search query.

Note the completion function is only set in files with `filetype` markdown. To
enable it elsewhere, simply set `omnifunc` to `CompleteMarkdownLink`.

## About

**Author**: Arjan van der Gaag  
**License**: MIT license  
**Issues**: http://github.com/avdgaag/vim-lucky-markdown/issues  
**Source**: http://github.com/avdgaag/vim-lucky-markdown
