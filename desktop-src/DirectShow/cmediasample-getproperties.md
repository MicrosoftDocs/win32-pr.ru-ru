---
description: 'Метод Properties извлекает свойства образца. Этот метод реализует метод IMediaSample2:: Properties.'
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: Метод Кмедиасампле.-Properties (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 856da0c73f3dd93d0c660f55aa0a9de35d87ab1b270df2179d7ad0b520e6d0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074028"
---
# <a name="cmediasamplegetproperties-method"></a>Кмедиасампле... Properties, метод

`GetProperties`Метод получает свойства образца. Этот метод реализует метод [**IMediaSample2:: Properties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кбпропертиес* 
</dt> <dd>

Длина извлекаемых данных свойства в байтах.

</dd> <dt>

*пбпропертиес* 
</dt> <dd>

Указатель на буфер размера *кбпропертиес*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                               | Описание                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>      | Успешно.<br/>                   |
| <dl> <dt>**\_указатель E**</dt> </dl> | **Пустой** аргумент указателя.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




