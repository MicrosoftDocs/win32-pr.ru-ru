---
title: Атрибут Медиаконтенттипес
description: Атрибут Медиаконтенттипес задает тип содержимого элемента.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- Медиаконтенттипес атрибут Windows Media Player
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8979864151e029abf2731f6f0b4663e078a2c061
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651818"
---
# <a name="mediacontenttypes-attribute"></a><span data-ttu-id="f4aca-104">Атрибут Медиаконтенттипес</span><span class="sxs-lookup"><span data-stu-id="f4aca-104">MediaContentTypes Attribute</span></span>

<span data-ttu-id="f4aca-105">Атрибут **медиаконтенттипес** задает тип содержимого элемента.</span><span class="sxs-lookup"><span data-stu-id="f4aca-105">The **MediaContentTypes** attribute specifies the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f4aca-106">Применение</span><span class="sxs-lookup"><span data-stu-id="f4aca-106">Applies To</span></span>

-   [<span data-ttu-id="f4aca-107">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="f4aca-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="f4aca-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4aca-108">Remarks</span></span>

<span data-ttu-id="f4aca-109">Этот атрибут может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f4aca-109">This attribute can be one of the following values:</span></span>



| <span data-ttu-id="f4aca-110">Значение</span><span class="sxs-lookup"><span data-stu-id="f4aca-110">Value</span></span> | <span data-ttu-id="f4aca-111">Значение</span><span class="sxs-lookup"><span data-stu-id="f4aca-111">Meaning</span></span>                                |
|-------|----------------------------------------|
| <span data-ttu-id="f4aca-112">1</span><span class="sxs-lookup"><span data-stu-id="f4aca-112">1</span></span>     | <span data-ttu-id="f4aca-113">Список воспроизведения содержит звуковое содержимое.</span><span class="sxs-lookup"><span data-stu-id="f4aca-113">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="f4aca-114">2</span><span class="sxs-lookup"><span data-stu-id="f4aca-114">2</span></span>     | <span data-ttu-id="f4aca-115">Будет предоставляться.</span><span class="sxs-lookup"><span data-stu-id="f4aca-115">To be supplied.</span></span>                        |
| <span data-ttu-id="f4aca-116">3</span><span class="sxs-lookup"><span data-stu-id="f4aca-116">3</span></span>     | <span data-ttu-id="f4aca-117">Список воспроизведения содержит звуковое содержимое.</span><span class="sxs-lookup"><span data-stu-id="f4aca-117">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="f4aca-118">4</span><span class="sxs-lookup"><span data-stu-id="f4aca-118">4</span></span>     | <span data-ttu-id="f4aca-119">Список воспроизведения содержит видеоматериалы.</span><span class="sxs-lookup"><span data-stu-id="f4aca-119">The playlist contains video content.</span></span>   |
| <span data-ttu-id="f4aca-120">5</span><span class="sxs-lookup"><span data-stu-id="f4aca-120">5</span></span>     | <span data-ttu-id="f4aca-121">Список воспроизведения содержит содержимое изображения.</span><span class="sxs-lookup"><span data-stu-id="f4aca-121">The playlist contains picture content.</span></span> |
| <span data-ttu-id="f4aca-122">6</span><span class="sxs-lookup"><span data-stu-id="f4aca-122">6</span></span>     | <span data-ttu-id="f4aca-123">Список воспроизведения содержит ТВ-содержимое.</span><span class="sxs-lookup"><span data-stu-id="f4aca-123">The playlist contains TV content.</span></span>      |



 

<span data-ttu-id="f4aca-124">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f4aca-124">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4aca-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f4aca-125">Requirements</span></span>



| <span data-ttu-id="f4aca-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f4aca-126">Requirement</span></span> | <span data-ttu-id="f4aca-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f4aca-127">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="f4aca-128">Версия</span><span class="sxs-lookup"><span data-stu-id="f4aca-128">Version</span></span><br/> | <span data-ttu-id="f4aca-129">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f4aca-129">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4aca-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4aca-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4aca-131">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="f4aca-131">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





