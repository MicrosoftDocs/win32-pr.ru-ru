---
description: Объект Иазаппликатионграуп представляет группу пользователей. Затем роли могут быть назначены этой группе пользователей в совокупности. Объект Иазаппликатионграуп может также включать другие объекты Иазаппликатионграуп в качестве членов.
ms.assetid: 8b445419-7316-4034-b742-a05845af1862
title: Определение групп пользователей в сценарии
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6198d31a53dbd7d30100a8df56536cf0336c9c1e7ca5b78ad4e9e73e40da13cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913990"
---
# <a name="defining-groups-of-users-in-script"></a>Определение групп пользователей в сценарии

В диспетчере авторизации объект [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) представляет группу пользователей. Затем роли могут быть назначены этой группе пользователей в совокупности. Объект **иазаппликатионграуп** может также включать другие объекты **иазаппликатионграуп** в качестве членов. Дополнительные сведения о группах приложений см. в разделе [Пользователи и группы](users-and-groups.md).

Группа может быть определена либо явными списками членов, либо нечленами, либо [](/windows/desktop/SecGloss/l-gly) запросом LDAP. В следующих примерах показано, как создать каждый тип группы приложений:

-   [Создание базовой группы](#creating-a-basic-group)
-   [Создание группы запросов LDAP](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>Создание базовой группы

Базовая группа приложений определяется членами, включенными в свойства [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) [**и Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) объекта [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , представляющего группу. Пользователи и группы, перечисленные в свойстве **Members** , включаются в группу приложений, а пользователи и группы, перечисленные в свойстве **нечленов** , исключаются из группы приложений. Перечисление в свойстве, не входящих в список **Members** , заменяется в свойстве **Members** .

В следующем примере показано, как создать базовую группу приложений и добавить всех локальных пользователей в качестве членов этой группы. В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Trusted Users")

'  Add a well-known SID for all local users to the group.
appGroup.AddMember("S-1-1-0")

'  Save the application group to the store.
appGroup.Submit
```



## <a name="creating-an-ldap-query-group"></a>Создание группы запросов LDAP

Группа запросов LDAP имеет членство, определенное запросом, содержащимся в значении его свойства [**лдапкуери**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .

В следующем примере показано, как создать группу приложений запросов LDAP и добавить всех пользователей в качестве членов этой группы. В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("LDAP Trusted Users")

'  Set the Type property of the group to two
'  (AZ_GROUPTYPE_LDAP_QUERY).
appGroup.Type = 2

'  Add LDAP query for all users.
appGroup.LdapQuery = ("&(objectCategory=person)(objectClass=user)")

'  Save the application group to the store.
appGroup.Submit

```



 

 
