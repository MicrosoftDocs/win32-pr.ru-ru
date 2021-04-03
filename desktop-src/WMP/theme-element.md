---
title: Элемент THEME
description: Элемент THEME
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Обложки проигрывателя Windows Media, элемент THEME
- обложки, элемент THEME
- Элемент THEME
- Справочник по обложкам, элементу THEME
- элементы, тема
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887996"
---
# <a name="theme-element"></a><span data-ttu-id="1aee3-108">Элемент THEME</span><span class="sxs-lookup"><span data-stu-id="1aee3-108">THEME Element</span></span>

<span data-ttu-id="1aee3-109">Элемент **Theme** является родительским элементом обложки и содержит один или несколько элементов **представления** , которые, в свою очередь, содержат все остальные элементы в обложке.</span><span class="sxs-lookup"><span data-stu-id="1aee3-109">The **THEME** element is the parent-level element of a skin, and contains one or more **VIEW** elements, which in turn contain all other elements within a skin.</span></span> <span data-ttu-id="1aee3-110">В коде скрипта доступ к элементу **темы** осуществляется через глобальный атрибут **темы** , а не через имя, заданное атрибутом **ID** , который не поддерживается элементом **Theme** .</span><span class="sxs-lookup"><span data-stu-id="1aee3-110">Within script code, the **THEME** element is accessed through the **theme** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **THEME** element.</span></span>

<span data-ttu-id="1aee3-111">Элемент **Theme** поддерживает следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="1aee3-111">The **THEME** element supports the following attributes.</span></span>



| <span data-ttu-id="1aee3-112">attribute</span><span class="sxs-lookup"><span data-stu-id="1aee3-112">Attribute</span></span>                                | <span data-ttu-id="1aee3-113">Описание</span><span class="sxs-lookup"><span data-stu-id="1aee3-113">Description</span></span>                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1aee3-114">календаря</span><span class="sxs-lookup"><span data-stu-id="1aee3-114">author</span></span>](theme-author.md)               | <span data-ttu-id="1aee3-115">Указывает или получает имя автора обложки.</span><span class="sxs-lookup"><span data-stu-id="1aee3-115">Specifies or retrieves the name of the author of the skin.</span></span>                                                                      |
| [<span data-ttu-id="1aee3-116">аусорверсион</span><span class="sxs-lookup"><span data-stu-id="1aee3-116">authorVersion</span></span>](theme-authorversion.md) | <span data-ttu-id="1aee3-117">Указывает или получает номер версии обложки, назначенный автором.</span><span class="sxs-lookup"><span data-stu-id="1aee3-117">Specifies or retrieves the version number of the skin as assigned by the author.</span></span>                                                |
| [<span data-ttu-id="1aee3-118">Информация</span><span class="sxs-lookup"><span data-stu-id="1aee3-118">copyright</span></span>](theme-copyright.md)         | <span data-ttu-id="1aee3-119">Указывает или получает строку авторских прав для обложки.</span><span class="sxs-lookup"><span data-stu-id="1aee3-119">Specifies or retrieves the copyright string for the skin.</span></span>                                                                       |
| [<span data-ttu-id="1aee3-120">куррентвиевид</span><span class="sxs-lookup"><span data-stu-id="1aee3-120">currentViewID</span></span>](theme-currentviewid.md) | <span data-ttu-id="1aee3-121">Указывает или получает отображаемое в данный момент **представление**.</span><span class="sxs-lookup"><span data-stu-id="1aee3-121">Specifies or retrieves the currently displayed **VIEW**.</span></span>                                                                        |
| [<span data-ttu-id="1aee3-122">title</span><span class="sxs-lookup"><span data-stu-id="1aee3-122">title</span></span>](theme-title.md)                 | <span data-ttu-id="1aee3-123">Указывает или получает заголовок обложки.</span><span class="sxs-lookup"><span data-stu-id="1aee3-123">Specifies or retrieves the title of the skin.</span></span>                                                                                   |
| [<span data-ttu-id="1aee3-124">version</span><span class="sxs-lookup"><span data-stu-id="1aee3-124">version</span></span>](theme-version.md)             | <span data-ttu-id="1aee3-125">Указывает или получает номер версии проигрывателя Windows Media, для которого была создана оболочка.</span><span class="sxs-lookup"><span data-stu-id="1aee3-125">Specifies or retrieves the Windows Media Player version number for which the skin was authored.</span></span> <span data-ttu-id="1aee3-126">Можно задать только во время разработки.</span><span class="sxs-lookup"><span data-stu-id="1aee3-126">Can only be set at design time.</span></span> |



 

<span data-ttu-id="1aee3-127">Элемент **Theme** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1aee3-127">The **THEME** element supports the following methods.</span></span>



| <span data-ttu-id="1aee3-128">Метод</span><span class="sxs-lookup"><span data-stu-id="1aee3-128">Method</span></span>                                         | <span data-ttu-id="1aee3-129">Описание</span><span class="sxs-lookup"><span data-stu-id="1aee3-129">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1aee3-130">closeView</span><span class="sxs-lookup"><span data-stu-id="1aee3-130">closeView</span></span>](theme-closeview.md)               | <span data-ttu-id="1aee3-131">Закрывает открытое **представление**.</span><span class="sxs-lookup"><span data-stu-id="1aee3-131">Closes an open **VIEW**.</span></span>                                                                                        |
| [<span data-ttu-id="1aee3-132">лоадпреференце</span><span class="sxs-lookup"><span data-stu-id="1aee3-132">loadPreference</span></span>](theme-loadpreference.md)     | <span data-ttu-id="1aee3-133">Загружает предпочтение из реестра.</span><span class="sxs-lookup"><span data-stu-id="1aee3-133">Loads a preference from the registry.</span></span>                                                                           |
| [<span data-ttu-id="1aee3-134">логстринг</span><span class="sxs-lookup"><span data-stu-id="1aee3-134">logString</span></span>](theme-logstring.md)               | <span data-ttu-id="1aee3-135">Записывает определяемую пользователем строку в файл ошибок, если ведение журнала включено.</span><span class="sxs-lookup"><span data-stu-id="1aee3-135">Logs a user-defined string to the error file, if logging is enabled.</span></span>                                            |
| [<span data-ttu-id="1aee3-136">опендиалог</span><span class="sxs-lookup"><span data-stu-id="1aee3-136">openDialog</span></span>](theme-opendialog.md)             | <span data-ttu-id="1aee3-137">Открывает диалоговое окно "файл".</span><span class="sxs-lookup"><span data-stu-id="1aee3-137">Opens a file dialog box.</span></span>                                                                                        |
| [<span data-ttu-id="1aee3-138">openView</span><span class="sxs-lookup"><span data-stu-id="1aee3-138">openView</span></span>](theme-openview.md)                 | <span data-ttu-id="1aee3-139">Открывает **представление** в новом окне.</span><span class="sxs-lookup"><span data-stu-id="1aee3-139">Opens a **VIEW** in a new window.</span></span>                                                                               |
| [<span data-ttu-id="1aee3-140">опенвиеврелативе</span><span class="sxs-lookup"><span data-stu-id="1aee3-140">openViewRelative</span></span>](theme-openviewrelative.md) | <span data-ttu-id="1aee3-141">Открывает **представление** в новом окне с указанной начальной позицией относительно левого верхнего угла обложки.</span><span class="sxs-lookup"><span data-stu-id="1aee3-141">Opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span> |
| [<span data-ttu-id="1aee3-142">playSound</span><span class="sxs-lookup"><span data-stu-id="1aee3-142">playSound</span></span>](theme-playsound.md)               | <span data-ttu-id="1aee3-143">Воспроизводит указанный звуковой файл.</span><span class="sxs-lookup"><span data-stu-id="1aee3-143">Plays the specified sound file.</span></span>                                                                                 |
| [<span data-ttu-id="1aee3-144">савепреференце</span><span class="sxs-lookup"><span data-stu-id="1aee3-144">savePreference</span></span>](theme-savepreference.md)     | <span data-ttu-id="1aee3-145">Сохраняет настройки в реестре.</span><span class="sxs-lookup"><span data-stu-id="1aee3-145">Saves a preference in the registry.</span></span>                                                                             |
| [<span data-ttu-id="1aee3-146">шоверрордиалог</span><span class="sxs-lookup"><span data-stu-id="1aee3-146">showErrorDialog</span></span>](theme-showerrordialog.md)   | <span data-ttu-id="1aee3-147">Отображает стандартное диалоговое окно ошибки.</span><span class="sxs-lookup"><span data-stu-id="1aee3-147">Displays the standard error dialog box.</span></span>                                                                         |



 

<span data-ttu-id="1aee3-148">Элемент **Theme** не поддерживает обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="1aee3-148">The **THEME** element does not support event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1aee3-149">См. также</span><span class="sxs-lookup"><span data-stu-id="1aee3-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aee3-150">**Справочник по программированию для обложки**</span><span class="sxs-lookup"><span data-stu-id="1aee3-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




