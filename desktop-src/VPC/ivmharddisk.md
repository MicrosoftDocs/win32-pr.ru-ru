---
title: Интерфейс Ивмхарддиск (Впккоминтерфацес. h)
description: Предоставляет доступ к образу жесткого диска. Доступ к нему можно получить с помощью свойства Ивмхарддискконнектион жесткого диска или метода Ивмвиртуалпк Жесарддиск.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- Виртуальный ПК с интерфейсом Ивмхарддиск
- Ивмхарддиск интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488931"
---
# <a name="ivmharddisk-interface"></a><span data-ttu-id="7fb92-106">Интерфейс Ивмхарддиск</span><span class="sxs-lookup"><span data-stu-id="7fb92-106">IVMHardDisk interface</span></span>

<span data-ttu-id="7fb92-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7fb92-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7fb92-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7fb92-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7fb92-109">Предоставляет доступ к образу жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="7fb92-109">Provides access to a hard disk image.</span></span> <span data-ttu-id="7fb92-110">Доступ к нему можно получить с помощью свойства [**ивмхарддискконнектион:: жесткого**](ivmharddiskconnection-harddisk.md) диска или метода [**Ивмвиртуалпк:: жесарддиск**](ivmvirtualpc-getharddisk.md) .</span><span class="sxs-lookup"><span data-stu-id="7fb92-110">It can be accessed through the [**IVMHardDiskConnection::HardDisk**](ivmharddiskconnection-harddisk.md) property or the [**IVMVirtualPC::GetHardDisk**](ivmvirtualpc-getharddisk.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="7fb92-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="7fb92-111">Members</span></span>

<span data-ttu-id="7fb92-112">Интерфейс **ивмхарддиск** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7fb92-112">The **IVMHardDisk** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="7fb92-113">**Ивмхарддиск** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7fb92-113">**IVMHardDisk** also has these types of members:</span></span>

-   [<span data-ttu-id="7fb92-114">Методы</span><span class="sxs-lookup"><span data-stu-id="7fb92-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="7fb92-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="7fb92-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7fb92-116">Методы</span><span class="sxs-lookup"><span data-stu-id="7fb92-116">Methods</span></span>

<span data-ttu-id="7fb92-117">Интерфейс **ивмхарддиск** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7fb92-117">The **IVMHardDisk** interface has these methods.</span></span>



| <span data-ttu-id="7fb92-118">Метод</span><span class="sxs-lookup"><span data-stu-id="7fb92-118">Method</span></span>                                 | <span data-ttu-id="7fb92-119">Описание</span><span class="sxs-lookup"><span data-stu-id="7fb92-119">Description</span></span>                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fb92-120">**Компактный**</span><span class="sxs-lookup"><span data-stu-id="7fb92-120">**Compact**</span></span>](ivmharddisk-compact.md) | <span data-ttu-id="7fb92-121">Сжимает динамически расширяемый образ виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="7fb92-121">Compacts a dynamically expanding virtual hard disk image.</span></span><br/>                                                                                        |
| [<span data-ttu-id="7fb92-122">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7fb92-122">**Convert**</span></span>](ivmharddisk-convert.md) | <span data-ttu-id="7fb92-123">Преобразует любой виртуальный жесткий диск в динамически расширяемый виртуальный жесткий диск или виртуальный жесткий диск фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="7fb92-123">Converts any virtual hard disk to either a dynamically expanding virtual hard disk or a fixed-size virtual hard disk.</span></span><br/>                            |
| [<span data-ttu-id="7fb92-124">**AutoMerge**</span><span class="sxs-lookup"><span data-stu-id="7fb92-124">**Merge**</span></span>](ivmharddisk-merge.md)     | <span data-ttu-id="7fb92-125">Слияние разностного виртуального жесткого диска с образом его родительского диска.</span><span class="sxs-lookup"><span data-stu-id="7fb92-125">Merges a differencing virtual hard disk with its parent disk image.</span></span><br/>                                                                              |
| [<span data-ttu-id="7fb92-126">**мержето**</span><span class="sxs-lookup"><span data-stu-id="7fb92-126">**MergeTo**</span></span>](ivmharddisk-mergeto.md) | <span data-ttu-id="7fb92-127">Слияние разностного виртуального жесткого диска со всеми его родительскими элементами (вплоть до корневого родительского виртуального жесткого диска и включая его) в новый файл жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="7fb92-127">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7fb92-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="7fb92-128">Properties</span></span>

<span data-ttu-id="7fb92-129">Интерфейс **ивмхарддиск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7fb92-129">The **IVMHardDisk** interface has these properties.</span></span>



| <span data-ttu-id="7fb92-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="7fb92-130">Property</span></span>                                                              | <span data-ttu-id="7fb92-131">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="7fb92-131">Access type</span></span>           | <span data-ttu-id="7fb92-132">Описание</span><span class="sxs-lookup"><span data-stu-id="7fb92-132">Description</span></span>                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fb92-133">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7fb92-133">**File**</span></span>](ivmharddisk-file.md)<br/>                           | <span data-ttu-id="7fb92-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7fb92-134">Read-only</span></span><br/>  | <span data-ttu-id="7fb92-135">Полный путь к файлу виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="7fb92-135">The full path name of the virtual hard disk file.</span></span><br/>                                   |
| [<span data-ttu-id="7fb92-136">**хостфридискспаце**</span><span class="sxs-lookup"><span data-stu-id="7fb92-136">**HostFreeDiskSpace**</span></span>](ivmharddisk-hostfreediskspace.md)<br/> | <span data-ttu-id="7fb92-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7fb92-137">Read-only</span></span><br/>  | <span data-ttu-id="7fb92-138">Объем оставшегося места на диске, доступного на узле для виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="7fb92-138">The amount of remaining disk space available on the host for the virtual hard disk.</span></span><br/> |
| [<span data-ttu-id="7fb92-139">**Parent**</span><span class="sxs-lookup"><span data-stu-id="7fb92-139">**Parent**</span></span>](ivmharddisk-parent.md)<br/>                       | <span data-ttu-id="7fb92-140">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7fb92-140">Read/write</span></span><br/> | <span data-ttu-id="7fb92-141">Родительский объект разностного виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="7fb92-141">The parent of the differencing virtual hard disk.</span></span><br/>                                   |
| [<span data-ttu-id="7fb92-142">**сизеингуест**</span><span class="sxs-lookup"><span data-stu-id="7fb92-142">**SizeInGuest**</span></span>](ivmharddisk-sizeinguest.md)<br/>             | <span data-ttu-id="7fb92-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7fb92-143">Read-only</span></span><br/>  | <span data-ttu-id="7fb92-144">Размер виртуального жесткого диска в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="7fb92-144">The size of the virtual hard disk in the guest operating system.</span></span><br/>                    |
| [<span data-ttu-id="7fb92-145">**сизеонхост**</span><span class="sxs-lookup"><span data-stu-id="7fb92-145">**SizeOnHost**</span></span>](ivmharddisk-sizeonhost.md)<br/>               | <span data-ttu-id="7fb92-146">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7fb92-146">Read-only</span></span><br/>  | <span data-ttu-id="7fb92-147">Размер файла виртуального жесткого диска на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7fb92-147">The size of the virtual hard disk file on the host computer.</span></span><br/>                        |
| [<span data-ttu-id="7fb92-148">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7fb92-148">**Type**</span></span>](ivmharddisk-type.md)<br/>                           | <span data-ttu-id="7fb92-149">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7fb92-149">Read-only</span></span><br/>  | <span data-ttu-id="7fb92-150">Тип виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="7fb92-150">The type of the virtual hard disk.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="7fb92-151">Требования</span><span class="sxs-lookup"><span data-stu-id="7fb92-151">Requirements</span></span>



| <span data-ttu-id="7fb92-152">Требование</span><span class="sxs-lookup"><span data-stu-id="7fb92-152">Requirement</span></span> | <span data-ttu-id="7fb92-153">Значение</span><span class="sxs-lookup"><span data-stu-id="7fb92-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fb92-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fb92-154">Minimum supported client</span></span><br/> | <span data-ttu-id="7fb92-155">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7fb92-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7fb92-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fb92-156">Minimum supported server</span></span><br/> | <span data-ttu-id="7fb92-157">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7fb92-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7fb92-158">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7fb92-158">End of client support</span></span><br/>    | <span data-ttu-id="7fb92-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7fb92-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7fb92-160">Продукт</span><span class="sxs-lookup"><span data-stu-id="7fb92-160">Product</span></span><br/>                  | <span data-ttu-id="7fb92-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7fb92-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7fb92-162">Header</span><span class="sxs-lookup"><span data-stu-id="7fb92-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fb92-163"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fb92-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7fb92-164">IID</span><span class="sxs-lookup"><span data-stu-id="7fb92-164">IID</span></span><br/>                      | <span data-ttu-id="7fb92-165">IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="7fb92-165">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



 

