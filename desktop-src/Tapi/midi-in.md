---
description: Класс MIDI/in Device состоит из последовательностей MIDI, используемых для ввода. Доступ к этим устройствам осуществляется с помощью функций MIDI, которые описаны в пакете SDK для платформы.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: MIDI/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309fe510b08a1e86ef6a00b34a9e3d3282c993babe78eb45aeb6ebb0dab1eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659954"
---
# <a name="midiin"></a>MIDI/in

Класс MIDI/in Device состоит из последовательностей MIDI, используемых для ввода. Доступ к этим устройствам осуществляется с помощью функций MIDI, которые описаны в пакете SDK для платформы.

Функции [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) и [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняют структуру [**Варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **двстрингформат** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Элемент **DeviceID** — это идентификатор закрытого устройства MIDI. Этот идентификатор используется в вызове функции [**мидиинопен**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) для открытия устройства для ввода. С помощью результирующего маркера устройства можно записывать данные MIDI с устройства линии или телефона.

Дополнительные сведения о функциях MIDI см. в разделе [**функции мультимедиа**](../multimedia/multimedia-functions.md).

 

 
