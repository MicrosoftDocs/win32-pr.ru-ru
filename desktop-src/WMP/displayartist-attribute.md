---
title: Атрибут Дисплайартист
description: Атрибут Дисплайартист — это имя исполнителя, отображаемого для элемента.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- Дисплайартист атрибут Windows Media Player
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694960"
---
# <a name="displayartist-attribute"></a><span data-ttu-id="b4c40-104">Атрибут Дисплайартист</span><span class="sxs-lookup"><span data-stu-id="b4c40-104">DisplayArtist Attribute</span></span>

<span data-ttu-id="b4c40-105">Атрибут **дисплайартист** — это имя исполнителя, отображаемого для элемента.</span><span class="sxs-lookup"><span data-stu-id="b4c40-105">The **DisplayArtist** attribute is the name of the artist that is displayed for an item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b4c40-106">Применение</span><span class="sxs-lookup"><span data-stu-id="b4c40-106">Applies To</span></span>

-   [<span data-ttu-id="b4c40-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="b4c40-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b4c40-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4c40-108">Remarks</span></span>

<span data-ttu-id="b4c40-109">Как правило, **дисплайартист** будет иметь то же значение, что и атрибут **WM/албумартист** , если задан этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="b4c40-109">Generally, **DisplayArtist** will have the same value as the **WM/AlbumArtist** attribute when that attribute is set.</span></span> <span data-ttu-id="b4c40-110">В противном случае значением будет имя исполнителя, связанного с первой записью в альбоме.</span><span class="sxs-lookup"><span data-stu-id="b4c40-110">Otherwise, the value will be the name of the artist that is associated with the first track on the album.</span></span>

<span data-ttu-id="b4c40-111">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b4c40-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4c40-112">Требования</span><span class="sxs-lookup"><span data-stu-id="b4c40-112">Requirements</span></span>



| <span data-ttu-id="b4c40-113">Требование</span><span class="sxs-lookup"><span data-stu-id="b4c40-113">Requirement</span></span> | <span data-ttu-id="b4c40-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b4c40-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="b4c40-115">Версия</span><span class="sxs-lookup"><span data-stu-id="b4c40-115">Version</span></span><br/> | <span data-ttu-id="b4c40-116">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="b4c40-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4c40-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4c40-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c40-118">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="b4c40-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="b4c40-119">**Атрибут WM/Албумартист**</span><span class="sxs-lookup"><span data-stu-id="b4c40-119">**WM/AlbumArtist Attribute**</span></span>](wm-albumartist-attribute.md)
</dt> </dl>

 

 





