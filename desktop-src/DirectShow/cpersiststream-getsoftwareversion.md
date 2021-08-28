---
description: Извлекает версию программного обеспечения для этого потока.
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: Кперсистстреам. Жетсофтвареверсион, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0ba5e9f3fd3dc5e8f021e40c9cb70d95a136ae7c09d6f43826e436a32854170
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084274"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a>Кперсистстреам. Жетсофтвареверсион, метод

Извлекает версию программного обеспечения для этого потока.

## <a name="syntax"></a>Синтаксис


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа DWORD** , содержащее номер версии. При каждом изменении формата потока эта функция должна быть изменена для возврата большего числа, чем раньше.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>пстреам. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кперсистстреам**](cpersiststream.md)
</dt> </dl>

 

 




