---
description: Приложение "Просмотр событий" использует функцию Опеневентлог, чтобы открыть журнал событий для источника событий.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Чтение из журнала событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4642c003d31c986be55a819b513f1c28c784af2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080626"
---
# <a name="reading-from-the-event-log"></a>Чтение из журнала событий

Приложение "Просмотр событий" использует функцию [**опеневентлог**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) , чтобы открыть журнал событий для источника событий. Затем средство просмотра событий может использовать функцию [**реадевентлог**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) для чтения записей событий из журнала. **Реадевентлог** возвращает буфер, содержащий структуру [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) , и дополнительные сведения, описывающие зарегистрированное событие. Этот процесс представлен на схеме ниже.

![чтение из журнала событий](images/readlog.png)

Пример кода см. в разделе [запросы сведений о событиях](querying-for-event-source-messages.md).

 

 



