# parser

parser = argparse.ArgumentParser()
这个用来解析命令行参数的意思是，我可以在执行 python image_show.py 这行参数后面可以加上更多的参数，然后 parser 就能获取到这个参数运用在代码里是吗

使用 `argparse.ArgumentParser()` 可以让你在运行程序时附加更多参数，例如：

```bash
python image_show.py image.jpg --option value
```

然后在代码中你可以通过调用 `parser.add_argument()` 来定义和解析这些参数，进而在程序中使用它们。这样可以让你的程序更加灵活，能根据不同的输入参数执行不同的操作。

---

在 `parser.add_argument('path_image', help="path to input image to be displayed")` 中，`help` 参数用于提供关于该参数的说明。当用户在终端运行程序并使用 `-h` 或 `--help` 选项时，程序会显示这个说明，帮助用户理解这个参数的作用以及如何使用它。例如，运行以下命令：

```bash
python image_show.py -h
```

输出中就会包含 `"path to input image to be displayed"` 这样的提示信息，告诉用户 `path_image` 应该是什么样的输入。
