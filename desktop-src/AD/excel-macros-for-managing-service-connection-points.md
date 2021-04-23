---
title: Макросы Excel для управления точками подключения службы
description: Точки подключения службы можно управлять с помощью простых макросов Excel.
ms.assetid: da8a7363-6814-4c26-b259-53e6f6ba98cd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69bc3561962b063c9128d46934d3cb87b84e0a24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654190"
---
# <a name="excel-macros-for-managing-service-connection-points"></a><span data-ttu-id="2a77c-103">Макросы Excel для управления точками подключения службы</span><span class="sxs-lookup"><span data-stu-id="2a77c-103">Excel Macros for Managing Service Connection Points</span></span>

<span data-ttu-id="2a77c-104">Точки подключения службы можно управлять с помощью простых макросов Excel.</span><span class="sxs-lookup"><span data-stu-id="2a77c-104">Service Connection Points can be managed using simple Excel Macros.</span></span>

<span data-ttu-id="2a77c-105">В следующем макросе Excel показаны минимальные требования к созданию новой точки подключения службы.</span><span class="sxs-lookup"><span data-stu-id="2a77c-105">The following Excel Macro shows the minimum requirements for creating a new Service Connection Point.</span></span>


```VB
Option Explicit

Private Sub p_CreateExampleSCP()

    Dim oAdSysInfo As ADSystemInfo
    Set oAdSysInfo = CreateObject("ADSystemInfo")
    
    Dim objComputer As ActiveDs.IADsContainer
    Set objComputer = GetObject("LDAP://" + oAdSysInfo.ComputerName)
    
    Dim IADsSCP As ActiveDs.IADs
    Set IADsSCP = objComputer.Create("ServiceConnectionPoint", _
                                "CN=Example SCP")
    
    IADsSCP.PutEx 2, "serviceBindingInformation", _
                    Array( _
                        " - UNC connection to Service", _
                        " - WS-Man connection to service" _
                    )
                    
    IADsSCP.PutEx 2, "Keywords", _
                    Array( _
                        "KW1=A kewyrowd value" _
                    )
                    
    IADsSCP.SetInfo

End Sub
```



<span data-ttu-id="2a77c-106">В следующем макросе Excel показано, как удалить образец точки подключения службы.</span><span class="sxs-lookup"><span data-stu-id="2a77c-106">The following Excel Macro shows how to delete the sample Service Connection Point.</span></span>


```VB
Option Explicit

Private Sub p_DeleteExampleScp()
    Dim oAdSysInfo As ADSystemInfo
    Set oAdSysInfo = CreateObject("ADSystemInfo")
    
    Dim objComputer As ActiveDs.IADsContainer
    Set objComputer = GetObject("LDAP://" + oAdSysInfo.ComputerName)

    objComputer.Delete "ServiceConnectionPoint", _
                        "CN=Example SCP"

End Sub
```



 

 




