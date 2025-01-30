Electronics is an Interesting subject (175 points)

This is the script for encryption
from PIL import Image






def changeImage():
   # open the image you want to encode data to
   image = Image.open('TEK0000.JPG')
  
   # This the string that will be encoded into the image
   flag = 'hacks{eAsY_Pe4Sy}'


   # a list to hold the tuples of pixels for the new image
   newImageData = []


   # count for looping around
   count = 0


   # COLOR is a tuple of RGB value data for each pixel
   for color in image.getdata():
      
       blue = (ord(flag[count]) + 13) % 256
       # creates a new RGB tuple with the ord value of the char from the flag string
       newPixel = (color[0], color[1], blue)
      
       # Appends the tuple to the list
       newImageData.append(newPixel)


       # used for wrapping back around the flag
       count += 1
       if count == len(flag):
           count = 0


   # creates a new IMAGE object with the same mode and size as the original
   newImage = Image.new('RGB', image.size)
  
   # Copies pixel data to the image
   newImage.putdata(newImageData)


   # Writes new image to disk
   newImage.save('test.png','PNG')


if __name__ == '__main__':
   changeImage()



This is the script for decryption: 
from PIL import Image


def extractMessage():
   # Open the encoded image
   image = Image.open('test.png')


   # Initialize an empty string to store the extracted message
   extracted_message = ""


   # Loop through the blue channel of each pixel
   for color in image.getdata():
       blue = color[2]  # Extract the blue channel


       # Reverse the encoding transformation: (blue - 13) % 256
       extracted_char = chr((blue - 13) % 256)


       extracted_message += extracted_char


       # Stop extraction if we detect a closing `}`
       if extracted_message.endswith("}"):
           break


   print("Extracted Message:", extracted_message)


if __name__ == '__main__':
   extractMessage()
