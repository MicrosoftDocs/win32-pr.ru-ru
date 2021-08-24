---
description: Класс устройства MIDI состоит из последовательностей MIDI, которые используются для вывода. Доступ к этим устройствам осуществляется с помощью функций MIDI, которые описаны в пакете SDK для платформы.
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: MIDI/OUT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c0199cc7918ab9aeacb3210b6f98d5ff03fc3bca90624bee00d864727ae0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518614"
---
# <a name="midiout"></a>MIDI/OUT

Класс устройства MIDI состоит из последовательностей MIDI, которые используются для вывода. Доступ к этим устройствам осуществляется с помощью функций MIDI, которые описаны в пакете SDK для платформы.

Функции [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) и [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняют структуру [**Варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **двстрингформат** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Элемент **DeviceID** — это идентификатор закрытого устройства MIDI. Этот идентификатор используется в вызове функции [**мидиаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) для открытия устройства для вывода. С помощью полученного маркера устройства можно воспроизводить данные MIDI на устройстве линии или телефоне.

Дополнительные сведения о функциях MIDI см. в разделе [**функции мультимедиа**](../multimedia/multimedia-functions.md).

 

 
