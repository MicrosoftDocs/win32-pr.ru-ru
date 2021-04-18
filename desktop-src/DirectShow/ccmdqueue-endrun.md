---
description: Метод Ендрун переключается в остановленный или приостановленный режим.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Ккмдкуеуе. Ендрун, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367ef026402ff191ceb04657c21d6f3bd11ebe73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656893"
---
# <a name="ccmdqueueendrun-method"></a>Ккмдкуеуе. Ендрун, метод

`EndRun`Метод переключается в режим "остановлено" или "приостановлено".

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** , которое зависит от реализации.

## <a name="remarks"></a>Комментарии

Сопоставление времени потока и времени презентации неизвестно после вызова этой функции-члена. Вызовите функцию члена [**ккмдкуеуе:: Run**](ccmdqueue-run.md) , чтобы выполнить это сопоставление.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




