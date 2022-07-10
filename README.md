# jax-guided-diffusion
jax version of clip guided diffusion scripts

Change Log (last updated 2022.06.03)

(1) automated stitching

(2) masked mse (inpainting)

(3) noise injects

(4) vitl14 336px

(5) updated as_cutout_image() to remove gray borders

(6) fixed print_time_remaining()

(7) changed run loop to fix resume_stitching and init errors

(8) added display_init


<B>Automated Stitching (AS)

Is a method for piecing together diffusion renders into larger images
A larger target image is selected and divided into a grid of smaller images (edited)
Each smaller image is loaded into the notebook as an initial image
We perform clip guided diffusion on each initial image (like normal) and stitch the result back into the larger target image.In the end we are left with a stitched image that is larger in size than what is normally possible with low VRAM GPUs

— Huemin </B>

The notebook has a section that you can visualize the above tile/grid pattern that you define based upon your tile/grid settings and final output image resolution under the Test Automated Stitching section.



