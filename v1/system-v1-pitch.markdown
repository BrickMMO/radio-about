<style>@import url("//readme.codeadam.ca/readme.css");</style>

## Pitch: Project Name: Version #1

Date: <MONTH> <DAY>, <YEAR>
Domain: <DOMAIN_NAME>  
GitHub: https://github.com/codeadamca/<REPO_NAME>

## Application Purpose

This application will convert a provided image to a set of instructions to recreate the image using LEGO™ bricks.

The end result will be instructions to create something similar to the [LEGO™ World Map](https://www.lego.com/en-us/product/world-map-31203):

![Sample Map](../images/v1-map.png)

### Front-End

Front end facing application will include the following features:

- A place to upload an image, specify width and height, and convert the image to a series of LEGO™ bricks (similar to [https://legoimage.com/ or https://mingze-gao.com/apps/legao/](https://legoimage.com/ or https://mingze-gao.com/apps/legao/))
- Resulting image can be downloaded as a JPG
- Result will also display a list of required bricks and quantity, should be styled like typical LEGO™ instructions
- Results will also display a copyable matrix of colours
- Instructions can be downloaded as a PDF
- Each submission will be saved to the database

Instructions will look similar to this:

![Sample Instructions](../images/v1-instructions.png)

Taken from the World Map LEGO™ instructions:  
[https://www.lego.com/cdn/product-assets/product.bi.core.pdf/6372756.pdf ](https://www.lego.com/cdn/product-assets/product.bi.core.pdf/6372756.pdf)

### Back-End

Application will include a control panel to achieve the following:

- Login to control panel
- Add, edit, and delete converted images
- View instructions
- Export instructions to PDF

### API

Application API will include the following API calls:

| Method | Endpoint     | Description                                                                                                                                                                                                                                                                                                                                                                      |
| ------ | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| POST   | /api/convert | Converts a specified image to a matrix of LEGO™ colours.<br><br>Parameters:<br>image (required): posted<br>JPG, PNG, or GIF<br>width (required): number of studs wide<br>heigh (required)t: number of studs high<br>format: format to return data in, default is "json"but also accepts "jpg"<br><br>Returns:<br>A matrix of colours for each LEGO™ brick or a JPG format image. |

[&#10132; Back to Version 1](/template-about-markdown/v1)

---

<a href="https://brickmmo.com">
<img src="https://brickmmo.com/images/brickmmo-logo-horizontal.jpg" width="100">
</a>
