---
title: Методы свойств Иадссессион (iAds. h)
description: Методы свойств интерфейса Иадссессион получают или задают свойства, описанные в следующей таблице. Дополнительные сведения и общее обсуждение методов свойств см. в разделе методы свойств интерфейса.
ms.assetid: b2366da7-c51c-4279-8931-2000d3110d72
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадссессион ADSI
topic_type:
- apiref
api_name:
- IADsSession Property Methods
- IADsSession.Computer
- IADsSession.get_Computer
- IADsSession.ComputerPath
- IADsSession.get_ComputerPath
- IADsSession.ConnectTime
- IADsSession.get_ConnectTime
- IADsSession.IdleTime
- IADsSession.get_IdleTime
- IADsSession.User
- IADsSession.get_User
- IADsSession.UserPath
- IADsSession.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf7dd9abe25d731ba63385cd8d632c4212ea349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891793"
---
# <a name="iadssession-property-methods"></a><span data-ttu-id="a23e3-105">Методы свойств Иадссессион</span><span class="sxs-lookup"><span data-stu-id="a23e3-105">IADsSession Property Methods</span></span>

<span data-ttu-id="a23e3-106">Методы свойств интерфейса [**иадссессион**](/windows/desktop/api/Iads/nn-iads-iadssession) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a23e3-106">The property methods of the [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="a23e3-107">Дополнительные сведения и общее обсуждение методов свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a23e3-107">For more information and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="a23e3-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="a23e3-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="a23e3-109">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="a23e3-109">**Computer**</span></span>
<span data-ttu-id="a23e3-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a23e3-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="a23e3-111">Имя клиентской рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="a23e3-111">Name of the client workstation.</span></span>

<dt>

<span data-ttu-id="a23e3-112">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a23e3-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a23e3-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a23e3-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Computer(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a23e3-114">**компутерпас**</span><span class="sxs-lookup"><span data-stu-id="a23e3-114">**ComputerPath**</span></span>
<span data-ttu-id="a23e3-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a23e3-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="a23e3-116">Путь к объекту компьютера для клиентской рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="a23e3-116">ADsPath of the computer object for the client workstation.</span></span>

<dt>

<span data-ttu-id="a23e3-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a23e3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a23e3-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a23e3-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerPath(
  [out] BSTR* pbstrComputerPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a23e3-119">**коннекттиме**</span><span class="sxs-lookup"><span data-stu-id="a23e3-119">**ConnectTime**</span></span>
<span data-ttu-id="a23e3-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a23e3-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="a23e3-121">Время, прошедшее с момента запуска сеанса (в секундах).</span><span class="sxs-lookup"><span data-stu-id="a23e3-121">Elapsed time, in seconds, since the session started.</span></span>

<dt>

<span data-ttu-id="a23e3-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a23e3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a23e3-123">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="a23e3-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ConnectTime(
  [out] LONG* plConnectTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a23e3-124">**идлетиме**</span><span class="sxs-lookup"><span data-stu-id="a23e3-124">**IdleTime**</span></span>
<span data-ttu-id="a23e3-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a23e3-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="a23e3-126">Время простоя в секундах сеанса.</span><span class="sxs-lookup"><span data-stu-id="a23e3-126">Idle time, in seconds, of the session.</span></span>

<dt>

<span data-ttu-id="a23e3-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a23e3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a23e3-128">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="a23e3-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IdleTime(
  [out] LONG* plIdleTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a23e3-129">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="a23e3-129">**User**</span></span>
<span data-ttu-id="a23e3-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a23e3-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="a23e3-131">Имя пользователя сеанса.</span><span class="sxs-lookup"><span data-stu-id="a23e3-131">The name of the user of the session.</span></span>

<dt>

<span data-ttu-id="a23e3-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a23e3-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a23e3-133">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a23e3-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a23e3-134">**усерпас**</span><span class="sxs-lookup"><span data-stu-id="a23e3-134">**UserPath**</span></span>
<span data-ttu-id="a23e3-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a23e3-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="a23e3-136">Путь к объекту пользователя для пользователя этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="a23e3-136">The ADsPath of the user object for the user of this session.</span></span>

<dt>

<span data-ttu-id="a23e3-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a23e3-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a23e3-138">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a23e3-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="a23e3-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="a23e3-139">Examples</span></span>

<span data-ttu-id="a23e3-140">В следующем примере кода показано, как проверить сеансы для службы файлов.</span><span class="sxs-lookup"><span data-stu-id="a23e3-140">The following code example shows how to examine sessions for a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
On Error GoTo Cleanup

' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate sessions.
If (IsEmpty(fso) = False) Then
    For Each session In fso.sessions
        MsgBox "Session Computer: " & session.Computer
        MsgBox "Session User: " & session.User
    Next Session
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="a23e3-141">В следующем примере кода перечисляются коллекции сеансов.</span><span class="sxs-lookup"><span data-stu-id="a23e3-141">The following code example enumerates a collection of sessions.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsSession *pSes = NULL;
IADsCollection *pColl = NULL;
HRESULT hr = S_OK;
IUnknown *pUnk = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IEnumVARIANT *pEnum = NULL;

VariantInit(&var);

LPWSTR adsPath = L"WinNT://aMachine/LanmanServer";

hr = ADsGetObject(adsPath,IID_IADsFileServiceOperations,
                  (void**)&pFso);

if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Sessions(&pColl);

// Enumerate sessions. 
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsSession, (void**)&pSes);
        pSes->get_Computer(&bstr);
        printf("Session host: %S\n",bstr);
        SysFreeString(bstr);

        pSes->get_User(&bstr);
        printf("Session user: %S\n",bstr);
        SysFreeString(bstr);

        pRes->Release();
    }

    VariantClear(&var);
    pDisp=NULL;
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pFso) pFso->Release();
    if(pColl) pColl->Release();
    if(pUnk) pUnk->Release();
    if(pEnum) pEnum->Release();
```



## <a name="requirements"></a><span data-ttu-id="a23e3-142">Требования</span><span class="sxs-lookup"><span data-stu-id="a23e3-142">Requirements</span></span>



| <span data-ttu-id="a23e3-143">Требование</span><span class="sxs-lookup"><span data-stu-id="a23e3-143">Requirement</span></span> | <span data-ttu-id="a23e3-144">Значение</span><span class="sxs-lookup"><span data-stu-id="a23e3-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a23e3-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a23e3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a23e3-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a23e3-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a23e3-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a23e3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a23e3-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a23e3-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a23e3-149">Header</span><span class="sxs-lookup"><span data-stu-id="a23e3-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a23e3-150"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="a23e3-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="a23e3-151">DLL</span><span class="sxs-lookup"><span data-stu-id="a23e3-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a23e3-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a23e3-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="a23e3-153">IID</span><span class="sxs-lookup"><span data-stu-id="a23e3-153">IID</span></span><br/>                      | <span data-ttu-id="a23e3-154">IID \_ иадссессион определен как 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="a23e3-154">IID\_IADsSession is defined as 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a23e3-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a23e3-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a23e3-156">**Иадсфилесервицеоператионс:: сеансы**</span><span class="sxs-lookup"><span data-stu-id="a23e3-156">**IADsFileServiceOperations::Sessions**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-sessions)
</dt> <dt>

[<span data-ttu-id="a23e3-157">**иадссессион**</span><span class="sxs-lookup"><span data-stu-id="a23e3-157">**IADsSession**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssession)
</dt> </dl>

 

 





