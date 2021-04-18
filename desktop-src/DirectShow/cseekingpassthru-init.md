---
description: Метод init Инициализирует объект.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: Метод CSeekingPassThru.Init (Сикпт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656901"
---
# <a name="cseekingpassthruinit-method"></a>Метод CSeekingPassThru.Init

`Init`Метод инициализирует объект.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бсуппортрендеринг* \[ окне\]
</dt> <dd>

Логическое значение, указывающее, является ли фильтр модулем подготовки отчетов. Используйте значение **true** , если фильтр является модулем подготовки отчетов, или **false** в противном случае.

</dd> <dt>

*ппин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) для входного ПИН-кода фильтра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                   | Описание                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>                                |
| <dl> <dt>**\_Ошибка E**</dt> </dl>        | Объект уже инициализирован.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти для создания объекта.<br/> |



 

## <a name="remarks"></a>Комментарии

Если значение *бсуппортрендеринг* равно **true**, этот метод создает экземпляр класса [**крендерерпоспасссру**](crendererpospassthru.md) . В противном случае создается экземпляр класса [**кпоспасссру**](cpospassthru.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Сикпт. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксикингпасссру**](cseekingpassthru.md)
</dt> </dl>

 

 




