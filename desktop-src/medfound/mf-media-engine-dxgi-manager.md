---
description: Задает диспетчер устройств в механизме мультимедиа Microsoft DirectX Graphics Framework (DXGI).
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: Атрибут MF_MEDIA_ENGINE_DXGI_MANAGER (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e731b5aa2449ae772427c6743ec4f97b5d7601
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703435"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a><span data-ttu-id="4a262-103">\_ \_ \_ Атрибут диспетчера DXGI для модуля передачи мультимедиа MF \_</span><span class="sxs-lookup"><span data-stu-id="4a262-103">MF\_MEDIA\_ENGINE\_DXGI\_MANAGER attribute</span></span>

<span data-ttu-id="4a262-104">Задает диспетчер устройств в механизме мультимедиа Microsoft DirectX Graphics Framework (DXGI).</span><span class="sxs-lookup"><span data-stu-id="4a262-104">Sets the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager on the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a262-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4a262-105">Data type</span></span>

<span data-ttu-id="4a262-106">**Имфдксгидевицеманажер \* *_ хранится как _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="4a262-106">**IMFDXGIDeviceManager\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="4a262-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="4a262-107">Get/set</span></span>

<span data-ttu-id="4a262-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="4a262-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="4a262-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="4a262-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a262-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a262-110">Remarks</span></span>

<span data-ttu-id="4a262-111">Значение этого атрибута является указателем на интерфейс [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="4a262-111">The value of this attribute is a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="4a262-112">В режиме «Frame-Server» этот атрибут позволяет подсистеме мультимедиа использовать аппаратное ускорение при декодировании и обработке видео.</span><span class="sxs-lookup"><span data-stu-id="4a262-112">In frame-server mode, this attribute enables the Media Engine to use hardware acceleration for video decoding and video processing.</span></span> <span data-ttu-id="4a262-113">Если атрибут не задан, подсистема мультимедиа использует программное декодирование и обработку.</span><span class="sxs-lookup"><span data-stu-id="4a262-113">If the attribute is not set, the Media Engine uses software decoding and processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a262-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4a262-114">Requirements</span></span>



| <span data-ttu-id="4a262-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4a262-115">Requirement</span></span> | <span data-ttu-id="4a262-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4a262-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a262-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a262-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a262-118">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="4a262-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="4a262-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a262-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a262-120">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="4a262-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="4a262-121">Header</span><span class="sxs-lookup"><span data-stu-id="4a262-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a262-122"><dt>Мфмедиаенгине. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a262-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a262-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a262-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a262-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4a262-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a262-125">**Имфмедиаенгинеклассфактори:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="4a262-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




