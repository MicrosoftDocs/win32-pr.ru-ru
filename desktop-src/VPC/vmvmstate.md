---
title: Перечисление Вмвмстате (Впккоминтерфацес. h)
description: Указывает состояние виртуальной машины.
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- Перечисление Вмвмстате Virtual PC
topic_type:
- apiref
api_name:
- VMVMState
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45505e4fb4b444b15697afca4576e889f2da9a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691917"
---
# <a name="vmvmstate-enumeration"></a><span data-ttu-id="e8e55-104">Перечисление Вмвмстате</span><span class="sxs-lookup"><span data-stu-id="e8e55-104">VMVMState enumeration</span></span>

<span data-ttu-id="e8e55-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e8e55-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e8e55-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e8e55-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e8e55-107">Указывает состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e8e55-107">Specifies the state of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e55-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8e55-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVMState_Invalid        = 0,
  vmVMState_TurnedOff      = 1,
  vmVMState_Saved          = 2,
  vmVMState_TurningOn      = 3,
  vmVMState_Restoring      = 4,
  vmVMState_Running        = 5,
  vmVMState_Paused         = 6,
  vmVMState_Saving         = 7,
  vmVMState_TurningOff     = 8,
  vmVMState_MergingDrives  = 9,
  vmVMState_DeleteMachine  = 10
} VMVMState;
```



## <a name="constants"></a><span data-ttu-id="e8e55-109">Константы</span><span class="sxs-lookup"><span data-stu-id="e8e55-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e8e55-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**Вмвмстате является \_ недопустимым**</span><span class="sxs-lookup"><span data-stu-id="e8e55-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-111">Недопустимое состояние (не должно выполняться, если виртуальная машина существует).</span><span class="sxs-lookup"><span data-stu-id="e8e55-111">An invalid state (should not occur if the virtual machine exists).</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**Вмвмстате \_ турнедофф**</span><span class="sxs-lookup"><span data-stu-id="e8e55-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState\_TurnedOff**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-113">Отключено и не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="e8e55-113">Off and not saved.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**Вмвмстате \_ сохранен**</span><span class="sxs-lookup"><span data-stu-id="e8e55-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState\_Saved**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-115">Отключено, но гостевой компьютер сохраняется.</span><span class="sxs-lookup"><span data-stu-id="e8e55-115">Off but the guest is saved.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**Вмвмстате \_ турнингон**</span><span class="sxs-lookup"><span data-stu-id="e8e55-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmVMState\_TurningOn**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-117">В процессе включения.</span><span class="sxs-lookup"><span data-stu-id="e8e55-117">In the process of turning on.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**Вмвмстате \_ восстановление**</span><span class="sxs-lookup"><span data-stu-id="e8e55-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmVMState\_Restoring**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-119">Восстановление состояния.</span><span class="sxs-lookup"><span data-stu-id="e8e55-119">Restoring the state.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**Вмвмстате \_ работает**</span><span class="sxs-lookup"><span data-stu-id="e8e55-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState\_Running**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-121">Работа и не приостановлена.</span><span class="sxs-lookup"><span data-stu-id="e8e55-121">Running and not paused.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**Вмвмстате \_ приостановлена**</span><span class="sxs-lookup"><span data-stu-id="e8e55-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState\_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-123">Запуск и приостановка.</span><span class="sxs-lookup"><span data-stu-id="e8e55-123">Running and paused.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**Вмвмстате \_ Сохранение**</span><span class="sxs-lookup"><span data-stu-id="e8e55-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState\_Saving**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-125">Сохранение состояния.</span><span class="sxs-lookup"><span data-stu-id="e8e55-125">Saving the state.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**Вмвмстате \_ турнингофф**</span><span class="sxs-lookup"><span data-stu-id="e8e55-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState\_TurningOff**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-127">В процессе отключения.</span><span class="sxs-lookup"><span data-stu-id="e8e55-127">In the process of turning off.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**Вмвмстате \_ мергингдривес**</span><span class="sxs-lookup"><span data-stu-id="e8e55-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState\_MergingDrives**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-129">В процессе объединения дисков отмены.</span><span class="sxs-lookup"><span data-stu-id="e8e55-129">In the process of merging undo drives.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**Вмвмстате \_ делетемачине**</span><span class="sxs-lookup"><span data-stu-id="e8e55-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState\_DeleteMachine**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-131">Идет Удаление виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e8e55-131">Deleting the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8e55-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e8e55-132">Requirements</span></span>



| <span data-ttu-id="e8e55-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e8e55-133">Requirement</span></span> | <span data-ttu-id="e8e55-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e8e55-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e55-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8e55-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e55-136">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e8e55-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8e55-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8e55-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e55-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e8e55-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e8e55-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e8e55-139">End of client support</span></span><br/>    | <span data-ttu-id="e8e55-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8e55-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e8e55-141">Продукт</span><span class="sxs-lookup"><span data-stu-id="e8e55-141">Product</span></span><br/>                  | <span data-ttu-id="e8e55-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e8e55-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e8e55-143">Header</span><span class="sxs-lookup"><span data-stu-id="e8e55-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e55-144"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e55-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e55-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8e55-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e55-146">**Ивмвиртуалмачине:: State**</span><span class="sxs-lookup"><span data-stu-id="e8e55-146">**IVMVirtualMachine::State**</span></span>](ivmvirtualmachine-state.md)
</dt> <dt>

[<span data-ttu-id="e8e55-147">**Ивмвиртуалмачинивентс:: Онстатечанже**</span><span class="sxs-lookup"><span data-stu-id="e8e55-147">**IVMVirtualMachineEvents::OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[<span data-ttu-id="e8e55-148">**Ивмвиртуалпцевентс:: Онвмстатечанже**</span><span class="sxs-lookup"><span data-stu-id="e8e55-148">**IVMVirtualPCEvents::OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

