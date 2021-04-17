---
description: 'Метод Сетсинкпоинт указывает, является ли начало этого образца точкой синхронизации. Этот метод реализует метод Имедиасампле:: Сетсинкпоинт.'
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Кмедиасампле. Сетсинкпоинт, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665195"
---
# <a name="cmediasamplesetsyncpoint-method"></a>Кмедиасампле. Сетсинкпоинт, метод

`SetSyncPoint`Метод указывает, является ли начало этого образца точкой синхронизации. Этот метод реализует метод [**имедиасампле:: сетсинкпоинт**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*биссинкпоинт* 
</dt> <dd>

Логическое значение, указывающее, является ли точка синхронизации. Если **значение равно true**, это точка синхронизации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод обновляет переменную-член [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) , которая указывает свойство точки синхронизации.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




