---
description: Указывает, будет ли подсистема мультимедиа воспроизводить защищенное содержимое.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: Атрибут MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33feb8d3e1d7c216cfd0392a1fcf9df0100f924
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351352"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a><span data-ttu-id="1b7cb-103">\_ \_ \_ \_ Атрибут флагов защиты содержимого для механизма \_ передачи мультимедиа MF</span><span class="sxs-lookup"><span data-stu-id="1b7cb-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_FLAGS attribute</span></span>

<span data-ttu-id="1b7cb-104">Указывает, будет ли подсистема мультимедиа воспроизводить защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="1b7cb-104">Specifies whether the Media Engine will play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="1b7cb-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1b7cb-105">Data type</span></span>

<span data-ttu-id="1b7cb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1b7cb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1b7cb-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b7cb-107">Remarks</span></span>

<span data-ttu-id="1b7cb-108">Значение этого атрибута является побитовым для **флагов из перечисления** [**\_ \_ \_ \_ флагов защиты Media Engine MF**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) .</span><span class="sxs-lookup"><span data-stu-id="1b7cb-108">The value of this attribute is a bitwise **OR** of flags from the [**MF\_MEDIA\_ENGINE\_PROTECTION\_FLAGS**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) enumeration.</span></span> <span data-ttu-id="1b7cb-109">Чтобы включить воспроизведение защищенного содержимого, установите флаг **" \_ \_ \_ включить \_ защищенное \_ содержимое" для компонента MF Media Engine** .</span><span class="sxs-lookup"><span data-stu-id="1b7cb-109">To enable playback of protected content, set the **MF\_MEDIA\_ENGINE\_ENABLE\_PROTECTED\_CONTENT** flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b7cb-110">Требования</span><span class="sxs-lookup"><span data-stu-id="1b7cb-110">Requirements</span></span>



| <span data-ttu-id="1b7cb-111">Требование</span><span class="sxs-lookup"><span data-stu-id="1b7cb-111">Requirement</span></span> | <span data-ttu-id="1b7cb-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1b7cb-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b7cb-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b7cb-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1b7cb-114">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="1b7cb-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="1b7cb-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b7cb-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1b7cb-116">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="1b7cb-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="1b7cb-117">Header</span><span class="sxs-lookup"><span data-stu-id="1b7cb-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b7cb-118"><dt>Мфмедиаенгине. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b7cb-118"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b7cb-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b7cb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b7cb-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1b7cb-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1b7cb-121">Атрибуты обработчика мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1b7cb-121">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="1b7cb-122">**Имфмедиаенгинеклассфактори:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="1b7cb-122">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




