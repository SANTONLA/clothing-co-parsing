Clothing Co-Parsing (CCP) Dataset
================================
📌 **Introducción**
Ahora que entendemos en qué consiste la segmentación semántica y las numerosas aplicaciones que tiene, veamos cómo abordar este problema utilizando redes neuronales convolucionales (CNNs).

💡 **Aprendizaje Supervisado**
Primero, es importante destacar que la segmentación semántica se trata como un problema de aprendizaje supervisado. Esto significa que para entrenar los modelos necesitamos disponer de imágenes junto con sus segmentaciones ideales.

📊 **Caso de Estudio: Dataset Clothing Co-Parsing (CCP)**
Para ilustrar esto y los demás conceptos en este notebook, nos enfocaremos en un problema específico utilizando el dataset Clothing Co-Parsing (CCP). Este dataset está diseñado para la segmentación semántica de prendas de vestir. Contiene 2,098 imágenes de alta resolución tomadas en entornos abiertos, principalmente urbanos. De estas, 1,004 imágenes han sido etiquetadas con 59 etiquetas que cubren una amplia variedad de prendas de vestir, accesorios, etc.

![CCP example](https://raw.githubusercontent.com/bearpaw/clothing-co-parsing/master/example.jpg)

Clothing Co-Parsing (CCP) dataset is a new clothing database including elaborately annotated clothing items.

  - 2, 098 high-resolution street fashion photos with totally 59 tags
  - Wide range of styles, accessaries, garments, and pose
  - All images are with image-level annotations
  - 1000+ images are with pixel-level annotations

Feel free to contact `platero.yang (at) gmail.com` should you have any suggestions or questions.

Please visit the [project page](http://www.sysu-hcp.net/clothing-co-parsing-by-joint-image-segmentation-and-labeling/) for more information.

Files
-----
Root directory contains following files and folders:
  - photos/                     - directory of original photos
  - annotations/                - directory of annotations
  	+ pixel-level/              - pixel-level annotations (1004 files)
  	+ image-level/              - image-level annotations (1094 files)
  - show_pixel_anno.m           - demo code for using pixel-level annotations
  - show_image_anno.m           - demo code for using image-level annotations 	
  - label_list.mat              - [1*59] cell array which maps label numbers to label names
  - samples.jpg                 - sample annotations
  - README.md                   - this file

Usage of the Database
---------------------
Please refer to `show_pixel_anno.m` and `show_image_anno.m` for detailed usage.

Notes on Image-Level Annotations
--------------------------------
Each annotation is saved in `annotations/image-level/` as a matlab `.mat` file, which is a variable
- tags: [n*1] matrix denotes the tags of the photo, where n is the number of the tags contained in the specific photo. 

Notes on Pixel-Level Annotations
--------------------------------
Each annotation is saved in `annotations/pixel-level` as a matlab `.mat` file, which is a variable

- groundtruth: [h*w] matrix denotes the annotated labels of pixels

Citation
--------
If you make use of the Clothing Co-Parsing (CCP) data, please cite the following reference in any publications:
```bib
@inproceedings{yang2014clothing,
  title={Clothing Co-Parsing by Joint Image Segmentation and Labeling},
  author={Yang, Wei and Luo, Ping and Lin, Liang}
  booktitle={Computer Vision and Pattern Recognition (CVPR), 2014 IEEE Conference on},
  year={2013},
  organization={IEEE}
}
```
