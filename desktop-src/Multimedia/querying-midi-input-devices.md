---
title: Запрос устройств ввода MIDI
description: Запрос устройств ввода MIDI
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- Цифровой интерфейс MIDI, устройства ввода
- MIDI (цифровой интерфейс музыкального инструмента), устройства ввода
- запись аудио MIDI, устройств ввода
- Устройства ввода MIDI
- Цифровой интерфейс музыкальных инструментов (MIDI), запрос устройств ввода
- MIDI (цифровой интерфейс музыкального инструмента), запрос устройств ввода
- запись аудио MIDI, запрос устройств ввода
- запрос устройств ввода MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a92bec8733887e20c25f37d1de3dd493e555c8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661705"
---
# <a name="querying-midi-input-devices"></a>Запрос устройств ввода MIDI

Перед записью звука MIDI следует использовать функцию [**мидиинжетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) для определения возможностей входного устройства MIDI, присутствующего в системе. Эта функция принимает адрес структуры [**мидиинкапс**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) , которая заполняется сведениями о возможностях данного устройства. Эти сведения включают в себя изготовителя и идентификаторы продуктов, название продукта для устройства и номер версии драйвера устройства.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Запись звука MIDI](recording-midi-audio.md)
</dt> </dl>

 

 