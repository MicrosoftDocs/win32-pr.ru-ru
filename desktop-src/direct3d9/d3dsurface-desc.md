---
description: Описывает поверхность.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: Структура D3DSURFACE_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6424bbe9b78532657670bc5cd9ad0705de89a3b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713595"
---
# <a name="d3dsurface_desc-structure"></a>\_Структура D3DSURFACE DESC

Описывает поверхность.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Формат**
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат поверхности.

</dd> <dt>

**Тип**
</dt> <dd>

Тип: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Член перечислимого типа [**D3DRESOURCETYPE**](./d3dresourcetype.md) , который определяет этот ресурс как поверхность.

</dd> <dt>

**Использование**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Значение D3DUSAGE \_ депсстенЦил или D3DUSAGE \_ рендертаржет. Дополнительные сведения см. в разделе [**D3DUSAGE**](d3dusage.md).

</dd> <dt>

**Пул.**
</dt> <dd>

Тип: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Член перечисляемого типа [**D3DPOOL**](./d3dpool.md) , указывающий класс памяти, выделенной для этой поверхности.

</dd> <dt>

**мултисамплетипе**
</dt> <dd>

Тип: **[ **D3DMULTISAMPLE \_ тип**](./d3dmultisample-type.md)**

</dd> <dd>

Член перечисляемого [**типа \_ D3DMULTISAMPLE**](./d3dmultisample-type.md) , указывающий уровни многофакторной множественной выборки, поддерживаемые поверхностью.

</dd> <dt>

**мултисамплекуалити**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Уровень качества. Диапазон допустимых значений — от нуля до уровня, возвращенного Пкуалитилевелс, используемым [**чеккдевицемултисамплетипе**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype). При передаче большего значения возвращается ошибка D3DERR \_ инвалидкалл. Значения Мултисамплекуалити для парных целевых объектов рендеринга, поверхности трафарета глубины и типа "многопримерные" должны соответствовать всем.

</dd> <dt>

**Width**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ширина поверхности (в пикселях).

</dd> <dt>

**Height**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Высота поверхности (в пикселях).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**жетлевелдеск**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[**жетлевелдеск**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
