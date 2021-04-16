---
title: Обработка ошибок с помощью функций MIDI
description: Обработка ошибок с помощью функций MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), ошибки
- MIDI (цифровой интерфейс музыкального инструмента), ошибки
- Службы MIDI, ошибки
- Ошибки MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650354"
---
# <a name="handling-errors-with-midi-functions"></a>Обработка ошибок с помощью функций MIDI

Функции аудио MIDI возвращают ненулевой код ошибки. Для ошибок, связанных с MIDI, функции [**мидиинжетеррортекст**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) и [**мидиаутжетеррортекст**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) извлекают текстовые описания кодов ошибок. Приложение должно по-прежнему просматривать значение ошибки, чтобы определить, как это можно сделать, но оно может использовать описания ошибок в диалоговых окнах для информирования пользователей об условиях ошибки.

Единственными функциями MIDI, которые не возвращают коды ошибок, являются функции [**мидиинжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) и [**мидиаутжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) . Эти функции возвращают нулевое значение, если в системе нет устройств или если какая-либо ошибка обнаружена функцией.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Службы MIDI](midi-services.md)
</dt> </dl>

 

 