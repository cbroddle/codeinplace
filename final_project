""" 
Videochat background image picker program.
---
Background Picker asks the user a series of questions to pick a background 
to use for video chat and group sessions. 
---
Background images are from Unsplash and resized to 1920px by 1080px (16:9 aspect ratio).
""" 

from simpleimage import SimpleImage

def main():

    #1) User answers questions to choose image
    chosen_image = choose_image()
    chosen_image.pil_image.save('chosen_image.jpg')
    chosen_image.show()
    #2) A dark filter is added to the final image choice
    final_image = add_filter(chosen_image)
    final_image.show()
    

def add_filter(chosen_image):
    final_image = SimpleImage('chosen_image.jpg')
    for pixel in final_image:
        pixel.red = pixel.red - 50
        pixel.green = pixel.green - 50
        pixel.blue = pixel.blue - 50
    
    return final_image

def choose_image():
    modern = SimpleImage('modern.jpg')
    bohemian = SimpleImage('bohemian.jpg')
    minimalist = SimpleImage('minimalist.jpg')
    mountains = SimpleImage('mountain.jpg')
    beach = SimpleImage('beach.jpg')
    desert = SimpleImage('desert.jpg')

    print("Let's get started!")
    print("Press the ENTER key after typing each response.\n")

    setting = input("Do you prefer an indoor or outdoor setting?\n")
    if setting.lower() == "indoor":
        print("Of the following decor styles, which do you prefer?")
        style = input("Modern, Bohemian, Minimalist\n")
        if style.lower() == "modern":
            return modern
        elif style.lower() == "bohemian":
            return bohemian
        elif style.lower() == "minimalist":
            return minimalist
    elif setting.lower() == "outdoor":
        print("Of the following settings, which do you prefer?")
        out_setting = input("Mountains, Beach, Desert\n")
        if out_setting.lower() == "mountains":
            return mountains
        elif out_setting.lower() == "beach":
            return beach
        elif out_setting.lower() == "desert":
            return desert
    
        
if __name__ == '__main__':
    main()
