---
description: 'Кпоспасссру. Конверттимеформат, метод Конверттимеформат преобразует из одного формата времени в другой. Этот метод реализует метод Имедиасикинг:: Конверттимеформат.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Кпоспасссру. Конверттимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc463cb6dc891e677266289971a1dac8b335a8c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098962"
---
# <a name="cpospassthruconverttimeformat-method"></a>Кпоспасссру. Конверттимеформат, метод

`ConvertTimeFormat`Метод преобразует из одного формата времени в другой. Этот метод реализует метод [**имедиасикинг:: конверттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птаржет* 
</dt> <dd>

Указатель на переменную, которая получает преобразованное время.

</dd> <dt>

*птаржетформат* 
</dt> <dd>

Указатель на идентификатор GUID формата времени целевого формата. Если **значение равно NULL**, используется текущий формат.

</dd> <dt>

*Источник* 
</dt> <dd>

Значение времени, которое необходимо преобразовать.

</dd> <dt>

*псаурцеформат* 
</dt> <dd>

Указатель на идентификатор GUID формата времени для преобразования. Если **значение равно NULL**, используется текущий формат.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> <dt>

[**Идентификаторы GUID формата времени**](time-format-guids.md)
</dt> </dl>

 

 




