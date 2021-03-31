---
title: Метод Ивмвиртуалмачине Дискардсаведстате (Впккоминтерфацес. h)
description: Отменяет все сохраненные сведения о состоянии для сохраненной виртуальной машины.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- Метод Дискардсаведстате Virtual PC
- Метод Дискардсаведстате Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Дискардсаведстате
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce5c9cc0b07af2cc8c995d0c368d7747fa1475a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071753"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a><span data-ttu-id="a96dc-106">Ивмвиртуалмачине: метод:D Искардсаведстате</span><span class="sxs-lookup"><span data-stu-id="a96dc-106">IVMVirtualMachine::DiscardSavedState method</span></span>

<span data-ttu-id="a96dc-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a96dc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a96dc-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a96dc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a96dc-109">Отменяет все сохраненные сведения о состоянии для сохраненной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a96dc-109">Discards any saved state information for a saved virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a96dc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a96dc-110">Syntax</span></span>


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a><span data-ttu-id="a96dc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a96dc-111">Parameters</span></span>

<span data-ttu-id="a96dc-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a96dc-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a96dc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a96dc-113">Return value</span></span>

<span data-ttu-id="a96dc-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a96dc-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a96dc-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="a96dc-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="a96dc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a96dc-116">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a96dc-117"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a96dc-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="a96dc-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a96dc-118">The operation was successful.</span></span><br/>                               |
| <dl> <span data-ttu-id="a96dc-119"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a96dc-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="a96dc-120">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="a96dc-120">The configuration is unknown.</span></span><br/>                               |
| <dl> <span data-ttu-id="a96dc-121"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ с**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="a96dc-121"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>           | <span data-ttu-id="a96dc-122">Виртуальная машина запущена.</span><span class="sxs-lookup"><span data-stu-id="a96dc-122">The virtual machine is running.</span></span><br/>                             |
| <dl> <span data-ttu-id="a96dc-123"><dt>**Виртуальная машина \_ Электронная \_ Виртуальная машина \_ без \_ сохраненного \_ состояния**</dt> <dt>0xA00400501</dt></span><span class="sxs-lookup"><span data-stu-id="a96dc-123"><dt>**VM\_E\_VM\_NO\_SAVED\_STATE**</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="a96dc-124">Виртуальная машина не запущена, но не имеет сохраненного состояния.</span><span class="sxs-lookup"><span data-stu-id="a96dc-124">The virtual machine is not running, but has no saved state.</span></span><br/> |
| <dl> <span data-ttu-id="a96dc-125"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a96dc-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="a96dc-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a96dc-126">An unexpected error has occurred.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="a96dc-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a96dc-127">Requirements</span></span>



| <span data-ttu-id="a96dc-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a96dc-128">Requirement</span></span> | <span data-ttu-id="a96dc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a96dc-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a96dc-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a96dc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a96dc-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a96dc-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a96dc-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a96dc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a96dc-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a96dc-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a96dc-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a96dc-134">End of client support</span></span><br/>    | <span data-ttu-id="a96dc-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a96dc-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a96dc-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="a96dc-136">Product</span></span><br/>                  | <span data-ttu-id="a96dc-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a96dc-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a96dc-138">Header</span><span class="sxs-lookup"><span data-stu-id="a96dc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a96dc-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="a96dc-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a96dc-140">IID</span><span class="sxs-lookup"><span data-stu-id="a96dc-140">IID</span></span><br/>                      | <span data-ttu-id="a96dc-141">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="a96dc-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a96dc-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a96dc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a96dc-143">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="a96dc-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

