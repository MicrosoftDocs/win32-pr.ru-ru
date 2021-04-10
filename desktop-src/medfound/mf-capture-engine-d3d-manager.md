---
description: Задает указатель на диспетчер устройств DXGI в подсистеме записи.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: Атрибут MF_CAPTURE_ENGINE_D3D_MANAGER (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154646"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a><span data-ttu-id="c9812-103">\_ \_ \_ Атрибут диспетчера D3D ядра записи MF \_</span><span class="sxs-lookup"><span data-stu-id="c9812-103">MF\_CAPTURE\_ENGINE\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="c9812-104">Задает указатель на диспетчер устройств DXGI в подсистеме записи.</span><span class="sxs-lookup"><span data-stu-id="c9812-104">Sets a pointer to the DXGI Device Manager on the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="c9812-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c9812-105">Data type</span></span>

<span data-ttu-id="c9812-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="c9812-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="c9812-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9812-107">Remarks</span></span>

<span data-ttu-id="c9812-108">Значение этого атрибута является указателем на интерфейс [_ *имфдксгидевицеманажер* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="c9812-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span> <span data-ttu-id="c9812-109">Этот атрибут позволяет подсистеме захвата выделять видеоматериалы с помощью поверхностей DXGI и использовать аппаратное ускорение для обработки декодирования и видео.</span><span class="sxs-lookup"><span data-stu-id="c9812-109">This attribute enables the capture engine to allocate video frames using DXGI surfaces, and to use hardware acceleration for decoding and video processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9812-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c9812-110">Requirements</span></span>



| <span data-ttu-id="c9812-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c9812-111">Requirement</span></span> | <span data-ttu-id="c9812-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c9812-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9812-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9812-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c9812-114">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c9812-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c9812-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9812-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c9812-116">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c9812-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c9812-117">Header</span><span class="sxs-lookup"><span data-stu-id="c9812-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9812-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9812-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9812-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9812-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9812-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9812-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9812-121">Атрибуты подсистемы захвата</span><span class="sxs-lookup"><span data-stu-id="c9812-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9812-122">**Имфкаптурингине:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="c9812-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




