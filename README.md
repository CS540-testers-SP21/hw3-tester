# hw3-tester

Tests for CS540 Spring 2021 HW3: Principal Component Analysis 

## Usage

Download [test.py](test.py) and move it into the directory that contains `pca.py` and `YaleB_32x32.npy`

The contents of your directory should look like this:

```shell
$ tree
.
├── YaleB_32x32.npy
├── pca.py
└── test.py
```

To run the tests, do

```python
$ python3 test.py
```

It is assumed that `YaleB_32x32.npy` is present in the same directory as `test.py` and `pca.py`. If this is not the case, you can the argument `--yale-path` like this:

```python
$ python3 test.py --yale-path path/to/YaleB_32x32.npy
```

### Testing with GitHub Actions

Tests can be run by GitHub Actions automatically every time you push your code.  To set this up, this file needs to be in a folder named `.github/workflows`.  Run this command to copy the file into your project:

```bash
$ cp example_github_actions.yml /path/to/CS540/hw3/.github/workflows/ci.yml
```

Then open the file and edit the `NET_ID` environment variable on line 23.  With this setup, GitHub automatically runs the unit tests in `test.py` whenever you run `git push`.  You will get an email from GitHub if the unit tests fail.  
This workflow will also generate the `hw<num>_<NETID>.zip` file you need to turn in.  It can be downloaded by going to the `Actions` tab of the main page of your GitHub repo, scrolling down to artifacts section, and clicking on the file.

One thing to note is Actions is included in a GitHub Pro account.  This comes in the [GitHub Student Deveoloper Pack](https://education.github.com/pack) which is free for students and comes with like 300 hours of Actions run time per month or something like that.

## Disclaimer

These tests are not endorsed or created by anyone working in an official capacity with UW Madison or any staff for CS540. The tests are make by students, for students.

By running `test.py`, you are executing code you downloaded from the internet. Back up your files and take a look at what you are running first.

If you have comments or questions, create an issue at [https://github.com/CS540-testers-SP21/hw3-tester/issues](https://github.com/CS540-testers-SP21/hw3-tester/issues) or ask in our discord at [https://discord.gg/RDFNsAxgCQ](https://discord.gg/RDFNsAxgCQ).