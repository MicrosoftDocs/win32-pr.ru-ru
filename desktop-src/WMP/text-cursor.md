---
title: TEXT. Cursor
description: Атрибут Cursor указывает или получает значение, указывающее, какой курсор отображается при наведении указателя мыши на элемент управления Text.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- ТЕКСТОВЫЙ. курсор Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8cf7b135ed0a99b5c65f760a08e4e7083234674
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717799"
---
# <a name="textcursor"></a><span data-ttu-id="d7170-104">TEXT. Cursor</span><span class="sxs-lookup"><span data-stu-id="d7170-104">TEXT.cursor</span></span>

<span data-ttu-id="d7170-105">Атрибут **cursor** указывает или получает значение, указывающее, какой курсор отображается при наведении указателя мыши на элемент управления Text.</span><span class="sxs-lookup"><span data-stu-id="d7170-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the Text control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="d7170-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="d7170-106">Possible Values</span></span>

<span data-ttu-id="d7170-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d7170-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="d7170-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d7170-108">Value</span></span>            | <span data-ttu-id="d7170-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d7170-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7170-110">система</span><span class="sxs-lookup"><span data-stu-id="d7170-110">system</span></span>           | <span data-ttu-id="d7170-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d7170-111">Default.</span></span> <span data-ttu-id="d7170-112">Зависимый от платформы курсор (обычно это стрелка).</span><span class="sxs-lookup"><span data-stu-id="d7170-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="d7170-113">правый</span><span class="sxs-lookup"><span data-stu-id="d7170-113">hand</span></span>             | <span data-ttu-id="d7170-114">Правый.</span><span class="sxs-lookup"><span data-stu-id="d7170-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="d7170-115">help</span><span class="sxs-lookup"><span data-stu-id="d7170-115">help</span></span>             | <span data-ttu-id="d7170-116">Стрелка с вопросительным знаком, указывающим на наличие справки.</span><span class="sxs-lookup"><span data-stu-id="d7170-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="d7170-117">сизеалл</span><span class="sxs-lookup"><span data-stu-id="d7170-117">sizeall</span></span>          | <span data-ttu-id="d7170-118">4-направленная стрелка, указывающая на север, Юг, Восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="d7170-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="d7170-119">сизенесв</span><span class="sxs-lookup"><span data-stu-id="d7170-119">sizenesw</span></span>         | <span data-ttu-id="d7170-120">Двойная стрелка, указывающая на северо-восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="d7170-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="d7170-121">сизенс</span><span class="sxs-lookup"><span data-stu-id="d7170-121">sizens</span></span>           | <span data-ttu-id="d7170-122">Двусторонняя стрелка, указывающая на север и Юг.</span><span class="sxs-lookup"><span data-stu-id="d7170-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="d7170-123">сизенвсе</span><span class="sxs-lookup"><span data-stu-id="d7170-123">sizenwse</span></span>         | <span data-ttu-id="d7170-124">Двойная стрелка, указывающая на северо-запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="d7170-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="d7170-125">сизеве</span><span class="sxs-lookup"><span data-stu-id="d7170-125">sizewe</span></span>           | <span data-ttu-id="d7170-126">Двойная стрелка, указывающая на запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="d7170-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="d7170-127">Стрелка вверх</span><span class="sxs-lookup"><span data-stu-id="d7170-127">uparrow</span></span>          | <span data-ttu-id="d7170-128">Вертикальная стрелка, указывающая вверх.</span><span class="sxs-lookup"><span data-stu-id="d7170-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="d7170-129">\*. ani или \* . cur</span><span class="sxs-lookup"><span data-stu-id="d7170-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="d7170-130">Любой ANI или cur-файл (должен находиться в том же каталоге, что и файл WMS, или в WMZ-файле).</span><span class="sxs-lookup"><span data-stu-id="d7170-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

<span data-ttu-id="d7170-131">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="d7170-131">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7170-132">Требования</span><span class="sxs-lookup"><span data-stu-id="d7170-132">Requirements</span></span>



| <span data-ttu-id="d7170-133">Требование</span><span class="sxs-lookup"><span data-stu-id="d7170-133">Requirement</span></span> | <span data-ttu-id="d7170-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d7170-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d7170-135">Версия</span><span class="sxs-lookup"><span data-stu-id="d7170-135">Version</span></span><br/> | <span data-ttu-id="d7170-136">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="d7170-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7170-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7170-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7170-138">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="d7170-138">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





