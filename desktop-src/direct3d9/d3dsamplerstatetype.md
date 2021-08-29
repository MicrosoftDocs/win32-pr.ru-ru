---
description: Состояния образцов определяют операции выборки текстур, такие как адресация текстур и фильтрация текстур.
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: Перечисление D3DSAMPLERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 55e8efe80390f64f2376fd3995e414fed604ec8cb854c14b94f71922e146a32e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988884"
---
# <a name="d3dsamplerstatetype-enumeration"></a>Перечисление D3DSAMPLERSTATETYPE

Состояния образцов определяют операции выборки текстур, такие как адресация текстур и фильтрация текстур. Некоторые состояния выборки настроили обработку вершин и некоторую обработку пикселов настройки. Состояния образцов можно сохранить и восстановить с помощью статеблоккс (см. раздел [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP \_ аддрессу**
</dt> <dd>

Режим адресации текстуры для координаты u. Значение по умолчанию — D3DTADDRESS \_ Wrap. Дополнительные сведения см. в разделе [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ аддрессв**
</dt> <dd>

Режим адресации текстуры для координаты v. Значение по умолчанию — D3DTADDRESS \_ Wrap. Дополнительные сведения см. в разделе [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ аддрессв**
</dt> <dd>

Режим адресации текстуры для координаты w. Значение по умолчанию — D3DTADDRESS \_ Wrap. Дополнительные сведения см. в разделе [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP \_ BORDERCOLOR**
</dt> <dd>

Цвет границы или тип [**D3DCOLOR**](d3dcolor.md). Цвет по умолчанию — 0x00000000.

</dd> <dt>

<span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP \_ магфилтер**
</dt> <dd>

Фильтр увеличения типа [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). Значение по умолчанию — D3DTEXF \_ Point.

</dd> <dt>

<span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ минфилтер**
</dt> <dd>

Фильтр минификации типа [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). Значение по умолчанию — D3DTEXF \_ Point.

</dd> <dt>

<span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ мипфилтер**
</dt> <dd>

Фильтр mipmap для использования во время минификации. См. [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). Значение по умолчанию — D3DTEXF \_ None.

</dd> <dt>

<span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ мипмаплодбиас**
</dt> <dd>

Mipmap уровень детализации. Значение по умолчанию равно нулю.

</dd> <dt>

<span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ максмиплевел**
</dt> <dd>

Индекс уровня детализации для максимальной используемой схемы. Диапазон значений — от 0 до (n – 1), где 0 — это самый крупный. Значение по умолчанию равно нулю.

</dd> <dt>

<span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ максанисотропи**
</dt> <dd>

Максимальная анизотропная длина DWORD. Значения находятся в диапазоне от 1 до значения, указанного в элементе **максанисотропи** структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . Значение по умолчанию — 1.

</dd> <dt>

<span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ сргбтекстуре**
</dt> <dd>

Значение гамма-коррекции. Значение по умолчанию — 0. Это означает, что гамма-1,0 и не требуется никаких исправлений. В противном случае это значение означает, что образец должен иметь гамму 2,2 на содержимом и преобразовать его в линейный (гамма-1,0) перед представлением в шейдер пикселей.

</dd> <dt>

<span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ елементиндекс**
</dt> <dd>

Если для образца назначена Многоэлементная текстура, это указывает, какой индекс элемента следует использовать. Значение по умолчанию — 0.

</dd> <dt>

<span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ дмапоффсет**
</dt> <dd>

Смещение вершины в предвыборочной карте смещения. Это константа, используемая тесселяцией, ее значение по умолчанию — 0.

</dd> <dt>

<span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
