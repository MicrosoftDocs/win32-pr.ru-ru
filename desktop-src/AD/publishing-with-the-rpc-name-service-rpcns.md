---
title: Публикация с помощью службы имен RPC
description: Службы RPC могут публиковать свои идентификаторы в пространстве имен с помощью API-интерфейсов службы имен RPC (Рпкнс).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Публикация с помощью службы имен RPC Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd53922bd4ce952c18c58d1b71cb485887bdc0fd020f4113679eb114b32b6f3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025372"
---
# <a name="publishing-with-the-rpc-name-service"></a>Публикация с помощью службы имен RPC

Службы RPC могут публиковать свои идентификаторы в пространстве имен с помощью API-интерфейсов службы имен RPC (Рпкнс). api-интерфейсы рпкнс в Windows 2000 публикуют записи RPC в службах домен Active Directory. Службы создают привязки RPC и публикуют их в пространстве имен как именованные записи RPC-сервера с атрибутами, включая уникальный идентификатор интерфейса, идентификатор GUID, распознаваемый клиентами. Затем клиент может выполнить поиск серверов RPC, предлагающих нужный интерфейс, импортировать привязку и подключиться к серверу.

Дополнительные сведения о публикации службы RPC см. в разделе [Привязка на стороне сервера](/windows/desktop/Rpc/server-side-binding).

 

 