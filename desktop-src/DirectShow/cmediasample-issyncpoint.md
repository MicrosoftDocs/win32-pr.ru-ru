---
description: 'Метод Иссинкпоинт определяет, является ли начало образца точкой синхронизации. Этот метод реализует метод Имедиасампле:: Иссинкпоинт.'
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Кмедиасампле. Иссинкпоинт, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8cc93c03ce3b864e1c1b0a5794d711b1b0c3d68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665212"
---
# <a name="cmediasampleissyncpoint-method"></a>Кмедиасампле. Иссинкпоинт, метод

`IsSyncPoint`Метод определяет, является ли начало образца точкой синхронизации. Этот метод реализует метод [**имедиасампле:: иссинкпоинт**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК, если образец является точкой синхронизации, или \_ false в противном случае.

## <a name="remarks"></a>Комментарии

Значение этого свойства указывается в переменной члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




