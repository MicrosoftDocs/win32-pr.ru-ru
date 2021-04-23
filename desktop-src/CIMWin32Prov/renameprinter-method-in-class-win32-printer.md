---
description: Переименовывает принтер.
ms.assetid: afbef871-5153-4b9e-9ad3-4d271a497c37
ms.tgt_platform: multiple
title: Метод Ренамепринтер класса Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.RenamePrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6066dfd4280f7c43c9804933fb1ed5fb931bfa08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262504"
---
# <a name="renameprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="ca439-103">Метод Ренамепринтер \_ класса принтера Win32</span><span class="sxs-lookup"><span data-stu-id="ca439-103">RenamePrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="ca439-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ренамепринтер переименовывает принтер.</span><span class="sxs-lookup"><span data-stu-id="ca439-104">The **RenamePrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a printer.</span></span>

<span data-ttu-id="ca439-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="ca439-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ca439-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ca439-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca439-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca439-107">Syntax</span></span>


```mof
uint32 RenamePrinter(
  [in] string NewPrinterName
);
```



## <a name="parameters"></a><span data-ttu-id="ca439-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca439-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca439-109">*Невпринтернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca439-109">*NewPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca439-110">Новое имя принтера.</span><span class="sxs-lookup"><span data-stu-id="ca439-110">New printer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca439-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca439-111">Return value</span></span>

<span data-ttu-id="ca439-112">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="ca439-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="ca439-113">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ca439-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ca439-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ca439-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ca439-115">**0**</span><span class="sxs-lookup"><span data-stu-id="ca439-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ca439-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="ca439-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="ca439-117">**5**</span><span class="sxs-lookup"><span data-stu-id="ca439-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ca439-118">доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="ca439-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="ca439-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="ca439-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="ca439-120">Недопустимое имя принтера</span><span class="sxs-lookup"><span data-stu-id="ca439-120">Invalid Printer Name</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ca439-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="ca439-121">Examples</span></span>

<span data-ttu-id="ca439-122">В следующем примере на языке VBScript переименовывается принтер и имя общего ресурса принтера.</span><span class="sxs-lookup"><span data-stu-id="ca439-122">The following VBScript example renames both a printer and its printer share name.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where DeviceID = 'HP LaserJet 4Si M'") 
 
For Each objPrinter in colPrinters 
    objPrinter.RenamePrinter("ArtDepartmentPrinter") 
Next 
 
Set colPrinters = objWMIService.ExecQuery _ 
    ("Select * From Win32_Printer Where DeviceID = 'ArtDepartmentPrinter' ") 
 
For Each objPrinter in colPrinters 
    objPrinter.ShareName = "ArtDepartmentPrinter" 
    objPrinter.Put_ 
Next 
```



## <a name="requirements"></a><span data-ttu-id="ca439-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ca439-123">Requirements</span></span>



| <span data-ttu-id="ca439-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ca439-124">Requirement</span></span> | <span data-ttu-id="ca439-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ca439-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca439-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca439-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ca439-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca439-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="ca439-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca439-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ca439-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca439-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="ca439-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ca439-130">Namespace</span></span><br/>                | <span data-ttu-id="ca439-131">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ca439-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="ca439-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ca439-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca439-133"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca439-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca439-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ca439-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca439-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca439-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ca439-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca439-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca439-137">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="ca439-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ca439-138">**\_Принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="ca439-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

