---
title: Перечисление Вмшутдовнактион (Впккоминтерфацес. h)
description: Указывает, как завершить работу виртуальной машины при завершении работы узла или завершении процесса vpc.exe.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- Перечисление Вмшутдовнактион Virtual PC
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b939954042a446f7ad9f128580e804d73e9d29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691832"
---
# <a name="vmshutdownaction-enumeration"></a><span data-ttu-id="8bb9b-104">Перечисление Вмшутдовнактион</span><span class="sxs-lookup"><span data-stu-id="8bb9b-104">VMShutdownAction enumeration</span></span>

<span data-ttu-id="8bb9b-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8bb9b-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8bb9b-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8bb9b-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8bb9b-107">Указывает, как завершить работу виртуальной машины (ВМ) при завершении работы узла или завершении процесса vpc.exe.</span><span class="sxs-lookup"><span data-stu-id="8bb9b-107">Specifies how to shut down a virtual machine (VM) when the host shuts down or the vpc.exe process exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb9b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bb9b-108">Syntax</span></span>


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a><span data-ttu-id="8bb9b-109">Константы</span><span class="sxs-lookup"><span data-stu-id="8bb9b-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8bb9b-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**Вмшутдовнактион \_ сохранить**</span><span class="sxs-lookup"><span data-stu-id="8bb9b-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction\_Save**</span></span>
</dt> <dd>

<span data-ttu-id="8bb9b-111">Сохраните состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8bb9b-111">Save the VM state.</span></span>

</dd> <dt>

<span data-ttu-id="8bb9b-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**Вмшутдовнактион \_ турнофф**</span><span class="sxs-lookup"><span data-stu-id="8bb9b-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction\_TurnOff**</span></span>
</dt> <dd>

<span data-ttu-id="8bb9b-113">Выключите виртуальную машину без отмены дисков.</span><span class="sxs-lookup"><span data-stu-id="8bb9b-113">Turn off the VM without undoing the drives.</span></span>

</dd> <dt>

<span data-ttu-id="8bb9b-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**Вмшутдовнактион \_ Завершение работы**</span><span class="sxs-lookup"><span data-stu-id="8bb9b-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmShutdownAction\_Shutdown**</span></span>
</dt> <dd>

<span data-ttu-id="8bb9b-115">Завершите работу гостевой операционной системы на виртуальной машине, не отменяя диски, если компоненты интеграции доступны и в противном случае сохранит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="8bb9b-115">Shut down the guest operating system on the VM without undoing the drives if the integration components are available and will save the VM otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bb9b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8bb9b-116">Requirements</span></span>



| <span data-ttu-id="8bb9b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8bb9b-117">Requirement</span></span> | <span data-ttu-id="8bb9b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8bb9b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb9b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bb9b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb9b-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8bb9b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8bb9b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bb9b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb9b-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8bb9b-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8bb9b-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8bb9b-123">End of client support</span></span><br/>    | <span data-ttu-id="8bb9b-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8bb9b-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8bb9b-125">Продукт</span><span class="sxs-lookup"><span data-stu-id="8bb9b-125">Product</span></span><br/>                  | <span data-ttu-id="8bb9b-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8bb9b-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8bb9b-127">Header</span><span class="sxs-lookup"><span data-stu-id="8bb9b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb9b-128"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb9b-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb9b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bb9b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb9b-130">Перечисления Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8bb9b-130">Windows Virtual PC Enumerations</span></span>](virtual-pc-enumerations.md)
</dt> <dt>

[<span data-ttu-id="8bb9b-131">**Ивмвиртуалмачине:: Шутдовнактиононкуит**</span><span class="sxs-lookup"><span data-stu-id="8bb9b-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

