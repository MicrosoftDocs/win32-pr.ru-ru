---
title: Список воспроизведения. Итемплайлист
description: Атрибут Итемплайлист извлекает список воспроизведения для элемента мультимедиа, который отображается по заданному индексу в элементе списка воспроизведения.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- Проигрыватель Windows Media Player. Итемплайлист
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708562"
---
# <a name="playlistitemplaylist"></a><span data-ttu-id="738a3-104">Список воспроизведения. Итемплайлист</span><span class="sxs-lookup"><span data-stu-id="738a3-104">PLAYLIST.itemPlaylist</span></span>

<span data-ttu-id="738a3-105">Атрибут **итемплайлист** извлекает список воспроизведения для элемента мультимедиа, который отображается по заданному индексу в элементе **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="738a3-105">The **itemPlaylist** attribute retrieves the playlist for the media item that is displayed at the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a><span data-ttu-id="738a3-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="738a3-106">Possible Values</span></span>

<span data-ttu-id="738a3-107">Этот атрибут является объектом **списка воспроизведения** , предназначенным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="738a3-107">This attribute is a read-only **Playlist** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="738a3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="738a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="738a3-109"><span id="index"></span><span id="INDEX"></span>*номер*</span><span class="sxs-lookup"><span data-stu-id="738a3-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="738a3-110">**Число**(**длинное**), содержащее индекс элемента списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="738a3-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="738a3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="738a3-111">Remarks</span></span>

<span data-ttu-id="738a3-112">Свойство **итемплайлист** вернет объект списка воспроизведения, который разворачивается в элементе **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="738a3-112">The **itemPlaylist** property will return the playlist object that is expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="738a3-113">Например, если есть два вложенных списка воспроизведения, которые не разворачиваются в элементе **списка воспроизведения** и содержат три клипа мультимедиа, **итемплайлист**(1) вернет родительский список воспроизведения, содержащий два вложенных списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="738a3-113">For example, if there are two nested playlists that are not expanded in the **PLAYLIST** element, and that contain three media clips each, **itemPlaylist**(1) will return the parent playlist that contains the two nested playlists.</span></span> <span data-ttu-id="738a3-114">Если второй список воспроизведения развернут, **итемплайлист**(1) вернет второй список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="738a3-114">If the second playlist is expanded, **itemPlaylist**(1) will return the second playlist.</span></span> <span data-ttu-id="738a3-115">Если оба списка воспроизведения развернуты, **итемплайлист**(1) вернет первый список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="738a3-115">If both playlists are expanded, **itemPlaylist**(1) will return the first playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="738a3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="738a3-116">Requirements</span></span>



| <span data-ttu-id="738a3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="738a3-117">Requirement</span></span> | <span data-ttu-id="738a3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="738a3-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="738a3-119">Версия</span><span class="sxs-lookup"><span data-stu-id="738a3-119">Version</span></span><br/> | <span data-ttu-id="738a3-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="738a3-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="738a3-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="738a3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738a3-122">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="738a3-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="738a3-123">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="738a3-123">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





