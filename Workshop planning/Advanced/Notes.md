### Content borrowed from https://github.com/agu-ossi/2018-agu-oss

1. Important to use functions to increase readibility
2. Building tests for your code is important so that you know it gives the right results depsite the changes. This can be automated and put on external servers.
3. Avoid using locally stored data. Download data directly from URL if possible. This makes the code more easily reusable.
4. Going from scipt to an open source library on Github:
  - Constinuous integration with tests
  - Version control
  - Choosing an open source license
  - Creating documentation
  - Including a code of conduct
  
5. For tests:
  - use `assert`
    - `assert np.all(<some-condition>)`
    - `np.allclose` actually is better as it does not ask for exact match. Useful because floats are always approximate. 
    
6. Putting functions into scripts for library makes them easily reusable instead of copy/pasting code again and again. 
7. For libraries:
  - docstring: 
  `
  '''
  This are my data analysis functions used to download and process some temperature time series from Berkeley Earth.
  ''' 
  `
  
8. For gitignore, selecting Python would setup the repository so that the auxiliary python files are not tracked. For example, temporary files that are created by Jupyter notebooks, etc. Jupyter notebooks have their own version of version control file stored in a folder called `.ipynb checkpoints`  (official list of .gitignore files https://github.com/github/gitignore)
 
9. Choose a license (choosealicense.com) (opensourceinitiative). Python mostly has MIT and BSD license. Can be used by both academics and industry. Completely open source. 
  - Having no license means its colpletely copyright you and no one else is allowed to use it or adapt it; prevents easy collaboration; others can spot bugs and make the code more usable. *People usually think otherwise and it creates a confusing and potentially tough situation*
  - Don't write your own license! 
  - Licenses take away liability as well. 

10. nbdime: For better view of differences between different versions of a Jupyter notebook.

11. setup-tools: set of functions and conventions that define how packages are built in python
  - module: a folder that has `__init__.py`; this is how python identifies a python package
  - create a folder with a name that you want your library to be: `mkdir <package-name>`
  - create a file called `setup.py`
    - uses package `setuptools`
    - version: 0.0.1  (the very first one; usually 1.0.0 is the first stable version)
    
12. To install the package: `pip install -e .`
      - `-e` means editable installation (creates a link to this folder instead of copying the contents as they stand right now to `site-packages` folder; the package stays alive and future edits are automatically incorporated.
      - `.` indicated current directory
      
13. To get documentation associated with a function, do `help(<function-name>)`
  - To add docstring, put `'''<some useful description of what the function does> ''' ` beneath the `def` statement
  - Conventional format:
  ```
  '''
  :param param_1: <description>
  :param param_2: <description>
  '''
  ```
  
14. It is useful to create a separate module for test functions: `touch ./data_analysis/test_<sometext>.py`

15. running `pytest` in your package's home directory looks for all the files starting with `test_` and runs the test.

16. Continuous Integration services automatically runs tests if there any changes in your repository. 
  - Travis-CI.org
  - create a configuration file to tell Travis what to do: `.travis.yml`
  - tests can be run for different versions of python, different os, etc. Make the code more robust. 

17. Select the repository in your Travis account.

18. Use ReadTheDocs/Sphinx to generate documentation

19. Add a code of conduct
  
  
  


