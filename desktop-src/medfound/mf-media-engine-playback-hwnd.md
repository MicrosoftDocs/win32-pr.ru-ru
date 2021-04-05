---
description: Задает маркер для окна воспроизведения видео для механизма мультимедиа.
ms.assetid: 63889D81-12C5-47C1-B52A-6358E68830C3
title: Атрибут MF_MEDIA_ENGINE_PLAYBACK_HWND (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6a9d38d40b04b32244f48289d3334199a7e035
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999886"
---
# <a name="mf_media_engine_playback_hwnd-attribute"></a><span data-ttu-id="90672-103">\_ \_ \_ Атрибут HWND воспроизведения ОБРАБОТЧИКа мультимедиа MF \_</span><span class="sxs-lookup"><span data-stu-id="90672-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND attribute</span></span>

<span data-ttu-id="90672-104">Задает маркер для окна воспроизведения видео для механизма мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="90672-104">Sets a handle to a video playback window for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="90672-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="90672-105">Data type</span></span>

<span data-ttu-id="90672-106">**HWND** хранится как **UINT64**</span><span class="sxs-lookup"><span data-stu-id="90672-106">**HWND** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="90672-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="90672-107">Get/set</span></span>

<span data-ttu-id="90672-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="90672-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="90672-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="90672-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="remarks"></a><span data-ttu-id="90672-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90672-110">Remarks</span></span>

<span data-ttu-id="90672-111">Этот атрибут используется с методом [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) для инициализации механизма мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="90672-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="90672-112">Требования</span><span class="sxs-lookup"><span data-stu-id="90672-112">Requirements</span></span>



| <span data-ttu-id="90672-113">Требование</span><span class="sxs-lookup"><span data-stu-id="90672-113">Requirement</span></span> | <span data-ttu-id="90672-114">Значение</span><span class="sxs-lookup"><span data-stu-id="90672-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="90672-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90672-115">Minimum supported client</span></span><br/> | <span data-ttu-id="90672-116">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="90672-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="90672-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90672-117">Minimum supported server</span></span><br/> | <span data-ttu-id="90672-118">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="90672-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="90672-119">Header</span><span class="sxs-lookup"><span data-stu-id="90672-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="90672-120"><dt>Мфмедиаенгине. h</dt></span><span class="sxs-lookup"><span data-stu-id="90672-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90672-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90672-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90672-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90672-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




