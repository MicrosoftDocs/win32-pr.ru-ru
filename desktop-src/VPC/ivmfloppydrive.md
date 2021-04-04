---
title: Интерфейс Ивмфлоппидриве (Впккоминтерфацес. h)
description: Управляет дисководом гибких дисков в виртуальной машине.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Виртуальный ПК с интерфейсом Ивмфлоппидриве
- Ивмфлоппидриве интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989208"
---
# <a name="ivmfloppydrive-interface"></a><span data-ttu-id="e6bbe-105">Интерфейс Ивмфлоппидриве</span><span class="sxs-lookup"><span data-stu-id="e6bbe-105">IVMFloppyDrive interface</span></span>

<span data-ttu-id="e6bbe-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e6bbe-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e6bbe-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e6bbe-108">Управляет дисководом гибких дисков в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-108">Controls a floppy drive within a virtual machine.</span></span> <span data-ttu-id="e6bbe-109">**Ивмфлоппидриве** может уведомлять клиентов о событиях с помощью исходящего интерфейса [**ивмфлоппидрививентс**](ivmfloppydriveevents.md) .</span><span class="sxs-lookup"><span data-stu-id="e6bbe-109">**IVMFloppyDrive** can notify clients about events using the [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) outgoing interface.</span></span> <span data-ttu-id="e6bbe-110">Объект **ивмфлоппидриве** можно получить из объекта [**ивмфлоппидривеколлектион**](ivmfloppydrivecollection.md) , возвращенного из свойства [**ивмвиртуалмачине:: флоппидривес**](ivmvirtualmachine-floppydrives.md) .</span><span class="sxs-lookup"><span data-stu-id="e6bbe-110">You can retrieve an **IVMFloppyDrive** object from the [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) object returned from the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="e6bbe-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="e6bbe-111">Members</span></span>

<span data-ttu-id="e6bbe-112">Интерфейс **ивмфлоппидриве** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="e6bbe-112">The **IVMFloppyDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e6bbe-113">**Ивмфлоппидриве** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e6bbe-113">**IVMFloppyDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="e6bbe-114">Методы</span><span class="sxs-lookup"><span data-stu-id="e6bbe-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="e6bbe-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="e6bbe-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e6bbe-116">Методы</span><span class="sxs-lookup"><span data-stu-id="e6bbe-116">Methods</span></span>

<span data-ttu-id="e6bbe-117">Интерфейс **ивмфлоппидриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-117">The **IVMFloppyDrive** interface has these methods.</span></span>



| <span data-ttu-id="e6bbe-118">Метод</span><span class="sxs-lookup"><span data-stu-id="e6bbe-118">Method</span></span>                                                      | <span data-ttu-id="e6bbe-119">Описание</span><span class="sxs-lookup"><span data-stu-id="e6bbe-119">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6bbe-120">**аттачхостдриве**</span><span class="sxs-lookup"><span data-stu-id="e6bbe-120">**AttachHostDrive**</span></span>](ivmfloppydrive-attachhostdrive.md)   | <span data-ttu-id="e6bbe-121">Подключает физический диск на узле к дисководу гибких дисков виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-121">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span><br/> |
| [<span data-ttu-id="e6bbe-122">**аттачимаже**</span><span class="sxs-lookup"><span data-stu-id="e6bbe-122">**AttachImage**</span></span>](ivmfloppydrive-attachimage.md)           | <span data-ttu-id="e6bbe-123">Подключает образ гибкого носителя на узле к дисководу гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-123">Attaches a floppy media image on the host to the floppy drive.</span></span><br/>                    |
| [<span data-ttu-id="e6bbe-124">**релеасехостдриве**</span><span class="sxs-lookup"><span data-stu-id="e6bbe-124">**ReleaseHostDrive**</span></span>](ivmfloppydrive-releasehostdrive.md) | <span data-ttu-id="e6bbe-125">Освобождает физический диск узла с дисковода гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-125">Releases a physical drive on the host from the floppy drive.</span></span><br/>                      |
| [<span data-ttu-id="e6bbe-126">**релеасеимаже**</span><span class="sxs-lookup"><span data-stu-id="e6bbe-126">**ReleaseImage**</span></span>](ivmfloppydrive-releaseimage.md)         | <span data-ttu-id="e6bbe-127">Выпускают образ гибкого носителя на узле с дисковода гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-127">Releases a floppy media image on the host from the floppy drive.</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="e6bbe-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="e6bbe-128">Properties</span></span>

<span data-ttu-id="e6bbe-129">Интерфейс **ивмфлоппидриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-129">The **IVMFloppyDrive** interface has these properties.</span></span>



| <span data-ttu-id="e6bbe-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="e6bbe-130">Property</span></span>                                                             | <span data-ttu-id="e6bbe-131">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="e6bbe-131">Access type</span></span>          | <span data-ttu-id="e6bbe-132">Описание</span><span class="sxs-lookup"><span data-stu-id="e6bbe-132">Description</span></span>                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6bbe-133">**Вложение**</span><span class="sxs-lookup"><span data-stu-id="e6bbe-133">**Attachment**</span></span>](ivmfloppydrive-attachment.md)<br/>           | <span data-ttu-id="e6bbe-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e6bbe-134">Read-only</span></span><br/> | <span data-ttu-id="e6bbe-135">Тип носителя, подключенного к дисководу гибких дисков в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-135">The type of media attached to the floppy drive within the virtual machine.</span></span><br/>     |
| [<span data-ttu-id="e6bbe-136">**дривенумбер**</span><span class="sxs-lookup"><span data-stu-id="e6bbe-136">**DriveNumber**</span></span>](ivmfloppydrive-drivenumber.md)<br/>         | <span data-ttu-id="e6bbe-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e6bbe-137">Read-only</span></span><br/> | <span data-ttu-id="e6bbe-138">Отсчитываемый от нуля индекс контроллера, к которому подключен гибкий дисковод.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-138">The zero-based index of the controller to which this floppy drive is attached.</span></span><br/> |
| [<span data-ttu-id="e6bbe-139">**хостдривелеттер**</span><span class="sxs-lookup"><span data-stu-id="e6bbe-139">**HostDriveLetter**</span></span>](ivmfloppydrive-hostdriveletter.md)<br/> | <span data-ttu-id="e6bbe-140">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e6bbe-140">Read-only</span></span><br/> | <span data-ttu-id="e6bbe-141">Буква диска узла, к которому подключен дисковод гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-141">The letter of the host drive to which the floppy drive is attached.</span></span><br/>            |
| [<span data-ttu-id="e6bbe-142">**Изображения**</span><span class="sxs-lookup"><span data-stu-id="e6bbe-142">**ImageFile**</span></span>](ivmfloppydrive-imagefile.md)<br/>             | <span data-ttu-id="e6bbe-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e6bbe-143">Read-only</span></span><br/> | <span data-ttu-id="e6bbe-144">Полный путь к файлу образа, к которому подключен дисковод гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="e6bbe-144">The full path of the image file to which the floppy drive is attached.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="e6bbe-145">Требования</span><span class="sxs-lookup"><span data-stu-id="e6bbe-145">Requirements</span></span>



| <span data-ttu-id="e6bbe-146">Требование</span><span class="sxs-lookup"><span data-stu-id="e6bbe-146">Requirement</span></span> | <span data-ttu-id="e6bbe-147">Значение</span><span class="sxs-lookup"><span data-stu-id="e6bbe-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6bbe-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6bbe-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e6bbe-149">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e6bbe-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6bbe-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6bbe-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e6bbe-151">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e6bbe-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e6bbe-152">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e6bbe-152">End of client support</span></span><br/>    | <span data-ttu-id="e6bbe-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6bbe-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e6bbe-154">Продукт</span><span class="sxs-lookup"><span data-stu-id="e6bbe-154">Product</span></span><br/>                  | <span data-ttu-id="e6bbe-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e6bbe-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e6bbe-156">Header</span><span class="sxs-lookup"><span data-stu-id="e6bbe-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6bbe-157"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6bbe-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e6bbe-158">IID</span><span class="sxs-lookup"><span data-stu-id="e6bbe-158">IID</span></span><br/>                      | <span data-ttu-id="e6bbe-159">IID \_ ивмфлоппидриве определен как 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="e6bbe-159">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



 

