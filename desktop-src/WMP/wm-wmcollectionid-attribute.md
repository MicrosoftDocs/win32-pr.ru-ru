---
title: Атрибут WM/Вмколлектионид
description: Атрибут WM/Вмколлектионид — это идентификатор GUID, определяющий коллекцию, которой принадлежит элемент.
ms.assetid: 21fc0a62-d374-4ca3-bbb8-278e0d2497ce
keywords:
- Windows Media Player для атрибута WM/Вмколлектионид
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bce21196e1da9583db293dab004812265c85308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718005"
---
# <a name="wmwmcollectionid-attribute"></a><span data-ttu-id="39a9e-104">Атрибут WM/Вмколлектионид</span><span class="sxs-lookup"><span data-stu-id="39a9e-104">WM/WMCollectionID Attribute</span></span>

<span data-ttu-id="39a9e-105">Атрибут **WM/вмколлектионид** — это идентификатор GUID, определяющий коллекцию, которой принадлежит элемент.</span><span class="sxs-lookup"><span data-stu-id="39a9e-105">The **WM/WMCollectionID** attribute is a GUID identifying the collection to which the item belongs.</span></span>

## <a name="applies-to"></a><span data-ttu-id="39a9e-106">Применение</span><span class="sxs-lookup"><span data-stu-id="39a9e-106">Applies To</span></span>

-   [<span data-ttu-id="39a9e-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="39a9e-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="39a9e-108">Списки воспроизведения компакт-дисков</span><span class="sxs-lookup"><span data-stu-id="39a9e-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="39a9e-109">Дорожки компакт-диска</span><span class="sxs-lookup"><span data-stu-id="39a9e-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="39a9e-110">Часто используемые атрибуты файлов Windows Media</span><span class="sxs-lookup"><span data-stu-id="39a9e-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="39a9e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39a9e-111">Remarks</span></span>

<span data-ttu-id="39a9e-112">Этот атрибут хранится как в библиотеке (или в кэше), так и в файле мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="39a9e-112">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="39a9e-113">**Вмколлектионид** является псевдонимом для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="39a9e-113">**WMCollectionID** is an alias for this attribute.</span></span>

<span data-ttu-id="39a9e-114">Константа Windows Media Format SDK для этого атрибута — g \_ всзвмколлектионид.</span><span class="sxs-lookup"><span data-stu-id="39a9e-114">The Windows Media Format SDK constant for this attribute is g\_wszWMCollectionID.</span></span>

<span data-ttu-id="39a9e-115">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="39a9e-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a9e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="39a9e-116">Requirements</span></span>



| <span data-ttu-id="39a9e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="39a9e-117">Requirement</span></span> | <span data-ttu-id="39a9e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="39a9e-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="39a9e-119">Версия</span><span class="sxs-lookup"><span data-stu-id="39a9e-119">Version</span></span><br/> | <span data-ttu-id="39a9e-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="39a9e-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39a9e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39a9e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a9e-122">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="39a9e-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





