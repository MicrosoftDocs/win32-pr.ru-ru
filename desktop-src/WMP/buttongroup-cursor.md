---
title: BUTTONGROUP. Cursor
description: Атрибут Cursor указывает или получает тип курсора, который появляется при наведении указателя мыши на кнопку в BUTTONGROUP.
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Cursor
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695134"
---
# <a name="buttongroupcursor"></a><span data-ttu-id="ad36f-104">BUTTONGROUP. Cursor</span><span class="sxs-lookup"><span data-stu-id="ad36f-104">BUTTONGROUP.cursor</span></span>

<span data-ttu-id="ad36f-105">Атрибут **cursor** указывает или получает тип курсора, который появляется при наведении указателя мыши на кнопку в **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="ad36f-105">The **cursor** attribute specifies or retrieves the type of cursor that appears when the mouse is over a button in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="ad36f-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ad36f-106">Possible Values</span></span>

<span data-ttu-id="ad36f-107">Этот атрибут является **строкой** для чтения и записи, содержащей одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ad36f-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="ad36f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ad36f-108">Value</span></span>            | <span data-ttu-id="ad36f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ad36f-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad36f-110">система</span><span class="sxs-lookup"><span data-stu-id="ad36f-110">system</span></span>           | <span data-ttu-id="ad36f-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad36f-111">Default.</span></span> <span data-ttu-id="ad36f-112">Зависимый от платформы курсор (обычно это стрелка).</span><span class="sxs-lookup"><span data-stu-id="ad36f-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="ad36f-113">правый</span><span class="sxs-lookup"><span data-stu-id="ad36f-113">hand</span></span>             | <span data-ttu-id="ad36f-114">Правый.</span><span class="sxs-lookup"><span data-stu-id="ad36f-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="ad36f-115">help</span><span class="sxs-lookup"><span data-stu-id="ad36f-115">help</span></span>             | <span data-ttu-id="ad36f-116">Стрелка с вопросительным знаком, указывающим на наличие справки.</span><span class="sxs-lookup"><span data-stu-id="ad36f-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="ad36f-117">сизеалл</span><span class="sxs-lookup"><span data-stu-id="ad36f-117">sizeall</span></span>          | <span data-ttu-id="ad36f-118">4-направленная стрелка, указывающая на север, Юг, Восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="ad36f-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="ad36f-119">сизенесв</span><span class="sxs-lookup"><span data-stu-id="ad36f-119">sizenesw</span></span>         | <span data-ttu-id="ad36f-120">Двойная стрелка, указывающая на северо-восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="ad36f-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="ad36f-121">сизенс</span><span class="sxs-lookup"><span data-stu-id="ad36f-121">sizens</span></span>           | <span data-ttu-id="ad36f-122">Двусторонняя стрелка, указывающая на север и Юг.</span><span class="sxs-lookup"><span data-stu-id="ad36f-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="ad36f-123">сизенвсе</span><span class="sxs-lookup"><span data-stu-id="ad36f-123">sizenwse</span></span>         | <span data-ttu-id="ad36f-124">Двойная стрелка, указывающая на северо-запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="ad36f-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="ad36f-125">сизеве</span><span class="sxs-lookup"><span data-stu-id="ad36f-125">sizewe</span></span>           | <span data-ttu-id="ad36f-126">Двойная стрелка, указывающая на запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="ad36f-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="ad36f-127">Стрелка вверх</span><span class="sxs-lookup"><span data-stu-id="ad36f-127">uparrow</span></span>          | <span data-ttu-id="ad36f-128">Вертикальная стрелка, указывающая вверх.</span><span class="sxs-lookup"><span data-stu-id="ad36f-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="ad36f-129">\*. ani или \* . cur</span><span class="sxs-lookup"><span data-stu-id="ad36f-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="ad36f-130">Любой ANI или cur-файл (должен находиться в том же каталоге, что и файл WMS, или в WMZ-файле).</span><span class="sxs-lookup"><span data-stu-id="ad36f-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ad36f-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad36f-131">Remarks</span></span>

<span data-ttu-id="ad36f-132">Указанный курсор применяется ко всем кнопкам в **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="ad36f-132">The cursor specified applies to all buttons in the **BUTTONGROUP**.</span></span>

<span data-ttu-id="ad36f-133">Если указано недопустимое значение курсора, оно остается в ранее заданном значении.</span><span class="sxs-lookup"><span data-stu-id="ad36f-133">If you specify an invalid cursor value, it remains at the previously set value.</span></span>

<span data-ttu-id="ad36f-134">Пути к именам файлов курсоров игнорируются, поэтому файл курсора должен находиться в каталоге по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad36f-134">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad36f-135">Требования</span><span class="sxs-lookup"><span data-stu-id="ad36f-135">Requirements</span></span>



| <span data-ttu-id="ad36f-136">Требование</span><span class="sxs-lookup"><span data-stu-id="ad36f-136">Requirement</span></span> | <span data-ttu-id="ad36f-137">Значение</span><span class="sxs-lookup"><span data-stu-id="ad36f-137">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ad36f-138">Версия</span><span class="sxs-lookup"><span data-stu-id="ad36f-138">Version</span></span><br/> | <span data-ttu-id="ad36f-139">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ad36f-139">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad36f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad36f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad36f-141">**BUTTONGROUP, элемент**</span><span class="sxs-lookup"><span data-stu-id="ad36f-141">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





