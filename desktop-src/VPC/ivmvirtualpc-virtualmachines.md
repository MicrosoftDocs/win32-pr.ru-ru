---
title: Свойство VirtualMachines Ивмвиртуалпк (Впккоминтерфацес. h)
description: Извлекает перечисляемую коллекцию виртуальных машин.
ms.assetid: 9e8dcd65-7cf8-4cdd-a412-62cbb96eb8ec
keywords:
- VirtualMachines свойство Virtual PC
- VirtualMachines свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство VirtualMachines
topic_type:
- apiref
api_name:
- IVMVirtualPC.VirtualMachines
- IVMVirtualPC.get_VirtualMachines
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44e141208994fa3d759074e7cbb294e1e2158917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650400"
---
# <a name="ivmvirtualpcvirtualmachines-property"></a><span data-ttu-id="ef917-106">Свойство Ивмвиртуалпк:: VirtualMachines</span><span class="sxs-lookup"><span data-stu-id="ef917-106">IVMVirtualPC::VirtualMachines property</span></span>

<span data-ttu-id="ef917-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ef917-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ef917-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ef917-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ef917-109">Извлекает перечисляемую коллекцию виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ef917-109">Retrieves an enumerable collection of virtual machines.</span></span>

<span data-ttu-id="ef917-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ef917-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef917-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef917-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachines(
  [out, retval] IVMVirtualMachineCollection **virtualMachineCollection
);
```



## <a name="property-value"></a><span data-ttu-id="ef917-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ef917-112">Property value</span></span>

<span data-ttu-id="ef917-113">Коллекция объектов [**ивмвиртуалмачине**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="ef917-113">A collection of [**IVMVirtualMachine**](ivmvirtualmachine.md) objects.</span></span> <span data-ttu-id="ef917-114">См. [**ивмвиртуалмачинеколлектион**](ivmvirtualmachinecollection.md).</span><span class="sxs-lookup"><span data-stu-id="ef917-114">See [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="ef917-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ef917-115">Error codes</span></span>



| <span data-ttu-id="ef917-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="ef917-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="ef917-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ef917-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef917-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ef917-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="ef917-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ef917-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ef917-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="ef917-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="ef917-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ef917-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ef917-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ef917-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="ef917-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ef917-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="ef917-124"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="ef917-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="ef917-125">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="ef917-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ef917-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ef917-126">Requirements</span></span>



| <span data-ttu-id="ef917-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ef917-127">Requirement</span></span> | <span data-ttu-id="ef917-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ef917-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef917-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef917-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ef917-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ef917-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef917-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef917-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ef917-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ef917-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ef917-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ef917-133">End of client support</span></span><br/>    | <span data-ttu-id="ef917-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ef917-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ef917-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="ef917-135">Product</span></span><br/>                  | <span data-ttu-id="ef917-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ef917-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ef917-137">Header</span><span class="sxs-lookup"><span data-stu-id="ef917-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef917-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef917-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ef917-139">IID</span><span class="sxs-lookup"><span data-stu-id="ef917-139">IID</span></span><br/>                      | <span data-ttu-id="ef917-140">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="ef917-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ef917-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef917-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef917-142">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="ef917-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

