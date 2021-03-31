---
title: Интерфейс Ивмнетворкадаптерколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию адаптеров виртуальных сетевых интерфейсов. Чтобы получить объект Ивмнетворкадаптерколлектион, используйте свойства Ивмвиртуалмачине адаптера, Ивмвиртуалнетворк адаптера и Ивмвиртуалпк Унконнектеднетворкадаптерс.
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Виртуальный ПК с интерфейсом Ивмнетворкадаптерколлектион
- Ивмнетворкадаптерколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071722"
---
# <a name="ivmnetworkadaptercollection-interface"></a><span data-ttu-id="0b9ff-106">Интерфейс Ивмнетворкадаптерколлектион</span><span class="sxs-lookup"><span data-stu-id="0b9ff-106">IVMNetworkAdapterCollection interface</span></span>

<span data-ttu-id="0b9ff-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0b9ff-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0b9ff-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0b9ff-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0b9ff-109">Определяет коллекцию адаптеров виртуальных сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="0b9ff-109">Defines a collection of virtual network interface cards.</span></span> <span data-ttu-id="0b9ff-110">Чтобы получить объект Ивмнетворкадаптерколлектион, используйте свойства [**ивмвиртуалмачине:: адаптера**](ivmvirtualmachine-networkadapters.md), [**Ивмвиртуалнетворк:: адаптера**](ivmvirtualnetwork-networkadapters.md)и [**ивмвиртуалпк:: унконнектеднетворкадаптерс**](ivmvirtualpc-unconnectednetworkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="0b9ff-110">To obtain an IVMNetworkAdapterCollection object, use the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md), and [**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="0b9ff-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="0b9ff-111">Members</span></span>

<span data-ttu-id="0b9ff-112">Интерфейс **ивмнетворкадаптерколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="0b9ff-112">The **IVMNetworkAdapterCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="0b9ff-113">**Ивмнетворкадаптерколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0b9ff-113">**IVMNetworkAdapterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="0b9ff-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="0b9ff-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b9ff-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="0b9ff-115">Properties</span></span>

<span data-ttu-id="0b9ff-116">Интерфейс **ивмнетворкадаптерколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0b9ff-116">The **IVMNetworkAdapterCollection** interface has these properties.</span></span>



| <span data-ttu-id="0b9ff-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="0b9ff-117">Property</span></span>                                                             | <span data-ttu-id="0b9ff-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="0b9ff-118">Access type</span></span>          | <span data-ttu-id="0b9ff-119">Описание</span><span class="sxs-lookup"><span data-stu-id="0b9ff-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b9ff-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="0b9ff-120">**\_NewEnum**</span></span>](ivmnetworkadaptercollection--newenum.md)<br/> | <span data-ttu-id="0b9ff-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b9ff-121">Read-only</span></span><br/> | <span data-ttu-id="0b9ff-122">Перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="0b9ff-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="0b9ff-123">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="0b9ff-123">**Count**</span></span>](ivmnetworkadaptercollection-count.md)<br/>        | <span data-ttu-id="0b9ff-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b9ff-124">Read-only</span></span><br/> | <span data-ttu-id="0b9ff-125">Число сетевых интерфейсов в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="0b9ff-125">The number of network interfaces in this collection.</span></span><br/>                                               |
| [<span data-ttu-id="0b9ff-126">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0b9ff-126">**Item**</span></span>](ivmnetworkadaptercollection-item.md)<br/>          | <span data-ttu-id="0b9ff-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b9ff-127">Read-only</span></span><br/> | <span data-ttu-id="0b9ff-128">Объект [**ивмнетворкадаптер**](ivmnetworkadapter.md) , соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="0b9ff-128">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0b9ff-129">Требования</span><span class="sxs-lookup"><span data-stu-id="0b9ff-129">Requirements</span></span>



| <span data-ttu-id="0b9ff-130">Требование</span><span class="sxs-lookup"><span data-stu-id="0b9ff-130">Requirement</span></span> | <span data-ttu-id="0b9ff-131">Значение</span><span class="sxs-lookup"><span data-stu-id="0b9ff-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9ff-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b9ff-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0b9ff-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0b9ff-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b9ff-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b9ff-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0b9ff-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0b9ff-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0b9ff-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0b9ff-136">End of client support</span></span><br/>    | <span data-ttu-id="0b9ff-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b9ff-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="0b9ff-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="0b9ff-138">Product</span></span><br/>                  | <span data-ttu-id="0b9ff-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0b9ff-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="0b9ff-140">Header</span><span class="sxs-lookup"><span data-stu-id="0b9ff-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b9ff-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b9ff-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="0b9ff-142">IID</span><span class="sxs-lookup"><span data-stu-id="0b9ff-142">IID</span></span><br/>                      | <span data-ttu-id="0b9ff-143">IID \_ ивмнетворкадаптерколлектион определен как ebaeafe9-EBCD-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="0b9ff-143">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b9ff-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b9ff-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9ff-145">**ивмнетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="0b9ff-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="0b9ff-146">**Ивмвиртуалмачине:: адаптера**</span><span class="sxs-lookup"><span data-stu-id="0b9ff-146">**IVMVirtualMachine::NetworkAdapters**</span></span>](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="0b9ff-147">**Ивмвиртуалнетворк:: адаптера**</span><span class="sxs-lookup"><span data-stu-id="0b9ff-147">**IVMVirtualNetwork::NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="0b9ff-148">**Ивмвиртуалпк:: Унконнектеднетворкадаптерс**</span><span class="sxs-lookup"><span data-stu-id="0b9ff-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span></span>](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

