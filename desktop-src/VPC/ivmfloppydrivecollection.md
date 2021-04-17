---
title: Интерфейс Ивмфлоппидривеколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию дисководов гибких дисков в виртуальной машине.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Виртуальный ПК с интерфейсом Ивмфлоппидривеколлектион
- Ивмфлоппидривеколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 664937a08bf7576c35b94a162fb5b6f4a7400f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416113"
---
# <a name="ivmfloppydrivecollection-interface"></a><span data-ttu-id="4c01c-105">Интерфейс Ивмфлоппидривеколлектион</span><span class="sxs-lookup"><span data-stu-id="4c01c-105">IVMFloppyDriveCollection interface</span></span>

<span data-ttu-id="4c01c-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4c01c-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4c01c-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4c01c-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4c01c-108">Определяет коллекцию дисководов гибких дисков в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4c01c-108">Defines a collection of floppy drives within the virtual machine.</span></span> <span data-ttu-id="4c01c-109">Чтобы получить объект **ивмфлоппидривеколлектион** , используйте свойство [**Ивмвиртуалмачине:: флоппидривес**](ivmvirtualmachine-floppydrives.md) .</span><span class="sxs-lookup"><span data-stu-id="4c01c-109">To obtain an **IVMFloppyDriveCollection** object, use the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="4c01c-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="4c01c-110">Members</span></span>

<span data-ttu-id="4c01c-111">Интерфейс **ивмфлоппидривеколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4c01c-111">The **IVMFloppyDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4c01c-112">**Ивмфлоппидривеколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4c01c-112">**IVMFloppyDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="4c01c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4c01c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c01c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4c01c-114">Properties</span></span>

<span data-ttu-id="4c01c-115">Интерфейс **ивмфлоппидривеколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4c01c-115">The **IVMFloppyDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="4c01c-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="4c01c-116">Property</span></span>                                                          | <span data-ttu-id="4c01c-117">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="4c01c-117">Access type</span></span>          | <span data-ttu-id="4c01c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4c01c-118">Description</span></span>                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="4c01c-119">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="4c01c-119">**\_NewEnum**</span></span>](ivmfloppydrivecollection--newenum.md)<br/> | <span data-ttu-id="4c01c-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c01c-120">Read-only</span></span><br/> | <span data-ttu-id="4c01c-121">Перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="4c01c-121">An enumerator for the collection.</span></span><br/>                                |
| [<span data-ttu-id="4c01c-122">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="4c01c-122">**Count**</span></span>](ivmfloppydrivecollection-count.md)<br/>        | <span data-ttu-id="4c01c-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c01c-123">Read-only</span></span><br/> | <span data-ttu-id="4c01c-124">Число дисководов гибких дисков в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="4c01c-124">The number of floppy drives in this collection.</span></span><br/>                  |
| [<span data-ttu-id="4c01c-125">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4c01c-125">**Item**</span></span>](ivmfloppydrivecollection-item.md)<br/>          | <span data-ttu-id="4c01c-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c01c-126">Read-only</span></span><br/> | <span data-ttu-id="4c01c-127">Объект дисковода гибких дисков, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="4c01c-127">The floppy drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4c01c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="4c01c-128">Requirements</span></span>



| <span data-ttu-id="4c01c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="4c01c-129">Requirement</span></span> | <span data-ttu-id="4c01c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="4c01c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c01c-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c01c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4c01c-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4c01c-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c01c-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c01c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4c01c-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4c01c-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4c01c-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4c01c-135">End of client support</span></span><br/>    | <span data-ttu-id="4c01c-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c01c-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4c01c-137">Продукт</span><span class="sxs-lookup"><span data-stu-id="4c01c-137">Product</span></span><br/>                  | <span data-ttu-id="4c01c-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4c01c-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4c01c-139">Header</span><span class="sxs-lookup"><span data-stu-id="4c01c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c01c-140"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c01c-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4c01c-141">IID</span><span class="sxs-lookup"><span data-stu-id="4c01c-141">IID</span></span><br/>                      | <span data-ttu-id="4c01c-142">IID \_ ивмфлоппидривеколлектион определен как 8ba70a25-F698-4ee5-85CE-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="4c01c-142">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="4c01c-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c01c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c01c-144">**ивмфлоппидриве**</span><span class="sxs-lookup"><span data-stu-id="4c01c-144">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="4c01c-145">**Ивмвиртуалмачине:: Флоппидривес**</span><span class="sxs-lookup"><span data-stu-id="4c01c-145">**IVMVirtualMachine::FloppyDrives**</span></span>](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

