# macOS Tutorial: Installing Anaconda Miniconda and Making `conda` Findable

This tutorial is for complete beginners installing **Anaconda Miniconda** on macOS.

Miniconda is a minimal installer for conda. It includes:

- `conda`, a package and environment manager
- Python
- A small set of essential packages

By the end, you should be able to open Terminal and run:

```bash
conda --help
conda --version
```


## 1. Choose the correct macOS installer

You need to know whether your Mac uses **Apple Silicon** or **Intel**.

Apple Silicon Macs include M1, M2, M3, M4, or newer chips.

### Apple Silicon Mac

Use this direct installer link:

```text
https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh
```

### Intel Mac

Use this direct installer link:

```text
https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
```

Download the correct file. It will usually be saved in your **Downloads** folder.


## 2. Open Terminal

Open **Terminal**.

One easy way is:

1. Press:

```text
Command + Space
```

2. Type:

```text
Terminal
```

3. Press Enter.


## 3. Go to your Downloads folder

In Terminal, run:

```bash
cd ~/Downloads
```


## 4. Run the installer

For Apple Silicon Macs, run:

```bash
bash Miniconda3-latest-MacOSX-arm64.sh
```

For Intel Macs, run:

```bash
bash Miniconda3-latest-MacOSX-x86_64.sh
```

If you are not sure what the file is called, run:

```bash
ls
```

Look for a file that starts with:

```text
Miniconda3
```

Then run it with `bash`.

For example:

```bash
bash Miniconda3-latest-MacOSX-arm64.sh
```


## 5. Accept the license

The installer will show license text.

Press Enter to scroll.

When asked whether you accept the license, type:

```text
yes
```

and press Enter.


## 6. Choose the install location

The installer will suggest a location such as:

```text
/Users/yourname/miniconda3
```

For beginners, the default location is usually fine.

Press Enter to accept it.


## 7. Initialize conda so it is findable

Near the end of the installer, you may see a question like:

```text
Do you wish to update your shell profile to automatically initialize conda?
```

Type:

```text
yes
```

and press Enter.

This lets the installer run `conda init`, which updates your shell configuration so that `conda` is available when you open a normal Terminal window.

On modern macOS, the default shell is usually `zsh`, so this usually updates:

```text
~/.zshrc
```

After installation, close Terminal completely and open it again.


## 8. Check that `conda` works

Open a new Terminal window.

Run:

```bash
conda --help
```

If the installation worked, you should see the `conda` help message.

Then run:

```bash
conda --version
```

You should see something like:

```text
conda 25.x.x
```

The exact version number may be different.

You can also run:

```bash
conda info
```

This prints detailed information about your conda installation.


## 9. Check where macOS finds `conda`

Run:

```bash
which conda
```

You should see something like:

```text
/Users/yourname/miniconda3/bin/conda
```

You can also check your PATH:

```bash
echo $PATH
```

Look for something like:

```text
/Users/yourname/miniconda3/bin
```


## 10. If `conda` is not found

If you see:

```text
conda: command not found
```

first close Terminal and open a new one.

Then try again:

```bash
conda --help
```

If it still does not work, activate Miniconda manually:

```bash
source ~/miniconda3/bin/activate
```

Then test:

```bash
conda --help
```

If that works, initialize conda for Zsh:

```bash
conda init zsh
```

Then close Terminal and open it again.

If you use Bash instead of Zsh, run:

```bash
conda init bash
```

Then close and reopen Terminal.


## 11. Manual macOS PATH fix

Most users should use `conda init`, but if you specifically need to add Miniconda to PATH manually, first check which shell you use:

```bash
echo $SHELL
```

If the result contains `zsh`, edit your Zsh configuration:

```bash
nano ~/.zshrc
```

If the result contains `bash`, edit your Bash configuration:

```bash
nano ~/.bashrc
```

Add this line at the end:

```bash
export PATH="$HOME/miniconda3/bin:$PATH"
```

Save the file.

In `nano`, press:

```text
Ctrl + O
Enter
Ctrl + X
```

Reload your shell configuration.

For Zsh:

```bash
source ~/.zshrc
```

For Bash:

```bash
source ~/.bashrc
```

Test again:

```bash
conda --help
```


## 12. Create a minimal environment

__Note__: We will use this minimal environment for the first sessions of the workshop. Be sure o have it created and running.

Once `conda` works, create a test environment:

```bash
conda create -n jupyter-env python=3.10 jupyterlab ipykernel ipython
```

Conda will show a list of packages it wants to install.

When it asks whether to proceed, type:

```text
y
```

and press Enter.


## 13. Activate the test environment

Run:

```bash
conda activate jupyter-env
```

Your terminal prompt may change.

You may see something like:

```text
(jupyter-env)
```

That means the environment is active.


## 14. Check that Python works

While the `jupyter-env` environment is active, run:

```bash
python --version
```

You should see a Python version number.

Now open Python:

```bash
python
```

You should see a Python prompt like:

```text
>>>
```

Type:

```python
print("Anaconda Miniconda is working!")
```

Then press Enter.

You should see:

```text
Anaconda Miniconda is working!
```

To exit Python, type:

```python
exit()
```

and press Enter.


## 15. Final success checklist

Your installation is working if these commands run successfully:

```bash
conda --help
conda --version
conda info
which conda
```

You should also be able to create and use an environment:

```bash
conda activate jupyter-env
python --version
conda deactivate
```

If these commands work, Anaconda Miniconda is installed correctly and `conda` is findable from your macOS Terminal.
