---
title: Атрибут MediaType
description: Атрибут MediaType — это тип содержимого элемента.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- Проигрыватель Windows Media, атрибут MediaType
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651817"
---
# <a name="mediatype-attribute"></a><span data-ttu-id="b24cd-104">Атрибут MediaType</span><span class="sxs-lookup"><span data-stu-id="b24cd-104">MediaType Attribute</span></span>

<span data-ttu-id="b24cd-105">Атрибут **mediaType** — это тип содержимого элемента.</span><span class="sxs-lookup"><span data-stu-id="b24cd-105">The **MediaType** attribute is the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b24cd-106">Применение</span><span class="sxs-lookup"><span data-stu-id="b24cd-106">Applies To</span></span>

-   [<span data-ttu-id="b24cd-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="b24cd-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="b24cd-108">Другие элементы</span><span class="sxs-lookup"><span data-stu-id="b24cd-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="b24cd-109">Элементы фото</span><span class="sxs-lookup"><span data-stu-id="b24cd-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="b24cd-110">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="b24cd-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="b24cd-111">Элементы Радио</span><span class="sxs-lookup"><span data-stu-id="b24cd-111">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="b24cd-112">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="b24cd-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b24cd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b24cd-113">Remarks</span></span>

<span data-ttu-id="b24cd-114">Этот атрибут хранится только в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="b24cd-114">This attribute is stored only in the library.</span></span>

<span data-ttu-id="b24cd-115">Этот атрибут имеет одно из следующих значений: "звук", "другое", "Фото", "список воспроизведения", "Радио" или "видео".</span><span class="sxs-lookup"><span data-stu-id="b24cd-115">This attribute has one of the following values: "audio", "other", "photo", "playlist", "radio", or "video".</span></span> <span data-ttu-id="b24cd-116">Используйте этот атрибут с параметром *медиаколлектион*. метод **жетбяттрибуте** для получения списка воспроизведения, содержащего все элементы определенного типа.</span><span class="sxs-lookup"><span data-stu-id="b24cd-116">Use this attribute with the *MediaCollection*.**getByAttribute** method to retrieve a playlist containing all of the items of a particular type.</span></span>

<span data-ttu-id="b24cd-117">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b24cd-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b24cd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b24cd-118">Requirements</span></span>



| <span data-ttu-id="b24cd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b24cd-119">Requirement</span></span> | <span data-ttu-id="b24cd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b24cd-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b24cd-121">Версия</span><span class="sxs-lookup"><span data-stu-id="b24cd-121">Version</span></span><br/> | <span data-ttu-id="b24cd-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b24cd-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b24cd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b24cd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b24cd-124">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="b24cd-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="b24cd-125">**Медиаколлектион. Жетбяттрибуте**</span><span class="sxs-lookup"><span data-stu-id="b24cd-125">**MediaCollection.getByAttribute**</span></span>](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





