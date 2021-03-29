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
ms.openlocfilehash: 4f0b652530167c71fbea7bc23d27434ae458f9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348935"
---
# <a name="defining-groups-of-users-in-script"></a><span data-ttu-id="f3fb0-105">Определение групп пользователей в сценарии</span><span class="sxs-lookup"><span data-stu-id="f3fb0-105">Defining Groups of Users in Script</span></span>

<span data-ttu-id="f3fb0-106">В диспетчере авторизации объект [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) представляет группу пользователей.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-106">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="f3fb0-107">Затем роли могут быть назначены этой группе пользователей в совокупности.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-107">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="f3fb0-108">Объект **иазаппликатионграуп** может также включать другие объекты **иазаппликатионграуп** в качестве членов.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-108">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="f3fb0-109">Дополнительные сведения о группах приложений см. в разделе [Пользователи и группы](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="f3fb0-109">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="f3fb0-110">Группа может быть определена либо явными списками членов, либо нечленами, либо [](/windows/desktop/SecGloss/l-gly) запросом LDAP.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-110">A group can be defined either by explicit lists of members and nonmembers or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="f3fb0-111">В следующих примерах показано, как создать каждый тип группы приложений:</span><span class="sxs-lookup"><span data-stu-id="f3fb0-111">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="f3fb0-112">Создание базовой группы</span><span class="sxs-lookup"><span data-stu-id="f3fb0-112">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="f3fb0-113">Создание группы запросов LDAP</span><span class="sxs-lookup"><span data-stu-id="f3fb0-113">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="f3fb0-114">Создание базовой группы</span><span class="sxs-lookup"><span data-stu-id="f3fb0-114">Creating a Basic Group</span></span>

<span data-ttu-id="f3fb0-115">Базовая группа приложений определяется членами, включенными в свойства [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) [**и Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) объекта [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , представляющего группу.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-115">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="f3fb0-116">Пользователи и группы, перечисленные в свойстве **Members** , включаются в группу приложений, а пользователи и группы, перечисленные в свойстве **нечленов** , исключаются из группы приложений.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-116">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="f3fb0-117">Перечисление в свойстве, не входящих в список **Members** , заменяется в свойстве **Members** .</span><span class="sxs-lookup"><span data-stu-id="f3fb0-117">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="f3fb0-118">В следующем примере показано, как создать базовую группу приложений и добавить всех локальных пользователей в качестве членов этой группы.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-118">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="f3fb0-119">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-119">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="f3fb0-120">Создание группы запросов LDAP</span><span class="sxs-lookup"><span data-stu-id="f3fb0-120">Creating an LDAP Query Group</span></span>

<span data-ttu-id="f3fb0-121">Группа запросов LDAP имеет членство, определенное запросом, содержащимся в значении его свойства [**лдапкуери**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .</span><span class="sxs-lookup"><span data-stu-id="f3fb0-121">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="f3fb0-122">В следующем примере показано, как создать группу приложений запросов LDAP и добавить всех пользователей в качестве членов этой группы.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-122">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="f3fb0-123">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-123">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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



 

 
