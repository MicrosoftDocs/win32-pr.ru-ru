---
title: Метод Ивмвиртуалпцевентс Онвмстатечанже (Впккоминтерфацес. h)
description: Получает уведомление о том, что состояние виртуальной машины изменилось. | Метод Ивмвиртуалпцевентс Онвмстатечанже (Впккоминтерфацес. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- Метод Онвмстатечанже Virtual PC
- Метод Онвмстатечанже Virtual PC, интерфейс Ивмвиртуалпцевентс
- Ивмвиртуалпцевентс интерфейс Virtual PC, метод Онвмстатечанже
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694007"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a><span data-ttu-id="145a7-107">Метод Ивмвиртуалпцевентс:: Онвмстатечанже</span><span class="sxs-lookup"><span data-stu-id="145a7-107">IVMVirtualPCEvents::OnVMStateChange method</span></span>

<span data-ttu-id="145a7-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="145a7-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="145a7-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="145a7-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="145a7-110">Получает уведомление о том, что состояние виртуальной машины изменилось.</span><span class="sxs-lookup"><span data-stu-id="145a7-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="145a7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="145a7-111">Syntax</span></span>


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="145a7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="145a7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="145a7-113">*виртуалмачинеконфиг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="145a7-113">*virtualMachineConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="145a7-114">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="145a7-114">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="145a7-115">*виртуалмачинестате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="145a7-115">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="145a7-116">Новое состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="145a7-116">The new state of the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="145a7-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="145a7-117">Return value</span></span>

<span data-ttu-id="145a7-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="145a7-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="145a7-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="145a7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="145a7-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="145a7-120">Remarks</span></span>

<span data-ttu-id="145a7-121">Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о событии **вмвиртуалпцевент \_ вмстатечанжед** , исходящем от [**ивмвиртуалпк**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="145a7-121">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_VMStateChanged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span> <span data-ttu-id="145a7-122">Чтобы отслеживать определенную виртуальную машину, используйте метод [**ивмвиртуалмачинивентс:: онстатечанже**](ivmvirtualmachineevents-onstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="145a7-122">To monitor a specific virtual machine, use the [**IVMVirtualMachineEvents::OnStateChange**](ivmvirtualmachineevents-onstatechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="145a7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="145a7-123">Requirements</span></span>



| <span data-ttu-id="145a7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="145a7-124">Requirement</span></span> | <span data-ttu-id="145a7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="145a7-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="145a7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="145a7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="145a7-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="145a7-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="145a7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="145a7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="145a7-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="145a7-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="145a7-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="145a7-130">End of client support</span></span><br/>    | <span data-ttu-id="145a7-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="145a7-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="145a7-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="145a7-132">Product</span></span><br/>                  | <span data-ttu-id="145a7-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="145a7-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="145a7-134">Header</span><span class="sxs-lookup"><span data-stu-id="145a7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="145a7-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="145a7-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="145a7-136">IID</span><span class="sxs-lookup"><span data-stu-id="145a7-136">IID</span></span><br/>                      | <span data-ttu-id="145a7-137">ДИИД \_ ивмвиртуалпцевентс определяется как efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="145a7-137">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="145a7-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="145a7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="145a7-139">**ивмвиртуалпцевентс**</span><span class="sxs-lookup"><span data-stu-id="145a7-139">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

