---
title: Интерфейс Ивмпараллелпорт (Впккоминтерфацес. h)
description: Определяет параллельный порт внутри виртуальной машины.
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- Виртуальный ПК с интерфейсом Ивмпараллелпорт
- Ивмпараллелпорт интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691946"
---
# <a name="ivmparallelport-interface"></a><span data-ttu-id="8a629-105">Интерфейс Ивмпараллелпорт</span><span class="sxs-lookup"><span data-stu-id="8a629-105">IVMParallelPort interface</span></span>

<span data-ttu-id="8a629-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8a629-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8a629-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8a629-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8a629-108">Определяет параллельный порт внутри виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8a629-108">Defines a parallel port inside a virtual machine.</span></span> <span data-ttu-id="8a629-109">Этот интерфейс позволяет настраивать параллельные порты внутри виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8a629-109">This interface allows you to configure parallel ports inside a virtual machine.</span></span> <span data-ttu-id="8a629-110">Объект **ивмпараллелпорт** можно получить из объекта [**ивмпараллелпортколлектион**](ivmparallelportcollection.md) , возвращенного из свойства [**ивмвиртуалмачине::P араллелпортс**](ivmvirtualmachine-parallelports.md) .</span><span class="sxs-lookup"><span data-stu-id="8a629-110">You can retrieve an **IVMParallelPort** object from the [**IVMParallelPortCollection**](ivmparallelportcollection.md) object returned from the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="8a629-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="8a629-111">Members</span></span>

<span data-ttu-id="8a629-112">Интерфейс **ивмпараллелпорт** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8a629-112">The **IVMParallelPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8a629-113">**Ивмпараллелпорт** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8a629-113">**IVMParallelPort** also has these types of members:</span></span>

-   [<span data-ttu-id="8a629-114">Методы</span><span class="sxs-lookup"><span data-stu-id="8a629-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="8a629-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="8a629-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8a629-116">Методы</span><span class="sxs-lookup"><span data-stu-id="8a629-116">Methods</span></span>

<span data-ttu-id="8a629-117">Интерфейс **ивмпараллелпорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8a629-117">The **IVMParallelPort** interface has these methods.</span></span>



| <span data-ttu-id="8a629-118">Метод</span><span class="sxs-lookup"><span data-stu-id="8a629-118">Method</span></span>                              | <span data-ttu-id="8a629-119">Описание</span><span class="sxs-lookup"><span data-stu-id="8a629-119">Description</span></span>                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="8a629-120">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="8a629-120">**\_ID**</span></span>](ivmparallelport--id.md) | <span data-ttu-id="8a629-121">Извлекает внутренний идентификатор параллельного порта.</span><span class="sxs-lookup"><span data-stu-id="8a629-121">Retrieves the internal identifier of the parallel port.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8a629-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="8a629-122">Properties</span></span>

<span data-ttu-id="8a629-123">Интерфейс **ивмпараллелпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8a629-123">The **IVMParallelPort** interface has these properties.</span></span>



| <span data-ttu-id="8a629-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="8a629-124">Property</span></span>                                        | <span data-ttu-id="8a629-125">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="8a629-125">Access type</span></span>           | <span data-ttu-id="8a629-126">Описание</span><span class="sxs-lookup"><span data-stu-id="8a629-126">Description</span></span>                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [<span data-ttu-id="8a629-127">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8a629-127">**Name**</span></span>](ivmparallelport-name.md)<br/> | <span data-ttu-id="8a629-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="8a629-128">Read/write</span></span><br/> | <span data-ttu-id="8a629-129">Имя параллельного порта.</span><span class="sxs-lookup"><span data-stu-id="8a629-129">The name of the parallel port.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8a629-130">Требования</span><span class="sxs-lookup"><span data-stu-id="8a629-130">Requirements</span></span>



| <span data-ttu-id="8a629-131">Требование</span><span class="sxs-lookup"><span data-stu-id="8a629-131">Requirement</span></span> | <span data-ttu-id="8a629-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8a629-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a629-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a629-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8a629-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8a629-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a629-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a629-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8a629-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8a629-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8a629-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8a629-137">End of client support</span></span><br/>    | <span data-ttu-id="8a629-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a629-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8a629-139">Продукт</span><span class="sxs-lookup"><span data-stu-id="8a629-139">Product</span></span><br/>                  | <span data-ttu-id="8a629-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8a629-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8a629-141">Header</span><span class="sxs-lookup"><span data-stu-id="8a629-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a629-142"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a629-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8a629-143">IID</span><span class="sxs-lookup"><span data-stu-id="8a629-143">IID</span></span><br/>                      | <span data-ttu-id="8a629-144">IID \_ ивмпараллелпорт определен как 097beecb-0a02-474f-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="8a629-144">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



 

