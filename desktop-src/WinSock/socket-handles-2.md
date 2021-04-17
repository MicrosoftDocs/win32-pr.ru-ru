---
description: При необходимости маркером сокета может быть описатель файла в сокетах Windows 2. Маркер сокета от поставщика Winsock можно использовать с другими функциями, отличными от Winsock, такими как ReadFile, WriteFile, Реадфиликс и Вритефиликс.
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: Дескрипторы сокетов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6ca8ed935819e018a59c52fb43dcf816530c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711766"
---
# <a name="socket-handles"></a>Дескрипторы сокетов

При необходимости маркером сокета может быть описатель файла в сокетах Windows 2. Маркер сокета от поставщика Winsock можно использовать с другими функциями, отличными от Winsock, такими как [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**реадфиликс**](/windows/win32/api/fileapi/nf-fileapi-readfileex)и [**вритефиликс**](/windows/win32/api/fileapi/nf-fileapi-writefileex).

Элемент **XP1 \_ IFS \_ Handles** в структуре сведений о протоколе для поставщика определяет, является ли дескриптор сокета поставщика подсистемой для установки файловой системы (IFS). Дескрипторы сокетов, которые являются дескрипторами IFS, можно использовать без снижения производительности с другими функциями, отличными от Winsock (например,[**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) и [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile)). Любые дескрипторы сокетов, не относящихся к IFS, при использовании с функциями, отличными от Winsock (например,**ReadFile** и **WriteFile**), приводят к взаимодействию между поставщиком и файловой системой, в которой участвуют дополнительные издержки на обработку, что может привести к значительному снижению производительности. При использовании дескрипторов сокетов с функциями, отличными от Winsock, коды ошибок, распространяемые из базовой файловой системы, не всегда сопоставляются с кодами ошибок Winsock. Поэтому рекомендуется использовать дескрипторы сокетов только с функциями Winsock.

Не следует использовать маркер сокета с функцией [**дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) . Наличие многоуровневых поставщиков служб (LSP) может привести к сбою, и процесс назначения не сможет импортировать маркер сокета.

> [!Note]  
> Многоуровневые поставщики служб являются устаревшими. Начиная с Windows 8 и Windows Server 2012, используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).

 

Сокеты Windows 2 развернули некоторые функции, которые передают данные между сокетами с помощью дескрипторов. Функции предоставляют преимущества, характерные для сокетов для передачи данных и включают [**всарекв**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**всасенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)и [**всадупликатесоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa).

 

 
