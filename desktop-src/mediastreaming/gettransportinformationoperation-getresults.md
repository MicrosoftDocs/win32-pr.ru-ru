---
title: Жеттранспортинформатионоператион, метод
description: Возвращает результаты асинхронной операции, запущенной Жеттранспортинформатионасинк.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Жеттранспортинформатионоператион
- API потоковой передачи мультимедиа интерфейса Жеттранспортинформатионоператион, метод Results
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbcc6345a09d0553df240c57e50b4498618be76cc75814f268892aa6e0b4dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100638"
---
# <a name="gettransportinformationoperationgetresults-method"></a>Жеттранспортинформатионоператион:: Results, метод

Возвращает результаты асинхронной операции, запущенной [**жеттранспортинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ out, retval\]
</dt> <dd>

Ссылка на структуру [**транспортинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) , которая содержит результаты операции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](gettransportinformationoperation-completed.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жеттранспортинформатионоператион**](gettransportinformationoperation.md)
</dt> </dl>

 

