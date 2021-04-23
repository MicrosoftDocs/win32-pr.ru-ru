---
title: Интерфейс IMsRdpCameraRedirConfigCollection
description: Представляет коллекцию камер (и связанных конфигураций), доступных для перенаправления.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, описание
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104139174"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a><span data-ttu-id="02592-105">Интерфейс IMsRdpCameraRedirConfigCollection</span><span class="sxs-lookup"><span data-stu-id="02592-105">IMsRdpCameraRedirConfigCollection interface</span></span>

 <span data-ttu-id="02592-106">Представляет коллекцию камер (и связанных конфигураций), доступных для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="02592-106">Represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="02592-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="02592-107">Members</span></span>

<span data-ttu-id="02592-108">Интерфейс **имсрдпкамераредирконфигколлектион** наследует от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="02592-108">The **IMsRdpCameraRedirConfigCollection** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="02592-109">**Имсрдпкамераредирконфигколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="02592-109">**IMsRdpCameraRedirConfigCollection** also has these types of members:</span></span>

- [<span data-ttu-id="02592-110">Методы</span><span class="sxs-lookup"><span data-stu-id="02592-110">Methods</span></span>](#methods)
- [<span data-ttu-id="02592-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="02592-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="02592-112">Методы</span><span class="sxs-lookup"><span data-stu-id="02592-112">Methods</span></span>

<span data-ttu-id="02592-113">Интерфейс **имсрдпкамераредирконфигколлектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="02592-113">The **IMsRdpCameraRedirConfigCollection** interface has these methods.</span></span>

| <span data-ttu-id="02592-114">Метод</span><span class="sxs-lookup"><span data-stu-id="02592-114">Method</span></span>            | <span data-ttu-id="02592-115">Описание</span><span class="sxs-lookup"><span data-stu-id="02592-115">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="02592-116">**аддконфиг**</span><span class="sxs-lookup"><span data-stu-id="02592-116">**AddConfig**</span></span>](imsrdpcameraredirconfigcollection-addconfig.md)       |  <span data-ttu-id="02592-117">Добавляет объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) в коллекцию (соответствующая камера не должна быть подключена).</span><span class="sxs-lookup"><span data-stu-id="02592-117">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>                   |
| [<span data-ttu-id="02592-118">**Повторное сканирование**</span><span class="sxs-lookup"><span data-stu-id="02592-118">**Rescan**</span></span>](imsrdpcameraredirconfigcollection-rescan.md)       |  <span data-ttu-id="02592-119">Перечисляет подключенные устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="02592-119">Enumerates connected camera devices.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="02592-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="02592-120">Properties</span></span>

<span data-ttu-id="02592-121">Интерфейс **имсрдпкамераредирконфигколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="02592-121">The **IMsRdpCameraRedirConfigCollection** interface has these properties.</span></span>

| <span data-ttu-id="02592-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="02592-122">Property</span></span>         | <span data-ttu-id="02592-123">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="02592-123">Access type</span></span>           | <span data-ttu-id="02592-124">Описание</span><span class="sxs-lookup"><span data-stu-id="02592-124">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="02592-125">**биндекс**</span><span class="sxs-lookup"><span data-stu-id="02592-125">**ByIndex**</span></span>](imsrdpcameraredirconfigcollection-byindex.md)      | <span data-ttu-id="02592-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="02592-126">Read-only</span></span> |  <span data-ttu-id="02592-127">Возвращает объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) по его индексу в коллекции.</span><span class="sxs-lookup"><span data-stu-id="02592-127">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>   |
| [<span data-ttu-id="02592-128">**бинстанцеид**</span><span class="sxs-lookup"><span data-stu-id="02592-128">**ByInstanceId**</span></span>](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | <span data-ttu-id="02592-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="02592-129">Read-only</span></span> |    <span data-ttu-id="02592-130">Возвращает из коллекции объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий заданному идентификатору экземпляра.</span><span class="sxs-lookup"><span data-stu-id="02592-130">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>    |
| [<span data-ttu-id="02592-131">**бисимболиклинк**</span><span class="sxs-lookup"><span data-stu-id="02592-131">**BySymbolicLink**</span></span>](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | <span data-ttu-id="02592-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="02592-132">Read-only</span></span> |  <span data-ttu-id="02592-133">Возвращает из коллекции объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий заданной символьной ссылке интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.</span><span class="sxs-lookup"><span data-stu-id="02592-133">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>  |
| [<span data-ttu-id="02592-134">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="02592-134">**Count**</span></span>](imsrdpcameraredirconfigcollection-count.md)                       | <span data-ttu-id="02592-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="02592-135">Read-only</span></span> |    <span data-ttu-id="02592-136">Возвращает число объектов [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="02592-136">Returns the number of [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) objects in the collection.</span></span>   |
| [<span data-ttu-id="02592-137">**енкодевидео**</span><span class="sxs-lookup"><span data-stu-id="02592-137">**EncodeVideo**</span></span>](imsrdpcameraredirconfigcollection-encodevideo.md)      | <span data-ttu-id="02592-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="02592-138">Read/Write</span></span> |  <span data-ttu-id="02592-139">Указывает, является ли поток видео закодированным H. 264.</span><span class="sxs-lookup"><span data-stu-id="02592-139">Specifies whether or not the video stream is H.264 encoded.</span></span>  |
| [<span data-ttu-id="02592-140">**енкодингкуалити**</span><span class="sxs-lookup"><span data-stu-id="02592-140">**EncodingQuality**</span></span>](imsrdpcameraredirconfigcollection-encodingquality.md)                       | <span data-ttu-id="02592-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="02592-141">Read/Write</span></span> |    <span data-ttu-id="02592-142">Задает качество кодирования (скорость потока).</span><span class="sxs-lookup"><span data-stu-id="02592-142">Specifies the encoding quality (bit rate).</span></span>   |
| [<span data-ttu-id="02592-143">**редиректбидефаулт**</span><span class="sxs-lookup"><span data-stu-id="02592-143">**RedirectByDefault**</span></span>](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | <span data-ttu-id="02592-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="02592-144">Read/Write</span></span> |   <span data-ttu-id="02592-145">Указывает, будет ли перенаправлена какая либо новая камера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="02592-145">Specifies whether or not any new camera gets redirected by default.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="02592-146">Требования</span><span class="sxs-lookup"><span data-stu-id="02592-146">Requirements</span></span>

| <span data-ttu-id="02592-147">Требование</span><span class="sxs-lookup"><span data-stu-id="02592-147">Requirement</span></span> | <span data-ttu-id="02592-148">Значение</span><span class="sxs-lookup"><span data-stu-id="02592-148">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="02592-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02592-149">Minimum supported client</span></span>| <span data-ttu-id="02592-150">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="02592-150">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="02592-151">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="02592-151">Type library</span></span>            | <span data-ttu-id="02592-152">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="02592-152">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="02592-153">DLL</span><span class="sxs-lookup"><span data-stu-id="02592-153">DLL</span></span>                  | <span data-ttu-id="02592-154">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="02592-154">MsTscAx.dll</span></span>     |
| <span data-ttu-id="02592-155">IID</span><span class="sxs-lookup"><span data-stu-id="02592-155">IID</span></span>                      | <span data-ttu-id="02592-156">IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="02592-156">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>            |

## <a name="see-also"></a><span data-ttu-id="02592-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02592-157">See also</span></span>

- [<span data-ttu-id="02592-158">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="02592-158">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
- [<span data-ttu-id="02592-159">**IMsRdpClientNonScriptable7:: Камераредирконфигколлектион**</span><span class="sxs-lookup"><span data-stu-id="02592-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
