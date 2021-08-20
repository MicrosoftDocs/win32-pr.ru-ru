---
title: Пример значений реестра
description: В следующем примере показаны возможные данные для некоторых значений реестра протокола проверки подлинности.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8a8bc87ef728d2524f9e7f21ad6ff69f1dd58ccee8d4836d8a2ceef4c676e00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118087015"
---
# <a name="registry-values-example"></a>Пример значений реестра

В следующем примере показаны возможные данные для некоторых значений реестра протокола проверки подлинности.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| Имя ключа            | Datatype        | Значение                                  |
|---------------------|-----------------|----------------------------------------|
| Путь                | \_распаковать \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| FriendlyName        | REG \_ SZ         | Пример протокола EAP                    |
| конфигуипас        | \_распаковать \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| идентитипас        | \_распаковать \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| интерактивеуипас   | \_распаковать \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| рекуиреконфигуи     | REG \_ DWORD      | 1                                      |
| конфигклсид         | REG \_ SZ         | {0000031A-0000-0000-C000-000000000046} |
| стандалонесуппортед | REG \_ DWORD      | 1                                      |



 

 

 




