---
description: Метод "info" извлекает сведения о текущих параметрах управления потоком, включая время начала и окончания. Этот метод реализует метод Иамстреамконтрол::/info.
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Метод Кбасестреамконтрол. info (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669131"
---
# <a name="cbasestreamcontrolgetinfo-method"></a>Кбасестреамконтрол. info, метод

`GetInfo`Метод получает сведения о текущих параметрах управления потоком, включая время начала и окончания. Этот метод реализует метод [**иамстреамконтрол::/info**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинфо* 
</dt> <dd>

Указатель на структуру [**\_ \_ сведений о потоке AM**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) , выделенную вызывающей стороной, которая получает текущие параметры управления потоком.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ (ОК) или \_ указатель E.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Стрмктл. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасестреамконтрол**](cbasestreamcontrol.md)
</dt> </dl>

 

 




