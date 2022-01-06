# Creating high resolution vector art for manuscripts using Powerpoint 

Powerpoint is a less capable, but quick alternative to creating high resulution vector images for manuscricpts compared to more powerful programs such as Illustrator or Inkscape. The following tips may be used to make high reslution figures even for initial submissions.
 
### 1. Copy MATLAB figures as vector art
- When using MATLAB figures in powerpoint, make sure to copy as vector graphic (see image below). Then paste the image in a powerpoint slide (make sure to simply paste and *not* paste as a picture.

![image](https://user-images.githubusercontent.com/79334732/148457080-57d493f0-55ed-4f35-951a-2b0cf1f9bef5.png)

### 2. When the MATLAB figure to be copied is a surface plot or 3-D plot, copying as vector graphic may not work. 
- In such cases, use the `print` command to export the plot as a PNG at a high resolution (usually 1200 dpi or more) so that the details are reasonably preserved when zoomed in. 
- The following command can be added to the script to generate a high resolution PNG.
- `print(gcf,['output.png'],'-dpng','-r1200')`
- The number following `-r` sets the output resolution and may be modified as needed.
  
### 3. Most art or text created using the tools in powerpoint can be exported as vector art. 
- It is often easier to add annotations such as axis labels, ticklabels, etc. within powerpoint after scaling the images from MATLAB appopriately.
- Note that shape/text effects such as shadows, reflections, etc. may not export well as vector art (if anyone knows how to do this, please suggest!).
- Similarily, raster images (such as those in PNG,JPG,BMP formats) will not get converted to vector art no matter what you do within powerpoint. Download and use a high resolution image instead.

### 4. Once the figure is created within powerpoint, there are two options to export it as vector art
- **PDF export for LaTeX or standalone figure files**: First change the slide size to match the figure dimensions and then save the current slide as a PDF. This preserve the vector elements and will allow to generate figure PDFs that can be then submitted directly or used in LaTeX.
- **EMF export for MS Word**: Select (or group) all elements in the powerpoint slide that are part of the figure and then save them as a picture in EMF format (Right click --> Save as Picture). Do NOT save as SVG. Then insert the saved EMF files inside the word document (Insert --> Pictures --> This Device). Save the word document as PDF and this will preseve the vector art in figure elements.
