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
ms.openlocfilehash: 17f846a5824ed07bcaf849a540429eaabe46f3d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412905"
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



 

## <a name="remarks"></a>Комментарии

Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](gettransportinformationoperation-completed.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жеттранспортинформатионоператион**](gettransportinformationoperation.md)
</dt> </dl>

 

