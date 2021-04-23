---
title: Атрибут Албумидалбумартист
description: Атрибут Албумидалбумартист является уникальным идентификатором для альбома.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- Албумидалбумартист атрибут Windows Media Player
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1925f40a50b15efcd339ad949d5d54ddb915cbe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698939"
---
# <a name="albumidalbumartist-attribute"></a><span data-ttu-id="dbf38-104">Атрибут Албумидалбумартист</span><span class="sxs-lookup"><span data-stu-id="dbf38-104">AlbumIDAlbumArtist Attribute</span></span>

<span data-ttu-id="dbf38-105">Атрибут **албумидалбумартист** является уникальным идентификатором для альбома.</span><span class="sxs-lookup"><span data-stu-id="dbf38-105">The **AlbumIDAlbumArtist** attribute is a unique identifier for the album.</span></span>

## <a name="applies-to"></a><span data-ttu-id="dbf38-106">Применение</span><span class="sxs-lookup"><span data-stu-id="dbf38-106">Applies To</span></span>

-   [<span data-ttu-id="dbf38-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="dbf38-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="dbf38-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbf38-108">Remarks</span></span>

<span data-ttu-id="dbf38-109">Этот атрибут хранится только в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="dbf38-109">This attribute is stored only in the library.</span></span>

<span data-ttu-id="dbf38-110">Уникальный идентификатор представляет собой сочетание названия альбома и имени исполнителя альбома.</span><span class="sxs-lookup"><span data-stu-id="dbf38-110">The unique identifier is a combination of the album title and the album artist name.</span></span> <span data-ttu-id="dbf38-111">В этом атрибуте сначала появляется имя исполнителя альбома.</span><span class="sxs-lookup"><span data-stu-id="dbf38-111">In this attribute, the album artist name comes first.</span></span> <span data-ttu-id="dbf38-112">При использовании метода [медиаколлектион. жетаттрибутестрингколлектион](mediacollection-getattributestringcollection.md) для получения объекта **StringCollection** с помощью этого атрибута значения сортируются по имени исполнителя альбома.</span><span class="sxs-lookup"><span data-stu-id="dbf38-112">When you use the [MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) method to get a **StringCollection** object using this attribute, the values are sorted by album artist name.</span></span>

<span data-ttu-id="dbf38-113">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="dbf38-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf38-114">Требования</span><span class="sxs-lookup"><span data-stu-id="dbf38-114">Requirements</span></span>



| <span data-ttu-id="dbf38-115">Требование</span><span class="sxs-lookup"><span data-stu-id="dbf38-115">Requirement</span></span> | <span data-ttu-id="dbf38-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dbf38-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="dbf38-117">Версия</span><span class="sxs-lookup"><span data-stu-id="dbf38-117">Version</span></span><br/> | <span data-ttu-id="dbf38-118">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="dbf38-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dbf38-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbf38-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf38-120">**Атрибут Албумид**</span><span class="sxs-lookup"><span data-stu-id="dbf38-120">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="dbf38-121">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="dbf38-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





