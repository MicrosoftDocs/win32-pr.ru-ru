---
title: Атрибут Author
description: Атрибут Author — это имя исполнителя или субъекта мультимедиа, связанного с содержимым.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Атрибут автора Windows Media Player
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698752"
---
# <a name="author-attribute"></a><span data-ttu-id="c7995-104">Атрибут Author</span><span class="sxs-lookup"><span data-stu-id="c7995-104">Author Attribute</span></span>

<span data-ttu-id="c7995-105">Атрибут **Author** — это имя исполнителя или субъекта мультимедиа, связанного с содержимым.</span><span class="sxs-lookup"><span data-stu-id="c7995-105">The **Author** attribute is the name of a media artist or actor associated with the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c7995-106">Применение</span><span class="sxs-lookup"><span data-stu-id="c7995-106">Applies To</span></span>

-   [<span data-ttu-id="c7995-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="c7995-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="c7995-108">Списки воспроизведения компакт-дисков</span><span class="sxs-lookup"><span data-stu-id="c7995-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="c7995-109">Дорожки компакт-диска</span><span class="sxs-lookup"><span data-stu-id="c7995-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="c7995-110">Часто используемые файлы Windows Media</span><span class="sxs-lookup"><span data-stu-id="c7995-110">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="c7995-111">DVD-диски</span><span class="sxs-lookup"><span data-stu-id="c7995-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="c7995-112">Media. Жетитеминфобитипе</span><span class="sxs-lookup"><span data-stu-id="c7995-112">Media.getItemInfoByType</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="c7995-113">Элементы фото</span><span class="sxs-lookup"><span data-stu-id="c7995-113">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="c7995-114">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="c7995-114">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="c7995-115">Элементы Радио</span><span class="sxs-lookup"><span data-stu-id="c7995-115">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="c7995-116">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="c7995-116">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="c7995-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7995-117">Remarks</span></span>

<span data-ttu-id="c7995-118">Этот атрибут хранится как в библиотеке (или в кэше), так и в файле мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c7995-118">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="c7995-119">Этот атрибут может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="c7995-119">This attribute may have multiple values.</span></span> <span data-ttu-id="c7995-120">Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать *носитель*. метод **жетитеминфобитипе** , а не *носитель*. метод **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="c7995-120">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.**getItemInfo** method.</span></span>

<span data-ttu-id="c7995-121">Константа Windows Media Format SDK для этого атрибута — g \_ всзвмаусор.</span><span class="sxs-lookup"><span data-stu-id="c7995-121">The Windows Media Format SDK constant for this attribute is g\_wszWMAuthor.</span></span>

<span data-ttu-id="c7995-122">**Субъект** и **исполнитель** — это псевдонимы для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="c7995-122">**Actor** and **Artist** are aliases for this attribute.</span></span>

<span data-ttu-id="c7995-123">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c7995-123">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7995-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c7995-124">Requirements</span></span>



| <span data-ttu-id="c7995-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c7995-125">Requirement</span></span> | <span data-ttu-id="c7995-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c7995-126">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="c7995-127">Версия</span><span class="sxs-lookup"><span data-stu-id="c7995-127">Version</span></span><br/> | <span data-ttu-id="c7995-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c7995-128">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7995-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7995-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7995-130">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="c7995-130">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





