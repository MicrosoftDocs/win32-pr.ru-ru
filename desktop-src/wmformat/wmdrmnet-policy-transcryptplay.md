---
title: Структура WMDRMNET_POLICY_TRANSCRYPTPLAY (Вмдрмсдк. h)
description: '\_ \_ Структура ТРАНСКРИПТПЛАЙ политики вмдрмнет содержит сведения о политике для воспроизведения содержимого с помощью Windows Media DRM для сетевых устройств.'
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- Формат WMDRMNET_POLICY_TRANSCRYPTPLAY структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647962"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a><span data-ttu-id="b54b5-105">\_ \_ Структура ТРАНСКРИПТПЛАЙ политики вмдрмнет</span><span class="sxs-lookup"><span data-stu-id="b54b5-105">WMDRMNET\_POLICY\_TRANSCRYPTPLAY structure</span></span>

<span data-ttu-id="b54b5-106">Структура **\_ \_ транскриптплай политики вмдрмнет** содержит сведения о политике для воспроизведения содержимого с помощью Windows Media DRM для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="b54b5-106">The **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure holds the policy information for playing content using Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b54b5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b54b5-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a><span data-ttu-id="b54b5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b54b5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b54b5-109">**Globals**</span><span class="sxs-lookup"><span data-stu-id="b54b5-109">**globals**</span></span>
</dt> <dd>

<span data-ttu-id="b54b5-110">Структура глобальной политики.</span><span class="sxs-lookup"><span data-stu-id="b54b5-110">Global policy structure.</span></span>

</dd> <dt>

<span data-ttu-id="b54b5-111">**плайоплс**</span><span class="sxs-lookup"><span data-stu-id="b54b5-111">**playOPLs**</span></span>
</dt> <dd>

<span data-ttu-id="b54b5-112">Уровни защиты выходных данных для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b54b5-112">Output protection levels for playback.</span></span> <span data-ttu-id="b54b5-113">**Вмдрмнет \_ ПОЛИТИКА \_ Play \_ ОПЛ** — это тип, определенный как [**DRM \_ Play \_ ОПЛ \_ ex**](drm-play-opl-ex.md).</span><span class="sxs-lookup"><span data-stu-id="b54b5-113">**WMDRMNET\_POLICY\_PLAY\_OPL** is a type defined as [**DRM\_PLAY\_OPL\_EX**](drm-play-opl-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b54b5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b54b5-114">Remarks</span></span>

<span data-ttu-id="b54b5-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="b54b5-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b54b5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b54b5-116">Requirements</span></span>



| <span data-ttu-id="b54b5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b54b5-117">Requirement</span></span> | <span data-ttu-id="b54b5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b54b5-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b54b5-119">Header</span><span class="sxs-lookup"><span data-stu-id="b54b5-119">Header</span></span><br/> | <dl> <span data-ttu-id="b54b5-120"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="b54b5-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b54b5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b54b5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b54b5-122">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="b54b5-122">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="b54b5-123">**\_Политика вмдрмнет**</span><span class="sxs-lookup"><span data-stu-id="b54b5-123">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





