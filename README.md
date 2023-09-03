# Lennard's Cookbook

Lennard's cookbook is a LaTex package that provides functions to create simple and clean recipe books.

# How to install

Copy the .sty file into your LaTex packet folder or directly into the directory of the LaTex document you want to use the packet in. Afterwards you can load the packet by using \usepackage{lennardscookbook} in the preamble.

# How to use

## Packet loading

Load the package with \usepackage{lennardscookbook}. The default language is english with degrees Celsius as the temperature unit.

- To change the language to german, specify \usepackage[german]{lennardscookbook}
- To change the temperature unit to Fahrenheit, specify \usepackage[tempunit=F]
- Both parameters can also be combined: \usepackage[german,tempunit=C]

## Recipe environment

- Import the packet as described above and create a recipe environment with \begin{recipe} ... \end{recipe}. Within the environment, pictures, information and steps can be added.
- Commands:
  - \rtitle{My First Recipe} sets the title
  - \rtwoimages{path_to_image1}{path_to_image2} defines two images that will be shown below the title next to each other
  - \rimage{path_to_image} defines only one image to be shown below the title
  - \rtime{duration} sets the time needed for preparation and cooking
  - \roven{SYMBOL}{temperature}{duration} to specify the mode, temperature and time for oven usage
  - \rovenalt{SYMBOL}{temperature}{duration} to specify an alternative option for oven usage
  - \rportions{amount} to specify the amount of portions
  - \source{name} to specify a source where you got the recipe from
  - \ringredientlist{ ... } to define the list of ingredients
    - Use \ringredient{amount}{unit}{name} commands within the list to define ingredients
    - For sectioning, you can use \ringredientsection{Name of Section}{ ... } within the list for further sectioning. In that case, you need to place the \ringredient commands within the body of the section command.
  - \rsteps{ ... } to define the steps to follow (preparation). For every step, define "\step TEXT" in \rsteps.
  - Except \rtitle and \rsteps, all other definitions are optional

The file recipe_example.tex gives an examle and shows how to use and place the commands.

## Demonstration

Please refer to the Wiki page on Github.
