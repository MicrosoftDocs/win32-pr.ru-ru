---
description: 'Метод Жеттимеформат извлекает текущий формат времени. Этот метод реализует метод Имедиасикинг:: Жеттимеформат.'
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: Кпоспасссру. Жеттимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7db1b46cfe2ac06dc43b52009043ae32676f154
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658020"
---
# <a name="cpospassthrugettimeformat-method"></a>Кпоспасссру. Жеттимеформат, метод

`GetTimeFormat`Метод получает текущий формат времени. Этот метод реализует метод [**имедиасикинг:: жеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пформат* 
</dt> <dd>

Указатель на переменную, которая получает GUID формата времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> <dt>

[**Идентификаторы GUID формата времени**](time-format-guids.md)
</dt> </dl>

 

 




