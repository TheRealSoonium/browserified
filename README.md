# The purpose of this repository is to provide the ability to generate browserified versions of select javascript modules.

**These instructions are for LINUX**

You will need git, npm, node, browserify (globally installed)

```
sudo apt install git
```

Install nvm (brings npm and node)
See https://github.com/nvm-sh/nvm
This creates ~/.nvm/ and adds some variables to the end of ~/.bashrc:
```
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
. ~/.bashrc  # load nvm
command -v nvm # see that it exists
```

Install the latest versions of node and switch to it:
```
nvm install --lts
nvm use --lts
```

Install browserify globally (for the user)
```
npm install -g browserify
```

Clone this repository (or your fork)
```
git clone https://github.com/TheRealSoonium/browserified
cd browserified
```

Install dependencies listed in package.json
```
npm install
```

Delete and recreate the browserified modules in the build/ directory
```
npm run clean
npm run build
```

Check that build files have been overwritten
```
git status
```

You can now commit and push 
```
git commit -a
git push 
```

# OTHER NOTES:

The last version of @solana/web3.js for which browserify works is 1.75.0 so that is the version that is used. Subsequent versions result in 'SyntaxError: Unexpected token'.




