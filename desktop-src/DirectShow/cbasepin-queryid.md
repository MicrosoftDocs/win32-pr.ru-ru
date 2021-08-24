---
description: 'Метод QueryId извлекает идентификатор ПИН-кода. Этот метод реализует метод Ипин:: QueryId.'
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: Кбасепин. QueryId, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ac4f7448b27e1780e2d44a512693f3a59113055d66f1b46a85038f04f87f045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158146"
---
# <a name="cbasepinqueryid-method"></a>Кбасепин. QueryId, метод

`QueryId`Метод получает идентификатор ПИН-кода. Этот метод реализует метод [**Ипин:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Id* 
</dt> <dd>

Указатель на идентификатор ПИН-кода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения перечислены в следующей таблице.



| Код возврата                                                                                   | Описание                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>       |
| <dl> <dt>**\_указатель E**</dt> </dl>     | **Пустой** аргумент указателя.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод возвращает копию переменной-члена [**кбасепин:: m \_ pName**](cbasepin-m-pname.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




