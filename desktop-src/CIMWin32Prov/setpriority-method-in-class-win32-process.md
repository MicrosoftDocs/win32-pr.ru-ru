---
description: SetPriority&\# 32; Метод класса WMI пытается изменить приоритет выполнения процесса.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Метод SetPriority класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf08057ec075448d9912e37c33b6087c381f97d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539260"
---
# <a name="setpriority-method-of-the-win32_process-class"></a><span data-ttu-id="66017-103">Метод SetPriority \_ класса процесса Win32</span><span class="sxs-lookup"><span data-stu-id="66017-103">SetPriority method of the Win32\_Process class</span></span>

<span data-ttu-id="66017-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) SetPriority пытается изменить приоритет выполнения процесса.</span><span class="sxs-lookup"><span data-stu-id="66017-104">The **SetPriority** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to change the execution priority of the process.</span></span>

<span data-ttu-id="66017-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="66017-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="66017-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="66017-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="66017-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66017-107">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="66017-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="66017-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66017-109">*Приоритет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66017-109">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66017-110">Новый класс приоритета для процесса.</span><span class="sxs-lookup"><span data-stu-id="66017-110">New priority class for the process.</span></span> <span data-ttu-id="66017-111">Обратите внимание, что эти значения отличаются от значений, явно указанных в свойстве **Priority** [**\_ процесса Win32**](win32-process.md).</span><span class="sxs-lookup"><span data-stu-id="66017-111">Note that these values are different than those explicitly stated in the **Priority** property of [**Win32\_Process**](win32-process.md).</span></span>

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="66017-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Бездействие** (64)</span><span class="sxs-lookup"><span data-stu-id="66017-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="66017-113">Задается для процесса с потоками, которые выполняются только при бездействии системы.</span><span class="sxs-lookup"><span data-stu-id="66017-113">Specified for a process with threads that run only when the system is idle.</span></span> <span data-ttu-id="66017-114">Потоки процесса прерываются потоками процесса, который выполняется в классе с более высоким приоритетом, например экранной заставкой.</span><span class="sxs-lookup"><span data-stu-id="66017-114">The threads of the process are preempted by the threads of a process that run in a higher priority class, for example, a screen saver.</span></span> <span data-ttu-id="66017-115">Класс с приоритетом простоя наследуется дочерними процессами.</span><span class="sxs-lookup"><span data-stu-id="66017-115">The idle-priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="66017-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Ниже среднего** (16384)</span><span class="sxs-lookup"><span data-stu-id="66017-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="66017-117">Обозначает процесс, который имеет приоритет **над \_ \_ классом приоритета простоя**, но ниже **обычного \_ \_ класса приоритета**.</span><span class="sxs-lookup"><span data-stu-id="66017-117">Indicates a process that has priority above **IDLE\_PRIORITY\_CLASS**, but below **NORMAL\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="66017-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** (32)</span><span class="sxs-lookup"><span data-stu-id="66017-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="66017-119">Задается для процесса без особых потребностей в планировании.</span><span class="sxs-lookup"><span data-stu-id="66017-119">Specified for a process with no special scheduling needs.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="66017-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Выше обычного** (32768)</span><span class="sxs-lookup"><span data-stu-id="66017-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="66017-121">Обозначает процесс, который имеет приоритет над **нормальным \_ \_ классом приоритета**, но ниже **класса с высоким \_ приоритетом \_**.</span><span class="sxs-lookup"><span data-stu-id="66017-121">Indicates a process that has priority above **NORMAL\_PRIORITY\_CLASS**, but below **HIGH\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span data-ttu-id="66017-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Высокий приоритет** (128)</span><span class="sxs-lookup"><span data-stu-id="66017-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**High Priority** (128)</span></span>


</dt> <dd>

<span data-ttu-id="66017-123">Задается для процесса, который выполняет критические по времени задачи, которые должны выполняться немедленно.</span><span class="sxs-lookup"><span data-stu-id="66017-123">Specified for a process that performs time-critical tasks that must be executed immediately.</span></span> <span data-ttu-id="66017-124">Потоки процесса выгружают потоки процессов с нормальными или низкими приоритетами.</span><span class="sxs-lookup"><span data-stu-id="66017-124">The threads of the process preempt the threads of normal or idle priority class processes.</span></span> <span data-ttu-id="66017-125">Примером может быть список задач, который должен быстро реагировать при вызове пользователем, независимо от нагрузки на операционную систему.</span><span class="sxs-lookup"><span data-stu-id="66017-125">An example is the Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="66017-126">При использовании класса с высоким приоритетом необходимо соблюдать осторожность, так как приложение класса с высоким приоритетом может использовать почти все доступное время ЦП.</span><span class="sxs-lookup"><span data-stu-id="66017-126">Use extreme care when using the high-priority class, because a high-priority class application can use nearly all of the available CPU time.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="66017-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Реальное** (256)</span><span class="sxs-lookup"><span data-stu-id="66017-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="66017-128">Задается для процесса, имеющего наивысший возможный приоритет.</span><span class="sxs-lookup"><span data-stu-id="66017-128">Specified for a process that has the highest possible priority.</span></span> <span data-ttu-id="66017-129">Потоки процесса выгружают потоки всех других процессов, включая процессы операционной системы, выполняющие важные задачи.</span><span class="sxs-lookup"><span data-stu-id="66017-129">The threads of the process preempt the threads of all of the other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="66017-130">Например, процесс в режиме реального времени, который выполняется в течение более короткого интервала, может привести к тому, что дисковые кэши не будут сбрасываться или мышь не будет отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="66017-130">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush or a mouse to be unresponsive.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66017-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66017-131">Return value</span></span>

<span data-ttu-id="66017-132">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="66017-132">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="66017-133">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="66017-133">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="66017-134">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="66017-134">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="66017-135">**Успешное завершение** (0)</span><span class="sxs-lookup"><span data-stu-id="66017-135">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="66017-136">**Отказано в доступе** (2)</span><span class="sxs-lookup"><span data-stu-id="66017-136">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="66017-137">**Недостаточно прав доступа** (3)</span><span class="sxs-lookup"><span data-stu-id="66017-137">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="66017-138">**Неизвестный сбой** (8)</span><span class="sxs-lookup"><span data-stu-id="66017-138">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="66017-139">**Путь не найден** (9)</span><span class="sxs-lookup"><span data-stu-id="66017-139">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="66017-140">**Недопустимый параметр** (21)</span><span class="sxs-lookup"><span data-stu-id="66017-140">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="66017-141">**Другие** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="66017-141">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="66017-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66017-142">Remarks</span></span>

<span data-ttu-id="66017-143">Чтобы установить приоритет в режиме реального времени, вызывающая сторона  должна иметь **\_ \_ \_ \_ права доступа с базовым приоритетом SeIncreaseBasePriorityPrivilege (SE Inc**).</span><span class="sxs-lookup"><span data-stu-id="66017-143">To set the priority to Realtime, the caller must have **SeIncreaseBasePriorityPrivilege** (**SE\_INC\_BASE\_PRIORITY\_PRIVILEGE**).</span></span> <span data-ttu-id="66017-144">Без этой привилегии наивысший приоритет можно задать с высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="66017-144">Without this privilege, the highest the priority can be set to is High Priority.</span></span>

## <a name="examples"></a><span data-ttu-id="66017-145">Примеры</span><span class="sxs-lookup"><span data-stu-id="66017-145">Examples</span></span>

<span data-ttu-id="66017-146">В примере [изменения приоритета выполняемого процесса](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript изменяется приоритет запущенного экземпляра Notepad.exe с обычного на выше нормального.</span><span class="sxs-lookup"><span data-stu-id="66017-146">The [Modify the Priority Of a Running Process](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript sample changes the priority of a running instance of Notepad.exe from Normal to Above Normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="66017-147">Требования</span><span class="sxs-lookup"><span data-stu-id="66017-147">Requirements</span></span>



| <span data-ttu-id="66017-148">Требование</span><span class="sxs-lookup"><span data-stu-id="66017-148">Requirement</span></span> | <span data-ttu-id="66017-149">Значение</span><span class="sxs-lookup"><span data-stu-id="66017-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66017-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66017-150">Minimum supported client</span></span><br/> | <span data-ttu-id="66017-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66017-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66017-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66017-152">Minimum supported server</span></span><br/> | <span data-ttu-id="66017-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66017-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66017-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="66017-154">Namespace</span></span><br/>                | <span data-ttu-id="66017-155">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="66017-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="66017-156">MOF</span><span class="sxs-lookup"><span data-stu-id="66017-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66017-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66017-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="66017-158">DLL</span><span class="sxs-lookup"><span data-stu-id="66017-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66017-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66017-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66017-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66017-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="66017-161">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="66017-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="66017-162">**\_Процесс Win32**</span><span class="sxs-lookup"><span data-stu-id="66017-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

