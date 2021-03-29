---
title: Интерфейс Ивмдвддривеколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию дисков CD и DVD в виртуальной машине. Чтобы получить объект Ивмдвддривеколлектион, используйте свойство Двдромдривес Ивмвиртуалмачине.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- Виртуальный ПК с интерфейсом Ивмдвддривеколлектион
- Ивмдвддривеколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afcf14a1ffe53dea0dcd7e21fcde8729e0bd0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650382"
---
# <a name="ivmdvddrivecollection-interface"></a><span data-ttu-id="885bd-106">Интерфейс Ивмдвддривеколлектион</span><span class="sxs-lookup"><span data-stu-id="885bd-106">IVMDVDDriveCollection interface</span></span>

<span data-ttu-id="885bd-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="885bd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="885bd-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="885bd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="885bd-109">Определяет коллекцию дисков CD и DVD в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="885bd-109">Defines the collection of CD and DVD drives within the virtual machine.</span></span> <span data-ttu-id="885bd-110">Чтобы получить объект **ивмдвддривеколлектион** , используйте свойство [**Ивмвиртуалмачине::D вдромдривес**](ivmvirtualmachine-dvdromdrives.md) .</span><span class="sxs-lookup"><span data-stu-id="885bd-110">To obtain an **IVMDVDDriveCollection** object, use the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="885bd-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="885bd-111">Members</span></span>

<span data-ttu-id="885bd-112">Интерфейс **ивмдвддривеколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="885bd-112">The **IVMDVDDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="885bd-113">**Ивмдвддривеколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="885bd-113">**IVMDVDDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="885bd-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="885bd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="885bd-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="885bd-115">Properties</span></span>

<span data-ttu-id="885bd-116">Интерфейс **ивмдвддривеколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="885bd-116">The **IVMDVDDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="885bd-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="885bd-117">Property</span></span>                                                       | <span data-ttu-id="885bd-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="885bd-118">Access type</span></span>          | <span data-ttu-id="885bd-119">Описание</span><span class="sxs-lookup"><span data-stu-id="885bd-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="885bd-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="885bd-120">**\_NewEnum**</span></span>](ivmdvddrivecollection--newenum.md)<br/> | <span data-ttu-id="885bd-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="885bd-121">Read-only</span></span><br/> | <span data-ttu-id="885bd-122">Перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="885bd-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="885bd-123">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="885bd-123">**Count**</span></span>](ivmdvddrivecollection-count.md)<br/>        | <span data-ttu-id="885bd-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="885bd-124">Read-only</span></span><br/> | <span data-ttu-id="885bd-125">Число дисководов компакт-дисков и дисков DVD в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="885bd-125">The number of CD and DVD drives in this collection.</span></span><br/>                 |
| [<span data-ttu-id="885bd-126">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="885bd-126">**Item**</span></span>](ivmdvddrivecollection-item.md)<br/>          | <span data-ttu-id="885bd-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="885bd-127">Read-only</span></span><br/> | <span data-ttu-id="885bd-128">Объект CD или DVD-дисковода, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="885bd-128">The CD or DVD drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="885bd-129">Требования</span><span class="sxs-lookup"><span data-stu-id="885bd-129">Requirements</span></span>



| <span data-ttu-id="885bd-130">Требование</span><span class="sxs-lookup"><span data-stu-id="885bd-130">Requirement</span></span> | <span data-ttu-id="885bd-131">Значение</span><span class="sxs-lookup"><span data-stu-id="885bd-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="885bd-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="885bd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="885bd-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="885bd-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="885bd-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="885bd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="885bd-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="885bd-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="885bd-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="885bd-136">End of client support</span></span><br/>    | <span data-ttu-id="885bd-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="885bd-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="885bd-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="885bd-138">Product</span></span><br/>                  | <span data-ttu-id="885bd-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="885bd-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="885bd-140">Header</span><span class="sxs-lookup"><span data-stu-id="885bd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="885bd-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="885bd-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="885bd-142">IID</span><span class="sxs-lookup"><span data-stu-id="885bd-142">IID</span></span><br/>                      | <span data-ttu-id="885bd-143">IID \_ ивмдвддривеколлектион определен как bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="885bd-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="885bd-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="885bd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="885bd-145">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="885bd-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="885bd-146">**Ивмвиртуалмачине::D Вдромдривес**</span><span class="sxs-lookup"><span data-stu-id="885bd-146">**IVMVirtualMachine::DVDROMDrives**</span></span>](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

