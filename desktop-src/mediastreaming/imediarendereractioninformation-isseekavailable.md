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
ms.openlocfilehash: 700afb72efbab01bbd3a8f5e15fa444eb6b06272
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890588"
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

 

