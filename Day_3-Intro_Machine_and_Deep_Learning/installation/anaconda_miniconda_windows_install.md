# Windows Tutorial: Installing Anaconda Miniconda and Making `conda` Findable

This tutorial is for complete beginners installing **Anaconda Miniconda** on Windows.

Miniconda is a minimal installer for conda. It includes:

- `conda`, a package and environment manager
- Python
- A small set of essential packages

By the end, you should be able to open Command Prompt or PowerShell and run:

```bat
conda --help
conda --version
```

---

## 1. Download the Windows installer

Use the official Anaconda Miniconda installer.

Direct download link for most Windows users:

```text
https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe
```

The file will usually be saved in your **Downloads** folder.

---

## 2. Run the installer

1. Open your **Downloads** folder.
2. Double-click:

```text
Miniconda3-latest-Windows-x86_64.exe
```

3. A setup window will open.
4. Click **Next**.

---

## 3. Accept the license

Read the license agreement.

Click:

```text
I Agree
```

---

## 4. Choose installation type

Choose:

```text
Just Me
```

This is usually best for new users because it avoids administrator permission problems.

Click **Next**.

---

## 5. Choose the install location

The default location is usually fine.

It may look something like:

```text
C:\Users\YourName\miniconda3
```

Avoid installing Miniconda inside cloud-synced folders such as:

```text
OneDrive
Dropbox
Google Drive
```

Also avoid paths with unusual characters or spaces.

Click **Next**.

---

## 6. Add Miniconda to PATH

During installation, you may see an advanced option like:

```text
Add Miniconda3 to my PATH environment variable
```

Select this option.

This makes `conda` findable from normal Command Prompt and PowerShell windows.

You may see a warning that adding conda to PATH is not recommended. The warning exists because adding Python tools to PATH can sometimes conflict with other Python installations.

For this beginner tutorial, the goal is to make `conda` easy to call from any terminal, so enable:

```text
Add Miniconda3 to my PATH environment variable
```

You may also see an option similar to:

```text
Register Miniconda3 as my default Python
```

For most beginners, it is okay to leave this selected unless your course, lab, or workplace tells you otherwise.

Click **Install**.

---

## 7. Finish installation

When installation finishes, click **Finish**.

Close any open Command Prompt or PowerShell windows.

Open a new Command Prompt or PowerShell window. This is important because PATH changes only apply to new terminal windows.

---

## 8. Check that `conda` works

Open **Command Prompt** or **PowerShell**.

Run:

```bat
conda --help
```

If the installation worked, you should see a help message listing available `conda` commands.

Then run:

```bat
conda --version
```

You should see something like:

```text
conda 25.x.x
```

The exact version number may be different.

You can also run:

```bat
conda info
```

This prints detailed information about your conda installation.

---

## 9. Check where Windows finds `conda`

Run:

```bat
where conda
```

You should see a path similar to:

```text
C:\Users\YourName\miniconda3\Scripts\conda.exe
```

You can also check your PATH:

```bat
echo %PATH%
```

Look for entries similar to:

```text
C:\Users\YourName\miniconda3
C:\Users\YourName\miniconda3\Scripts
C:\Users\YourName\miniconda3\Library\bin
```

---

## 10. If `conda` is not found

If you see:

```text
'conda' is not recognized as an internal or external command
```

first close Command Prompt or PowerShell and open a new one.

Then try again:

```bat
conda --help
```

If it still does not work, manually add Miniconda to your user PATH.

### Manual Windows PATH fix

1. Open the Start Menu.
2. Search for:

```text
Environment Variables
```

3. Open:

```text
Edit environment variables for your account
```

4. Under **User variables**, select:

```text
Path
```

5. Click **Edit**.
6. Add these entries, replacing `YourName` with your Windows username:

```text
C:\Users\YourName\miniconda3
C:\Users\YourName\miniconda3\Scripts
C:\Users\YourName\miniconda3\Library\bin
```

7. Click **OK** on all windows.
8. Close and reopen Command Prompt or PowerShell.
9. Test again:

```bat
conda --help
```

---

## 11. Create a test environment

Once `conda` works, create a test environment:

```bat
conda create -n test-conda python
```

Conda will show a list of packages it wants to install.

When it asks whether to proceed, type:

```text
y
```

and press Enter.

---

## 12. Activate the test environment

Run:

```bat
conda activate test-conda
```

Your terminal prompt may change.

You may see something like:

```text
(test-conda)
```

That means the environment is active.

---

## 13. Check that Python works

While the `test-conda` environment is active, run:

```bat
python --version
```

You should see a Python version number.

Now open Python:

```bat
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

---

## 14. Install a small test package

With the `test-conda` environment still active, install NumPy:

```bat
conda install numpy
```

When conda asks whether to proceed, type:

```text
y
```

and press Enter.

Then test NumPy:

```bat
python -c "import numpy; print(numpy.__version__)"
```

If this prints a version number, the package installed correctly.

---

## 15. Deactivate the environment

When you are done, run:

```bat
conda deactivate
```

Your terminal prompt should return to normal.

---

## 16. Optional: Remove the test environment

After you confirm everything works, you can delete the test environment:

```bat
conda remove -n test-conda --all
```

When asked whether to proceed, type:

```text
y
```

and press Enter.

---

## 17. Final success checklist

Your installation is working if these commands run successfully:

```bat
conda --help
conda --version
conda info
where conda
```

You should also be able to create and use a test environment:

```bat
conda create -n test-conda python
conda activate test-conda
python --version
```

If these commands work, Anaconda Miniconda is installed correctly and `conda` is findable from your Windows terminal.
