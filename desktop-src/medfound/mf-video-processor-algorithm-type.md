---
description: Определяет алгоритмы для обработчика видео, используемого \_ \_ алгоритмом обработчика видео MF \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: Перечисление MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 604fee61ae4b6a34d876de8c2863ee6dddad73d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692538"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a><span data-ttu-id="90710-103">\_ \_ \_ Перечисление типов алгоритмов ВИДЕОпроцессора MF \_</span><span class="sxs-lookup"><span data-stu-id="90710-103">MF\_VIDEO\_PROCESSOR\_ALGORITHM\_TYPE enumeration</span></span>

<span data-ttu-id="90710-104">Определяет алгоритмы для обработчика видео, используемого [ \_ \_ \_ алгоритмом обработчика видео MF](mf-video-processor-algorithm.md).</span><span class="sxs-lookup"><span data-stu-id="90710-104">Defines algorithms for the video processor which is use by [MF\_VIDEO\_PROCESSOR\_ALGORITHM](mf-video-processor-algorithm.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="90710-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90710-105">Syntax</span></span>


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a><span data-ttu-id="90710-106">Константы</span><span class="sxs-lookup"><span data-stu-id="90710-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="90710-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**\_ \_ алгоритм процессора видео \_ MF \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="90710-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="90710-108">режим по умолчанию подходит к балансу качества и скорости</span><span class="sxs-lookup"><span data-stu-id="90710-108">default mode favors a balance of quality and speed</span></span>

</dd> <dt>

<span data-ttu-id="90710-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**\_ \_ Алгоритм видеопроцессора MF \_ \_ МРФ \_ КРФ \_ 444**</span><span class="sxs-lookup"><span data-stu-id="90710-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_MRF\_CRF\_444**</span></span>
</dt> <dd>

<span data-ttu-id="90710-110">Обработчик видео всегда будет внутренне обрабатывать в АЙУВ и использовать фильтры высокого качества.</span><span class="sxs-lookup"><span data-stu-id="90710-110">The video processor will always internally process in AYUV and use high quality filters.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90710-111">Требования</span><span class="sxs-lookup"><span data-stu-id="90710-111">Requirements</span></span>



| <span data-ttu-id="90710-112">Требование</span><span class="sxs-lookup"><span data-stu-id="90710-112">Requirement</span></span> | <span data-ttu-id="90710-113">Значение</span><span class="sxs-lookup"><span data-stu-id="90710-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="90710-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90710-114">Minimum supported client</span></span><br/> | <span data-ttu-id="90710-115">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="90710-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="90710-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90710-116">Minimum supported server</span></span><br/> | <span data-ttu-id="90710-117">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="90710-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="90710-118">IDL</span><span class="sxs-lookup"><span data-stu-id="90710-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90710-119"><dt>Мфидл. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90710-119"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90710-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90710-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90710-121">Перечисления Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90710-121">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




