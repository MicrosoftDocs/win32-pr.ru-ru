---
title: Разработка поставщика
description: Для записи событий, определенных в манифесте, используются функции, входящие в API трассировки событий (ETW). Дополнительные сведения о создании поставщика см. в разделе Предоставление событий.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134439"
---
# <a name="developing-a-provider"></a>Разработка поставщика

Для записи событий, определенных в манифесте, используются функции, входящие в API [трассировки событий](/windows/desktop/ETW/event-tracing-portal) (ETW). Дополнительные сведения о создании поставщика см. в разделе [предоставление событий](/windows/desktop/ETW/providing-events).

После записи поставщика используйте средство WevtUtil.exe для регистрации поставщика и схемы. Дополнительные сведения об использовании WevtUtil см. в разделе [средства журнала событий Windows](windows-event-log-tools.md). Ниже показано, как использовать WevtUtil для регистрации поставщика и удаления регистрации.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```