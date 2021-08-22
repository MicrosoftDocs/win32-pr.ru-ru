---
description: Метод Доневисвиндов уничтожает окно.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Кбасевиндов. Доневисвиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6871a42e1a08693a7daf691195b86cd5a41dd208295dc625a33e41083b53adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016672"
---
# <a name="cbasewindowdonewithwindow-method"></a>Кбасевиндов. Доневисвиндов, метод

`DoneWithWindow`Метод уничтожает окно.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Вызовите этот метод из метода деструктора производного объекта.

Если этот метод вызывается из того же потока, который создал окно, метод выполняет следующие действия:

-   Вызывает метод [**кбасевиндов:: инактиватевиндов**](cbasewindow-inactivatewindow.md) , который деактивирует окно.
-   Вызывает метод [**кбасевиндов:: унинитиалисевиндов**](cbasewindow-uninitialisewindow.md) , который освобождает ресурсы, используемые окном.
-   Уничтожает окно.

Если поток вызывает `DoneWithWindow` не поток, создавший окно, метод отправляет в окно частное сообщение "Destroy". Когда окно получает это сообщение, оно вызывает `DoneWithWindow` сам себя. (Если [**кбасевиндов:: m \_ Бдопосттодестрой**](cbasewindow-m-bdoposttodestroy.md) имеет **значение true**, окно отправляет сообщение.)

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




