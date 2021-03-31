---
description: Сбрасывает глобальное время анимации в ноль. Все события, ожидающие обработки, сохраняют свои исходные расписания, но в новом периоде времени.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'Метод ID3DXAnimationController:: Ресеттиме (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821301"
---
# <a name="id3dxanimationcontrollerresettime-method"></a>Метод ID3DXAnimationController:: Ресеттиме

Сбрасывает глобальное время анимации в ноль. Все события, ожидающие обработки, сохраняют свои исходные расписания, но в новом периоде времени.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Этот метод обычно используется, когда значение глобального времени анимации приближается к максимальной точности ДВОЙНого хранилища или 2 ⁶ ⁴-1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




