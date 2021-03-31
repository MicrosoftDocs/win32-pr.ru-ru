---
title: Интерфейс Ивмдвддриве (Впккоминтерфацес. h)
description: Управляет дисководом компакт-дисков или DVD-дисков в виртуальной машине. Ивмдвддриве может уведомлять клиентов о событиях с помощью исходящего интерфейса Ивмдвддрививентс.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- Виртуальный ПК с интерфейсом Ивмдвддриве
- Ивмдвддриве интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071760"
---
# <a name="ivmdvddrive-interface"></a><span data-ttu-id="78dfa-106">Интерфейс Ивмдвддриве</span><span class="sxs-lookup"><span data-stu-id="78dfa-106">IVMDVDDrive interface</span></span>

<span data-ttu-id="78dfa-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="78dfa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="78dfa-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="78dfa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="78dfa-109">Управляет дисководом компакт-дисков или DVD-дисков в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="78dfa-109">Controls a CD-ROM or DVD-ROM drive within a virtual machine.</span></span> <span data-ttu-id="78dfa-110">**Ивмдвддриве** может уведомлять клиентов о событиях с помощью исходящего интерфейса [**ивмдвддрививентс**](ivmdvddriveevents.md) .</span><span class="sxs-lookup"><span data-stu-id="78dfa-110">**IVMDVDDrive** can notify clients about events using the [**IVMDVDDriveEvents**](ivmdvddriveevents.md) outgoing interface.</span></span>

<span data-ttu-id="78dfa-111">На виртуальную машину можно добавить новый дисковод компакт-или DVD-дисков с помощью метода [**ивмвиртуалмачине:: адддвдромдриве**](ivmvirtualmachine-adddvdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="78dfa-111">You can add a new CD-ROM or DVD-ROM drive to a virtual machine using the [**IVMVirtualMachine::AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) method.</span></span> <span data-ttu-id="78dfa-112">Вы можете удалить существующий компакт-диск или DVD-дисковод из виртуальной машины с помощью метода [**ивмвиртуалмачине:: ремоведвдромдриве**](ivmvirtualmachine-removedvdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="78dfa-112">You can remove an existing CD-ROM or DVD-ROM drive from a virtual machine using the [**IVMVirtualMachine::RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) method.</span></span> <span data-ttu-id="78dfa-113">Объект **ивмдвддриве** можно получить из объекта [**ивмдвддривеколлектион**](ivmdvddrivecollection.md) , возвращенного из свойства [**ивмвиртуалмачине::D вдромдривес**](ivmvirtualmachine-dvdromdrives.md) .</span><span class="sxs-lookup"><span data-stu-id="78dfa-113">You can retrieve an **IVMDVDDrive** object from the [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) object returned from the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="78dfa-114">Элементы</span><span class="sxs-lookup"><span data-stu-id="78dfa-114">Members</span></span>

<span data-ttu-id="78dfa-115">Интерфейс **ивмдвддриве** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="78dfa-115">The **IVMDVDDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="78dfa-116">**Ивмдвддриве** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="78dfa-116">**IVMDVDDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="78dfa-117">Методы</span><span class="sxs-lookup"><span data-stu-id="78dfa-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="78dfa-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="78dfa-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="78dfa-119">Методы</span><span class="sxs-lookup"><span data-stu-id="78dfa-119">Methods</span></span>

<span data-ttu-id="78dfa-120">Интерфейс **ивмдвддриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="78dfa-120">The **IVMDVDDrive** interface has these methods.</span></span>



| <span data-ttu-id="78dfa-121">Метод</span><span class="sxs-lookup"><span data-stu-id="78dfa-121">Method</span></span>                                                   | <span data-ttu-id="78dfa-122">Описание</span><span class="sxs-lookup"><span data-stu-id="78dfa-122">Description</span></span>                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="78dfa-123">**аттачхостдриве**</span><span class="sxs-lookup"><span data-stu-id="78dfa-123">**AttachHostDrive**</span></span>](ivmdvddrive-attachhostdrive.md)   | <span data-ttu-id="78dfa-124">Подключает диск узла к DVD-дисководу в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="78dfa-124">Attaches a host drive to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="78dfa-125">**аттачимаже**</span><span class="sxs-lookup"><span data-stu-id="78dfa-125">**AttachImage**</span></span>](ivmdvddrive-attachimage.md)           | <span data-ttu-id="78dfa-126">Подключает образ ISO к DVD-дисководу в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="78dfa-126">Attaches an ISO image to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="78dfa-127">**релеасехостдриве**</span><span class="sxs-lookup"><span data-stu-id="78dfa-127">**ReleaseHostDrive**</span></span>](ivmdvddrive-releasehostdrive.md) | <span data-ttu-id="78dfa-128">Освобождает захваченный диск узла с DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="78dfa-128">Releases a captured host drive from the DVD drive.</span></span><br/>                           |
| [<span data-ttu-id="78dfa-129">**релеасеимаже**</span><span class="sxs-lookup"><span data-stu-id="78dfa-129">**ReleaseImage**</span></span>](ivmdvddrive-releaseimage.md)         | <span data-ttu-id="78dfa-130">Освобождает захваченный образ ISO с DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="78dfa-130">Releases a captured ISO image from the DVD drive.</span></span><br/>                            |
| [<span data-ttu-id="78dfa-131">**сетбуслокатион**</span><span class="sxs-lookup"><span data-stu-id="78dfa-131">**SetBusLocation**</span></span>](ivmdvddrive-setbuslocation.md)     | <span data-ttu-id="78dfa-132">Подключает DVD-дисковод к указанному расположению шины на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="78dfa-132">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="78dfa-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="78dfa-133">Properties</span></span>

<span data-ttu-id="78dfa-134">Интерфейс **ивмдвддриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="78dfa-134">The **IVMDVDDrive** interface has these properties.</span></span>



| <span data-ttu-id="78dfa-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="78dfa-135">Property</span></span>                                                          | <span data-ttu-id="78dfa-136">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="78dfa-136">Access type</span></span>          | <span data-ttu-id="78dfa-137">Описание</span><span class="sxs-lookup"><span data-stu-id="78dfa-137">Description</span></span>                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="78dfa-138">**Вложение**</span><span class="sxs-lookup"><span data-stu-id="78dfa-138">**Attachment**</span></span>](ivmdvddrive-attachment.md)<br/>           | <span data-ttu-id="78dfa-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="78dfa-139">Read-only</span></span><br/> | <span data-ttu-id="78dfa-140">Тип носителя, подключенного к DVD-дисководу в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="78dfa-140">The type of media attached to the DVD drive within the virtual machine.</span></span><br/> |
| [<span data-ttu-id="78dfa-141">**буснумбер**</span><span class="sxs-lookup"><span data-stu-id="78dfa-141">**BusNumber**</span></span>](ivmdvddrive-busnumber.md)<br/>             | <span data-ttu-id="78dfa-142">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="78dfa-142">Read-only</span></span><br/> | <span data-ttu-id="78dfa-143">Номер шины, к которой подключено устройство.</span><span class="sxs-lookup"><span data-stu-id="78dfa-143">The bus number to which this device is attached.</span></span><br/>                        |
| [<span data-ttu-id="78dfa-144">**девиценумбер**</span><span class="sxs-lookup"><span data-stu-id="78dfa-144">**DeviceNumber**</span></span>](ivmdvddrive-devicenumber.md)<br/>       | <span data-ttu-id="78dfa-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="78dfa-145">Read-only</span></span><br/> | <span data-ttu-id="78dfa-146">Номер устройства, к которому подключен диск.</span><span class="sxs-lookup"><span data-stu-id="78dfa-146">The device number to which this drive is attached.</span></span><br/>                      |
| [<span data-ttu-id="78dfa-147">**хостдривелеттер**</span><span class="sxs-lookup"><span data-stu-id="78dfa-147">**HostDriveLetter**</span></span>](ivmdvddrive-hostdriveletter.md)<br/> | <span data-ttu-id="78dfa-148">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="78dfa-148">Read-only</span></span><br/> | <span data-ttu-id="78dfa-149">Буква диска узла, заданная для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="78dfa-149">The letter of the host drive set for this device.</span></span><br/>                       |
| [<span data-ttu-id="78dfa-150">**Изображения**</span><span class="sxs-lookup"><span data-stu-id="78dfa-150">**ImageFile**</span></span>](ivmdvddrive-imagefile.md)<br/>             | <span data-ttu-id="78dfa-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="78dfa-151">Read-only</span></span><br/> | <span data-ttu-id="78dfa-152">Полный путь к набору файлов изображений для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="78dfa-152">The full path of the image file set for this device.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="78dfa-153">Требования</span><span class="sxs-lookup"><span data-stu-id="78dfa-153">Requirements</span></span>



| <span data-ttu-id="78dfa-154">Требование</span><span class="sxs-lookup"><span data-stu-id="78dfa-154">Requirement</span></span> | <span data-ttu-id="78dfa-155">Значение</span><span class="sxs-lookup"><span data-stu-id="78dfa-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78dfa-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78dfa-156">Minimum supported client</span></span><br/> | <span data-ttu-id="78dfa-157">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="78dfa-157">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78dfa-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78dfa-158">Minimum supported server</span></span><br/> | <span data-ttu-id="78dfa-159">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="78dfa-159">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="78dfa-160">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="78dfa-160">End of client support</span></span><br/>    | <span data-ttu-id="78dfa-161">Windows 7</span><span class="sxs-lookup"><span data-stu-id="78dfa-161">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="78dfa-162">Продукт</span><span class="sxs-lookup"><span data-stu-id="78dfa-162">Product</span></span><br/>                  | <span data-ttu-id="78dfa-163">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="78dfa-163">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="78dfa-164">Header</span><span class="sxs-lookup"><span data-stu-id="78dfa-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="78dfa-165"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="78dfa-165"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="78dfa-166">IID</span><span class="sxs-lookup"><span data-stu-id="78dfa-166">IID</span></span><br/>                      | <span data-ttu-id="78dfa-167">IID \_ ивмдвддриве определен как b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="78dfa-167">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



 

