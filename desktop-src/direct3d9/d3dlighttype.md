---
description: Определяет тип освещения.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: Перечисление D3DLIGHTTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 66aefec5d614e5fc51f82741fbb30ace71222997273b7647c0bf51f2d5038878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804779"
---
# <a name="d3dlighttype-enumeration"></a>Перечисление D3DLIGHTTYPE

Определяет тип освещения.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**\_Точка D3DLIGHT**
</dt> <dd>

Light — это источник точки. Источник содержит место в пространстве и испускаемое освещение во всех направлениях.

</dd> <dt>

<span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_**
</dt> <dd>

Light — это источник Spotlight. Этот источник подобен точечному излучению, за исключением того, что освещения ограничен конусом. Этот тип освещения имеет направление и несколько других параметров, определяющих форму конуса, который он создает. Дополнительные сведения об этих параметрах см. в разделе Структура [**D3DLIGHT9**](d3dlight9.md) .

</dd> <dt>

<span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ направление**
</dt> <dd>

Light — это направленный источник освещения. Это эквивалентно использованию источника «точка-источник» с бесконечным расстоянием.

</dd> <dt>

<span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Направленные источники света немного быстрее, чем источники света, но световые индикаторы выглядят немного лучше. Прожекторы предлагают интересные визуальные эффекты, но они потребляют много времени.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DLIGHT9**](d3dlight9.md)
</dt> </dl>

 

 




