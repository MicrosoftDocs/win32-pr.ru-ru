---
title: Структура DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS (Вмдрмсдк. h)
description: '\_ \_ \_ Структура уровней минимальной защиты от DRM \_ содержит минимальные уровни защиты выходных данных (оплс) для воспроизведения содержимого различных типов. Устройство должно поддерживать минимальный ОПЛ для типа данных, чтобы получить данные этого типа из модуля чтения.'
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- Формат DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704112"
---
# <a name="drm_minimum_output_protection_levels-structure"></a><span data-ttu-id="835f7-106">\_Минимальная \_ \_ \_ Структура уровней защиты выходных данных DRM</span><span class="sxs-lookup"><span data-stu-id="835f7-106">DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="835f7-107">Структура **\_ уровней минимальной \_ \_ защиты от \_ DRM** содержит минимальные уровни защиты выходных данных (оплс) для воспроизведения содержимого различных типов.</span><span class="sxs-lookup"><span data-stu-id="835f7-107">The **DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS** structure holds the minimum output protection levels (OPLs) for playback of various types of content.</span></span> <span data-ttu-id="835f7-108">Устройство должно поддерживать минимальный ОПЛ для типа данных, чтобы получить данные этого типа из модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="835f7-108">A device must support the minimum OPL for a type of data to receive that type of data from the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="835f7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="835f7-109">Syntax</span></span>


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a><span data-ttu-id="835f7-110">Члены</span><span class="sxs-lookup"><span data-stu-id="835f7-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="835f7-111">**вкомпресседдигиталвидео**</span><span class="sxs-lookup"><span data-stu-id="835f7-111">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="835f7-112">Минимальный ОПЛ, необходимый для получения сжатого цифрового видео.</span><span class="sxs-lookup"><span data-stu-id="835f7-112">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="835f7-113">**вункомпресседдигиталвидео**</span><span class="sxs-lookup"><span data-stu-id="835f7-113">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="835f7-114">Минимальный ОПЛ, необходимый для получения несжатого цифрового видео.</span><span class="sxs-lookup"><span data-stu-id="835f7-114">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="835f7-115">**ваналогвидео**</span><span class="sxs-lookup"><span data-stu-id="835f7-115">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="835f7-116">Минимальный ОПЛ, необходимый для получения аналогового видео.</span><span class="sxs-lookup"><span data-stu-id="835f7-116">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="835f7-117">**вкомпресседдигиталаудио**</span><span class="sxs-lookup"><span data-stu-id="835f7-117">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="835f7-118">Для получения сжатого цифрового аудио требуется минимум ОПЛ.</span><span class="sxs-lookup"><span data-stu-id="835f7-118">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="835f7-119">**вункомпресседдигиталаудио**</span><span class="sxs-lookup"><span data-stu-id="835f7-119">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="835f7-120">Минимальный ОПЛ, необходимый для получения несжатого цифрового аудио.</span><span class="sxs-lookup"><span data-stu-id="835f7-120">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="835f7-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="835f7-121">Remarks</span></span>

<span data-ttu-id="835f7-122">Эта структура используется в качестве члена структуры [**DRM \_ Play \_ ОПЛ**](drmdrm-play-opl.md) .</span><span class="sxs-lookup"><span data-stu-id="835f7-122">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="835f7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="835f7-123">Requirements</span></span>



| <span data-ttu-id="835f7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="835f7-124">Requirement</span></span> | <span data-ttu-id="835f7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="835f7-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="835f7-126">Header</span><span class="sxs-lookup"><span data-stu-id="835f7-126">Header</span></span><br/> | <dl> <span data-ttu-id="835f7-127"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="835f7-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="835f7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="835f7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="835f7-129">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="835f7-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





