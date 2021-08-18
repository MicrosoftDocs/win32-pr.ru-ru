---
title: Использование службы каталогов ячеек (компакт-дисков)
description: При наличии компакт-дисков его можно использовать вместо локатора Майкрософт.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- Удаленный вызов процедур RPC, задачи, использование службы каталогов ячеек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df9058d917396a4e2e2dc3579768c3f3d5b46242b34c0fa5411c6d2204ed20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010641"
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

 

 




