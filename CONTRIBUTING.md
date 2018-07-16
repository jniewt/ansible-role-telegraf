# Contributing

### Git guidelines

First and foremost, please read the "Commit Guidelines" section from the [Pro Git book](https://git-scm.com/book/en/v2/Distributed-Git-Contributing-to-a-Project) and abide by the best practice described there. It takes some practice but it makes cooperation much easier for everyone.

### Large binary files

Git doesn't handle binary files very well out of the box, for reasons you can read up if you do a very short research on the subject. This applies to all sort of binary files like `jpg`, `ppt`, `mp4`, `exe`, `zip`, etc. The ignore file in this repository doesn't allow these files here. If you need to version such files, you are strongly advised to use git extension Git LFS. If your repository is already tracking binary files with LFS, you should install LFS before cloning (and advise other contributors to do so). Packages are available for many operating systems (e.g. git-lfs for ubuntu/debian). See [setup instructions](https://git-lfs.github.com/).
