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
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355933"
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

## <a name="remarks"></a>Комментарии

Значение времени, возвращаемое этим методом, можно использовать в качестве параметра Периодикпоситион [**ID3DXAnimationSet:: жетсрт**](id3dxanimationset--getsrt.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
