---
description: Задает визуальный элемент Microsoft DirectComposition в качестве региона воспроизведения для механизма мультимедиа.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: Атрибут MF_MEDIA_ENGINE_PLAYBACK_VISUAL (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105647757"
---
# <a name="mf_media_engine_playback_visual-attribute"></a><span data-ttu-id="e8dd9-103">\_ \_ \_ Визуальный атрибут воспроизведения МУЛЬТИМЕДИЙного модуля MF \_</span><span class="sxs-lookup"><span data-stu-id="e8dd9-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_VISUAL attribute</span></span>

<span data-ttu-id="e8dd9-104">Задает визуальный элемент Microsoft DirectComposition в качестве региона воспроизведения для механизма мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e8dd9-104">Sets a Microsoft DirectComposition visual as the playback region for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="e8dd9-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e8dd9-105">Data type</span></span>

<span data-ttu-id="e8dd9-106">**Идкомпоситионвисуал \* *_ хранится как _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="e8dd9-106">**IDCompositionVisual\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="e8dd9-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="e8dd9-107">Get/set</span></span>

<span data-ttu-id="e8dd9-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="e8dd9-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="e8dd9-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="e8dd9-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8dd9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8dd9-110">Remarks</span></span>

<span data-ttu-id="e8dd9-111">Дополнительные сведения о DirectComposition см. в разделе [DirectComposition](../directcomp/directcomposition-portal.md) и [**идкомпоситионвисуал**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span><span class="sxs-lookup"><span data-stu-id="e8dd9-111">For more information on DirectComposition, see [DirectComposition](../directcomp/directcomposition-portal.md) and [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span></span>

<span data-ttu-id="e8dd9-112">Этот атрибут используется с методом [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) для инициализации механизма мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e8dd9-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8dd9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e8dd9-113">Requirements</span></span>



| <span data-ttu-id="e8dd9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e8dd9-114">Requirement</span></span> | <span data-ttu-id="e8dd9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e8dd9-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8dd9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8dd9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e8dd9-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="e8dd9-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="e8dd9-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8dd9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e8dd9-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="e8dd9-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="e8dd9-120">Header</span><span class="sxs-lookup"><span data-stu-id="e8dd9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8dd9-121"><dt>Мфмедиаенгине. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8dd9-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8dd9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8dd9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8dd9-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8dd9-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
