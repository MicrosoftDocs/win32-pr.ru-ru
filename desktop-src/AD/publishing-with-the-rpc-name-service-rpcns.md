---
title: Публикация с помощью службы имен RPC
description: Службы RPC могут публиковать свои идентификаторы в пространстве имен с помощью API-интерфейсов службы имен RPC (Рпкнс).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Публикация с помощью службы имен RPC Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b672eec6308d709fe2f4cbc64ad22ecf0d6edd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069756"
---
# <a name="publishing-with-the-rpc-name-service"></a>Публикация с помощью службы имен RPC

Службы RPC могут публиковать свои идентификаторы в пространстве имен с помощью API-интерфейсов службы имен RPC (Рпкнс). API-интерфейсы Рпкнс в Windows 2000 публикуют записи RPC в домен Active Directory Services. Службы создают привязки RPC и публикуют их в пространстве имен как именованные записи RPC-сервера с атрибутами, включая уникальный идентификатор интерфейса, идентификатор GUID, распознаваемый клиентами. Затем клиент может выполнить поиск серверов RPC, предлагающих нужный интерфейс, импортировать привязку и подключиться к серверу.

Дополнительные сведения о публикации службы RPC см. в разделе [Привязка на стороне сервера](/windows/desktop/Rpc/server-side-binding).

 

 