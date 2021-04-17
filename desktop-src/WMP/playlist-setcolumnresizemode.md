---
title: Список воспроизведения. Сетколумнресиземоде
description: Метод Сетколумнресиземоде определяет, как именно изменяются размеры индексированных столбцов.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- Проигрыватель Windows Media Player. Сетколумнресиземоде
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a1b83020f4400f4f1095c84e281fe498f2b67da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708618"
---
# <a name="playlistsetcolumnresizemode"></a><span data-ttu-id="bc082-104">Список воспроизведения. Сетколумнресиземоде</span><span class="sxs-lookup"><span data-stu-id="bc082-104">PLAYLIST.setColumnResizeMode</span></span>

<span data-ttu-id="bc082-105">Метод **сетколумнресиземоде** определяет, как именно изменяются размеры индексированных столбцов.</span><span class="sxs-lookup"><span data-stu-id="bc082-105">The **setColumnResizeMode** method specifies how the indexed column sizes itself.</span></span>

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a><span data-ttu-id="bc082-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc082-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc082-107"><span id="column"></span><span id="COLUMN"></span>*рубрик*</span><span class="sxs-lookup"><span data-stu-id="bc082-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="bc082-108">**Число** (**длинное**), указывающее индекс столбца, который необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="bc082-108">**Number** (**long**) indicating the index of the column to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="bc082-109"><span id="mode"></span><span id="MODE"></span>*режима*</span><span class="sxs-lookup"><span data-stu-id="bc082-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="bc082-110">**Строка** , указывающая режим изменения размера.</span><span class="sxs-lookup"><span data-stu-id="bc082-110">**String** indicating the sizing mode.</span></span> <span data-ttu-id="bc082-111">Содержит одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="bc082-111">Contains one of the following values.</span></span>



| <span data-ttu-id="bc082-112">Значение</span><span class="sxs-lookup"><span data-stu-id="bc082-112">Value</span></span>          | <span data-ttu-id="bc082-113">Описание</span><span class="sxs-lookup"><span data-stu-id="bc082-113">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc082-114">аутосизехеадер</span><span class="sxs-lookup"><span data-stu-id="bc082-114">AutosizeHeader</span></span> | <span data-ttu-id="bc082-115">Столбец изменяется в соответствии со всеми данными в столбце и в заголовке.</span><span class="sxs-lookup"><span data-stu-id="bc082-115">The column resizes to accommodate all data in both the column and the header.</span></span>                                  |
| <span data-ttu-id="bc082-116">аутосизедата</span><span class="sxs-lookup"><span data-stu-id="bc082-116">AutosizeData</span></span>   | <span data-ttu-id="bc082-117">Столбец изменяется в соответствии со всеми данными в столбце.</span><span class="sxs-lookup"><span data-stu-id="bc082-117">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="bc082-118">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="bc082-118">Fixed</span></span>          | <span data-ttu-id="bc082-119">Столбец имеет фиксированный размер.</span><span class="sxs-lookup"><span data-stu-id="bc082-119">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="bc082-120">Растягивается</span><span class="sxs-lookup"><span data-stu-id="bc082-120">Stretches</span></span>      | <span data-ttu-id="bc082-121">Размер столбца изменяется для использования оставшегося пространства в элементе **списка воспроизведения** после изменения размера всех остальных столбцов.</span><span class="sxs-lookup"><span data-stu-id="bc082-121">The column resizes to use the remaining space in the **PLAYLIST** element after all other columns are resized.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc082-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc082-122">Return Value</span></span>

<span data-ttu-id="bc082-123">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bc082-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc082-124">Требования</span><span class="sxs-lookup"><span data-stu-id="bc082-124">Requirements</span></span>



| <span data-ttu-id="bc082-125">Требование</span><span class="sxs-lookup"><span data-stu-id="bc082-125">Requirement</span></span> | <span data-ttu-id="bc082-126">Значение</span><span class="sxs-lookup"><span data-stu-id="bc082-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bc082-127">Версия</span><span class="sxs-lookup"><span data-stu-id="bc082-127">Version</span></span><br/> | <span data-ttu-id="bc082-128">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="bc082-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc082-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc082-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc082-130">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="bc082-130">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





