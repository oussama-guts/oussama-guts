from PIL import Image, ImageDraw, ImageFont

# Create an image with a white background
width, height = 400, 200
image = Image.new('RGB', (width, height), (255, 255, 255))

# Draw a black rectangle as the shirt
draw = ImageDraw.Draw(image)
draw.rectangle((50, 50, 350, 150), fill=(0, 0, 0))

# Add the brand name to the shirt using a font
font = ImageFont.truetype('arial.ttf', 24)
draw.text((100, 75), 'Brand Name', font=font, fill=(255, 255, 255))

# Save the image as a PNG file
image.save('brand_shirt.png')
