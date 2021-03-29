---
title: Список воспроизведения. itemCount
description: Атрибут itemCount извлекает количество элементов, отображаемых в данный момент в элементе списка воспроизведения.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- Проигрыватель Windows Media Player. itemCount
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657949"
---
# <a name="playlistitemcount"></a><span data-ttu-id="f7e47-104">Список воспроизведения. itemCount</span><span class="sxs-lookup"><span data-stu-id="f7e47-104">PLAYLIST.itemCount</span></span>

<span data-ttu-id="f7e47-105">Атрибут **ItemCount** извлекает количество элементов, отображаемых в данный момент в элементе **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="f7e47-105">The **itemCount** attribute retrieves the number of items currently displayed in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a><span data-ttu-id="f7e47-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="f7e47-106">Possible Values</span></span>

<span data-ttu-id="f7e47-107">Этот атрибут является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="f7e47-107">This attribute is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7e47-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7e47-108">Remarks</span></span>

<span data-ttu-id="f7e47-109">Свойство **ItemCount** будет считать общее число развернутых элементов.</span><span class="sxs-lookup"><span data-stu-id="f7e47-109">The **itemCount** property will count the total number of expanded items.</span></span> <span data-ttu-id="f7e47-110">Например, если имеется два списка воспроизведения, каждый из которых содержит три элемента мультимедиа, **ItemCount** возвратит 2, если списки воспроизведения не развернуты.</span><span class="sxs-lookup"><span data-stu-id="f7e47-110">For example, if there are two playlists that contain three media items each, **itemCount** will return 2 if the playlists are not expanded.</span></span> <span data-ttu-id="f7e47-111">Если развернут только первый список воспроизведения, **ItemCount** возвратит 4.</span><span class="sxs-lookup"><span data-stu-id="f7e47-111">If only the first playlist is expanded, **itemCount** will return 4.</span></span> <span data-ttu-id="f7e47-112">Если оба списка воспроизведения развернуты, **ItemCount** возвратит значение 6.</span><span class="sxs-lookup"><span data-stu-id="f7e47-112">If both playlists are expanded, **itemCount** will return 6.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7e47-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f7e47-113">Requirements</span></span>



| <span data-ttu-id="f7e47-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f7e47-114">Requirement</span></span> | <span data-ttu-id="f7e47-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f7e47-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="f7e47-116">Версия</span><span class="sxs-lookup"><span data-stu-id="f7e47-116">Version</span></span><br/> | <span data-ttu-id="f7e47-117">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f7e47-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7e47-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7e47-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e47-119">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="f7e47-119">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





