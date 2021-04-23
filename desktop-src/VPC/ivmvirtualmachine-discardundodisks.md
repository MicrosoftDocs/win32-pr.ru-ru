---
title: Метод Ивмвиртуалмачине Дискардундодискс (Впккоминтерфацес. h)
description: Отменяет виртуальные диски отмены.
ms.assetid: 5c3a4b3f-ea58-498c-b7cf-54f028fa061c
keywords:
- Метод Дискардундодискс Virtual PC
- Метод Дискардундодискс Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Дискардундодискс
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d548b69a6cfebc383a0233f01ef19ad14d051474
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490935"
---
# <a name="ivmvirtualmachinediscardundodisks-method"></a><span data-ttu-id="5436d-106">Ивмвиртуалмачине: метод:D Искардундодискс</span><span class="sxs-lookup"><span data-stu-id="5436d-106">IVMVirtualMachine::DiscardUndoDisks method</span></span>

<span data-ttu-id="5436d-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5436d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5436d-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5436d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5436d-109">Отменяет виртуальные диски отмены.</span><span class="sxs-lookup"><span data-stu-id="5436d-109">Discards the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="5436d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5436d-110">Syntax</span></span>


```C++
HRESULT DiscardUndoDisks();
```



## <a name="parameters"></a><span data-ttu-id="5436d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5436d-111">Parameters</span></span>

<span data-ttu-id="5436d-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5436d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5436d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5436d-113">Return value</span></span>

<span data-ttu-id="5436d-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="5436d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="5436d-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="5436d-115">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="5436d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5436d-116">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5436d-117"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5436d-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="5436d-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5436d-118">The operation was successful.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="5436d-119"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5436d-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="5436d-120">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="5436d-120">The configuration is unknown.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="5436d-121"><dt>**Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="5436d-121"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="5436d-122">Виртуальные диски отмены не могут быть удалены, пока виртуальная машина работает или находится в сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="5436d-122">The virtual undo disks cannot be discarded while the virtual machine is running or in a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="5436d-123"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5436d-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="5436d-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5436d-124">An unexpected error has occurred.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="5436d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5436d-125">Requirements</span></span>



| <span data-ttu-id="5436d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5436d-126">Requirement</span></span> | <span data-ttu-id="5436d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5436d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5436d-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5436d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5436d-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5436d-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5436d-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5436d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5436d-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5436d-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5436d-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5436d-132">End of client support</span></span><br/>    | <span data-ttu-id="5436d-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5436d-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5436d-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="5436d-134">Product</span></span><br/>                  | <span data-ttu-id="5436d-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5436d-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5436d-136">Header</span><span class="sxs-lookup"><span data-stu-id="5436d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5436d-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="5436d-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5436d-138">IID</span><span class="sxs-lookup"><span data-stu-id="5436d-138">IID</span></span><br/>                      | <span data-ttu-id="5436d-139">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="5436d-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="5436d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5436d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5436d-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="5436d-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

