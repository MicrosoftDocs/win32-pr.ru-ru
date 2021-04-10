---
description: Включает аппаратное ускорение декодирования устройства Direct3D 9 с помощью ускорения видео DirectX (ДКСВА) версии 1,0.
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: Интерфейс IDirect3DVideoDevice9 (Дксва. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155186"
---
# <a name="idirect3dvideodevice9-interface"></a><span data-ttu-id="b44a1-103">Интерфейс IDirect3DVideoDevice9</span><span class="sxs-lookup"><span data-stu-id="b44a1-103">IDirect3DVideoDevice9 interface</span></span>

<span data-ttu-id="b44a1-104">Включает аппаратное ускорение декодирования устройства Direct3D 9 с помощью ускорения видео DirectX (ДКСВА) версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="b44a1-104">Enables hardware-accelerated decoding from a Direct3D 9 device, using DirectX Video Acceleration (DXVA) version 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b44a1-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="b44a1-105">When to use</span></span>

<span data-ttu-id="b44a1-106">Этот интерфейс не предназначен для общего использования приложением.</span><span class="sxs-lookup"><span data-stu-id="b44a1-106">This interface is not intended for general application use.</span></span> <span data-ttu-id="b44a1-107">Фильтры декодера DirectShow должны использовать интерфейс [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , а не **IDirect3DVideoDevice9**.</span><span class="sxs-lookup"><span data-stu-id="b44a1-107">DirectShow decoder filters should use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, not **IDirect3DVideoDevice9**.</span></span> <span data-ttu-id="b44a1-108">Входные контакты фильтра формирователя микширования видео (VMR) и фильтра микшера наложения предоставляют **иамвидеоакцелератор**.</span><span class="sxs-lookup"><span data-stu-id="b44a1-108">The input pins of the Video Mixing Renderer (VMR) filter and the Overlay Mixer filter expose **IAMVideoAccelerator**.</span></span>

## <a name="members"></a><span data-ttu-id="b44a1-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="b44a1-109">Members</span></span>

<span data-ttu-id="b44a1-110">Интерфейс **IDirect3DVideoDevice9** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b44a1-110">The **IDirect3DVideoDevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b44a1-111">**IDirect3DVideoDevice9** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b44a1-111">**IDirect3DVideoDevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="b44a1-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b44a1-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b44a1-113">Методы</span><span class="sxs-lookup"><span data-stu-id="b44a1-113">Methods</span></span>

<span data-ttu-id="b44a1-114">Интерфейс **IDirect3DVideoDevice9** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b44a1-114">The **IDirect3DVideoDevice9** interface has these methods.</span></span>



| <span data-ttu-id="b44a1-115">Метод</span><span class="sxs-lookup"><span data-stu-id="b44a1-115">Method</span></span>                                                                                   | <span data-ttu-id="b44a1-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b44a1-116">Description</span></span>                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b44a1-117">**креатедксвадевице**</span><span class="sxs-lookup"><span data-stu-id="b44a1-117">**CreateDXVADevice**</span></span>](idirect3dvideodevice9-createdxvadevice.md)                       | <span data-ttu-id="b44a1-118">Создает устройство декодера ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="b44a1-118">Creates a DXVA decoder device.</span></span><br/>                                                                                         |
| [<span data-ttu-id="b44a1-119">**креатесурфаце**</span><span class="sxs-lookup"><span data-stu-id="b44a1-119">**CreateSurface**</span></span>](idirect3dvideodevice9-createsurface.md)                             | <span data-ttu-id="b44a1-120">Создает сжатую поверхность для декодирования ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="b44a1-120">Creates a compressed surface for DXVA decoding.</span></span><br/>                                                                        |
| [<span data-ttu-id="b44a1-121">**жетдксвакомпресседбуфферинфо**</span><span class="sxs-lookup"><span data-stu-id="b44a1-121">**GetDXVACompressedBufferInfo**</span></span>](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | <span data-ttu-id="b44a1-122">Возвращает сведения о сжатых буферах, необходимых для декодирования с аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="b44a1-122">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span><br/>                                |
| [<span data-ttu-id="b44a1-123">**жетдксвагуидс**</span><span class="sxs-lookup"><span data-stu-id="b44a1-123">**GetDXVAGuids**</span></span>](idirect3dvideodevice9-getdxvaguids.md)                               | <span data-ttu-id="b44a1-124">Возвращает список профилей ДКСВА, поддерживаемых драйвером экрана.</span><span class="sxs-lookup"><span data-stu-id="b44a1-124">Gets a list of the DXVA profiles that are supported by the display driver.</span></span><br/>                                             |
| [<span data-ttu-id="b44a1-125">**жетдксваинтерналинфо**</span><span class="sxs-lookup"><span data-stu-id="b44a1-125">**GetDXVAInternalInfo**</span></span>](idirect3dvideodevice9-getdxvainternalinfo.md)                 | <span data-ttu-id="b44a1-126">Запрашивает объем вспомогательной памяти, выделяемой слоем абстрагирования оборудования (HAL) для частного использования.</span><span class="sxs-lookup"><span data-stu-id="b44a1-126">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span> <br/> |
| [<span data-ttu-id="b44a1-127">**жетункомпресседдксваформатс**</span><span class="sxs-lookup"><span data-stu-id="b44a1-127">**GetUncompressedDXVAFormats**</span></span>](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | <span data-ttu-id="b44a1-128">Возвращает список несжатых форматов пикселей, которые могут быть отображены с помощью указанного профиля ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="b44a1-128">Gets a list of uncompressed pixel formats that can be rendered using a specified DXVA profile.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="b44a1-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b44a1-129">Remarks</span></span>

<span data-ttu-id="b44a1-130">Чтобы получить указатель на этот интерфейс, вызовите метод **QueryInterface** для указателя [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) или [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) .</span><span class="sxs-lookup"><span data-stu-id="b44a1-130">To get a pointer to this interface, call **QueryInterface** on an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) or [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) pointer.</span></span>

<span data-ttu-id="b44a1-131">Этот интерфейс поддерживает только ДКСВА 1,0.</span><span class="sxs-lookup"><span data-stu-id="b44a1-131">This interface supports DXVA 1.0 only.</span></span> <span data-ttu-id="b44a1-132">Он не поддерживает ДКСВА 2,0.</span><span class="sxs-lookup"><span data-stu-id="b44a1-132">It does not support DXVA 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="b44a1-133">Требования</span><span class="sxs-lookup"><span data-stu-id="b44a1-133">Requirements</span></span>



| <span data-ttu-id="b44a1-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b44a1-134">Requirement</span></span> | <span data-ttu-id="b44a1-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b44a1-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b44a1-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b44a1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b44a1-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b44a1-137">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b44a1-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b44a1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b44a1-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b44a1-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b44a1-140">Header</span><span class="sxs-lookup"><span data-stu-id="b44a1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b44a1-141"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="b44a1-141"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b44a1-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b44a1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b44a1-143">Интерфейсы видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="b44a1-143">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b44a1-144">Ускорение видео DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="b44a1-144">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="b44a1-145">Спецификация ДКСВА 1,0</span><span class="sxs-lookup"><span data-stu-id="b44a1-145">DXVA 1.0 specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
