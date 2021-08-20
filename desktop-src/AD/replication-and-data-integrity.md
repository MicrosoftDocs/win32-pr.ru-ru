---
title: Репликация и целостность данных
description: Домен Active Directory Services обеспечивают обновление нескольких хозяев.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, использование, репликация и целостность данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ec62ec3e44b9252d2d186b690105623b338bdaedf6ed15e4a253bfc2f06927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184459"
---
# <a name="replication-and-data-integrity"></a>Репликация и целостность данных

Домен Active Directory Services обеспечивают *Обновление нескольких хозяев*. Обновление с несколькими хозяевами означает, что все полные реплики данного раздела доступны для записи (частичные реплики на серверах глобального каталога недоступны для записи). Обновление с несколькими хозяевами означает, что обновления не блокируются даже в том случае, если некоторые реплики неработоспособны. Сервер Active Directory распространяет изменения из обновленной реплики на все остальные реплики. Репликация является автоматической и прозрачной.

Дополнительные сведения см. в следующих статьях.

-   [Модель репликации в службах домен Active Directory](replication-model-in-active-directory-domain-services.md)
-   [Поведение репликации в службах домен Active Directory Services](replication-behavior-in-active-directory-domain-services.md)
-   [Обнаружение и предотвращение задержки репликации](detecting-and-avoiding-replication-latency.md)

 

 




