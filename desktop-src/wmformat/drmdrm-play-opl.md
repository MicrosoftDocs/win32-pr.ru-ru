---
title: Структура DRM_PLAY_OPL (Вмдрмсдк. h)
description: Структура DRM \_ Play \_ ОПЛ содержит сведения об уровнях защиты выходных данных (оплс), указанных в лицензии на действия воспроизведения.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- Формат DRM_PLAY_OPL структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699232"
---
# <a name="drm_play_opl-structure"></a><span data-ttu-id="ecb6a-105">\_Структура DRM Play \_ ОПЛ</span><span class="sxs-lookup"><span data-stu-id="ecb6a-105">DRM\_PLAY\_OPL structure</span></span>

<span data-ttu-id="ecb6a-106">Структура **DRM \_ Play \_ ОПЛ** содержит сведения об уровнях защиты выходных данных (оплс), указанных в лицензии на действия воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ecb6a-106">The **DRM\_PLAY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb6a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecb6a-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="ecb6a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ecb6a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ecb6a-109">**минопл**</span><span class="sxs-lookup"><span data-stu-id="ecb6a-109">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="ecb6a-110">[**DRM \_ Минимальная \_ Структура \_ \_ уровней защиты выходных данных**](drmdrm-minimum-output-protection-levels.md) , содержащая минимум ОПЛ, необходимый для воспроизведения содержимого в различных форматах.</span><span class="sxs-lookup"><span data-stu-id="ecb6a-110">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="ecb6a-111">**оплидресервед**</span><span class="sxs-lookup"><span data-stu-id="ecb6a-111">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="ecb6a-112">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="ecb6a-112">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="ecb6a-113">**вопи**</span><span class="sxs-lookup"><span data-stu-id="ecb6a-113">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="ecb6a-114">[**DRM \_ Структура \_ \_ \_ идентификаторов защиты видео**](drmdrm-video-output-protection-ids.md) , содержащая идентификаторы защиты видео, которые применяются к воспроизведению содержимого.</span><span class="sxs-lookup"><span data-stu-id="ecb6a-114">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecb6a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ecb6a-115">Requirements</span></span>



| <span data-ttu-id="ecb6a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ecb6a-116">Requirement</span></span> | <span data-ttu-id="ecb6a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ecb6a-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb6a-118">Header</span><span class="sxs-lookup"><span data-stu-id="ecb6a-118">Header</span></span><br/> | <dl> <span data-ttu-id="ecb6a-119"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecb6a-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb6a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecb6a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb6a-121">**\_ОПЛ копирования \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="ecb6a-121">**DRM\_COPY\_OPL**</span></span>](drmdrm-copy-opl.md)
</dt> <dt>

[<span data-ttu-id="ecb6a-122">**DRM \_ Play \_ ОПЛ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="ecb6a-122">**DRM\_PLAY\_OPL\_EX**</span></span>](drm-play-opl-ex.md)
</dt> <dt>

[<span data-ttu-id="ecb6a-123">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="ecb6a-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





