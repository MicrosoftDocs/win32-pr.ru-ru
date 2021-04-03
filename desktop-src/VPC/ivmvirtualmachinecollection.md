---
title: Интерфейс Ивмвиртуалмачинеколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию виртуальных машин в Windows Virtual PC. Чтобы получить объект Ивмвиртуалмачинеколлектион, используйте свойство VirtualMachines Ивмвиртуалпк.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- Виртуальный ПК с интерфейсом Ивмвиртуалмачинеколлектион
- Ивмвиртуалмачинеколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137210"
---
# <a name="ivmvirtualmachinecollection-interface"></a><span data-ttu-id="25595-106">Интерфейс Ивмвиртуалмачинеколлектион</span><span class="sxs-lookup"><span data-stu-id="25595-106">IVMVirtualMachineCollection interface</span></span>

<span data-ttu-id="25595-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="25595-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="25595-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="25595-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="25595-109">Определяет коллекцию виртуальных машин в Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="25595-109">Defines the collection of virtual machines within Windows Virtual PC.</span></span> <span data-ttu-id="25595-110">Чтобы получить объект **ивмвиртуалмачинеколлектион** , используйте свойство [**Ивмвиртуалпк:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .</span><span class="sxs-lookup"><span data-stu-id="25595-110">To obtain an **IVMVirtualMachineCollection** object, use the [**IVMVirtualPC::VirtualMachines**](ivmvirtualpc-virtualmachines.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="25595-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="25595-111">Members</span></span>

<span data-ttu-id="25595-112">Интерфейс **ивмвиртуалмачинеколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="25595-112">The **IVMVirtualMachineCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="25595-113">**Ивмвиртуалмачинеколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="25595-113">**IVMVirtualMachineCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="25595-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="25595-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25595-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="25595-115">Properties</span></span>

<span data-ttu-id="25595-116">Интерфейс **ивмвиртуалмачинеколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="25595-116">The **IVMVirtualMachineCollection** interface has these properties.</span></span>



| <span data-ttu-id="25595-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="25595-117">Property</span></span>                                                             | <span data-ttu-id="25595-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="25595-118">Access type</span></span>          | <span data-ttu-id="25595-119">Описание</span><span class="sxs-lookup"><span data-stu-id="25595-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="25595-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="25595-120">**\_NewEnum**</span></span>](ivmvirtualmachinecollection--newenum.md)<br/> | <span data-ttu-id="25595-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="25595-121">Read-only</span></span><br/> | <span data-ttu-id="25595-122">Перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="25595-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="25595-123">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="25595-123">**Count**</span></span>](ivmvirtualmachinecollection-count.md)<br/>        | <span data-ttu-id="25595-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="25595-124">Read-only</span></span><br/> | <span data-ttu-id="25595-125">Число виртуальных машин в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="25595-125">The number of virtual machines in this collection.</span></span><br/>                  |
| [<span data-ttu-id="25595-126">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="25595-126">**Item**</span></span>](ivmvirtualmachinecollection-item.md)<br/>          | <span data-ttu-id="25595-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="25595-127">Read-only</span></span><br/> | <span data-ttu-id="25595-128">Объект виртуальной машины, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="25595-128">The virtual machine object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="25595-129">Требования</span><span class="sxs-lookup"><span data-stu-id="25595-129">Requirements</span></span>



| <span data-ttu-id="25595-130">Требование</span><span class="sxs-lookup"><span data-stu-id="25595-130">Requirement</span></span> | <span data-ttu-id="25595-131">Значение</span><span class="sxs-lookup"><span data-stu-id="25595-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25595-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25595-132">Minimum supported client</span></span><br/> | <span data-ttu-id="25595-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="25595-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="25595-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25595-134">Minimum supported server</span></span><br/> | <span data-ttu-id="25595-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25595-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="25595-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="25595-136">End of client support</span></span><br/>    | <span data-ttu-id="25595-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="25595-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="25595-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="25595-138">Product</span></span><br/>                  | <span data-ttu-id="25595-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="25595-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="25595-140">Header</span><span class="sxs-lookup"><span data-stu-id="25595-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="25595-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="25595-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="25595-142">IID</span><span class="sxs-lookup"><span data-stu-id="25595-142">IID</span></span><br/>                      | <span data-ttu-id="25595-143">IID \_ ивмвиртуалмачинеколлектион определен как 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="25595-143">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25595-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25595-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25595-145">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="25595-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="25595-146">**Ивмвиртуалпк:: VirtualMachines**</span><span class="sxs-lookup"><span data-stu-id="25595-146">**IVMVirtualPC::VirtualMachines**</span></span>](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

