---
title: Интерфейс Ивмдисплай (Впккоминтерфацес. h)
description: Управляет параметрами экрана виртуальной машины. Интерфейс Ивмдисплай для виртуальной машины можно получить с помощью свойства Ивмвиртуалмачине дисплея.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Виртуальный ПК с интерфейсом Ивмдисплай
- Ивмдисплай интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989034"
---
# <a name="ivmdisplay-interface"></a><span data-ttu-id="39bad-106">Интерфейс Ивмдисплай</span><span class="sxs-lookup"><span data-stu-id="39bad-106">IVMDisplay interface</span></span>

<span data-ttu-id="39bad-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="39bad-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="39bad-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="39bad-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="39bad-109">Управляет параметрами экрана виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="39bad-109">Controls the display settings of a virtual machine.</span></span> <span data-ttu-id="39bad-110">Интерфейс **ивмдисплай** для виртуальной машины можно получить с помощью свойства [**ивмвиртуалмачине::D Play**](ivmvirtualmachine-display.md) .</span><span class="sxs-lookup"><span data-stu-id="39bad-110">The **IVMDisplay** interface for a virtual machine can be retrieved using the [**IVMVirtualMachine::Display**](ivmvirtualmachine-display.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="39bad-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="39bad-111">Members</span></span>

<span data-ttu-id="39bad-112">Интерфейс **ивмдисплай** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="39bad-112">The **IVMDisplay** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="39bad-113">**Ивмдисплай** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="39bad-113">**IVMDisplay** also has these types of members:</span></span>

-   [<span data-ttu-id="39bad-114">Методы</span><span class="sxs-lookup"><span data-stu-id="39bad-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="39bad-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="39bad-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="39bad-116">Методы</span><span class="sxs-lookup"><span data-stu-id="39bad-116">Methods</span></span>

<span data-ttu-id="39bad-117">Интерфейс **ивмдисплай** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="39bad-117">The **IVMDisplay** interface has these methods.</span></span>



| <span data-ttu-id="39bad-118">Метод</span><span class="sxs-lookup"><span data-stu-id="39bad-118">Method</span></span>                                                       | <span data-ttu-id="39bad-119">Описание</span><span class="sxs-lookup"><span data-stu-id="39bad-119">Description</span></span>                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39bad-120">**\_GenerateThumbnail**</span><span class="sxs-lookup"><span data-stu-id="39bad-120">**\_GenerateThumbnail**</span></span>](ivmdisplay--generatethumbnail.md) | <span data-ttu-id="39bad-121">Извлекает массив пикселей, представляющий эскиз изображения экрана виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="39bad-121">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="39bad-122">**сетдименсионс**</span><span class="sxs-lookup"><span data-stu-id="39bad-122">**SetDimensions**</span></span>](ivmdisplay-setdimensions.md)            | <span data-ttu-id="39bad-123">Задает высоту и ширину дисплея виртуальной машины в пикселях.</span><span class="sxs-lookup"><span data-stu-id="39bad-123">Sets the height and width of the virtual machine's display, in pixels.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="39bad-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="39bad-124">Properties</span></span>

<span data-ttu-id="39bad-125">Интерфейс **ивмдисплай** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="39bad-125">The **IVMDisplay** interface has these properties.</span></span>



| <span data-ttu-id="39bad-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="39bad-126">Property</span></span>                                             | <span data-ttu-id="39bad-127">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="39bad-127">Access type</span></span>          | <span data-ttu-id="39bad-128">Описание</span><span class="sxs-lookup"><span data-stu-id="39bad-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39bad-129">**канресизе**</span><span class="sxs-lookup"><span data-stu-id="39bad-129">**CanResize**</span></span>](ivmdisplay-canresize.md)<br/> | <span data-ttu-id="39bad-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="39bad-130">Read-only</span></span><br/> | <span data-ttu-id="39bad-131">Указывает, допускает ли гостевое изменение разрешение изменений.</span><span class="sxs-lookup"><span data-stu-id="39bad-131">Indicates whether the Guest allows resolution changes.</span></span><br/>                             |
| [<span data-ttu-id="39bad-132">**Высота**</span><span class="sxs-lookup"><span data-stu-id="39bad-132">**Height**</span></span>](ivmdisplay-height.md)<br/>       | <span data-ttu-id="39bad-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="39bad-133">Read-only</span></span><br/> | <span data-ttu-id="39bad-134">Высота дисплея виртуальной машины в пикселях.</span><span class="sxs-lookup"><span data-stu-id="39bad-134">The height of the virtual machine's display, in pixels.</span></span><br/>                            |
| [<span data-ttu-id="39bad-135">**Thumbnail**</span><span class="sxs-lookup"><span data-stu-id="39bad-135">**Thumbnail**</span></span>](ivmdisplay-thumbnail.md)<br/> | <span data-ttu-id="39bad-136">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="39bad-136">Read-only</span></span><br/> | <span data-ttu-id="39bad-137">Массив пикселей, представляющий эскиз изображения экрана виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="39bad-137">An array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="39bad-138">**видеомоде**</span><span class="sxs-lookup"><span data-stu-id="39bad-138">**VideoMode**</span></span>](ivmdisplay-videomode.md)<br/> | <span data-ttu-id="39bad-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="39bad-139">Read-only</span></span><br/> | <span data-ttu-id="39bad-140">Текущий режим видео (текст, VGA, SVGA и т. д.).</span><span class="sxs-lookup"><span data-stu-id="39bad-140">The current video mode (Text, VGA, SVGA, and so on).</span></span><br/>                               |
| [<span data-ttu-id="39bad-141">**Ширина**</span><span class="sxs-lookup"><span data-stu-id="39bad-141">**Width**</span></span>](ivmdisplay-width.md)<br/>         | <span data-ttu-id="39bad-142">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="39bad-142">Read-only</span></span><br/> | <span data-ttu-id="39bad-143">Ширина дисплея виртуальной машины в пикселях.</span><span class="sxs-lookup"><span data-stu-id="39bad-143">The width of the virtual machine's display, in pixels.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="39bad-144">Требования</span><span class="sxs-lookup"><span data-stu-id="39bad-144">Requirements</span></span>



| <span data-ttu-id="39bad-145">Требование</span><span class="sxs-lookup"><span data-stu-id="39bad-145">Requirement</span></span> | <span data-ttu-id="39bad-146">Значение</span><span class="sxs-lookup"><span data-stu-id="39bad-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39bad-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39bad-147">Minimum supported client</span></span><br/> | <span data-ttu-id="39bad-148">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="39bad-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39bad-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39bad-149">Minimum supported server</span></span><br/> | <span data-ttu-id="39bad-150">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="39bad-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="39bad-151">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="39bad-151">End of client support</span></span><br/>    | <span data-ttu-id="39bad-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39bad-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39bad-153">Продукт</span><span class="sxs-lookup"><span data-stu-id="39bad-153">Product</span></span><br/>                  | <span data-ttu-id="39bad-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="39bad-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="39bad-155">Header</span><span class="sxs-lookup"><span data-stu-id="39bad-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="39bad-156"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="39bad-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="39bad-157">IID</span><span class="sxs-lookup"><span data-stu-id="39bad-157">IID</span></span><br/>                      | <span data-ttu-id="39bad-158">IID \_ ивмдисплай определен как 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="39bad-158">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



 

