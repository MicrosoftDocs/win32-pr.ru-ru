---
description: Метод Disconnect прерывает текущее подключение ПИН-кода. Этот метод реализует метод Ипин::D соединения.
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Метод Кбасепин. Disconnect (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98cbf894767eeb89042134344df218f2c18bc1be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668775"
---
# <a name="cbasepindisconnect-method"></a>Кбасепин. Disconnect, метод

`Disconnect`Метод прерывает текущее подключение к ПИН-коду. Этот метод реализует метод [**Ипин::D соединения**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения перечислены в следующей таблице.



| Код возврата                                                                                         | Описание                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | ПИН-код не подключен.<br/>                                              |
| <dl> <dt>**\_ОК**</dt> </dl>                | Успешно.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ не \_ остановлен**</dt> </dl> | Фильтр активен, и ПИН-код не поддерживает динамическое повторное подключение.<br/> |



 

## <a name="remarks"></a>Комментарии

Базовый класс делегирует большую часть работы методу [**кбасепин::D исконнектинтернал**](cbasepin-disconnectinternal.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




