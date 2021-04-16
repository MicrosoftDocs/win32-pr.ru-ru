---
title: БУТТОНЕЛЕМЕНТ. Cursor
description: Атрибут Cursor указывает или получает значение курсора БУТТОНЕЛЕМЕНТ, которое появляется при наведении указателя мыши на БУТТОНЕЛЕМЕНТ.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- Проигрыватель Windows Media БУТТОНЕЛЕМЕНТ. Cursor
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699245"
---
# <a name="buttonelementcursor"></a><span data-ttu-id="a4d94-104">БУТТОНЕЛЕМЕНТ. Cursor</span><span class="sxs-lookup"><span data-stu-id="a4d94-104">BUTTONELEMENT.cursor</span></span>

<span data-ttu-id="a4d94-105">Атрибут **cursor** указывает или получает значение курсора **буттонелемент** , которое появляется при наведении указателя мыши на **буттонелемент**.</span><span class="sxs-lookup"><span data-stu-id="a4d94-105">The **cursor** attribute specifies or retrieves the value of the **BUTTONELEMENT** cursor that appears when the mouse is over the **BUTTONELEMENT**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="a4d94-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="a4d94-106">Possible Values</span></span>

<span data-ttu-id="a4d94-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a4d94-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="a4d94-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a4d94-108">Value</span></span>            | <span data-ttu-id="a4d94-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a4d94-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d94-110">система</span><span class="sxs-lookup"><span data-stu-id="a4d94-110">system</span></span>           | <span data-ttu-id="a4d94-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4d94-111">Default.</span></span> <span data-ttu-id="a4d94-112">Зависимый от платформы курсор (обычно это стрелка).</span><span class="sxs-lookup"><span data-stu-id="a4d94-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="a4d94-113">правый</span><span class="sxs-lookup"><span data-stu-id="a4d94-113">hand</span></span>             | <span data-ttu-id="a4d94-114">Правый.</span><span class="sxs-lookup"><span data-stu-id="a4d94-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="a4d94-115">help</span><span class="sxs-lookup"><span data-stu-id="a4d94-115">help</span></span>             | <span data-ttu-id="a4d94-116">Стрелка с вопросительным знаком, указывающим на наличие справки.</span><span class="sxs-lookup"><span data-stu-id="a4d94-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="a4d94-117">сизеалл</span><span class="sxs-lookup"><span data-stu-id="a4d94-117">sizeall</span></span>          | <span data-ttu-id="a4d94-118">4-направленная стрелка, указывающая на север, Юг, Восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="a4d94-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="a4d94-119">сизенесв</span><span class="sxs-lookup"><span data-stu-id="a4d94-119">sizenesw</span></span>         | <span data-ttu-id="a4d94-120">Двойная стрелка, указывающая на северо-восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="a4d94-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="a4d94-121">сизенс</span><span class="sxs-lookup"><span data-stu-id="a4d94-121">sizens</span></span>           | <span data-ttu-id="a4d94-122">Двусторонняя стрелка, указывающая на север и Юг.</span><span class="sxs-lookup"><span data-stu-id="a4d94-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="a4d94-123">сизенвсе</span><span class="sxs-lookup"><span data-stu-id="a4d94-123">sizenwse</span></span>         | <span data-ttu-id="a4d94-124">Двойная стрелка, указывающая на северо-запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="a4d94-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="a4d94-125">сизеве</span><span class="sxs-lookup"><span data-stu-id="a4d94-125">sizewe</span></span>           | <span data-ttu-id="a4d94-126">Двойная стрелка, указывающая на запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="a4d94-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="a4d94-127">Стрелка вверх</span><span class="sxs-lookup"><span data-stu-id="a4d94-127">uparrow</span></span>          | <span data-ttu-id="a4d94-128">Вертикальная стрелка, указывающая вверх.</span><span class="sxs-lookup"><span data-stu-id="a4d94-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="a4d94-129">\*. ani или \* . cur</span><span class="sxs-lookup"><span data-stu-id="a4d94-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="a4d94-130">Любой ANI или cur-файл (должен находиться в том же каталоге, что и файл WMS, или в WMZ-файле).</span><span class="sxs-lookup"><span data-stu-id="a4d94-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a4d94-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4d94-131">Remarks</span></span>

<span data-ttu-id="a4d94-132">Если указано недопустимое значение, сохраняется предыдущее значение.</span><span class="sxs-lookup"><span data-stu-id="a4d94-132">If an invalid value is specified, the previous value is maintained.</span></span>

<span data-ttu-id="a4d94-133">Пути к именам файлов курсоров игнорируются, поэтому файл курсора должен находиться в каталоге по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4d94-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4d94-134">Требования</span><span class="sxs-lookup"><span data-stu-id="a4d94-134">Requirements</span></span>



| <span data-ttu-id="a4d94-135">Требование</span><span class="sxs-lookup"><span data-stu-id="a4d94-135">Requirement</span></span> | <span data-ttu-id="a4d94-136">Значение</span><span class="sxs-lookup"><span data-stu-id="a4d94-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a4d94-137">Версия</span><span class="sxs-lookup"><span data-stu-id="a4d94-137">Version</span></span><br/> | <span data-ttu-id="a4d94-138">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="a4d94-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4d94-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4d94-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d94-140">**БУТТОНЕЛЕМЕНТ, элемент**</span><span class="sxs-lookup"><span data-stu-id="a4d94-140">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> </dl>

 

 





