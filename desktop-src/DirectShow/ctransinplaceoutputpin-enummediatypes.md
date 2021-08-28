---
description: 'Ктрансинплацеаутпутпин. Енуммедиатипес, метод Енуммедиатипес перечисляет предпочтительные типы мультимедиа для ПИН-кода. Этот метод реализует метод Ипин:: Енуммедиатипес.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: Ктрансинплацеаутпутпин. Енуммедиатипес, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7a351f947b0526b8daf77b0b15ea0d2a2894ef6ff90390be484b5d0ce4b7fa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076174"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a>Ктрансинплацеаутпутпин. Енуммедиатипес, метод

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



| Код возврата                                                                                           | Описание                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                  | Успешно.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Недостаточно памяти.<br/>                     |
| <dl> <dt>**\_указатель E**</dt> </dl>             | **Пустой** указатель.<br/>                        |
| <dl> <dt>**VFW \_ E \_ не \_ подключен**</dt> </dl> | Входной ПИН-код фильтра не подключен.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод возвращает интерфейс **иенуммедиатипес** из вышестоящего выходного контакта.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансип. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансинплацеаутпутпин**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




