---
description: Удаляет все задания, включая текущую печать из очереди.
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Метод Канцелаллжобс класса Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d2d816dab837aafd7b6e9c6beff75c4e62b19b2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895534"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a><span data-ttu-id="9c574-103">Метод Канцелаллжобс \_ класса принтера Win32</span><span class="sxs-lookup"><span data-stu-id="9c574-103">CancelAllJobs method of the Win32\_Printer class</span></span>

<span data-ttu-id="9c574-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) канцелаллжобс удаляет все задания, включая текущую печать из очереди.</span><span class="sxs-lookup"><span data-stu-id="9c574-104">The **CancelAllJobs** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method removes all jobs, including the one currently printing from the queue.</span></span>

<span data-ttu-id="9c574-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="9c574-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9c574-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9c574-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c574-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c574-107">Syntax</span></span>


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a><span data-ttu-id="9c574-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c574-108">Parameters</span></span>

<span data-ttu-id="9c574-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9c574-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9c574-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c574-110">Return value</span></span>

<span data-ttu-id="9c574-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="9c574-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="9c574-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9c574-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9c574-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9c574-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9c574-114">**0**</span><span class="sxs-lookup"><span data-stu-id="9c574-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="9c574-115">Успешно</span><span class="sxs-lookup"><span data-stu-id="9c574-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="9c574-116">**5**</span><span class="sxs-lookup"><span data-stu-id="9c574-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="9c574-117">доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="9c574-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9c574-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="9c574-118">Examples</span></span>

<span data-ttu-id="9c574-119">[Уведомление пользователей об очистке очереди печати](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) использует Msg.exe для отправки сетевого оповещения всем пользователям, имеющим документы в очереди печати, для очистки.</span><span class="sxs-lookup"><span data-stu-id="9c574-119">The [Notify Users When a Print Queue is Purged](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) uses Msg.exe to send a network alert to any users who had documents in a print queue about to be purged.</span></span> <span data-ttu-id="9c574-120">После отправки предупреждений сценарий удаляет очередь печати.</span><span class="sxs-lookup"><span data-stu-id="9c574-120">After sending the alerts, the script purges the print queue.</span></span>

<span data-ttu-id="9c574-121">Пример кода VBScript " [удалить все задания печати](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) " удаляет все задания печати на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9c574-121">The [Delete all print jobs](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) VBScript code sample deletes all print jobs on the local computer.</span></span>

<span data-ttu-id="9c574-122">Следующий пример сценария VBScript удаляет все задания печати для принтера с именем HP Куиетжет.</span><span class="sxs-lookup"><span data-stu-id="9c574-122">The following VBScript sample deletes all the print jobs for a printer named HP QuietJet.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="9c574-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9c574-123">Requirements</span></span>



| <span data-ttu-id="9c574-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9c574-124">Requirement</span></span> | <span data-ttu-id="9c574-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9c574-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c574-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c574-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9c574-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c574-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="9c574-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c574-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9c574-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c574-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="9c574-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9c574-130">Namespace</span></span><br/>                | <span data-ttu-id="9c574-131">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9c574-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="9c574-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9c574-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c574-133"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c574-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c574-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9c574-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c574-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c574-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="9c574-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c574-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c574-137">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="9c574-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="9c574-138">**\_Принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="9c574-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

