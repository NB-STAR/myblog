如果直接安装`pip install gmpy2`会出现一些报错

```
src/gmpy.h:106:12: fatal error: 'gmp.h' file not found
  #  include "gmp.h"
             ^~~~~~~
  1 error generated.
  error: command 'clang' failed with exit status 1

  ----------------------------------------
  Failed building wheel for gmpy2
```

需要先安装一些依赖

```
brew install gmp
brew install mpfr 
brew install libmpc
```

最后再安装 gmpy2

```
pip install gmpy2
```