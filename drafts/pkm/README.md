# Dataset 'The Mabinogion'

![Static Badge](https://img.shields.io/badge/TEI_validation-passing-green)

This is a TEI port of a [TITUS dataset](http://titus.uni-frankfurt.de/texte/etcs/celt/mcymr/pkm/pkm.htm).

* URL: https://github.com/TITUS-2-0/celtic/tree/main/drafts/pkm
* version: unreleased
* date: 2026-02-02

## Citation
```text
Digital version of The Mabinogion (draft version). By: Jost Gippert, Florian Matter, Elena Parina. In: Carling, Gerd & Jost Gippert (2025). TITUS 2.0. Frankfurt: Goethe University. (URL: https://github.com/TITUS-2-0/celtic/tree/main/drafts/pkm, visited on <insert date>)
```

## TEI encoding


### Unit Mapping
The TITUS 1 structural units are mapped onto TEI as follows:

| Source Unit | TEI Mapping | Notes |
|-------------|-------------|-------|
| Chapter | `div@chapter` | Automatically translated into named div |
| Ms. page | `pb@manuscript` |  |
| Page of edition | `pb@edition[main=yes]` |  |
| Line | `lb@edition` |  |

### Structural overview
```text
text (@xml:lang=wlm-Latn)
  body
    div (@data-level=1, @n, @type=chapter, @xml:id) (multiple)
      head (multiple)
      p (@xml:id) (multiple)
        [lb (@n, @type=edition) (multiple)]
        [pb (@n, @type=manuscript) (multiple)]
        [pb (@main=yes, @n, @type=edition) (multiple)]
        [note (@xml:id) (multiple)]
          [foreign (@xml:lang=cym-Latn | und-Latn-x-general) (multiple)]
        [pb (@break=no, @n, @type=manuscript) (multiple)]
        [lb (@break=no, @n, @type=edition) (multiple)]
        [pb (@type=manuscript)]
      [pb (@main=yes, @n, @type=edition) (multiple)]
      [pb (@n, @type=manuscript)]
```

### Structure Example

```xml
<div xmlns="http://www.tei-c.org/ns/1.0" n="PPD" xml:id="chapter-1" type="chapter" data-level="1">
        <pb main="yes" type="edition" n="1"/>
        <pb type="manuscript" n="1"/>
        <head>Pwyll Pendeuic Dyuet</head>
        <p xml:id="chapter-1-p-1">
          <lb type="edition" n="1"/>PWYLL, Pendeuic Dyuet, a oed yn arglwyd ar seith
          <lb type="edition" n="2"/>cantref Dyuet. A threigylgweith yd oed yn
          <lb type="edition" n="3"/>Arberth, prif lys idaw, a dyuot yn y uryt ac yn y
          <lb type="edition" n="4"/>uedwl uynet y hela. Sef kyueir o'y gyuoeth a uynnei y
          <lb type="edition" n="5"/>hela, Glynn Cuch. Ac ef a gychwynnwys y nos honno
          <lb type="edition" n="6"/>o Arberth, ac a doeth hyt ym Penn Llwyn Diarwya, ac
          <lb type="edition" n="7"/>yno y bu y nos honno. A thrannoeth yn ieuengtit y
  ...
```
