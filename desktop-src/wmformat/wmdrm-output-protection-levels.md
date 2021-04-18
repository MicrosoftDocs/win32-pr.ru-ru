---
title: Структура WMDRM_OUTPUT_PROTECTION_LEVELS (Вмдрмсдк. h)
description: '\_ \_ Структура уровней защиты WMDRM OUTPUT \_ содержит уровни защиты выходных данных (оплс), необходимые для выполнения различных действий в лицензии.'
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- Формат WMDRM_OUTPUT_PROTECTION_LEVELS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717864"
---
# <a name="wmdrm_output_protection_levels-structure"></a><span data-ttu-id="9f825-105">\_ \_ Структура уровней защиты данных WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="9f825-105">WMDRM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="9f825-106">Структура **\_ \_ \_ уровней защиты WMDRM Output** содержит уровни защиты выходных данных (оплс), необходимые для выполнения различных действий в лицензии.</span><span class="sxs-lookup"><span data-stu-id="9f825-106">The **WMDRM\_OUTPUT\_PROTECTION\_LEVELS** structure contains the output protections levels (OPLs) required by a license to perform various actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f825-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f825-107">Syntax</span></span>


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
} ;
```



## <a name="members"></a><span data-ttu-id="9f825-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9f825-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9f825-109">**вкомпресседдигиталвидео**</span><span class="sxs-lookup"><span data-stu-id="9f825-109">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="9f825-110">Минимальный ОПЛ, необходимый для получения сжатого цифрового видео.</span><span class="sxs-lookup"><span data-stu-id="9f825-110">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="9f825-111">**вункомпресседдигиталвидео**</span><span class="sxs-lookup"><span data-stu-id="9f825-111">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="9f825-112">Минимальный ОПЛ, необходимый для получения несжатого цифрового видео.</span><span class="sxs-lookup"><span data-stu-id="9f825-112">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="9f825-113">**ваналогвидео**</span><span class="sxs-lookup"><span data-stu-id="9f825-113">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="9f825-114">Минимальный ОПЛ, необходимый для получения аналогового видео.</span><span class="sxs-lookup"><span data-stu-id="9f825-114">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="9f825-115">**вкомпресседдигиталаудио**</span><span class="sxs-lookup"><span data-stu-id="9f825-115">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="9f825-116">Для получения сжатого цифрового аудио требуется минимум ОПЛ.</span><span class="sxs-lookup"><span data-stu-id="9f825-116">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="9f825-117">**вункомпресседдигиталаудио**</span><span class="sxs-lookup"><span data-stu-id="9f825-117">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="9f825-118">Минимальный ОПЛ, необходимый для получения несжатого цифрового аудио.</span><span class="sxs-lookup"><span data-stu-id="9f825-118">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="9f825-119">**вминимумкопипротектионлевел**</span><span class="sxs-lookup"><span data-stu-id="9f825-119">**wMinimumCopyProtectionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="9f825-120">Для копирования содержимого требуется минимум ОПЛ.</span><span class="sxs-lookup"><span data-stu-id="9f825-120">Minimum OPL required to copy the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f825-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f825-121">Remarks</span></span>

<span data-ttu-id="9f825-122">Эта структура используется методом [**ивмдрмлиценсе:: жетаутпутпротектионлевелс**](iwmdrmlicense-getoutputprotectionlevels.md) .</span><span class="sxs-lookup"><span data-stu-id="9f825-122">This structure is used by the [**IWMDRMLicense::GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f825-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9f825-123">Requirements</span></span>



| <span data-ttu-id="9f825-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9f825-124">Requirement</span></span> | <span data-ttu-id="9f825-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9f825-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f825-126">Header</span><span class="sxs-lookup"><span data-stu-id="9f825-126">Header</span></span><br/> | <dl> <span data-ttu-id="9f825-127"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f825-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f825-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f825-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f825-129">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="9f825-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





