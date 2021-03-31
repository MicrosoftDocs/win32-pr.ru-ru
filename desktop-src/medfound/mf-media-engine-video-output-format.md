---
description: Задает формат целевого объекта подготовки к просмотру для механизма мультимедиа.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: Атрибут MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820204"
---
# <a name="mf_media_engine_video_output_format-attribute"></a><span data-ttu-id="19ec1-103">\_ \_ \_ \_ Атрибут формата вывода видео для ОБРАБОТЧИКа передачи мультимедиа MF \_</span><span class="sxs-lookup"><span data-stu-id="19ec1-103">MF\_MEDIA\_ENGINE\_VIDEO\_OUTPUT\_FORMAT attribute</span></span>

<span data-ttu-id="19ec1-104">Задает формат целевого объекта подготовки к просмотру для механизма мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="19ec1-104">Sets the render-target format for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="19ec1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="19ec1-105">Data type</span></span>

<span data-ttu-id="19ec1-106">**DXGI \_ ФОРМАТ** хранится как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="19ec1-106">**DXGI\_FORMAT** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="19ec1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19ec1-107">Remarks</span></span>

<span data-ttu-id="19ec1-108">Установите этот атрибут при создании подсистемы мультимедиа в режиме "Frame-Server".</span><span class="sxs-lookup"><span data-stu-id="19ec1-108">Set this attribute if you create the Media Engine in frame-server mode.</span></span> <span data-ttu-id="19ec1-109">Дополнительные сведения см. в разделе [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="19ec1-109">For more information, see [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="19ec1-110">Значением атрибута является значение [ \_ формата DXGI](../direct3d9/d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="19ec1-110">The value of the attribute is a [DXGI\_FORMAT](../direct3d9/d3dformat.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ec1-111">Требования</span><span class="sxs-lookup"><span data-stu-id="19ec1-111">Requirements</span></span>



| <span data-ttu-id="19ec1-112">Требование</span><span class="sxs-lookup"><span data-stu-id="19ec1-112">Requirement</span></span> | <span data-ttu-id="19ec1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="19ec1-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="19ec1-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19ec1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="19ec1-115">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="19ec1-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="19ec1-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19ec1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="19ec1-117">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="19ec1-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="19ec1-118">Header</span><span class="sxs-lookup"><span data-stu-id="19ec1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="19ec1-119"><dt>Мфмедиаенгине. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ec1-119"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19ec1-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19ec1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ec1-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19ec1-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
