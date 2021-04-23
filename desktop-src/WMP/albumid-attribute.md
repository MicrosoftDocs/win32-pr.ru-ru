---
title: Атрибут Албумид
description: Атрибут Албумид является уникальным идентификатором для альбома.
ms.assetid: 0412d91a-11a7-434c-8717-a71d85655679
keywords:
- Албумид атрибут Windows Media Player
topic_type:
- apiref
api_name:
- AlbumID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339253c82554579fa549371e2ebe4cb2f1926cc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699257"
---
# <a name="albumid-attribute"></a><span data-ttu-id="a0f68-104">Атрибут Албумид</span><span class="sxs-lookup"><span data-stu-id="a0f68-104">AlbumID Attribute</span></span>

<span data-ttu-id="a0f68-105">Атрибут **албумид** является уникальным идентификатором для альбома.</span><span class="sxs-lookup"><span data-stu-id="a0f68-105">The **AlbumID** attribute is a unique identifier for the album.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a0f68-106">Применение</span><span class="sxs-lookup"><span data-stu-id="a0f68-106">Applies To</span></span>

-   [<span data-ttu-id="a0f68-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="a0f68-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="a0f68-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0f68-108">Remarks</span></span>

<span data-ttu-id="a0f68-109">Этот атрибут хранится только в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a0f68-109">This attribute is stored only in the library.</span></span>

<span data-ttu-id="a0f68-110">Уникальный идентификатор представляет собой сочетание названия альбома и имени исполнителя альбома.</span><span class="sxs-lookup"><span data-stu-id="a0f68-110">The unique identifier is a combination of the album title and the album artist name.</span></span> <span data-ttu-id="a0f68-111">В этом атрибуте сначала появляется заголовок альбома.</span><span class="sxs-lookup"><span data-stu-id="a0f68-111">In this attribute, the album title comes first.</span></span> <span data-ttu-id="a0f68-112">При использовании метода [медиаколлектион. жетаттрибутестрингколлектион](mediacollection-getattributestringcollection.md) для получения объекта **StringCollection** с помощью этого атрибута значения сортируются по названию альбома.</span><span class="sxs-lookup"><span data-stu-id="a0f68-112">When you use the [MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) method to get a **StringCollection** object using this attribute, the values are sorted by album title.</span></span>

<span data-ttu-id="a0f68-113">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f68-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f68-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a0f68-114">Requirements</span></span>



| <span data-ttu-id="a0f68-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a0f68-115">Requirement</span></span> | <span data-ttu-id="a0f68-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a0f68-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="a0f68-117">Версия</span><span class="sxs-lookup"><span data-stu-id="a0f68-117">Version</span></span><br/> | <span data-ttu-id="a0f68-118">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a0f68-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a0f68-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0f68-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f68-120">**Атрибут Албумидалбумартист**</span><span class="sxs-lookup"><span data-stu-id="a0f68-120">**AlbumIDAlbumArtist Attribute**</span></span>](albumidalbumartist-attribute.md)
</dt> <dt>

[<span data-ttu-id="a0f68-121">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="a0f68-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





