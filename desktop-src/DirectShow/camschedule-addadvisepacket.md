---
description: Метод Аддадвисепаккет добавляет запрос advise в список ожидающих запросов.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Камсчедуле. Аддадвисепаккет, метод (Дссчедуле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668787"
---
# <a name="camscheduleaddadvisepacket-method"></a>Камсчедуле. Аддадвисепаккет, метод

`AddAdvisePacket`Метод добавляет запрос advise в список ожидающих запросов.

## <a name="syntax"></a>Синтаксис


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*time1* \[ ЗНАЧ\]
</dt> <dd>

Запрошенное время для уведомления.

</dd> <dt>

*time2* \[ ЗНАЧ\]
</dt> <dd>

Для периодических запросов рекомендаций — время между уведомлениями. Этот параметр игнорируется, если *бпериодик* имеет **значение false**.

</dd> <dt>

*хнотифи* 
</dt> <dd>

Обработчик для семафора, если *бпериодик* имеет **значение true**, или обрабатывает событие, если *бпериодик* имеет **значение false**.

</dd> <dt>

*бпериодик* 
</dt> <dd>

Логическое значение, указывающее, следует ли добавить периодическое уведомление или одно уведомление. **Значение true** показывает, что уведомление является периодическим; параметр *time2* указывает время между уведомлениями. Если **значение равно false**, уведомление возникает только один раз.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает идентификатор для запроса advise ("cookie"). Если метод завершается с ошибкой, возвращаемое значение равно нулю.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дссчедуле. h (включение Streams. h)</dt> </dl>                                                                                |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсчедуле**](camschedule.md)
</dt> </dl>

 

 




