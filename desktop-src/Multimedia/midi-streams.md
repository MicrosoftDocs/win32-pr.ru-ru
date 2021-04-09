---
title: Потоки MIDI
description: Потоки MIDI
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- Цифровой интерфейс MIDI, потоки
- MIDI (цифровой интерфейс музыкального инструмента), потоки
- буферы потоков, потоки MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133830"
---
# <a name="midi-streams"></a>Потоки MIDI

События MIDI возникают в контексте потока данных MIDI. Хотя приложение может использовать несколько потоков для определения музыкальных данных, средство сопоставления MIDI не распознает несколько потоков. Большинство приложений, использующих потоки, используют один поток MIDI.

Следующие функции работают с потоками.



| Значение                                            | Значение                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**мидистреамклосе**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | Закрывает поток MIDI.                                                   |
| [**мидистреамопен**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | Открывает поток MIDI и получает маркер.                             |
| [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | Воспроизводит поток (буфер) данных MIDI на устройстве вывода MIDI. |
| [**мидистреампаусе**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | Приостанавливает воспроизведение указанного потока MIDI.                             |
| [**мидистреампоситион**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | Возвращает текущую точку в потоке MIDI.                        |
| [**мидистреампроперти**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | Задает и получает свойства потока.                                   |
| [**мидистреамрестарт**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | Перезапускает воспроизведение приостановленного потока MIDI.                              |
| [**мидистреамстоп**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | Отключает все заметки на всех каналах MIDI для указанного потока MIDI. |



 

 

 