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
# <a name="using-the-cell-directory-service-cds"></a><span data-ttu-id="06b9f-104">Использование службы каталогов ячеек (компакт-дисков)</span><span class="sxs-lookup"><span data-stu-id="06b9f-104">Using the Cell Directory Service (CDS)</span></span>

<span data-ttu-id="06b9f-105">При наличии компакт-дисков его можно использовать вместо локатора Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="06b9f-105">If you have CDS, you can use it instead of Microsoft Locator.</span></span> <span data-ttu-id="06b9f-106">Измените записи реестра, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="06b9f-106">Change the registry entries as shown:</span></span>

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

<span data-ttu-id="06b9f-107">Изменение этих записей будет указывать на компьютер шлюза, на котором выполняется НСИД.</span><span class="sxs-lookup"><span data-stu-id="06b9f-107">Changing these entries will point to a gateway computer that is running the NSID.</span></span> <span data-ttu-id="06b9f-108">Он будет использоваться в качестве основного локатора.</span><span class="sxs-lookup"><span data-stu-id="06b9f-108">This will be used as the master locator.</span></span> <span data-ttu-id="06b9f-109">В случае сбоя поиск замены не будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="06b9f-109">In the event of a crash, there will be no search for a replacement.</span></span>

 

 




