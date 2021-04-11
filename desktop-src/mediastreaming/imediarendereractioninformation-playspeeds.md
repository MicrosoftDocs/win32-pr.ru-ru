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
ms.openlocfilehash: 31089dd7616c035ebde4079c51988b94d1c27562
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337276"
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

 

