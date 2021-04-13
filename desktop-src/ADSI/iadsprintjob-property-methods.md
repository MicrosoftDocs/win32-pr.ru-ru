---
title: Методы свойств Иадспринтжоб (iAds. h)
description: Методы свойств для интерфейса Иадспринтжоб получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 23e7cbf3-09ce-44ce-b618-2c0fa6b34428
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспринтжоб ADSI
topic_type:
- apiref
api_name:
- IADsPrintJob Property Methods
- IADsPrintJob.Description
- IADsPrintJob.get_Description
- IADsPrintJob.put_Description
- IADsPrintJob.HostPrintQueue
- IADsPrintJob.get_HostPrintQueue
- IADsPrintJob.Notify
- IADsPrintJob.get_Notify
- IADsPrintJob.put_Notify
- IADsPrintJob.NotifyPath
- IADsPrintJob.get_NotifyPath
- IADsPrintJob.put_NotifyPath
- IADsPrintJob.Priority
- IADsPrintJob.get_Priority
- IADsPrintJob.put_Priority
- IADsPrintJob.Size
- IADsPrintJob.get_Size
- IADsPrintJob.StartTime
- IADsPrintJob.get_StartTime
- IADsPrintJob.put_StartTime
- IADsPrintJob.TimeSubmitted
- IADsPrintJob.get_TimeSubmitted
- IADsPrintJob.TotalPages
- IADsPrintJob.get_TotalPages
- IADsPrintJob.UntilTime
- IADsPrintJob.get_UntilTime
- IADsPrintJob.User
- IADsPrintJob.get_User
- IADsPrintJob.UserPath
- IADsPrintJob.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1680484ff16d563ef5bc89de6d5abbfec2ce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492012"
---
# <a name="iadsprintjob-property-methods"></a><span data-ttu-id="0c13d-105">Методы свойств Иадспринтжоб</span><span class="sxs-lookup"><span data-stu-id="0c13d-105">IADsPrintJob Property Methods</span></span>

<span data-ttu-id="0c13d-106">Методы свойств для интерфейса [**иадспринтжоб**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0c13d-106">Property methods for the [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="0c13d-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="0c13d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="0c13d-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c13d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="0c13d-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0c13d-109">**Description**</span></span>
<span data-ttu-id="0c13d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-111">Описание задания печати.</span><span class="sxs-lookup"><span data-stu-id="0c13d-111">The description of the print job.</span></span>

<dt>

<span data-ttu-id="0c13d-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c13d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0c13d-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="0c13d-114">**хостпринткуеуе**</span><span class="sxs-lookup"><span data-stu-id="0c13d-114">**HostPrintQueue**</span></span>
<span data-ttu-id="0c13d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-116">Строка ADsPath очереди печати, которая обрабатывает задание печати.</span><span class="sxs-lookup"><span data-stu-id="0c13d-116">The ADsPath string of the Print Queue that processes the print job.</span></span>

<dt>

<span data-ttu-id="0c13d-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c13d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0c13d-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostPrintQueue(
  [out] BSTR* pbstrHostPrintQueue
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c13d-119">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="0c13d-119">**Notify**</span></span>
<span data-ttu-id="0c13d-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-121">Пользователь, который будет уведомлен о завершении задания.</span><span class="sxs-lookup"><span data-stu-id="0c13d-121">The user to be notified when job is completed.</span></span>

<dt>

<span data-ttu-id="0c13d-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c13d-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0c13d-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Notify(
  [out] BSTR* pbstrNotify
);
HRESULT put_Notify(
  [in] BSTR bstrNotify
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c13d-124">**нотифипас**</span><span class="sxs-lookup"><span data-stu-id="0c13d-124">**NotifyPath**</span></span>
<span data-ttu-id="0c13d-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-126">Строка ADsPath объекта User, которая будет уведомлена о завершении задания печати.</span><span class="sxs-lookup"><span data-stu-id="0c13d-126">The ADsPath string of the user object to be notified when the print job is completed.</span></span>

<dt>

<span data-ttu-id="0c13d-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c13d-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-128">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0c13d-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NotifyPath(
  [out] BSTR* pbstrNotifyPath
);
HRESULT put_NotifyPath(
  [in] BSTR bstrNotifyPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c13d-129">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="0c13d-129">**Priority**</span></span>
<span data-ttu-id="0c13d-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-131">Приоритет задания печати.</span><span class="sxs-lookup"><span data-stu-id="0c13d-131">The priority of the print job.</span></span>

<dt>

<span data-ttu-id="0c13d-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c13d-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-133">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="0c13d-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Priority(
  [out] LONG* plPriority
);
HRESULT put_Priority(
  [in] LONG lPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c13d-134">**Размер**</span><span class="sxs-lookup"><span data-stu-id="0c13d-134">**Size**</span></span>
<span data-ttu-id="0c13d-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-136">Размер задания печати в байтах.</span><span class="sxs-lookup"><span data-stu-id="0c13d-136">The size, in bytes, of the print job.</span></span>

<dt>

<span data-ttu-id="0c13d-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c13d-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-138">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="0c13d-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Size(
  [out] LONG* plSize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c13d-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="0c13d-139">**StartTime**</span></span>
<span data-ttu-id="0c13d-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-141">Самое раннее время запуска задания печати.</span><span class="sxs-lookup"><span data-stu-id="0c13d-141">The earliest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="0c13d-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c13d-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-143">Тип данных скрипта: **Дата**</span><span class="sxs-lookup"><span data-stu-id="0c13d-143">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartTime(
  [out] DATE* pdateStartTime
);
HRESULT put_StartTime(
  [in] DATE dateStartTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c13d-144">**тимесубмиттед**</span><span class="sxs-lookup"><span data-stu-id="0c13d-144">**TimeSubmitted**</span></span>
<span data-ttu-id="0c13d-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-146">Время, когда задание было отправлено в очередь.</span><span class="sxs-lookup"><span data-stu-id="0c13d-146">The time when the job was submitted to the queue.</span></span>

<dt>

<span data-ttu-id="0c13d-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c13d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-148">Тип данных скрипта: **Дата**</span><span class="sxs-lookup"><span data-stu-id="0c13d-148">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeSubmitted(
  [out] DATE* pdateTimeSubmitted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c13d-149">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="0c13d-149">**TotalPages**</span></span>
<span data-ttu-id="0c13d-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-151">Общее число страниц в задании печати.</span><span class="sxs-lookup"><span data-stu-id="0c13d-151">The total number of pages in the print job.</span></span>

<dt>

<span data-ttu-id="0c13d-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c13d-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-153">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="0c13d-153">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TotalPages(
  [out] LONG* plTotalPages
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c13d-154">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="0c13d-154">**UntilTime**</span></span>
<span data-ttu-id="0c13d-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-156">Последнее время, когда должно быть запущено задание печати.</span><span class="sxs-lookup"><span data-stu-id="0c13d-156">The latest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="0c13d-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c13d-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-158">Тип данных скрипта: **Дата**</span><span class="sxs-lookup"><span data-stu-id="0c13d-158">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c13d-159">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="0c13d-159">**User**</span></span>
<span data-ttu-id="0c13d-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-161">Имя пользователя, отправившего задание печати.</span><span class="sxs-lookup"><span data-stu-id="0c13d-161">The name of user who submitted the print job.</span></span>

<dt>

<span data-ttu-id="0c13d-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c13d-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-163">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0c13d-163">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c13d-164">**усерпас**</span><span class="sxs-lookup"><span data-stu-id="0c13d-164">**UserPath**</span></span>
<span data-ttu-id="0c13d-165"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0c13d-165"></dt> <dd> <dl></span></span>

<span data-ttu-id="0c13d-166">Строка ADsPath объекта пользователя, отправившего это задание печати.</span><span class="sxs-lookup"><span data-stu-id="0c13d-166">The ADsPath string of the user object that submitted this print job.</span></span>

<dt>

<span data-ttu-id="0c13d-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c13d-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c13d-168">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0c13d-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="0c13d-169">Примеры</span><span class="sxs-lookup"><span data-stu-id="0c13d-169">Examples</span></span>

<span data-ttu-id="0c13d-170">В следующем примере кода показано, как работать со свойствами объекта задания печати.</span><span class="sxs-lookup"><span data-stu-id="0c13d-170">The following code example shows how to work with properties of a print job object.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pj As IADsPrintJob
On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    MsgBox "Host Printer: " & pj.HostPrintQueue
    MsgBox "Job description: " & pj.Description
    MsgBox "job requester: " & pj.User 
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pj = Nothing
```



<span data-ttu-id="0c13d-171">В следующем примере кода показано, как работать со свойствами объекта задания печати.</span><span class="sxs-lookup"><span data-stu-id="0c13d-171">The following code example shows how to work with properties of a print job object.</span></span>


```C++
IADsPrintQueueOperations *pqo = NULL;
IADsPrintJob *pJob = NULL;
HRESULT hr = S_OK;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
LPWSTR adsPath =L"WinNT://aMachine/aPrinter";

VariantInit(&var);

hr = ADsGetObject(adsPath, 
                  IID_IADsPrintQueueOperations, 
                  (void**)&pqo);
if(FAILED(hr)){goto Cleanup;}


hr = pqo->PrintJobs(&pColl);

// Enumerate print jobs. Code omitted.

hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)){goto Cleanup;}


IEnumVARIANT *pEnum;
hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)){goto Cleanup;}


// Now Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
if(FAILED(hr)){goto Cleanup;}

while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsPrintJob, (void**)&pJob);

        pJob->get_HostPrintQueue(&bstr);
        printf("HostPrintQueue: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_Description(&bstr);
        printf("Print job name: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_User(&bstr);
        printf("Requester: %S\n",bstr);
        SysFreeString(bstr);

        pJob->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="0c13d-172">Требования</span><span class="sxs-lookup"><span data-stu-id="0c13d-172">Requirements</span></span>



| <span data-ttu-id="0c13d-173">Требование</span><span class="sxs-lookup"><span data-stu-id="0c13d-173">Requirement</span></span> | <span data-ttu-id="0c13d-174">Значение</span><span class="sxs-lookup"><span data-stu-id="0c13d-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c13d-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c13d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="0c13d-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c13d-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c13d-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c13d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="0c13d-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c13d-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c13d-179">Header</span><span class="sxs-lookup"><span data-stu-id="0c13d-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c13d-180"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c13d-180"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="0c13d-181">DLL</span><span class="sxs-lookup"><span data-stu-id="0c13d-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c13d-182"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c13d-182"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="0c13d-183">IID</span><span class="sxs-lookup"><span data-stu-id="0c13d-183">IID</span></span><br/>                      | <span data-ttu-id="0c13d-184">IID \_ иадспринтжоб определен как 32FB6780-1ED0-11CF-A988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="0c13d-184">IID\_IADsPrintJob is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="0c13d-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c13d-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c13d-186">**иадспринтжоб**</span><span class="sxs-lookup"><span data-stu-id="0c13d-186">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="0c13d-187">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="0c13d-187">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





