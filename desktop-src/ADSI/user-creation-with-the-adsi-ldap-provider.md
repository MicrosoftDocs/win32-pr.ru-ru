---
title: Создание пользователей с помощью поставщика LDAP ADSI
description: С помощью поставщика LDAP ADSI можно создать только глобальную учетную запись пользователя.
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- ADSI поставщика LDAP, объект User, создание пользователей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843bb5bc9d0696c3af7c5f06ce8c76123ae93c3a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104081832"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a><span data-ttu-id="e7764-104">Создание пользователей с помощью поставщика LDAP ADSI</span><span class="sxs-lookup"><span data-stu-id="e7764-104">User Creation with the ADSI LDAP Provider</span></span>

<span data-ttu-id="e7764-105">С помощью поставщика LDAP ADSI можно создать только глобальную учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7764-105">With the ADSI LDAP provider, you can only create a global user account.</span></span> <span data-ttu-id="e7764-106">Локальные учетные записи находятся в базе данных SAM и должны создаваться с помощью поставщика WinNT.</span><span class="sxs-lookup"><span data-stu-id="e7764-106">Local accounts reside in the SAM database and must be created using the WinNT provider.</span></span> <span data-ttu-id="e7764-107">Дополнительные сведения о создании объекта пользователя с помощью поставщика WinNT см. в разделе [объект пользователя WinNT](winnt-user-object.md).</span><span class="sxs-lookup"><span data-stu-id="e7764-107">For more information about creating a user object with the WinNT provider, see [WinNT User Object](winnt-user-object.md).</span></span>

<span data-ttu-id="e7764-108">**Создание объекта User**</span><span class="sxs-lookup"><span data-stu-id="e7764-108">**To create a user object**</span></span>

1.  <span data-ttu-id="e7764-109">Выполните привязку к контейнеру, где будет располагаться объект пользователя, и получите для контейнера интерфейс [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) или [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) .</span><span class="sxs-lookup"><span data-stu-id="e7764-109">Bind to the container where the user object will reside and obtain either the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) or [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for the container.</span></span>
2.  <span data-ttu-id="e7764-110">Чтобы создать объект пользователя, используйте метод [**иадсконтаинер. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) или [**Идиректорйобжект:: креатедсобжект**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="e7764-110">Use the [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) or [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method to create the user object.</span></span>
3.  <span data-ttu-id="e7764-111">Минимальные атрибуты, необходимые для создания объекта пользователя, зависят от используемой службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="e7764-111">The minimum attributes required to create a user object will depend on the directory service used.</span></span> <span data-ttu-id="e7764-112">Дополнительные сведения о создании Active Directory пользователя см. в разделе [Создание пользователя](/windows/desktop/AD/creating-a-user).</span><span class="sxs-lookup"><span data-stu-id="e7764-112">For more information about creating an Active Directory user, see [Creating a User](/windows/desktop/AD/creating-a-user).</span></span>
4.  <span data-ttu-id="e7764-113">Если используется интерфейс [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) , новый объект фактически не создается, пока не будет вызван метод [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="e7764-113">If the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface is used, the new object is not actually created until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

    <span data-ttu-id="e7764-114">Если используется интерфейс [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) , то новый объект создается при вызове метода [**креатедсобжект**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="e7764-114">If the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface is used, the new object is created when the [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method is called.</span></span> <span data-ttu-id="e7764-115">Минимальные атрибуты, включая [**objectClass**](/windows/desktop/ADSchema/a-objectclass), должны быть указаны в массиве [**\_ \_ сведений attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) , переданном в метод **креатедсобжект** .</span><span class="sxs-lookup"><span data-stu-id="e7764-115">The minimum attributes, including the [**objectClass**](/windows/desktop/ADSchema/a-objectclass), must be specified in the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) array passed to the **CreateDSObject** method.</span></span>

## <a name="example-1"></a><span data-ttu-id="e7764-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7764-116">Example 1</span></span>

<span data-ttu-id="e7764-117">В следующем примере кода создается учетная запись пользователя с атрибутами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7764-117">The following code example creates a user account with the default attributes.</span></span>


```VB
Dim ou As IADs
Dim usr as IADsUser

On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Finance,DC=Fabrikam,DC=COM")
Set usr = ou.Create("user", "cn=Jeff Smith")
usr.Put "samAccountName", "jeffsmith"
usr.SetInfo

Cleanup:
   If (Err.Number <> 0) Then
      MsgBox ("An error has occurred. " &  Err.Number)
   End If
   Set ou = Nothing
   Set usr = Nothing
```



## <a name="example-2"></a><span data-ttu-id="e7764-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e7764-118">Example 2</span></span>

<span data-ttu-id="e7764-119">В следующем примере кода создается учетная запись пользователя с атрибутами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7764-119">The following code example creates a user account with the default attributes.</span></span> <span data-ttu-id="e7764-120">Для краткости проверка ошибок пропущена.</span><span class="sxs-lookup"><span data-stu-id="e7764-120">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>

int main()
{
   HRESULT hr = CoInitialize(NULL);

   IADsContainer *pCont;
   IADsUser *pUser;

   LPWSTR adsPath = L"LDAP://serv1/CN=Users,dc=Fabrikam,dc=com";
   LPWSTR usrPass = NULL;
   LPWSTR usrName = NULL;

   // Add code to securely get the user name and password or leave
   // as NULL to use the current security context.

   hr = ADsOpenObject(adsPath, 
                      usrName,
                      usrPass,
                      ADS_SECURE_AUTHENTICATION,
                      IID_IADsContainer,
                      (void**)&pCont);

   IDispatch *pDisp;
   hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=Jeff Smith"), &pDisp);
   pCont->Release();

   hr = pDisp->QueryInterface(IID_IADsUser,(void**)&pUser);
   pDisp->Release();

   VARIANT var;
   VariantInit(&var);
   V_BSTR(&var) = L"jeffsmith";
   V_VT(&var)=VT_BSTR;
   hr = pUser->Put(CComBSTR("samAccountName"), var);

   hr = pUser->SetInfo();

   VariantClear(&var);
   pUser->Release();

   CoUninitialize();

   return 0;
}
```



 

 