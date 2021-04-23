---
description: Указывает уровень MPEG-2 или H. 264 в типе видеоматериала. Это псевдоним для \_ уровня MF MT \_ MPEG2 \_ .
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: Атрибут MF_MT_VIDEO_LEVEL (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2c5eb00390df1b5c18cab7e04a5f7449f84fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712913"
---
# <a name="mf_mt_video_level-attribute"></a><span data-ttu-id="d6cf7-104">\_ \_ Атрибут уровня видео MF MT \_</span><span class="sxs-lookup"><span data-stu-id="d6cf7-104">MF\_MT\_VIDEO\_LEVEL attribute</span></span>

<span data-ttu-id="d6cf7-105">Указывает уровень MPEG-2 или H. 264 в типе видеоматериала.</span><span class="sxs-lookup"><span data-stu-id="d6cf7-105">Specifies the MPEG-2 or H.264 level in a video media type.</span></span> <span data-ttu-id="d6cf7-106">Это псевдоним для [ \_ \_ \_ уровня MF MT MPEG2](mf-mt-mpeg2-level-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="d6cf7-106">This is an alias of [MF\_MT\_MPEG2\_LEVEL](mf-mt-mpeg2-level-attribute.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="d6cf7-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d6cf7-107">Data type</span></span>

<span data-ttu-id="d6cf7-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d6cf7-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d6cf7-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6cf7-109">Remarks</span></span>

<span data-ttu-id="d6cf7-110">**Кодировщики H. 264:**</span><span class="sxs-lookup"><span data-stu-id="d6cf7-110">**H.264 encoders:**</span></span>

<span data-ttu-id="d6cf7-111">Поддерживаемые уровни расширены для включения [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).</span><span class="sxs-lookup"><span data-stu-id="d6cf7-111">Supported levels are extended to include the [**eAVEncH264VLevel5\_2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).</span></span>

<span data-ttu-id="d6cf7-112">По умолчанию: Рекомендуемый вариант по умолчанию — выбор минимального уровня для соответствия конфигурации кодирования видео, включая разрешение, частоту кадров и т. д.</span><span class="sxs-lookup"><span data-stu-id="d6cf7-112">Default : Recommended default is to select the minimum level to match video encoding configuration including resolution, frame rate etc.</span></span>

<span data-ttu-id="d6cf7-113">Рекомендуемое значение по умолчанию: выберите минимальный уровень для соответствия конфигурации кодирования видео, включая разрешение, частоту кадров и т. д.</span><span class="sxs-lookup"><span data-stu-id="d6cf7-113">Recommended default: select the minimum level to match video encoding configuration including resolution, frame rate, etc.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6cf7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d6cf7-114">Requirements</span></span>



| <span data-ttu-id="d6cf7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d6cf7-115">Requirement</span></span> | <span data-ttu-id="d6cf7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d6cf7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6cf7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6cf7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d6cf7-118">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d6cf7-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d6cf7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6cf7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d6cf7-120">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6cf7-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d6cf7-121">Header</span><span class="sxs-lookup"><span data-stu-id="d6cf7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6cf7-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6cf7-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6cf7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6cf7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6cf7-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6cf7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




