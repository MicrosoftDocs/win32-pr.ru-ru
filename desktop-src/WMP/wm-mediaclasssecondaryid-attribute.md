---
title: Атрибут WM/Медиакласссекондарид
description: Атрибут WM/Медиакласссекондарид — это идентификатор GUID, указывающий класс вторичного носителя, который является подклассом основного класса мультимедиа.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Windows Media Player для атрибута WM/Медиакласссекондарид
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704293"
---
# <a name="wmmediaclasssecondaryid-attribute"></a><span data-ttu-id="bec14-104">Атрибут WM/Медиакласссекондарид</span><span class="sxs-lookup"><span data-stu-id="bec14-104">WM/MediaClassSecondaryID Attribute</span></span>

<span data-ttu-id="bec14-105">Атрибут **WM/медиакласссекондарид** — это идентификатор GUID, указывающий класс вторичного носителя, который является подклассом основного класса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bec14-105">The **WM/MediaClassSecondaryID** attribute is a GUID specifying the secondary media class, which is a subclass of the primary media class.</span></span>

## <a name="applies-to"></a><span data-ttu-id="bec14-106">Применение</span><span class="sxs-lookup"><span data-stu-id="bec14-106">Applies To</span></span>

-   [<span data-ttu-id="bec14-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="bec14-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="bec14-108">Часто используемые атрибуты файлов Windows Media</span><span class="sxs-lookup"><span data-stu-id="bec14-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="bec14-109">Другие элементы</span><span class="sxs-lookup"><span data-stu-id="bec14-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="bec14-110">Элементы фото</span><span class="sxs-lookup"><span data-stu-id="bec14-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="bec14-111">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="bec14-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="bec14-112">Элементы Радио</span><span class="sxs-lookup"><span data-stu-id="bec14-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="bec14-113">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="bec14-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="bec14-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bec14-114">Remarks</span></span>

<span data-ttu-id="bec14-115">Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bec14-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="bec14-116">В следующей таблице перечислены поддерживаемые идентификаторы GUID и их описания.</span><span class="sxs-lookup"><span data-stu-id="bec14-116">The following table lists the supported GUIDs and their descriptions.</span></span>



| <span data-ttu-id="bec14-117">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="bec14-117">GUID</span></span>                                 | <span data-ttu-id="bec14-118">Описание</span><span class="sxs-lookup"><span data-stu-id="bec14-118">Description</span></span>                                    |
|--------------------------------------|------------------------------------------------|
| <span data-ttu-id="bec14-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span><span class="sxs-lookup"><span data-stu-id="bec14-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span></span> | <span data-ttu-id="bec14-120">Объект мультимедиа представляет статический список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bec14-120">The media object represents a static playlist.</span></span> |
| <span data-ttu-id="bec14-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span><span class="sxs-lookup"><span data-stu-id="bec14-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span></span> | <span data-ttu-id="bec14-122">Объект мультимедиа представляет автоматический список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bec14-122">The media object represents an auto playlist.</span></span>  |



 

<span data-ttu-id="bec14-123">**Медиакласссекондарид** является псевдонимом для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="bec14-123">**MediaClassSecondaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="bec14-124">Константа Windows Media Format SDK для этого атрибута — g \_ всзвммедиакласссекондарид.</span><span class="sxs-lookup"><span data-stu-id="bec14-124">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassSecondaryID.</span></span>

<span data-ttu-id="bec14-125">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="bec14-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bec14-126">Требования</span><span class="sxs-lookup"><span data-stu-id="bec14-126">Requirements</span></span>



| <span data-ttu-id="bec14-127">Требование</span><span class="sxs-lookup"><span data-stu-id="bec14-127">Requirement</span></span> | <span data-ttu-id="bec14-128">Значение</span><span class="sxs-lookup"><span data-stu-id="bec14-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec14-129">Версия</span><span class="sxs-lookup"><span data-stu-id="bec14-129">Version</span></span><br/> | <span data-ttu-id="bec14-130">Элемент Photo поддерживается только в проигрывателе Windows Media 10 или более поздней версии. элемент Radio поддерживается только в проигрывателе Windows Media 9 Series все остальные элементы поддерживаются в серии проигрывателя Windows Media 9 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="bec14-130">The photo item is supported only in Windows Media Player 10 or later The radio item is supported only in Windows Media Player 9 Series All other items are supported in Windows Media Player 9 Series and later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bec14-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bec14-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec14-132">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="bec14-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





