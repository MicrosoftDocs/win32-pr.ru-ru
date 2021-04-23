---
title: Интерфейс Ивмвиртуалмачинивентс (Впккоминтерфацес. h)
description: Определяет интерфейс исходящего события для интерфейса Ивмвиртуалмачине.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- Виртуальный ПК с интерфейсом Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2ded96f5a39a520d3b5a712e63fbb0a65d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492561"
---
# <a name="ivmvirtualmachineevents-interface"></a><span data-ttu-id="d6ae9-105">Интерфейс Ивмвиртуалмачинивентс</span><span class="sxs-lookup"><span data-stu-id="d6ae9-105">IVMVirtualMachineEvents interface</span></span>

<span data-ttu-id="d6ae9-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d6ae9-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d6ae9-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d6ae9-108">Определяет интерфейс исходящего события для интерфейса [**ивмвиртуалмачине**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="d6ae9-108">Defines the outgoing event interface for the [**IVMVirtualMachine**](ivmvirtualmachine.md) interface.</span></span> <span data-ttu-id="d6ae9-109">Клиент реализует эти методы для получения событий, отправленных из [**ивмвиртуалмачине**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="d6ae9-109">The client implements these methods to receive events sent from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="members"></a><span data-ttu-id="d6ae9-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="d6ae9-110">Members</span></span>

<span data-ttu-id="d6ae9-111">Интерфейс **ивмвиртуалмачинивентс** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d6ae9-111">The **IVMVirtualMachineEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d6ae9-112">**Ивмвиртуалмачинивентс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d6ae9-112">**IVMVirtualMachineEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="d6ae9-113">Методы</span><span class="sxs-lookup"><span data-stu-id="d6ae9-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d6ae9-114">Методы</span><span class="sxs-lookup"><span data-stu-id="d6ae9-114">Methods</span></span>

<span data-ttu-id="d6ae9-115">Интерфейс **ивмвиртуалмачинивентс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-115">The **IVMVirtualMachineEvents** interface has these methods.</span></span>



| <span data-ttu-id="d6ae9-116">Метод</span><span class="sxs-lookup"><span data-stu-id="d6ae9-116">Method</span></span>                                                                                   | <span data-ttu-id="d6ae9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d6ae9-117">Description</span></span>                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6ae9-118">**онаддитионсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-118">**OnAdditionsAvailable**</span></span>](ivmvirtualmachineevents-onadditionsavailable.md)             | <span data-ttu-id="d6ae9-119">Получает уведомление о том, что компоненты интеграции доступны на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-119">Receives notification that integration components are available in a virtual machine.</span></span><br/>                                                |
| [<span data-ttu-id="d6ae9-120">**онаддитионсунинсталлед**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-120">**OnAdditionsUninstalled**</span></span>](ivmvirtualmachineevents-onadditionsuninstalled.md)         | <span data-ttu-id="d6ae9-121">Получает уведомление об удалении компонентов интеграции на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-121">Receives notification that integration components are uninstalled in a virtual machine.</span></span><br/>                                              |
| [<span data-ttu-id="d6ae9-122">**онконфигуратиончанжед**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-122">**OnConfigurationChanged**</span></span>](ivmvirtualmachineevents-onconfigurationchanged.md)         | <span data-ttu-id="d6ae9-123">Получает уведомление о том, что значение в конфигурации этой виртуальной машины изменилось.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-123">Receives notification that a value in the configuration for this virtual machine has changed.</span></span><br/>                                        |
| [<span data-ttu-id="d6ae9-124">**ондискаутофспаце**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-124">**OnDiskOutOfSpace**</span></span>](ivmvirtualmachineevents-ondiskoutofspace.md)                     | <span data-ttu-id="d6ae9-125">Получает уведомление о том, что на диске, требуемом для виртуальной машины, недостаточно места, а виртуальная машина не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-125">Receives notification that a disk required for a virtual machine is out of space and the virtual machine is unable to run.</span></span><br/>           |
| [<span data-ttu-id="d6ae9-126">**оненханцедвидеомодечанжед**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-126">**OnEnhancedVideoModeChanged**</span></span>](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | <span data-ttu-id="d6ae9-127">Получает уведомление о том, что изменилась поддержка виртуальной машины для расширенного видеорежима.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-127">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span><br/>                                          |
| [<span data-ttu-id="d6ae9-128">**онгуестлогофф**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-128">**OnGuestLogoff**</span></span>](ivmvirtualmachineevents-onguestlogoff.md)                           | <span data-ttu-id="d6ae9-129">Получает уведомление о том, что пользователь вышел из операционной системы на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-129">Receives notification that a user has logged off from the guest operating system.</span></span><br/>                                                    |
| [<span data-ttu-id="d6ae9-130">**онгуестшутдовн**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-130">**OnGuestShutdown**</span></span>](ivmvirtualmachineevents-onguestshutdown.md)                       | <span data-ttu-id="d6ae9-131">Получает уведомление о завершении работы гостевой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-131">Receives notification that guest operating system has shut down.</span></span><br/>                                                                     |
| [<span data-ttu-id="d6ae9-132">**онхеартбеатстоппед**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-132">**OnHeartbeatStopped**</span></span>](ivmvirtualmachineevents-onheartbeatstopped.md)                 | <span data-ttu-id="d6ae9-133">Получает уведомление о том, что пульс виртуальной машины остановлен.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-133">Receives notification that a virtual machine's heartbeat has stopped.</span></span> <span data-ttu-id="d6ae9-134">Обычно это свидетельствует о сбое операционной системы на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-134">This usually indicates the guest operating system has crashed.</span></span><br/> |
| [<span data-ttu-id="d6ae9-135">**онрекуестшутдовн**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-135">**OnRequestShutdown**</span></span>](ivmvirtualmachineevents-onrequestshutdown.md)                   | <span data-ttu-id="d6ae9-136">Получает уведомление о том, что был выполнен запрос на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-136">Receives notification that a shutdown request has been made.</span></span><br/>                                                                         |
| [<span data-ttu-id="d6ae9-137">**OnReset**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-137">**OnReset**</span></span>](ivmvirtualmachineevents-onreset.md)                                       | <span data-ttu-id="d6ae9-138">Получает уведомление о том, что виртуальная машина сброшена.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-138">Receives notification that a virtual machine has been reset.</span></span><br/>                                                                         |
| [<span data-ttu-id="d6ae9-139">**онстатечанже**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-139">**OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)                           | <span data-ttu-id="d6ae9-140">Получает уведомление о том, что состояние виртуальной машины изменилось.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-140">Receives notification that a virtual machine's state has changed.</span></span><br/>                                                                    |
| [<span data-ttu-id="d6ae9-141">**онтриплефаулт**</span><span class="sxs-lookup"><span data-stu-id="d6ae9-141">**OnTripleFault**</span></span>](ivmvirtualmachineevents-ontriplefault.md)                           | <span data-ttu-id="d6ae9-142">Получает уведомление о том, что на виртуальной машине возникла тройная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d6ae9-142">Receives notification that a virtual machine has triple-faulted.</span></span><br/>                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="d6ae9-143">Требования</span><span class="sxs-lookup"><span data-stu-id="d6ae9-143">Requirements</span></span>



| <span data-ttu-id="d6ae9-144">Требование</span><span class="sxs-lookup"><span data-stu-id="d6ae9-144">Requirement</span></span> | <span data-ttu-id="d6ae9-145">Значение</span><span class="sxs-lookup"><span data-stu-id="d6ae9-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ae9-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6ae9-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d6ae9-147">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d6ae9-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d6ae9-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6ae9-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d6ae9-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d6ae9-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d6ae9-150">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d6ae9-150">End of client support</span></span><br/>    | <span data-ttu-id="d6ae9-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d6ae9-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d6ae9-152">Продукт</span><span class="sxs-lookup"><span data-stu-id="d6ae9-152">Product</span></span><br/>                  | <span data-ttu-id="d6ae9-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d6ae9-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d6ae9-154">Header</span><span class="sxs-lookup"><span data-stu-id="d6ae9-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6ae9-155"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6ae9-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d6ae9-156">IID</span><span class="sxs-lookup"><span data-stu-id="d6ae9-156">IID</span></span><br/>                      | <span data-ttu-id="d6ae9-157">ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="d6ae9-157">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



 

