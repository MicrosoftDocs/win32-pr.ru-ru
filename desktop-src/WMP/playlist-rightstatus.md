---
title: Список воспроизведения. Ригхтстатус
description: Атрибут Ригхтстатус указывает или получает текст состояния, отображаемый в правой части и внизу элемента списка воспроизведения.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- Проигрыватель Windows Media Player. Ригхтстатус
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b382da4ae214c9a830cc64fb1aa0d0edadbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704256"
---
# <a name="playlistrightstatus"></a><span data-ttu-id="87e97-104">Список воспроизведения. Ригхтстатус</span><span class="sxs-lookup"><span data-stu-id="87e97-104">PLAYLIST.rightStatus</span></span>

<span data-ttu-id="87e97-105">Атрибут **ригхтстатус** указывает или получает текст состояния, отображаемый в правой части и внизу элемента **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="87e97-105">The **rightStatus** attribute specifies or retrieves the status text that is displayed on the right side and bottom of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a><span data-ttu-id="87e97-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="87e97-106">Possible Values</span></span>

<span data-ttu-id="87e97-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="87e97-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="87e97-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87e97-108">Remarks</span></span>

<span data-ttu-id="87e97-109">Этот атрибут может сочетать любой текст с конкретными ключевыми словами, которые будут отображать необходимую информацию, например общую длительность списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="87e97-109">This attribute can combine any text with specific keywords that will display the desired information, such as the total duration of the playlist.</span></span> <span data-ttu-id="87e97-110">Ключевые слова заключены в процентные символы (%) чтобы они не изменялись, используйте обычный текст.</span><span class="sxs-lookup"><span data-stu-id="87e97-110">The keywords are surrounded by percentage symbols (%) to keep them distinct from the ordinary text.</span></span>

<span data-ttu-id="87e97-111">Можно использовать следующие ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="87e97-111">The following keywords can be used.</span></span>



| <span data-ttu-id="87e97-112">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="87e97-112">Keyword</span></span>               | <span data-ttu-id="87e97-113">Описание</span><span class="sxs-lookup"><span data-stu-id="87e97-113">Description</span></span>                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87e97-114">count</span><span class="sxs-lookup"><span data-stu-id="87e97-114">count</span></span>                 | <span data-ttu-id="87e97-115">Число элементов в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="87e97-115">Number of items in the playlist.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="87e97-116">size</span><span class="sxs-lookup"><span data-stu-id="87e97-116">size</span></span>                  | <span data-ttu-id="87e97-117">Общий размер списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="87e97-117">Total size of the playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="87e97-118">длительность</span><span class="sxs-lookup"><span data-stu-id="87e97-118">duration</span></span>              | <span data-ttu-id="87e97-119">Общая длительность списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="87e97-119">Total duration of the playlist.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="87e97-120">*XXX*</span><span class="sxs-lookup"><span data-stu-id="87e97-120">*XXX*</span></span>                 | <span data-ttu-id="87e97-121">Выполняет **getItemInfo** для списка воспроизведения с *xxx* , который получает элемент.</span><span class="sxs-lookup"><span data-stu-id="87e97-121">Does a **getItemInfo** on the playlist with *XXX* being the item to receive.</span></span>                                                                                                                                 |
| <span data-ttu-id="87e97-122">SelectedSize</span><span class="sxs-lookup"><span data-stu-id="87e97-122">SelectedSize</span></span>          | <span data-ttu-id="87e97-123">Общий размер выбранных записей в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="87e97-123">Total size of the selected entries in the playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="87e97-124">селектедкаунт</span><span class="sxs-lookup"><span data-stu-id="87e97-124">SelectedCount</span></span>         | <span data-ttu-id="87e97-125">Общее число выбранных записей в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="87e97-125">Total number of selected entries in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="87e97-126">селектеддуратион</span><span class="sxs-lookup"><span data-stu-id="87e97-126">SelectedDuration</span></span>      | <span data-ttu-id="87e97-127">Общая длительность выбранных записей в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="87e97-127">Total duration of the selected entries in the playlist.</span></span>                                                                                                                                                      |
| <span data-ttu-id="87e97-128">чеккедкаунт</span><span class="sxs-lookup"><span data-stu-id="87e97-128">CheckedCount</span></span>          | <span data-ttu-id="87e97-129">Общее число проверенных дорожек в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="87e97-129">Total number of checked tracks in the playlist.</span></span>                                                                                                                                                              |
| <span data-ttu-id="87e97-130">чеккеддуратион</span><span class="sxs-lookup"><span data-stu-id="87e97-130">CheckedDuration</span></span>       | <span data-ttu-id="87e97-131">Общая продолжительность проверенных дорожек в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="87e97-131">Total duration of the checked tracks in the playlist.</span></span>                                                                                                                                                        |
| <span data-ttu-id="87e97-132">чеккедсизе</span><span class="sxs-lookup"><span data-stu-id="87e97-132">CheckedSize</span></span>           | <span data-ttu-id="87e97-133">Общий размер проверенных дорожек в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="87e97-133">Total size of the checked tracks in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="87e97-134">дуратионстринг</span><span class="sxs-lookup"><span data-stu-id="87e97-134">DurationString</span></span>        | <span data-ttu-id="87e97-135">Отображает текст с описанием длительности "Общее время" или "предполагаемое время" в зависимости от того, известны ли итоговые значения.</span><span class="sxs-lookup"><span data-stu-id="87e97-135">Displays text that describes the duration as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="87e97-136">За этим текстом следует "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="87e97-136">This text is followed by "%duration%".</span></span>                                       |
| <span data-ttu-id="87e97-137">чеккеддуратионстринг</span><span class="sxs-lookup"><span data-stu-id="87e97-137">CheckedDurationString</span></span> | <span data-ttu-id="87e97-138">Отображает текст, описывающий продолжительность всех отмеченных элементов в списке воспроизведения как "Общее время" или "предполагаемое время" в зависимости от того, известны ли итоговые значения.</span><span class="sxs-lookup"><span data-stu-id="87e97-138">Displays text that describes the duration for all checked items in the playlist as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="87e97-139">За этим текстом следует "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="87e97-139">This text is followed by "%duration%".</span></span> |



 

<span data-ttu-id="87e97-140">Значение "Общее время:% Duration%" для списка воспроизведения, содержащего общую длительность семь минут, будет содержать "Общее время: 07:00".</span><span class="sxs-lookup"><span data-stu-id="87e97-140">The value "Total Time: %duration%" for a playlist that contains a total duration of seven minutes will display "Total Time: 07:00".</span></span>

## <a name="requirements"></a><span data-ttu-id="87e97-141">Требования</span><span class="sxs-lookup"><span data-stu-id="87e97-141">Requirements</span></span>



| <span data-ttu-id="87e97-142">Требование</span><span class="sxs-lookup"><span data-stu-id="87e97-142">Requirement</span></span> | <span data-ttu-id="87e97-143">Значение</span><span class="sxs-lookup"><span data-stu-id="87e97-143">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="87e97-144">Версия</span><span class="sxs-lookup"><span data-stu-id="87e97-144">Version</span></span><br/> | <span data-ttu-id="87e97-145">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="87e97-145">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87e97-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87e97-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e97-147">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="87e97-147">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





