
# Table of Contents

-   [eterm-256color](#org59b410b)
    -   [Usage](#org5f67bf3)
        -   [Notes](#orgf4c6713)
    -   [Installation](#org554ac84)
    -   [Customization](#orga7015c4)
        -   [Bold](#org52a9541)
        -   [Faces](#org98ab195)



<a id="org59b410b"></a>

# eterm-256color

[![img](https://melpa.org/packages/eterm-256color-badge.svg)](https://melpa.org/#/eterm-256color)
[![img](https://stable.melpa.org/packages/eterm-256color-badge.svg)](https://stable.melpa.org/#/eterm-256color)

This package uses [xterm-color](https://github.com/atomontage/xterm-color) to add customizable 256 color support to `term`
and `ansi-term`.


<a id="org5f67bf3"></a>

## Usage

Add `eterm-256color-mode` to `term-mode-hook`:

    (add-hook 'term-mode-hook #'eterm-256color-mode)

Enjoy more colors.


<a id="orgf4c6713"></a>

### Notes

-   This package requires `eterm-color`. If it doesn't exist on your system, you
    will be offered the option of fetching and compiling it from [emacs-mirror](https://github.com/emacs-mirror/emacs).
    If instead you want to install manually, you can try:
    -   linux
        
            tic $(find /usr/share/emacs -name 'eterm-color.ti')
            # or
            tic -o ~/.terminfo $(find /usr/share/emacs -name 'eterm-color')
    -   macOS
        
            tic $(find $(brew --prefix emacs)/ -name 'eterm-color.ti')
            # or
            tic -o ~/.terminfo $(find $(brew --prefix emacs-plus)/ -name 'eterm-color.ti')
            # or
            tic -o ~/.terminfo /Applications/Emacs.app/Contents/Resources/etc/e/eterm-color.ti
-   You may have to restart ansi-term the very first time you start it after
    installing this package and adding the hook above - it should "just work" any
    time after that.
-   Make sure `TERM` really gets set to `eterm-256color`. It may be
    overridden if you export `TERM` in any of your shell init files.


<a id="org554ac84"></a>

## Installation

This package is on melpa. If you have melpa in your package repositiories, you
can use `M-x RET package-install RET eterm-256color` or install with
[use-package](https://github.com/jwiegley/use-package):

    (use-package eterm-256color
      :ensure t)

Alternatively, consider installing with [straight.el](https://github.com/raxod502/straight.el) or
[quelpa-use-package](https://github.com/quelpa/quelpa-use-package).

Otherwise, download the files to somewhere in your load path, and require
eterm-256color:

    (require 'eterm-256color)

If installing manually, make sure the file `eterm-256color.ti` is in the same
place as `eterm-256color.el`.


<a id="orga7015c4"></a>

## Customization


<a id="org52a9541"></a>

### Bold

You can use the variable `eterm-256color-disable-bold` disable bold colors.
When specified as bold, colors 0 - 7 will be rendered with their "bright"
counterpart instead.


<a id="org98ab195"></a>

### Faces

Each of the 256 faces is customizable:

<table>


<colgroup>
<col  class="org-left">

<col  class="org-left">

<col  class="org-left">
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Face</th>
<th scope="col" class="org-left">Alias</th>
<th scope="col" class="org-left">Default Value</th>
</tr>
</thead>
<tbody>
<tr>
<td class="org-left"><code>eterm-256color-default</code></td>
<td class="org-left">&#xa0;</td>
<td class="org-left">Inherited from <code>default</code> face</td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-black</code></td>
<td class="org-left"><code>eterm-256color-0</code></td>
<td class="org-left">Inherited from <code>xterm-color-names</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-red</code></td>
<td class="org-left"><code>eterm-256color-1</code></td>
<td class="org-left">Inherited from <code>xterm-color-names</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-green</code></td>
<td class="org-left"><code>eterm-256color-2</code></td>
<td class="org-left">Inherited from <code>xterm-color-names</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-yellow</code></td>
<td class="org-left"><code>eterm-256color-3</code></td>
<td class="org-left">Inherited from <code>xterm-color-names</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-blue</code></td>
<td class="org-left"><code>eterm-256color-4</code></td>
<td class="org-left">Inherited from <code>xterm-color-names</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-magenta</code></td>
<td class="org-left"><code>eterm-256color-5</code></td>
<td class="org-left">Inherited from <code>xterm-color-names</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-cyan</code></td>
<td class="org-left"><code>eterm-256color-6</code></td>
<td class="org-left">Inherited from <code>xterm-color-names</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-white</code></td>
<td class="org-left"><code>eterm-256color-7</code></td>
<td class="org-left">Inherited from <code>xterm-color-names</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-bright-black</code></td>
<td class="org-left"><code>eterm-256color-8</code></td>
<td class="org-left">Inherited from <code>xterm-color-names-bright</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-bright-red</code></td>
<td class="org-left"><code>eterm-256color-9</code></td>
<td class="org-left">Inherited from <code>xterm-color-names-bright</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-bright-green</code></td>
<td class="org-left"><code>eterm-256color-10</code></td>
<td class="org-left">Inherited from <code>xterm-color-names-bright</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-bright-yellot</code></td>
<td class="org-left"><code>eterm-256color-11</code></td>
<td class="org-left">Inherited from <code>xterm-color-names-bright</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-bright-blue</code></td>
<td class="org-left"><code>eterm-256color-12</code></td>
<td class="org-left">Inherited from <code>xterm-color-names-bright</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-bright-magenta</code></td>
<td class="org-left"><code>eterm-256color-13</code></td>
<td class="org-left">Inherited from <code>xterm-color-names-bright</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-bright-cyan</code></td>
<td class="org-left"><code>eterm-256color-14</code></td>
<td class="org-left">Inherited from <code>xterm-color-names-bright</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-bright-white</code></td>
<td class="org-left"><code>eterm-256color-15</code></td>
<td class="org-left">Inherited from <code>xterm-color-names-bright</code></td>
</tr>

<tr>
<td class="org-left"><code>eterm-256color-16</code> - <code>eterm-256color-255</code></td>
<td class="org-left">&#xa0;</td>
<td class="org-left">Generated by with <code>xterm-color--256</code></td>
</tr>
</tbody>
</table>

Note that to customize the first 16 colors you can either customize the
variables `xterm-color-names` and `xterm-color-names-bright` or customize the
faces directly.

