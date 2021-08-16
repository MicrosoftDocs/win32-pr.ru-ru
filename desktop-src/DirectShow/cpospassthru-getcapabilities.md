---
description: 'Кпоспасссру. capabilities-метод — метод capabilities извлекает все возможности поиска в потоке. Этот метод реализует метод Имедиасикинг:: Capabilities.'
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: Метод Кпоспасссру. Capabilities (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3f9c47022ece0305e3111fe21f365544ed495cfe3c1343b908309f801a1a0b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073547"
---
# <a name="cpospassthrugetcapabilities-method"></a>Кпоспасссру. capabilities, метод

Метод **capabilities** извлекает все возможности поиска в потоке. Этот метод реализует метод [**имедиасикинг:: Capabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкапабилитиес* 
</dt> <dd>

Указатель на переменную, которая получает побитовую комбинацию флагов [**\_ \_ поиска \_ возможностей**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .

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
</dt> </dl>

 

 




