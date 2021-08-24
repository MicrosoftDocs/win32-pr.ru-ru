---
title: Имедиарендерерактионинформатион Исстопаваилабле, метод
description: Получает значение, указывающее, принимает ли ДМР метод Стопасинк в настоящий момент.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- API потоковой передачи мультимедиа метода Исстопаваилабле
- API потоковой передачи мультимедиа метода Исстопаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Исстопаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c177c46c62309525d9362f985075cec293105a80678b3b857eafa0524179d17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712894"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a>Метод Имедиарендерерактионинформатион:: Исстопаваилабле

Получает значение, указывающее, принимает ли ДМР метод [**стопасинк**](imediarenderer-stopasync.md) в настоящий момент.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Логическое значение, равное **true** , если ДМР в настоящее время принимает метод [**Стопасинк**](imediarenderer-stopasync.md) , и **false** в противном случае.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**имедиарендерерактионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

