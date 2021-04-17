---
description: Позволяет модулю мультимедиа воспроизводить защищенное содержимое.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: Атрибут MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb99d1df36c9b9adbf1c099d619df60e1144b87
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703448"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a><span data-ttu-id="6ff62-103">\_ \_ \_ \_ Атрибут диспетчера защиты содержимого для компонента MF Media Engine \_</span><span class="sxs-lookup"><span data-stu-id="6ff62-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="6ff62-104">Позволяет модулю мультимедиа воспроизводить защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="6ff62-104">Enables the Media Engine to play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="6ff62-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6ff62-105">Data type</span></span>

<span data-ttu-id="6ff62-106">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="6ff62-106">**IUnknown\***</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff62-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ff62-107">Remarks</span></span>

<span data-ttu-id="6ff62-108">Значение этого атрибута является указателем на интерфейс [**имфконтентпротектионманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .</span><span class="sxs-lookup"><span data-stu-id="6ff62-108">The value of this attribute is a pointer to the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span> <span data-ttu-id="6ff62-109">Вызывающий объект должен реализовать интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6ff62-109">The caller must implement the interface.</span></span>

<span data-ttu-id="6ff62-110">Этот атрибут может быть одним из атрибутов, передаваемых в [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="6ff62-110">This attribute can be one of the attributes passed to [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="6ff62-111">Он необходим, если защищенное содержимое должно воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="6ff62-111">It is required if protected content is to be played.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ff62-112">Требования</span><span class="sxs-lookup"><span data-stu-id="6ff62-112">Requirements</span></span>



| <span data-ttu-id="6ff62-113">Требование</span><span class="sxs-lookup"><span data-stu-id="6ff62-113">Requirement</span></span> | <span data-ttu-id="6ff62-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6ff62-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff62-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ff62-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff62-116">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="6ff62-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="6ff62-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ff62-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff62-118">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="6ff62-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="6ff62-119">Header</span><span class="sxs-lookup"><span data-stu-id="6ff62-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ff62-120"><dt>Мфмедиаенгине. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ff62-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ff62-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ff62-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff62-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ff62-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6ff62-123">**Имфмедиаенгинеклассфактори:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="6ff62-123">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




