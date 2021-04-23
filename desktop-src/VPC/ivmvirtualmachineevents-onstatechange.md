---
title: Метод Ивмвиртуалмачинивентс Онстатечанже (Впккоминтерфацес. h)
description: Получает уведомление о том, что состояние виртуальной машины изменилось. | Метод Ивмвиртуалмачинивентс Онстатечанже (Впккоминтерфацес. h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- Метод Онстатечанже Virtual PC
- Метод Онстатечанже Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Онстатечанже
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da112d8f6211882953056afef0219b9efdf9843
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353822"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a><span data-ttu-id="2a393-107">Метод Ивмвиртуалмачинивентс:: Онстатечанже</span><span class="sxs-lookup"><span data-stu-id="2a393-107">IVMVirtualMachineEvents::OnStateChange method</span></span>

<span data-ttu-id="2a393-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2a393-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2a393-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2a393-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2a393-110">Получает уведомление о том, что состояние виртуальной машины изменилось.</span><span class="sxs-lookup"><span data-stu-id="2a393-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a393-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a393-111">Syntax</span></span>


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="2a393-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a393-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a393-113">*виртуалмачинестате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a393-113">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a393-114">Новое состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a393-114">The new state of the virtual machine.</span></span> <span data-ttu-id="2a393-115">Список значений см. в разделе [**вмвмстате**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="2a393-115">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a393-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a393-116">Return value</span></span>

<span data-ttu-id="2a393-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2a393-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2a393-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2a393-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a393-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a393-119">Remarks</span></span>

<span data-ttu-id="2a393-120">Этот метод вызывается при изменении состояния этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a393-120">This method is called when the state for this virtual machine changes.</span></span> <span data-ttu-id="2a393-121">Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о \_ событии вмвиртуалмачинивент StateChanged, исходящем от [**ивмвиртуалмачине**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="2a393-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_StateChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a393-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2a393-122">Requirements</span></span>



| <span data-ttu-id="2a393-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2a393-123">Requirement</span></span> | <span data-ttu-id="2a393-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2a393-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a393-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a393-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2a393-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2a393-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a393-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a393-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2a393-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2a393-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2a393-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2a393-129">End of client support</span></span><br/>    | <span data-ttu-id="2a393-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2a393-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2a393-131">Продукт</span><span class="sxs-lookup"><span data-stu-id="2a393-131">Product</span></span><br/>                  | <span data-ttu-id="2a393-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2a393-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2a393-133">Header</span><span class="sxs-lookup"><span data-stu-id="2a393-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a393-134"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a393-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2a393-135">IID</span><span class="sxs-lookup"><span data-stu-id="2a393-135">IID</span></span><br/>                      | <span data-ttu-id="2a393-136">ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="2a393-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="2a393-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a393-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a393-138">**ивмвиртуалмачинивентс**</span><span class="sxs-lookup"><span data-stu-id="2a393-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

