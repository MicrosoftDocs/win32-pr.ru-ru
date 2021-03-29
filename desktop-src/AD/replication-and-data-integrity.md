---
title: Репликация и целостность данных
description: Домен Active Directory Services обеспечивают обновление нескольких хозяев.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, использование, репликация и целостность данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654173"
---
# <a name="replication-and-data-integrity"></a>Репликация и целостность данных

Домен Active Directory Services обеспечивают *Обновление нескольких хозяев*. Обновление с несколькими хозяевами означает, что все полные реплики данного раздела доступны для записи (частичные реплики на серверах глобального каталога недоступны для записи). Обновление с несколькими хозяевами означает, что обновления не блокируются даже в том случае, если некоторые реплики неработоспособны. Сервер Active Directory распространяет изменения из обновленной реплики на все остальные реплики. Репликация является автоматической и прозрачной.

Дополнительные сведения см. в следующих разделах:

-   [Модель репликации в службах домен Active Directory](replication-model-in-active-directory-domain-services.md)
-   [Поведение репликации в службах домен Active Directory Services](replication-behavior-in-active-directory-domain-services.md)
-   [Обнаружение и предотвращение задержки репликации](detecting-and-avoiding-replication-latency.md)

 

 




