---
description: 'Метод Коннектионмедиатипе Извлекает тип носителя для текущего соединения ПИН-кода, если таковой имеется. Этот метод реализует метод Ипин:: Коннектионмедиатипе.'
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Кбасепин. Коннектионмедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cdeed52a212a659ca280163ea9513f0cb4f373ea2686bfde00078ebccb183daa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916754"
---
# <a name="cbasepinconnectionmediatype-method"></a>Кбасепин. Коннектионмедиатипе, метод

Метод **коннектионмедиатипе** Извлекает тип носителя для текущего соединения ПИН-кода, если таковой имеется. Этот метод реализует метод [**Ипин:: коннектионмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*состоит* 
</dt> <dd>

Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , которая получает тип мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения перечислены в следующей таблице.



| Код возврата                                                                                           | Описание                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                  | Успешно.<br/>                   |
| <dl> <dt>**\_указатель E**</dt> </dl>             | **Пустой** аргумент указателя.<br/> |
| <dl> <dt>**VFW \_ E \_ не \_ подключен**</dt> </dl> | ПИН-код не подключен.<br/>      |



 

## <a name="remarks"></a>Remarks

Если ПИН-код подключен, этот метод копирует тип носителя в структуру [**\_ \_ типа данных AM Media**](/windows/win32/api/strmif/ns-strmif-am_media_type) , заданную функцией *ПЛТ*. Вызывающий объект должен освободить блок формата типа мультимедиа. Можно использовать функцию [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) или вспомогательную функцию [**фримедиатипе**](freemediatype.md) .

Если ПИН-код не подключен, этот метод обнуляет блок памяти, заданный функцией *ПЛТ* , и возвращает код ошибки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

