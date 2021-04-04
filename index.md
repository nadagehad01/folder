# Nada Galal
#### Click [here](https://drive.google.com/file/d/1tbphR8kmyYPuSg8CLP7bACFbI2jLU9XA/view?usp=sharing "Nada's resume") for my resume.

Hello! My name is Nada (she/her). I'm a class of 2023 student at UCSD majoring in computer science and minoring in design and business. I'm currently also a computer science tutor in the computer science department, a middle school mentor with an organization called [CovEd](coved.org "CovEd website"), and a publicity, social media, and monthly newsletter intern at the [Diversity, Equity, and Inclusion community](https://cse.ucsd.edu/diversity_equity_inclusion "DEI community website") in the UCSD computer science department. Check out the rest of this page to know more about my [educational background](https://github.com/nadagehad01/110/blob/main/index.md#about-my-educational-background "educational background") and [tutoring](https://github.com/nadagehad01/110/blob/main/index.md#about-my-tutoring "tutoring") experience!

#### About my educational background
* Graduated high school in 2019 from Riada American School in Alexandria, Egypt
* Currently a B.S. student at the University of California, San Diego planning to graduate in 2023
  * Major: Computer Science
  * Minors:
    * Design (with a focus on interaction design)
    * Business


#### About my tutoring
I have a great passion for teaching. I was an elementary school tutor when I was in high school, I mentored students in underserved areas in Egypt and helped design their curriculums, and I became a computer science tutor for the first time in January of 2021. I tutored for CSE 8B (_Introduction to Programming and Computational Problem-Solving II_) with Professor Christine Alvarado, and I'm currently tutoring for CSE 30 (_Computer Organization and Systems Programming_) with Professor Bryan Chin. In March of 2021, I joined an organization called CovEd as a volunteer mentor to mentor for students in Chicago Heights Middle School.

#### Some of my skills
1. Programming in `Java`, `C`, `C++`, `Python`
2. Design
3. Problem Solving
4. Speaking Arabic, English, and some French

#### Other
__My career goals:__
* [ ] succeed in the industry in a job that allows me to blend and make use of my design skills and my problem solving skills
* [x] always be teaching on the side
* [ ] contribute to the making of an animation movie (ideally a Disney movie)

**Some fun:**
A staff member who graded a programming assignment of mine in my first programming class (CSE 8A) commented on my submission
> If you explain more on how you achieve vibrance I would have given you the star point :) I think you did something really cool here, you should include it on your github account if you have one.

However, I never included the code on my github because I didn't know how to use it. Now that I'm using it, thanks to CSE 110, here is the vibrance method the grader was referring to:
```Java
    public static Image vibrance(Image img, int level){
      Color[][] imgArr = img.getPixels2D();
      //these variables track which color component is more frequently bigger in the array of colors
      int moreRedCount = 0;
      int moreGreenCount = 0;
      int moreBlueCount = 0;
      //this nested loop increases a color's component if it's bigger than the other 2 components in every pixel
      for (int row = 0; row < img.getHeight(); row++){
        for (int col = 0; col < img.getWidth(); col++){
          Color currPixel = imgArr[row][col];
          int red = currPixel.getRed();
          int green = currPixel.getGreen();
          int blue = currPixel.getBlue();
          if (red > green && red > blue){
            red += level;
            moreRedCount += 1;
          }
          else if (green > blue && green > red){
            green += level;
            moreGreenCount += 1;
          }
          else if (blue > red && blue > green){
            blue += level;
            moreBlueCount += 1;
          }
          //these if statements ensure that a color component doesn't go out of bound
          if (red > 255){
            red = 255;
          }
          if (green > 255){
            green = 255;
          }
          if (blue > 255){
            blue = 255;
          }
          if (red < 0){
            red = 0;
          }
          if (green < 0){
            green = 0;
          }
          if (blue < 0){
            blue = 0;
          }
          imgArr[row][col] = new Color (red, green, blue);
        }
      }
      //this nested loop deals with pixels that have equal amount of color in every component
      //it increases the number of the most frequently bigger color component in white/gray/black pixels
      for (int row = 0; row < img.getHeight(); row++){
        for (int col = 0; col < img.getWidth(); col++){
          Color currPixel = imgArr[row][col];
          int red = currPixel.getRed();
          int green = currPixel.getGreen();
          int blue = currPixel.getBlue();
          if (red == green && red == blue){
            if (moreRedCount > moreGreenCount && moreRedCount > moreBlueCount){
              red += level;
            }
            else if (moreGreenCount > moreRedCount && moreGreenCount > moreBlueCount){
              green += level;
            }
            else if (moreBlueCount > moreRedCount && moreBlueCount > moreGreenCount){
              blue += level;
            }
          }
          //these if statements ensure that a color component doesn't go out of bound
          if (red > 255){
            red = 255;
          }
          if (green > 255){
            green = 255;
          }
          if (blue > 255){
            blue = 255;
          }
          if (red < 0){
            red = 0;
          }
          if (green < 0){
            green = 0;
          }
          if (blue < 0){
            blue = 0;
          }
          imgArr[row][col] = new Color (red, green, blue);
        }
      }
      Image newImg = new Image(imgArr);
      return newImg;
    }
```
Additionally, [this]( "submission") is a link to my entire submission, and [this](https://www.google.com/url?q=https://drive.google.com/open?id%3D1oP2t_aYbAYIl2k-xlZwsUkywcfBjFfg9nJETNeFUV1o&sa=D&source=editors&ust=1617553838112000&usg=AFQjCNE9IXNU88hMVBn8f-tf8OGvTp8jLQ "writeup") is a link the programming assignment's writeup.

In case you haven't had enough of my fantastic solution to the programming assignment, check out [this collage](/fantastic.jpg "collage") I made with the filters I created.

__Home:__
I'm from Egypt, and I really enjoy exploring my hometown and different places in Egypt, so here are some shots I took while doing that!

![egy](egy.png "the shots")




