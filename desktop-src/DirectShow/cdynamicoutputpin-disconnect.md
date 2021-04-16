---
description: Метод Disconnect прерывает текущее подключение ПИН-кода. Этот метод реализует метод Ипин::D соединения.
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Метод Кдинамикаутпутпин. Disconnect (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65c61ecc825d703976aa3163be5922da1ac4471a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669142"
---
# <a name="cdynamicoutputpindisconnect-method"></a>Кдинамикаутпутпин. Disconnect, метод

`Disconnect`Метод прерывает текущее подключение к ПИН-коду. Этот метод реализует метод [**Ипин::D соединения**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                             | Описание                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | ПИН-код не подключен.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>                   |



 

## <a name="remarks"></a>Комментарии

Этот метод переопределяет метод [**кбасепин::D соединения**](cbasepin-disconnect.md) , чтобы разрешить отсоединение, пока фильтр активен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




