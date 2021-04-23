---
title: КУСТОМСЛИДЕР. Cursor
description: Атрибут Cursor указывает или получает значение элемента управления "ползунок", которое появляется при наведении указателя мыши на ползунок.
ms.assetid: 965c21ab-18a0-4459-9d5b-0a35ea2c212f
keywords:
- Проигрыватель Windows Media КУСТОМСЛИДЕР. Cursor
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e836dc7ec6efececf81789efe43d8b19d0df1783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699123"
---
# <a name="customslidercursor"></a><span data-ttu-id="1cfef-104">КУСТОМСЛИДЕР. Cursor</span><span class="sxs-lookup"><span data-stu-id="1cfef-104">CUSTOMSLIDER.cursor</span></span>

<span data-ttu-id="1cfef-105">Атрибут **cursor** указывает или получает значение элемента управления "ползунок", которое появляется при наведении указателя мыши на ползунок.</span><span class="sxs-lookup"><span data-stu-id="1cfef-105">The **cursor** attribute specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="1cfef-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1cfef-106">Possible Values</span></span>

<span data-ttu-id="1cfef-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1cfef-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="1cfef-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1cfef-108">Value</span></span>            | <span data-ttu-id="1cfef-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1cfef-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfef-110">система</span><span class="sxs-lookup"><span data-stu-id="1cfef-110">system</span></span>           | <span data-ttu-id="1cfef-111">Зависимый от платформы курсор (обычно это стрелка).</span><span class="sxs-lookup"><span data-stu-id="1cfef-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="1cfef-112">правый</span><span class="sxs-lookup"><span data-stu-id="1cfef-112">hand</span></span>             | <span data-ttu-id="1cfef-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1cfef-113">Default.</span></span> <span data-ttu-id="1cfef-114">Курсор — это рука.</span><span class="sxs-lookup"><span data-stu-id="1cfef-114">Cursor is a hand.</span></span>                                                                  |
| <span data-ttu-id="1cfef-115">help</span><span class="sxs-lookup"><span data-stu-id="1cfef-115">help</span></span>             | <span data-ttu-id="1cfef-116">Стрелка с вопросительным знаком, указывающим на наличие справки.</span><span class="sxs-lookup"><span data-stu-id="1cfef-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="1cfef-117">сизеалл</span><span class="sxs-lookup"><span data-stu-id="1cfef-117">sizeall</span></span>          | <span data-ttu-id="1cfef-118">4-направленная стрелка, указывающая на север, Юг, Восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="1cfef-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="1cfef-119">сизенесв</span><span class="sxs-lookup"><span data-stu-id="1cfef-119">sizenesw</span></span>         | <span data-ttu-id="1cfef-120">Двойная стрелка, указывающая на северо-восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="1cfef-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="1cfef-121">сизенс</span><span class="sxs-lookup"><span data-stu-id="1cfef-121">sizens</span></span>           | <span data-ttu-id="1cfef-122">Двусторонняя стрелка, указывающая на север и Юг.</span><span class="sxs-lookup"><span data-stu-id="1cfef-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="1cfef-123">сизенвсе</span><span class="sxs-lookup"><span data-stu-id="1cfef-123">sizenwse</span></span>         | <span data-ttu-id="1cfef-124">Двойная стрелка, указывающая на северо-запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="1cfef-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="1cfef-125">сизеве</span><span class="sxs-lookup"><span data-stu-id="1cfef-125">sizewe</span></span>           | <span data-ttu-id="1cfef-126">Двойная стрелка, указывающая на запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="1cfef-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="1cfef-127">Стрелка вверх</span><span class="sxs-lookup"><span data-stu-id="1cfef-127">uparrow</span></span>          | <span data-ttu-id="1cfef-128">Вертикальная стрелка, указывающая вверх.</span><span class="sxs-lookup"><span data-stu-id="1cfef-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="1cfef-129">\*. ani или \* . cur</span><span class="sxs-lookup"><span data-stu-id="1cfef-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="1cfef-130">Любой ANI или cur-файл (должен находиться в том же каталоге, что и файл WMS, или в WMZ-файле).</span><span class="sxs-lookup"><span data-stu-id="1cfef-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1cfef-131">Требования</span><span class="sxs-lookup"><span data-stu-id="1cfef-131">Requirements</span></span>



| <span data-ttu-id="1cfef-132">Требование</span><span class="sxs-lookup"><span data-stu-id="1cfef-132">Requirement</span></span> | <span data-ttu-id="1cfef-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1cfef-133">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1cfef-134">Версия</span><span class="sxs-lookup"><span data-stu-id="1cfef-134">Version</span></span><br/> | <span data-ttu-id="1cfef-135">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="1cfef-135">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1cfef-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1cfef-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cfef-137">**КУСТОМСЛИДЕР, элемент**</span><span class="sxs-lookup"><span data-stu-id="1cfef-137">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





