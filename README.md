# meteor-slow-build-bug

### Steps to reproduce:
mkdir meteor-slow-build-bug</br>
cd meteor-slow-build-bug</br>
git clone https://github.com/lawrentiy/meteor-slow-build-bug.git</br>
meteor npm i</br>
METEOR_PROFILE=1 meteor run</br>
find line 'linker File#getPrelinkedOutput' - it has amout of time</br>
</br>
### How to "fix" (1 variant)
change server.js</br>
write import {ToggleStar} from 'material-ui/svg-icons' instead of import {SvgIcon} from 'material-ui'</br>
</br>
### How to "fix" (2 variant)
change node_packages/svg-icons/index.js</br>
remove line with multiple assigment "exports.ToggleStar = exports.ToggleStarHalf ... exports.ActionAccessibility = undefined;"</br>
