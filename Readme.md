Elves of santa 101, global packaging.

This repository is purposely kept simple as a hello world template to enable others to allow other elves to join team North-Pole and publish global packages.

This is one way to create a global package, in the future this repo will suport other global install implementations. If they exist.

The current implementation was sourced from: https://ourcodeworld.com/articles/read/393/how-to-create-a-global-module-for-node-js-properly

This program is helpful for an experiment that I am working on for my screensaver application:
https://www.npmjs.com/package/aerial_desktop

## Usage:

first put this in terminal
```bash
bangWithHammer() {
git clone --depth=1 https://github.com/michaeldimmitt/elves-of-santa-101-global-packaging.git $1;
cd $1;
info='  ''"'name'"'': "'$1'",';
sed -i '' '2s?.*?'"$info"'?' ./package.json;
echo "Prompting for npm login information, I sure hope you know what you are doing."
npm login;
npm publish;
npm install -g $1;
};
```

Then run bangWithHammer for your application:
```bash
# Anything in < > field means enter your specific information
bangWithHammer <your application>

# run your the package after the npm install:
playWithPackageWrapping
```
