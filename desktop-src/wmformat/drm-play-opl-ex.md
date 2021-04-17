---
title: Структура DRM_PLAY_OPL_EX (Вмдрмсдк. h)
description: Структура DRM \_ Play \_ ОПЛ \_ ex содержит сведения об уровнях защиты выходных данных (оплс), указанных в лицензии на действия воспроизведения.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- Формат DRM_PLAY_OPL_EX структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704527"
---
# <a name="drm_play_opl_ex-structure"></a><span data-ttu-id="d8187-105">\_Структура DRM Play \_ ОПЛ \_ ex</span><span class="sxs-lookup"><span data-stu-id="d8187-105">DRM\_PLAY\_OPL\_EX structure</span></span>

<span data-ttu-id="d8187-106">Структура **DRM \_ Play \_ ОПЛ \_ ex** содержит сведения об уровнях защиты выходных данных (оплс), указанных в лицензии на действия воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d8187-106">The **DRM\_PLAY\_OPL\_EX** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8187-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8187-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="d8187-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d8187-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d8187-109">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="d8187-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d8187-110">Номер версии.</span><span class="sxs-lookup"><span data-stu-id="d8187-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="d8187-111">**минопл**</span><span class="sxs-lookup"><span data-stu-id="d8187-111">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="d8187-112">[**DRM \_ Минимальная \_ Структура \_ \_ уровней защиты выходных данных**](drmdrm-minimum-output-protection-levels.md) , содержащая минимум ОПЛ, необходимый для воспроизведения содержимого в различных форматах.</span><span class="sxs-lookup"><span data-stu-id="d8187-112">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="d8187-113">**оплидресервед**</span><span class="sxs-lookup"><span data-stu-id="d8187-113">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="d8187-114">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="d8187-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="d8187-115">**вопи**</span><span class="sxs-lookup"><span data-stu-id="d8187-115">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="d8187-116">[**DRM \_ Структура \_ \_ \_ идентификаторов защиты видео**](drmdrm-video-output-protection-ids.md) , содержащая идентификаторы защиты видео, которые применяются к воспроизведению содержимого.</span><span class="sxs-lookup"><span data-stu-id="d8187-116">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8187-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8187-117">Remarks</span></span>

<span data-ttu-id="d8187-118">Эта структура идентична структуре **DRM \_ Play \_ ОПЛ** , за исключением того, что она включает номер версии.</span><span class="sxs-lookup"><span data-stu-id="d8187-118">This structure is identical to the **DRM\_PLAY\_OPL** structure, except that it includes a version number.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8187-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d8187-119">Requirements</span></span>



| <span data-ttu-id="d8187-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d8187-120">Requirement</span></span> | <span data-ttu-id="d8187-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d8187-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8187-122">Header</span><span class="sxs-lookup"><span data-stu-id="d8187-122">Header</span></span><br/> | <dl> <span data-ttu-id="d8187-123"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8187-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8187-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8187-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8187-125">**DRM \_ Play \_ ОПЛ**</span><span class="sxs-lookup"><span data-stu-id="d8187-125">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="d8187-126">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="d8187-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





