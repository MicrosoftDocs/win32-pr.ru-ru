---
description: Метод класса WMI SetDefaultPrinter задает системный принтер по умолчанию для пользователя, вызывающего метод.
ms.assetid: 7e896961-363d-4b8b-9d22-bbfc9681e97b
ms.tgt_platform: multiple
title: Метод SetDefaultPrinter класса Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetDefaultPrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a18c6d7771eb0e95d86142f41262d721509eb6f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896506"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="12726-103">Метод SetDefaultPrinter \_ класса принтера Win32</span><span class="sxs-lookup"><span data-stu-id="12726-103">SetDefaultPrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="12726-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) SetDefaultPrinter задает системный принтер по умолчанию для пользователя, вызывающего метод.</span><span class="sxs-lookup"><span data-stu-id="12726-104">The **SetDefaultPrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the default system printer for the user calling the method.</span></span>

<span data-ttu-id="12726-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="12726-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="12726-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="12726-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="12726-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12726-107">Syntax</span></span>


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a><span data-ttu-id="12726-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="12726-108">Parameters</span></span>

<span data-ttu-id="12726-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="12726-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12726-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12726-110">Return value</span></span>

<span data-ttu-id="12726-111">Возвращает 0 (нуль) в случае успеха и другое значение, если возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="12726-111">Returns 0 (zero) if successful, and some other value if an error occurs.</span></span> <span data-ttu-id="12726-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="12726-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="12726-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="12726-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="examples"></a><span data-ttu-id="12726-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="12726-114">Examples</span></span>

<span data-ttu-id="12726-115">В примере [установки принтера TCP/IP-порта и принтера](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) на языке VBScript устанавливается порт принтера TCP/IP, устанавливается принтер, а затем принтеру назначается значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="12726-115">The [Install a TCP/IP Printer Port and Printer](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) VBScript sample installs a TCP/IP printer port, installs a printer, and then sets the printer to be default.</span></span>

<span data-ttu-id="12726-116">Следующий пример кода VBScript задает принтер по умолчанию на компьютере.</span><span class="sxs-lookup"><span data-stu-id="12726-116">The following VBScript code sample sets the default printer on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'ScriptedPrinter'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.SetDefaultPrinter() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="12726-117">Требования</span><span class="sxs-lookup"><span data-stu-id="12726-117">Requirements</span></span>



| <span data-ttu-id="12726-118">Требование</span><span class="sxs-lookup"><span data-stu-id="12726-118">Requirement</span></span> | <span data-ttu-id="12726-119">Значение</span><span class="sxs-lookup"><span data-stu-id="12726-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="12726-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12726-120">Minimum supported client</span></span><br/> | <span data-ttu-id="12726-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12726-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="12726-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12726-122">Minimum supported server</span></span><br/> | <span data-ttu-id="12726-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12726-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="12726-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="12726-124">Namespace</span></span><br/>                | <span data-ttu-id="12726-125">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="12726-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="12726-126">MOF</span><span class="sxs-lookup"><span data-stu-id="12726-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12726-127"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12726-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="12726-128">DLL</span><span class="sxs-lookup"><span data-stu-id="12726-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12726-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12726-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="12726-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12726-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12726-131">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="12726-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="12726-132">Задачи WMI: принтеры и печать</span><span class="sxs-lookup"><span data-stu-id="12726-132">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="12726-133">**\_Принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="12726-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

