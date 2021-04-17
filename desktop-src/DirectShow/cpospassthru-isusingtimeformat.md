---
description: 'Метод Исусингтимеформат определяет, является ли указанный формат времени используемым в данный момент форматом. Этот метод реализует метод Имедиасикинг:: Исусингтимеформат.'
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: Кпоспасссру. Исусингтимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 012a9487f5840117edb9f8bc0afa1d9388b4bce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658016"
---
# <a name="cpospassthruisusingtimeformat-method"></a>Кпоспасссру. Исусингтимеформат, метод

`IsUsingTimeFormat`Метод определяет, является ли указанный формат времени используемым в данный момент форматом. Этот метод реализует метод [**имедиасикинг:: исусингтимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пформат* 
</dt> <dd>

Указатель на GUID формата времени.

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

 

 




