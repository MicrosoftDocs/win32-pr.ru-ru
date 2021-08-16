---
title: Имедиарендерерактионинформатион Иссикаваилабле, метод
description: Получает значение, указывающее, принимает ли ДМР метод Сикасинк в настоящий момент.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- API потоковой передачи мультимедиа метода Иссикаваилабле
- API потоковой передачи мультимедиа метода Иссикаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Иссикаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32b5c7eef78dad4ebfeeebb40c323d7b13e540033eb54852f7da41942f5ec83e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735517"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a>Метод Имедиарендерерактионинформатион:: Иссикаваилабле

Получает значение, указывающее, принимает ли ДМР метод [**сикасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) в настоящий момент.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Логическое значение, равное **true** , если ДМР в настоящее время принимает метод [**Сикасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) , и **false** в противном случае.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имедиарендерерактионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

