---
description: Содержит указатель на интерфейс обратного вызова для механизма мультимедиа.
ms.assetid: 5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D
title: Атрибут MF_MEDIA_ENGINE_CALLBACK (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173e22f9d87f4a77f9ed4a1d1b405fc040bd32b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703447"
---
# <a name="mf_media_engine_callback-attribute"></a><span data-ttu-id="cb79e-103">\_ \_ Атрибут обратного вызова для обработчика мультимедиа MF \_</span><span class="sxs-lookup"><span data-stu-id="cb79e-103">MF\_MEDIA\_ENGINE\_CALLBACK attribute</span></span>

<span data-ttu-id="cb79e-104">Содержит указатель на интерфейс обратного вызова для механизма мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cb79e-104">Contains a pointer to the callback interface for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="cb79e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cb79e-105">Data type</span></span>

<span data-ttu-id="cb79e-106">**Имфмедиаенгиненотифи \* *_ хранится как _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="cb79e-106">**IMFMediaEngineNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="cb79e-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="cb79e-107">Get/set</span></span>

<span data-ttu-id="cb79e-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="cb79e-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="cb79e-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="cb79e-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb79e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb79e-110">Remarks</span></span>

<span data-ttu-id="cb79e-111">Значением этого атрибута является указатель на интерфейс [**имфмедиаенгиненотифи**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) , реализованный приложением.</span><span class="sxs-lookup"><span data-stu-id="cb79e-111">The value of this attribute is a pointer to the [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) interface, implemented by the application.</span></span>

<span data-ttu-id="cb79e-112">Этот атрибут используется с методом [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) для инициализации механизма мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cb79e-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="cb79e-113">Атрибут является обязательным.</span><span class="sxs-lookup"><span data-stu-id="cb79e-113">The attribute is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb79e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cb79e-114">Requirements</span></span>



| <span data-ttu-id="cb79e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cb79e-115">Requirement</span></span> | <span data-ttu-id="cb79e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cb79e-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb79e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb79e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cb79e-118">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="cb79e-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="cb79e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb79e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cb79e-120">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="cb79e-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="cb79e-121">Header</span><span class="sxs-lookup"><span data-stu-id="cb79e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb79e-122"><dt>Мфмедиаенгине. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb79e-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb79e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb79e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb79e-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb79e-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cb79e-125">**Имфмедиаенгинеклассфактори:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="cb79e-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> <dt>

[<span data-ttu-id="cb79e-126">**имфмедиаенгиненотифи**</span><span class="sxs-lookup"><span data-stu-id="cb79e-126">**IMFMediaEngineNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify)
</dt> </dl>

 

 




