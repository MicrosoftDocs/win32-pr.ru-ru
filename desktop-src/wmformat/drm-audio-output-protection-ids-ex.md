---
title: Структура DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX (Вмдрмсдк. h)
description: '\_ \_ \_ Структура ИД защиты звука в \_ DRM \_ содержит список идентификаторов защиты звука. Эта структура расширяет \_ \_ \_ идентификаторы защиты звука DRM \_ , добавляя номер версии.'
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- Формат DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718114"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a><span data-ttu-id="15ee8-106">\_ \_ \_ Идентификаторы защиты аудио вывода DRM \_ \_ Структура ex</span><span class="sxs-lookup"><span data-stu-id="15ee8-106">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="15ee8-107">Структура **\_ \_ \_ \_ \_ ИД защиты звука в DRM** содержит список идентификаторов защиты звука.</span><span class="sxs-lookup"><span data-stu-id="15ee8-107">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX** structure contains a list of audio output protection identifiers.</span></span> <span data-ttu-id="15ee8-108">Эта структура расширяет **\_ \_ \_ \_ идентификаторы защиты звука DRM** , добавляя номер версии.</span><span class="sxs-lookup"><span data-stu-id="15ee8-108">This structure extends **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ee8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15ee8-109">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="15ee8-110">Члены</span><span class="sxs-lookup"><span data-stu-id="15ee8-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="15ee8-111">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="15ee8-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="15ee8-112">Номер версии.</span><span class="sxs-lookup"><span data-stu-id="15ee8-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="15ee8-113">**центриес**</span><span class="sxs-lookup"><span data-stu-id="15ee8-113">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="15ee8-114">Число записей в массиве **ргаоп** .</span><span class="sxs-lookup"><span data-stu-id="15ee8-114">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="15ee8-115">**ргаоп**</span><span class="sxs-lookup"><span data-stu-id="15ee8-115">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="15ee8-116">Массив структур **для \_ \_ \_ защиты \_ звука DRM** .</span><span class="sxs-lookup"><span data-stu-id="15ee8-116">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="15ee8-117">**DRM \_ \_Защита звука \_ , \_ например** , представляет собой тип, определенный как [**\_ \_ Защита \_ выходных данных DRM**](drm-output-protection-ex.md), например.</span><span class="sxs-lookup"><span data-stu-id="15ee8-117">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15ee8-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15ee8-118">Remarks</span></span>

<span data-ttu-id="15ee8-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="15ee8-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="15ee8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="15ee8-120">Requirements</span></span>



| <span data-ttu-id="15ee8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="15ee8-121">Requirement</span></span> | <span data-ttu-id="15ee8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="15ee8-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15ee8-123">Header</span><span class="sxs-lookup"><span data-stu-id="15ee8-123">Header</span></span><br/> | <dl> <span data-ttu-id="15ee8-124"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="15ee8-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15ee8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15ee8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ee8-126">**\_ \_ \_ идентификаторы защиты звука в DRM \_**</span><span class="sxs-lookup"><span data-stu-id="15ee8-126">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="15ee8-127">**\_ \_ \_ идентификаторы защиты вывода видео DRM \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="15ee8-127">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="15ee8-128">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="15ee8-128">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





