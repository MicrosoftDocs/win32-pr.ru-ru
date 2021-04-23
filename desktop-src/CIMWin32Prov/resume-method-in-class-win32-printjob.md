---
description: Метод класса Resume WMI продолжает приостановленное задание печати.
ms.assetid: acfbca2b-19af-4339-bbca-834db50c3d8d
ms.tgt_platform: multiple
title: Метод Resume класса Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8ca1602eb29e1e18d83d2e8b79760d13f63e101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655708"
---
# <a name="resume-method-of-the-win32_printjob-class"></a><span data-ttu-id="ae363-103">Метод Resume \_ класса Win32 PrintJob</span><span class="sxs-lookup"><span data-stu-id="ae363-103">Resume method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="ae363-104">Метод класса **Resume** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) продолжает приостановленное задание печати.</span><span class="sxs-lookup"><span data-stu-id="ae363-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method continues a paused print job.</span></span>

<span data-ttu-id="ae363-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="ae363-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ae363-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ae363-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae363-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae363-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="ae363-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae363-108">Parameters</span></span>

<span data-ttu-id="ae363-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ae363-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae363-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae363-110">Return value</span></span>

<span data-ttu-id="ae363-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="ae363-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ae363-112">**0**</span><span class="sxs-lookup"><span data-stu-id="ae363-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ae363-113">Успешно</span><span class="sxs-lookup"><span data-stu-id="ae363-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="ae363-114">**5**</span><span class="sxs-lookup"><span data-stu-id="ae363-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ae363-115">доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="ae363-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ae363-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="ae363-116">Examples</span></span>

<span data-ttu-id="ae363-117">Следующий пример кода VBScript возобновляет все задания печати на компьютере.</span><span class="sxs-lookup"><span data-stu-id="ae363-117">The following VBScript code sample resumes all the print jobs on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Resume 
Next 
```



## <a name="requirements"></a><span data-ttu-id="ae363-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ae363-118">Requirements</span></span>



| <span data-ttu-id="ae363-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ae363-119">Requirement</span></span> | <span data-ttu-id="ae363-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ae363-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae363-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae363-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ae363-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae363-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="ae363-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae363-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ae363-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae363-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="ae363-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ae363-125">Namespace</span></span><br/>                | <span data-ttu-id="ae363-126">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ae363-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="ae363-127">MOF</span><span class="sxs-lookup"><span data-stu-id="ae363-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae363-128"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae363-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae363-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ae363-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae363-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae363-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ae363-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae363-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae363-132">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="ae363-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ae363-133">**Win32 \_ PrintJob**</span><span class="sxs-lookup"><span data-stu-id="ae363-133">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

