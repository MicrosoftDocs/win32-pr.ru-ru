---
title: Перечисление Вмвиртуалмачинивентс (Впккоминтерфацес. h)
description: Указывает события виртуальной машины.
ms.assetid: 158bdada-6fd3-488c-9ff1-e04df9a79127
keywords:
- Перечисление Вмвиртуалмачинивентс Virtual PC
topic_type:
- apiref
api_name:
- VMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1e1d8f4d89c28f63886444537fb9d894fc42e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071922"
---
# <a name="vmvirtualmachineevents-enumeration"></a><span data-ttu-id="44319-104">Перечисление Вмвиртуалмачинивентс</span><span class="sxs-lookup"><span data-stu-id="44319-104">VMVirtualMachineEvents enumeration</span></span>

<span data-ttu-id="44319-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="44319-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="44319-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="44319-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="44319-107">Указывает события виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="44319-107">Specifies the virtual machine (VM) events.</span></span>

## <a name="syntax"></a><span data-ttu-id="44319-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44319-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualMachineEvent_StateChanged              = 1,
  vmVirtualMachineEvent_RequestShutdown           = 2,
  vmVirtualMachineEvent_Reset                     = 3,
  vmVirtualMachineEvent_TripleFault               = 4,
  vmVirtualMachineEvent_HeartbeatStopped          = 5,
  vmVirtualMachineEvent_ConfigurationChanged      = 6,
  vmVirtualMachineEvent_EnhancedVideoModeChanged  = 7,
  vmVirtualMachineEvent_AdditionsUninstalled      = 8,
  vmVirtualMachineEvent_AdditionsAvailable        = 9,
  vmVirtualMachineEvent_GuestShutdown             = 10,
  vmVirtualMachineEvent_GuestLogoff               = 11,
  vmVirtualMachineEvent_DiskOutOfSpace            = 12
} VMVirtualMachineEvents;
```



## <a name="constants"></a><span data-ttu-id="44319-109">Константы</span><span class="sxs-lookup"><span data-stu-id="44319-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="44319-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**Вмвиртуалмачинивент \_ StateChanged**</span><span class="sxs-lookup"><span data-stu-id="44319-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent\_StateChanged**</span></span>
</dt> <dd>

<span data-ttu-id="44319-111">Состояние виртуальной машины изменилось.</span><span class="sxs-lookup"><span data-stu-id="44319-111">A VM's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="44319-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**Вмвиртуалмачинивент \_ рекуестшутдовн**</span><span class="sxs-lookup"><span data-stu-id="44319-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_RequestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="44319-113">Запрошено завершение работы.</span><span class="sxs-lookup"><span data-stu-id="44319-113">A shutdown has been requested.</span></span>

</dd> <dt>

<span data-ttu-id="44319-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**\_Сброс вмвиртуалмачинивент**</span><span class="sxs-lookup"><span data-stu-id="44319-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**vmVirtualMachineEvent\_Reset**</span></span>
</dt> <dd>

<span data-ttu-id="44319-115">Виртуальная машина сброшена.</span><span class="sxs-lookup"><span data-stu-id="44319-115">A VM has been reset.</span></span>

</dd> <dt>

<span data-ttu-id="44319-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**Вмвиртуалмачинивент \_ триплефаулт**</span><span class="sxs-lookup"><span data-stu-id="44319-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent\_TripleFault**</span></span>
</dt> <dd>

<span data-ttu-id="44319-117">На виртуальной машине возникла тройная ошибка.</span><span class="sxs-lookup"><span data-stu-id="44319-117">A VM has triple-faulted.</span></span>

</dd> <dt>

<span data-ttu-id="44319-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**Вмвиртуалмачинивент \_ хеартбеатстоппед**</span><span class="sxs-lookup"><span data-stu-id="44319-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent\_HeartbeatStopped**</span></span>
</dt> <dd>

<span data-ttu-id="44319-119">Пульс виртуальной машины остановлен.</span><span class="sxs-lookup"><span data-stu-id="44319-119">A VM's heartbeat has stopped.</span></span> <span data-ttu-id="44319-120">Обычно это означает, что произошел сбой гостевой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="44319-120">This usually indicates that the guest operating system has crashed.</span></span>

</dd> <dt>

<span data-ttu-id="44319-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**Вмвиртуалмачинивент \_ конфигуратиончанжед**</span><span class="sxs-lookup"><span data-stu-id="44319-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmVirtualMachineEvent\_ConfigurationChanged**</span></span>
</dt> <dd>

<span data-ttu-id="44319-122">Значение в конфигурации для этой виртуальной машины изменилось</span><span class="sxs-lookup"><span data-stu-id="44319-122">A value in the configuration for this VM has changed</span></span>

</dd> <dt>

<span data-ttu-id="44319-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**Вмвиртуалмачинивент \_ енханцедвидеомодечанжед**</span><span class="sxs-lookup"><span data-stu-id="44319-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent\_EnhancedVideoModeChanged**</span></span>
</dt> <dd>

<span data-ttu-id="44319-124">Изменился режим видео виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="44319-124">A VM's video mode has changed.</span></span>

</dd> <dt>

<span data-ttu-id="44319-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**Вмвиртуалмачинивент \_ аддитионсунинсталлед**</span><span class="sxs-lookup"><span data-stu-id="44319-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent\_AdditionsUninstalled**</span></span>
</dt> <dd>

<span data-ttu-id="44319-126">Компоненты интеграции были удалены с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="44319-126">Integration components have been uninstalled from the VM.</span></span>

</dd> <dt>

<span data-ttu-id="44319-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**Вмвиртуалмачинивент \_ аддитионсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="44319-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent\_AdditionsAvailable**</span></span>
</dt> <dd>

<span data-ttu-id="44319-128">Интеграция доступна в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="44319-128">Integration are available in the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="44319-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**Вмвиртуалмачинивент \_ гуестшутдовн**</span><span class="sxs-lookup"><span data-stu-id="44319-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_GuestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="44319-130">Работа гостевой операционной системы завершается.</span><span class="sxs-lookup"><span data-stu-id="44319-130">A guest operating system is shutting down.</span></span>

</dd> <dt>

<span data-ttu-id="44319-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**Вмвиртуалмачинивент \_ гуестлогофф**</span><span class="sxs-lookup"><span data-stu-id="44319-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent\_GuestLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="44319-132">Пользователь вышел из операционной системы на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="44319-132">A user logged off from the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="44319-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**Вмвиртуалмачинивент \_ дискаутофспаце**</span><span class="sxs-lookup"><span data-stu-id="44319-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent\_DiskOutOfSpace**</span></span>
</dt> <dd>

<span data-ttu-id="44319-134">Недостаточно места на диске, требуемом для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="44319-134">A disk required by the VM is low on space.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44319-135">Требования</span><span class="sxs-lookup"><span data-stu-id="44319-135">Requirements</span></span>



| <span data-ttu-id="44319-136">Требование</span><span class="sxs-lookup"><span data-stu-id="44319-136">Requirement</span></span> | <span data-ttu-id="44319-137">Значение</span><span class="sxs-lookup"><span data-stu-id="44319-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="44319-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44319-138">Minimum supported client</span></span><br/> | <span data-ttu-id="44319-139">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="44319-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44319-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44319-140">Minimum supported server</span></span><br/> | <span data-ttu-id="44319-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="44319-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="44319-142">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="44319-142">End of client support</span></span><br/>    | <span data-ttu-id="44319-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="44319-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="44319-144">Продукт</span><span class="sxs-lookup"><span data-stu-id="44319-144">Product</span></span><br/>                  | <span data-ttu-id="44319-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="44319-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="44319-146">Header</span><span class="sxs-lookup"><span data-stu-id="44319-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="44319-147"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="44319-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44319-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44319-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44319-149">**ивмвиртуалмачинивентс**</span><span class="sxs-lookup"><span data-stu-id="44319-149">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

