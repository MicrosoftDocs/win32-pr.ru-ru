---
title: Изменение пользователя не может изменить пароль (поставщик LDAP)
description: Возможность изменения собственного пароля пользователем — это разрешение, которое может быть предоставлено или запрещено.
ms.assetid: 9d5c2d6a-9997-4d0c-b896-bf1b578e64ac
ms.tgt_platform: multiple
keywords:
- Изменение пользователя не может изменить пароль (поставщик LDAP) ADSI
- Пользователь не может изменять пароль (поставщик LDAP) ADSI, изменение
- Поставщик LDAP ADSI, примеры управления пользователями, пользователь должен сменить пароль при следующем входе в систему, изменить
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1628b113c2f15278bc72e41aa79e4be03a98f2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793855"
---
# <a name="modifying-user-cannot-change-password-ldap-provider"></a><span data-ttu-id="51c89-106">Изменение пользователя не может изменить пароль (поставщик LDAP)</span><span class="sxs-lookup"><span data-stu-id="51c89-106">Modifying User Cannot Change Password (LDAP Provider)</span></span>

<span data-ttu-id="51c89-107">Возможность изменения собственного пароля пользователем — это разрешение, которое может быть предоставлено или запрещено.</span><span class="sxs-lookup"><span data-stu-id="51c89-107">The ability of a user to change their own password is a permission that can be grant or denied.</span></span> <span data-ttu-id="51c89-108">Чтобы запретить это разрешение, установите два элемента ACE в списке управления доступом на уровне пользователей (DACL) для объекта пользователя с типом ACE **AD \_ ACETYPE \_ доступ \_ запрещенный \_ объект** .</span><span class="sxs-lookup"><span data-stu-id="51c89-108">To deny this permission, set two ACEs in the security descriptor discretionary access control list (DACL) of the user object with the **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** ace type.</span></span> <span data-ttu-id="51c89-109">Одна запись ACE запрещает пользователю разрешение, а другая ACE запрещает разрешение для группы «все».</span><span class="sxs-lookup"><span data-stu-id="51c89-109">One ACE denies the permission to the user and another ACE denies the permission to the Everyone group.</span></span> <span data-ttu-id="51c89-110">Оба элемента ACE — это отклонения ACE для конкретного объекта, которые указывают идентификатор GUID расширенного разрешения на смену паролей.</span><span class="sxs-lookup"><span data-stu-id="51c89-110">Both ACEs are object-specific deny ACEs that specify the GUID of the extended permission for changing passwords.</span></span> <span data-ttu-id="51c89-111">Чтобы предоставить это разрешение, задайте те же записи ACE с типом ACE **AD \_ ACETYPE \_ Access \_ Allowed \_ Object** .</span><span class="sxs-lookup"><span data-stu-id="51c89-111">To grant this permission, set the same ACEs with the **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** ace type.</span></span>

<span data-ttu-id="51c89-112">В следующей процедуре описывается, как изменить или добавить ACE для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="51c89-112">The following procedure describes how to modify or add ACEs for this permission.</span></span>

<span data-ttu-id="51c89-113">**Изменение или добавление записей ACE для этого разрешения**</span><span class="sxs-lookup"><span data-stu-id="51c89-113">**To modify or add the ACEs for this permission**</span></span>

1.  <span data-ttu-id="51c89-114">Привязка к объекту пользователя.</span><span class="sxs-lookup"><span data-stu-id="51c89-114">Bind to the user object.</span></span>
2.  <span data-ttu-id="51c89-115">Получите объект [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) из свойства **нтсекуритидескриптор** объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="51c89-115">Obtain the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) object from the **ntSecurityDescriptor** property of the user object.</span></span>
3.  <span data-ttu-id="51c89-116">Получите интерфейс [**иадсакцессконтроллист**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) для дескриптора безопасности из свойства [**иадссекуритидескриптор. дискретионарякл**](iadssecuritydescriptor-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="51c89-116">Obtain an [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) interface for the security descriptor from the [**IADsSecurityDescriptor.DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) property.</span></span>
4.  <span data-ttu-id="51c89-117">Перечислите записи ACE для объекта и выполните поиск записей ACE с изменением GUID пароля ({AB721A53-1E2F-11D0-9819-00AA0040529B}) для свойства [**иадсакцессконтролентри. ObjectType**](iadsaccesscontrolentry-property-methods.md) и "Everyone" или "NT Authority \\ Self" для свойства **иадсакцессконтролентри. опекун** .</span><span class="sxs-lookup"><span data-stu-id="51c89-117">Enumerate the ACEs for the object and search for the ACEs that have the change password GUID ({AB721A53-1E2F-11D0-9819-00AA0040529B}) for the [**IADsAccessControlEntry.ObjectType**](iadsaccesscontrolentry-property-methods.md) property and "Everyone" or "NT AUTHORITY\\SELF" for the **IADsAccessControlEntry.Trustee** property.</span></span>

    > [!Note]  
    > <span data-ttu-id="51c89-118">Строки "все" и "самоцентр NT \\ " локализуются на основе языка первого контроллера домена в домене.</span><span class="sxs-lookup"><span data-stu-id="51c89-118">The "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="51c89-119">По этой причине строки не следует использовать напрямую.</span><span class="sxs-lookup"><span data-stu-id="51c89-119">Because of this, the strings should not be used directly.</span></span> <span data-ttu-id="51c89-120">Имена учетных записей должны быть получены во время выполнения путем вызова функции [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) с идентификатором безопасности для хорошо известных субъектов безопасности ("s-1-1-0") и "NT Authority" \\ ("s-1-5-10").</span><span class="sxs-lookup"><span data-stu-id="51c89-120">The account names should be obtained at run time by calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function with the SID for "Everyone" ("S-1-1-0") and "NT AUTHORITY\\SELF" ("S-1-5-10") well-known security principals.</span></span> <span data-ttu-id="51c89-121">Примеры функций **жетсидаккаунтнаме**, **Жетсидаккаунтнаме \_ Everyone** и **жетсидаккаунтнаме \_ Self** C++, показанные в статье [Чтение пользователя, не могут изменить пароль (поставщик LDAP)](reading-user-cannot-change-password-ldap-provider.md) демонстрируют, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="51c89-121">The **GetSidAccountName**, **GetSidAccountName\_Everyone**, and **GetSidAccountName\_Self** C++ example functions shown in [Reading User Cannot Change Password (LDAP Provider)](reading-user-cannot-change-password-ldap-provider.md) demonstrate how to do this.</span></span>

     

5.  <span data-ttu-id="51c89-122">Измените свойство [**иадсакцессконтролентри. AceType**](iadsaccesscontrolentry-property-methods.md) записей ACE, найденных в **ADS \_ AceType \_ доступ \_ \_** , если пользователь не может изменить пароль или **рекламу \_ AceType \_ доступ к \_ разрешенному \_ объекту** , если пользователь может изменить свой пароль.</span><span class="sxs-lookup"><span data-stu-id="51c89-122">Modify the [**IADsAccessControlEntry.AceType**](iadsaccesscontrolentry-property-methods.md) property of the ACEs that were found to **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** if the user cannot change their password or **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** if the user can change their password.</span></span>
6.  <span data-ttu-id="51c89-123">Если элемент управления доступом "все" не найден, создайте новый объект [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , содержащий значения свойств, показанные в таблице ниже, и добавьте новую запись в список управления доступом с помощью метода [**иадсакцессконтроллист. аддаце**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .</span><span class="sxs-lookup"><span data-stu-id="51c89-123">If the "Everyone" ACE is not found, create a new [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object that contains the property values shown in the table below and add the new entry to the ACL with the [**IADsAccessControlList.AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) method.</span></span>
7.  <span data-ttu-id="51c89-124">Если элемент управления доступом "самоцентр NT \\ " не найден, создайте новый объект [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) с теми же значениями свойств, приведенными в таблице ниже, за исключением того, что свойство " [**доверенное лицо**](iadsaccesscontrolentry-property-methods.md) " содержит имя учетной записи для SID "S-1-5-10" ("NT Authority \\ Self").</span><span class="sxs-lookup"><span data-stu-id="51c89-124">If the "NT AUTHORITY\\SELF" ACE is not found, create a new [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object with the same property values shown in the table below except the [**Trustee**](iadsaccesscontrolentry-property-methods.md) property contains the account name for SID "S-1-5-10" ("NT AUTHORITY\\SELF").</span></span> <span data-ttu-id="51c89-125">Добавьте запись в список управления доступом с помощью метода [**иадсакцессконтроллист. аддаце**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .</span><span class="sxs-lookup"><span data-stu-id="51c89-125">Add the entry to the ACL with the [**IADsAccessControlList.AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) method.</span></span>
8.  <span data-ttu-id="51c89-126">Чтобы обновить свойство **нтсекуритидескриптор** объекта, вызовите метод [**iAds. разместил**](/windows/desktop/api/Iads/nf-iads-iads-put) с тем же [**Иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) , полученным на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="51c89-126">To update the **ntSecurityDescriptor** property of the object, call the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method with the same [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtained in Step 2.</span></span>
9.  <span data-ttu-id="51c89-127">Зафиксируйте локальные изменения на сервере с помощью метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="51c89-127">Commit the local changes to the server with the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span>
10. <span data-ttu-id="51c89-128">Если был создан любой из записей ACE, необходимо переупорядочить список управления доступом, чтобы записи ACE находились в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="51c89-128">If either of the ACEs were created, you must reorder the ACL so that the ACEs are in the correct order.</span></span> <span data-ttu-id="51c89-129">Для этого вызовите функцию [**жетнамедсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) с параметром LDAP ADsPath объекта, а затем функцию [**сетнамедсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) с тем же списком DACL.</span><span class="sxs-lookup"><span data-stu-id="51c89-129">To do this, call the [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) function with the LDAP ADsPath of the object and then the [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) function with the same DACL.</span></span> <span data-ttu-id="51c89-130">Эта Переупорядочение выполняется автоматически при добавлении записей ACE.</span><span class="sxs-lookup"><span data-stu-id="51c89-130">This reordering will occur automatically when the ACEs are added.</span></span>

<span data-ttu-id="51c89-131">В следующей таблице перечислены значения свойств объекта [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="51c89-131">The following table lists the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object property values.</span></span>



| <span data-ttu-id="51c89-132">Иадсакцессконтролентри, свойство</span><span class="sxs-lookup"><span data-stu-id="51c89-132">IADsAccessControlEntry Property</span></span>                                        | <span data-ttu-id="51c89-133">Значение</span><span class="sxs-lookup"><span data-stu-id="51c89-133">Value</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51c89-134">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="51c89-134">**AccessMask**</span></span>](iadsaccesscontrolentry-property-methods.md)          | <span data-ttu-id="51c89-135">**AD \_ , \_ права \_ \_ доступа к управлению DS**</span><span class="sxs-lookup"><span data-stu-id="51c89-135">**ADS\_RIGHT\_DS\_CONTROL\_ACCESS**</span></span>                                                                                                                                   |
| [<span data-ttu-id="51c89-136">**AceType**</span><span class="sxs-lookup"><span data-stu-id="51c89-136">**AceType**</span></span>](iadsaccesscontrolentry-property-methods.md)             | <span data-ttu-id="51c89-137">**Реклама \_ ACETYPE \_ отказ в доступе \_ \_** , если пользователь не может изменить пароль или **ADS \_ ACETYPE \_ доступ к \_ разрешенному \_ объекту** , если пользователь может изменить свой пароль.</span><span class="sxs-lookup"><span data-stu-id="51c89-137">**ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** if the user cannot change their password or **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** if the user can change their password.</span></span> |
| [<span data-ttu-id="51c89-138">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="51c89-138">**AceFlags**</span></span>](iadsaccesscontrolentry-property-methods.md)            | <span data-ttu-id="51c89-139">0</span><span class="sxs-lookup"><span data-stu-id="51c89-139">0</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="51c89-140">**Метки**</span><span class="sxs-lookup"><span data-stu-id="51c89-140">**Flags**</span></span>](iadsaccesscontrolentry-property-methods.md)               | <span data-ttu-id="51c89-141">**\_ \_ \_ имеется тип объекта флага ADS \_**</span><span class="sxs-lookup"><span data-stu-id="51c89-141">**ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**</span></span>                                                                                                                                  |
| [<span data-ttu-id="51c89-142">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="51c89-142">**ObjectType**</span></span>](iadsaccesscontrolentry-property-methods.md)          | <span data-ttu-id="51c89-143">"{AB721A53-1E2F-11D0-9819-00AA0040529B}" — это идентификатор GUID изменения пароля в строковой форме.</span><span class="sxs-lookup"><span data-stu-id="51c89-143">"{AB721A53-1E2F-11D0-9819-00AA0040529B}" which is the change password GUID in string form.</span></span>                                                                            |
| [<span data-ttu-id="51c89-144">**инхеритедобжекттипе**</span><span class="sxs-lookup"><span data-stu-id="51c89-144">**InheritedObjectType**</span></span>](iadsaccesscontrolentry-property-methods.md) | <span data-ttu-id="51c89-145">Не используется</span><span class="sxs-lookup"><span data-stu-id="51c89-145">Not used</span></span>                                                                                                                                                              |
| [<span data-ttu-id="51c89-146">**Доверенное лицо**</span><span class="sxs-lookup"><span data-stu-id="51c89-146">**Trustee**</span></span>](iadsaccesscontrolentry-property-methods.md)             | <span data-ttu-id="51c89-147">Имя учетной записи для SID "S-1-1-0" (все).</span><span class="sxs-lookup"><span data-stu-id="51c89-147">Account name for SID "S-1-1-0" (Everyone).</span></span>                                                                                                                            |



 

## <a name="example-code"></a><span data-ttu-id="51c89-148">Пример кода</span><span class="sxs-lookup"><span data-stu-id="51c89-148">Example Code</span></span>

<span data-ttu-id="51c89-149">В следующем примере кода показано, как получить интерфейс для изменения списка DACL.</span><span class="sxs-lookup"><span data-stu-id="51c89-149">The following code example shows how to obtain an interface to change a DACL.</span></span> <span data-ttu-id="51c89-150">Интерфейс [**иадсобжектоптионс**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) можно использовать, задав параметр **\_ \_ \_ DACL для сведений о безопасности в ADS** .</span><span class="sxs-lookup"><span data-stu-id="51c89-150">The [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) interface can be used by setting the **ADS\_SECURITY\_INFO\_DACL** option.</span></span>

> [!Note]  
> <span data-ttu-id="51c89-151">Чтобы использовать код, описанный в этом примере, необходимо быть администратором.</span><span class="sxs-lookup"><span data-stu-id="51c89-151">To use the code documented in this example, you will need to be an Administrator.</span></span> <span data-ttu-id="51c89-152">Если вы не являетесь администратором, вам потребуется добавить дополнительный код, который будет использовать интерфейс, позволяющий пользователю изменить способ сброса кэша на стороне клиента в службу домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="51c89-152">If you are not an Administrator, then you will need to add more code that will use an interface that will allow a user to change the way the client-side cache is flushed back to the Active Directory Domain Service.</span></span>

 


```C++
//
// Obtain an IADsObjectOptions interface from the object whose
// DACL you wish to modify.
//
long CanReadSetDACL = ADS_SECURITY_INFO_DACL;

CComPtr<IADsObjectOptions> spObjOps;

hr = pads->QueryInterface(IID_IADsObjectOptions, (void**)&spObjOps);

if(SUCCEEDED(hr))

{

//
// Set the option mask you want to change. In this case
// we want to change the objects security information, so we'll
// use the ADS_OPTION_SECURITY_MASK. Since we want to modify the 
// DACL, we'll set the variant to ADS_SEDCURITY_INFO_DACL flag. 
//

    CComVariant svar;
    svar = CanReadSetDACL;
    hr = spObjOps->SetOption(ADS_OPTION_SECURITY_MASK, svar); 

}
//
// The smart pointer declared for pObjOptions can be released
// or it will be destroyed and released once the pointer goes 
// out of scope.
//

```



<span data-ttu-id="51c89-153">В следующем примере кода показано, как изменить пользователь не может изменить пароль с помощью поставщика LDAP.</span><span class="sxs-lookup"><span data-stu-id="51c89-153">The following code example shows how to modify the User Cannot Change Password Permission using the LDAP provider.</span></span> <span data-ttu-id="51c89-154">В этом примере кода используется функция служебной программы **жетобжектаце** , определенная выше.</span><span class="sxs-lookup"><span data-stu-id="51c89-154">This code example uses the **GetObjectACE** utility function defined above.</span></span>

<span data-ttu-id="51c89-155">В этом примере используются примеры функций **жетсидаккаунтнаме \_ Everyone** и **жетсидаккаунтнаме \_ Self** C++, показанные в статье [Чтение пользователя не может изменить пароль (поставщик LDAP)](reading-user-cannot-change-password-ldap-provider.md).</span><span class="sxs-lookup"><span data-stu-id="51c89-155">This example uses the **GetSidAccountName\_Everyone** and **GetSidAccountName\_Self** C++ example functions shown in [Reading User Cannot Change Password (LDAP Provider)](reading-user-cannot-change-password-ldap-provider.md).</span></span>


```C++
#include <aclapi.h>

#define CHANGE_PASSWORD_GUID_W L"{AB721A53-1E2F-11D0-9819-00AA0040529B}"

/***************************************************************************

    CreateACE()

    Creates an ACE and returns the IDispatch pointer for the ACE. This 
    pointer can be passed directly to IADsAccessControlList::AddAce.

    bstrTrustee - Contains the Trustee for the ACE.

    bstrObjectType - Contains the ObjectType for the ACE.

    lAccessMask - Contains the AccessMask for the ACE.

    lACEType - Contains the ACEType for the ACE.

    lACEFlags - Contains the ACEFlags for the ACE.

    lFlags - Contains the Flags for the ACE.

***************************************************************************/

IDispatch* CreateACE(BSTR bstrTrustee, 
                     BSTR bstrObjectType, 
                     long lAccessMask, 
                     long lACEType, 
                     long lACEFlags, 
                     long lFlags)
{
    HRESULT hr;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE = NULL;

    hr = CoCreateInstance(CLSID_AccessControlEntry,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsAccessControlEntry,
                          (void**)&pACE);
    if(SUCCEEDED(hr)) 
    {
        hr = pACE->put_Trustee(bstrTrustee); 
        hr = pACE->put_ObjectType(bstrObjectType);
        hr = pACE->put_AccessMask(lAccessMask); 
        hr = pACE->put_AceType(lACEType);
        hr = pACE->put_AceFlags(lACEFlags);
        hr = pACE->put_Flags(lFlags);

        hr = pACE->QueryInterface(IID_IDispatch, (LPVOID*)&pDisp);

        pACE->Release();
    }

    return pDisp;
}

/***************************************************************************

    ReorderACEs()

    Causes the ACEs of an object DACL to be reordered properly. The ACEs are 
    automatically put in the proper order when they are added to the DACL. 
    On older systems however, this does not occur automatically, so this 
    function is necessary so the deny ACEs are ordered in the list before 
    the allow ACEs.

    pwszDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the DS object to reorder the DACL for.

***************************************************************************/

HRESULT ReorderACEs(LPCWSTR pwszDN)
{
    HRESULT hr = E_FAIL;
    DWORD dwResult;
    ACL *pdacl;
    PSECURITY_DESCRIPTOR psd;
    
    dwResult = GetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                        SE_DS_OBJECT_ALL,
                                        DACL_SECURITY_INFORMATION,
                                        NULL,
                                        NULL,
                                        &pdacl,
                                        NULL,
                                        &psd);

    if(ERROR_SUCCESS == dwResult)
    {
        dwResult = SetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                            SE_DS_OBJECT_ALL,
                                            DACL_SECURITY_INFORMATION,
                                            NULL,
                                            NULL,
                                            pdacl,
                                            NULL);

        LocalFree(psd);
        
        if(ERROR_SUCCESS == dwResult)
        {
            hr = S_OK;
        }
    }
    
    return hr;
}

/***************************************************************************

    SetUserCannotChangePassword()

    Sets the "User Cannot Change Password" permission using the LDAP provider 
    to the specified setting. To do this, find the existing 
    ACEs and modify the AceType. If the ACE is not found, a new one of the 
    proper type is created and added. The ACEs should always be present, but 
    it is possible that the default DACL excludes them, so this situation 
    will be handled correctly.

    pwszUserDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the user object to modify.

    pwszUsername - A null-terminated Unicode string that contains the user 
    name to use for authorization. If this is NULL, the credentials of the 
    current user are used.

    pwszPassword - A null-terminated Unicode string that contains the 
    password to use for authorization. This is ignored if pwszUsername is 
    NULL.

    fCannotChangePassword - Contains the new setting for the privilege. 
    Contains nonzero if the user cannot change their password or zero if 
    the can change their password.

***************************************************************************/

HRESULT SetUserCannotChangePassword(LPCWSTR pwszUserDN, 
                                    LPCWSTR pwszUsername, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    HRESULT hr;

    CComBSTR sbstrEveryone;
    hr = GetSidAccountName_Everyone(&sbstrEveryone);
    if(FAILED(hr))
    {
        return hr;
    }

    CComBSTR sbstrSelf;
    hr = GetSidAccountName_Self(&sbstrSelf);
    if(FAILED(hr))
    {
        return hr;
    }

    if(NULL == pwszUserDN)
    {
        return E_INVALIDARG;
    }
    
    IADs *pads;

    hr = ADsOpenObject( pwszUserDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&pads);

    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrSecDesc = "ntSecurityDescriptor";
        CComVariant svar;
        
        hr = pads->Get(sbstrSecDesc, &svar);
        if(SUCCEEDED(hr))
        {
            IADsSecurityDescriptor *psd;

            hr = svar.pdispVal->QueryInterface(IID_IADsSecurityDescriptor, (LPVOID*)&psd);
            if(SUCCEEDED(hr))
            {
                IDispatch *pDisp;

                hr = psd->get_DiscretionaryAcl(&pDisp);
                if(SUCCEEDED(hr))
                {
                    IADsAccessControlList *pACL;

                    hr = pDisp->QueryInterface(IID_IADsAccessControlList, (void**)&pACL);
                    if(SUCCEEDED(hr)) 
                    {
                        BOOL fMustReorder = FALSE;
                        /*
                        Get the existing ACE for the change password permission 
                        for Everyone. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACEEveryone = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrEveryone, &pACEEveryone);
                        if(pACEEveryone)
                        {
                            hr = pACEEveryone->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);

                            pACEEveryone->Release();
                        }
                        else
                        {
                            IDispatch *pDispEveryone = NULL;
                            
                            pDispEveryone = CreateACE(sbstrEveryone, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);
                            
                            if(pDispEveryone)
                            {
                                //add the new ACE for everyone
                                hr = pACL->AddAce(pDispEveryone);

                                pDispEveryone->Release();

                                fMustReorder = TRUE;
                            }                            
                        }
                        
                        /*
                        Get the existing ACE for the change password permission 
                        for Self. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACESelf = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrSelf, &pACESelf);
                        if(pACESelf)
                        {
                            hr = pACESelf->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);
                        
                            pACESelf->Release();
                        }
                        else
                        {
                            IDispatch *pDispSelf = NULL;
                            
                            pDispSelf = CreateACE(sbstrSelf, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);

                            if(pDispSelf)
                            {
                                //add the new ACE for self
                                hr = pACL->AddAce(pDispSelf);

                                pDispSelf->Release();

                                fMustReorder = TRUE;
                            }                            
                        }

                        //update the security descriptor property
                        hr = pads->Put(sbstrSecDesc, svar);
                        
                        //commit the changes
                        hr = pads->SetInfo();

                        if(fMustReorder)
                        {
                            ReorderACEs(pwszUserDN);
                        }

                        pACL->Release();
                    }

                    pDisp->Release();
                }
                
                psd->Release();
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="51c89-156">В следующем примере кода показано, как изменить пользователь не может изменить пароль с помощью поставщика LDAP.</span><span class="sxs-lookup"><span data-stu-id="51c89-156">The following code example shows how to modify the User Cannot Change Password Permission using the LDAP provider.</span></span>

> [!Note]  
> <span data-ttu-id="51c89-157">Приведенный ниже пример будет работать только с доменами, на которых первичным языком является английский, так как строки "все" и "самоцентр NT \\ " локализуются на основе языка первого контроллера домена в домене.</span><span class="sxs-lookup"><span data-stu-id="51c89-157">The example below will only work on domains where the primary language is English because the "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="51c89-158">Не существует способа Visual Basic получить имена учетных записей для хорошо известного субъекта безопасности, не вызывая функцию [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) .</span><span class="sxs-lookup"><span data-stu-id="51c89-158">There is no way in Visual Basic to obtain the account names for a well-known security principal without calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function.</span></span> <span data-ttu-id="51c89-159">При использовании Visual Basic рекомендуется использовать поставщика WinNT для изменения пользователя, не изменяющего разрешения на смену пароля, как показано в подокне [изменение пользователя не может изменить пароль (поставщик WinNT)](modifying-user-cannot-change-password-winnt-provider.md).</span><span class="sxs-lookup"><span data-stu-id="51c89-159">If using Visual Basic, it is suggested that you use the WinNT provider to modify the User Cannot Change Password Permission as shown in [Modifying User Cannot Change Password (WinNT Provider)](modifying-user-cannot-change-password-winnt-provider.md).</span></span>

 


```VB
'******************************************************************************
'
'    SetUserCannotChangePassword
'
'    Sets the "User Cannot Change Password" permission using the LDAP provider
'    to the specified setting. This is accomplished by finding the existing
'    ACEs and modifying the AceType. The ACEs should always be present, but
'    it is possible that the default DACL excludes them. This function will not
'    work correctly if both ACEs are not present.
'
'    strUserDN - A string that contains the LDAP ADsPath of the user object to
'    modify.
'
'    strUsername - A string that contains the user name to use for
'    authorization. If this is an empty string, the credentials of the current
'    user are used.
'
'    strPassword - A string that contains the password to use for authorization.
'    This is ignored if strUsername is empty.
'
'    fCannotChangePassword - Contains the new setting for the privilege.
'    Contains True if the user cannot change their password or False if
'    the can change their password.
'
'******************************************************************************
Sub SetUserCannotChangePassword(strUserDN As String, strUsername As String, strPassword As String, fUserCannotChangePassword As Boolean)
    Dim oUser As IADs
    Dim oSecDesc As IADsSecurityDescriptor
    Dim oACL As IADsAccessControlList
    Dim oACE As IADsAccessControlEntry
    
    fEveryone = False
    fSelf = False
    
    If "" <> strUsername Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("LDAP:")
        Set oUser = dso.OpenDSObject(strUserDN, strUsername, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strUserDN)
    End If
    
    Set oSecDesc = oUser.Get("ntSecurityDescriptor")
    Set oACL = oSecDesc.DiscretionaryAcl
    
    ' Modify the existing entries.
    For Each oACE In oACL
        If UCase(oACE.ObjectType) = UCase(CHANGE_PASSWORD_GUID) Then
            If oACE.Trustee = "Everyone" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        
            If oACE.Trustee = "NT AUTHORITY\SELF" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        End If
    Next
    
    ' Update the ntSecurityDescriptor property.
    oUser.Put "ntSecurityDescriptor", oSecDesc
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



 

 