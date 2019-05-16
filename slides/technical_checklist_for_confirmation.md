# Checklist demo technique:

### Slides:
+ port 8001
+ http://localhost:8001/slides/hello_minh.html#/
+ print-pdf: http://localhost:8001/slides/hello_minh.html?print-pdf#/

+ jupyter notebook for ppca-uncertainty runs on port 8881
+ embed: http://localhost:8881/notebooks/Interactive%20PPCA%20model.ipynb
+ dash_app: http://0.0.0.0:8050/ port 8050



### Fixed point with tsne:

+ BUILT env:
    * socket server port 5000
    * static server port 8888 (root: idr-server)
    * http://localhost:8888/main.html

+ DEV env: 
    * socket server port 5000
    * static server port 8888 (root: idr-server)
    * elm client port 8000 (root: idr-elm, run elm-reactor)


### Let jupyter notebook run on embedded iframe
+ generate jupyter config: `jupyter notebook --generate-config`

+ edit: `~/.jupyter/jupyter_notebook_config.py`
```
# Enable notebook in iframe
c.NotebookApp.tornado_settings = {'headers': {
    'Content-Security-Policy': "frame-ancestors 'self' http://localhost:8001"}}
```