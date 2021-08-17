---
description: Возвращает значение времени в локальном интервале в наборе анимации.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'Метод ID3DXAnimationSet:: Жетпериодикпоситион (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8451e3332b61d7e6e993de7df0832a78c0c45c0240633fd5f421998816f7f26f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122065"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a>Метод ID3DXAnimationSet:: Жетпериодикпоситион

Возвращает значение времени в локальном интервале в наборе анимации.

## <a name="syntax"></a>Синтаксис


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Местное время набора анимации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Временной интервал, измеряемый в промежутке времени набора анимации. Это значение будет ограничено периодом набора анимации.

## <a name="remarks"></a>Remarks

Значение времени, возвращаемое этим методом, можно использовать в качестве параметра Периодикпоситион [**ID3DXAnimationSet:: жетсрт**](id3dxanimationset--getsrt.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
