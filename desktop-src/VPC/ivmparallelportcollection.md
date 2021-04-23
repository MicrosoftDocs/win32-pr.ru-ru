---
title: Интерфейс Ивмпараллелпортколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию параллельных портов в виртуальной машине. Чтобы получить объект Ивмпараллелпортколлектион, используйте свойство Параллелпортс Ивмвиртуалмачине.
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- Виртуальный ПК с интерфейсом Ивмпараллелпортколлектион
- Ивмпараллелпортколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137479"
---
# <a name="ivmparallelportcollection-interface"></a><span data-ttu-id="8f755-106">Интерфейс Ивмпараллелпортколлектион</span><span class="sxs-lookup"><span data-stu-id="8f755-106">IVMParallelPortCollection interface</span></span>

<span data-ttu-id="8f755-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8f755-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8f755-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8f755-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8f755-109">Определяет коллекцию параллельных портов в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="8f755-109">Defines the collection of parallel ports within the virtual machine.</span></span> <span data-ttu-id="8f755-110">Чтобы получить объект **ивмпараллелпортколлектион** , используйте свойство [**Ивмвиртуалмачине::P араллелпортс**](ivmvirtualmachine-parallelports.md) .</span><span class="sxs-lookup"><span data-stu-id="8f755-110">To obtain an **IVMParallelPortCollection** object, use the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="8f755-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="8f755-111">Members</span></span>

<span data-ttu-id="8f755-112">Интерфейс **ивмпараллелпортколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8f755-112">The **IVMParallelPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8f755-113">**Ивмпараллелпортколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8f755-113">**IVMParallelPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="8f755-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="8f755-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f755-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="8f755-115">Properties</span></span>

<span data-ttu-id="8f755-116">Интерфейс **ивмпараллелпортколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8f755-116">The **IVMParallelPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="8f755-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="8f755-117">Property</span></span>                                                           | <span data-ttu-id="8f755-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="8f755-118">Access type</span></span>          | <span data-ttu-id="8f755-119">Описание</span><span class="sxs-lookup"><span data-stu-id="8f755-119">Description</span></span>                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="8f755-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="8f755-120">**\_NewEnum**</span></span>](ivmparallelportcollection--newenum.md)<br/> | <span data-ttu-id="8f755-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8f755-121">Read-only</span></span><br/> | <span data-ttu-id="8f755-122">Перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="8f755-122">An enumerator for the collection.</span></span><br/>                                 |
| [<span data-ttu-id="8f755-123">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="8f755-123">**Count**</span></span>](ivmparallelportcollection-count.md)<br/>        | <span data-ttu-id="8f755-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8f755-124">Read-only</span></span><br/> | <span data-ttu-id="8f755-125">Число параллельных портов в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="8f755-125">The number of parallel ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="8f755-126">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8f755-126">**Item**</span></span>](ivmparallelportcollection-item.md)<br/>          | <span data-ttu-id="8f755-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8f755-127">Read-only</span></span><br/> | <span data-ttu-id="8f755-128">Объект параллельного порта, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="8f755-128">The parallel port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8f755-129">Требования</span><span class="sxs-lookup"><span data-stu-id="8f755-129">Requirements</span></span>



| <span data-ttu-id="8f755-130">Требование</span><span class="sxs-lookup"><span data-stu-id="8f755-130">Requirement</span></span> | <span data-ttu-id="8f755-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8f755-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f755-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f755-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8f755-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8f755-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f755-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f755-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8f755-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8f755-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8f755-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8f755-136">End of client support</span></span><br/>    | <span data-ttu-id="8f755-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8f755-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8f755-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="8f755-138">Product</span></span><br/>                  | <span data-ttu-id="8f755-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8f755-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8f755-140">Header</span><span class="sxs-lookup"><span data-stu-id="8f755-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f755-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f755-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8f755-142">IID</span><span class="sxs-lookup"><span data-stu-id="8f755-142">IID</span></span><br/>                      | <span data-ttu-id="8f755-143">IID \_ ивмпараллелпортколлектион определен как 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="8f755-143">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8f755-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f755-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f755-145">**ивмпараллелпорт**</span><span class="sxs-lookup"><span data-stu-id="8f755-145">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="8f755-146">**Ивмвиртуалмачине::P Араллелпортс**</span><span class="sxs-lookup"><span data-stu-id="8f755-146">**IVMVirtualMachine::ParallelPorts**</span></span>](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

