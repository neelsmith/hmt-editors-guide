## 3: Semantic disambiguation

Tier 3 semantically disambiguates tokens. This class of mark up is primarily named entities.

## Named entities (proper nouns and adjectives) ##

**personal names**

For people, mythological or historical, use TEI `persName` element; include an `@n` attribute with the full URN value from the [reference table of identifiers for personal names][pers]. If a person does not yet exist in the authority list, create an issue in the repository to request its addition.

[![Achilles][Achilles]][500]

Example:

`<persName n="urn:cite:hmt:pers.pers1">Ἀχιλλεύς</persName>`

(urn:cts:greekLit:tlg0012.tlg001.msA:1.58)

[Achilles]: http://www.homermultitext.org/iipsrv?OBJ=IIP,1.0&FIF=/project/homer/pyramidal/VenA/VA013RN-0014.tif&RGN=0.488,0.2915,0.063,0.0263&WID=100&CVT=JPEG

[500]: http://www.homermultitext.org/hmt-digital/images?request=GetIIPMooViewer&urn=urn:cite:hmt:vaimg.VA013RN-0014@0.488,0.2915,0.063,0.0263

- Note in cases where more than one person is refered to, such as the Atreidai, you double wrap personal names

[![Atreidai][Atreidai]][501]

Example:

`<persName n="urn:cite:hmt:pers.pers22"><persName n="urn:cite:hmt:pers.pers119">Ἀτρεΐδαι</persName></persName>`

(urn:cts:greekLit:tlg0012.tlg001.msA:1.17)

[Atreidai]: http://www.homermultitext.org/iipsrv?OBJ=IIP,1.0&FIF=/project/homer/pyramidal/VenA/VA012RN-0013.tif&RGN=0.1602,0.5465,0.0841,0.0263&WID=100&CVT=JPEG

[501]: http://www.homermultitext.org/hmt-digital/images?request=GetIIPMooViewer&urn=urn:cite:hmt:vaimg.VA012RN-0013@0.1602,0.5465,0.0841,0.0263

**place names**

For places, mythological or historical, use TEI `placeName` element; include on the `@n` attribute has a full URN value from  the [reference table of identifiers for place names][place]. If a place does not yet exist in the authority list, create an issue in the repository to request its addition.

[![Argos][Argos]][503]

Example:

`<placeName n="urn:cite:hmt:place.place114">Ἄργεϊ</placeName>`

(urn:cts:greekLit:tlg0012.tlg001.msA:1.30)

[Argos]: http://www.homermultitext.org/iipsrv?OBJ=IIP,1.0&FIF=/project/homer/pyramidal/VenA/VA012VN-0514.tif&RGN=0.655,0.2915,0.049,0.0293&WID=100&CVT=JPEG

[503]: http://www.homermultitext.org/hmt-digital/images?request=GetIIPMooViewer&urn=urn:cite:hmt:vaimg.VA012VN-0514@0.655,0.2915,0.049,0.0293


**ethnic groups**

These are exclusively for groups of people that can be traced either to a geographic place or an emponymous ancestor. Use TEI `rs` element. Include a `@type` attribute with value `ethnic`, and `@n` attribute with an identifier from the  [reference table for place names][place] or the [reference table for personal names][pers], when you need to use an eponymous ancestor (such as the Danaans).

[![Achaious][Achaious]][504]

Example:

`<rs type="ethnic" n="urn:cite:hmt:place.place96">Ἀχαιούς</rs>`

(urn:cts:greekLit:tlg0012.tlg001.msA:1.61)

- Since some ethnic names could be attributed to a location or an eponymous ancester (e.g. Trojans link to Tros or Troy), always take the geographic location before resorting to an eponymous ancestor.
- Note that the ethnic mark up is only for people or groups of people (e.g. Trojan man or Trojans). We would not use it to describe a dialect (e.g. Ionic) or an inanimate object. Those are treated as normal vocabulary items that can be searched.
- Groups that cannot be tied to a geographic place or an eponymous ancestor are also treated as vocabulary items (e.g. Centaurs, Myrmidons, Gorgons, Giants, Fates, etc).
- Adjectival forms of people's names are also not tagged (ergo, we can tag 'Homer' but not 'Homeric')
- We also do not tag unclear epithets, even if the identity can be determined from context. For example "Phoebus Apollo" is ok, but the "Earthshaker" to refer to Poseidon is not. If you are in doubt, refer to the description of the indiviual in the authority list. If the epithet is not listed there, you can request it, via Issue Tracker and our editorial guide team can render a judgement.

[Achaious]: http://www.homermultitext.org/iipsrv?OBJ=IIP,1.0&FIF=/project/homer/pyramidal/VenA/VA013RN-0014.tif&RGN=0.461,0.426,0.071,0.027&WID=100&CVT=JPEG

[504]: http://www.homermultitext.org/hmt-digital/images?request=GetIIPMooViewer&urn=urn:cite:hmt:vaimg.VA013RN-0014@0.461,0.426,0.071,0.027

**astronomical bodies**

:   Use TEI `rs` element.   Include a `@type` attribute with value `astro`, and `@n` attribute with an identifer from the [reference table for astronomical bodies][astro].

[![Orion][Orion]][505]

Example:

`<rs type="astro" n="urn:cite:hmt:astro.1">Ὠρίωνος</rs>`

(urn:cts:greekLit:tlg0012.tlg001.msA:18.486)

[astro]: https://github.com/homermultitext/hmt-authlists/blob/master/data/astronomy.csv

[Orion]: http://www.homermultitext.org/iipsrv?OBJ=IIP,1.0&FIF=/project/homer/pyramidal/VenA/VA248VN-0750.tif&RGN=0.811,0.3343,0.084,0.0323&WID=100&CVT=JPEG

[505]: http://www.homermultitext.org/hmt-digital/images?request=GetIIPMooViewer&urn=urn:cite:hmt:vaimg.VA248VN-0750@0.811,0.3343,0.084,0.0323
