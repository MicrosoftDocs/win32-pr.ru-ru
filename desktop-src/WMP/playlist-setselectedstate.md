---
title: Список воспроизведения. Сетселектедстате
description: Метод Сетселектедстате указывает, что в списке воспроизведения выбран индексированный элемент.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- Проигрыватель Windows Media Player. Сетселектедстате
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708615"
---
# <a name="playlistsetselectedstate"></a><span data-ttu-id="383f3-104">Список воспроизведения. Сетселектедстате</span><span class="sxs-lookup"><span data-stu-id="383f3-104">PLAYLIST.setSelectedState</span></span>

<span data-ttu-id="383f3-105">Метод **сетселектедстате** указывает, что в списке воспроизведения выбран индексированный элемент.</span><span class="sxs-lookup"><span data-stu-id="383f3-105">The **setSelectedState** method specifies that the indexed item in the playlist is selected.</span></span>

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a><span data-ttu-id="383f3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="383f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="383f3-107"><span id="item"></span><span id="ITEM"></span>*детализирован*</span><span class="sxs-lookup"><span data-stu-id="383f3-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="383f3-108">**Число** (**длинное**), указывающее индекс элемента в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="383f3-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="383f3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="383f3-109">Return Value</span></span>

<span data-ttu-id="383f3-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="383f3-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="383f3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="383f3-111">Remarks</span></span>

<span data-ttu-id="383f3-112">Вы можете задать для всех элементов выбранное состояние, указав значение 1 в параметре *Item* .</span><span class="sxs-lookup"><span data-stu-id="383f3-112">You can set all items to the selected state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="383f3-113">Этот метод был заменен **setSelectedState2**, который поддерживает вложенные списки воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="383f3-113">This method has been replaced by **setSelectedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="383f3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="383f3-114">Requirements</span></span>



| <span data-ttu-id="383f3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="383f3-115">Requirement</span></span> | <span data-ttu-id="383f3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="383f3-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="383f3-117">Версия</span><span class="sxs-lookup"><span data-stu-id="383f3-117">Version</span></span><br/> | <span data-ttu-id="383f3-118">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="383f3-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="383f3-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="383f3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="383f3-120">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="383f3-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="383f3-121">**Список воспроизведения. setSelectedState2**</span><span class="sxs-lookup"><span data-stu-id="383f3-121">**PLAYLIST.setSelectedState2**</span></span>](playlist-setselectedstate2.md)
</dt> </dl>

 

 





