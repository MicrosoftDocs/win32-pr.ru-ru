---
title: Интерфейс Ивмтаскколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию объектов Task. Чтобы получить объект Ивмтаскколлектион, используйте свойство Tasks Ивмвиртуалпк.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Виртуальный ПК с интерфейсом Ивмтаскколлектион
- Ивмтаскколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415917"
---
# <a name="ivmtaskcollection-interface"></a><span data-ttu-id="be9f0-106">Интерфейс Ивмтаскколлектион</span><span class="sxs-lookup"><span data-stu-id="be9f0-106">IVMTaskCollection interface</span></span>

<span data-ttu-id="be9f0-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="be9f0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="be9f0-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="be9f0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="be9f0-109">Определяет коллекцию объектов Task.</span><span class="sxs-lookup"><span data-stu-id="be9f0-109">Defines the collection of task objects.</span></span> <span data-ttu-id="be9f0-110">Чтобы получить объект **ивмтаскколлектион** , используйте свойство [**Ивмвиртуалпк:: Tasks**](ivmvirtualpc-tasks.md) .</span><span class="sxs-lookup"><span data-stu-id="be9f0-110">To obtain an **IVMTaskCollection** object, use the [**IVMVirtualPC::Tasks**](ivmvirtualpc-tasks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="be9f0-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="be9f0-111">Members</span></span>

<span data-ttu-id="be9f0-112">Интерфейс **ивмтаскколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="be9f0-112">The **IVMTaskCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="be9f0-113">**Ивмтаскколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be9f0-113">**IVMTaskCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="be9f0-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="be9f0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be9f0-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="be9f0-115">Properties</span></span>

<span data-ttu-id="be9f0-116">Интерфейс **ивмтаскколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be9f0-116">The **IVMTaskCollection** interface has these properties.</span></span>



| <span data-ttu-id="be9f0-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="be9f0-117">Property</span></span>                                                   | <span data-ttu-id="be9f0-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="be9f0-118">Access type</span></span>          | <span data-ttu-id="be9f0-119">Описание</span><span class="sxs-lookup"><span data-stu-id="be9f0-119">Description</span></span>                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="be9f0-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="be9f0-120">**\_NewEnum**</span></span>](ivmtaskcollection--newenum.md)<br/> | <span data-ttu-id="be9f0-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="be9f0-121">Read-only</span></span><br/> | <span data-ttu-id="be9f0-122">Перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="be9f0-122">An enumerator for the collection.</span></span><br/>                        |
| [<span data-ttu-id="be9f0-123">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="be9f0-123">**Count**</span></span>](ivmtaskcollection-count.md)<br/>        | <span data-ttu-id="be9f0-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="be9f0-124">Read-only</span></span><br/> | <span data-ttu-id="be9f0-125">Число задач в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="be9f0-125">The number of tasks in this collection.</span></span><br/>                  |
| [<span data-ttu-id="be9f0-126">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="be9f0-126">**Item**</span></span>](ivmtaskcollection-item.md)<br/>          | <span data-ttu-id="be9f0-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="be9f0-127">Read-only</span></span><br/> | <span data-ttu-id="be9f0-128">Объект Task, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="be9f0-128">The task object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be9f0-129">Требования</span><span class="sxs-lookup"><span data-stu-id="be9f0-129">Requirements</span></span>



| <span data-ttu-id="be9f0-130">Требование</span><span class="sxs-lookup"><span data-stu-id="be9f0-130">Requirement</span></span> | <span data-ttu-id="be9f0-131">Значение</span><span class="sxs-lookup"><span data-stu-id="be9f0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="be9f0-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be9f0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="be9f0-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="be9f0-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="be9f0-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be9f0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="be9f0-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="be9f0-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="be9f0-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="be9f0-136">End of client support</span></span><br/>    | <span data-ttu-id="be9f0-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="be9f0-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="be9f0-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="be9f0-138">Product</span></span><br/>                  | <span data-ttu-id="be9f0-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="be9f0-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="be9f0-140">Header</span><span class="sxs-lookup"><span data-stu-id="be9f0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="be9f0-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="be9f0-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="be9f0-142">IID</span><span class="sxs-lookup"><span data-stu-id="be9f0-142">IID</span></span><br/>                      | <span data-ttu-id="be9f0-143">IID \_ ивмтаскколлектион определен как 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="be9f0-143">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="be9f0-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be9f0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9f0-145">**ивмтаск**</span><span class="sxs-lookup"><span data-stu-id="be9f0-145">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="be9f0-146">**Ивмвиртуалпк:: Tasks**</span><span class="sxs-lookup"><span data-stu-id="be9f0-146">**IVMVirtualPC::Tasks**</span></span>](ivmvirtualpc-tasks.md)
</dt> </dl>

 

