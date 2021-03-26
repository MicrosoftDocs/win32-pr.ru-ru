---
description: Вы можете зарегистрировать список свойств уникального представления содержимого и шаблон макета для типа файла или элемента.
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: Регистрация набора свойств и шаблона макета представления содержимого для типа файла или элемента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e84861a0761f2f5ebb9737f62409c8f72e00bd
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104350802"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a><span data-ttu-id="d4253-103">Регистрация уникального набора свойств представления содержимого и шаблона макета для типа файла или элемента</span><span class="sxs-lookup"><span data-stu-id="d4253-103">How to Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item</span></span>

<span data-ttu-id="d4253-104">Вы можете зарегистрировать список свойств уникального представления содержимого и шаблон макета для типа файла или элемента.</span><span class="sxs-lookup"><span data-stu-id="d4253-104">You can register a unique Content view property list and layout pattern for the file type or item.</span></span> <span data-ttu-id="d4253-105">Если тип файла или элемент также связан с типом, регистрация конкретного представления содержимого для типа файла или элемента будет переопределять регистрацию типа.</span><span class="sxs-lookup"><span data-stu-id="d4253-105">If your file type or item is also associated with a Kind, the specific Content view registration of the file type or item will override the Kind registration.</span></span> <span data-ttu-id="d4253-106">Это может быть полезно, если наиболее важные свойства этого элемента отличаются от других элементов того же типа.</span><span class="sxs-lookup"><span data-stu-id="d4253-106">This might be useful if the most important properties for this item are different from other items of the same Kind.</span></span> <span data-ttu-id="d4253-107">Если не связать тип файла или элемент с типом элемента или напрямую зарегистрировать представление содержимого, система использует сведения о представлении содержимого по умолчанию (хранятся в разделе реестра, на который ссылается последний элемент в массиве ассоциаций всех элементов, в \_ корневом классе hKey classes \_ \\ \* )</span><span class="sxs-lookup"><span data-stu-id="d4253-107">If you do not associate your file type or item with an item Kind or directly register the Content view, the system uses the default Content view information (stored in a registry key referenced by the last element in all items' association array, HKEY\_CLASSES\_ROOT\\\*)</span></span>

<span data-ttu-id="d4253-108">Перед регистрацией пользовательского списка свойств для типа файла необходимо ознакомиться с режимом результатов поиска и режимом просмотра, а также с доступными шаблонами макета.</span><span class="sxs-lookup"><span data-stu-id="d4253-108">Before registering a custom property list for your file type, you should understand the Search Result mode and Browse mode, and the layout patterns that are available to you.</span></span>

## <a name="instructions"></a><span data-ttu-id="d4253-109">Инструкции</span><span class="sxs-lookup"><span data-stu-id="d4253-109">Instructions</span></span>

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a><span data-ttu-id="d4253-110">Шаг 1. Основные сведения о режиме результатов поиска и режиме просмотра</span><span class="sxs-lookup"><span data-stu-id="d4253-110">Step 1: Understanding the Search Result Mode and Browse Mode</span></span>

<span data-ttu-id="d4253-111">Для представления содержимого требуется определить шаблон макета и набор списков свойств для элемента в наборе результатов поиска (режим результатов поиска), а при переходе к расположению оболочки (режим просмотра).</span><span class="sxs-lookup"><span data-stu-id="d4253-111">Content view requires defining a layout pattern and set of property lists for an item in a set of search results (Search result mode), and when browsing to a Shell location (Browse mode).</span></span> <span data-ttu-id="d4253-112">Можно использовать те же значения для результатов поиска и для обзора, что и в случае `Kind.Music` .</span><span class="sxs-lookup"><span data-stu-id="d4253-112">You can use the same values for Search result and Browse, as `Kind.Music` does.</span></span> <span data-ttu-id="d4253-113">Кроме того, можно определить другой список свойств и (или) шаблон макета как `Kind.Document` есть.</span><span class="sxs-lookup"><span data-stu-id="d4253-113">Alternatively, you can define a different property list and/or layout pattern as `Kind.Document` does.</span></span>

<span data-ttu-id="d4253-114">В случае `Kind.Document` Пользователи часто выполняют поиск слов в тексте документа.</span><span class="sxs-lookup"><span data-stu-id="d4253-114">In the case of `Kind.Document`, users often search for words in the text of the document.</span></span> <span data-ttu-id="d4253-115">Поэтому лучшим выбором может быть выбор большего количества примеров текста в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="d4253-115">Therefore, including more sample text in the search result might be the best choice.</span></span> <span data-ttu-id="d4253-116">В следующем примере показано представление просмотра содержимого для `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="d4253-116">The following example illustrates the Browse Content view of `Kind.Document`.</span></span>

![Просмотр содержимого представления kind.docумент](images/content-view/browsecontentviewkinddocument.png)

<span data-ttu-id="d4253-118">Так как пользователи редко ищут определенный текст при просмотре документов, оптимизация выбора свойств и макета для отображения большего числа результатов поиска на экране может быть лучшим выбором.</span><span class="sxs-lookup"><span data-stu-id="d4253-118">Because users are rarely looking for particular text when browsing for documents, optimizing your choice of properties and layout to fit more search results on the screen might be the best choice.</span></span> <span data-ttu-id="d4253-119">На следующем снимке экрана показано представление содержимого поиска `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="d4253-119">The following screen shot illustrates the Search Content view of `Kind.Document`.</span></span>

### <a name="step-2-understanding-layout-patterns"></a><span data-ttu-id="d4253-120">Шаг 2. Основные сведения о шаблонах макета</span><span class="sxs-lookup"><span data-stu-id="d4253-120">Step 2: Understanding Layout Patterns</span></span>

<span data-ttu-id="d4253-121">Существует четыре шаблона макета: альфа, бета, гамма и Дельта.</span><span class="sxs-lookup"><span data-stu-id="d4253-121">There are four layout patterns: Alpha, Beta, Gamma, and Delta.</span></span>

<span data-ttu-id="d4253-122">**Макет Alpha**</span><span class="sxs-lookup"><span data-stu-id="d4253-122">**Alpha layout**</span></span>

<span data-ttu-id="d4253-123">Шаблон макета Alpha оптимизирован для результатов поиска документов, содержащих фрагменты.</span><span class="sxs-lookup"><span data-stu-id="d4253-123">The Alpha layout pattern is optimized for document search results that contain excerpts.</span></span> <span data-ttu-id="d4253-124">Он имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="d4253-124">It has the following specifications:</span></span>

-   <span data-ttu-id="d4253-125">Строки: 4</span><span class="sxs-lookup"><span data-stu-id="d4253-125">Rows: 4</span></span>
-   <span data-ttu-id="d4253-126">Свойства: 7</span><span class="sxs-lookup"><span data-stu-id="d4253-126">Properties: 7</span></span>
-   <span data-ttu-id="d4253-127">Макет Alpha, если элемент имеет 350 пикселей или больше пространства по горизонтали, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d4253-127">Alpha layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![шаблон макета Alpha](images/content-view/layout1.png)

-   <span data-ttu-id="d4253-129">На следующем рисунке показан макет Alpha, если элемент имеет 350 пикселей или больше пространства по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d4253-129">The following illustration shows the Alpha layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Схема, на которой показан пример макета Alpha](images/content-view/alphaviewmore.png)

-   <span data-ttu-id="d4253-131">На следующем рисунке показан макет Alpha, когда элемент имеет менее 350 пикселей горизонтального пространства.</span><span class="sxs-lookup"><span data-stu-id="d4253-131">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Снимок экрана, показывающий пример макета альфа в Microsoft Word.](images/content-view/layout2.png)

-   <span data-ttu-id="d4253-133">На следующем рисунке показан макет Alpha, когда элемент имеет менее 350 пикселей горизонтального пространства.</span><span class="sxs-lookup"><span data-stu-id="d4253-133">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Пример макета Alpha](images/content-view/alphaviewless.png)

<span data-ttu-id="d4253-135">**Макет бета-версии**</span><span class="sxs-lookup"><span data-stu-id="d4253-135">**Beta Layout**</span></span>

<span data-ttu-id="d4253-136">Шаблон макета бета-версии оптимизирован для результатов поиска по электронной почте, содержащих фрагменты.</span><span class="sxs-lookup"><span data-stu-id="d4253-136">The Beta layout pattern is optimized for email document search results that contain excerpts.</span></span> <span data-ttu-id="d4253-137">Он имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="d4253-137">It has the following specifications:</span></span>

-   <span data-ttu-id="d4253-138">Строки: 4</span><span class="sxs-lookup"><span data-stu-id="d4253-138">Rows: 4</span></span>
-   <span data-ttu-id="d4253-139">Свойства: 5</span><span class="sxs-lookup"><span data-stu-id="d4253-139">Properties: 5</span></span>
-   <span data-ttu-id="d4253-140">Бета-макет, если элемент имеет 350 пикселей или больше пространства по горизонтали, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d4253-140">Beta layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Схема, на которой показан пример макета бета-версии.](images/content-view/layout3.png)

-   <span data-ttu-id="d4253-142">На следующем рисунке показан макет бета-версии, если элемент имеет 350 пикселей или больше пространства по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d4253-142">The following illustration shows the beta layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Снимок экрана, на котором показан пример макета бета-версии для электронной почты.](images/content-view/betaviewmore.png)

-   <span data-ttu-id="d4253-144">На следующем рисунке показан макет бета-версии, когда у элемента меньше 350 пикселей по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d4253-144">The following illustration shows the Beta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Схема, на которой показан пример макета бета-версии с менее чем 350 пикселями по горизонтали.](images/content-view/layout4.png)

-   <span data-ttu-id="d4253-146">На следующем рисунке показан макет бета-версии, когда у элемента меньше 350 пикселей по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d4253-146">The following illustration shows the beta layout when the item has less than 350 pixels of horizontal space:</span></span>

    ![Пример макета бета-версии](images/content-view/betaviewless.png)

<span data-ttu-id="d4253-148">**Гамма-схема**</span><span class="sxs-lookup"><span data-stu-id="d4253-148">**Gamma Layout**</span></span>

<span data-ttu-id="d4253-149">Шаблон макета гаммы напоминает альфа, но использует макет с двумя строками, а не четыре.</span><span class="sxs-lookup"><span data-stu-id="d4253-149">The Gamma layout pattern is similar to Alpha but uses a two-line layout instead of four.</span></span> <span data-ttu-id="d4253-150">Этот макет идеально подходит для сценариев, в которых требуется просмотреть фрагмент, но требуется разместить на экране больше элементов, или для типов файлов, для которых требуется меньше места для отображения наиболее важных сведений.</span><span class="sxs-lookup"><span data-stu-id="d4253-150">This layout is ideal for scenarios in which you want to see a snippet but want to fit more items on the screen, or for file types that require less space to show the most critical information.</span></span> <span data-ttu-id="d4253-151">Гамма макета имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="d4253-151">The Gamma layout has the following specifications:</span></span>

-   <span data-ttu-id="d4253-152">Строки: 2</span><span class="sxs-lookup"><span data-stu-id="d4253-152">Rows: 2</span></span>
-   <span data-ttu-id="d4253-153">Свойства: 4</span><span class="sxs-lookup"><span data-stu-id="d4253-153">Properties: 4</span></span>
-   <span data-ttu-id="d4253-154">На следующем рисунке показана гамма макета, если элемент имеет 350 пикселей или больше пространства по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d4253-154">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Схема, на которой показан пример гамма-макета.](images/content-view/layout5.png)

-   <span data-ttu-id="d4253-156">На следующем рисунке показана гамма макета, если элемент имеет 350 пикселей или больше пространства по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d4253-156">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Снимок экрана, показывающий пример гамма макета для элемента контрольного списка.](images/content-view/gammaviewmore.png)

-   <span data-ttu-id="d4253-158">На следующем рисунке показана гамма макета, если элемент имеет менее 350 пикселей горизонтального пространства.</span><span class="sxs-lookup"><span data-stu-id="d4253-158">The following illustration shows the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Схема, на которой показан пример гамма макета с менее чем 350 пикселями по горизонтали.](images/content-view/layout6.png)

-   <span data-ttu-id="d4253-160">Пример гаммы макета, когда элемент имеет менее 350 пикселей горизонтального пространства.</span><span class="sxs-lookup"><span data-stu-id="d4253-160">Example of the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Пример гамма-макета](images/content-view/gammaviewless.png)

<span data-ttu-id="d4253-162">**Разностный макет**</span><span class="sxs-lookup"><span data-stu-id="d4253-162">**Delta Layout**</span></span>

<span data-ttu-id="d4253-163">Шаблон разностного макета оптимизирован для отображения множества более коротких свойств, таких как музыка и изображения.</span><span class="sxs-lookup"><span data-stu-id="d4253-163">The Delta layout pattern is optimized for displaying many shorter properties such as for music and pictures.</span></span> <span data-ttu-id="d4253-164">Он имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="d4253-164">It has the following specifications:</span></span>

-   <span data-ttu-id="d4253-165">Строки: 2</span><span class="sxs-lookup"><span data-stu-id="d4253-165">Rows: 2</span></span>
-   <span data-ttu-id="d4253-166">Свойства: 6</span><span class="sxs-lookup"><span data-stu-id="d4253-166">Properties: 6</span></span>
-   <span data-ttu-id="d4253-167">Разностный макет, если элемент имеет 700 пикселей или больше пространства по горизонтали, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d4253-167">Delta layout when the item has 700 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Схема, на которой показан пример разностной структуры.](images/content-view/layout7.png)

-   <span data-ttu-id="d4253-169">Пример разностного макета, когда элемент имеет 700 пикселей или больше пространства по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d4253-169">Example of the delta layout when the item has 700 pixels or more of horizontal space.</span></span>

    ![Снимок экрана, на котором показан пример разностной структуры для музыкального файла.](images/content-view/deltalayoutmore.png)

-   <span data-ttu-id="d4253-171">Разностный макет, если элемент находится в диапазоне от 350 до 700 пикселей по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d4253-171">Delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![Схема, на которой показан пример разностного макета с интервалом от 350 до 700 пикселей по горизонтали.](images/content-view/layout8.png)

-   <span data-ttu-id="d4253-173">Пример разностного макета, когда у элемента есть от 350 до 700 пикселей горизонтального пространства.</span><span class="sxs-lookup"><span data-stu-id="d4253-173">Example of the delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![Пример разностного макета](images/content-view/deltaviewbetween.png)

-   <span data-ttu-id="d4253-175">Разностный макет, если элемент имеет менее 350 пикселей горизонтального пространства.</span><span class="sxs-lookup"><span data-stu-id="d4253-175">Delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Пример макета](images/content-view/layout9.png)

-   <span data-ttu-id="d4253-177">Пример разностного макета, когда элемент имеет менее 350 пикселей горизонтального пространства.</span><span class="sxs-lookup"><span data-stu-id="d4253-177">Example of the delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Снимок экрана, на котором показан пример разностного файла, размер которого меньше 350 пикселей по горизонтали.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="d4253-179">Шаг 3. Регистрация пользовательских свойств и макета для типа файлов</span><span class="sxs-lookup"><span data-stu-id="d4253-179">Step 3: Registering Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="d4253-180">После знакомства с режимом результатов поиска, режимом просмотра и шаблонами макета можно зарегистрировать пользовательский список свойств для типа файлов.</span><span class="sxs-lookup"><span data-stu-id="d4253-180">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="d4253-181">**Для регистрации пользовательского списка свойств и шаблона макета для типа файла.**</span><span class="sxs-lookup"><span data-stu-id="d4253-181">**To register a custom property list and layout pattern for your file type.**</span></span>

1.  <span data-ttu-id="d4253-182">Выберите один из четырех шаблонов макета: альфа, бета, гамма или Дельта.</span><span class="sxs-lookup"><span data-stu-id="d4253-182">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>
2.  <span data-ttu-id="d4253-183">Рассмотрим следующие правила форматирования, которые применяются одинаково ко всем четырем шаблонам макета:</span><span class="sxs-lookup"><span data-stu-id="d4253-183">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>
    -   <span data-ttu-id="d4253-184">Свойство 1 всегда отображается в более крупном размере шрифта.</span><span class="sxs-lookup"><span data-stu-id="d4253-184">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="d4253-185">Крупный размер шрифта, обычно используемый для имени элемента, но также может использоваться для свойства привязки или другого элемента.</span><span class="sxs-lookup"><span data-stu-id="d4253-185">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
    -   <span data-ttu-id="d4253-186">Свойство 4 предназначено для фрагментов в шаблонах макета Alpha, бета-версии и гаммы.</span><span class="sxs-lookup"><span data-stu-id="d4253-186">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="d4253-187">Это свойство выделяет больше пространства в этих шаблонах и отображается серым цветом шрифта, а не черным, как и другие свойства, чтобы помочь ему выделить.</span><span class="sxs-lookup"><span data-stu-id="d4253-187">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
    -   <span data-ttu-id="d4253-188">Приведенные ниже размеры пикселов находятся в относительных пикселях, а размер включает значок или эскиз слева от свойств и расстояние между значком/эскизом и прямоугольником выделения.</span><span class="sxs-lookup"><span data-stu-id="d4253-188">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
    -   <span data-ttu-id="d4253-189">Большинство свойств имеют минимальный отображаемый размер.</span><span class="sxs-lookup"><span data-stu-id="d4253-189">Most properties have a minimum display size.</span></span> <span data-ttu-id="d4253-190">Поэтому они не будут отображаться, если для них недостаточно места в определенном размере представления.</span><span class="sxs-lookup"><span data-stu-id="d4253-190">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="d4253-191">Минимальный размер обычно составляет 100 пикселей в ширину.</span><span class="sxs-lookup"><span data-stu-id="d4253-191">The minimum size is usually 100 pixels wide.</span></span>
    -   <span data-ttu-id="d4253-192">Каждый шаблон макета определяет количество строк и число свойств в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="d4253-192">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>
3.  <span data-ttu-id="d4253-193">Определите, какие свойства должны отображаться в макете, и какое свойство должно отображаться в каждом расположении.</span><span class="sxs-lookup"><span data-stu-id="d4253-193">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="d4253-194">При принятии решения о том, какое свойство должно отображаться в каждой из позиций макета, учитывайте стандартную длину свойства, его важность для пользователя и необходимость удаления, если размер окна слишком мал для размещения всех свойств.</span><span class="sxs-lookup"><span data-stu-id="d4253-194">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>
4.  <span data-ttu-id="d4253-195">Зарегистрируйте шаблон макета и список свойств для типа файла или элемента, добавив следующие ключи в раздел реестра ProgID для типа файла или элемента (в этом примере — для типа файла. XYZ).</span><span class="sxs-lookup"><span data-stu-id="d4253-195">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  <span data-ttu-id="d4253-196">Обратите внимание на следующие рекомендации по форматированию для регистрации свойств:</span><span class="sxs-lookup"><span data-stu-id="d4253-196">Observe the following formatting guidelines for registering properties:</span></span>

    -   <span data-ttu-id="d4253-197">Каждая регистрация начинается с `prop:`</span><span class="sxs-lookup"><span data-stu-id="d4253-197">Each registration starts with `prop:`</span></span>
    -   <span data-ttu-id="d4253-198">Для каждого свойства требуется полное имя свойства.</span><span class="sxs-lookup"><span data-stu-id="d4253-198">Each property requires the full property name.</span></span>
    -   <span data-ttu-id="d4253-199">Свойства разделяются точкой с запятой без пробела.</span><span class="sxs-lookup"><span data-stu-id="d4253-199">Properties are separated by a semicolon with no space.</span></span>
    -   <span data-ttu-id="d4253-200">Свойства отображаются в порядке, определенном выбранным шаблоном макета.</span><span class="sxs-lookup"><span data-stu-id="d4253-200">Properties are displayed in the order defined by the selected layout pattern.</span></span>
    -   <span data-ttu-id="d4253-201">`~` Указывает, что не следует отображать метку свойства.</span><span class="sxs-lookup"><span data-stu-id="d4253-201">`~` indicates that the property label should not be displayed.</span></span>
    -   <span data-ttu-id="d4253-202">`~System.LayoutPattern.PlaceHolder` следует использовать, если вы хотите оставить пустое свойство, указанное в шаблоне макета.</span><span class="sxs-lookup"><span data-stu-id="d4253-202">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

    <span data-ttu-id="d4253-203">В следующем примере раздела реестра показаны эти рекомендации по форматированию.</span><span class="sxs-lookup"><span data-stu-id="d4253-203">The following sample registry key illustrates these formatting guidelines.</span></span>

    ```
    HKEY_CLASSES_ROOT\
       Kind.Document
          (ContentViewModeForBrowse) = <PropertyList>
    ```

    <span data-ttu-id="d4253-204">Возможные значения для (Контентвиевмодефорбровсе) включают следующее: Prop: ~ System. Итемнамедисплай; System. Author; System. Лайаутпаттерн. заполнителей; System. keywords; System. DateModified; ~ System. size</span><span class="sxs-lookup"><span data-stu-id="d4253-204">Possible values for (ContentViewModeForBrowse) include the following: prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified; ~System.Size</span></span>

## <a name="remarks"></a><span data-ttu-id="d4253-205">Примечания</span><span class="sxs-lookup"><span data-stu-id="d4253-205">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4253-206">См. также</span><span class="sxs-lookup"><span data-stu-id="d4253-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4253-207">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="d4253-207">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="d4253-208">Имена видов</span><span class="sxs-lookup"><span data-stu-id="d4253-208">Kind Names</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="d4253-209">System. Проплист. Контентвиевмодефорбровсе</span><span class="sxs-lookup"><span data-stu-id="d4253-209">System.PropList.ContentViewModeForBrowse</span></span>](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[<span data-ttu-id="d4253-210">System. Проплист. Контентвиевмодефорсеарч</span><span class="sxs-lookup"><span data-stu-id="d4253-210">System.PropList.ContentViewModeForSearch</span></span>](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
