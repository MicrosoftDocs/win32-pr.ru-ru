---
title: Интерфейс Имсрдпдевице
description: Содержит сведения об объекте устройства.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпдевице
- Службы удаленных рабочих столов интерфейса Имсрдпдевице, описание
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ddfbb739a8cf8e93ee2c2214e14095ac68bd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672541"
---
# <a name="imsrdpdevice-interface"></a><span data-ttu-id="18f26-105">Интерфейс Имсрдпдевице</span><span class="sxs-lookup"><span data-stu-id="18f26-105">IMsRdpDevice interface</span></span>

<span data-ttu-id="18f26-106">Содержит сведения об объекте устройства.</span><span class="sxs-lookup"><span data-stu-id="18f26-106">Contains information about a device object.</span></span>

## <a name="members"></a><span data-ttu-id="18f26-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="18f26-107">Members</span></span>

<span data-ttu-id="18f26-108">Интерфейс **имсрдпдевице** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="18f26-108">The **IMsRdpDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="18f26-109">**Имсрдпдевице** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="18f26-109">**IMsRdpDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="18f26-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="18f26-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18f26-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="18f26-111">Properties</span></span>

<span data-ttu-id="18f26-112">Интерфейс **имсрдпдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="18f26-112">The **IMsRdpDevice** interface has these properties.</span></span>



| <span data-ttu-id="18f26-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="18f26-113">Property</span></span>                                                               | <span data-ttu-id="18f26-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="18f26-114">Access type</span></span>           | <span data-ttu-id="18f26-115">Описание</span><span class="sxs-lookup"><span data-stu-id="18f26-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18f26-116">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="18f26-116">**DeviceDescription**</span></span>](imsrdpdevice-devicedescription.md)<br/> | <span data-ttu-id="18f26-117">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="18f26-117">Read-only</span></span><br/>  | <span data-ttu-id="18f26-118">Возвращает описание устройства, отображаемое пользователю, если отображаемое имя недоступно.</span><span class="sxs-lookup"><span data-stu-id="18f26-118">Retrieves the device description to be displayed to the user if the display name is not available.</span></span><br/> |
| [<span data-ttu-id="18f26-119">**девицеинстанцеид**</span><span class="sxs-lookup"><span data-stu-id="18f26-119">**DeviceInstanceId**</span></span>](imsrdpdevice-deviceinstanceid.md)<br/>   | <span data-ttu-id="18f26-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="18f26-120">Read-only</span></span><br/>  | <span data-ttu-id="18f26-121">Возвращает идентификатор экземпляра устройства.</span><span class="sxs-lookup"><span data-stu-id="18f26-121">Retrieves the device instance identifier of the device.</span></span><br/>                                            |
| [<span data-ttu-id="18f26-122">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="18f26-122">**FriendlyName**</span></span>](imsrdpdevice-friendlyname.md)<br/>           | <span data-ttu-id="18f26-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="18f26-123">Read-only</span></span><br/>  | <span data-ttu-id="18f26-124">Извлекает отображаемое имя для устройства.</span><span class="sxs-lookup"><span data-stu-id="18f26-124">Retrieves the display name for the device.</span></span><br/>                                                         |
| [<span data-ttu-id="18f26-125">**редиректионстате**</span><span class="sxs-lookup"><span data-stu-id="18f26-125">**RedirectionState**</span></span>](imsrdpdevice-redirectionstate.md)<br/>   | <span data-ttu-id="18f26-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="18f26-126">Read/write</span></span><br/> | <span data-ttu-id="18f26-127">Указывает состояние перенаправления устройства.</span><span class="sxs-lookup"><span data-stu-id="18f26-127">Indicates the redirection state of the device.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="18f26-128">Требования</span><span class="sxs-lookup"><span data-stu-id="18f26-128">Requirements</span></span>



| <span data-ttu-id="18f26-129">Требование</span><span class="sxs-lookup"><span data-stu-id="18f26-129">Requirement</span></span> | <span data-ttu-id="18f26-130">Значение</span><span class="sxs-lookup"><span data-stu-id="18f26-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18f26-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18f26-131">Minimum supported client</span></span><br/> | <span data-ttu-id="18f26-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18f26-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="18f26-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18f26-133">Minimum supported server</span></span><br/> | <span data-ttu-id="18f26-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18f26-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="18f26-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="18f26-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="18f26-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18f26-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="18f26-137">DLL</span><span class="sxs-lookup"><span data-stu-id="18f26-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18f26-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18f26-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="18f26-139">IID</span><span class="sxs-lookup"><span data-stu-id="18f26-139">IID</span></span><br/>                      | <span data-ttu-id="18f26-140">IID \_ имсрдпдевице определен как 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="18f26-140">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="18f26-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18f26-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f26-142">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="18f26-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="18f26-143">**имсрдпдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="18f26-143">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

