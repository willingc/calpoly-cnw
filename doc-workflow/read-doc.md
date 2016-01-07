# Working config for conda and readthedocs

## conda-env.yml
```
name: testjup_docs
channels:
- asmeurer
dependencies:
- sphinx==1.3.1
- pandoc
- nbformat
- jupyter_client
- ipykernel
- jupyter
```

##readthedocs.yml
```
conda:
    file: docs/conda-env.yml
python:
    version: 3.4
    setup_py_install: true
```


## Notes
- No sphinx in default dependencies
- Default sphinx is 1.2 (not high enough for us); Only creates first page with
no caption content or any content in sidebar

- Does not yet support sphinx 1.3.3
- Fall back and pin sphinx to 1.3.1
