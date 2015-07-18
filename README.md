# Asciidoctor Docker Container


## This Docker container provides:

* Asciidoctor (1.5.2 current version)
* Asciidoctor PDF (1.5.0.alpha.8)
* Source highlighting using CodeRay or Pygments

# How to use it. 

### There are three options:

## 1. Startup container

```sh
docker run -it emedeiros/asciidoctor
```

## 2. Startup container with shared folder

```sh
docker run -it -v {local_shared_folder}:/pub emedeiros/asciidoctor
```

## 3. Startup container with shared folder and nginx (webserver)

### 3.1 Startup container

```sh
docker run -it -p 8080:80 -v {local_shared_folder}:/pub/ emedeiros/asciidoctor
```

### 3.2 Start nginx

```sh
nginx
```

### 3.3 Access your document

Open your browser and type the url: 

```sh
http://docker.ip:8080/asciidoctor/{file.html}
http://docker.ip:8080/asciidoctor/{file.pdf}
```


## TIPS:

### Save your documments on /pub directory

### Convert adoc document to html

```sh
asciidoctor example.adoc
```

### Convert adoc document to pdf

```sh
asciidoctor-pdf example.adoc
```

Any question or sugestion? post here.