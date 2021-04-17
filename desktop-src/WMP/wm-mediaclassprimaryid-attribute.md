---
title: Атрибут WM/Медиакласспримарид
description: 'Атрибут WM/Медиакласспримарид — это идентификатор GUID, указывающий на один из основных классов мультимедиа: Музыкальные, Немузыкальные аудио, видео или другие.'
ms.assetid: eb78f4a9-7c18-4cad-bb34-fd1ff15bad4f
keywords:
- Windows Media Player для атрибута WM/Медиакласспримарид
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5107a2c4e04e9424bf0a20a7d4cf7b8edef80492
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704294"
---
# <a name="wmmediaclassprimaryid-attribute"></a><span data-ttu-id="e3ed6-104">Атрибут WM/Медиакласспримарид</span><span class="sxs-lookup"><span data-stu-id="e3ed6-104">WM/MediaClassPrimaryID Attribute</span></span>

<span data-ttu-id="e3ed6-105">Атрибут **WM/медиакласспримарид** — это идентификатор GUID, указывающий один из основных классов мультимедиа: Music, не музыкальное аудио, видео или другое.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-105">The **WM/MediaClassPrimaryID** attribute is a GUID specifying one of the primary media classes: music, non-music audio, video, or other.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e3ed6-106">Применение</span><span class="sxs-lookup"><span data-stu-id="e3ed6-106">Applies To</span></span>

-   [<span data-ttu-id="e3ed6-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="e3ed6-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="e3ed6-108">Часто используемые атрибуты файлов Windows Media</span><span class="sxs-lookup"><span data-stu-id="e3ed6-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="e3ed6-109">Другие элементы</span><span class="sxs-lookup"><span data-stu-id="e3ed6-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="e3ed6-110">Элементы фото</span><span class="sxs-lookup"><span data-stu-id="e3ed6-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="e3ed6-111">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="e3ed6-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="e3ed6-112">Элементы Радио</span><span class="sxs-lookup"><span data-stu-id="e3ed6-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="e3ed6-113">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="e3ed6-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="e3ed6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3ed6-114">Remarks</span></span>

<span data-ttu-id="e3ed6-115">Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="e3ed6-116">**Медиакласспримарид** является псевдонимом для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-116">**MediaClassPrimaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="e3ed6-117">Константа Windows Media Format SDK для этого атрибута — g \_ всзвммедиакласспримарид.</span><span class="sxs-lookup"><span data-stu-id="e3ed6-117">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassPrimaryID.</span></span>

<span data-ttu-id="e3ed6-118">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="e3ed6-118">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ed6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e3ed6-119">Requirements</span></span>



| <span data-ttu-id="e3ed6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e3ed6-120">Requirement</span></span> | <span data-ttu-id="e3ed6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e3ed6-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ed6-122">Версия</span><span class="sxs-lookup"><span data-stu-id="e3ed6-122">Version</span></span><br/> | <span data-ttu-id="e3ed6-123">Проигрыватель Windows Media 9 Series или более поздней версии (элемент Photo поддерживается только в проигрывателе Windows Media 10 или более поздней версии)</span><span class="sxs-lookup"><span data-stu-id="e3ed6-123">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3ed6-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3ed6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ed6-125">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="e3ed6-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





