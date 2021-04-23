---
title: Интерфейс Ивмтаск (Впккоминтерфацес. h)
description: Используйте интерфейс Ивмтаск для мониторинга и управления асинхронными задачами для различных методов COM.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- Виртуальный ПК с интерфейсом Ивмтаск
- Ивмтаск интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534769"
---
# <a name="ivmtask-interface"></a><span data-ttu-id="85de8-105">Интерфейс Ивмтаск</span><span class="sxs-lookup"><span data-stu-id="85de8-105">IVMTask interface</span></span>

<span data-ttu-id="85de8-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="85de8-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="85de8-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="85de8-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="85de8-108">Используйте интерфейс **ивмтаск** для мониторинга и управления асинхронными задачами для различных методов COM.</span><span class="sxs-lookup"><span data-stu-id="85de8-108">Use the **IVMTask** interface to monitor and control asynchronous tasks for various COM methods.</span></span>

## <a name="members"></a><span data-ttu-id="85de8-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="85de8-109">Members</span></span>

<span data-ttu-id="85de8-110">Интерфейс **ивмтаск** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="85de8-110">The **IVMTask** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="85de8-111">**Ивмтаск** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="85de8-111">**IVMTask** also has these types of members:</span></span>

-   [<span data-ttu-id="85de8-112">Методы</span><span class="sxs-lookup"><span data-stu-id="85de8-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="85de8-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="85de8-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="85de8-114">Методы</span><span class="sxs-lookup"><span data-stu-id="85de8-114">Methods</span></span>

<span data-ttu-id="85de8-115">Интерфейс **ивмтаск** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="85de8-115">The **IVMTask** interface has these methods.</span></span>



| <span data-ttu-id="85de8-116">Метод</span><span class="sxs-lookup"><span data-stu-id="85de8-116">Method</span></span>                                                 | <span data-ttu-id="85de8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="85de8-117">Description</span></span>                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85de8-118">**Отменить**</span><span class="sxs-lookup"><span data-stu-id="85de8-118">**Cancel**</span></span>](ivmtask-cancel.md)                       | <span data-ttu-id="85de8-119">Отменяет задачу.</span><span class="sxs-lookup"><span data-stu-id="85de8-119">Cancels the task.</span></span><br/>                                                                |
| [<span data-ttu-id="85de8-120">**ваитфоркомплетион**</span><span class="sxs-lookup"><span data-stu-id="85de8-120">**WaitForCompletion**</span></span>](ivmtask-waitforcompletion.md) | <span data-ttu-id="85de8-121">Ожидает завершения задачи или до истечения указанного интервала времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="85de8-121">Waits for the task to complete or for the specified time-out interval to elapse.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="85de8-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="85de8-122">Properties</span></span>

<span data-ttu-id="85de8-123">Интерфейс **ивмтаск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="85de8-123">The **IVMTask** interface has these properties.</span></span>



| <span data-ttu-id="85de8-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="85de8-124">Property</span></span>                                                        | <span data-ttu-id="85de8-125">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="85de8-125">Access type</span></span>          | <span data-ttu-id="85de8-126">Описание</span><span class="sxs-lookup"><span data-stu-id="85de8-126">Description</span></span>                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="85de8-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="85de8-127">**Description**</span></span>](ivmtask-description.md)<br/>           | <span data-ttu-id="85de8-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="85de8-128">Read-only</span></span><br/> | <span data-ttu-id="85de8-129">Описание задачи.</span><span class="sxs-lookup"><span data-stu-id="85de8-129">A description of the task.</span></span><br/>                              |
| [<span data-ttu-id="85de8-130">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="85de8-130">**Error**</span></span>](ivmtask-error.md)<br/>                       | <span data-ttu-id="85de8-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="85de8-131">Read-only</span></span><br/> | <span data-ttu-id="85de8-132">Ошибка, записанная для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="85de8-132">The error recorded for this task.</span></span><br/>                       |
| [<span data-ttu-id="85de8-133">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="85de8-133">**ErrorDescription**</span></span>](ivmtask-errordescription.md)<br/> | <span data-ttu-id="85de8-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="85de8-134">Read-only</span></span><br/> | <span data-ttu-id="85de8-135">Локализованное описание ошибки, записанное для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="85de8-135">The localized error description recorded for this task.</span></span><br/> |
| [<span data-ttu-id="85de8-136">**ID**</span><span class="sxs-lookup"><span data-stu-id="85de8-136">**ID**</span></span>](ivmtask-id.md)<br/>                             | <span data-ttu-id="85de8-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="85de8-137">Read-only</span></span><br/> | <span data-ttu-id="85de8-138">Уникальный идентификатор для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="85de8-138">A unique identifier for this task.</span></span><br/>                      |
| [<span data-ttu-id="85de8-139">**Доменять**</span><span class="sxs-lookup"><span data-stu-id="85de8-139">**IsCancelable**</span></span>](ivmtask-iscancelable.md)<br/>         | <span data-ttu-id="85de8-140">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="85de8-140">Read-only</span></span><br/> | <span data-ttu-id="85de8-141">Указывает, может ли задача быть отменена.</span><span class="sxs-lookup"><span data-stu-id="85de8-141">Indicates whether the task can be canceled.</span></span><br/>             |
| [<span data-ttu-id="85de8-142">**IsComplete**</span><span class="sxs-lookup"><span data-stu-id="85de8-142">**IsComplete**</span></span>](ivmtask-iscomplete.md)<br/>             | <span data-ttu-id="85de8-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="85de8-143">Read-only</span></span><br/> | <span data-ttu-id="85de8-144">Указывает, завершена ли задача.</span><span class="sxs-lookup"><span data-stu-id="85de8-144">Indicates whether the task has completed.</span></span><br/>               |
| [<span data-ttu-id="85de8-145">**перценткомплетед**</span><span class="sxs-lookup"><span data-stu-id="85de8-145">**PercentCompleted**</span></span>](ivmtask-percentcompleted.md)<br/> | <span data-ttu-id="85de8-146">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="85de8-146">Read-only</span></span><br/> | <span data-ttu-id="85de8-147">Процент завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="85de8-147">The completion percentage of the task.</span></span><br/>                  |
| [<span data-ttu-id="85de8-148">**Результат**</span><span class="sxs-lookup"><span data-stu-id="85de8-148">**Result**</span></span>](ivmtask-result.md)<br/>                     | <span data-ttu-id="85de8-149">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="85de8-149">Read-only</span></span><br/> | <span data-ttu-id="85de8-150">Результат задачи.</span><span class="sxs-lookup"><span data-stu-id="85de8-150">The result of the task.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="85de8-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85de8-151">Remarks</span></span>

<span data-ttu-id="85de8-152">Объект **ивмтаск** возвращается методами, которые могут потребовать значительного времени на выполнение.</span><span class="sxs-lookup"><span data-stu-id="85de8-152">An **IVMTask** object is returned by methods that could potentially require a significant amount of time to complete.</span></span> <span data-ttu-id="85de8-153">Это позволяет приложению отслеживать ход выполнения требуемой операции без принудительной блокировки дальнейших операций, ожидая завершения операции.</span><span class="sxs-lookup"><span data-stu-id="85de8-153">This allows the application to monitor the progress of the desired operation without forcing it to block further execution while waiting for the completion of the operation.</span></span>

<span data-ttu-id="85de8-154">Следующие методы возвращают объект **ивмтаск** , который можно использовать для отслеживания хода выполнения:</span><span class="sxs-lookup"><span data-stu-id="85de8-154">The following methods return an **IVMTask** object that can be used to track progress:</span></span>

-   [<span data-ttu-id="85de8-155">**Ивмгуестос:: выход из системы**</span><span class="sxs-lookup"><span data-stu-id="85de8-155">**IVMGuestOS::Logoff**</span></span>](ivmguestos-logoff.md)
-   [<span data-ttu-id="85de8-156">**Ивмгуестос:: Restart**</span><span class="sxs-lookup"><span data-stu-id="85de8-156">**IVMGuestOS::Restart**</span></span>](ivmguestos-restart.md)
-   [<span data-ttu-id="85de8-157">**Ивмгуестос:: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="85de8-157">**IVMGuestOS::Shutdown**</span></span>](ivmguestos-shutdown.md)
-   [<span data-ttu-id="85de8-158">**Ивмхарддиск:: Compact**</span><span class="sxs-lookup"><span data-stu-id="85de8-158">**IVMHardDisk::Compact**</span></span>](ivmharddisk-compact.md)
-   [<span data-ttu-id="85de8-159">**Ивмхарддиск:: Convert**</span><span class="sxs-lookup"><span data-stu-id="85de8-159">**IVMHardDisk::Convert**</span></span>](ivmharddisk-convert.md)
-   [<span data-ttu-id="85de8-160">**Ивмхарддиск:: Merge**</span><span class="sxs-lookup"><span data-stu-id="85de8-160">**IVMHardDisk::Merge**</span></span>](ivmharddisk-merge.md)
-   [<span data-ttu-id="85de8-161">**Ивмхарддиск:: Мержето**</span><span class="sxs-lookup"><span data-stu-id="85de8-161">**IVMHardDisk::MergeTo**</span></span>](ivmharddisk-mergeto.md)
-   [<span data-ttu-id="85de8-162">**Ивмвиртуалмачине:: Мержеундодискс**</span><span class="sxs-lookup"><span data-stu-id="85de8-162">**IVMVirtualMachine::MergeUndoDisks**</span></span>](ivmvirtualmachine-mergeundodisks.md)
-   [<span data-ttu-id="85de8-163">**Ивмвиртуалмачине:: Reset**</span><span class="sxs-lookup"><span data-stu-id="85de8-163">**IVMVirtualMachine::Reset**</span></span>](ivmvirtualmachine-reset.md)
-   [<span data-ttu-id="85de8-164">**Ивмвиртуалмачине:: Save**</span><span class="sxs-lookup"><span data-stu-id="85de8-164">**IVMVirtualMachine::Save**</span></span>](ivmvirtualmachine-save.md)
-   [<span data-ttu-id="85de8-165">**Ивмвиртуалмачине:: Startup**</span><span class="sxs-lookup"><span data-stu-id="85de8-165">**IVMVirtualMachine::Startup**</span></span>](ivmvirtualmachine-startup.md)
-   [<span data-ttu-id="85de8-166">**Ивмвиртуалмачине:: Startup2**</span><span class="sxs-lookup"><span data-stu-id="85de8-166">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
-   [<span data-ttu-id="85de8-167">**Ивмвиртуалмачине:: Турнофф**</span><span class="sxs-lookup"><span data-stu-id="85de8-167">**IVMVirtualMachine::TurnOff**</span></span>](ivmvirtualmachine-turnoff.md)
-   [<span data-ttu-id="85de8-168">**Ивмвиртуалпк:: КреатедифференЦингвиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="85de8-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span></span>](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [<span data-ttu-id="85de8-169">**Ивмвиртуалпк:: Креатединамиквиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="85de8-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span></span>](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [<span data-ttu-id="85de8-170">**Ивмвиртуалпк:: Креатефикседвиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="85de8-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span></span>](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a><span data-ttu-id="85de8-171">Требования</span><span class="sxs-lookup"><span data-stu-id="85de8-171">Requirements</span></span>



| <span data-ttu-id="85de8-172">Требование</span><span class="sxs-lookup"><span data-stu-id="85de8-172">Requirement</span></span> | <span data-ttu-id="85de8-173">Значение</span><span class="sxs-lookup"><span data-stu-id="85de8-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="85de8-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85de8-174">Minimum supported client</span></span><br/> | <span data-ttu-id="85de8-175">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="85de8-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85de8-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85de8-176">Minimum supported server</span></span><br/> | <span data-ttu-id="85de8-177">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="85de8-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="85de8-178">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="85de8-178">End of client support</span></span><br/>    | <span data-ttu-id="85de8-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="85de8-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="85de8-180">Продукт</span><span class="sxs-lookup"><span data-stu-id="85de8-180">Product</span></span><br/>                  | <span data-ttu-id="85de8-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="85de8-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="85de8-182">Header</span><span class="sxs-lookup"><span data-stu-id="85de8-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="85de8-183"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="85de8-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="85de8-184">IID</span><span class="sxs-lookup"><span data-stu-id="85de8-184">IID</span></span><br/>                      | <span data-ttu-id="85de8-185">IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="85de8-185">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



 

