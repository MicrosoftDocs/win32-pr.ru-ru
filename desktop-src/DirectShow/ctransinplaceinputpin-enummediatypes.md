---
description: 'Ктрансинплацеинпутпин. Енуммедиатипес, метод Енуммедиатипес перечисляет предпочтительные типы мультимедиа для ПИН-кода. Этот метод реализует метод Ипин:: Енуммедиатипес.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Ктрансинплацеинпутпин. Енуммедиатипес, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f0c60a3fd20887975011ba54fba374d0af880cb2711bb501a40d64c6a66f206
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076224"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a>Ктрансинплацеинпутпин. Енуммедиатипес, метод

`EnumMediaTypes`Метод перечисляет предпочтительные типы мультимедиа для ПИН-кода. Этот метод реализует метод [**Ипин:: енуммедиатипес**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппенум* 
</dt> <dd>

Получает указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                                           | Описание                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                  | Успешно.<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Недостаточно памяти.<br/>             |
| <dl> <dt>**\_указатель E**</dt> </dl>             | **Пустой** указатель.<br/>                |
| <dl> <dt>**VFW \_ E \_ не \_ подключен**</dt> </dl> | Выходной ПИН-код не подключен.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод возвращает интерфейс **иенуммедиатипес** из нисходящего входного ПИН-кода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансип. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансинплацеинпутпин**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




