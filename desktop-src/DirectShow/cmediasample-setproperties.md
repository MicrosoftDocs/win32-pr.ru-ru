---
description: 'Метод SetProperties задает свойства образца. Этот метод реализует метод IMediaSample2:: SetProperties.'
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: Кмедиасампле. SetProperties, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4bac378d41e0a9933f0903990e6368979c669c048102665a06b2ce59e4a45c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156536"
---
# <a name="cmediasamplesetproperties-method"></a>Кмедиасампле. SetProperties, метод

`SetProperties`Метод задает свойства образца. Этот метод реализует метод [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кбпропертиес* 
</dt> <dd>

Длина устанавливаемых данных свойств в байтах.

</dd> <dt>

*пбпропертиес* 
</dt> <dd>

Указатель на буфер размера *кбпропертиес*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                   | Описание                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Success<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый аргумент<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти<br/>       |
| <dl> <dt>**\_указатель E**</dt> </dl>     | **Пустой** аргумент указателя<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




