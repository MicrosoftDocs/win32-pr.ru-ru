---
title: Структура DRM_OUTPUT_PROTECTION (Вмдрмсдк. h)
description: '\_Структура защиты выходных данных DRM \_ содержит сведения о технологии защиты выходных данных.'
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- Формат DRM_OUTPUT_PROTECTION структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704528"
---
# <a name="drm_output_protection-structure"></a><span data-ttu-id="70153-105">\_Структура защиты выходных данных DRM \_</span><span class="sxs-lookup"><span data-stu-id="70153-105">DRM\_OUTPUT\_PROTECTION structure</span></span>

<span data-ttu-id="70153-106">Структура **\_ \_ защиты выходных данных DRM** содержит сведения о технологии защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="70153-106">The **DRM\_OUTPUT\_PROTECTION** structure holds information about an output protection technology.</span></span>

## <a name="syntax"></a><span data-ttu-id="70153-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70153-107">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="70153-108">Члены</span><span class="sxs-lookup"><span data-stu-id="70153-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="70153-109">**guidId**</span><span class="sxs-lookup"><span data-stu-id="70153-109">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="70153-110">Идентификатор GUID, определяющий технологию защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="70153-110">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="70153-111">**бконфигдата**</span><span class="sxs-lookup"><span data-stu-id="70153-111">**bConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="70153-112">Данные конфигурации для технологии.</span><span class="sxs-lookup"><span data-stu-id="70153-112">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70153-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70153-113">Remarks</span></span>

<span data-ttu-id="70153-114">**DRM \_ Защита \_ аудио \_** и **\_ видео \_ \_ DRM** в инструкциях **typedef** определяется как **\_ \_ Защита выходных данных DRM** .</span><span class="sxs-lookup"><span data-stu-id="70153-114">**DRM\_AUDIO\_OUTPUT\_PROTECTION** and **DRM\_VIDEO\_OUTPUT\_PROTECTION** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="70153-115">Требования</span><span class="sxs-lookup"><span data-stu-id="70153-115">Requirements</span></span>



| <span data-ttu-id="70153-116">Требование</span><span class="sxs-lookup"><span data-stu-id="70153-116">Requirement</span></span> | <span data-ttu-id="70153-117">Значение</span><span class="sxs-lookup"><span data-stu-id="70153-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70153-118">Header</span><span class="sxs-lookup"><span data-stu-id="70153-118">Header</span></span><br/> | <dl> <span data-ttu-id="70153-119"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="70153-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70153-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70153-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70153-121">**\_Защита вывода DRM, \_ \_ пример**</span><span class="sxs-lookup"><span data-stu-id="70153-121">**DRM\_OUTPUT\_PROTECTION\_EX**</span></span>](drm-output-protection-ex.md)
</dt> <dt>

[<span data-ttu-id="70153-122">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="70153-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





