---
title: Структура DRM_AUDIO_OUTPUT_PROTECTION_IDS (Вмдрмсдк. h)
description: '\_ \_ \_ Структура идентификаторов защиты звукового выхода DRM \_ содержит список идентификаторов защиты звука.'
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- Формат DRM_AUDIO_OUTPUT_PROTECTION_IDS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718113"
---
# <a name="drm_audio_output_protection_ids-structure"></a><span data-ttu-id="e18e9-105">\_ \_ \_ Структура идентификаторов защиты ЗВУКового выхода DRM \_</span><span class="sxs-lookup"><span data-stu-id="e18e9-105">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="e18e9-106">Структура **\_ \_ \_ \_ идентификаторов защиты звукового выхода DRM** содержит список идентификаторов защиты звука.</span><span class="sxs-lookup"><span data-stu-id="e18e9-106">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** structure contains a list of audio output protection identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e18e9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e18e9-107">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="e18e9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e18e9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e18e9-109">**центриес**</span><span class="sxs-lookup"><span data-stu-id="e18e9-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="e18e9-110">Число записей в массиве **ргаоп** .</span><span class="sxs-lookup"><span data-stu-id="e18e9-110">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="e18e9-111">**ргаоп**</span><span class="sxs-lookup"><span data-stu-id="e18e9-111">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="e18e9-112">Массив структур **\_ \_ \_ защиты выходного звука DRM** .</span><span class="sxs-lookup"><span data-stu-id="e18e9-112">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="e18e9-113">**DRM \_ \_ \_ Защита звука** — это тип, определенный как [**\_ \_ Защита выходных данных DRM**](drm-output-protection.md).</span><span class="sxs-lookup"><span data-stu-id="e18e9-113">**DRM\_AUDIO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e18e9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e18e9-114">Remarks</span></span>

<span data-ttu-id="e18e9-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="e18e9-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e18e9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e18e9-116">Requirements</span></span>



| <span data-ttu-id="e18e9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e18e9-117">Requirement</span></span> | <span data-ttu-id="e18e9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e18e9-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e18e9-119">Header</span><span class="sxs-lookup"><span data-stu-id="e18e9-119">Header</span></span><br/> | <dl> <span data-ttu-id="e18e9-120"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="e18e9-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e18e9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e18e9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e18e9-122">**\_ \_ \_ идентификаторы защиты аудио вывода DRM \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="e18e9-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="e18e9-123">**\_ \_ \_ идентификаторы защиты вывода видео DRM \_**</span><span class="sxs-lookup"><span data-stu-id="e18e9-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="e18e9-124">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="e18e9-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





