---
description: Класс MIDI/in Device состоит из последовательностей MIDI, используемых для ввода. Доступ к этим устройствам осуществляется с помощью функций MIDI, которые описаны в пакете SDK для платформы.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: MIDI/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808303"
---
# <a name="midiin"></a>MIDI/in

Класс MIDI/in Device состоит из последовательностей MIDI, используемых для ввода. Доступ к этим устройствам осуществляется с помощью функций MIDI, которые описаны в пакете SDK для платформы.

Функции [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) и [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняют структуру [**Варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **двстрингформат** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Элемент **DeviceID** — это идентификатор закрытого устройства MIDI. Этот идентификатор используется в вызове функции [**мидиинопен**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) для открытия устройства для ввода. С помощью результирующего маркера устройства можно записывать данные MIDI с устройства линии или телефона.

Дополнительные сведения о функциях MIDI см. в разделе [**функции мультимедиа**](../multimedia/multimedia-functions.md).

 

 
