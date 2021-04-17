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
ms.openlocfilehash: 2bfc3c2c1d5bb0bbbb3c364b47f22f0790f8d102
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703873"
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

## <a name="remarks"></a>Комментарии

Анимации разрабатываются с использованием местного времени анимации и смешиваются в глобальном времени с помощью [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
