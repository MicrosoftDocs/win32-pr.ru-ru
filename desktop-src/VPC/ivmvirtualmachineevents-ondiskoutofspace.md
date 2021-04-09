---
title: Метод Ивмвиртуалмачинивентс Ондискаутофспаце (Впккоминтерфацес. h)
description: Получает уведомление о том, что на диске, требуемом для виртуальной машины, недостаточно свободного места.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- Метод Ондискаутофспаце Virtual PC
- Метод Ондискаутофспаце Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Ондискаутофспаце
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891386"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a><span data-ttu-id="ba248-106">Метод Ивмвиртуалмачинивентс:: Ондискаутофспаце</span><span class="sxs-lookup"><span data-stu-id="ba248-106">IVMVirtualMachineEvents::OnDiskOutOfSpace method</span></span>

<span data-ttu-id="ba248-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ba248-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ba248-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ba248-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ba248-109">Получает уведомление о недостатке свободного места на диске, требуемом для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ba248-109">Receives notification that a disk required for a virtual machine (VM) is low on free space.</span></span> <span data-ttu-id="ba248-110">Если свободное пространство становится меньше 100 МБ, это событие получается как предупреждение, и если свободное пространство становится меньше 20 МБ, это событие снова принимается как ошибка, и виртуальная машина будет приостановлена.</span><span class="sxs-lookup"><span data-stu-id="ba248-110">If free space drops below 100 MB this event is received as a warning and if free space drops below 20 MB this event is received again as an error and the VM will be paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba248-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba248-111">Syntax</span></span>


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a><span data-ttu-id="ba248-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba248-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba248-113">*критикаллилов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba248-113">*criticallyLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba248-114">Задайте значение **\_ true** , если объем свободного места на диске меньше 20 МБ, а значение — **\_ false** , если размер свободного пространства превышает 20 МБ, но менее 100 МБ.</span><span class="sxs-lookup"><span data-stu-id="ba248-114">Set to **VARIANT\_TRUE** if the disk has less than 20 MB free and to **VARIANT\_FALSE** if the free space is more than 20 MB but less than 100 MB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba248-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba248-115">Return value</span></span>

<span data-ttu-id="ba248-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ba248-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba248-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ba248-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba248-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ba248-118">Requirements</span></span>



| <span data-ttu-id="ba248-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ba248-119">Requirement</span></span> | <span data-ttu-id="ba248-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ba248-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba248-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba248-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ba248-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ba248-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba248-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba248-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ba248-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ba248-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ba248-125">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ba248-125">End of client support</span></span><br/>    | <span data-ttu-id="ba248-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ba248-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ba248-127">Продукт</span><span class="sxs-lookup"><span data-stu-id="ba248-127">Product</span></span><br/>                  | <span data-ttu-id="ba248-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ba248-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ba248-129">Header</span><span class="sxs-lookup"><span data-stu-id="ba248-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba248-130"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba248-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ba248-131">IID</span><span class="sxs-lookup"><span data-stu-id="ba248-131">IID</span></span><br/>                      | <span data-ttu-id="ba248-132">ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="ba248-132">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="ba248-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba248-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba248-134">**ивмвиртуалмачинивентс**</span><span class="sxs-lookup"><span data-stu-id="ba248-134">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

