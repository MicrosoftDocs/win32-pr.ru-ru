---
title: иажентусеринпут
description: иажентусеринпут
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58ed14c9097a4bd5d3d743a5c026f3e13d6d5ed29a73edb619dd0b2e8bdae17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114654"
---
# <a name="iagentuserinput"></a>иажентусеринпут

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

Когда сервер уведомляет входной-активный клиент с [**иажентнотифисинк:: Command**](iagentnotifysink--command.md), он возвращает сведения через объект [**иажентусеринпут**](/windows/desktop/lwef/iagentuserinput) . **Иажентусеринпут** определяет интерфейс, позволяющий приложениям запрашивать эти значения.

**Методы в порядке таблицы Vtable**



| Методы Иажентусеринпут                                         | Описание                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iagentuserinput--getcount.md)                   | Возвращает количество вариантов команд, возвращаемых в [**командном**](command-event.md) событии.                                         |
| [**жетитемид**](iagentuserinput--getitemid.md)                 | Возвращает идентификатор для определенной альтернативной [**команды**](command-event.md) .                                                              |
| [**жетитемконфиденце**](iagentuserinput--getitemconfidence.md) | Возвращает значение свойства [**достоверности**](confidence-property.md) для определенной альтернативной [**команды**](command-event.md) . |
| [**жетитемтекст**](iagentuserinput--getitemtext.md)             | Возвращает значение текста [**голоса**](voice-property.md) для определенной альтернативной [**команды**](command-event.md) .                   |
| [**жеталлитемдата**](iagentuserinput--getallitemdata.md)       | Возвращает данные для всех альтернативных [**команд**](command-event.md) .                                                                  |



 

 

 