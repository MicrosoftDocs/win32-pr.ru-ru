---
description: 'Метод Куерипреферредформат извлекает предпочтительный формат времени для потока. Этот метод реализует метод Имедиасикинг:: Куерипреферредформат.'
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: Кпоспасссру. Куерипреферредформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6744516f52a22bf322670388295c55f15f19d19c1b3e5896bba1a66e0668a30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757044"
---
# <a name="cpospassthruquerypreferredformat-method"></a>Кпоспасссру. Куерипреферредформат, метод

`QueryPreferredFormat`Метод получает предпочтительный формат времени для потока. Этот метод реализует метод [**имедиасикинг:: куерипреферредформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
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
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> <dt>

[**Идентификаторы GUID формата времени**](time-format-guids.md)
</dt> </dl>

 

 




