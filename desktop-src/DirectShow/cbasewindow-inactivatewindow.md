---
description: Метод Инактиватевиндов деактивирует окно. В базовом классе этот метод скрывает окно.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Кбасевиндов. Инактиватевиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3cf175a55ab5739b0fa171fe4c9553d3691be82d71b38fd5eb480d6e28043440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567464"
---
# <a name="cbasewindowinactivatewindow-method"></a>Кбасевиндов. Инактиватевиндов, метод

`InactivateWindow`Метод деактивирует окно. В базовом классе этот метод скрывает окно.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                             | Описание                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>                    |
| <dl> <dt>**S \_ false**</dt> </dl> | Окно уже неактивно.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




