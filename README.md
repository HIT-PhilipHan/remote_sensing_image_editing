
# Introduction
Artificial Intelligence Generative Content (AIGC) technologies have significantly influenced the remote sensing domain, particularly in the realm of image generation. However, remote sensing image editing, an equally vital research area, has not garnered sufficient attention. Different from text-guided editing in natural images, which relies on extensive text-image paired data for semantic correlation, the application scenarios of remote sensing image editing are often extreme, such as forest on fire, so it is difficult to obtain sufficient paired samples. At the same time, the lack of remote sensing semantics and the ambiguity of text also restrict the further application of image editing in remote sensing field. To solve above problems, this letter proposes a diffusion based method to fulfill stable and controllable remote sensing image editing with text guidance. Our method avoids the use of a large number of paired image, and can achieve satisfactory image editing results using only a single image. The quantitative evaluation system including CLIP score and subjective evaluation metrics shows that our method has better editing effect on remote sensing images than existing image editing models. \textcolor{red}{Additionally, we use the generated edited images to support a disaster assessment mission to determine whether a building was destroyed by a tsunami and obtain excellent experimental results. 

# Contributions
1. The training of DDPMs specially designed for remote sensing image editing often hinges on a substantial volume of samples with semantic information to be edited, which are often insufficient.
2. The existing text-guided image editing model relies on text-image pre-training models trained on nature images and lacks the semantic understanding specific to remote sensing tasks.
3. Incorporating a text-guided image editing model often leads to semantic confusion due to the ambiguity inherent in the text, resulting in illogical generation outcomes.

# Expriments
We evaluate our text-guided remote sensing image editing model through two editing scenarios. First, when comes to the scenario where the type of ground objects is homogeneous and the overall editing is required, we adopt the method of directly repainting the whole image through text guidance to edit the image. Secondly, in the scenario where the types of ground objects are complex and the editing of local areas needs to be refined, we edit it by combining the text guidance and ROI region mask.The images before and after editing are compared as follows:

![full_image_edit](/asserts/full_image_edit.png)

![impaiting_image_edit](/asserts/impainting_image_edit.png)

To validate the quality of the edited images quantificationally, we also use CLIP score and a subjective evaluation metric to compare the generation results.
