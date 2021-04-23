---
title: Интерфейс Ивмусбдевице (Впккоминтерфацес. h)
description: Определяет интерфейс USB-устройства, подключенного к узлу. USB-устройство можно подключить к виртуальной машине для использования устройства внутри виртуальной машины.
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- Виртуальный ПК с интерфейсом Ивмусбдевице
- Ивмусбдевице интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691856"
---
# <a name="ivmusbdevice-interface"></a><span data-ttu-id="7e049-106">Интерфейс Ивмусбдевице</span><span class="sxs-lookup"><span data-stu-id="7e049-106">IVMUSBDevice interface</span></span>

<span data-ttu-id="7e049-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7e049-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7e049-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7e049-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7e049-109">Определяет интерфейс USB-устройства, подключенного к узлу.</span><span class="sxs-lookup"><span data-stu-id="7e049-109">Defines the interface for a USB device attached to host.</span></span> <span data-ttu-id="7e049-110">USB-устройство можно подключить к виртуальной машине для использования устройства внутри виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7e049-110">You can attach USB device to a virtual machine to use the device inside the virtual machine.</span></span>

## <a name="members"></a><span data-ttu-id="7e049-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="7e049-111">Members</span></span>

<span data-ttu-id="7e049-112">Интерфейс **ивмусбдевице** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7e049-112">The **IVMUSBDevice** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="7e049-113">**Ивмусбдевице** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7e049-113">**IVMUSBDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="7e049-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="7e049-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e049-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="7e049-115">Properties</span></span>

<span data-ttu-id="7e049-116">Интерфейс **ивмусбдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7e049-116">The **IVMUSBDevice** interface has these properties.</span></span>



| <span data-ttu-id="7e049-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="7e049-117">Property</span></span>                                                                 | <span data-ttu-id="7e049-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="7e049-118">Access type</span></span>          | <span data-ttu-id="7e049-119">Описание</span><span class="sxs-lookup"><span data-stu-id="7e049-119">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="7e049-120">**аттачедтовм**</span><span class="sxs-lookup"><span data-stu-id="7e049-120">**AttachedToVM**</span></span>](ivmusbdevice-attachedtovm.md)<br/>             | <span data-ttu-id="7e049-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7e049-121">Read-only</span></span><br/> | <span data-ttu-id="7e049-122">Имя виртуальной машины, к которой подключено USB-устройство.</span><span class="sxs-lookup"><span data-stu-id="7e049-122">The name of the virtual machine to which the USB device is attached.</span></span><br/> |
| [<span data-ttu-id="7e049-123">**DeviceClass**</span><span class="sxs-lookup"><span data-stu-id="7e049-123">**DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)<br/>               | <span data-ttu-id="7e049-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7e049-124">Read-only</span></span><br/> | <span data-ttu-id="7e049-125">Класс устройства USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="7e049-125">The device class of the USB device.</span></span><br/>                                  |
| [<span data-ttu-id="7e049-126">**девицестринг**</span><span class="sxs-lookup"><span data-stu-id="7e049-126">**DeviceString**</span></span>](ivmusbdevice-devicestring.md)<br/>             | <span data-ttu-id="7e049-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7e049-127">Read-only</span></span><br/> | <span data-ttu-id="7e049-128">Имя USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="7e049-128">The name of the USB device.</span></span><br/>                                          |
| [<span data-ttu-id="7e049-129">**хубид**</span><span class="sxs-lookup"><span data-stu-id="7e049-129">**HubID**</span></span>](ivmusbdevice-hubid.md)<br/>                           | <span data-ttu-id="7e049-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7e049-130">Read-only</span></span><br/> | <span data-ttu-id="7e049-131">Идентификатор концентратора, к которому подключено устройство.</span><span class="sxs-lookup"><span data-stu-id="7e049-131">The identifier of the hub on which the device is connected.</span></span><br/>          |
| [<span data-ttu-id="7e049-132">**мануфактурерстринг**</span><span class="sxs-lookup"><span data-stu-id="7e049-132">**ManufacturerString**</span></span>](ivmusbdevice-manufacturerstring.md)<br/> | <span data-ttu-id="7e049-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7e049-133">Read-only</span></span><br/> | <span data-ttu-id="7e049-134">Имя изготовителя USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="7e049-134">The name of the USB device manufacturer.</span></span><br/>                             |
| [<span data-ttu-id="7e049-135">**Порту**</span><span class="sxs-lookup"><span data-stu-id="7e049-135">**Port**</span></span>](ivmusbdevice-port.md)<br/>                             | <span data-ttu-id="7e049-136">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7e049-136">Read-only</span></span><br/> | <span data-ttu-id="7e049-137">Идентификатор порта, к которому подключено устройство.</span><span class="sxs-lookup"><span data-stu-id="7e049-137">The identifier of the port on which the device is connected.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="7e049-138">Требования</span><span class="sxs-lookup"><span data-stu-id="7e049-138">Requirements</span></span>



| <span data-ttu-id="7e049-139">Требование</span><span class="sxs-lookup"><span data-stu-id="7e049-139">Requirement</span></span> | <span data-ttu-id="7e049-140">Значение</span><span class="sxs-lookup"><span data-stu-id="7e049-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e049-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e049-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7e049-142">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7e049-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e049-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e049-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7e049-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7e049-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7e049-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7e049-145">End of client support</span></span><br/>    | <span data-ttu-id="7e049-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e049-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7e049-147">Продукт</span><span class="sxs-lookup"><span data-stu-id="7e049-147">Product</span></span><br/>                  | <span data-ttu-id="7e049-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7e049-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7e049-149">Header</span><span class="sxs-lookup"><span data-stu-id="7e049-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e049-150"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e049-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7e049-151">IID</span><span class="sxs-lookup"><span data-stu-id="7e049-151">IID</span></span><br/>                      | <span data-ttu-id="7e049-152">IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="7e049-152">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



 

