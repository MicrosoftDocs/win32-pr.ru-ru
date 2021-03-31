---
title: Пример значений реестра
description: В следующем примере показаны возможные данные для некоторых значений реестра протокола проверки подлинности.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104069412"
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



 

 

 




