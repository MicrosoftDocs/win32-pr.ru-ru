---
title: Интерфейс Имсрдпдевицеколлектион
description: Представляет коллекцию объектов Device.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпдевицеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдевицеколлектион, описание
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414757"
---
# <a name="imsrdpdevicecollection-interface"></a><span data-ttu-id="baa57-105">Интерфейс Имсрдпдевицеколлектион</span><span class="sxs-lookup"><span data-stu-id="baa57-105">IMsRdpDeviceCollection interface</span></span>

<span data-ttu-id="baa57-106">Представляет коллекцию объектов Device.</span><span class="sxs-lookup"><span data-stu-id="baa57-106">Represents a collection of device objects.</span></span>

## <a name="members"></a><span data-ttu-id="baa57-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="baa57-107">Members</span></span>

<span data-ttu-id="baa57-108">Интерфейс **имсрдпдевицеколлектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="baa57-108">The **IMsRdpDeviceCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="baa57-109">**Имсрдпдевицеколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="baa57-109">**IMsRdpDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="baa57-110">Методы</span><span class="sxs-lookup"><span data-stu-id="baa57-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="baa57-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="baa57-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="baa57-112">Методы</span><span class="sxs-lookup"><span data-stu-id="baa57-112">Methods</span></span>

<span data-ttu-id="baa57-113">Интерфейс **имсрдпдевицеколлектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="baa57-113">The **IMsRdpDeviceCollection** interface has these methods.</span></span>



| <span data-ttu-id="baa57-114">Метод</span><span class="sxs-lookup"><span data-stu-id="baa57-114">Method</span></span>                                                        | <span data-ttu-id="baa57-115">Описание</span><span class="sxs-lookup"><span data-stu-id="baa57-115">Description</span></span>                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="baa57-116">**рескандевицес**</span><span class="sxs-lookup"><span data-stu-id="baa57-116">**RescanDevices**</span></span>](imsrdpdevicecollection-rescandevices.md) | <span data-ttu-id="baa57-117">Обновляет список объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="baa57-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="baa57-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="baa57-118">Properties</span></span>

<span data-ttu-id="baa57-119">Интерфейс **имсрдпдевицеколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="baa57-119">The **IMsRdpDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="baa57-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="baa57-120">Property</span></span>                                                                 | <span data-ttu-id="baa57-121">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="baa57-121">Access type</span></span>          | <span data-ttu-id="baa57-122">Описание</span><span class="sxs-lookup"><span data-stu-id="baa57-122">Description</span></span>                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="baa57-123">**девицебид**</span><span class="sxs-lookup"><span data-stu-id="baa57-123">**DeviceById**</span></span>](imsrdpdevicecollection-devicebyid.md)<br/>       | <span data-ttu-id="baa57-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="baa57-124">Read-only</span></span><br/> | <span data-ttu-id="baa57-125">Извлекает устройство с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="baa57-125">Retrieves the device with the specified identifier.</span></span><br/> |
| [<span data-ttu-id="baa57-126">**девицебиндекс**</span><span class="sxs-lookup"><span data-stu-id="baa57-126">**DeviceByIndex**</span></span>](imsrdpdevicecollection-devicebyindex.md)<br/> | <span data-ttu-id="baa57-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="baa57-127">Read-only</span></span><br/> | <span data-ttu-id="baa57-128">Извлекает устройство по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="baa57-128">Retrieves the device at the specified index.</span></span><br/>        |
| [<span data-ttu-id="baa57-129">**DeviceCount**</span><span class="sxs-lookup"><span data-stu-id="baa57-129">**DeviceCount**</span></span>](imsrdpdevicecollection-devicecount.md)<br/>     | <span data-ttu-id="baa57-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="baa57-130">Read-only</span></span><br/> | <span data-ttu-id="baa57-131">Возвращает число объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="baa57-131">Retrieves the count of objects in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="baa57-132">Требования</span><span class="sxs-lookup"><span data-stu-id="baa57-132">Requirements</span></span>



| <span data-ttu-id="baa57-133">Требование</span><span class="sxs-lookup"><span data-stu-id="baa57-133">Requirement</span></span> | <span data-ttu-id="baa57-134">Значение</span><span class="sxs-lookup"><span data-stu-id="baa57-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa57-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="baa57-135">Minimum supported client</span></span><br/> | <span data-ttu-id="baa57-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="baa57-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="baa57-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="baa57-137">Minimum supported server</span></span><br/> | <span data-ttu-id="baa57-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="baa57-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="baa57-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="baa57-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="baa57-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baa57-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="baa57-141">DLL</span><span class="sxs-lookup"><span data-stu-id="baa57-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baa57-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baa57-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="baa57-143">IID</span><span class="sxs-lookup"><span data-stu-id="baa57-143">IID</span></span><br/>                      | <span data-ttu-id="baa57-144">IID \_ имсрдпдевицеколлектион определен как 56540617-d281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="baa57-144">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="baa57-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="baa57-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa57-146">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="baa57-146">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="baa57-147">**имсрдпдевице**</span><span class="sxs-lookup"><span data-stu-id="baa57-147">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

