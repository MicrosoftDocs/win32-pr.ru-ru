---
description: Active Directory объекты можно использовать для нахождение ресурсов в домене сети компьютера, например пользователей, политик безопасности, принтеров, распределенных компонентов и других ресурсов.
ms.assetid: 96f89537-9419-495e-819c-fd07ba546620
ms.tgt_platform: multiple
title: Создание и обновление объектов Active Directory
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0b36a12860ea2c2dc9085b784fdaf85cd95ab87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702077"
---
# <a name="creating-and-updating-active-directory-objects"></a>Создание и обновление объектов Active Directory

Active Directory объекты можно использовать для нахождение ресурсов в домене сети компьютера, например пользователей, политик безопасности, принтеров, распределенных компонентов и других ресурсов. Active Directory объекты можно создавать и обновлять с помощью WMI. Можно обновить объект Active Directory, когда новые сведения о объекте становятся доступными с помощью уведомления о событии WMI. Например, после создания объекта пользователя Active Directory можно определить его создание с помощью запроса события в WMI, а также при получении события можно обновить объект новыми данными.

В следующем примере кода создается новый экземпляр WMI класса, представляющий объект Active Directory User. В примере показано, как присвоить значения различным свойствам, необходимым для создания нового Active Directory пользовательского экземпляра.


```VB
Const cUserID = "WMIUser"
Const cComputerName = "LocalHost"
Const cWMInamespace = "root/directory/LDAP"
Const cWMIclass = "ds_user"

Const ADS_UF_ACCOUNTDISABLE = &h000002

Set objWMILocator = _
    CreateObject("WbemScripting.SWbemLocator")
objWMILocator.Security_.AuthenticationLevel = _
    wbemAuthenticationLevelDefault

Set objWMIServices = objWMILocator. _
    ConnectServer(cComputerName, cWMInamespace, "", "")

Set objWMIClass = objWMIServices.Get(cWMIclass)

Set objWMIInstance = objWMIClass.SpawnInstance_

objWMIInstance.DS_sAMAccountName = userID
objWMIInstance.ADSIPath = "LDAP://CN=" & userID & _
    ",CN=Users,DC=LissWare,DC=Net"

objWMIInstance.Put_ (wbemChangeFlagCreateOrUpdate Or _
    wbemFlagReturnWhenComplete)

WScript.Echo "Active Directory user created."
```



В следующем примере кода обновляется экземпляр WMI объекта Active Directory. В этом примере обновляется атрибут DisplayName.


```VB
set svc = getObject("Winmgmts:root\directory\ldap")

' A context object is used to tell the provider which
' specific properties are going to be updated.  
' In most cases, when you update a WMI object you do not
' need to specify an additional context object. 
' However,  if a context object is not supplied for a
' directory service provider, the update fails.

set octx = createobject( _
    "wbemscripting.swbemnamedvalueset")
octx.add "__PUT_EXT_PROPERTIES", array("ds_displayname")
octx.add "__PUT_EXTENSIONS", true
octx.add "__PUT_EXT_CLIENT_REQUEST", true


set objEnum = svc.execQuery( _
    "select * from ds_computer where ds_cn = 'userName'", "WQL", 32)

for each obj in objEnum
 obj.ds_DisplayName = "updatedName"
 obj.put_ 1, octx
next

WScript.Echo "Active Directory user successfully updated"
```



 

 



