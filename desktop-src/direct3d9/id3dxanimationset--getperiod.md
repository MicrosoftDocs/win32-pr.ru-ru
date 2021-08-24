---
description: Возвращает период набора анимации.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'Метод ID3DXAnimationSet:: period (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d8e984d1593fbbd79561bbb15fb27b62a9961c1830c42465ed529f08c374e180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522333"
---
# <a name="id3dxanimationsetgetperiod-method"></a>Метод ID3DXAnimationSet:: period

Возвращает период набора анимации.

## <a name="syntax"></a>Синтаксис


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Период набора анимации.

## <a name="remarks"></a>Remarks

Период — это диапазон времени, в течение которого действуют ключевые кадры анимации. Для циклических анимаций это период цикла. Единицы времени, в которых указаны ключевые кадры (например, секунды), определяются приложением.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
