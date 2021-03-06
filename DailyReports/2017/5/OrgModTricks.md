# Emacs的Org-mode技巧总结

&ensp;&ensp; Emacs的 `Org-mode` 是一个强大的写作工具，与 `Markdown` 相比， `Org-mode` 的功能更为强大，但是同时它的学习成本相对来说要高一些。 `Org-mode` 中有许多很方便的 小技巧，这篇博文主要是用来记载和总结使用过程发现的技巧， 以便以后忘了可以查找。并会一直更新。


## `Org-mode` 将 `Latex` 导出到 `Markdown`

&ensp;&ensp; `Org-mode` 对 `Latex` 支持很好，可以直接通过 `\begin{}-\end{}` 方式嵌入 `Latex` 代码，但是在 `Org-mode` 中导出为 `Markdown` 后， `Latex` 并不会进行转换。 这里就稍微进行下设置。 比如:

```latex
\begin{equation}
x(k) = As(k)+n(k)
\end{equation}
```

会输出为:

`\begin{equation}x(k) = As(k)+n(k)\end{equation}`

&ensp;&ensp; 这时你只需要添加一行配置， 让 `Emacs` 将 `Latex` 转换成图片， 然后在导出 `Markdown` 中显示。 这里你可以选择 `Emacs` 内置的 `dvipng` 或者 `imagemagick` (需要安装)来进行图片转换。 其中 `divpng` 只能转换成 `png` 图片格式, 而 `imagemagick` 可以转换成多种图片格式。

-   如果你采用 `divpng` 的话:

需要在代码上方或者文档顶部添加 `#+OPTIONS: tex:dvipng` , 比如:

```latex
#+OPTIONS :tex:dvipng
\begin{equation}
x(k) = As(k)+n(k)
\end{equation}
```

&ensp;&ensp; 导出的 `Markdown` 中会显示为:


<div class="figure">
<p><img src="ltximg/OrgModTricks_da989f80eca58d5a7e6beb1b360c34d57f8c2336.png" alt="OrgModTricks_da989f80eca58d5a7e6beb1b360c34d57f8c2336.png" /></p>
</div>

-   如果你使用 `imagemagick` 的话

需要在代码上方或者文档顶部添加 `#+OPTIONS: tex:iamgemagick` , 比如:

```latex
#+OPTIONS :tex:imagemagick
\begin{equation}
x(k) = As(k)+n(k)
\end{equation}
```

&ensp;&ensp; 导出的 `Markdown` 中会显示为:


<div class="figure">
<p><img src="ltximg/OrgModTricks_da989f80eca58d5a7e6beb1b360c34d57f8c2336.png" alt="OrgModTricks_da989f80eca58d5a7e6beb1b360c34d57f8c2336.png" /></p>
</div>

> 
> 
> Everything should be made as simple as possible, but not any simpler &#x2013; Albert Einstein
