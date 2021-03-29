---
title: Методы свойств Иадспринткуеуе (iAds. h)
description: Методы свойств интерфейса Иадспринткуеуе получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 7f5b4200-65c8-4230-8561-ad4fefb391f3
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспринткуеуе ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueue Property Methods
- IADsPrintQueue.BannerPage
- IADsPrintQueue.get_BannerPage
- IADsPrintQueue.put_BannerPage
- IADsPrintQueue.Datatype
- IADsPrintQueue.get_Datatype
- IADsPrintQueue.put_Datatype
- IADsPrintQueue.DefaultJobPriority
- IADsPrintQueue.get_DefaultJobPriority
- IADsPrintQueue.put_DefaultJobPriority
- IADsPrintQueue.Description
- IADsPrintQueue.get_Description
- IADsPrintQueue.put_Description
- IADsPrintQueue.HostComputer
- IADsPrintQueue.get_HostComputer
- IADsPrintQueue.put_HostComputer
- IADsPrintQueue.Location
- IADsPrintQueue.get_Location
- IADsPrintQueue.put_Location
- IADsPrintQueue.Model
- IADsPrintQueue.get_Model
- IADsPrintQueue.put_Model
- IADsPrintQueue.PrintDevices
- IADsPrintQueue.get_PrintDevices
- IADsPrintQueue.put_PrintDevices
- IADsPrintQueue.PrinterPath
- IADsPrintQueue.get_PrinterPath
- IADsPrintQueue.put_PrinterPath
- IADsPrintQueue.PrintProcessor
- IADsPrintQueue.get_PrintProcessor
- IADsPrintQueue.put_PrintProcessor
- IADsPrintQueue.Priority
- IADsPrintQueue.get_Priority
- IADsPrintQueue.put_Priority
- IADsPrintQueue.StartTime
- IADsPrintQueue.get_StartTime
- IADsPrintQueue.put_StartTime
- IADsPrintQueue.UntilTime
- IADsPrintQueue.get_UntilTime
- IADsPrintQueue.put_UntilTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e8b7b2260805dbf5fa144f239111b6e29f5ec78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262206"
---
# <a name="iadsprintqueue-property-methods"></a><span data-ttu-id="05f2f-105">Методы свойств Иадспринткуеуе</span><span class="sxs-lookup"><span data-stu-id="05f2f-105">IADsPrintQueue Property Methods</span></span>

<span data-ttu-id="05f2f-106">Методы свойств интерфейса [**иадспринткуеуе**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="05f2f-106">The property methods of the [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="05f2f-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="05f2f-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="05f2f-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="05f2f-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="05f2f-109">**баннерпаже**</span><span class="sxs-lookup"><span data-stu-id="05f2f-109">**BannerPage**</span></span>
<span data-ttu-id="05f2f-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-111">Путь файловой системы, указывающий на страницу заголовка, используемую для разделения заданий печати.</span><span class="sxs-lookup"><span data-stu-id="05f2f-111">The file system path that points to the banner page used to separate print jobs.</span></span> <span data-ttu-id="05f2f-112">Если **значение равно NULL**, то страница баннера не используется.</span><span class="sxs-lookup"><span data-stu-id="05f2f-112">If **NULL**, no banner page is used.</span></span>

<dt>

<span data-ttu-id="05f2f-113">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-114">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="05f2f-114">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BannerPage(
  [out] BSTR* pbstrBannerPage
);
HRESULT put_BannerPage(
  [in] BSTR bstrBannerPage
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="05f2f-115">**Заданий**</span><span class="sxs-lookup"><span data-stu-id="05f2f-115">**Datatype**</span></span>
<span data-ttu-id="05f2f-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-117">Тип данных, который может быть обработан этой очередью.</span><span class="sxs-lookup"><span data-stu-id="05f2f-117">The data type that can be processed by this queue.</span></span>

<dt>

<span data-ttu-id="05f2f-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-119">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="05f2f-119">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Datatype(
  [out] BSTR* pbstrDatatype
);
HRESULT put_Datatype(
  [in] BSTR bstrDatatype
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="05f2f-120">**дефаултжобприорити**</span><span class="sxs-lookup"><span data-stu-id="05f2f-120">**DefaultJobPriority**</span></span>
<span data-ttu-id="05f2f-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-122">Приоритет по умолчанию, назначаемый каждому заданию печати.</span><span class="sxs-lookup"><span data-stu-id="05f2f-122">The default priority assigned to each print job.</span></span>

<dt>

<span data-ttu-id="05f2f-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-124">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="05f2f-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultJobPriority(
  [out] LONG* plDefaultJobPriority
);
HRESULT put_DefaultJobPriority(
  [in] BSTR lDefaultJobPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="05f2f-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="05f2f-125">**Description**</span></span>
<span data-ttu-id="05f2f-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-127">Текстовое описание этой очереди печати.</span><span class="sxs-lookup"><span data-stu-id="05f2f-127">The text description of this print queue.</span></span>

<dt>

<span data-ttu-id="05f2f-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-129">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="05f2f-129">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="05f2f-130">**хосткомпутер**</span><span class="sxs-lookup"><span data-stu-id="05f2f-130">**HostComputer**</span></span>
<span data-ttu-id="05f2f-131"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-131"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-132">Строка ADsPath, которая ссылается на главный компьютер.</span><span class="sxs-lookup"><span data-stu-id="05f2f-132">The ADsPath string that references the host computer.</span></span>

<dt>

<span data-ttu-id="05f2f-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-134">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="05f2f-134">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="05f2f-135">**Расположение**</span><span class="sxs-lookup"><span data-stu-id="05f2f-135">**Location**</span></span>
<span data-ttu-id="05f2f-136"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-136"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-137">Расположение очереди, описанное администратором.</span><span class="sxs-lookup"><span data-stu-id="05f2f-137">The location of the queue as described by an administrator.</span></span>

<dt>

<span data-ttu-id="05f2f-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-139">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="05f2f-139">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="05f2f-140">**Модель**</span><span class="sxs-lookup"><span data-stu-id="05f2f-140">**Model**</span></span>
<span data-ttu-id="05f2f-141"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-141"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-142">Имя драйвера, используемого этой очередью печати.</span><span class="sxs-lookup"><span data-stu-id="05f2f-142">The name of the driver used by this print queue.</span></span>

<dt>

<span data-ttu-id="05f2f-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-144">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="05f2f-144">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="05f2f-145">**принтдевицес**</span><span class="sxs-lookup"><span data-stu-id="05f2f-145">**PrintDevices**</span></span>
<span data-ttu-id="05f2f-146"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-146"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-147">МАССИВ SAFEARRAY типа **BSTR** , содержащий имена устройств печати, на которых в очереди печати находятся задания.</span><span class="sxs-lookup"><span data-stu-id="05f2f-147">A SAFEARRAY of **BSTR** that contains the names of the print devices to which this print queue spools jobs.</span></span>

<dt>

<span data-ttu-id="05f2f-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-149">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="05f2f-149">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintDevices(
  [out] VARIANT* pvPrintDevices
);
HRESULT put_PrintDevices(
  [in] VARIANT vPrintDevices
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="05f2f-150">**принтерпас**</span><span class="sxs-lookup"><span data-stu-id="05f2f-150">**PrinterPath**</span></span>
<span data-ttu-id="05f2f-151"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-151"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-152">Строка, которая ссылается на путь, по которому можно получить доступ к общему принтеру.</span><span class="sxs-lookup"><span data-stu-id="05f2f-152">The string that references the path by which a shared printer can be accessed.</span></span>

<dt>

<span data-ttu-id="05f2f-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-154">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="05f2f-154">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrinterPath(
  [out] BSTR* pbstrPrinterPath
);
HRESULT put_PrinterPath(
  [in] BSTR bstrPrinterPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="05f2f-155">**принтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="05f2f-155">**PrintProcessor**</span></span>
<span data-ttu-id="05f2f-156"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-156"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-157">Обработчик печати, связанный с этой очередью.</span><span class="sxs-lookup"><span data-stu-id="05f2f-157">The print processor associated with this queue.</span></span>

<dt>

<span data-ttu-id="05f2f-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-159">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="05f2f-159">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintProcessor(
  [out] BSTR* pbstrPrintProcessor
);
HRESULT put_PrintProcessor(
  [in] BSTR bstrPrintProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="05f2f-160">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="05f2f-160">**Priority**</span></span>
<span data-ttu-id="05f2f-161"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-161"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-162">Приоритет очереди заданий объекта принтера для всех подключенных устройств.</span><span class="sxs-lookup"><span data-stu-id="05f2f-162">The priority of this printer object job queue for any connected devices.</span></span> <span data-ttu-id="05f2f-163">Все задания с более высоким приоритетом объекты очереди печати будут обработаны первыми.</span><span class="sxs-lookup"><span data-stu-id="05f2f-163">All jobs in higher priority print queue objects will be processed first.</span></span>

<dt>

<span data-ttu-id="05f2f-164">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-164">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-165">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="05f2f-165">Scripting data type: **LONG**</span></span>
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

<span data-ttu-id="05f2f-166">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="05f2f-166">**StartTime**</span></span>
<span data-ttu-id="05f2f-167"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-167"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-168">Время, когда очередь должна начать обработку заданий.</span><span class="sxs-lookup"><span data-stu-id="05f2f-168">The time when the queue should begin processing jobs.</span></span> <span data-ttu-id="05f2f-169">Часть времени, относящаяся к дате, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="05f2f-169">The date portion of the time is ignored.</span></span>

<dt>

<span data-ttu-id="05f2f-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-171">Тип данных скрипта: **Дата**</span><span class="sxs-lookup"><span data-stu-id="05f2f-171">Scripting data type: **DATE**</span></span>
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

<span data-ttu-id="05f2f-172">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="05f2f-172">**UntilTime**</span></span>
<span data-ttu-id="05f2f-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="05f2f-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="05f2f-174">Время, когда очередь должна прерывать обработку заданий.</span><span class="sxs-lookup"><span data-stu-id="05f2f-174">The time when the queue should stop processing jobs.</span></span>

<dt>

<span data-ttu-id="05f2f-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="05f2f-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05f2f-176">Тип данных скрипта: **Дата**</span><span class="sxs-lookup"><span data-stu-id="05f2f-176">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
HRESULT put_UntilTime(
  [in] DATE dateUntilTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="05f2f-177">Примеры</span><span class="sxs-lookup"><span data-stu-id="05f2f-177">Examples</span></span>

<span data-ttu-id="05f2f-178">В следующем примере кода показано, как определить, находится ли указанный принтер в сети или в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="05f2f-178">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```VB
Dim pq As IADsPrintQueue
Dim pqo As IADsPrintQueueOperations
On Error GoTo Cleanup
 
Set pq = GetObject("WinNT://aMachine/aPrinter")
Set pqo = pq
If pqo.status = ADS_PRINTER_OFFLINE Then
    MsgBox pq.Model & "@" & pq.Location & is offline."
Else
    MsgBox pq.Model & "@" & pq.Location & is online."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pq = Nothing
    Set pqo = Nothing
```



<span data-ttu-id="05f2f-179">В следующем примере кода показано, как определить, находится ли указанный принтер в сети или в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="05f2f-179">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```C++
IADsPrintQueue *pq = NULL;
HRESULT hr = S_OK;
IADsPrintQueueOperations *pqo = NULL;
BSTR model = NULL;
BSTR location = NULL;

LPWSTR adsPath = L"WinNT://aMachine/aPrinter";
hr = ADsGetObject(adsPath,
                  IID_IADsPrintQueue,
                  (void**)&pq);
if(FAILED(hr)) {goto Cleanup;}


hr = pq->QueryInterface(IID_IADsPrintQueueOperations,(void**)&pqo);
if(FAILED(hr)) {goto Cleanup;}

long status;
hr = pqo->get_Status(&status);
if(FAILED(hr)) {goto Cleanup;}

hr = pq->get_Model(&model);
if(FAILED(hr)) {goto Cleanup;}

hr =pq->get_Location(&location);
if(FAILED(hr)) {goto Cleanup;}

if(status == ADS_PRINTER_OFFLINE) 
{
    printf("%S @ %S is offline.\n",model,location);
} 
else 
{
    printf("%S @ %S is online.\n",model,location);
}


Cleanup:
    SysFreeString(model);
    SysFreeString(location);
    if(pq) pq->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="05f2f-180">Требования</span><span class="sxs-lookup"><span data-stu-id="05f2f-180">Requirements</span></span>



| <span data-ttu-id="05f2f-181">Требование</span><span class="sxs-lookup"><span data-stu-id="05f2f-181">Requirement</span></span> | <span data-ttu-id="05f2f-182">Значение</span><span class="sxs-lookup"><span data-stu-id="05f2f-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05f2f-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05f2f-183">Minimum supported client</span></span><br/> | <span data-ttu-id="05f2f-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05f2f-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05f2f-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05f2f-185">Minimum supported server</span></span><br/> | <span data-ttu-id="05f2f-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05f2f-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05f2f-187">Header</span><span class="sxs-lookup"><span data-stu-id="05f2f-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="05f2f-188"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="05f2f-188"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="05f2f-189">DLL</span><span class="sxs-lookup"><span data-stu-id="05f2f-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05f2f-190"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05f2f-190"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="05f2f-191">IID</span><span class="sxs-lookup"><span data-stu-id="05f2f-191">IID</span></span><br/>                      | <span data-ttu-id="05f2f-192">IID \_ иадспринткуеуе определен как B15160D0-1226-11CF-A985-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="05f2f-192">IID\_IADsPrintQueue is defined as B15160D0-1226-11CF-A985-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="05f2f-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05f2f-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f2f-194">**иадспринткуеуе**</span><span class="sxs-lookup"><span data-stu-id="05f2f-194">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="05f2f-195">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="05f2f-195">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





