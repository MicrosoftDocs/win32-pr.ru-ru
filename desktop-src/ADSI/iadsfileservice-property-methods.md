---
title: Методы свойств Иадсфилесервице (iAds. h)
description: Методы свойств интерфейса Иадсфилесервице получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 1455df61-9218-450b-b956-1cf127364f24
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсфилесервице ADSI
topic_type:
- apiref
api_name:
- IADsFileService Property Methods
- IADsFileService.Description
- IADsFileService.get_Description
- IADsFileService.put_Description
- IADsFileService.MaxUserCount
- IADsFileService.get_MaxUserCount
- IADsFileService.put_MaxUserCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a46b37522bbdce6e99b969811e2909c8ecc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534847"
---
# <a name="iadsfileservice-property-methods"></a><span data-ttu-id="407e0-105">Методы свойств Иадсфилесервице</span><span class="sxs-lookup"><span data-stu-id="407e0-105">IADsFileService Property Methods</span></span>

<span data-ttu-id="407e0-106">Методы свойств интерфейса [**иадсфилесервице**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="407e0-106">The property methods of the [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="407e0-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="407e0-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="407e0-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="407e0-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="407e0-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="407e0-109">**Description**</span></span>
<span data-ttu-id="407e0-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="407e0-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="407e0-111">Описание службы файлов.</span><span class="sxs-lookup"><span data-stu-id="407e0-111">The description of the file service.</span></span>

<dt>

<span data-ttu-id="407e0-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="407e0-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="407e0-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="407e0-113">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> <dt>

<span data-ttu-id="407e0-114">**максусеркаунт**</span><span class="sxs-lookup"><span data-stu-id="407e0-114">**MaxUserCount**</span></span>
<span data-ttu-id="407e0-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="407e0-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="407e0-116">Максимальное число пользователей, разрешенных в службе в любое время.</span><span class="sxs-lookup"><span data-stu-id="407e0-116">The maximum number of users allowed on the service at any time.</span></span>

<dt>

<span data-ttu-id="407e0-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="407e0-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="407e0-118">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="407e0-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
HRESULT put_MaxUserCount(
  [in] LONG lMaxUserCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="407e0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="407e0-119">Remarks</span></span>

<span data-ttu-id="407e0-120">Для доступа к общим папкам, сеансам и ресурсам на компьютере необходимо пройти через службу файлов.</span><span class="sxs-lookup"><span data-stu-id="407e0-120">You must go through the file service to access file shares, sessions, and resources on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="407e0-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="407e0-121">Examples</span></span>

<span data-ttu-id="407e0-122">В следующем примере кода записывается описание и проверяется предельное число пользователей в службе файлов.</span><span class="sxs-lookup"><span data-stu-id="407e0-122">The following code example writes a description for and check the user limit of the file service.</span></span>


```VB
Dim fs As IADsFileService
On Error GoTo Cleanup

' Bind to a file service object on "myComputer" in the local domain.
Set fs = GetObject("WinNT://myComputer/LanmanServer")

fs.Description = "WinNT file service."
n = fs.MaxUserCount
If n = -1 Then
   MsgBox "No limit has been imposed on number of users allowed."
Else
   MsgBox n & " users are allowed."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
```



<span data-ttu-id="407e0-123">В следующем примере кода записывается описание и проверяется предельное число пользователей для объекта службы файлов.</span><span class="sxs-lookup"><span data-stu-id="407e0-123">The following code example writes a description for and check the user limit on a file service object.</span></span>


```C++
HRESULT CheckFileService()
{
    IADsFileService *pFs = NULL;
    LPWSTR adsPath = L"WinNT://myComputer/LanmanServer";
    HRESULT hr = S_OK;
    long count = 0;

    hr = ADsGetObject(adsPath, IID_IADsFileService, (void**)&pFs)
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->put_Description(CComBSTR("WinNT File Service"));
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->SetInfo();
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->get_MaxUserCount(&count);
    if(FAILED(hr)) {goto Cleanup;}

    if(count == -1) {
        printf("No limit has been imposed on the number of users.\n");
    } 
    else {
        printf("Number of allowed users are %d\n",count);
    }

Cleanup:
    if(pFs) pFs->Release();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="407e0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="407e0-124">Requirements</span></span>



| <span data-ttu-id="407e0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="407e0-125">Requirement</span></span> | <span data-ttu-id="407e0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="407e0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="407e0-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="407e0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="407e0-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="407e0-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="407e0-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="407e0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="407e0-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="407e0-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="407e0-131">Header</span><span class="sxs-lookup"><span data-stu-id="407e0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="407e0-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="407e0-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="407e0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="407e0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="407e0-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="407e0-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="407e0-135">IID</span><span class="sxs-lookup"><span data-stu-id="407e0-135">IID</span></span><br/>                      | <span data-ttu-id="407e0-136">IID \_ иадсфилесервице определен как A89D1900-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="407e0-136">IID\_IADsFileService is defined as A89D1900-31CA-11CF-A98A-00AA006BC149</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="407e0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="407e0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="407e0-138">**иадссервице**</span><span class="sxs-lookup"><span data-stu-id="407e0-138">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="407e0-139">**иадсфилесервице**</span><span class="sxs-lookup"><span data-stu-id="407e0-139">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="407e0-140">**иадсфилесервицеоператионс**</span><span class="sxs-lookup"><span data-stu-id="407e0-140">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="407e0-141">**иадссервицеоператионс**</span><span class="sxs-lookup"><span data-stu-id="407e0-141">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> <dt>

[<span data-ttu-id="407e0-142">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="407e0-142">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





