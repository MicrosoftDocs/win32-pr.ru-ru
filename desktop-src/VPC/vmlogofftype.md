---
title: Перечисление Вмлогоффтипе (Впккоминтерфацес. h)
description: Указывает, как завершить работу виртуальной машины.
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- Перечисление Вмлогоффтипе Virtual PC
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2311736115390d807058bbfc54c24e7f9e9654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071580"
---
# <a name="vmlogofftype-enumeration"></a><span data-ttu-id="b854f-104">Перечисление Вмлогоффтипе</span><span class="sxs-lookup"><span data-stu-id="b854f-104">VMLogoffType enumeration</span></span>

<span data-ttu-id="b854f-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b854f-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b854f-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b854f-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b854f-107">Указывает, как завершить работу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b854f-107">Specifies how to shut down a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="b854f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b854f-108">Syntax</span></span>


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a><span data-ttu-id="b854f-109">Константы</span><span class="sxs-lookup"><span data-stu-id="b854f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b854f-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**Вмлогофф, \_ Обычная**</span><span class="sxs-lookup"><span data-stu-id="b854f-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="b854f-111">Выход из системы гостевой виртуальной машины был нормальным.</span><span class="sxs-lookup"><span data-stu-id="b854f-111">The logoff in the guest VM was normal.</span></span>

</dd> <dt>

<span data-ttu-id="b854f-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**Вмлогофф \_ принудительно**</span><span class="sxs-lookup"><span data-stu-id="b854f-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff\_Forced**</span></span>
</dt> <dd>

<span data-ttu-id="b854f-113">На гостевой виртуальной машине был принудительно выполнен выход из системы.</span><span class="sxs-lookup"><span data-stu-id="b854f-113">The logoff in the guest VM was forced.</span></span>

</dd> <dt>

<span data-ttu-id="b854f-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**Вмлогофф \_ внешний**</span><span class="sxs-lookup"><span data-stu-id="b854f-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff\_External**</span></span>
</dt> <dd>

<span data-ttu-id="b854f-115">Выход из системы гостевой виртуальной машины выполнен с помощью метода [**ивмгуестос:: logoff**](ivmguestos-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="b854f-115">The logoff in the guest VM was done using the [**IVMGuestOS::Logoff**](ivmguestos-logoff.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b854f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b854f-116">Requirements</span></span>



| <span data-ttu-id="b854f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b854f-117">Requirement</span></span> | <span data-ttu-id="b854f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b854f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b854f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b854f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b854f-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b854f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b854f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b854f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b854f-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b854f-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b854f-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b854f-123">End of client support</span></span><br/>    | <span data-ttu-id="b854f-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b854f-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b854f-125">Продукт</span><span class="sxs-lookup"><span data-stu-id="b854f-125">Product</span></span><br/>                  | <span data-ttu-id="b854f-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b854f-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b854f-127">Header</span><span class="sxs-lookup"><span data-stu-id="b854f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b854f-128"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b854f-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b854f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b854f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b854f-130">**Ивмвиртуалмачине:: Шутдовнактиононкуит**</span><span class="sxs-lookup"><span data-stu-id="b854f-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

