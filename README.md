# STEPIN-Project_302388
# Title : Chess Board using C programming
# Prerequisite:

In Computer Graphics, we use graphics.h which provide direct functions to draw different coordinate shapes(like circle, rectangle etc). By using these functions we can draw different objects like car, hut, trees etc. In this program, the task is to draw a Chess Board using the functions in graphics.

# Approach: 

We will create a Chess Board with the help below functions:

1.rectangle(left, top, right, bottom): A function from graphics.h header file which is used to draw a rectangle. Coordinates of the left top and right bottom corners are required to draw the rectangle. left specifies the X-coordinate of the top left corner, top specifies the Y-coordinate of the top left corner, right specifies the X-coordinate of the right bottom corner, bottom specifies the Y-coordinate of the right bottom corner.

2.delay(): This function is present in library “dos.h” is used for holding the program output for a small period of time since processing is very fast so use it to see the result.

3.setcolor(): A function from graphics.h header file which sets the color of the pointer (cursor). There are some predefined colors in computer graphics. Here n is the color number.

4.setfillstyle(): A function from graphics.h header file which sets the current fill pattern and fill color.

5.floodfill(): A function from graphics.h header file which is used to fill an enclosed area.

|Build|Unit Test|cppcheck|Valgrind|Codacy|Coverage|
|:--:|:--:|:--:|:--:|:--:|:--:|
|[![C-Build](https://github.com/jagadeesharadhyula7608/Stepin_MiniProject_256282/actions/workflows/c-build.yml/badge.svg)](https://github.com/jagadeesharadhyula7608/Stepin_MiniProject_256282/actions/workflows/c-build.yml)|[![Unit_Testing](https://github.com/jagadeesharadhyula7608/Stepin_MiniProject_256282/actions/workflows/unit_test.yml/badge.svg)](https://github.com/jagadeesharadhyula7608/Stepin_MiniProject_256282/actions/workflows/unit_test.yml)|[![Cpp_Check](https://github.com/jagadeesharadhyula7608/Stepin_MiniProject_256282/actions/workflows/cpp-check.yml/badge.svg)](https://github.com/jagadeesharadhyula7608/Stepin_MiniProject_256282/actions/workflows/cpp-check.yml)|[![Valgrind](https://github.com/jagadeesharadhyula7608/Stepin_MiniProject_256282/actions/workflows/Valgrind.yml/badge.svg)](https://github.com/jagadeesharadhyula7608/Stepin_MiniProject_256282/actions/workflows/Valgrind.yml)|[![Codacy Badge](https://app.codacy.com/project/badge/Grade/3ac7e2a959a24fa4b5d1b9c1c886ff75)](https://www.codacy.com/manual/stepin654321/MiniProject_Template?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=stepin654321/MiniProject_Template&amp;utm_campaign=Badge_Grade)|[![Code-Coverage](https://github.com/jagadeesharadhyula7608/Stepin_MiniProject_256282/actions/workflows/coverage.yml/badge.svg)](https://github.com/jagadeesharadhyula7608/Stepin_MiniProject_256282/actions/workflows/coverage.yml)|

![chessGfg](https://user-images.githubusercontent.com/83154833/125827562-22e6695a-e58e-4179-85ee-85c2307e7e35.png)

# Folder Structure

   | Folder	| Description |
   |-------|-------------|    
|1_Requirements	| Documents detailing requirements and research|
|2_Design |Documents specifying design details|
|3_Implementation| All code and documentation|
|4_Test_plan&Output|Documents with test plans and procedures|
|5_Report| Documents with overall report|
|6_ImagesAndVideos|Related Videos and images regarding project|
|7_Other|Related other documents|


# GitHub Actions

Build using Make for CI

Unit tests with Cunit

Static code analysis using cppcheck

Dynamic code using Valgrind

Code Quality using Codacy

