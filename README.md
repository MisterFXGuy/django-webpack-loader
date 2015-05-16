# django-webpack-loader
(support for production environments coming soon.)

Use webpack to generate your static bundles without django's staticfiles or opaque wrappers. 


Django webpack loader consumes the output generated by [webpack-bundle-tracker](https://github.com/owais/webpack-bundle-tracker) and lets you use the generated bundles in django.



<br><br>
### Configuration

Assuming `assets/` is in `settings.STATICFILES_DIRS` like 
```
STATICFILES_DIRS = (
    os.path.join(BASE_DIR, 'assets'),
)
```

<br>

##### WEBPACK_BUNDLE_URL
```
WEBPACK_BUNDLE_URL = STATIC_URL + 'bundles/'
```

URL (not path) to the directory that webpack outputs the bundles to. This should correspond to `output.path` in your webpack config.

<br>

##### WEBPACK_STATS_FILE
```
WEBPACK_STATS_FILE_PATH = os.path.join(BASE_DIR, 'assets/webpack-stats.json')
```

PATH (not url) to the `webpack-stats.json` file. This corresponds to `filename` in `new BundleTracker({filename: './assets/webpack-stats.json'})` from your webpack config.
`

<br>
