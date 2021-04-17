---
title: Интерфейс Ивмусбдевицеколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию USB-устройств, подключенных к системе узла. Чтобы получить объект Ивмусбдевицеколлектион, используйте свойство Усбдевицеколлектион Ивмвиртуалпк.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Виртуальный ПК с интерфейсом Ивмусбдевицеколлектион
- Ивмусбдевицеколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e773f006a1d98253a20ad37d5a70db43f487980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691836"
---
# <a name="ivmusbdevicecollection-interface"></a><span data-ttu-id="93861-106">Интерфейс Ивмусбдевицеколлектион</span><span class="sxs-lookup"><span data-stu-id="93861-106">IVMUSBDeviceCollection interface</span></span>

<span data-ttu-id="93861-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="93861-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="93861-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="93861-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="93861-109">Определяет коллекцию USB-устройств, подключенных к системе узла.</span><span class="sxs-lookup"><span data-stu-id="93861-109">Defines the collection of USB devices attached to the host system.</span></span> <span data-ttu-id="93861-110">Чтобы получить объект **ивмусбдевицеколлектион** , используйте свойство [**Ивмвиртуалпк:: усбдевицеколлектион**](ivmvirtualpc-usbdevicecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="93861-110">To obtain an **IVMUSBDeviceCollection** object, use the [**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="93861-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="93861-111">Members</span></span>

<span data-ttu-id="93861-112">Интерфейс **ивмусбдевицеколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="93861-112">The **IVMUSBDeviceCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="93861-113">**Ивмусбдевицеколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="93861-113">**IVMUSBDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="93861-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="93861-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93861-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="93861-115">Properties</span></span>

<span data-ttu-id="93861-116">Интерфейс **ивмусбдевицеколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="93861-116">The **IVMUSBDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="93861-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="93861-117">Property</span></span>                                                        | <span data-ttu-id="93861-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="93861-118">Access type</span></span>          | <span data-ttu-id="93861-119">Описание</span><span class="sxs-lookup"><span data-stu-id="93861-119">Description</span></span>                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="93861-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="93861-120">**\_NewEnum**</span></span>](ivmusbdevicecollection--newenum.md)<br/> | <span data-ttu-id="93861-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="93861-121">Read-only</span></span><br/> | <span data-ttu-id="93861-122">Перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="93861-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="93861-123">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="93861-123">**Count**</span></span>](ivmusbdevicecollection-count.md)<br/>        | <span data-ttu-id="93861-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="93861-124">Read-only</span></span><br/> | <span data-ttu-id="93861-125">Число USB-устройств в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="93861-125">The number of USB devices in this collection.</span></span><br/>                            |
| [<span data-ttu-id="93861-126">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="93861-126">**Item**</span></span>](ivmusbdevicecollection-item.md)<br/>          | <span data-ttu-id="93861-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="93861-127">Read-only</span></span><br/> | <span data-ttu-id="93861-128">Объект USB-устройства, соответствующий заданному индексу (от 1).</span><span class="sxs-lookup"><span data-stu-id="93861-128">The USB device object that corresponds to the specified index (1-based).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="93861-129">Требования</span><span class="sxs-lookup"><span data-stu-id="93861-129">Requirements</span></span>



| <span data-ttu-id="93861-130">Требование</span><span class="sxs-lookup"><span data-stu-id="93861-130">Requirement</span></span> | <span data-ttu-id="93861-131">Значение</span><span class="sxs-lookup"><span data-stu-id="93861-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="93861-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93861-132">Minimum supported client</span></span><br/> | <span data-ttu-id="93861-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="93861-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93861-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93861-134">Minimum supported server</span></span><br/> | <span data-ttu-id="93861-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="93861-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="93861-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="93861-136">End of client support</span></span><br/>    | <span data-ttu-id="93861-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="93861-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="93861-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="93861-138">Product</span></span><br/>                  | <span data-ttu-id="93861-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="93861-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="93861-140">Header</span><span class="sxs-lookup"><span data-stu-id="93861-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="93861-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="93861-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="93861-142">IID</span><span class="sxs-lookup"><span data-stu-id="93861-142">IID</span></span><br/>                      | <span data-ttu-id="93861-143">IID \_ ивмусбдевицеколлектион определен как 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="93861-143">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="93861-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93861-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93861-145">**ивмусбдевице**</span><span class="sxs-lookup"><span data-stu-id="93861-145">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="93861-146">**Ивмвиртуалпк:: Усбдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="93861-146">**IVMVirtualPC::USBDeviceCollection**</span></span>](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

