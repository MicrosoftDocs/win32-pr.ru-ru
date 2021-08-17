---
title: Имедиарендерерактионинформатион Исмутеаваилабле, метод
description: Получает значение, указывающее, поддерживает ли ДМР звук.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- API потоковой передачи мультимедиа метода Исмутеаваилабле
- API потоковой передачи мультимедиа метода Исмутеаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Исмутеаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 331e2831ff18656f23a3d7067b8ab472835bf4a25760f6e86a92302621048a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871071"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a>Метод Имедиарендерерактионинформатион:: Исмутеаваилабле

Получает значение, указывающее, поддерживает ли ДМР звук.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Логическое значение, равное **true** , если ДМР поддерживает озвучивание звука и **false** в противном случае.

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

 

