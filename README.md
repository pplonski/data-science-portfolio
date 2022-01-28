# Data Science Portfolio website with Jupyter notebook and Mercury

Data Science Portfolio website contructed from Jupyter notebooks and served with [Mercury](https://github.com/mljar/mercury).

<p align="left" >
  <img 
    alt="Mercury Custom Welcome Message"
    src="https://raw.githubusercontent.com/mljar/visual-identity/main/mercury/custom_welcome_message.png" width="90%" />
</p>

### :notebook: Notebooks

There are thre notebooks served. Each notebooks is interactive - they have YAML header defined for Mercury.
- [Hello notebook](https://github.com/pplonski/data-science-portfolio/blob/main/hello_notebook.ipynb) - it accepts the name, and display welcome message,
- [CSV preview](https://github.com/pplonski/data-science-portfolio/blob/main/csv_preview.ipynb) - it accepts a CSV file and display it,
- [Show image](https://github.com/pplonski/data-science-portfolio/blob/main/show_image_notebook.ipynb) - it accpets image file and display it. 

:warning: The GitHub is not displaying the **RAW** cells when preview notebooks in GitHub. It is the best to clone the repo and open it in Jupyter Notebook/Lab.

### :computer: Demo

Demo is running at Heroku free dyno at http://piotr-data-science-portfolio.herokuapp.com.

### Run locally

#### Clone the code
```
git clone git@github.com:pplonski/data-science-portfolio.git
```

#### Add notebooks to Mercury

```
mercury add hello_notebook.ipynb
mercury add csv_preview.ipynb
mercury add show_image_notebook.ipynb
```

#### Run local server

``` 
mercury runserver --runworker
```

Please open a web browser, the website is running at [http://127.0.0.1:8000](http://127.0.0.1:8000).

### 🧰 Deploy

The repo can be easily deployed to Heroku with few commands.

#### Create Heroku app

```
heroku create my-amazing-app-name
```

#### Set environment variables in Heroku

```
heroku config:set SERVE_STATIC=True
heroku config:set ALLOWED_HOSTS=my-amazing-app-name.herokuapp.com
heroku config:set NOTEBOOKS=*.ipynb
heroku config:set WELCOME=welcome.md
```

#### Push the code to Heroku

```
git push heroku main
```

## Happy coding!

I hope that this example Data Science Portfolio will help you create your own website. Good luck!
