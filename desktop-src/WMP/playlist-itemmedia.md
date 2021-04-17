---
title: Список воспроизведения. Итеммедиа
description: Атрибут Итеммедиа извлекает объект мультимедиа, соответствующий заданному индексу в элементе списка воспроизведения.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- Проигрыватель Windows Media Player. Итеммедиа
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657265"
---
# <a name="playlistitemmedia"></a><span data-ttu-id="1773a-104">Список воспроизведения. Итеммедиа</span><span class="sxs-lookup"><span data-stu-id="1773a-104">PLAYLIST.itemMedia</span></span>

<span data-ttu-id="1773a-105">Атрибут **итеммедиа** извлекает объект **мультимедиа** , соответствующий заданному индексу в элементе **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="1773a-105">The **itemMedia** attribute retrieves the **Media** object corresponding to the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a><span data-ttu-id="1773a-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1773a-106">Possible Values</span></span>

<span data-ttu-id="1773a-107">Этот атрибут является объектом **мультимедиа** , предназначенным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1773a-107">This attribute is a read-only **Media** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1773a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1773a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1773a-109"><span id="index"></span><span id="INDEX"></span>*номер*</span><span class="sxs-lookup"><span data-stu-id="1773a-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="1773a-110">**Число**(**длинное**), содержащее индекс элемента списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1773a-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1773a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1773a-111">Remarks</span></span>

<span data-ttu-id="1773a-112">Свойство **итеммедиа** будет возвращать объекты мультимедиа, развернутые в элементе **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="1773a-112">The **itemMedia** property will return media objects that are expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="1773a-113">Например, если имеется список воспроизведения, содержащий три клипа мультимедиа, которые не разворачиваются в элементе **списка воспроизведения** , **итеммедиа**(0) вернет список воспроизведения в качестве объекта мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1773a-113">For example, if there is a playlist that contains three media clips that is not expanded in the **PLAYLIST** element, **itemMedia**(0) will return the playlist as the media object.</span></span> <span data-ttu-id="1773a-114">Если список воспроизведения расширен, **итеммедиа**(0) вернет первый клип из списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1773a-114">If the playlist is expanded, **itemMedia**(0) will return the first media clip in the playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="1773a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1773a-115">Requirements</span></span>



| <span data-ttu-id="1773a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1773a-116">Requirement</span></span> | <span data-ttu-id="1773a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1773a-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1773a-118">Версия</span><span class="sxs-lookup"><span data-stu-id="1773a-118">Version</span></span><br/> | <span data-ttu-id="1773a-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1773a-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1773a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1773a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1773a-121">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="1773a-121">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1773a-122">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="1773a-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





