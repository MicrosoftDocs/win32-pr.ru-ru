---
title: Атрибут WM/Composer
description: Атрибут WM/Composer — это имя композитора музыки.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- Проигрыватель Windows Media с атрибутом WM/Composer
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f206b1a23126612f3f7c875b9a9b4badca8339
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704316"
---
# <a name="wmcomposer-attribute"></a><span data-ttu-id="0ccb6-104">Атрибут WM/Composer</span><span class="sxs-lookup"><span data-stu-id="0ccb6-104">WM/Composer Attribute</span></span>

<span data-ttu-id="0ccb6-105">Атрибут **WM/Composer** — это имя композитора музыки.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-105">The **WM/Composer** attribute is the name of the composer of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="0ccb6-106">Применение</span><span class="sxs-lookup"><span data-stu-id="0ccb6-106">Applies To</span></span>

-   [<span data-ttu-id="0ccb6-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="0ccb6-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="0ccb6-108">Списки воспроизведения компакт-дисков</span><span class="sxs-lookup"><span data-stu-id="0ccb6-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="0ccb6-109">Дорожки компакт-диска</span><span class="sxs-lookup"><span data-stu-id="0ccb6-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="0ccb6-110">Часто используемые атрибуты файлов Windows Media</span><span class="sxs-lookup"><span data-stu-id="0ccb6-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="0ccb6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ccb6-111">Remarks</span></span>

<span data-ttu-id="0ccb6-112">Этот атрибут хранится как в библиотеке (или в кэше), так и в файле цифрового носителя.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="0ccb6-113">Этот атрибут может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-113">This attribute may have multiple values.</span></span> <span data-ttu-id="0ccb6-114">Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать метод **Media. жетитеминфобитипе** , а не метод **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="0ccb6-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="0ccb6-115">**Composer** — это псевдоним для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-115">**Composer** is an alias for this attribute.</span></span>

<span data-ttu-id="0ccb6-116">Константа Windows Media Format SDK для этого атрибута — g \_ всзвмкомпосер.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-116">The Windows Media Format SDK constant for this attribute is g\_wszWMComposer.</span></span>

<span data-ttu-id="0ccb6-117">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="0ccb6-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ccb6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0ccb6-118">Requirements</span></span>



| <span data-ttu-id="0ccb6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0ccb6-119">Requirement</span></span> | <span data-ttu-id="0ccb6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0ccb6-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="0ccb6-121">Версия</span><span class="sxs-lookup"><span data-stu-id="0ccb6-121">Version</span></span><br/> | <span data-ttu-id="0ccb6-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0ccb6-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ccb6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ccb6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ccb6-124">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="0ccb6-125">**Media. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





