---
title: Выделение и подготовка блоков данных MIDI
description: Выделение и подготовка блоков данных MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), выделение блоков данных
- MIDI (цифровой интерфейс музыкального инструмента), выделение блоков данных
- Службы MIDI, выделение блоков данных
- Выделение блоков данных MIDI
- Цифровой интерфейс MIDI, подготовка блоков данных
- MIDI (цифровой интерфейс музыкального инструмента), подготовка блоков данных
- Службы MIDI, подготовка блоков данных
- подготовка блоков данных MIDI
- Цифровой интерфейс MIDI, блоки данных
- MIDI (цифровой интерфейс музыкального инструмента), блоки данных
- Службы MIDI, блоки данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672281"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>Выделение и подготовка блоков данных MIDI

Для функций [**мидиаутлонгмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**мидиинаддбуффер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)и [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) требуется, чтобы приложения выделили блоки данных для передачи в драйверы устройств для воспроизведения или записи. Каждая из этих функций использует структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) для описания своего блока данных.

Прежде чем использовать одну из этих функций для передачи блока данных в драйвер устройства, необходимо выделить память для буфера и структуру заголовка, описывающую блок данных.

Windows предоставляет следующие функции для подготовки и очистки блоков данных MIDI.



| Значение                                                    | Значение                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**мидиинпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | Подготавливает блок входных данных MIDI.                      |
| [**мидиинунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | Очищает подготовку блока входных данных MIDI.  |
| [**мидиаутпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | Подготавливает блок выходных данных MIDI.                     |
| [**мидиаутунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | Очищает подготовку блока выходных данных MIDI. |



 

Перед передачей блока данных MIDI в драйвер устройства необходимо подготовить буфер, передав его в функцию [**мидиинпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) или [**мидиаутпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) . Когда драйвер устройства завершает работу с буфером и возвращает его, необходимо очистить эту подготовку, передав буфер в функцию [**мидиинунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) или [**мидиаутунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) , прежде чем можно будет освободить выделенную память.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Службы MIDI](midi-services.md)
</dt> </dl>

 

 