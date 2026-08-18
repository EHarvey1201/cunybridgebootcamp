## Installing Anaconda i.e.  

You have the option to use install  __Python 3.13__. 

- [Download Anaconda](https://www.anaconda.com/download/success) (larger installation file, may take a while on CUNY GC Wifi)

## Installing miniforge

### Miniforge is a mini-installer of anaconda that defaults to installing packages from the community-based conda-forge channel (which is free!) and organization independent: university vs non-profit, doesn't matter!

## Step 1a: Locate the "Terminal" application in your macbook. Can be found with Mac shortcut for spotlight (⌘ + space), then typing in "Terminal". (I'd recommend pinning this application to your dock)

## Step 1b: Get the installer (about 60MB)
```
curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
```

## Step 1c: Run the installer
```
bash Miniforge3-$(uname)-$(uname -m).sh
```

## follow prompts
- hit enter until prompted with yes/no to accept/reject licensing terms
- set where you wanna set base installation for where to place miniforge3
- default to ${HOME}, press enter
- after installation is finished, you'll be prompted with yes/no to have your shell environment automatically initialize conda. We want this. Enter yes.

## You should see a message that looks something like:
```
==> For changes to take effect, close and re-open your current shell. <==

Running `shell init`, which:
 - modifies RC file: "/Users/YOUR_USER_NAME/.zshrc"
 - generates config for root prefix: "/Users/YOUR_USER_NAME/miniforge3"
 - sets mamba executable to: "/Users/YOUR_USER_NAME/miniforge3/bin/mamba"
The following has been added in your "/Users/YOUR_USER_NAME/.zshrc" file

# >>> mamba initialize >>>
# !! Contents within this block are managed by 'mamba shell init' !!
export MAMBA_EXE='/Users/YOUR_USER_NAME/miniforge3/bin/mamba';
export MAMBA_ROOT_PREFIX='/Users/YOUR_USER_NAME/miniforge3';
__mamba_setup="$("$MAMBA_EXE" shell hook --shell zsh --root-prefix "$MAMBA_ROOT_PREFIX" 2> /dev/null)"
if [ $? -eq 0 ]; then
    eval "$__mamba_setup"
else
    alias mamba="$MAMBA_EXE"  # Fallback on help from mamba activate
fi
unset __mamba_setup
# <<< mamba initialize <<<

Thank you for installing Miniforge3!
```

## Step 1d: conda should now be installed! For changes to take effect, close this terminal and open a new one! 

## Step 1e: Update everything next! (May take a few minutes)
```
conda update --all
```
- Eventually you'll be prompted with y/n to install recommended packages. Enter y.

## Step 1f: Install "git" and "notebook"
```
conda install git
conda install notebook
```
