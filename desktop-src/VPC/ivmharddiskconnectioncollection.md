---
title: Интерфейс Ивмхарддискконнектионколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию подключений к жестким дискам в пределах виртуальной машины. Чтобы получить объект Ивмхарддискконнектионколлектион, используйте свойство Харддискконнектионс Ивмвиртуалмачине.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Виртуальный ПК с интерфейсом Ивмхарддискконнектионколлектион
- Ивмхарддискконнектионколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488925"
---
# <a name="ivmharddiskconnectioncollection-interface"></a><span data-ttu-id="b990b-106">Интерфейс Ивмхарддискконнектионколлектион</span><span class="sxs-lookup"><span data-stu-id="b990b-106">IVMHardDiskConnectionCollection interface</span></span>

<span data-ttu-id="b990b-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b990b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b990b-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b990b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b990b-109">Определяет коллекцию подключений к жестким дискам в пределах виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b990b-109">Defines the collection of hard disk connections within the virtual machine.</span></span> <span data-ttu-id="b990b-110">Чтобы получить объект **ивмхарддискконнектионколлектион** , используйте свойство [**Ивмвиртуалмачине:: харддискконнектионс**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="b990b-110">To obtain an **IVMHardDiskConnectionCollection** object, use the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="b990b-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="b990b-111">Members</span></span>

<span data-ttu-id="b990b-112">Интерфейс **ивмхарддискконнектионколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b990b-112">The **IVMHardDiskConnectionCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b990b-113">**Ивмхарддискконнектионколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b990b-113">**IVMHardDiskConnectionCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="b990b-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="b990b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b990b-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="b990b-115">Properties</span></span>

<span data-ttu-id="b990b-116">Интерфейс **ивмхарддискконнектионколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b990b-116">The **IVMHardDiskConnectionCollection** interface has these properties.</span></span>



| <span data-ttu-id="b990b-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="b990b-117">Property</span></span>                                                                 | <span data-ttu-id="b990b-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="b990b-118">Access type</span></span>          | <span data-ttu-id="b990b-119">Описание</span><span class="sxs-lookup"><span data-stu-id="b990b-119">Description</span></span>                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="b990b-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="b990b-120">**\_NewEnum**</span></span>](ivmharddiskconnectioncollection--newenum.md)<br/> | <span data-ttu-id="b990b-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b990b-121">Read-only</span></span><br/> | <span data-ttu-id="b990b-122">Перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="b990b-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="b990b-123">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="b990b-123">**Count**</span></span>](ivmharddiskconnectioncollection-count.md)<br/>        | <span data-ttu-id="b990b-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b990b-124">Read-only</span></span><br/> | <span data-ttu-id="b990b-125">Число подключений к жестким дискам в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="b990b-125">The number of hard disk connections in this collection.</span></span><br/>                  |
| [<span data-ttu-id="b990b-126">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b990b-126">**Item**</span></span>](ivmharddiskconnectioncollection-item.md)<br/>          | <span data-ttu-id="b990b-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b990b-127">Read-only</span></span><br/> | <span data-ttu-id="b990b-128">Объект подключения к жесткому диску, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="b990b-128">The hard disk connection object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b990b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="b990b-129">Requirements</span></span>



| <span data-ttu-id="b990b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="b990b-130">Requirement</span></span> | <span data-ttu-id="b990b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b990b-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b990b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b990b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b990b-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b990b-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="b990b-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b990b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b990b-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b990b-135">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="b990b-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b990b-136">End of client support</span></span><br/>    | <span data-ttu-id="b990b-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b990b-137">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="b990b-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="b990b-138">Product</span></span><br/>                  | <span data-ttu-id="b990b-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b990b-139">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="b990b-140">Header</span><span class="sxs-lookup"><span data-stu-id="b990b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b990b-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b990b-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="b990b-142">IID</span><span class="sxs-lookup"><span data-stu-id="b990b-142">IID</span></span><br/>                      | <span data-ttu-id="b990b-143">IID \_ ивмхарддискконнектионколлектион определен как b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="b990b-143">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b990b-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b990b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b990b-145">**ивмхарддискконнектион**</span><span class="sxs-lookup"><span data-stu-id="b990b-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="b990b-146">**Ивмвиртуалмачине:: Харддискконнектионс**</span><span class="sxs-lookup"><span data-stu-id="b990b-146">**IVMVirtualMachine::HardDiskConnections**</span></span>](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

