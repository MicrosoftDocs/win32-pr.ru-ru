---
description: Обеспечивает подключение к существующему принтеру в сети и добавляет его в список доступных принтеров.
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: Метод Аддпринтерконнектион класса Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2ad9e225a60e33fdf51d5f677dd4342acd148b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895541"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a><span data-ttu-id="8b660-103">Метод Аддпринтерконнектион \_ класса принтера Win32</span><span class="sxs-lookup"><span data-stu-id="8b660-103">AddPrinterConnection method of the Win32\_Printer class</span></span>

<span data-ttu-id="8b660-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) аддпринтерконнектион обеспечивает подключение к существующему принтеру в сети и добавляет его в список доступных принтеров.</span><span class="sxs-lookup"><span data-stu-id="8b660-104">The **AddPrinterConnection** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method provides a connection to an existing printer on the network, and adds it to the list of available printers.</span></span>

<span data-ttu-id="8b660-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="8b660-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8b660-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8b660-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b660-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b660-107">Syntax</span></span>


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="8b660-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b660-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b660-109">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8b660-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b660-110">Понятное имя принтера.</span><span class="sxs-lookup"><span data-stu-id="8b660-110">Friendly name for the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b660-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b660-111">Return value</span></span>

<span data-ttu-id="8b660-112">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="8b660-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="8b660-113">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8b660-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8b660-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8b660-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8b660-115">**0**</span><span class="sxs-lookup"><span data-stu-id="8b660-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8b660-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="8b660-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="8b660-117">**5**</span><span class="sxs-lookup"><span data-stu-id="8b660-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="8b660-118">доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="8b660-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="8b660-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="8b660-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="8b660-120">Недопустимое имя принтера</span><span class="sxs-lookup"><span data-stu-id="8b660-120">Invalid Printer Name</span></span>

</dd> <dt>

<span data-ttu-id="8b660-121">**1930**</span><span class="sxs-lookup"><span data-stu-id="8b660-121">**1930**</span></span>
</dt> <dd>

<span data-ttu-id="8b660-122">Несовместимый драйвер принтера</span><span class="sxs-lookup"><span data-stu-id="8b660-122">Incompatible Printer Driver</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8b660-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="8b660-123">Examples</span></span>

<span data-ttu-id="8b660-124">Образец PowerShell [Add-принтердривер](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) устанавливает все драйверы принтеров с указанного сервера печати.</span><span class="sxs-lookup"><span data-stu-id="8b660-124">The [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) PowerShell sample installs all printer drivers from a specified print server.</span></span>

<span data-ttu-id="8b660-125">В [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) примере PowerShell перечисляются общие принтеры на удаленном компьютере и предоставляется возможность добавить подключение принтера с удаленного компьютера на компьютер.</span><span class="sxs-lookup"><span data-stu-id="8b660-125">The [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell sample lists shared printers on a remote comptuer, and gives you the ability to add a printer connection from the remote computer to your computer.</span></span>

<span data-ttu-id="8b660-126">В следующем примере кода VBScript добавляется локальный принтер.</span><span class="sxs-lookup"><span data-stu-id="8b660-126">The following VBScript code sample adds a local printer.</span></span>


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
```



## <a name="requirements"></a><span data-ttu-id="8b660-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8b660-127">Requirements</span></span>



| <span data-ttu-id="8b660-128">Требование</span><span class="sxs-lookup"><span data-stu-id="8b660-128">Requirement</span></span> | <span data-ttu-id="8b660-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8b660-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b660-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b660-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8b660-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b660-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="8b660-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b660-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8b660-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b660-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="8b660-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8b660-134">Namespace</span></span><br/>                | <span data-ttu-id="8b660-135">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8b660-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="8b660-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8b660-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b660-137"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b660-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b660-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8b660-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b660-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b660-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="8b660-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b660-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b660-141">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="8b660-141">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8b660-142">Задачи WMI: принтеры и печать</span><span class="sxs-lookup"><span data-stu-id="8b660-142">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="8b660-143">**\_Принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="8b660-143">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

