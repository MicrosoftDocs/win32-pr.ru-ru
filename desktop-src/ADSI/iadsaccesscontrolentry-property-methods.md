---
title: Методы свойств Иадсакцессконтролентри (iAds. h)
description: Методы свойств интерфейса Иадсакцессконтролентри получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: dce11723-0e30-4baa-8666-0a32f0968ebb
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсакцессконтролентри ADSI
topic_type:
- apiref
api_name:
- IADsAccessControlEntry Property Methods
- IADsAccessControlEntry.AccessMask
- IADsAccessControlEntry.get_AccessMask
- IADsAccessControlEntry.put_AccessMask
- IADsAccessControlEntry.AceType
- IADsAccessControlEntry.get_AceType
- IADsAccessControlEntry.put_AceType
- IADsAccessControlEntry.AceFlags
- IADsAccessControlEntry.get_AceFlags
- IADsAccessControlEntry.put_AceFlags
- IADsAccessControlEntry.Flags
- IADsAccessControlEntry.get_Flags
- IADsAccessControlEntry.put_Flags
- IADsAccessControlEntry.ObjectType
- IADsAccessControlEntry.get_ObjectType
- IADsAccessControlEntry.put_ObjectType
- IADsAccessControlEntry.InheritedObjectType
- IADsAccessControlEntry.get_InheritedObjectType
- IADsAccessControlEntry.put_InheritedObjectType
- IADsAccessControlEntry.Trustee
- IADsAccessControlEntry.get_Trustee
- IADsAccessControlEntry.put_Trustee
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8539807f21944ab6f4b2c03f04b14a53dffdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801546"
---
# <a name="iadsaccesscontrolentry-property-methods"></a><span data-ttu-id="40e96-105">Методы свойств Иадсакцессконтролентри</span><span class="sxs-lookup"><span data-stu-id="40e96-105">IADsAccessControlEntry Property Methods</span></span>

<span data-ttu-id="40e96-106">Методы свойств интерфейса [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="40e96-106">The property methods of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="40e96-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="40e96-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="40e96-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="40e96-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="40e96-109">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="40e96-109">**AccessMask**</span></span>
<span data-ttu-id="40e96-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="40e96-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="40e96-111">Содержит набор флагов, указывающих права доступа для объекта.</span><span class="sxs-lookup"><span data-stu-id="40e96-111">Contains a set of flags that specifies access privileges for the object.</span></span> <span data-ttu-id="40e96-112">Допустимые значения для Active Directory объектов определены в перечислении [**\_ \_ перечисления прав на рекламу**](/windows/win32/api/iads/ne-iads-ads_rights_enum) .</span><span class="sxs-lookup"><span data-stu-id="40e96-112">Valid values for Active Directory objects are defined in the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration.</span></span>

<span data-ttu-id="40e96-113">Дополнительные сведения и список возможных значений для объектов файловых или файловых ресурсов см. в разделе [безопасность и права доступа к](/windows/desktop/FileIO/file-security-and-access-rights)файлам.</span><span class="sxs-lookup"><span data-stu-id="40e96-113">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="40e96-114">Дополнительные сведения и список возможных значений для объектов реестра см. в разделе раздел [реестра Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="40e96-114">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

<dt>

<span data-ttu-id="40e96-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40e96-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40e96-116">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="40e96-116">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AccessMask(
  [out] LONG* plnAccessMask
);
HRESULT put_AccessMask(
  [in] LONG lnAccessMask
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="40e96-117">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="40e96-117">**AceFlags**</span></span>
<span data-ttu-id="40e96-118"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="40e96-118"></dt> <dd> <dl></span></span>

<span data-ttu-id="40e96-119">Содержит набор флагов, указывающих, могут ли другие контейнеры или объекты наследовать ACE.</span><span class="sxs-lookup"><span data-stu-id="40e96-119">Contains a set of flags that specifies if other containers or objects can inherit the ACE.</span></span> <span data-ttu-id="40e96-120">Допустимые значения для Active Directory объекта определены в перечислении перечисления [**ADS \_ ацефлаг \_**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) .</span><span class="sxs-lookup"><span data-stu-id="40e96-120">Valid values for Active Directory object are defined in the [**ADS\_ACEFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) enumeration.</span></span>

<span data-ttu-id="40e96-121">Дополнительные сведения и возможные значения для файлов, файловых ресурсов и объектов реестра см. в разделе **AceFlags** элемента структуры [**\_ заголовка ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="40e96-121">For more information and possible values for file, file share, and registry objects, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="40e96-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40e96-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40e96-123">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="40e96-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceFlags(
  [out] LONG* plnAceFlags
);
HRESULT put_AceFlags(
  [in] LONG lnAceFlags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="40e96-124">**AceType**</span><span class="sxs-lookup"><span data-stu-id="40e96-124">**AceType**</span></span>
<span data-ttu-id="40e96-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="40e96-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="40e96-126">Содержит значение, указывающее тип записи ACE.</span><span class="sxs-lookup"><span data-stu-id="40e96-126">Contains a value that indicates the type of ACE.</span></span> <span data-ttu-id="40e96-127">Допустимые значения для Active Directory объектов определены в перечислении перечисления [**ADS \_ ACETYPE \_**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) .</span><span class="sxs-lookup"><span data-stu-id="40e96-127">Valid values for Active Directory objects are defined in the [**ADS\_ACETYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) enumeration.</span></span>

<span data-ttu-id="40e96-128">Дополнительные сведения и возможные значения для файлов, файловых ресурсов и объектов реестра см. в разделе **AceType** элемента структуры [**\_ заголовка ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="40e96-128">For more information and possible values for file, file share, and registry objects, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="40e96-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40e96-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40e96-130">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="40e96-130">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceType(
  [out] LONG* plAceType
);
HRESULT put_AceType(
  [in] LONG lnAceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="40e96-131">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="40e96-131">**Flags**</span></span>
<span data-ttu-id="40e96-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="40e96-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="40e96-133">Флаг, указывающий, имеет ли ACE тип объекта или тип наследуемого объекта.</span><span class="sxs-lookup"><span data-stu-id="40e96-133">A flag that indicates if the ACE has an object type or inherited object type.</span></span> <span data-ttu-id="40e96-134">Допустимые флаги определены в перечислении перечисления [**ADS \_ флагтипе \_**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) .</span><span class="sxs-lookup"><span data-stu-id="40e96-134">Valid flags are defined in the [**ADS\_FLAGTYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="40e96-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40e96-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40e96-136">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="40e96-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Flags(
  [out] LONG* lnflags
);
HRESULT put_Flags(
  [in] LONG lnflags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="40e96-137">**инхеритедобжекттипе**</span><span class="sxs-lookup"><span data-stu-id="40e96-137">**InheritedObjectType**</span></span>
<span data-ttu-id="40e96-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="40e96-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="40e96-139">Флаг, указывающий тип дочернего объекта объекта ADSI.</span><span class="sxs-lookup"><span data-stu-id="40e96-139">A flag that indicates the type of a child object of an ADSI object.</span></span> <span data-ttu-id="40e96-140">Его значение является **идентификатором GUID** объекта в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="40e96-140">Its value is a **GUID** to an object in string format.</span></span> <span data-ttu-id="40e96-141">Если такой **идентификатор GUID** ЗАДАН, ACE применяется только к объекту, на который ссылается **GUID**.</span><span class="sxs-lookup"><span data-stu-id="40e96-141">When such a **GUID** is set, the ACE applies only to the object referred to by the **GUID**.</span></span>

<dt>

<span data-ttu-id="40e96-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40e96-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40e96-143">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="40e96-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_InheritedObjectType(
  [out] BSTR* bstrInheritedObjectType
);
HRESULT put_InheritedObjectType(
  [in] BSTR bstrInheritedObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="40e96-144">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="40e96-144">**ObjectType**</span></span>
<span data-ttu-id="40e96-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="40e96-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="40e96-146">Флаг, указывающий тип объекта ADSI.</span><span class="sxs-lookup"><span data-stu-id="40e96-146">A flag that indicates the ADSI object type.</span></span> <span data-ttu-id="40e96-147">Его значение является **идентификатором GUID** для свойства или объекта в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="40e96-147">Its value is a **GUID** to a property or an object in string format.</span></span> <span data-ttu-id="40e96-148">**Идентификатор GUID** ссылается на свойство, когда используются **объявления \_ right \_ DS Redirectory \_ Read \_ prop** и ADSS права доступа к свойствам- **\_ \_ \_ \_ prop** .</span><span class="sxs-lookup"><span data-stu-id="40e96-148">The **GUID** refers to a property when **ADS\_RIGHT\_DS\_READ\_PROP** and **ADS\_RIGHT\_DS\_WRITE\_PROP** access masks are used.</span></span> <span data-ttu-id="40e96-149">**Идентификатор GUID** определяет объект, когда в **ADS \_ справа \_ DS \_ создаются \_ дочерние** объекты и **AD \_ \_ DS \_ \_ right** .</span><span class="sxs-lookup"><span data-stu-id="40e96-149">The **GUID** specifies an object when **ADS\_RIGHT\_DS\_CREATE\_CHILD** and **ADS\_RIGHT\_DS\_DELETE\_CHILD** access masks are used.</span></span>

<dt>

<span data-ttu-id="40e96-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40e96-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40e96-151">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="40e96-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectType(
  [out] BSTR* bstrObjectType
);
HRESULT put_ObjectType(
  [in] BSTR bstrObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="40e96-152">**Доверенное лицо**</span><span class="sxs-lookup"><span data-stu-id="40e96-152">**Trustee**</span></span>
<span data-ttu-id="40e96-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="40e96-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="40e96-154">Содержит имя учетной записи, к которой применяется ACE.</span><span class="sxs-lookup"><span data-stu-id="40e96-154">Contains the name of the account that the ACE applies to.</span></span>

<dt>

<span data-ttu-id="40e96-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40e96-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40e96-156">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="40e96-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Trustee(
  [out] BSTR* pbstrSecurityId
);
HRESULT put_Trustee(
  [in] BSTR bstrSecurityId
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="40e96-157">Примеры</span><span class="sxs-lookup"><span data-stu-id="40e96-157">Examples</span></span>

<span data-ttu-id="40e96-158">В следующем примере кода показано, как добавлять записи в избирательный список управления доступом с помощью методов свойств [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="40e96-158">The following code example shows how to add entries to a discretionary ACL using the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property methods.</span></span>


```VB
Dim x As IADs
Dim sd As IADsSecurityDescriptor
Dim ace As IADsAccessControlEntry
Dim Dacl As IADsAccessControlList
Dim Ace1 As New AccessControlEntry
Dim Ace2 As New AccessControlEntry

On Error GoTo Cleanup
 
Set x = GetObject("LDAP://OU=Sales, DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
 
' Show the existing ACEs.
For Each ace In Dacl
  Debug.Print ace.Trustee
Next
 
 
' Setup the first ACE.
Ace1.AccessMask = -1 'Full Permission (Allowed)
Ace1.AceType = ADS_ACETYPE_ACCESS_ALLOWED
Ace1.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace1.Trustee = "ACTIVED\Administrator"
 
' Setup the 2nd ACE.
Ace2.AccessMask = -1 'Full Permission (Denied)
Ace2.AceType = ADS_ACETYPE_ACCESS_DENIED
Ace2.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace2.Trustee = "ACTIVED\Andyhar"
 
' Add the ACEs to the Discretionary ACL.
Dacl.AddAce Ace1
Dacl.AddAce Ace2
 
sd.DiscretionaryAcl = Dacl
x.Put "ntSecurityDescriptor", Array(sd)
x.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set x = Nothing
    Set sd = Nothing
    Set ace = Nothing
    Set Dacl = Nothing
    Set Ace1 = Nothing
    Set Ace2 = Nothing
    Set obj = Nothing
    Set cls = Nothing
```



<span data-ttu-id="40e96-159">В следующем примере кода отображаются записи управления доступом.</span><span class="sxs-lookup"><span data-stu-id="40e96-159">The following code example displays access-control entries.</span></span>


```C++
IADs *pADs = NULL;
IDispatch *pDisp = NULL;
IADsSecurityDescriptor *pSD = NULL;
VARIANT var;
HRESULT hr = S_OK;
 
VariantInit(&var);

hr = ADsOpenObject(L"LDAP://OU=Sales, DC=Fabrikam,DC=com",NULL,NULL,
                   ADS_SECURE_AUTHENTICATION, IID_IADs,(void**)&pADs);
if(FAILED(hr)) {goto Cleanup;}

hr = pADs->Get(CComBSTR("ntSecurityDescriptor"),&var);
if(FAILED(hr)) {goto Cleanup;}

pDisp = V_DISPATCH(&var);

hr = pDisp->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
if(FAILED(hr)) {goto Cleanup;}
pDisp->Release();


pSD->get_DiscretionaryAcl(&pDisp);

hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
if(FAILED(hr)) {goto Cleanup;}

hr = DisplayAccessInfo(pSD);
if(FAILED(hr)) {goto Cleanup;}
VariantClear(&var);

Cleanup:
    if(pADs) pADs->Release();
    if(pDisp) pDisp->Release();
    if(pSD) pSD->Release();
    return hr;



HRESULT DisplayAccessInfo(IADsSecurityDescriptor *pSD)
{
    LPWSTR lpszFunction = L"DisplayAccessInfo";
    IDispatch *pDisp = NULL;
    IADsAccessControlList *pACL = NULL;
    IADsAccessControlEntry *pACE = NULL;
    IEnumVARIANT *pEnum = NULL;
    IUnknown *pUnk = NULL;
    HRESULT hr = S_OK;
    ULONG nFetch = 0;
    BSTR bstrValue = NULL;
    VARIANT var;
    LPWSTR lpszOutput = NULL;
    LPWSTR lpszMask = NULL;
    size_t nLength = 0;
    
    VariantInit(&var);
    
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if(FAILED(hr)){goto Cleanup;}
    hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pACL->get__NewEnum(&pUnk);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
    
    if(FAILED(hr)){goto Cleanup;}
    hr = pEnum->Next(1,&var,&nFetch);
    
    while(hr == S_OK)
    {
        if(nFetch==1)
        {
            if(VT_DISPATCH != V_VT(&var))
            {
                goto Cleanup;
            }
            
            pDisp = V_DISPATCH(&var);
            hr = pDisp->QueryInterface(IID_IADsAccessControlEntry,(void**)&pACE);
            
            if(SUCCEEDED(hr))
            {
                lpszMask = L"Trustee: %s";
                hr = pACE->get_Trustee(&bstrValue);
                nLength = wcslen(lpszMask) + wcslen(bstrValue) + 1;
                lpszOutput = new WCHAR[nLength];
                swprintf_s(lpszOutput,lpszMask,bstrValue);
                printf(lpszOutput);
                delete [] lpszOutput;
                SysFreeString(bstrValue);
                
                pACE->Release();
                pACE = NULL;
                pDisp->Release();
                pDisp = NULL;
            }       
            
            VariantClear(&var);
        }       
        hr = pEnum->Next(1,&var,&nFetch);
    }
    
Cleanup:
    if(pDisp) pDisp->Release();
    if(pACL) pACL->Release();
    if(pACE) pACE->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(szValue) SysFreeString(szValue);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="40e96-160">Требования</span><span class="sxs-lookup"><span data-stu-id="40e96-160">Requirements</span></span>



| <span data-ttu-id="40e96-161">Требование</span><span class="sxs-lookup"><span data-stu-id="40e96-161">Requirement</span></span> | <span data-ttu-id="40e96-162">Значение</span><span class="sxs-lookup"><span data-stu-id="40e96-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="40e96-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40e96-163">Minimum supported client</span></span><br/> | <span data-ttu-id="40e96-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40e96-164">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="40e96-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40e96-165">Minimum supported server</span></span><br/> | <span data-ttu-id="40e96-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40e96-166">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="40e96-167">Header</span><span class="sxs-lookup"><span data-stu-id="40e96-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="40e96-168"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="40e96-168"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="40e96-169">DLL</span><span class="sxs-lookup"><span data-stu-id="40e96-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40e96-170"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40e96-170"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="40e96-171">IID</span><span class="sxs-lookup"><span data-stu-id="40e96-171">IID</span></span><br/>                      | <span data-ttu-id="40e96-172">IID \_ иадсакцессконтролентри определен как B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="40e96-172">IID\_IADsAccessControlEntry is defined as B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40e96-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40e96-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40e96-174">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="40e96-174">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="40e96-175">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="40e96-175">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[<span data-ttu-id="40e96-176">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="40e96-176">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

