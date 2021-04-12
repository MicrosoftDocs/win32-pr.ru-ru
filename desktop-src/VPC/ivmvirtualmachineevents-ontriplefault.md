---
title: Метод Ивмвиртуалмачинивентс Онтриплефаулт (Впккоминтерфацес. h)
description: Получает уведомление о том, что на виртуальной машине возникла тройная ошибка.
ms.assetid: a17b1a05-3058-48ba-a196-7e9563f3e1c0
keywords:
- Метод Онтриплефаулт Virtual PC
- Метод Онтриплефаулт Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Онтриплефаулт
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnTripleFault
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d635b9009ecadecb7aed4a921a9c609ef69505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534949"
---
# <a name="ivmvirtualmachineeventsontriplefault-method"></a><span data-ttu-id="d455c-106">Метод Ивмвиртуалмачинивентс:: Онтриплефаулт</span><span class="sxs-lookup"><span data-stu-id="d455c-106">IVMVirtualMachineEvents::OnTripleFault method</span></span>

<span data-ttu-id="d455c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d455c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d455c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d455c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d455c-109">Получает уведомление о том, что на виртуальной машине возникла тройная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d455c-109">Receives notification that a virtual machine has triple-faulted.</span></span>

## <a name="syntax"></a><span data-ttu-id="d455c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d455c-110">Syntax</span></span>


```C++
HRESULT OnTripleFault();
```



## <a name="parameters"></a><span data-ttu-id="d455c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d455c-111">Parameters</span></span>

<span data-ttu-id="d455c-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d455c-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d455c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d455c-113">Return value</span></span>

<span data-ttu-id="d455c-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d455c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d455c-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d455c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d455c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d455c-116">Remarks</span></span>

<span data-ttu-id="d455c-117">Этот метод вызывается при тройном сбое виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d455c-117">This method is called when a virtual machine has triple-faulted.</span></span> <span data-ttu-id="d455c-118">Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о \_ событии вмвиртуалмачинивент триплефаулт, исходящем от [**ивмвиртуалмачине**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="d455c-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_TripleFault event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d455c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d455c-119">Requirements</span></span>



| <span data-ttu-id="d455c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d455c-120">Requirement</span></span> | <span data-ttu-id="d455c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d455c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d455c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d455c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d455c-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d455c-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d455c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d455c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d455c-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d455c-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d455c-126">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d455c-126">End of client support</span></span><br/>    | <span data-ttu-id="d455c-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d455c-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d455c-128">Продукт</span><span class="sxs-lookup"><span data-stu-id="d455c-128">Product</span></span><br/>                  | <span data-ttu-id="d455c-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d455c-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d455c-130">Header</span><span class="sxs-lookup"><span data-stu-id="d455c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d455c-131"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d455c-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d455c-132">IID</span><span class="sxs-lookup"><span data-stu-id="d455c-132">IID</span></span><br/>                      | <span data-ttu-id="d455c-133">ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="d455c-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="d455c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d455c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d455c-135">**ивмвиртуалмачинивентс**</span><span class="sxs-lookup"><span data-stu-id="d455c-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

