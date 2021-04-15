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
ms.openlocfilehash: b56ae2a846b4d89da4c6a9d4c8f88bd3094c5cff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669371"
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
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти<br/>       |
| <dl> <dt>**\_указатель E**</dt> </dl>     | **Пустой** аргумент указателя<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод выделяет строку расширенных символов "in" и присваивает ее параметру *ID* . Вызывающий объект должен освободить выделенную память с помощью функции **CoTaskMemFree** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Крендереринпутпин**](crendererinputpin.md)
</dt> </dl>

 

 




