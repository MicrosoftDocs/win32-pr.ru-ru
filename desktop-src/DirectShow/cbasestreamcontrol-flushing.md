---
description: Метод очистки уведомляет базовый класс о том, что ПИН-код начал или прекратил запись на диск.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: Метод Кбасестреамконтрол. Flush (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668953"
---
# <a name="cbasestreamcontrolflushing-method"></a>Метод Кбасестреамконтрол. Flush

`Flushing`Метод уведомляет базовый класс о том, что ПИН-код запущен или прекратил запись на диск.

## <a name="syntax"></a>Синтаксис


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бинпрогресс* 
</dt> <dd>

Задает логическое значение, указывающее, является ли ПИН-код записью на диск. Используйте значение **true** , когда ПИН-код начинает операцию записи на диск, и **значение false** , если ПИН-код завершает операцию очистки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

ПИН-код должен вызывать этот метод из методов [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) и [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) . Укажите **true** в **бегинфлуш** и **false** в **ендфлуш**.

Этот метод заставляет метод [**кбасестреамконтрол:: чеккстреамстате**](cbasestreamcontrol-checkstreamstate.md) прерывать ожидание. Пока ПИН-код очищается, **чеккстреамстате** всегда возвращает ПОТОКовую \_ отмену.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Стрмктл. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасестреамконтрол**](cbasestreamcontrol.md)
</dt> </dl>

 

 




