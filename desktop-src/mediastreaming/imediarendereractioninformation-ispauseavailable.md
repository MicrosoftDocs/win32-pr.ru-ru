---
title: Имедиарендерерактионинформатион Испаусеаваилабле, метод
description: Получает значение, указывающее, принимает ли ДМР метод Паусеасинк в настоящий момент.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- API потоковой передачи мультимедиа метода Испаусеаваилабле
- API потоковой передачи мультимедиа метода Испаусеаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Испаусеаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fad69863306a8a937771f16c2ab9a83a2622c571d2cd5ee5658a279bf7564132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870851"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a>Метод Имедиарендерерактионинформатион:: Испаусеаваилабле

Получает значение, указывающее, принимает ли ДМР метод [**паусеасинк**](imediarenderer-pauseasync.md) в настоящий момент.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Логическое значение, равное **true** , если ДМР в настоящее время принимает метод [**Паусеасинк**](imediarenderer-pauseasync.md) , и **false** в противном случае.

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

 

