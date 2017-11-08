## Configuring jupyter notebook

### Find the desired version of python
```
import sys
sys.executable
```


### Remove old kernel
```
jupyter kernelspec list
jupyter kernelspec remove [old-address]
```
Find the json file of your notebook:

```
vi /usr/local/share/jupyter/kernels/python2/kernel.json
``` 

and edit the file accordingly:

```
{
 "display_name": "Python 2",
 "language": "python",
 "argv": [
  "/home/javidi/anaconda2/bin/python",
  "-m",
  "ipykernel",
  "-f",
  "{connection_file}"
 ]
}

```

### Reinstall the ipython kernel
```
/home/javidi/anaconda2/bin/python -m pip uninstall ipykernel
/home/javidi/anaconda2/bin/python -m pip install ipykernel
```

