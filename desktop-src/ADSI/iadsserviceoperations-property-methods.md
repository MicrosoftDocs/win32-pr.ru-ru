---
title: Методы свойств Иадссервицеоператионс (iAds. h)
description: Методы свойств интерфейса Иадссервицеоператионс считывают и записывают свойства, описанные в следующем списке. Дополнительные сведения о методах свойств см. в разделе методы свойств интерфейса.
ms.assetid: ebddfc42-1d2f-495b-b57c-f57419b54ff8
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадссервицеоператионс ADSI
topic_type:
- apiref
api_name:
- IADsServiceOperations Property Methods
- IADsServiceOperations.Status
- IADsServiceOperations.get_Status
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 654a92be1052d4e4c70e0274d719a49be965d8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891794"
---
# <a name="iadsserviceoperations-property-methods"></a><span data-ttu-id="25e3e-105">Методы свойств Иадссервицеоператионс</span><span class="sxs-lookup"><span data-stu-id="25e3e-105">IADsServiceOperations Property Methods</span></span>

<span data-ttu-id="25e3e-106">Методы свойств интерфейса [**иадссервицеоператионс**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) считывают и записывают свойства, описанные в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="25e3e-106">The property methods of the [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) interface read and write the properties described in the following list.</span></span> <span data-ttu-id="25e3e-107">Дополнительные сведения о методах свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="25e3e-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="25e3e-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="25e3e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="25e3e-109">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="25e3e-109">**Status**</span></span>
<span data-ttu-id="25e3e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="25e3e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="25e3e-111">Состояние службы.</span><span class="sxs-lookup"><span data-stu-id="25e3e-111">Status of service.</span></span>

<span data-ttu-id="25e3e-112">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="25e3e-112">The following are possible values.</span></span>

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

<span data-ttu-id="25e3e-113">**Реклама \_ Служба \_ остановлена** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="25e3e-113">**ADS\_SERVICE\_STOPPED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

<span data-ttu-id="25e3e-114">**Реклама \_ \_ \_ Ожидание запуска службы** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="25e3e-114">**ADS\_SERVICE\_START\_PENDING** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

<span data-ttu-id="25e3e-115">**Реклама \_ \_ \_ Ожидание завершения службы** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="25e3e-115">**ADS\_SERVICE\_STOP\_PENDING** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

<span data-ttu-id="25e3e-116">**Реклама \_ Служба \_ работает** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="25e3e-116">**ADS\_SERVICE\_RUNNING** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

<span data-ttu-id="25e3e-117">**Реклама \_ \_ \_ Ожидается продолжение работы службы** (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="25e3e-117">**ADS\_SERVICE\_CONTINUE\_PENDING** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

<span data-ttu-id="25e3e-118">**Реклама \_ \_ \_ Ожидание приостановки службы** (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="25e3e-118">**ADS\_SERVICE\_PAUSE\_PENDING** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

<span data-ttu-id="25e3e-119">**Реклама \_ Служба \_ приостановлена** (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="25e3e-119">**ADS\_SERVICE\_PAUSED** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

<span data-ttu-id="25e3e-120">**Реклама \_ \_Ошибка службы** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="25e3e-120">**ADS\_SERVICE\_ERROR** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="25e3e-121">**Реклама \_ \_Собственный \_ процесс службы** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="25e3e-121">**ADS\_SERVICE\_OWN\_PROCESS** (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="25e3e-122">**Реклама \_ \_ \_ Процесс предоставления общего доступа к службе** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="25e3e-122">**ADS\_SERVICE\_SHARE\_PROCESS** (0x00000020)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="25e3e-123">**Реклама \_ \_ \_ Драйвер ядра службы** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="25e3e-123">**ADS\_SERVICE\_KERNEL\_DRIVER** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="25e3e-124">**Реклама \_ \_Драйвер файловой \_ системы \_ службы** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="25e3e-124">**ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="25e3e-125">**Реклама \_ \_ \_ Запуск службы** (загрузка службы \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="25e3e-125">**ADS\_SERVICE\_BOOT\_START** (SERVICE\_BOOT\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="25e3e-126">**Реклама \_ \_ \_ Запуск системы службы** ( \_ Запуск системы службы \_ )</span><span class="sxs-lookup"><span data-stu-id="25e3e-126">**ADS\_SERVICE\_SYSTEM\_START** (SERVICE\_SYSTEM\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="25e3e-127">**Реклама \_ \_автозапуск службы \_** ( \_ Автоматический запуск службы \_ )</span><span class="sxs-lookup"><span data-stu-id="25e3e-127">**ADS\_SERVICE\_AUTO\_START** (SERVICE\_AUTO\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="25e3e-128">**Реклама \_ \_ \_ Запуск запроса службы** ( \_ Запуск по требованию службы \_ )</span><span class="sxs-lookup"><span data-stu-id="25e3e-128">**ADS\_SERVICE\_DEMAND\_START** (SERVICE\_DEMAND\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="25e3e-129">**Реклама \_ Служба \_ отключена** (служба \_ отключена)</span><span class="sxs-lookup"><span data-stu-id="25e3e-129">**ADS\_SERVICE\_DISABLED** (SERVICE\_DISABLED)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="25e3e-130">**Реклама \_ \_ \_ Пропуск ошибки службы** (0)</span><span class="sxs-lookup"><span data-stu-id="25e3e-130">**ADS\_SERVICE\_ERROR\_IGNORE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="25e3e-131">**Реклама \_ Ошибка службы — \_ \_ Обычная** (1)</span><span class="sxs-lookup"><span data-stu-id="25e3e-131">**ADS\_SERVICE\_ERROR\_NORMAL** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="25e3e-132">**Реклама \_ \_ \_ Серьезная ошибка службы** (2)</span><span class="sxs-lookup"><span data-stu-id="25e3e-132">**ADS\_SERVICE\_ERROR\_SEVERE** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="25e3e-133">**Реклама \_ \_ \_ Критическая ошибка службы** (3)</span><span class="sxs-lookup"><span data-stu-id="25e3e-133">**ADS\_SERVICE\_ERROR\_CRITICAL** (3)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="25e3e-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25e3e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25e3e-135">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="25e3e-135">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="25e3e-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="25e3e-136">Examples</span></span>

<span data-ttu-id="25e3e-137">В следующем примере кода показано, как проверить состояние службы факсов Microsoft, работающей в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="25e3e-137">The following code example shows how to verify the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```VB
Dim cp As IADsComputer
Dim sr As IADsService
Dim so As IADsServiceOperations
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
Set sr = cp.GetObject("Service", "Fax")
Set so = sr

Select Case so.Status
    Case ADS_SERVICE_STOPPED
        MsgBox "Microsoft Fax Service has stopped."
    Case ADS_SERVICE_RUNNING
        MsgBox "Microsoft Fax Service is running."
    Case ADS_SERVICE_PAUSED
        MsgBox "Microsoft Fax Service has paused."
    Case ADS_SERVICE_ERROR
        MsgBox "Microsoft Fax Service has errors."
End Select

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
    Set sr = Nothing
    Set so = Nothing
```



<span data-ttu-id="25e3e-138">В следующем примере кода проверяется состояние службы факсов Майкрософт, работающей в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="25e3e-138">The following code example verifies the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```C++
IADsContainer *pCont = NULL;
IADsServiceOperations *pSrvOp = NULL;
LPWSTR adsPath = L"WinNT://myMachine,computer";
IDispatch *pDisp = NULL;
long status = 0;

HRESULT hr = S_OK;

hr = ADsGetObject(adsPath,IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->GetObject(CComBSTR("Service"), CComBSTR("Fax"), &pDisp);
if(FAILED(hr)) {goto Cleanup;}

hr = pDisp->QueryInterface(IID_IADsServiceOperations,(void**)&pSrvOp);
if(FAILED(hr)) {goto Cleanup;}

hr = pSrvOp->get_Status(&status);
switch (status) 
{
    case ADS_SERVICE_STOPPED:
        printf("The service has stopped.\n");
        break;
    case ADS_SERVICE_RUNNING:
        printf("The service is running.\n");
        break;
    case ADS_SERVICE_PAUSED:
        printf("The service has paused.\n");
        break;
    case ADS_SERVICE_ERROR:
        printf("The service has errors.\n");
        break;
}

Cleanup:
    if(pDisp) pDisp->Release();
    if(pCont) pCont->Release();
    if(pSrvOp) pSrvOp->Release();
```



## <a name="requirements"></a><span data-ttu-id="25e3e-139">Требования</span><span class="sxs-lookup"><span data-stu-id="25e3e-139">Requirements</span></span>



| <span data-ttu-id="25e3e-140">Требование</span><span class="sxs-lookup"><span data-stu-id="25e3e-140">Requirement</span></span> | <span data-ttu-id="25e3e-141">Значение</span><span class="sxs-lookup"><span data-stu-id="25e3e-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25e3e-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25e3e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="25e3e-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25e3e-143">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="25e3e-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25e3e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="25e3e-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25e3e-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="25e3e-146">Header</span><span class="sxs-lookup"><span data-stu-id="25e3e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="25e3e-147"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="25e3e-147"><dt>Iads.h</dt></span></span> </dl>        |
| <span data-ttu-id="25e3e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="25e3e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25e3e-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25e3e-149"><dt>Activeds.dll</dt></span></span> </dl>  |
| <span data-ttu-id="25e3e-150">IID</span><span class="sxs-lookup"><span data-stu-id="25e3e-150">IID</span></span><br/>                      | <span data-ttu-id="25e3e-151">IID \_ иадссервицеоператионс определен как 5D7B33F0-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="25e3e-151">IID\_IADsServiceOperations is defined as 5D7B33F0-31CA-11CF-A98A-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25e3e-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25e3e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e3e-153">**иадсфилесервице**</span><span class="sxs-lookup"><span data-stu-id="25e3e-153">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="25e3e-154">**иадсфилесервицеоператионс**</span><span class="sxs-lookup"><span data-stu-id="25e3e-154">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="25e3e-155">**иадссервице**</span><span class="sxs-lookup"><span data-stu-id="25e3e-155">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="25e3e-156">**иадссервицеоператионс**</span><span class="sxs-lookup"><span data-stu-id="25e3e-156">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 





