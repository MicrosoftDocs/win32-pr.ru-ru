---
title: Элемент LISTBOX
description: Элемент LISTBOX
ms.assetid: b83ba0cb-1838-494d-b4cb-55b4da18a038
keywords:
- Обложки проигрывателя Windows Media, элемент LISTBOX
- обложки, элемент LISTBOX
- Элемент LISTBOX
- Справочник по обложкам, элементу LISTBOX
- элементы, LISTBOX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d9566d11586e995b289a0048dacb29a91921b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067761"
---
# <a name="listbox-element"></a><span data-ttu-id="ffdb3-108">Элемент LISTBOX</span><span class="sxs-lookup"><span data-stu-id="ffdb3-108">LISTBOX Element</span></span>

<span data-ttu-id="ffdb3-109">Элемент **ListBox** предоставляет пользователям возможность выбирать элементы из списка.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-109">The **LISTBOX** element provides a way for users to select items from a list.</span></span> <span data-ttu-id="ffdb3-110">Эти элементы могут быть заданы с помощью элементов **Item** в качестве потомков элемента **ListBox** .</span><span class="sxs-lookup"><span data-stu-id="ffdb3-110">These items can be specified by using **ITEM** elements as children of the **LISTBOX** element.</span></span> <span data-ttu-id="ffdb3-111">Если необходим элемент управления "список", который отображается только при необходимости, используйте элемент **Popup** , который идентичен элементу **ListBox** , за исключением значения по умолчанию для атрибута **всплывающего окна** , определяющего его поведение при отображении.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-111">If you need a list box control that is displayed only when needed, use the **POPUP** element, which is identical to the **LISTBOX** element except for the default value of the **popUp** attribute, which dictates its display behavior.</span></span>

<span data-ttu-id="ffdb3-112">Элемент **ListBox** поддерживает следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-112">The **LISTBOX** element supports the following attributes.</span></span>



| <span data-ttu-id="ffdb3-113">attribute</span><span class="sxs-lookup"><span data-stu-id="ffdb3-113">Attribute</span></span>                                        | <span data-ttu-id="ffdb3-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ffdb3-114">Description</span></span>                                                                                                           |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffdb3-115">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ffdb3-115">backgroundColor</span></span>](listbox-backgroundcolor.md)   | <span data-ttu-id="ffdb3-116">Указывает или получает цвет фона в элементе управления "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-116">Specifies or retrieves the background color in the list box control.</span></span>                                                  |
| [<span data-ttu-id="ffdb3-117">цвета</span><span class="sxs-lookup"><span data-stu-id="ffdb3-117">border</span></span>](listbox-border.md)                     | <span data-ttu-id="ffdb3-118">Указывает или получает значение, указывающее, имеет ли элемент управления "список" границу.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-118">Specifies or retrieves a value indicating whether the list box control has a border.</span></span> <span data-ttu-id="ffdb3-119">Можно задать только во время разработки.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-119">Can only be set at design time.</span></span>  |
| [<span data-ttu-id="ffdb3-120">фирствисиблеитем</span><span class="sxs-lookup"><span data-stu-id="ffdb3-120">firstVisibleItem</span></span>](listbox-firstvisibleitem.md) | <span data-ttu-id="ffdb3-121">Указывает или получает индекс первой видимой строки в элементе управления "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-121">Specifies or retrieves the index of the first visible line in the list box control.</span></span>                                   |
| [<span data-ttu-id="ffdb3-122">фокуситем</span><span class="sxs-lookup"><span data-stu-id="ffdb3-122">focusItem</span></span>](listbox-focusitem.md)               | <span data-ttu-id="ffdb3-123">Указывает или получает строку, содержащую фокус.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-123">Specifies or retrieves the line that contains focus.</span></span>                                                                  |
| [<span data-ttu-id="ffdb3-124">фонтфаце</span><span class="sxs-lookup"><span data-stu-id="ffdb3-124">fontFace</span></span>](listbox-fontface.md)                 | <span data-ttu-id="ffdb3-125">Указывает или получает шрифт для элемента управления "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-125">Specifies or retrieves the font for the list box control.</span></span>                                                             |
| [<span data-ttu-id="ffdb3-126">fontSize</span><span class="sxs-lookup"><span data-stu-id="ffdb3-126">fontSize</span></span>](listbox-fontsize.md)                 | <span data-ttu-id="ffdb3-127">Указывает или получает размер шрифта для элемента управления "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-127">Specifies or retrieves the font size for the list box control.</span></span>                                                        |
| [<span data-ttu-id="ffdb3-128">fontStyle</span><span class="sxs-lookup"><span data-stu-id="ffdb3-128">fontStyle</span></span>](listbox-fontstyle.md)               | <span data-ttu-id="ffdb3-129">Указывает или получает стиль шрифта для элемента управления "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-129">Specifies or retrieves the font style for the list box control.</span></span>                                                       |
| [<span data-ttu-id="ffdb3-130">foregroundColor</span><span class="sxs-lookup"><span data-stu-id="ffdb3-130">foregroundColor</span></span>](listbox-foregroundcolor.md)   | <span data-ttu-id="ffdb3-131">Указывает или получает цвет текста в элементе управления "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-131">Specifies or retrieves the text color in the list box control.</span></span>                                                        |
| [<span data-ttu-id="ffdb3-132">itemCount</span><span class="sxs-lookup"><span data-stu-id="ffdb3-132">itemCount</span></span>](listbox-itemcount.md)               | <span data-ttu-id="ffdb3-133">Возвращает число элементов в элементе управления "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-133">Retrieves the number of items in the list box control.</span></span>                                                                |
| [<span data-ttu-id="ffdb3-134">Множественный выбор</span><span class="sxs-lookup"><span data-stu-id="ffdb3-134">multiSelect</span></span>](listbox-multiselect.md)           | <span data-ttu-id="ffdb3-135">Указывает или получает значение, указывающее, может ли пользователь выбрать несколько строк.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-135">Specifies or retrieves a value indicating whether the user can select multiple lines.</span></span> <span data-ttu-id="ffdb3-136">Можно задать только во время разработки.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-136">Can only be set at design time.</span></span> |
| [<span data-ttu-id="ffdb3-137">Подсказки</span><span class="sxs-lookup"><span data-stu-id="ffdb3-137">popUp</span></span>](listbox-popup.md)                       | <span data-ttu-id="ffdb3-138">Задает значение, указывающее, представляет ли элемент элемент управления "всплывающее окно" или "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-138">Specifies a value indicating whether the element represents a popup or list box control.</span></span>                              |
| [<span data-ttu-id="ffdb3-139">readOnly</span><span class="sxs-lookup"><span data-stu-id="ffdb3-139">readOnly</span></span>](listbox-readonly.md)                 | <span data-ttu-id="ffdb3-140">Указывает или получает значение, указывающее, доступен ли текст только для чтения, или пользователь может выбрать текст.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-140">Specifies or retrieves a value indicating whether text is read-only or text can be selected by the user.</span></span>              |
| [<span data-ttu-id="ffdb3-141">selectedItem</span><span class="sxs-lookup"><span data-stu-id="ffdb3-141">selectedItem</span></span>](listbox-selecteditem.md)         | <span data-ttu-id="ffdb3-142">Указывает или получает индекс элемента, выбранного в элементе управления "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-142">Specifies or retrieves the index of the item selected in the list box control.</span></span>                                        |
| [<span data-ttu-id="ffdb3-143">сортируются</span><span class="sxs-lookup"><span data-stu-id="ffdb3-143">sorted</span></span>](listbox-sorted.md)                     | <span data-ttu-id="ffdb3-144">Указывает или получает значение, указывающее, сортируется ли элемент управления "список" в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-144">Specifies or retrieves a value indicating whether the list box control is sorted alphabetically.</span></span>                      |



 

<span data-ttu-id="ffdb3-145">Элемент **ListBox** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-145">The **LISTBOX** element supports the following methods.</span></span>



| <span data-ttu-id="ffdb3-146">Метод</span><span class="sxs-lookup"><span data-stu-id="ffdb3-146">Method</span></span>                                                 | <span data-ttu-id="ffdb3-147">Описание</span><span class="sxs-lookup"><span data-stu-id="ffdb3-147">Description</span></span>                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffdb3-148">аппендитем</span><span class="sxs-lookup"><span data-stu-id="ffdb3-148">appendItem</span></span>](listbox-appenditem.md)                   | <span data-ttu-id="ffdb3-149">Вставляет новый текст в конец элемента управления "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-149">Inserts new text at the end of the list box control.</span></span>                                                                  |
| [<span data-ttu-id="ffdb3-150">deleteAll</span><span class="sxs-lookup"><span data-stu-id="ffdb3-150">deleteAll</span></span>](listbox-deleteall.md)                     | <span data-ttu-id="ffdb3-151">Удаляет все элементы из элемента управления "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-151">Deletes all items from the list box control.</span></span>                                                                          |
| [<span data-ttu-id="ffdb3-152">deleteItem</span><span class="sxs-lookup"><span data-stu-id="ffdb3-152">deleteItem</span></span>](listbox-deleteitem.md)                   | <span data-ttu-id="ffdb3-153">Удаляет элемент управления "список" по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-153">Deletes the list box control item at the specified index.</span></span>                                                             |
| [<span data-ttu-id="ffdb3-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="ffdb3-154">dismiss</span></span>](listbox-dismiss.md)                         | <span data-ttu-id="ffdb3-155">Скрывает элемент управления.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-155">Hides the control.</span></span>                                                                                                    |
| [<span data-ttu-id="ffdb3-156">findItem</span><span class="sxs-lookup"><span data-stu-id="ffdb3-156">findItem</span></span>](listbox-finditem.md)                       | <span data-ttu-id="ffdb3-157">Выполняет поиск заданной строки, начиная с элемента, следующего за указанным индексом элемента.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-157">Searches for a given string starting with the item following the specified item index.</span></span>                                |
| [<span data-ttu-id="ffdb3-158">getItem</span><span class="sxs-lookup"><span data-stu-id="ffdb3-158">getItem</span></span>](listbox-getitem.md)                         | <span data-ttu-id="ffdb3-159">Извлекает текст для элемента с указанным индексом.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-159">Retrieves the text for the item with the specified index.</span></span>                                                             |
| [<span data-ttu-id="ffdb3-160">жетнекстселектедитем</span><span class="sxs-lookup"><span data-stu-id="ffdb3-160">getNextSelectedItem</span></span>](listbox-getnextselecteditem.md) | <span data-ttu-id="ffdb3-161">Извлекает следующий выбранный элемент в элементе управления "список", начиная с элемента с указанным индексом.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-161">Retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span> |
| [<span data-ttu-id="ffdb3-162">insertItem</span><span class="sxs-lookup"><span data-stu-id="ffdb3-162">insertItem</span></span>](listbox-insertitem.md)                   | <span data-ttu-id="ffdb3-163">Вставляет указанный текст по указанному индексу в элементе управления "список".</span><span class="sxs-lookup"><span data-stu-id="ffdb3-163">Inserts the specified text at the specified index in the list box control.</span></span>                                            |
| [<span data-ttu-id="ffdb3-164">replaceItem</span><span class="sxs-lookup"><span data-stu-id="ffdb3-164">replaceItem</span></span>](listbox-replaceitem.md)                 | <span data-ttu-id="ffdb3-165">Заменяет текст с указанным индексом на указанный текст.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-165">Replaces the text at the specified index with the specified text.</span></span>                                                     |
| [<span data-ttu-id="ffdb3-166">сетселектедстате</span><span class="sxs-lookup"><span data-stu-id="ffdb3-166">setSelectedState</span></span>](listbox-setselectedstate.md)       | <span data-ttu-id="ffdb3-167">Выбирает или отменяет выделение элемента с указанным индексом.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-167">Selects or unselects the item with the specified index.</span></span>                                                               |
| <span data-ttu-id="ffdb3-168">[show](listbox-show.md).</span><span class="sxs-lookup"><span data-stu-id="ffdb3-168">[show](listbox-show.md)</span></span>                               | <span data-ttu-id="ffdb3-169">Отображает элемент управления.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-169">Displays the control.</span></span>                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="ffdb3-170">Для этого элемента требуется проигрыватель Windows Media для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ffdb3-170">This element requires Windows Media Player for Windows XP or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ffdb3-171">См. также</span><span class="sxs-lookup"><span data-stu-id="ffdb3-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffdb3-172">**Элемент POPUP**</span><span class="sxs-lookup"><span data-stu-id="ffdb3-172">**POPUP Element**</span></span>](popup-element.md)
</dt> <dt>

[<span data-ttu-id="ffdb3-173">**Справочник по программированию для обложки**</span><span class="sxs-lookup"><span data-stu-id="ffdb3-173">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




