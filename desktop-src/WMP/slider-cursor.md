---
title: ПОЛЗУНок. Cursor
description: Атрибут Cursor указывает или получает значение, указывающее, какой курсор отображается при наведении мыши на элемент управления Slider.
ms.assetid: 5b96a20c-b3a6-4e08-95b2-32937bb15cc6
keywords:
- ПОЛЗУНок. курсор Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc8f581d7d087545e666565dd03f649112064d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656939"
---
# <a name="slidercursor"></a><span data-ttu-id="e1a22-104">ПОЛЗУНок. Cursor</span><span class="sxs-lookup"><span data-stu-id="e1a22-104">SLIDER.cursor</span></span>

<span data-ttu-id="e1a22-105">Атрибут **cursor** указывает или получает значение, указывающее, какой курсор отображается при наведении мыши на элемент управления Slider.</span><span class="sxs-lookup"><span data-stu-id="e1a22-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the slider control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="e1a22-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="e1a22-106">Possible Values</span></span>

<span data-ttu-id="e1a22-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e1a22-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="e1a22-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e1a22-108">Value</span></span>            | <span data-ttu-id="e1a22-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e1a22-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1a22-110">система</span><span class="sxs-lookup"><span data-stu-id="e1a22-110">system</span></span>           | <span data-ttu-id="e1a22-111">Зависимый от платформы курсор (обычно это стрелка).</span><span class="sxs-lookup"><span data-stu-id="e1a22-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="e1a22-112">правый</span><span class="sxs-lookup"><span data-stu-id="e1a22-112">hand</span></span>             | <span data-ttu-id="e1a22-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1a22-113">Default.</span></span> <span data-ttu-id="e1a22-114">Правый.</span><span class="sxs-lookup"><span data-stu-id="e1a22-114">Hand.</span></span>                                                                              |
| <span data-ttu-id="e1a22-115">help</span><span class="sxs-lookup"><span data-stu-id="e1a22-115">help</span></span>             | <span data-ttu-id="e1a22-116">Стрелка с вопросительным знаком, указывающим на наличие справки.</span><span class="sxs-lookup"><span data-stu-id="e1a22-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="e1a22-117">сизеалл</span><span class="sxs-lookup"><span data-stu-id="e1a22-117">sizeall</span></span>          | <span data-ttu-id="e1a22-118">4-направленная стрелка, указывающая на север, Юг, Восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="e1a22-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="e1a22-119">сизенесв</span><span class="sxs-lookup"><span data-stu-id="e1a22-119">sizenesw</span></span>         | <span data-ttu-id="e1a22-120">Двойная стрелка, указывающая на северо-восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="e1a22-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="e1a22-121">сизенс</span><span class="sxs-lookup"><span data-stu-id="e1a22-121">sizens</span></span>           | <span data-ttu-id="e1a22-122">Двусторонняя стрелка, указывающая на север и Юг.</span><span class="sxs-lookup"><span data-stu-id="e1a22-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="e1a22-123">сизенвсе</span><span class="sxs-lookup"><span data-stu-id="e1a22-123">sizenwse</span></span>         | <span data-ttu-id="e1a22-124">Двойная стрелка, указывающая на северо-запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="e1a22-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="e1a22-125">сизеве</span><span class="sxs-lookup"><span data-stu-id="e1a22-125">sizewe</span></span>           | <span data-ttu-id="e1a22-126">Двойная стрелка, указывающая на запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="e1a22-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="e1a22-127">Стрелка вверх</span><span class="sxs-lookup"><span data-stu-id="e1a22-127">uparrow</span></span>          | <span data-ttu-id="e1a22-128">Вертикальная стрелка, указывающая вверх.</span><span class="sxs-lookup"><span data-stu-id="e1a22-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="e1a22-129">\*. ani или \* . cur</span><span class="sxs-lookup"><span data-stu-id="e1a22-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="e1a22-130">Любой ANI или cur-файл (должен находиться в том же каталоге, что и файл WMS, или в WMZ-файле).</span><span class="sxs-lookup"><span data-stu-id="e1a22-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e1a22-131">Требования</span><span class="sxs-lookup"><span data-stu-id="e1a22-131">Requirements</span></span>



| <span data-ttu-id="e1a22-132">Требование</span><span class="sxs-lookup"><span data-stu-id="e1a22-132">Requirement</span></span> | <span data-ttu-id="e1a22-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e1a22-133">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e1a22-134">Версия</span><span class="sxs-lookup"><span data-stu-id="e1a22-134">Version</span></span><br/> | <span data-ttu-id="e1a22-135">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="e1a22-135">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1a22-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1a22-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1a22-137">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="e1a22-137">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





