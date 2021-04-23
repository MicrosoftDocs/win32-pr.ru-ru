---
title: Методы свойств Иадсграуп (iAds. h)
description: Методы свойств интерфейса Иадсграуп.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсграуп ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654617"
---
# <a name="iadsgroup-property-methods"></a><span data-ttu-id="90dba-104">Методы свойств Иадсграуп</span><span class="sxs-lookup"><span data-stu-id="90dba-104">IADsGroup Property Methods</span></span>

<span data-ttu-id="90dba-105">Методы свойств интерфейса [**иадсграуп**](/windows/desktop/api/Iads/nn-iads-iadsgroup) считывают и записывают следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="90dba-105">The property methods of the [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) interface read and write the following properties.</span></span> <span data-ttu-id="90dba-106">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="90dba-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="90dba-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="90dba-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="90dba-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="90dba-108">**Description**</span></span>
<span data-ttu-id="90dba-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="90dba-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="90dba-110">Указывает текстовое описание членства в группе.</span><span class="sxs-lookup"><span data-stu-id="90dba-110">Indicates the textual description of the group membership.</span></span>

<dt>

<span data-ttu-id="90dba-111">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="90dba-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="90dba-112">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="90dba-112">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="90dba-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90dba-113">Remarks</span></span>

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a><span data-ttu-id="90dba-114">Использование Иадсграуп для получения описания встроенных групп</span><span class="sxs-lookup"><span data-stu-id="90dba-114">Using IADsGroup to Retrieve Descriptions of Built-in Groups</span></span>

<span data-ttu-id="90dba-115">В следующих примерах показано, как получить сведения об объектах группы Windows по имени.</span><span class="sxs-lookup"><span data-stu-id="90dba-115">The following examples show how to retrieve information about Windows group objects by name.</span></span> <span data-ttu-id="90dba-116">В многоязычной среде встроенные группы иногда называются разными локализованными именами. Это означает, что они не могут быть получены напрямую с помощью строковых идентификаторов, таких как "WinNT://Microsoft/Administrators".</span><span class="sxs-lookup"><span data-stu-id="90dba-116">In a multilingual environment, built-in groups are sometimes known by different localized names, which means that they cannot be retrieved directly by using string identifiers such as "WinNT://Microsoft/Administrators".</span></span> <span data-ttu-id="90dba-117">В этом случае пользователь может выполнить привязку к хорошо известному объекту идентификатора безопасности для группы, получить локализованное имя группы и предоставить его методу GetObject.</span><span class="sxs-lookup"><span data-stu-id="90dba-117">In that case, the user can bind to the well-known SID object for the group, retrieve the localized group name, and supply that to the GetObject method.</span></span> <span data-ttu-id="90dba-118">Дополнительные сведения см. в разделе [хорошо известные идентификаторы безопасности](/windows/desktop/SecAuthZ/well-known-sids).</span><span class="sxs-lookup"><span data-stu-id="90dba-118">For more information, see [Well-known SIDs](/windows/desktop/SecAuthZ/well-known-sids).</span></span>

## <a name="examples"></a><span data-ttu-id="90dba-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="90dba-119">Examples</span></span>

<span data-ttu-id="90dba-120">В следующем Visual Basic примере показано, как выполнить привязку к объекту группы и отобразить описание группы.</span><span class="sxs-lookup"><span data-stu-id="90dba-120">The following Visual Basic example shows how to bind to a group object and display the description of the group.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="90dba-121">В следующем примере C++ показано, как выполнить привязку к объекту группы и отобразить описание группы.</span><span class="sxs-lookup"><span data-stu-id="90dba-121">The following C++ example shows how to bind to a group object and display the description of the group.</span></span>


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a><span data-ttu-id="90dba-122">Требования</span><span class="sxs-lookup"><span data-stu-id="90dba-122">Requirements</span></span>



| <span data-ttu-id="90dba-123">Требование</span><span class="sxs-lookup"><span data-stu-id="90dba-123">Requirement</span></span> | <span data-ttu-id="90dba-124">Значение</span><span class="sxs-lookup"><span data-stu-id="90dba-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90dba-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90dba-125">Minimum supported client</span></span><br/> | <span data-ttu-id="90dba-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90dba-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90dba-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90dba-127">Minimum supported server</span></span><br/> | <span data-ttu-id="90dba-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90dba-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90dba-129">Header</span><span class="sxs-lookup"><span data-stu-id="90dba-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="90dba-130"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="90dba-130"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="90dba-131">DLL</span><span class="sxs-lookup"><span data-stu-id="90dba-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90dba-132"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90dba-132"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="90dba-133">IID</span><span class="sxs-lookup"><span data-stu-id="90dba-133">IID</span></span><br/>                      | <span data-ttu-id="90dba-134">IID \_ иадсграуп определен как 27636B00-410F-11CF-B1FF-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="90dba-134">IID\_IADsGroup is defined as 27636B00-410F-11CF-B1FF-02608C9E7553</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="90dba-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90dba-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90dba-136">**IADs**</span><span class="sxs-lookup"><span data-stu-id="90dba-136">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="90dba-137">**иадсграуп**</span><span class="sxs-lookup"><span data-stu-id="90dba-137">**IADsGroup**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[<span data-ttu-id="90dba-138">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="90dba-138">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

