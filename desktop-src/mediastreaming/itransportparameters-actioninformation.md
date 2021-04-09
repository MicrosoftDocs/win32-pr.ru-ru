---
title: Итранспортпараметерс Актионинформатион, метод
description: Получает интерфейс Имедиарендерерактионинформатион, который предоставляет сведения о том, какие методы в настоящее время можно вызывать в ДМР.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- API потоковой передачи мультимедиа метода Актионинформатион
- API потоковой передачи мультимедиа метода Актионинформатион, интерфейс Итранспортпараметерс
- API потоковой передачи мультимедиа интерфейса Итранспортпараметерс, метод Актионинформатион
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b194da50e71402b6af69eb4cc9d67902e8ae89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069904"
---
# <a name="itransportparametersactioninformation-method"></a>Метод Итранспортпараметерс:: Актионинформатион

Получает интерфейс [**имедиарендерерактионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) , который предоставляет сведения о том, какие методы в настоящее время можно вызывать в ДМР.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ out, retval\]
</dt> <dd>

Получает ссылку на интерфейс [**имедиарендерерактионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итранспортпараметерс**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

