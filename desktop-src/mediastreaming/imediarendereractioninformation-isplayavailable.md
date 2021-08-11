---
title: Имедиарендерерактионинформатион Исплайаваилабле, метод
description: Извлекает значение, указывающее, принимает ли ДМР в настоящее время принятие методов Плайасинк и Плайатспидасинк.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- API потоковой передачи мультимедиа метода Исплайаваилабле
- API потоковой передачи мультимедиа метода Исплайаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Исплайаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 912e5478ef1d9bd7114d198a9671d38ba7b721c9dbd82d2a8080b5a7876e76cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235849"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a>Метод Имедиарендерерактионинформатион:: Исплайаваилабле

Извлекает значение, указывающее, принимает ли ДМР в настоящее время принятие методов [**плайасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) и [**плайатспидасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Логическое значение, равное **true** , если в настоящее время ДМР принимает методы [**плайасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) и [**плайатспидасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) , и **false** , если это не так.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также статью

<dl> <dt>

[**имедиарендерерактионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

