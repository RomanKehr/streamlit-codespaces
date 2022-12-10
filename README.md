# PROBLEM

If you try to start streamlit in a github codespace with

```streamlit run YourFile.py```

and open the provided URL, you'll be stuck at

![alt text](https://github.com/RomanKehr/streamlit-codespaces/raw/main/pleasewait.png "Please wait...")

# SOLUTION

Add the following lines to your _.streamlit\config.toml_

```
[server]
enableCORS = false
enableXsrfProtection = false
```

After this, you can access your streamlit app in the browser from inside the codespace without a problem.
