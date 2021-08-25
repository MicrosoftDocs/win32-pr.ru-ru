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
ms.openlocfilehash: a3f5f4ba6f10d5119e479a56e9e207e410b2d1e817d6809e7ceac1c98c8d2ee5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893744"
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

## <a name="remarks"></a>Remarks

Этот метод обычно используется, когда значение глобального времени анимации приближается к максимальной точности ДВОЙНого хранилища или 2 ⁶ ⁴-1.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




