---
title: Excel Макросы для управления точками подключения службы
description: точки подключения службы можно управлять с помощью простых макросов Excel.
ms.assetid: da8a7363-6814-4c26-b259-53e6f6ba98cd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f0f6d0897e7579fab45e5b952c3f03456f73a38183f07e87235f671f795763d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189622"
---
# <a name="excel-macros-for-managing-service-connection-points"></a>Excel Макросы для управления точками подключения службы

точки подключения службы можно управлять с помощью простых макросов Excel.

в следующем макросе Excel показаны минимальные требования для создания новой точки подключения службы.


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



в следующем макросе Excel показано, как удалить образец точки подключения службы.


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



 

 




