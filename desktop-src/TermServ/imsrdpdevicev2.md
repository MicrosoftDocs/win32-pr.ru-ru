---
title: Интерфейс IMsRdpDeviceV2
description: Содержит сведения об объекте устройства. Это усовершенствование интерфейса Имсрдпдевице.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, описание
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681758"
---
# <a name="imsrdpdevicev2-interface"></a><span data-ttu-id="0a668-106">Интерфейс IMsRdpDeviceV2</span><span class="sxs-lookup"><span data-stu-id="0a668-106">IMsRdpDeviceV2 interface</span></span>

<span data-ttu-id="0a668-107">Содержит сведения об объекте устройства.</span><span class="sxs-lookup"><span data-stu-id="0a668-107">Contains information about a device object.</span></span> <span data-ttu-id="0a668-108">Это усовершенствование интерфейса [**имсрдпдевице**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="0a668-108">This is an enhancement of the [**IMsRdpDevice**](imsrdpdevice.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="0a668-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="0a668-109">Members</span></span>

<span data-ttu-id="0a668-110">Интерфейс **IMsRdpDeviceV2** наследует от [**имсрдпдевице**](imsrdpdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0a668-110">The **IMsRdpDeviceV2** interface inherits from [**IMsRdpDevice**](imsrdpdevice.md).</span></span> <span data-ttu-id="0a668-111">**IMsRdpDeviceV2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0a668-111">**IMsRdpDeviceV2** also has these types of members:</span></span>

-   [<span data-ttu-id="0a668-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="0a668-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a668-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0a668-113">Properties</span></span>

<span data-ttu-id="0a668-114">Интерфейс **IMsRdpDeviceV2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0a668-114">The **IMsRdpDeviceV2** interface has these properties.</span></span>



| <span data-ttu-id="0a668-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="0a668-115">Property</span></span>                                                                 | <span data-ttu-id="0a668-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="0a668-116">Access type</span></span>          | <span data-ttu-id="0a668-117">Описание</span><span class="sxs-lookup"><span data-stu-id="0a668-117">Description</span></span>                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a668-118">**кмклассгуид**</span><span class="sxs-lookup"><span data-stu-id="0a668-118">**CmClassGuid**</span></span>](imsrdpdevicev2-cmclassguid.md)<br/>             | <span data-ttu-id="0a668-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a668-119">Read-only</span></span><br/> | <span data-ttu-id="0a668-120">Содержит GUID класса установки Configuration Manager для устройства.</span><span class="sxs-lookup"><span data-stu-id="0a668-120">Contains the configuration manager setup class GUID for the device.</span></span><br/>                     |
| [<span data-ttu-id="0a668-121">**кмдевицеинстанце**</span><span class="sxs-lookup"><span data-stu-id="0a668-121">**CmDeviceInstance**</span></span>](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | <span data-ttu-id="0a668-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a668-122">Read-only</span></span><br/> | <span data-ttu-id="0a668-123">Содержит экземпляр устройства Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0a668-123">Contains the configuration manager device instance of the device.</span></span><br/>                       |
| [<span data-ttu-id="0a668-124">**девицетекст**</span><span class="sxs-lookup"><span data-stu-id="0a668-124">**DeviceText**</span></span>](imsrdpdevicev2-devicetext.md)<br/>               | <span data-ttu-id="0a668-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a668-125">Read-only</span></span><br/> | <span data-ttu-id="0a668-126">Содержит текст устройства.</span><span class="sxs-lookup"><span data-stu-id="0a668-126">Contains the device text.</span></span><br/>                                                               |
| [<span data-ttu-id="0a668-127">**дривелеттербитмап**</span><span class="sxs-lookup"><span data-stu-id="0a668-127">**DriveLetterBitmap**</span></span>](imsrdpdevicev2-driveletterbitmap.md)<br/> | <span data-ttu-id="0a668-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a668-128">Read-only</span></span><br/> | <span data-ttu-id="0a668-129">Содержит битовое значение, представляющее собой карту букв диска, содержащихся в устройстве.</span><span class="sxs-lookup"><span data-stu-id="0a668-129">Contains a bitfield that represents a map of drive letters contained within the device.</span></span><br/> |
| [<span data-ttu-id="0a668-130">**искомпоситедевице**</span><span class="sxs-lookup"><span data-stu-id="0a668-130">**IsCompositeDevice**</span></span>](imsrdpdevicev2-iscompositedevice.md)<br/> | <span data-ttu-id="0a668-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a668-131">Read-only</span></span><br/> | <span data-ttu-id="0a668-132">Указывает, является ли устройство составным.</span><span class="sxs-lookup"><span data-stu-id="0a668-132">Specifies if the device is a composite device.</span></span><br/>                                          |
| [<span data-ttu-id="0a668-133">**исоптионалдевице**</span><span class="sxs-lookup"><span data-stu-id="0a668-133">**IsOptionalDevice**</span></span>](imsrdpdevicev2-isoptionaldevice.md)<br/>   | <span data-ttu-id="0a668-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a668-134">Read-only</span></span><br/> | <span data-ttu-id="0a668-135">Указывает, является ли устройство необязательным для перенаправления USB.</span><span class="sxs-lookup"><span data-stu-id="0a668-135">Specifies if the device is optional for USB redirection.</span></span><br/>                                |
| [<span data-ttu-id="0a668-136">**исусбдевице**</span><span class="sxs-lookup"><span data-stu-id="0a668-136">**IsUSBDevice**</span></span>](imsrdpdevicev2-isusbdevice.md)<br/>             | <span data-ttu-id="0a668-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a668-137">Read-only</span></span><br/> | <span data-ttu-id="0a668-138">Указывает, что устройство предназначено для перенаправления USB.</span><span class="sxs-lookup"><span data-stu-id="0a668-138">Specifies if the device is for USB redirection.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="0a668-139">Требования</span><span class="sxs-lookup"><span data-stu-id="0a668-139">Requirements</span></span>



| <span data-ttu-id="0a668-140">Требование</span><span class="sxs-lookup"><span data-stu-id="0a668-140">Requirement</span></span> | <span data-ttu-id="0a668-141">Значение</span><span class="sxs-lookup"><span data-stu-id="0a668-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a668-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a668-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0a668-143">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="0a668-143">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="0a668-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a668-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0a668-145">Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="0a668-145">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="0a668-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0a668-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a668-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a668-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a668-148">DLL</span><span class="sxs-lookup"><span data-stu-id="0a668-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a668-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a668-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a668-150">IID</span><span class="sxs-lookup"><span data-stu-id="0a668-150">IID</span></span><br/>                      | <span data-ttu-id="0a668-151">IID \_ IMsRdpDeviceV2 определен как 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="0a668-151">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



 

 





