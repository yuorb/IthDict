# IthDict
New Ithkuil Dictionary (ITH-ENG) in [XDXF](https://github.com/soshial/xdxf_makedict) format.

XDXF specifies a semantic format for storing dictionaries.

![state](https://img.shields.io/badge/STATE-In%20Progress-green)
![version](https://img.shields.io/badge/VERSION-0.0.1-red)
![root](https://img.shields.io/badge/ROOT-v0.5.1-informational)
![affix](https://img.shields.io/badge/AFFIX-v1.0-informational)
![grammar](https://img.shields.io/badge/GRAMMAR-v1.2-informational)

TODO:
- [ ] Roots
  - [x] ROOTS ASSOCIATED WITH ITHKUIL GRAMMATICAL FUNCTIONS
  - [ ] COMMON STATES AND ACTS
  - [ ] SPACETIME and MOTION
  - [ ] PSYCHOLOGICAL AND SOCIOLOGICAL PHENOMENA
  - [ ] MISCELLANEOUS ENTITIES AND OBJECTS
  - [ ] NATURE AND NATURAL PHENOMENA (Non-Biological)
  - [ ] NATURAL PHENOMENA (BIOLOGICAL/ZOOLOGICAL)
- [ ] Affixes
  - [x] Demonstrative, Determinative, and Deictic Affixes
  - [ ] Sequential/Temporal Affixes
  - [ ] Spatial, Positional, and Motion Affixes
  - [ ] Quantifying Affixes
  - [ ] Qualifying Affixes
  - [ ] Adverbial Affixes
  - [ ] Modality Affixes
  - [ ] Agential/Participant Affixes
  - [ ] Affixes Relating to Bodily Position
  - [ ] Instrumentative/Utilitative Affixes
  - [ ] Configurative Affixes
  - [ ] Affixes Relating to Meta-Level Qualification
  - [ ] Sensory Affixes
  - [ ] Affixes Relating to Mathematics and Measurement
  - [ ] Coordinative and Connective Affixes
  - [ ] Grammatical Affixes
  - [ ] Affixes for Biological Genera, Species and Sub-Species Differentiation
  - [ ] Miscellaneous Affixes
- [ ] Grammatical Categories and Definitions 

feel free to pull requests :3

# Usage

Place the folder `ithdict2023` under the dictionary folder of [GoldenDict](https://github.com/xiaoyifang/goldendict/releases) or other compatible software.

Search `contents` for a catalog

![image](https://user-images.githubusercontent.com/12672523/212417016-2e77cfa5-f8f3-4574-9a28-5795e8a328a1.png)

Info is obtained by entering keywords (letters or abbreviations) in black. 

![image](https://user-images.githubusercontent.com/12672523/212417506-a2a70334-3fb0-4b89-8bf4-46b8c00b4a3f.png)

Equivalent of Wiktionary categories

![image](https://user-images.githubusercontent.com/12672523/212418132-90fe6d76-40c4-44f6-b87b-b05aedac9da5.png)

# For Developers

## Templates

Each lexical item is within the <ar>…</ar> tags.

At least these three parts are included in each article：

1. <k>key</k>
2. <def>definition</def>
3. <categ>category</categ>

Other parts are optional.

An article for a normal root may include the following parts:

```
        <ar>
            <k>
                <opt>-</opt>
                the root's value
                <opt>-</opt>
            </k>
            <def>
                <def>
                    <gr>
                        <abbr>S0</abbr>
                    </gr>
                    <gr>the root's semantic notion</gr>
                    <def>
                        <gr>
                            <abbr>BSC</abbr>
                        </gr>
                        <deftext>...</deftext>
                    </def>
                    <def>
                        <gr>
                            <abbr>CTE</abbr>
                        </gr>
                        <deftext>...</deftext>
                    </def>
                    <def>
                        <gr>
                            <abbr>CSV</abbr>
                        </gr>
                        <deftext>...</deftext>
                    </def>
                    <def>
                        <gr>
                            <abbr>OBJ</abbr>
                        </gr>
                        <deftext>...</deftext>
                    </def>
                </def>
                <def>
                    <gr>
                        <abbr>S1</abbr>
                    </gr>
                    ...
                </def>
                <def>
                    <gr>
                        <abbr>S2</abbr>
                    </gr>
                    ...
                </def>
                <def>
                    <gr>
                        <abbr>S3</abbr>
                    </gr>
                    ...
                </def>
            </def>
            <def>
                <sr>
                    Associated Affix: <kref type="rel">XXX</kref>
                </sr>
            </def>
            <categ>
                <kref>input the root's category</kref>
            </categ>
        </ar>
```

An article for a normal affix may include the following parts:

```
        <ar>
            <k>
                <opt>-</opt>
                the affix's value
            </k>
            <k>the affix's abbr.</k>
            <def>
                <gr>Gradient Type XX</gr>
                <deftext>the affix's semantic notion</deftext>
                <def>
                    <deftext>Degree 1 definition</deftext>
                    <!-- if need, insert <abbr>T+number</abbr> for affix-type -->
                </def>
                <def>
                    <deftext>Degree 2 definition</deftext>
                </def>
                <def>
                    <deftext>Degree 3 definition</deftext>
                </def>
                <def>
                    <deftext>Degree 4 definition</deftext>
                </def>
                <def>
                    <deftext>Degree 5 definition</deftext>
                </def>
                <def>
                    <deftext>Degree 6 definition</deftext>
                </def>
                <def>
                    <deftext>Degree 7 definition</deftext>
                </def>
                <def>
                    <deftext>Degree 8 definition</deftext>
                </def>
                <def>
                    <deftext>Degree 9 definition</deftext>
                </def>
            </def>
            <def>
                <sr>
                    Associated Root: -<kref type="rel">the root's value</kref>-
                </sr>
            </def>
            <categ>
                <kref>input the affix's category</kref>
            </categ>
        </ar>
```


