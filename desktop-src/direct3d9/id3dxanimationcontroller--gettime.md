---
description: Возвращает глобальное время анимации.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: Метод ID3DXAnimationController::-Time (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6241bbd8c447889a4718369feabf8f26dacc73c58b8e6826c1797d0639422fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987834"
---
# <a name="id3dxanimationcontrollergettime-method"></a>Метод ID3DXAnimationController:: OnTime

Возвращает глобальное время анимации.

## <a name="syntax"></a>Синтаксис


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Возвращает глобальное время анимации.

## <a name="remarks"></a>Remarks

Анимации разрабатываются с использованием местного времени анимации и смешиваются в глобальном времени с помощью [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
