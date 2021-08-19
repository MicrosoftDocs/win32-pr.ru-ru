---
description: Приложение "Просмотр событий" использует функцию Опеневентлог, чтобы открыть журнал событий для источника событий.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Чтение из журнала событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d0756ba7d9609bca285ce33d69738984badf7effff8867fc5c3e1943b09145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151543"
---
# <a name="reading-from-the-event-log"></a>Чтение из журнала событий

Приложение "Просмотр событий" использует функцию [**опеневентлог**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) , чтобы открыть журнал событий для источника событий. Затем средство просмотра событий может использовать функцию [**реадевентлог**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) для чтения записей событий из журнала. **Реадевентлог** возвращает буфер, содержащий структуру [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) , и дополнительные сведения, описывающие зарегистрированное событие. Этот процесс представлен на схеме ниже.

![чтение из журнала событий](images/readlog.png)

Пример кода см. в разделе [запросы сведений о событиях](querying-for-event-source-messages.md).

 

 



