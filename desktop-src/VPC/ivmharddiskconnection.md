---
title: Интерфейс Ивмхарддискконнектион (Впккоминтерфацес. h)
description: Определяет подключение для жесткого диска в виртуальной машине.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- Виртуальный ПК с интерфейсом Ивмхарддискконнектион
- Ивмхарддискконнектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691870"
---
# <a name="ivmharddiskconnection-interface"></a><span data-ttu-id="d552d-105">Интерфейс Ивмхарддискконнектион</span><span class="sxs-lookup"><span data-stu-id="d552d-105">IVMHardDiskConnection interface</span></span>

<span data-ttu-id="d552d-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d552d-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d552d-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d552d-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d552d-108">Определяет подключение для жесткого диска в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d552d-108">Defines the connection for a hard disk within the virtual machine.</span></span> <span data-ttu-id="d552d-109">Объект **ивмхарддискконнектион** возвращается из метода [**Ивмвиртуалмачине:: AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="d552d-109">An **IVMHardDiskConnection** object is returned from the [**IVMVirtualMachine::AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) method.</span></span> <span data-ttu-id="d552d-110">Можно также получить объект **ивмхарддискконнектион** из объекта [**ивмхарддискконнектионколлектион**](ivmharddiskconnectioncollection.md) , возвращенного из свойства [**ивмвиртуалмачине:: харддискконнектионс**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="d552d-110">You can also retrieve an **IVMHardDiskConnection** object from the [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) object returned from the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="d552d-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="d552d-111">Members</span></span>

<span data-ttu-id="d552d-112">Интерфейс **ивмхарддискконнектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d552d-112">The **IVMHardDiskConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d552d-113">**Ивмхарддискконнектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d552d-113">**IVMHardDiskConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="d552d-114">Методы</span><span class="sxs-lookup"><span data-stu-id="d552d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d552d-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="d552d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d552d-116">Методы</span><span class="sxs-lookup"><span data-stu-id="d552d-116">Methods</span></span>

<span data-ttu-id="d552d-117">Интерфейс **ивмхарддискконнектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d552d-117">The **IVMHardDiskConnection** interface has these methods.</span></span>



| <span data-ttu-id="d552d-118">Метод</span><span class="sxs-lookup"><span data-stu-id="d552d-118">Method</span></span>                                                         | <span data-ttu-id="d552d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="d552d-119">Description</span></span>                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="d552d-120">**сетбуслокатион**</span><span class="sxs-lookup"><span data-stu-id="d552d-120">**SetBusLocation**</span></span>](ivmharddiskconnection-setbuslocation.md) | <span data-ttu-id="d552d-121">Задает расположение шины, к которой подключен этот жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="d552d-121">Sets the bus location to which this hard disk is attached.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d552d-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="d552d-122">Properties</span></span>

<span data-ttu-id="d552d-123">Интерфейс **ивмхарддискконнектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d552d-123">The **IVMHardDiskConnection** interface has these properties.</span></span>



| <span data-ttu-id="d552d-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="d552d-124">Property</span></span>                                                              | <span data-ttu-id="d552d-125">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="d552d-125">Access type</span></span>          | <span data-ttu-id="d552d-126">Описание</span><span class="sxs-lookup"><span data-stu-id="d552d-126">Description</span></span>                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="d552d-127">**буснумбер**</span><span class="sxs-lookup"><span data-stu-id="d552d-127">**BusNumber**</span></span>](ivmharddiskconnection-busnumber.md)<br/>       | <span data-ttu-id="d552d-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d552d-128">Read-only</span></span><br/> | <span data-ttu-id="d552d-129">Номер шины, к которой подключен образ диска.</span><span class="sxs-lookup"><span data-stu-id="d552d-129">The bus number to which the drive image is attached.</span></span><br/>                   |
| [<span data-ttu-id="d552d-130">**девиценумбер**</span><span class="sxs-lookup"><span data-stu-id="d552d-130">**DeviceNumber**</span></span>](ivmharddiskconnection-devicenumber.md)<br/> | <span data-ttu-id="d552d-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d552d-131">Read-only</span></span><br/> | <span data-ttu-id="d552d-132">Номер устройства, к которому подключен образ диска.</span><span class="sxs-lookup"><span data-stu-id="d552d-132">The device number to which the drive image is attached.</span></span><br/>                |
| [<span data-ttu-id="d552d-133">**Отключения**</span><span class="sxs-lookup"><span data-stu-id="d552d-133">**HardDisk**</span></span>](ivmharddiskconnection-harddisk.md)<br/>         | <span data-ttu-id="d552d-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d552d-134">Read-only</span></span><br/> | <span data-ttu-id="d552d-135">Объект жесткого диска, соответствующий этому соединению.</span><span class="sxs-lookup"><span data-stu-id="d552d-135">A hard disk object corresponding to this connection.</span></span><br/>                   |
| [<span data-ttu-id="d552d-136">**ундохарддиск**</span><span class="sxs-lookup"><span data-stu-id="d552d-136">**UndoHardDisk**</span></span>](ivmharddiskconnection-undoharddisk.md)<br/> | <span data-ttu-id="d552d-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d552d-137">Read-only</span></span><br/> | <span data-ttu-id="d552d-138">Объект жесткого диска, соответствующий образу диска отмены этого подключения.</span><span class="sxs-lookup"><span data-stu-id="d552d-138">A hard disk object corresponding to this connection's undo disk image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d552d-139">Требования</span><span class="sxs-lookup"><span data-stu-id="d552d-139">Requirements</span></span>



| <span data-ttu-id="d552d-140">Требование</span><span class="sxs-lookup"><span data-stu-id="d552d-140">Requirement</span></span> | <span data-ttu-id="d552d-141">Значение</span><span class="sxs-lookup"><span data-stu-id="d552d-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d552d-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d552d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d552d-143">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d552d-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d552d-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d552d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d552d-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d552d-145">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d552d-146">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d552d-146">End of client support</span></span><br/>    | <span data-ttu-id="d552d-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d552d-147">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d552d-148">Продукт</span><span class="sxs-lookup"><span data-stu-id="d552d-148">Product</span></span><br/>                  | <span data-ttu-id="d552d-149">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d552d-149">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d552d-150">Header</span><span class="sxs-lookup"><span data-stu-id="d552d-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d552d-151"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d552d-151"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d552d-152">IID</span><span class="sxs-lookup"><span data-stu-id="d552d-152">IID</span></span><br/>                      | <span data-ttu-id="d552d-153">IID \_ ивмхарддискконнектион определен как aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="d552d-153">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



 

