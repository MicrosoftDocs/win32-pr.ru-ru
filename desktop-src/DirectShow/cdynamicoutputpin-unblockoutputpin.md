---
description: Метод Унблоккаутпутпин разблокирует ПИН-код. Если ПИН-код разблокирован, он может доставлять образцы, изменять формат вывода и повторно подключаться к нему.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Кдинамикаутпутпин. Унблоккаутпутпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669129"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a>Кдинамикаутпутпин. Унблоккаутпутпин, метод

`UnblockOutputPin`Метод разблокирует ПИН-код. Если ПИН-код разблокирован, он может доставлять образцы, изменять формат вывода и повторно подключаться к нему.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                             | Описание                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | ПИН-код уже разблокирован.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>                   |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




