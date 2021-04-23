---
title: Метод OnReset Ивмвиртуалмачинивентс (Впккоминтерфацес. h)
description: Получает уведомление о том, что виртуальная машина сброшена.
ms.assetid: 10a66aea-9a8f-4663-8eb6-cc35f361e43f
keywords:
- Виртуальный ПК с методом OnReset
- Виртуальный ПК с методом OnReset, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод OnReset
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnReset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6345d0e925777fbecf42247b3e3064b9f993c7c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988154"
---
# <a name="ivmvirtualmachineeventsonreset-method"></a><span data-ttu-id="85ecd-106">Метод Ивмвиртуалмачинивентс:: OnReset</span><span class="sxs-lookup"><span data-stu-id="85ecd-106">IVMVirtualMachineEvents::OnReset method</span></span>

<span data-ttu-id="85ecd-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="85ecd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="85ecd-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="85ecd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="85ecd-109">Получает уведомление о том, что виртуальная машина сброшена.</span><span class="sxs-lookup"><span data-stu-id="85ecd-109">Receives notification that a virtual machine has been reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="85ecd-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85ecd-110">Syntax</span></span>


```C++
HRESULT OnReset();
```



## <a name="parameters"></a><span data-ttu-id="85ecd-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="85ecd-111">Parameters</span></span>

<span data-ttu-id="85ecd-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="85ecd-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85ecd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85ecd-113">Return value</span></span>

<span data-ttu-id="85ecd-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="85ecd-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85ecd-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85ecd-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="85ecd-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85ecd-116">Remarks</span></span>

<span data-ttu-id="85ecd-117">Этот метод вызывается при сбросе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="85ecd-117">This method is called when the virtual machine has been reset.</span></span> <span data-ttu-id="85ecd-118">Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о \_ событии сброса вмвиртуалмачинивент, исходящем от [**ивмвиртуалмачине**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="85ecd-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_Reset event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85ecd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="85ecd-119">Requirements</span></span>



| <span data-ttu-id="85ecd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="85ecd-120">Requirement</span></span> | <span data-ttu-id="85ecd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="85ecd-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="85ecd-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85ecd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="85ecd-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="85ecd-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85ecd-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85ecd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="85ecd-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="85ecd-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="85ecd-126">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="85ecd-126">End of client support</span></span><br/>    | <span data-ttu-id="85ecd-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="85ecd-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="85ecd-128">Продукт</span><span class="sxs-lookup"><span data-stu-id="85ecd-128">Product</span></span><br/>                  | <span data-ttu-id="85ecd-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="85ecd-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="85ecd-130">Header</span><span class="sxs-lookup"><span data-stu-id="85ecd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="85ecd-131"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="85ecd-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="85ecd-132">IID</span><span class="sxs-lookup"><span data-stu-id="85ecd-132">IID</span></span><br/>                      | <span data-ttu-id="85ecd-133">ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="85ecd-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="85ecd-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85ecd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ecd-135">**ивмвиртуалмачинивентс**</span><span class="sxs-lookup"><span data-stu-id="85ecd-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

