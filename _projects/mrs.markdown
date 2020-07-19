---
layout: page
title: MRS
description: tools for magnetic resonance spectroscopy
img: /assets/img/vps-e1508119269104.png
importance: 3
github: https://github.com/rhancockn/mrs_voxel_positioning
---

## Planning SVS
The [VOI Planning System (VPS)](https://github.com/rhancockn/mrs_voxel_positioning) is a tool prototyped as a ParaView pipeline for interactively placing bounding boxes on a 3D volume, intended as an aid for planning single voxel magnetic resonance spectroscopy (MRS) experiments.

VPS allows you to easily evaluate the feasibility of different voxel geometries based on expected field homogeneity, tissue fractions, and ROI content of a voxel. The desired geometry can then be saved as a transform that can be aligned to individual anatomy and/or entered directly into the scanner console to support systematic voxel placement across participants. Notably, this supports oblique voxel orientations around any axis.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/vps_1.png' | relative_url }}" alt="" title="VPS interface"/>
    </div>
</div>
<div class="caption">VPS interface</div>


## DICOM Processing

The [autovps](https://github.com/rhancockn/autovps.git) package includes utilities for manipulating MRS data, primarily Siemens DICOM format.

Features:

- Extract FID data from DICOMs and export to a FID-A Matlab structure
- Generate a VOI mask on a T1w or other volume
- Convert transform matrices to a voxel prescription (for Siemens)  

