---
title: Структура DRM_OUTPUT_PROTECTION_EX (Вмдрмсдк. h)
description: Структура для \_ защиты выходных данных DRM \_ \_ содержит сведения о технологии защиты выходных данных. Эта структура расширяет \_ защиту выхода DRM \_ путем добавления номера версии.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- Формат DRM_OUTPUT_PROTECTION_EX структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708573"
---
# <a name="drm_output_protection_ex-structure"></a><span data-ttu-id="e74ed-106">\_Структура для \_ защиты \_ вывода DRM</span><span class="sxs-lookup"><span data-stu-id="e74ed-106">DRM\_OUTPUT\_PROTECTION\_EX structure</span></span>

<span data-ttu-id="e74ed-107">Структура **для \_ защиты выходных данных \_ \_ DRM** содержит сведения о технологии защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e74ed-107">The **DRM\_OUTPUT\_PROTECTION\_EX** structure holds information about an output protection technology.</span></span> <span data-ttu-id="e74ed-108">Эта структура расширяет **\_ \_ защиту выхода DRM** путем добавления номера версии.</span><span class="sxs-lookup"><span data-stu-id="e74ed-108">This structure extends **DRM\_OUTPUT\_PROTECTION** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e74ed-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e74ed-109">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="e74ed-110">Члены</span><span class="sxs-lookup"><span data-stu-id="e74ed-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e74ed-111">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="e74ed-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e74ed-112">Номер версии.</span><span class="sxs-lookup"><span data-stu-id="e74ed-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="e74ed-113">**guidId**</span><span class="sxs-lookup"><span data-stu-id="e74ed-113">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="e74ed-114">Идентификатор GUID, определяющий технологию защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e74ed-114">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="e74ed-115">**двконфигдата**</span><span class="sxs-lookup"><span data-stu-id="e74ed-115">**dwConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="e74ed-116">Данные конфигурации для технологии.</span><span class="sxs-lookup"><span data-stu-id="e74ed-116">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e74ed-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e74ed-117">Remarks</span></span>

<span data-ttu-id="e74ed-118">**DRM \_ Защита звука с аудио \_ и \_ \_** защитой, например, в инструкциях **typedef** определяется как **\_ \_ Защита выходных данных DRM** . **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e74ed-118">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** and **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="e74ed-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e74ed-119">Requirements</span></span>



| <span data-ttu-id="e74ed-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e74ed-120">Requirement</span></span> | <span data-ttu-id="e74ed-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e74ed-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e74ed-122">Header</span><span class="sxs-lookup"><span data-stu-id="e74ed-122">Header</span></span><br/> | <dl> <span data-ttu-id="e74ed-123"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="e74ed-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e74ed-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e74ed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e74ed-125">**\_Защита вывода \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="e74ed-125">**DRM\_OUTPUT\_PROTECTION**</span></span>](drm-output-protection.md)
</dt> <dt>

[<span data-ttu-id="e74ed-126">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="e74ed-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





