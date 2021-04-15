---
title: Методы свойств Иадсакцессконтроллист (iAds. h)
description: Методы свойств интерфейса Иадсакцессконтроллист получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: cb68bb61-4216-4f69-bea1-ab7f98937a27
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсакцессконтроллист ADSI
topic_type:
- apiref
api_name:
- IADsAccessControlList Property Methods
- IADsAccessControlList.AclRevision
- IADsAccessControlList.get_AclRevision
- IADsAccessControlList.put_AclRevision
- IADsAccessControlList.AceCount
- IADsAccessControlList.get_AceCount
- IADsAccessControlList.put_AceCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55763b7c52071ca5bfd0a875912941090b7992c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415009"
---
# <a name="iadsaccesscontrollist-property-methods"></a><span data-ttu-id="628f4-105">Методы свойств Иадсакцессконтроллист</span><span class="sxs-lookup"><span data-stu-id="628f4-105">IADsAccessControlList Property Methods</span></span>

<span data-ttu-id="628f4-106">Методы свойств интерфейса [**иадсакцессконтроллист**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="628f4-106">The property methods of the [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="628f4-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="628f4-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="628f4-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="628f4-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="628f4-109">**ацекаунт**</span><span class="sxs-lookup"><span data-stu-id="628f4-109">**AceCount**</span></span>
<span data-ttu-id="628f4-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="628f4-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="628f4-111">Число записей управления доступом в списке управления доступом.</span><span class="sxs-lookup"><span data-stu-id="628f4-111">The number of access control entries in the access-control list.</span></span>

<dt>

<span data-ttu-id="628f4-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="628f4-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="628f4-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="628f4-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceCount(
  [out] LONG* lnAceCount
);
HRESULT put_AceCount(
  [in] LONG lnAceCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="628f4-114">**аклревисион**</span><span class="sxs-lookup"><span data-stu-id="628f4-114">**AclRevision**</span></span>
<span data-ttu-id="628f4-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="628f4-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="628f4-116">Уровень редакции списка управления доступом.</span><span class="sxs-lookup"><span data-stu-id="628f4-116">The revision level of an access-control list.</span></span> <span data-ttu-id="628f4-117">Это значение может быть **\_ версией ACL** или **\_ версией списка \_ ACL**.</span><span class="sxs-lookup"><span data-stu-id="628f4-117">This value can be **ACL\_REVISION** or **ACL\_REVISION\_DS**.</span></span> <span data-ttu-id="628f4-118">Используйте **ACL \_ версии \_ DS** , если список ACL содержит запись ACE для конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="628f4-118">Use **ACL\_REVISION\_DS** if the ACL contains an object-specific ACE.</span></span> <span data-ttu-id="628f4-119">Все ACE в списке ACL должны иметь одинаковый уровень редакции.</span><span class="sxs-lookup"><span data-stu-id="628f4-119">All ACEs in an ACL must be at the same revision level.</span></span>

<dt>

<span data-ttu-id="628f4-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="628f4-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="628f4-121">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="628f4-121">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AclRevision(
  [out] LONG* lnAclRevision
);
HRESULT put_AclRevision(
  [in] LONG lnAclRevision
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="628f4-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="628f4-122">Examples</span></span>

<span data-ttu-id="628f4-123">В следующем примере кода показано количество записей ACE в списке ACL.</span><span class="sxs-lookup"><span data-stu-id="628f4-123">The following code example displays the number of ACEs in an ACL.</span></span>


```VB
Dim x as IADs
Dim sd As IADsSecurityDescriptor
Dim Dacl As IADsAccessControlList

On Error GoTo Cleanup

Set x = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
Debug.Print Dacl.AceCount

Cleanup:
    If (Err.Number <> 0) Then
        MsgBox ("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
```



<span data-ttu-id="628f4-124">В следующем примере кода показано количество записей ACE в списке ACL.</span><span class="sxs-lookup"><span data-stu-id="628f4-124">The following code example displays the number of ACEs in an ACL.</span></span>


```C++
HRESULT ShowACEInACL(LPWSTR guestPath,LPWSTR user,LPWSTR passwd)
{
  IADs *pObj = NULL;
  IADsSecurityDescriptor *psd = NULL;
  HRESULT hr = S_OK;
  VARIANT var;

  VariantInit(&var);

  hr = ADsOpenObject(guestPath,user,passwd,ADS_SECURE_AUTHENTICATION,
                     IID_IADs,(void**)&pObj);
  if(FAILED(hr)) {
      printf("hr = %x\n",hr);
      return hr;
  }
  else {
      BSTR bstr = NULL;
      pObj->get_Class(&bstr);
      printf("Object class: %S\n",bstr);
      SysFreeString(bstr);
  }

  hr = pObj->Get(CComBSTR("ntSecurityDescriptor"), &var);
  pObj->Release();

  if(FAILED(hr)) {
      printf("Get ntSD: hr = %x\n",hr);
      return hr;
  }

  hr = V_DISPATCH(&var)->QueryInterface(IID_IADsSecurityDescriptor,
                                        (void**)&psd);

  if(FAILED(hr)) {
      printf("DISP: hr = %x\n",hr);
      VariantClear(&var);
      return hr;
  }

  IDispatch *pDisp = NULL;
  hr = psd->get_DiscretionaryAcl(&pDisp);
  VariantClear(&var);

  if(FAILED(hr)) {
      printf("get_DACL : hr = %x\n",hr);
      return hr;
  }

  IADsAccessControlList *pAcl = NULL;
  hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pAcl);
  pDisp->Release();

  if(FAILED(hr)) {
      printf("QI ACL: hr = %x\n",hr);
      return hr;
  }

  long count = 0;
  hr = pAcl->get_AceCount(&count);
  pAcl->Release();
  if(FAILED(hr)) {
      printf("Count: hr = %x\n",hr);
      return hr;
  }

  printf("AceCount = %d\n",count);

  return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="628f4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="628f4-125">Requirements</span></span>



| <span data-ttu-id="628f4-126">Требование</span><span class="sxs-lookup"><span data-stu-id="628f4-126">Requirement</span></span> | <span data-ttu-id="628f4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="628f4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="628f4-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="628f4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="628f4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="628f4-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="628f4-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="628f4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="628f4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="628f4-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="628f4-132">Header</span><span class="sxs-lookup"><span data-stu-id="628f4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="628f4-133"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="628f4-133"><dt>Iads.h</dt></span></span> </dl>        |
| <span data-ttu-id="628f4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="628f4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="628f4-135"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="628f4-135"><dt>Activeds.dll</dt></span></span> </dl>  |
| <span data-ttu-id="628f4-136">IID</span><span class="sxs-lookup"><span data-stu-id="628f4-136">IID</span></span><br/>                      | <span data-ttu-id="628f4-137">IID \_ иадсакцессконтроллист определен как B7EE91CC-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="628f4-137">IID\_IADsAccessControlList is defined as B7EE91CC-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="628f4-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="628f4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="628f4-139">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="628f4-139">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[<span data-ttu-id="628f4-140">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="628f4-140">**IEnumVARIANT**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)
</dt> <dt>

[<span data-ttu-id="628f4-141">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="628f4-141">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="628f4-142">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="628f4-142">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

