# Kustomize issue #2538 

Files to reproduce the issue described here: https://github.com/kubernetes-sigs/kustomize/issues/2538#issuecomment-636929842

## To reproduce:

```
$ ./no-https.sh
Error: accumulating resources: accumulateFile "accumulating resources from '../base': evalsymlink failure on '/private/var/folders/f8/sscyyk1n3cq98pnj14_ghk8m0000gn/T/kustomize-003321775/base' : lstat /private/var/folders/f8/sscyyk1n3cq98pnj14_ghk8m0000gn/T/kustomize-003321775/base: no such file or directory", loader.New "Error loading ../base with git: url lacks host: ../base, dir: evalsymlink failure on '/private/var/folders/f8/sscyyk1n3cq98pnj14_ghk8m0000gn/T/kustomize-003321775/base' : lstat /private/var/folders/f8/sscyyk1n3cq98pnj14_ghk8m0000gn/T/kustomize-003321775/base: no such file or directory, get: invalid source string: ../base"

$ ./with-https.sh
# no output, exit 0
```
