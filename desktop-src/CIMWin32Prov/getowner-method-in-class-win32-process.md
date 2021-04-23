---
description: '&\# 8194; Метод класса WMI извлекает имя пользователя и доменное имя, под которым выполняется процесс.'
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Метод, являющийся владельцем класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141307"
---
# <a name="getowner-method-of-the-win32_process-class"></a><span data-ttu-id="e766c-103">Метод, являющийся владельцем \_ класса процесса Win32</span><span class="sxs-lookup"><span data-stu-id="e766c-103">GetOwner method of the Win32\_Process class</span></span>

<span data-ttu-id="e766c-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) -владельца получает имя пользователя и доменное имя, под которым выполняется процесс.</span><span class="sxs-lookup"><span data-stu-id="e766c-104">The **GetOwner** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the user name and domain name under which the process is running.</span></span>

<span data-ttu-id="e766c-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="e766c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e766c-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e766c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e766c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e766c-107">Syntax</span></span>


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="e766c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e766c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e766c-109">*Пользователь* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e766c-109">*User* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e766c-110">Возвращает имя пользователя, владеющего этим процессом.</span><span class="sxs-lookup"><span data-stu-id="e766c-110">Returns the user name of the owner of this process.</span></span>

</dd> <dt>

<span data-ttu-id="e766c-111">*Домен* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e766c-111">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e766c-112">Возвращает имя домена, в котором выполняется этот процесс.</span><span class="sxs-lookup"><span data-stu-id="e766c-112">Returns the domain name under which this process is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e766c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e766c-113">Return value</span></span>

<span data-ttu-id="e766c-114">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="e766c-114">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="e766c-115">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="e766c-115">Any other number indicates an error.</span></span> <span data-ttu-id="e766c-116">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e766c-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e766c-117">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e766c-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e766c-118">**Успешное завершение** (0)</span><span class="sxs-lookup"><span data-stu-id="e766c-118">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e766c-119">**Отказано в доступе** (2)</span><span class="sxs-lookup"><span data-stu-id="e766c-119">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e766c-120">**Недостаточно прав доступа** (3)</span><span class="sxs-lookup"><span data-stu-id="e766c-120">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e766c-121">**Неизвестный сбой** (8)</span><span class="sxs-lookup"><span data-stu-id="e766c-121">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e766c-122">**Путь не найден** (9)</span><span class="sxs-lookup"><span data-stu-id="e766c-122">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e766c-123">**Недопустимый параметр** (21)</span><span class="sxs-lookup"><span data-stu-id="e766c-123">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="e766c-124">**Другие** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="e766c-124">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="e766c-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="e766c-125">Examples</span></span>

<span data-ttu-id="e766c-126">[Процесс мониторинга PCT по имени с владельцем](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) Пример на языке VBScript собирает данные об использовании ЦП или процессора и выполняет поиск владельца процесса.</span><span class="sxs-lookup"><span data-stu-id="e766c-126">[The Monitor Process CPU Pct by Name with Owner](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) VBScript sample collects the CPU or Processor utilization percent and looks up the process owner.</span></span>

<span data-ttu-id="e766c-127">На странице [Получение всех серверов, в которые входит список пользователей,](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) в пример запросов PowerShell для владельца всех explorer.exe процессов.</span><span class="sxs-lookup"><span data-stu-id="e766c-127">The [Get all servers that a list of users is logged onto](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) PowerShell sample querys WMI for the owner of all explorer.exe processes.</span></span>

<span data-ttu-id="e766c-128">Следующий пример кода VBScript получает сведения о владельце для каждого выполняющегося процесса.</span><span class="sxs-lookup"><span data-stu-id="e766c-128">The following VBScript code example obtains the owner for each running process.</span></span>


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="e766c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e766c-129">Requirements</span></span>



| <span data-ttu-id="e766c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e766c-130">Requirement</span></span> | <span data-ttu-id="e766c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e766c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e766c-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e766c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e766c-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e766c-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e766c-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e766c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e766c-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e766c-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e766c-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e766c-136">Namespace</span></span><br/>                | <span data-ttu-id="e766c-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e766c-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e766c-138">MOF</span><span class="sxs-lookup"><span data-stu-id="e766c-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e766c-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e766c-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e766c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e766c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e766c-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e766c-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e766c-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e766c-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="e766c-143">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e766c-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e766c-144">**\_Процесс Win32**</span><span class="sxs-lookup"><span data-stu-id="e766c-144">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

