---
description: В диспетчере авторизации объект Иазаппликатионграуп представляет группу пользователей. Затем роли могут быть назначены этой группе пользователей в совокупности.
ms.assetid: 13950da1-b04f-4346-b216-9713cbdcd5b5
title: Определение групп пользователей в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b4931d3b35658539284305e98096d7ecfc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913059"
---
# <a name="defining-groups-of-users-in-c"></a><span data-ttu-id="e6391-104">Определение групп пользователей в C++</span><span class="sxs-lookup"><span data-stu-id="e6391-104">Defining Groups of Users in C++</span></span>

<span data-ttu-id="e6391-105">В диспетчере авторизации объект [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) представляет группу пользователей.</span><span class="sxs-lookup"><span data-stu-id="e6391-105">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="e6391-106">Затем роли могут быть назначены этой группе пользователей в совокупности.</span><span class="sxs-lookup"><span data-stu-id="e6391-106">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="e6391-107">Объект [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) может также включать другие объекты **иазаппликатионграуп** в качестве членов.</span><span class="sxs-lookup"><span data-stu-id="e6391-107">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="e6391-108">Дополнительные сведения о группах приложений см. в разделе [Пользователи и группы](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="e6391-108">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="e6391-109">Группа может быть определена либо явными списками членов, либо нечленами, либо запросом LDAP. [](/windows/desktop/SecGloss/l-gly)</span><span class="sxs-lookup"><span data-stu-id="e6391-109">A group can be defined either by explicit lists of members and nonmembers, or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="e6391-110">В следующих примерах показано, как создать каждый тип группы приложений:</span><span class="sxs-lookup"><span data-stu-id="e6391-110">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="e6391-111">Создание базовой группы</span><span class="sxs-lookup"><span data-stu-id="e6391-111">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="e6391-112">Создание группы запросов LDAP</span><span class="sxs-lookup"><span data-stu-id="e6391-112">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="e6391-113">Создание базовой группы</span><span class="sxs-lookup"><span data-stu-id="e6391-113">Creating a Basic Group</span></span>

<span data-ttu-id="e6391-114">Базовая группа приложений определяется членами, включенными в свойства [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) [**и Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) объекта [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , представляющего группу.</span><span class="sxs-lookup"><span data-stu-id="e6391-114">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="e6391-115">Пользователи и группы, перечисленные в свойстве **Members** , включаются в группу приложений, а пользователи и группы, перечисленные в свойстве **нечленов** , исключаются из группы приложений.</span><span class="sxs-lookup"><span data-stu-id="e6391-115">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="e6391-116">Перечисление в свойстве, не входящих в список **Members** , заменяется в свойстве **Members** .</span><span class="sxs-lookup"><span data-stu-id="e6391-116">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="e6391-117">В следующем примере показано, как создать базовую группу приложений и добавить всех локальных пользователей в качестве членов этой группы.</span><span class="sxs-lookup"><span data-stu-id="e6391-117">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="e6391-118">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C.</span><span class="sxs-lookup"><span data-stu-id="e6391-118">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif
#pragma comment(lib, "duser.lib")

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR sidString = NULL;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    //  Create null VARIANT for parameters.
    VARIANT myVar; 
    VariantInit(&myVar);

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Add well-known SID for all local users to the group.
    if (!(sidString = SysAllocString(L"S-1-2-0")))
        MyHandleError("Could not allocate SID string name");
    hr = pAppGroup->AddMember(sidString, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add member to group");

    //  Save changes to the store.
    pAppGroup->Submit(0, myVar);

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(sidString);
    VariantClear(&myVar);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="e6391-119">Создание группы запросов LDAP</span><span class="sxs-lookup"><span data-stu-id="e6391-119">Creating an LDAP Query Group</span></span>

<span data-ttu-id="e6391-120">Группа запросов LDAP имеет членство, определенное запросом, содержащимся в значении его свойства [**лдапкуери**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .</span><span class="sxs-lookup"><span data-stu-id="e6391-120">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="e6391-121">В следующем примере показано, как создать группу приложений запросов LDAP и добавить всех пользователей в качестве членов этой группы.</span><span class="sxs-lookup"><span data-stu-id="e6391-121">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="e6391-122">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C.</span><span class="sxs-lookup"><span data-stu-id="e6391-122">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif
#pragma comment(lib, "duser.lib")

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR ldapString = NULL;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users3")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Set the Type property to AZ_GROUPTYPE_LDAP_QUERY.
    hr = pAppGroup->put_Type(AZ_GROUPTYPE_LDAP_QUERY);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Error changing type to LDAP query");

    //  Add LDAP query for all users.
    if (!(ldapString =
   SysAllocString(L"(&(objectCategory=person)(objectClass=user))")))
        MyHandleError("Could not allocate LDAP query string");
    hr = pAppGroup->put_LdapQuery(ldapString);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add query to group");

    //  Save changes to the store.
    hr = pAppGroup->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save changes to store.");

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(ldapString);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 
