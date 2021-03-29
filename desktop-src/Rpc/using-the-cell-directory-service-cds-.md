---
title: Использование службы каталогов ячеек (компакт-дисков)
description: При наличии компакт-дисков его можно использовать вместо локатора Майкрософт.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- Удаленный вызов процедур RPC, задачи, использование службы каталогов ячеек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0029bf78308d6963d615daa04eaf87f3617ebbb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776118"
---
# <a name="using-the-cell-directory-service-cds"></a>Использование службы каталогов ячеек (компакт-дисков)

При наличии компакт-дисков его можно использовать вместо локатора Майкрософт. Измените записи реестра, как показано ниже.

``` syntax
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    NetworkAddress
 
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    Endpoint
```

Изменение этих записей будет указывать на компьютер шлюза, на котором выполняется НСИД. Он будет использоваться в качестве основного локатора. В случае сбоя поиск замены не будет выполняться.

 

 




