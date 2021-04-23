---
description: Метод класса Pause WMI приостанавливает задание печати.
ms.assetid: f1e3906f-1ca2-45c0-9863-5762e4e2119a
ms.tgt_platform: multiple
title: Метод Pause класса Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 785ba54b56c65fd298b6ef763ec2d7eca0d8f61a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896517"
---
# <a name="pause-method-of-the-win32_printjob-class"></a><span data-ttu-id="61c92-103">Приостановка метода класса Win32 \_ PrintJob</span><span class="sxs-lookup"><span data-stu-id="61c92-103">Pause method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="61c92-104">Метод класса **Pause** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) приостанавливает задание печати.</span><span class="sxs-lookup"><span data-stu-id="61c92-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method suspends a print job.</span></span>

<span data-ttu-id="61c92-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="61c92-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="61c92-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="61c92-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="61c92-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61c92-107">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="61c92-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="61c92-108">Parameters</span></span>

<span data-ttu-id="61c92-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="61c92-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61c92-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61c92-110">Return value</span></span>

<span data-ttu-id="61c92-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="61c92-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="61c92-112">**0**</span><span class="sxs-lookup"><span data-stu-id="61c92-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="61c92-113">Успешно</span><span class="sxs-lookup"><span data-stu-id="61c92-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="61c92-114">**5**</span><span class="sxs-lookup"><span data-stu-id="61c92-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="61c92-115">доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="61c92-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="61c92-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="61c92-116">Examples</span></span>

<span data-ttu-id="61c92-117">Пример кода " [приостановить все принтеры с пустыми очередями печати](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) " приостанавливает работу всех принтеров, для которых нет ожидающих заданий печати.</span><span class="sxs-lookup"><span data-stu-id="61c92-117">The [Pause All Printers with Empty Print Queues](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) VBScript code sample pauses any printers that have no pending print jobs.</span></span>

<span data-ttu-id="61c92-118">Следующий пример кода VBScript приостанавливает все задания печати на сервере печати.</span><span class="sxs-lookup"><span data-stu-id="61c92-118">The following VBScript code sample pauses all the print jobs on a print server.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Pause 
Next 
```



## <a name="requirements"></a><span data-ttu-id="61c92-119">Требования</span><span class="sxs-lookup"><span data-stu-id="61c92-119">Requirements</span></span>



| <span data-ttu-id="61c92-120">Требование</span><span class="sxs-lookup"><span data-stu-id="61c92-120">Requirement</span></span> | <span data-ttu-id="61c92-121">Значение</span><span class="sxs-lookup"><span data-stu-id="61c92-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="61c92-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61c92-122">Minimum supported client</span></span><br/> | <span data-ttu-id="61c92-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61c92-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="61c92-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61c92-124">Minimum supported server</span></span><br/> | <span data-ttu-id="61c92-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61c92-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="61c92-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="61c92-126">Namespace</span></span><br/>                | <span data-ttu-id="61c92-127">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="61c92-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="61c92-128">MOF</span><span class="sxs-lookup"><span data-stu-id="61c92-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61c92-129"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61c92-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="61c92-130">DLL</span><span class="sxs-lookup"><span data-stu-id="61c92-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61c92-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61c92-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="61c92-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61c92-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61c92-133">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="61c92-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="61c92-134">**Win32 \_ PrintJob**</span><span class="sxs-lookup"><span data-stu-id="61c92-134">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

