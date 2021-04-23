---
title: Методы свойств Иадсресаурце (iAds. h)
description: Методы свойств интерфейса Иадсресаурце получают или задают свойства, описанные в следующей таблице. Общее описание методов свойств см. в разделе методы свойств интерфейса.
ms.assetid: a2d6ed76-88e9-468f-928a-a038b73fb362
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсресаурце ADSI
topic_type:
- apiref
api_name:
- IADsResource Property Methods
- IADsResource.LockCount
- IADsResource.get_LockCount
- IADsResource.Path
- IADsResource.get_Path
- IADsResource.User
- IADsResource.get_User
- IADsResource.UserPath
- IADsResource.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f2ab2642dd8d03062a26d096190cf7615977a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654484"
---
# <a name="iadsresource-property-methods"></a><span data-ttu-id="baa64-105">Методы свойств Иадсресаурце</span><span class="sxs-lookup"><span data-stu-id="baa64-105">IADsResource Property Methods</span></span>

<span data-ttu-id="baa64-106">Методы свойств интерфейса [**иадсресаурце**](/windows/desktop/api/Iads/nn-iads-iadsresource) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="baa64-106">The property methods of the [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="baa64-107">Общее описание методов свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="baa64-107">For a general discussion of property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="baa64-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="baa64-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="baa64-109">**локккаунт**</span><span class="sxs-lookup"><span data-stu-id="baa64-109">**LockCount**</span></span>
<span data-ttu-id="baa64-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="baa64-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="baa64-111">Количество блокировок ресурса.</span><span class="sxs-lookup"><span data-stu-id="baa64-111">Number of locks on the resource.</span></span>

<dt>

<span data-ttu-id="baa64-112">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="baa64-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baa64-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="baa64-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockCount(
  [out] LONG* plLockCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="baa64-114">**Путь**</span><span class="sxs-lookup"><span data-stu-id="baa64-114">**Path**</span></span>
<span data-ttu-id="baa64-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="baa64-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="baa64-116">Путь файловой системы к открытому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="baa64-116">The file system path of the opened resource.</span></span>

<dt>

<span data-ttu-id="baa64-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="baa64-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baa64-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="baa64-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="baa64-119">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="baa64-119">**User**</span></span>
<span data-ttu-id="baa64-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="baa64-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="baa64-121">Имя пользователя, открывшего ресурс.</span><span class="sxs-lookup"><span data-stu-id="baa64-121">The name of the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="baa64-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="baa64-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baa64-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="baa64-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="baa64-124">**усерпас**</span><span class="sxs-lookup"><span data-stu-id="baa64-124">**UserPath**</span></span>
<span data-ttu-id="baa64-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="baa64-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="baa64-126">Путь к объекту пользователя для пользователя, открывшего ресурс.</span><span class="sxs-lookup"><span data-stu-id="baa64-126">The ADsPath of the user object for the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="baa64-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="baa64-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baa64-128">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="baa64-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="baa64-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="baa64-129">Examples</span></span>

<span data-ttu-id="baa64-130">В следующем примере кода показано, как проверить открытые ресурсы файловой службы.</span><span class="sxs-lookup"><span data-stu-id="baa64-130">The following code example shows how to examine open resources of a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate resources.
If (IsEmpty(fso) = False) Then
    For Each resource In fso.resources
        MsgBox "Resource name: " & resource.name
        MsgBox "Resource path: " & resource.path
    Next resource
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="baa64-131">В следующем примере кода перечисляются наборы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="baa64-131">The following code example enumerates a collection of resources.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsResource *pRes = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
IEnumVARIANT *pEnum = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
HRESULT hr = S_OK;

LPWSTR adsPath =L"WinNT://aMachine/LanmanServer";
hr = ADsGetObject(adsPath, IID_IADsFileServiceOperations,(void**)&pFso);
if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Resources(&pColl);
if(FAILED(hr)) {goto Cleanup;}


// Enumerate print jobs. Code omitted.
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
VariantInit(&var);
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsResource, (void**)&pRes);
        pRes->get_Name(&bstr);
        printf("Resource name: %S\n",bstr);
        SysFreeString(bstr);
        pRes->get_Path(&bstr);
        printf("Resource path: %S\n",bstr);
        SysFreeString(bstr);
        pRes->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pRes) pRes->Release();
    if(pDisp) pDisp->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pFso) pFso->Release();
```



## <a name="requirements"></a><span data-ttu-id="baa64-132">Требования</span><span class="sxs-lookup"><span data-stu-id="baa64-132">Requirements</span></span>



| <span data-ttu-id="baa64-133">Требование</span><span class="sxs-lookup"><span data-stu-id="baa64-133">Requirement</span></span> | <span data-ttu-id="baa64-134">Значение</span><span class="sxs-lookup"><span data-stu-id="baa64-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="baa64-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="baa64-135">Minimum supported client</span></span><br/> | <span data-ttu-id="baa64-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="baa64-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="baa64-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="baa64-137">Minimum supported server</span></span><br/> | <span data-ttu-id="baa64-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="baa64-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="baa64-139">Header</span><span class="sxs-lookup"><span data-stu-id="baa64-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="baa64-140"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="baa64-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="baa64-141">DLL</span><span class="sxs-lookup"><span data-stu-id="baa64-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baa64-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baa64-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="baa64-143">IID</span><span class="sxs-lookup"><span data-stu-id="baa64-143">IID</span></span><br/>                      | <span data-ttu-id="baa64-144">IID \_ иадсресаурце определен как 34A05B20-4AAB-11CF-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="baa64-144">IID\_IADsResource is defined as 34A05B20-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="baa64-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="baa64-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa64-146">**иадсресаурце**</span><span class="sxs-lookup"><span data-stu-id="baa64-146">**IADsResource**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsresource)
</dt> <dt>

[<span data-ttu-id="baa64-147">**Иадсфилесервицеоператионс:: ресурсы**</span><span class="sxs-lookup"><span data-stu-id="baa64-147">**IADsFileServiceOperations::Resources**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-resources)
</dt> </dl>

 

 





