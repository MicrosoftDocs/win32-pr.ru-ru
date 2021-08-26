---
description: 'Метод QueryId извлекает идентификатор ПИН-кода. Этот метод переопределяет метод Кбасепин:: QueryId.'
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: Крендереринпутпин. QueryId, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 732bf7aa6d0d247c93c0334db48b86bccd2ac15715dd2da9a4d60a0d315966bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054576"
---
# <a name="crendererinputpinqueryid-method"></a>Крендереринпутпин. QueryId, метод

`QueryId`Метод получает идентификатор ПИН-кода. Этот метод переопределяет метод [**кбасепин:: QueryId**](cbasepin-queryid.md) .

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

Получает строку, содержащую идентификатор ПИН-кода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                   | Описание                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Success<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти<br/>       |
| <dl> <dt>**\_указатель E**</dt> </dl>     | **Пустой** аргумент указателя<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод выделяет строку расширенных символов "in" и присваивает ее параметру *ID* . Вызывающий объект должен освободить выделенную память с помощью функции **CoTaskMemFree** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Крендереринпутпин**](crendererinputpin.md)
</dt> </dl>

 

 




