---
title: Разработка поставщика
description: Для записи событий, определенных в манифесте, используются функции, входящие в API трассировки событий (ETW). Дополнительные сведения о создании поставщика см. в разделе Предоставление событий.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdcbf17113eb926aba245f270b84e7ab50bf3072e15a9a7752b8828296a00a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937189"
---
# <a name="developing-a-provider"></a>Разработка поставщика

Для записи событий, определенных в манифесте, используются функции, входящие в API [трассировки событий](/windows/desktop/ETW/event-tracing-portal) (ETW). Дополнительные сведения о создании поставщика см. в разделе [предоставление событий](/windows/desktop/ETW/providing-events).

После записи поставщика используйте средство WevtUtil.exe для регистрации поставщика и схемы. дополнительные сведения об использовании WevtUtil см. в разделе [Windows средства журнала событий](windows-event-log-tools.md). Ниже показано, как использовать WevtUtil для регистрации поставщика и удаления регистрации.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```