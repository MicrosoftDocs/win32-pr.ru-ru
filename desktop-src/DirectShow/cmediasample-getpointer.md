---
description: Метод-указатель извлекает указатель чтения/записи в буфер. Этот метод реализует метод Имедиасампле::/.
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Метод Кмедиасампле.-Point (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21a39fae4f243c0a4e7305573f1b06ee2f11766729ef4933124d059b20b3a14b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832274"
---
# <a name="cmediasamplegetpointer-method"></a>Кмедиасампле. метод.

`GetPointer`Метод извлекает указатель чтения/записи в буфер. Этот метод реализует метод [**имедиасампле::**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) /.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ppBuffer* 
</dt> <dd>

Адрес переменной, которая получает указатель на буфер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




