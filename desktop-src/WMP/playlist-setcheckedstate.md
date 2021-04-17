---
title: Список воспроизведения. Сетчеккедстате
description: Метод Сетчеккедстате указывает, что установлен индексированный элемент в списке воспроизведения.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- Проигрыватель Windows Media Player. Сетчеккедстате
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704114"
---
# <a name="playlistsetcheckedstate"></a><span data-ttu-id="f792f-104">Список воспроизведения. Сетчеккедстате</span><span class="sxs-lookup"><span data-stu-id="f792f-104">PLAYLIST.setCheckedState</span></span>

<span data-ttu-id="f792f-105">Метод **сетчеккедстате** указывает, что установлен индексированный элемент в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f792f-105">The **setCheckedState** method specifies that the indexed item in the playlist is checked.</span></span>

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a><span data-ttu-id="f792f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f792f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f792f-107"><span id="item"></span><span id="ITEM"></span>*детализирован*</span><span class="sxs-lookup"><span data-stu-id="f792f-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="f792f-108">**Число** (**длинное**), указывающее индекс элемента списка воспроизведения, который должен быть проверен.</span><span class="sxs-lookup"><span data-stu-id="f792f-108">**Number** (**long**) indicating the index of the playlist item to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f792f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f792f-109">Return Value</span></span>

<span data-ttu-id="f792f-110">Этот метод возвращает **логическое значение**.</span><span class="sxs-lookup"><span data-stu-id="f792f-110">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f792f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f792f-111">Remarks</span></span>

<span data-ttu-id="f792f-112">Можно задать для всех элементов состояние checked, указав значение 1 в параметре *Item* .</span><span class="sxs-lookup"><span data-stu-id="f792f-112">You can set all items to the checked state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="f792f-113">Этот метод был заменен **setCheckedState2**, который поддерживает вложенные списки воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f792f-113">This method has been replaced by **setCheckedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="f792f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f792f-114">Requirements</span></span>



| <span data-ttu-id="f792f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f792f-115">Requirement</span></span> | <span data-ttu-id="f792f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f792f-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f792f-117">Версия</span><span class="sxs-lookup"><span data-stu-id="f792f-117">Version</span></span><br/> | <span data-ttu-id="f792f-118">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="f792f-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f792f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f792f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f792f-120">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="f792f-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="f792f-121">**Список воспроизведения. setCheckedState2**</span><span class="sxs-lookup"><span data-stu-id="f792f-121">**PLAYLIST.setCheckedState2**</span></span>](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





