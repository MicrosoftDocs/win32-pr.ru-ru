---
description: Конструирует битовые шаблоны, используемые для распознавания форматов координат текстуры в описании ФВФ. Результаты этих макросов можно объединить в описании ФВФ с помощью оператора или.
ms.assetid: c3076d7c-7935-40ee-b513-7ff6551a535f
title: D3DFVF_TEXCOORDSIZEN (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFVF_TEXCOORDSIZEN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f5a39827f94f0415d6235797489f6e18c5fb515a5e5c36c0f26153b7ba8303ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988914"
---
# <a name="d3dfvf_texcoordsizen"></a>D3DFVF \_ текскурдсизен

Конструирует битовые шаблоны, используемые для распознавания форматов координат текстуры в описании ФВФ. Результаты этих макросов можно объединить в описании ФВФ с помощью оператора или.

``` syntax
#define D3DFVF_TEXCOORDSIZEN(CoordIndex) 
#define D3DFVF_TEXCOORDSIZE1(CoordIndex) (D3DFVF_TEXTUREFORMAT1 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE2(CoordIndex) (D3DFVF_TEXTUREFORMAT2) 
#define D3DFVF_TEXCOORDSIZE3(CoordIndex) (D3DFVF_TEXTUREFORMAT3 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE4(CoordIndex) (D3DFVF_TEXTUREFORMAT4 << (CoordIndex*2 + 16))
```

## <a name="parameters"></a>Параметры



| Параметр                                                                                                    | Описание                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>курдиндекс<br/> | Значение, определяющее набор координат текстуры, в котором применяется размер координаты текстуры (1-, 2-, 3-или 4Dimensional). <br/> |



 

## <a name="remarks"></a>Remarks

Макросы **\_ текскурдсизен D3DFVF** используют следующие константы.


```C++
#define D3DFVF_TEXTUREFORMAT1 3 // one floating point value
#define D3DFVF_TEXTUREFORMAT2 0 // two floating point values
#define D3DFVF_TEXTUREFORMAT3 1 // three floating point values
#define D3DFVF_TEXTUREFORMAT4 2 // four floating point values
```



Следующее описание ФВФ определяет формат вершины, в котором есть расположение. Обычная; рассеянные и бликовые цвета; и два набора координат текстуры. Первый набор координат текстуры включает один элемент, а второй набор включает два элемента:


```C++
DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE |
              D3DFVF_SPECULAR | D3DFVF_TEX2 |
              D3DFVF_TEXCOORDSIZE1(0) |  // Uses 1D texture coordinates for
                                         // texture coordinate set 1 (index 0).
              D3DFVF_TEXCOORDSIZE2(1);   // And 2D texture coordinates for 
                                         // texture coordinate set 2 (index 1).
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DFVF](d3dfvf.md)
</dt> </dl>

 

 




