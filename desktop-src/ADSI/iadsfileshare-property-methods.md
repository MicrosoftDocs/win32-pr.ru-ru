---
title: Методы свойств Иадсфилешаре (iAds. h)
description: Методы свойств интерфейса Иадсфилешаре получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: c5a81c42-507f-4a68-b6f4-83097bd0fa01
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсфилешаре ADSI
topic_type:
- apiref
api_name:
- IADsFileShare Property Methods
- IADsFileShare.CurrentUserCount
- IADsFileShare.get_CurrentUserCount
- IADsFileShare.Description
- IADsFileShare.get_Description
- IADsFileShare.put_Description
- IADsFileShare.HostComputer
- IADsFileShare.get_HostComputer
- IADsFileShare.put_HostComputer
- IADsFileShare.MaxUserCount
- IADsFileShare.get_MaxUserCount
- IADsFileShare.Path
- IADsFileShare.get_Path
- IADsFileShare.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38369a4054f1848d5e35ff8bdb2dda9e9423a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136871"
---
# <a name="iadsfileshare-property-methods"></a><span data-ttu-id="834fb-105">Методы свойств Иадсфилешаре</span><span class="sxs-lookup"><span data-stu-id="834fb-105">IADsFileShare Property Methods</span></span>

<span data-ttu-id="834fb-106">Методы свойств интерфейса [**иадсфилешаре**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="834fb-106">The property methods of the [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="834fb-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="834fb-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="834fb-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="834fb-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="834fb-109">**куррентусеркаунт**</span><span class="sxs-lookup"><span data-stu-id="834fb-109">**CurrentUserCount**</span></span>
<span data-ttu-id="834fb-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="834fb-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="834fb-111">Число пользователей, подключенных к общей папке.</span><span class="sxs-lookup"><span data-stu-id="834fb-111">The number of users connected to the share.</span></span>

<dt>

<span data-ttu-id="834fb-112">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="834fb-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="834fb-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="834fb-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CurrentUserCount(
  [out] LONG* plCurrentUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="834fb-114">**Описание**</span><span class="sxs-lookup"><span data-stu-id="834fb-114">**Description**</span></span>
<span data-ttu-id="834fb-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="834fb-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="834fb-116">Описание общей папки.</span><span class="sxs-lookup"><span data-stu-id="834fb-116">The description of the file share.</span></span>

<dt>

<span data-ttu-id="834fb-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="834fb-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="834fb-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="834fb-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="834fb-119">**хосткомпутер**</span><span class="sxs-lookup"><span data-stu-id="834fb-119">**HostComputer**</span></span>
<span data-ttu-id="834fb-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="834fb-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="834fb-121">Путь ADsPath к главному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="834fb-121">An ADsPath reference to the host computer.</span></span>

<dt>

<span data-ttu-id="834fb-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="834fb-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="834fb-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="834fb-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="834fb-124">**максусеркаунт**</span><span class="sxs-lookup"><span data-stu-id="834fb-124">**MaxUserCount**</span></span>
<span data-ttu-id="834fb-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="834fb-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="834fb-126">Максимальное число пользователей, которым разрешено одновременный доступ к общей папке.</span><span class="sxs-lookup"><span data-stu-id="834fb-126">The maximum number of users allowed to access the share at one time.</span></span>

<dt>

<span data-ttu-id="834fb-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="834fb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="834fb-128">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="834fb-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="834fb-129">**Путь**</span><span class="sxs-lookup"><span data-stu-id="834fb-129">**Path**</span></span>
<span data-ttu-id="834fb-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="834fb-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="834fb-131">Путь файловой системы к общему каталогу.</span><span class="sxs-lookup"><span data-stu-id="834fb-131">The file system path to the shared directory.</span></span>

<dt>

<span data-ttu-id="834fb-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="834fb-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="834fb-133">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="834fb-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="834fb-134">Примеры</span><span class="sxs-lookup"><span data-stu-id="834fb-134">Examples</span></span>

<span data-ttu-id="834fb-135">Чтобы получить доступ к свойствам общих файловых ресурсов на компьютере, необходимо сначала выполнить привязку к "LanmanServer" на компьютере.</span><span class="sxs-lookup"><span data-stu-id="834fb-135">To access the properties of file shares on a computer, you must first bind to the "LanmanServer" on the machine.</span></span> <span data-ttu-id="834fb-136">В следующем примере кода показано, как настроить описание и максимальное число разрешенных пользователей для всех общедоступных файловых ресурсов на компьютере с именем "Мойкомпьютер" в домене по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="834fb-136">The following code example shows how to set up the description and the maximum number of allowed users for all the public file shares on the computer, named as "myMachine", in the default domain.</span></span>


```VB
Dim fs As IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://myMachine/LanmanServer")
If (fs.class = "FileService") Then
    For Each share In fs
        share.description = share.name & " is my working folder."
        share.MaxUserCount =  10
        share.SetInfo
    Next share
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
```



<span data-ttu-id="834fb-137">В следующем примере кода показано, как сделать существующий каталог C: \\ MyFolder общедоступным общим файловым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="834fb-137">The following code example shows how to make the existing C:\\MyFolder directory a public file share.</span></span>


```VB
Dim fs As IADsFileShare
Dim cont As IADsContainer
On Error GoTo Cleanup
 
Set cont = GetObject("WinNT://yourDomain/yourMachineName/LanmanServer")
 
Set fs = cont.Create("FileShare", "Public")
Debug.Print fs.Class
fs.Path = "C:\MyFolder"
fs.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set fs = Nothing
```



<span data-ttu-id="834fb-138">В следующем примере кода существующий каталог C: \\ MyFolder становится общедоступным общим файловым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="834fb-138">The following code example makes the existing C:\\MyFolder directory a public file share.</span></span>


```C++
IADsFileShare *pShare = NULL;
IADsContainer *pCont = NULL;
LPWSTR adsPath = L"WinNT://yourMachineName/LanmanServer";
HRESULT hr = S_OK;

hr = ADsGetObject(adsPath, IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->Create(CComBSTR("FileShare"), CComBSTR("Public"), (IDispatch**)&pShare);

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->put_Path(CComBSTR("c:\\public"));

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->SetInfo();

Cleanup:
    if(pCont) pCont->Release();
    if(pShare) pShare->Release();
```



## <a name="requirements"></a><span data-ttu-id="834fb-139">Требования</span><span class="sxs-lookup"><span data-stu-id="834fb-139">Requirements</span></span>



| <span data-ttu-id="834fb-140">Требование</span><span class="sxs-lookup"><span data-stu-id="834fb-140">Requirement</span></span> | <span data-ttu-id="834fb-141">Значение</span><span class="sxs-lookup"><span data-stu-id="834fb-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="834fb-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="834fb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="834fb-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="834fb-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="834fb-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="834fb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="834fb-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="834fb-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="834fb-146">Header</span><span class="sxs-lookup"><span data-stu-id="834fb-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="834fb-147"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="834fb-147"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="834fb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="834fb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="834fb-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="834fb-149"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="834fb-150">IID</span><span class="sxs-lookup"><span data-stu-id="834fb-150">IID</span></span><br/>                      | <span data-ttu-id="834fb-151">IID \_ иадсфилешаре определен как EB6DCAF0-4B83-11CF-A995-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="834fb-151">IID\_IADsFileShare is defined as EB6DCAF0-4B83-11CF-A995-00AA006BC149</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="834fb-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="834fb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="834fb-153">**иадссервице**</span><span class="sxs-lookup"><span data-stu-id="834fb-153">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="834fb-154">**иадсфилешаре**</span><span class="sxs-lookup"><span data-stu-id="834fb-154">**IADsFileShare**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileshare)
</dt> <dt>

[<span data-ttu-id="834fb-155">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="834fb-155">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





