---
title: Интерфейс Ивммаусе (Впккоминтерфацес. h)
description: Управляет устройством мыши в виртуальной машине.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- Виртуальный ПК с интерфейсом Ивммаусе
- Ивммаусе интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7041b8a28b924ffedc8ff23edd2b04afdaa78be2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892501"
---
# <a name="ivmmouse-interface"></a><span data-ttu-id="e7555-105">Интерфейс Ивммаусе</span><span class="sxs-lookup"><span data-stu-id="e7555-105">IVMMouse interface</span></span>

<span data-ttu-id="e7555-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e7555-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e7555-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e7555-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e7555-108">Управляет устройством мыши в пределах виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e7555-108">Controls the mouse device within a virtual machine (VM).</span></span> <span data-ttu-id="e7555-109">**Ивммаусе** для виртуальной машины можно получить с помощью свойства [**Ивмвиртуалмачине:: Mouse**](ivmvirtualmachine-mouse.md) .</span><span class="sxs-lookup"><span data-stu-id="e7555-109">The **IVMMouse** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Mouse**](ivmvirtualmachine-mouse.md) property.</span></span> <span data-ttu-id="e7555-110">Координаты устройства мыши можно представить в абсолютных координатах или в разностных координатах.</span><span class="sxs-lookup"><span data-stu-id="e7555-110">Coordinates for the mouse device can be represented either in absolute coordinates or in delta coordinates.</span></span> <span data-ttu-id="e7555-111">Используйте свойство [**усингабсолутекурдинатес**](ivmmouse-usingabsolutecoordinates.md) , чтобы различать два метода представления координат.</span><span class="sxs-lookup"><span data-stu-id="e7555-111">Use the [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) property to distinguish between the two methods of coordinate representation.</span></span> <span data-ttu-id="e7555-112">Обратите внимание, что получение текущей позиции курсора и использование абсолютных координат поддерживаются только в том случае, если на гостевой операционной системе установлены компоненты интеграции.</span><span class="sxs-lookup"><span data-stu-id="e7555-112">Note that retrieving the current cursor position and the use of absolute coordinates are only supported if the guest operating system has the integration components installed.</span></span>

## <a name="members"></a><span data-ttu-id="e7555-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="e7555-113">Members</span></span>

<span data-ttu-id="e7555-114">Интерфейс **ивммаусе** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="e7555-114">The **IVMMouse** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e7555-115">**Ивммаусе** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e7555-115">**IVMMouse** also has these types of members:</span></span>

-   [<span data-ttu-id="e7555-116">Методы</span><span class="sxs-lookup"><span data-stu-id="e7555-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="e7555-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7555-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e7555-118">Методы</span><span class="sxs-lookup"><span data-stu-id="e7555-118">Methods</span></span>

<span data-ttu-id="e7555-119">Интерфейс **ивммаусе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e7555-119">The **IVMMouse** interface has these methods.</span></span>



| <span data-ttu-id="e7555-120">Метод</span><span class="sxs-lookup"><span data-stu-id="e7555-120">Method</span></span>                                  | <span data-ttu-id="e7555-121">Описание</span><span class="sxs-lookup"><span data-stu-id="e7555-121">Description</span></span>                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="e7555-122">**Щелкните**</span><span class="sxs-lookup"><span data-stu-id="e7555-122">**Click**</span></span>](ivmmouse-click.md)         | <span data-ttu-id="e7555-123">Имитирует нажатие кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="e7555-123">Simulates a mouse button click.</span></span><br/>                                         |
| [<span data-ttu-id="e7555-124">**Кнопка**</span><span class="sxs-lookup"><span data-stu-id="e7555-124">**GetButton**</span></span>](ivmmouse-getbutton.md) | <span data-ttu-id="e7555-125">Извлекает текущее состояние (вверх или вниз) указанной кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="e7555-125">Retrieves the current state (up or down) of the specified mouse button.</span></span><br/> |
| [<span data-ttu-id="e7555-126">**сетбуттон**</span><span class="sxs-lookup"><span data-stu-id="e7555-126">**SetButton**</span></span>](ivmmouse-setbutton.md) | <span data-ttu-id="e7555-127">Задает текущее состояние (вверх или вниз) указанной кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="e7555-127">Sets the current state (up or down) of the specified mouse button.</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="e7555-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7555-128">Properties</span></span>

<span data-ttu-id="e7555-129">Интерфейс **ивммаусе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e7555-129">The **IVMMouse** interface has these properties.</span></span>



| <span data-ttu-id="e7555-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="e7555-130">Property</span></span>                                                                         | <span data-ttu-id="e7555-131">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="e7555-131">Access type</span></span>           | <span data-ttu-id="e7555-132">Описание</span><span class="sxs-lookup"><span data-stu-id="e7555-132">Description</span></span>                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7555-133">**хоризонталпоситион**</span><span class="sxs-lookup"><span data-stu-id="e7555-133">**HorizontalPosition**</span></span>](ivmmouse-horizontalposition.md)<br/>             | <span data-ttu-id="e7555-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e7555-134">Read/write</span></span><br/> | <span data-ttu-id="e7555-135">Абсолютная координата по оси x мыши.</span><span class="sxs-lookup"><span data-stu-id="e7555-135">The absolute x-coordinate of the mouse.</span></span><br/>                                         |
| [<span data-ttu-id="e7555-136">**скроллвхилпоситион**</span><span class="sxs-lookup"><span data-stu-id="e7555-136">**ScrollWheelPosition**</span></span>](ivmmouse-scrollwheelposition.md)<br/>           | <span data-ttu-id="e7555-137">Только на запись</span><span class="sxs-lookup"><span data-stu-id="e7555-137">Write-only</span></span><br/> | <span data-ttu-id="e7555-138">Z-координата мыши (относительная).</span><span class="sxs-lookup"><span data-stu-id="e7555-138">The z-coordinate of the mouse (relative only).</span></span><br/>                                  |
| [<span data-ttu-id="e7555-139">**усингабсолутекурдинатес**</span><span class="sxs-lookup"><span data-stu-id="e7555-139">**UsingAbsoluteCoordinates**</span></span>](ivmmouse-usingabsolutecoordinates.md)<br/> | <span data-ttu-id="e7555-140">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e7555-140">Read/write</span></span><br/> | <span data-ttu-id="e7555-141">Указывает, представляют ли координаты мыши абсолютные или относительные координаты.</span><span class="sxs-lookup"><span data-stu-id="e7555-141">Indicates whether mouse coordinates represent absolute or relative coordinates.</span></span><br/> |
| [<span data-ttu-id="e7555-142">**вертикалпоситион**</span><span class="sxs-lookup"><span data-stu-id="e7555-142">**VerticalPosition**</span></span>](ivmmouse-verticalposition.md)<br/>                 | <span data-ttu-id="e7555-143">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e7555-143">Read/write</span></span><br/> | <span data-ttu-id="e7555-144">Абсолютная координата y мыши.</span><span class="sxs-lookup"><span data-stu-id="e7555-144">The absolute y-coordinate of the mouse.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="e7555-145">Требования</span><span class="sxs-lookup"><span data-stu-id="e7555-145">Requirements</span></span>



| <span data-ttu-id="e7555-146">Требование</span><span class="sxs-lookup"><span data-stu-id="e7555-146">Requirement</span></span> | <span data-ttu-id="e7555-147">Значение</span><span class="sxs-lookup"><span data-stu-id="e7555-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7555-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7555-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e7555-149">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e7555-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7555-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7555-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e7555-151">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e7555-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e7555-152">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e7555-152">End of client support</span></span><br/>    | <span data-ttu-id="e7555-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7555-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e7555-154">Продукт</span><span class="sxs-lookup"><span data-stu-id="e7555-154">Product</span></span><br/>                  | <span data-ttu-id="e7555-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e7555-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e7555-156">Header</span><span class="sxs-lookup"><span data-stu-id="e7555-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7555-157"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7555-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e7555-158">IID</span><span class="sxs-lookup"><span data-stu-id="e7555-158">IID</span></span><br/>                      | <span data-ttu-id="e7555-159">IID \_ ивммаусе определен как ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="e7555-159">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



 

