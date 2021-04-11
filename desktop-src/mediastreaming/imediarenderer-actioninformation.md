---
title: Имедиарендерер Актионинформатион, метод
description: Извлекает сведения о том, какие методы в данный момент можно вызывать в ДМР.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- API потоковой передачи мультимедиа метода Актионинформатион
- API потоковой передачи мультимедиа метода Актионинформатион, интерфейс Имедиарендерер
- API потоковой передачи мультимедиа интерфейса Имедиарендерер, метод Актионинформатион
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 346e43d6aaf3503c21f6a7586db5a731f0a7c478
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069919"
---
# <a name="imediarendereractioninformation-method"></a>Метод Имедиарендерер:: Актионинформатион

Извлекает сведения о том, какие методы в данный момент можно вызывать в ДМР.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
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

[**имедиарендерер**](imediarenderer.md)
</dt> </dl>

 

