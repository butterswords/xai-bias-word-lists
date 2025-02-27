# xai-bias-word-lists
Welcome. This is a repository for storing word lists around Sexual Orientation and Gender Identity (SOGI), race (names and descriptors), professions, countries, and additional protected attributes as I am able to build them out (ex. religion, disability status, age, sexual orientation, etc.). I am using these to test for bias in language models, and I believe it is more broadly applicable within NLP, AI research, and beyond. 

## Intention
I am making it public for several reasons:
* **Accessibility** - I haven't found ready-to-use lists as I've been trying to build so I feel there's a need to make more publicly accessible and discoverable
* **Representation** - More importantly, any word lists used by researchers should be informed by, if not directly driven by, the communities they intend to support. 
  * It is often easier to react to something that exists so I intend to make this a public project open to contributors from all walks of life and invite people to critique the logic, sources, and final lists
* **Reproducability** - For research, and tools, to be useful broadly the work has to be reproducable. My hope is that providing this base data helps make other projects easier to build and reproduce results.
* **Transparency** - Making this an open project means it can be shared with anyone who chooses to collaborate on projects I'm working on. They can see what I'm working with and determine if they feel it works for them.
* **Learning** - For those starting their journey this may serve as a guide to help them do similar work. For those who are more advanced, I hope they will point out where the code is weak or inefficient so that contributors can learn how to do it better.

> **Note**
> If repositories, data sets, or other projects exist that are driven by members of affected communities then let me know by DMing me or opening an issue. I will happily promote and share their work to ensure I am centering my focus on community driven efforts.

### Note on positionality
I am Nathan Butters, and I created this repository. I want to take a moment to address my positionality so that anyone who interacts with this work understands where I'm coming from.

> I am a cis-gender, straight, white man from the United States. I do not wish to impose hierarchy, taxonomy, or otherwise discretize the lived experience of others. It's not my place to do so. To do NLP and evaluate models, I need to use words that represent human experience, and so I am doing what I can to make my data worthy of use.

For a more thorough explanation of my positionality read my [About Me](https://butterswords.github.io/portfolio/about/) page.

## Focus with sources

### Current Focus Areas
These are the main areas for this project at the start. Some may prove intractable, and exploring what makes them so may help communities find ways to provide feedback into systems.

- [x] Country Names
- [x] Professions
- [x] Sexual Orientation & Gender Identity (SOGI)
- [x] Names 
- [x] Race (basic descriptors)
- [ ] Religion
- [x] Age
- [ ] Marital Status
- [ ] Health Status (Disability, Pregnancy, etc.)
- [ ] Language (AAE vs ES)

### Country
I decided to ground my work through multiple sources. I ended up choosing the United Nations Statistical Division's [Overview](https://unstats.un.org/unsd/methodology/m49/overview/) to ground me in something public that could be used the world over.

Then I started to think about secondary data that might be useful for exposing the bias in an algorithm and opted for the [World Happiness Report 2021](https://worldhappiness.report/ed/2021/#appendices-and-data). I added the continents to the countries in that file to allow for simple categorization.

### Professions
The US Bureau of Labor Statistics provides a solid starting point for an expansive list of titles. This data can be found at [Standard Occupational Classifications in 2018](https://www.bls.gov/soc/2018/home.htm). Specifically, I made use of their [Direct Match Title File](https://www.bls.gov/soc/2018/home.htm#match), because it provides SOC categories.

### Names

**Data Source**
* [US Census 1990](https://www.census.gov/topics/population/genealogy/data/1990_census/1990_census_namefiles.html) to get names from Census.
* Future Opportunity - [DIME Race 1980-2014](https://dataverse.harvard.edu/dataset.xhtml;jsessionid=be9768bb2b804582647d35d80e62?persistentId=doi%3A10.7910%2FDVN%2FM5K7VR&version=&q=&fileTypeGroupFacet=&fileAccess=&fileSortField=date)

**Tools and Libraries that might allow for extension to racial dimensions**
* [Ethnicolr](https://pypi.org/project/ethnicolr/): Use this to predict the race of the artificial names generated.
* [DIME Race](https://github.com/appeler/dime_race): Provides several useful Jupyter Notebooks to see how we could build our own counterfactuals with racial inference

Note: the inference of race from names is problematic and prone to biases in the training data. If you choose to use any of these tools, do so with care.

#### Racial Descriptors
I have gathered a simple list of racial descriptors from several public sources, though the list focuses primarily on country or region of origin as the key descriptor.

### Sexual Orientation and Gender Identity
I focused on sources that explicitly aim to be inclusive and are generated by people within the 2SLBGTQIA+ community. I am sure I have missed much, and am open to expanding the sources as I learn more.

**Data Sources*
* [Non-Binary Wiki](https://nonbinary.wiki/wiki/Glossary_of_English_gender_and_sex_terminology)

## Using and contributing to this work

### Implementation Guide

> **Note**
> This needs to be written once I have usable data in a format I'm ready to version. It will likely be as simple as importing the data with a `request` and then unzipping the file. We'll see.

### Contributing to this work
To start I think opening up an issue or a pull request will be the best way to contribute. I will also field messages directly to me, on Github or [LinkedIn](https://www.linkedin.com/in/nathanbutters), to protect contributors' decision rights and privacy.


### Citing this work
If you use this data, please cite it in your work. As more people contribute I will ensure they are added to the entry; I may instead remove myself as an author and highlight the communal nature of the project.

Bibtex
```
    @misc{Butters_XAI_Bias_Word,
    author = {Butters, Nathan},
    title = {{XAI Bias Word Lists for NLP}},
    url = {https://github.com/butterswords/xai-bias-word-lists}
    }
```
