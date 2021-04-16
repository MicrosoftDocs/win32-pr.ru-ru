---
title: Интерфейс IMsRdpCameraRedirConfig
description: Представляет конфигурации для камеры, доступной для перенаправления.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг, описание
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104536383"
---
# <a name="imsrdpcameraredirconfig-interface"></a><span data-ttu-id="d65ef-105">Интерфейс IMsRdpCameraRedirConfig</span><span class="sxs-lookup"><span data-stu-id="d65ef-105">IMsRdpCameraRedirConfig interface</span></span>

<span data-ttu-id="d65ef-106">Представляет конфигурации для камеры, доступной для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="d65ef-106">Represents the configurations for a camera that is available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="d65ef-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="d65ef-107">Members</span></span>

<span data-ttu-id="d65ef-108">Интерфейс **имсрдпкамераредирконфиг** наследует от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="d65ef-108">The **IMsRdpCameraRedirConfig** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="d65ef-109">**Имсрдпкамераредирконфиг** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d65ef-109">**IMsRdpCameraRedirConfig** also has these types of members:</span></span>

- [<span data-ttu-id="d65ef-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d65ef-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d65ef-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d65ef-111">Properties</span></span>

<span data-ttu-id="d65ef-112">Интерфейс **имсрдпкамераредирконфиг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d65ef-112">The **IMsRdpCameraRedirConfig** interface has these properties.</span></span>

| <span data-ttu-id="d65ef-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="d65ef-113">Property</span></span>         | <span data-ttu-id="d65ef-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="d65ef-114">Access type</span></span>           | <span data-ttu-id="d65ef-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d65ef-115">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="d65ef-116">**девицеексистс**</span><span class="sxs-lookup"><span data-stu-id="d65ef-116">**DeviceExists**</span></span>](imsrdpcameraredirconfig-deviceexists.md)      | <span data-ttu-id="d65ef-117">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d65ef-117">Read-only</span></span> | <span data-ttu-id="d65ef-118">Указывает, существует ли устройство камеры (т. е. Камера подключено).</span><span class="sxs-lookup"><span data-stu-id="d65ef-118">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>   |
| [<span data-ttu-id="d65ef-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="d65ef-119">**FriendlyName**</span></span>](imsrdpcameraredirconfig-friendlyname.md)                       | <span data-ttu-id="d65ef-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d65ef-120">Read-only</span></span> |    <span data-ttu-id="d65ef-121">Возвращает понятное имя камеры.</span><span class="sxs-lookup"><span data-stu-id="d65ef-121">Gets the camera’s friendly name.</span></span>    |
| [<span data-ttu-id="d65ef-122">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="d65ef-122">**InstanceId**</span></span>](imsrdpcameraredirconfig-instanceid.md)      | <span data-ttu-id="d65ef-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d65ef-123">Read-only</span></span> |  <span data-ttu-id="d65ef-124">Возвращает идентификатор экземпляра камеры.</span><span class="sxs-lookup"><span data-stu-id="d65ef-124">Gets the instance ID of the camera.</span></span>  |
| [<span data-ttu-id="d65ef-125">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="d65ef-125">**ParentInstanceId**</span></span>](imsrdpcameraredirconfig-parentinstanceid.md)                       | <span data-ttu-id="d65ef-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d65ef-126">Read-only</span></span> |    <span data-ttu-id="d65ef-127">Возвращает идентификатор родительского экземпляра устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="d65ef-127">Gets the parent device instance ID of the camera.</span></span>   |
| [<span data-ttu-id="d65ef-128">**Redirected**</span><span class="sxs-lookup"><span data-stu-id="d65ef-128">**Redirected**</span></span>](imsrdpcameraredirconfig-redirected.md)      | <span data-ttu-id="d65ef-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d65ef-129">Read/Write</span></span> |  <span data-ttu-id="d65ef-130">Указывает, будет ли перенаправлена камера.</span><span class="sxs-lookup"><span data-stu-id="d65ef-130">Specifies whether or not the camera is redirected.</span></span>  |
| [<span data-ttu-id="d65ef-131">**SymbolicLink**</span><span class="sxs-lookup"><span data-stu-id="d65ef-131">**SymbolicLink**</span></span>](imsrdpcameraredirconfig-symboliclink.md)                       | <span data-ttu-id="d65ef-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d65ef-132">Read-only</span></span> |   <span data-ttu-id="d65ef-133">Возвращает символьную ссылку интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.</span><span class="sxs-lookup"><span data-stu-id="d65ef-133">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>   |

## <a name="requirements"></a><span data-ttu-id="d65ef-134">Требования</span><span class="sxs-lookup"><span data-stu-id="d65ef-134">Requirements</span></span>

| <span data-ttu-id="d65ef-135">Требование</span><span class="sxs-lookup"><span data-stu-id="d65ef-135">Requirement</span></span> | <span data-ttu-id="d65ef-136">Значение</span><span class="sxs-lookup"><span data-stu-id="d65ef-136">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="d65ef-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d65ef-137">Minimum supported client</span></span>| <span data-ttu-id="d65ef-138">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="d65ef-138">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="d65ef-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d65ef-139">Type library</span></span>            | <span data-ttu-id="d65ef-140">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d65ef-140">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="d65ef-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d65ef-141">DLL</span></span>                  | <span data-ttu-id="d65ef-142">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d65ef-142">MsTscAx.dll</span></span>     |
| <span data-ttu-id="d65ef-143">IID</span><span class="sxs-lookup"><span data-stu-id="d65ef-143">IID</span></span>                      | <span data-ttu-id="d65ef-144">IID \_ имсрдпкамераредирконфиг определен как 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="d65ef-144">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="d65ef-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d65ef-145">See also</span></span>

- [<span data-ttu-id="d65ef-146">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="d65ef-146">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
- [<span data-ttu-id="d65ef-147">**IMsRdpClientNonScriptable7:: Камераредирконфигколлектион**</span><span class="sxs-lookup"><span data-stu-id="d65ef-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)