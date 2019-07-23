+++
date = "2019-03-14T19:02:13-04:00"
title = "Overview"
linktitle = "Overview"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Data"

+++

# Mapping file

A records file is provided which provides useful information, including:

* a mapping between the image (dicom_id), the study (study_id), and the patient (subject_id)
* the view position of the image
* the orientation of the patient in the image

Images are provided in DICOM format; see the [image](/image) section for more information about the images.

Reports are provided as plain text files; see the [reports](/reports) section for more information about the reports.

# Data Organization

Data files are made available in a hierarchical strcture.
The following block lists first patient's records as an demonstrative example (MIMIC-CXR v2.0.0):


```
files/
 p10000032/
  s50414267/
    02aa804e-bde0afdd-112c0b34-7bc16630-4e384014.dcm.gz
    174413ec-4ec4c1f7-34ea26b7-c5f994f8-79ef1962.dcm.gz
  s53189527/
    2a2277a9-b0ded155-c0de8eb9-c124d10e-82c5caab.dcm.gz
    e084de3b-be89b11e-20fe3f9f-9c8d8dfe-4cfd202c.dcm.gz
  s53911762/
    68b5c4b1-227d0485-9cc38c3f-7b84ab51-4b472714.dcm.gz
    fffabebf-74fd3a1f-673b6b41-96ec0ac9-2ab69818.dcm.gz
  s56699142/
    ea030e7a-2e3b1346-bc518786-7a8fd698-f673b44c.dcm.gz
  s50414267.txt
  s53189527.txt
  s53911762.txt
  s56699142.txt
 ...
 ```

 Above, this patient (`10000032`) has four studies. Most of the studies have two scans (a frontal and lateral), but one study `56699142` has only one image.
 Each study is associated with a de-identified free-text radiology report (e.g. s56699142.txt).
 Note that the identifiers are random, and do not indicate order of the studies in any way.