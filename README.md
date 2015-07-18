# Asciidoctor Docker Container


## This Docker container provides:

* Asciidoctor (1.5.2 current version)
* Asciidoctor PDF (1.5.0.alpha.8)
* Source highlighting using CodeRay or Pygments

# How to use it. 

### There are three options:

## 1. Startup container

```docker run -it emedeiros/asciidoctor```

## 2. Startup container with shared folder

```docker run -it -v {local_shared_folder}:/pub emedeiros/asciidoctor```

## 3. Startup container with shared folder and nginx (webserver).


## 3.1 Startup container

```docker run -it -p 8080:80 -v {local_shared_folder}:/pub/ emedeiros/asciidoctor```


## 3.2 Start nginx

```nginx```


## 3.3 Access your document.

Open your browser and type the url: 
```http://docker.ip:8080/asciidoctor/{file.html}```


## TIPS:

### Convert adoc document to html

```asciidoctor example.adoc```

### Convert adoc document to pdf

```asciidoctor-pdf example.adoc```


Any question or sugestion? post here.