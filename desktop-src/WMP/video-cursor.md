---
title: ВИДЕО. курсор
description: Атрибут Cursor указывает или получает значение курсора, которое используется при наведении мыши на область видео, доступную для щелчка.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- Проигрыватель Windows Media Player с видео. курсор
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708374"
---
# <a name="videocursor"></a><span data-ttu-id="0fac8-104">ВИДЕО. курсор</span><span class="sxs-lookup"><span data-stu-id="0fac8-104">VIDEO.cursor</span></span>

<span data-ttu-id="0fac8-105">Атрибут **cursor** указывает или получает значение курсора, которое используется при наведении мыши на область видео, доступную для щелчка.</span><span class="sxs-lookup"><span data-stu-id="0fac8-105">The **cursor** attribute specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="0fac8-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="0fac8-106">Possible Values</span></span>

<span data-ttu-id="0fac8-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0fac8-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="0fac8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0fac8-108">Value</span></span>            | <span data-ttu-id="0fac8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0fac8-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fac8-110">система</span><span class="sxs-lookup"><span data-stu-id="0fac8-110">system</span></span>           | <span data-ttu-id="0fac8-111">Зависимый от платформы курсор (обычно это стрелка).</span><span class="sxs-lookup"><span data-stu-id="0fac8-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="0fac8-112">правый</span><span class="sxs-lookup"><span data-stu-id="0fac8-112">hand</span></span>             | <span data-ttu-id="0fac8-113">Правый.</span><span class="sxs-lookup"><span data-stu-id="0fac8-113">Hand.</span></span>                                                                                       |
| <span data-ttu-id="0fac8-114">help</span><span class="sxs-lookup"><span data-stu-id="0fac8-114">help</span></span>             | <span data-ttu-id="0fac8-115">Стрелка с вопросительным знаком, указывающим на наличие справки.</span><span class="sxs-lookup"><span data-stu-id="0fac8-115">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="0fac8-116">сизеалл</span><span class="sxs-lookup"><span data-stu-id="0fac8-116">sizeall</span></span>          | <span data-ttu-id="0fac8-117">4-направленная стрелка, указывающая на север, Юг, Восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="0fac8-117">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="0fac8-118">сизенесв</span><span class="sxs-lookup"><span data-stu-id="0fac8-118">sizenesw</span></span>         | <span data-ttu-id="0fac8-119">Двойная стрелка, указывающая на северо-восток и Запад.</span><span class="sxs-lookup"><span data-stu-id="0fac8-119">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="0fac8-120">сизенс</span><span class="sxs-lookup"><span data-stu-id="0fac8-120">sizens</span></span>           | <span data-ttu-id="0fac8-121">Двусторонняя стрелка, указывающая на север и Юг.</span><span class="sxs-lookup"><span data-stu-id="0fac8-121">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="0fac8-122">сизенвсе</span><span class="sxs-lookup"><span data-stu-id="0fac8-122">sizenwse</span></span>         | <span data-ttu-id="0fac8-123">Двойная стрелка, указывающая на северо-запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="0fac8-123">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="0fac8-124">сизеве</span><span class="sxs-lookup"><span data-stu-id="0fac8-124">sizewe</span></span>           | <span data-ttu-id="0fac8-125">Двойная стрелка, указывающая на запад и Восток.</span><span class="sxs-lookup"><span data-stu-id="0fac8-125">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="0fac8-126">Стрелка вверх</span><span class="sxs-lookup"><span data-stu-id="0fac8-126">uparrow</span></span>          | <span data-ttu-id="0fac8-127">Вертикальная стрелка, указывающая вверх.</span><span class="sxs-lookup"><span data-stu-id="0fac8-127">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="0fac8-128">\*. ani или \* . cur</span><span class="sxs-lookup"><span data-stu-id="0fac8-128">\*.ani or \*.cur</span></span> | <span data-ttu-id="0fac8-129">Любой ANI или cur-файл (должен находиться в том же каталоге, что и файл WMS, или в WMZ-файле).</span><span class="sxs-lookup"><span data-stu-id="0fac8-129">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0fac8-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0fac8-130">Remarks</span></span>

<span data-ttu-id="0fac8-131">В целях отрисовки по умолчанию используется System.</span><span class="sxs-lookup"><span data-stu-id="0fac8-131">For rendering purposes, system is the default cursor.</span></span> <span data-ttu-id="0fac8-132">Значение по умолчанию, полученное из этого атрибута, — "" (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="0fac8-132">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fac8-133">Требования</span><span class="sxs-lookup"><span data-stu-id="0fac8-133">Requirements</span></span>



| <span data-ttu-id="0fac8-134">Требование</span><span class="sxs-lookup"><span data-stu-id="0fac8-134">Requirement</span></span> | <span data-ttu-id="0fac8-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0fac8-135">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0fac8-136">Версия</span><span class="sxs-lookup"><span data-stu-id="0fac8-136">Version</span></span><br/> | <span data-ttu-id="0fac8-137">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="0fac8-137">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0fac8-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fac8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fac8-139">**Элемент VIDEO**</span><span class="sxs-lookup"><span data-stu-id="0fac8-139">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





