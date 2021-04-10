---
description: Метод Win32ShutdownTracker предоставляет тот же набор параметров завершения работы, что и метод Win32Shutdown в Win32 \_ операционной системы, но он также позволяет указать комментарии, причину завершения работы или время ожидания.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Метод Win32ShutdownTracker класса Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141034"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="cf44f-103">Метод Win32ShutdownTracker \_ класса операционной системы Win32</span><span class="sxs-lookup"><span data-stu-id="cf44f-103">Win32ShutdownTracker method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="cf44f-104">Метод **Win32ShutdownTracker** предоставляет тот же набор параметров завершения работы, что и метод [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) в [**Win32 \_ операционной**](win32-operatingsystem.md)системы, но он также позволяет указать комментарии, причину завершения работы или время ожидания.</span><span class="sxs-lookup"><span data-stu-id="cf44f-104">The **Win32ShutdownTracker** method provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in [**Win32\_OperatingSystem**](win32-operatingsystem.md), but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf44f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf44f-105">Syntax</span></span>


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="cf44f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf44f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf44f-107">*Время ожидания* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf44f-107">*Timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-108">Время в секундах до завершения работы.</span><span class="sxs-lookup"><span data-stu-id="cf44f-108">Time, in seconds, before shutdown takes place.</span></span> <span data-ttu-id="cf44f-109">Значение по умолчанию — 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="cf44f-109">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="cf44f-110">*Комментарий* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf44f-110">*Comment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-111">Сообщение, отображаемое в диалоговом окне завершения работы, которое также хранится в виде комментария в записи журнала событий.</span><span class="sxs-lookup"><span data-stu-id="cf44f-111">Message to display in the shutdown dialog box that is also stored as a comment in the event log entry.</span></span>

</dd> <dt>

<span data-ttu-id="cf44f-112">*Реасонкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf44f-112">*ReasonCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-113">Причина начала завершения работы.</span><span class="sxs-lookup"><span data-stu-id="cf44f-113">Reason for initiating the shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="cf44f-114">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf44f-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-115">Набор флагов битовой панели для выключения компьютера.</span><span class="sxs-lookup"><span data-stu-id="cf44f-115">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="cf44f-116">Чтобы принудительно выполнить команду, добавьте к значению команды флаг force (4).</span><span class="sxs-lookup"><span data-stu-id="cf44f-116">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="cf44f-117">Использование Force в сочетании с завершением работы или перезагрузкой на удаленном компьютере немедленно завершает все (включая WMI, COM и т. д.) или перезагружает удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="cf44f-117">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="cf44f-118">Это приводит к неопределенному возвращаемому значению.</span><span class="sxs-lookup"><span data-stu-id="cf44f-118">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="cf44f-119">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="cf44f-119">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-120">Выход из системы</span><span class="sxs-lookup"><span data-stu-id="cf44f-120">Log Off</span></span>

</dd> <dt>

<span data-ttu-id="cf44f-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="cf44f-121">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-122">Принудительный выход из системы (0 + 4)</span><span class="sxs-lookup"><span data-stu-id="cf44f-122">Forced Log Off (0 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="cf44f-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="cf44f-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-124">Завершить работу</span><span class="sxs-lookup"><span data-stu-id="cf44f-124">Shutdown</span></span>

</dd> <dt>

<span data-ttu-id="cf44f-125">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="cf44f-125">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-126">Принудительное завершение работы (1 + 4)</span><span class="sxs-lookup"><span data-stu-id="cf44f-126">Forced Shutdown (1 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="cf44f-127">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="cf44f-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-128">Перезагрузка</span><span class="sxs-lookup"><span data-stu-id="cf44f-128">Reboot</span></span>

</dd> <dt>

<span data-ttu-id="cf44f-129">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="cf44f-129">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-130">Принудительная перезагрузка (2 + 4)</span><span class="sxs-lookup"><span data-stu-id="cf44f-130">Forced Reboot (2 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="cf44f-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="cf44f-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-132">Выключение питания</span><span class="sxs-lookup"><span data-stu-id="cf44f-132">Power Off</span></span>

</dd> <dt>

<span data-ttu-id="cf44f-133">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="cf44f-133">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="cf44f-134">Принудительное выключение питания (8 + 4)</span><span class="sxs-lookup"><span data-stu-id="cf44f-134">Forced Power Off (8 + 4)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf44f-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf44f-135">Return value</span></span>

<span data-ttu-id="cf44f-136">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="cf44f-136">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="cf44f-137">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="cf44f-137">Any other number indicates an error.</span></span> <span data-ttu-id="cf44f-138">Коды ошибок см. в разделе [**константы WMI Error**](../wmisdk/wmi-error-constants.md) или [**вбемерроренум**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cf44f-138">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cf44f-139">Общие значения **HRESULT** см. в разделе [коды системных ошибок](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cf44f-139">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="cf44f-140">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="cf44f-140">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cf44f-141">**Другое** (1 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="cf44f-141">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cf44f-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf44f-142">Remarks</span></span>

<span data-ttu-id="cf44f-143">Вызывающий процесс должен иметь привилегию **SE \_ Shutdown \_ Name** .</span><span class="sxs-lookup"><span data-stu-id="cf44f-143">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="cf44f-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="cf44f-144">Examples</span></span>

<span data-ttu-id="cf44f-145">В следующем примере кода VBScript описано, как вызвать **Win32ShutdownTracker**.</span><span class="sxs-lookup"><span data-stu-id="cf44f-145">The following VBScript code sample describes how to call **Win32ShutdownTracker**.</span></span>


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
Next
```



## <a name="requirements"></a><span data-ttu-id="cf44f-146">Требования</span><span class="sxs-lookup"><span data-stu-id="cf44f-146">Requirements</span></span>



| <span data-ttu-id="cf44f-147">Требование</span><span class="sxs-lookup"><span data-stu-id="cf44f-147">Requirement</span></span> | <span data-ttu-id="cf44f-148">Значение</span><span class="sxs-lookup"><span data-stu-id="cf44f-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf44f-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf44f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="cf44f-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf44f-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf44f-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf44f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="cf44f-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf44f-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf44f-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cf44f-153">Namespace</span></span><br/>                | <span data-ttu-id="cf44f-154">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cf44f-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf44f-155">MOF</span><span class="sxs-lookup"><span data-stu-id="cf44f-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf44f-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf44f-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf44f-157">DLL</span><span class="sxs-lookup"><span data-stu-id="cf44f-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf44f-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf44f-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf44f-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf44f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf44f-160">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="cf44f-160">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="cf44f-161">**Win32, \_ Операционная система**</span><span class="sxs-lookup"><span data-stu-id="cf44f-161">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="cf44f-162">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="cf44f-162">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
