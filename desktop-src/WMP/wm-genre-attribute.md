---
title: Атрибут WM/жанра
description: Атрибут WM/жанр является жанром содержимого.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- Атрибут WM/жанр проигрыватель Windows Media
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae4a0c6ae27e85fa1ed147a3173c4cc31b20f1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704303"
---
# <a name="wmgenre-attribute"></a><span data-ttu-id="3d5d5-104">Атрибут WM/жанра</span><span class="sxs-lookup"><span data-stu-id="3d5d5-104">WM/Genre Attribute</span></span>

<span data-ttu-id="3d5d5-105">Атрибут **WM/жанр** является жанром содержимого.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-105">The **WM/Genre** attribute is the genre of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3d5d5-106">Применение</span><span class="sxs-lookup"><span data-stu-id="3d5d5-106">Applies To</span></span>

-   [<span data-ttu-id="3d5d5-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="3d5d5-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="3d5d5-108">Списки воспроизведения компакт-дисков</span><span class="sxs-lookup"><span data-stu-id="3d5d5-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="3d5d5-109">Дорожки компакт-диска</span><span class="sxs-lookup"><span data-stu-id="3d5d5-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="3d5d5-110">Часто используемые атрибуты файлов Windows Media</span><span class="sxs-lookup"><span data-stu-id="3d5d5-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="3d5d5-111">DVD-диски</span><span class="sxs-lookup"><span data-stu-id="3d5d5-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="3d5d5-112">Другие элементы</span><span class="sxs-lookup"><span data-stu-id="3d5d5-112">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="3d5d5-113">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="3d5d5-113">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="3d5d5-114">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="3d5d5-114">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="3d5d5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d5d5-115">Remarks</span></span>

<span data-ttu-id="3d5d5-116">Этот атрибут хранится как в библиотеке (или в кэше), так и в файле цифрового носителя.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-116">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="3d5d5-117">Этот атрибут может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-117">This attribute may have multiple values.</span></span> <span data-ttu-id="3d5d5-118">Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать метод **Media. жетитеминфобитипе** , а не метод **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="3d5d5-118">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="3d5d5-119">**Жанр** — это псевдоним для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-119">**Genre** is an alias for this attribute.</span></span>

<span data-ttu-id="3d5d5-120">Константа Windows Media Format SDK для этого атрибута — g \_ всзвмженре.</span><span class="sxs-lookup"><span data-stu-id="3d5d5-120">The Windows Media Format SDK constant for this attribute is g\_wszWMGenre.</span></span>

<span data-ttu-id="3d5d5-121">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="3d5d5-121">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d5d5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3d5d5-122">Requirements</span></span>



| <span data-ttu-id="3d5d5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3d5d5-123">Requirement</span></span> | <span data-ttu-id="3d5d5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3d5d5-124">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="3d5d5-125">Версия</span><span class="sxs-lookup"><span data-stu-id="3d5d5-125">Version</span></span><br/> | <span data-ttu-id="3d5d5-126">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3d5d5-126">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d5d5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d5d5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d5d5-128">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="3d5d5-128">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="3d5d5-129">**Media. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="3d5d5-129">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





