# IthDict
New Ithkuil Dictionary (ITH-ENG) in [XDXF](https://github.com/soshial/xdxf_makedict) format.

XDXF specifies a semantic format for storing dictionaries.

![state](https://img.shields.io/badge/STATE-In%20Progress-green)
![version](https://img.shields.io/badge/VERSION-0.0.3-red)
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

Search `contents` for a catalog. It has Equivalent of Wiktionary categories

Info is obtained by entering keywords (letters or abbreviations) in black. 

![image](https://user-images.githubusercontent.com/12672523/212503498-d96a6f20-a401-4c47-9099-35b59d7f51c4.png)

![image](https://user-images.githubusercontent.com/12672523/212503459-4241e75b-973f-4dfa-b61d-2d6230b8d1b3.png)

![image](https://user-images.githubusercontent.com/12672523/212503477-4206ad27-2660-410b-bb61-5f319e4818ba.png)

# For Developers

Refer to [XDXF Format Standard](https://github.com/soshial/xdxf_makedict/tree/master/format_standard)

## Templates

Each lexical item is within the `<ar>…</ar>` tags, their upper level element is `<lexicon></lexicon>`.

At least these two parts are included in each article：

1. `<k>key</k>` or more
2. `<def>...definition(s)...<categ>category</categ></def>`

Other parts are optional.

An article for a normal root may include the following parts:

```
<ar>
    <k><opt>-</opt>the root's value<opt>-</opt></k>
    <def>
        <def>
            <gr><abbr>S0</abbr><b>the root's semantic notion</b></gr>
            <def>
                <deftext><abbr>BSC</abbr> the text of definition</deftext>
            </def>
            <def>
                <deftext><abbr>CTE</abbr> the text of definition</deftext>
            </def>
            <def>
                <deftext><abbr>CSV</abbr> the text of definition</deftext>
            </def>
            <def>
                <deftext><abbr>OBJ</abbr> the text of definition</deftext>
            </def>
        </def>
        <def>
            <gr><abbr>S1</abbr></gr>
            <deftext>the text of definition</deftext>
        </def>
        <def>
            <gr><abbr>S2</abbr></gr>
            <deftext>the text of definition</deftext>
        </def>
        <def>
            <gr><abbr>S3</abbr></gr>
            <deftext>the text of definition</deftext>
        </def>
        <def>
            <gr>Grammar Description</gr>
            <deftext>...</deftext> <!-- Or <def></def> tag(s) -->
        </def>
        <def>
            <deftext>Associated Affix: <kref type="rel">XXX</kref></deftext>
        </def>
        <categ>
            <kref>the root's category</kref>
        </categ>
    </def>
</ar>
```

An article for a normal affix may include the following parts:

```
<ar>
    <k><opt>-</opt>the affix's value</k>
    <k>the affix's abbr.</k>
    <def>
        <def>
            <gr><abbr>Gradient Type XX</abbr><b>the affix's semantic notion</b></gr>
            <def>
                <deftext><abbr>D1</abbr> the text of definition</deftext>
            </def>
            <def>
                <deftext><abbr>D2</abbr> the text of definition</deftext>
            </def>
            <def>
                <deftext><abbr>D3</abbr> the text of definition</deftext>
            </def>
            <def>
                <deftext><abbr>D4</abbr> the text of definition</deftext>
            </def>
            <def>
                <deftext><abbr>D5</abbr> the text of definition</deftext>
            </def>
            <def>
                <deftext><abbr>D6</abbr> the text of definition</deftext>
            </def>
            <def>
                <deftext><abbr>D7</abbr> the text of definition</deftext>
            </def>
            <def>
                <deftext><abbr>D8</abbr> the text of definition</deftext>
            </def>
            <def>
                <deftext><abbr>D9</abbr> the text of definition</deftext>
            </def>
        </def>
        <def>
            <deftext>Associated Root: -<kref type="rel">Cr</kref>-</deftext>
        </def>
        <categ>
            <kref>the affix's category</kref>
        </categ>
    </def>
</ar>
```

`<co>comment</co>` has `type` attribute which specifies what kind of comment it is: `grammatical`, `usage`, etc.

```
<ex>
  <ex_orig>the original phrase of the example</ex_orig>
  <ex_tran>multiple translations:optional</ex_tran>
</ex>
```


