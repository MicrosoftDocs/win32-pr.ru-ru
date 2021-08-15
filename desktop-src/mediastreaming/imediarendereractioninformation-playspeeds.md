---
title: Имедиарендерерактионинформатион Плайспидс, метод
description: Извлекает полный список значений Плайспид, которые принимаются параметром ДМР.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- API потоковой передачи мультимедиа метода Плайспидс
- API потоковой передачи мультимедиа метода Плайспидс, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Плайспидс
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 573fe9da4e71f9c16a9850da352e866ddbb0f77abc8c30861f2aa29647065fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972203"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a>Имедиарендерерактионинформатион: метод:P Лайспидс

Извлекает полный список значений [**плайспид**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) , которые принимаются параметром ДМР.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Получает вектор структур [**плайспид**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) , указывающий полный список значений **плайспид** , принимаемых ДМР.

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

 

