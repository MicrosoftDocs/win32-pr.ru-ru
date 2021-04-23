---
title: Поля поиска
description: С помощью поля поиска пользователи могут быстро находить определенные объекты или текст в большом наборе данных путем фильтрации или выделения совпадений.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9d1fca8fdb96b17098cee79fd5b62ecd7ab7531
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "103999838"
---
# <a name="search-boxes"></a><span data-ttu-id="15656-103">Поля поиска</span><span class="sxs-lookup"><span data-stu-id="15656-103">Search Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="15656-104">Это руководство по проектированию было создано для Windows 7 и не Обновлено для более новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="15656-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="15656-105">Многие рекомендации по-прежнему применяются в принципе, но презентация и примеры не соответствуют нашим [текущим руководствам по проектированию](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="15656-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="15656-106">С помощью поля поиска пользователи могут быстро находить определенные объекты или текст в большом наборе данных путем фильтрации или выделения совпадений.</span><span class="sxs-lookup"><span data-stu-id="15656-106">With a Search box, users can quickly locate specific objects or text within a large set of data by filtering or highlighting matches.</span></span> <span data-ttu-id="15656-107">Нет стандартного элемента управления поиском, но следует стремиться к тому, чтобы функции поиска программы соответствовали возможностям Windows.</span><span class="sxs-lookup"><span data-stu-id="15656-107">There is no standard search control, but you should strive to make your program's search features consistent with those of Windows.</span></span>

<span data-ttu-id="15656-108">Существует два типа поиска:</span><span class="sxs-lookup"><span data-stu-id="15656-108">There are two types of searches:</span></span>

-   <span data-ttu-id="15656-109">**Мгновенный поиск**, где результаты отображаются сразу же при вводе пользователем.</span><span class="sxs-lookup"><span data-stu-id="15656-109">**Instant search**, where the results are displayed immediately as the user types.</span></span> <span data-ttu-id="15656-110">Кнопка не должна быть нажата, поэтому символ поиска лупы отображается как рисунок, а не как кнопка.</span><span class="sxs-lookup"><span data-stu-id="15656-110">No button needs to be clicked, so the magnifying glass search symbol is shown as a graphic, not a button.</span></span>

    ![Снимок экрана, на котором отображается поле мгновенного поиска с выноской "prompt", указывающей на поле поиска, и выноской "Поиск символа", указывающей на рисунок с увеличительным стеклом.](images/ctrl-search-boxes-image1.png)

    <span data-ttu-id="15656-112">Типичное поле поиска, использующее мгновенный поиск.</span><span class="sxs-lookup"><span data-stu-id="15656-112">A typical Search box using Instant search.</span></span> <span data-ttu-id="15656-113">Поиск автоматически выполняется при каждом нажатии клавиши.</span><span class="sxs-lookup"><span data-stu-id="15656-113">Search is automatically executed on every keystroke.</span></span>

-   <span data-ttu-id="15656-114">**Обычный поиск**, при котором выполняется поиск, когда пользователь нажимает кнопку "Поиск".</span><span class="sxs-lookup"><span data-stu-id="15656-114">**Regular search**, where a search is performed when the user clicks the search button.</span></span> <span data-ttu-id="15656-115">Символ поиска лупы отображается на кнопке.</span><span class="sxs-lookup"><span data-stu-id="15656-115">The magnifying glass search symbol is shown on a button.</span></span>

    ![<span data-ttu-id="15656-116">снимок экрана обычного поля поиска</span><span class="sxs-lookup"><span data-stu-id="15656-116">screen shot of a regular search box</span></span> ](images/ctrl-search-boxes-image2.png)

    <span data-ttu-id="15656-117">Типичное поле поиска, использующее обычный поиск.</span><span class="sxs-lookup"><span data-stu-id="15656-117">A typical Search box using regular search.</span></span> <span data-ttu-id="15656-118">Пользователи нажимайте кнопку для выполнения поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-118">Users click a button to perform the search.</span></span>

    <span data-ttu-id="15656-119">Для пользователей можно указать один или оба варианта поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-119">You can provide either or both kinds of search options for your users.</span></span>

## <a name="is-this-the-right-control"></a><span data-ttu-id="15656-120">Выбор правильного элемента управления</span><span class="sxs-lookup"><span data-stu-id="15656-120">Is this the right control?</span></span>

<span data-ttu-id="15656-121">Чтобы определиться, ответьте на вопросы:</span><span class="sxs-lookup"><span data-stu-id="15656-121">To decide, consider these questions:</span></span>

-   <span data-ttu-id="15656-122">**Трудно найти определенные объекты?**</span><span class="sxs-lookup"><span data-stu-id="15656-122">**Are specific objects difficult to find?**</span></span> <span data-ttu-id="15656-123">Это может произойти в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="15656-123">This can happen when:</span></span>
    -   <span data-ttu-id="15656-124">Существует много объектов.</span><span class="sxs-lookup"><span data-stu-id="15656-124">There are many objects.</span></span>
    -   <span data-ttu-id="15656-125">Объекты не находятся в одном месте.</span><span class="sxs-lookup"><span data-stu-id="15656-125">The objects aren't located in a single location.</span></span> <span data-ttu-id="15656-126">Поиск особенно удобен для поиска объектов в деревьях.</span><span class="sxs-lookup"><span data-stu-id="15656-126">Search is especially useful for finding objects in trees.</span></span>
    -   <span data-ttu-id="15656-127">Поисковые данные трудно найти (например, метаданные).</span><span class="sxs-lookup"><span data-stu-id="15656-127">The search data is difficult to find (for example, metadata).</span></span>
-   <span data-ttu-id="15656-128">**Нужно ли пользователям искать конкретный текст в документах?**</span><span class="sxs-lookup"><span data-stu-id="15656-128">**Do users need to find specific text within documents?**</span></span>
-   <span data-ttu-id="15656-129">**Будет ли функция возвращать релевантные результаты поиска в течение пяти секунд?**</span><span class="sxs-lookup"><span data-stu-id="15656-129">**Does your feature return relevant search results within five seconds?**</span></span> <span data-ttu-id="15656-130">В противном случае можно предоставить функцию поиска, но использовать альтернативную конструкцию, которая предоставляет видимые отзывы для выполнения длительных поисков, таких как диалоговое окно поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-130">If not, you can provide a search feature, but use an alternative design that gives visible feedback to accommodate long-running searches, such as a search dialog box.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="15656-131">Принципы проектирования</span><span class="sxs-lookup"><span data-stu-id="15656-131">Design concepts</span></span>

<span data-ttu-id="15656-132">Поиск является важнейшим первым шагом во многих сценариях: пользователи должны найти объекты, прежде чем они смогут их использовать.</span><span class="sxs-lookup"><span data-stu-id="15656-132">Searching is a crucial first step in many scenarios: Users must find objects before they can use them.</span></span> <span data-ttu-id="15656-133">Пользователи сохраняют больше и больше объектов на всех более крупных жестких дисках, но просмотр объектов не масштабируется хорошо.</span><span class="sxs-lookup"><span data-stu-id="15656-133">Users are saving more and more objects on increasingly larger hard disks, but browsing for objects doesn't scale well.</span></span> <span data-ttu-id="15656-134">Поиск должен быть простой, стабильной и надежной частью взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="15656-134">Search must be a simple, consistent, reliable part of the user experience.</span></span>

<span data-ttu-id="15656-135">Поля поиска в Windows:</span><span class="sxs-lookup"><span data-stu-id="15656-135">Search boxes in Windows:</span></span>

-   <span data-ttu-id="15656-136">Являются частью всех окон проводника, поэтому их легко найти и распознать.</span><span class="sxs-lookup"><span data-stu-id="15656-136">Are part of all Explorer windows, so they are easy to find and recognize.</span></span>
-   <span data-ttu-id="15656-137">Имеют единообразный внешний вид и поведение.</span><span class="sxs-lookup"><span data-stu-id="15656-137">Have consistent appearance and behavior.</span></span>
-   <span data-ttu-id="15656-138">Работают эффективно и быстро, обеспечивая мгновенный поиск в режиме мгновенного поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-138">Are efficient and fast, giving instant results in Instant search mode.</span></span>

<span data-ttu-id="15656-139">Поле поиска используется в Windows в следующих местах:</span><span class="sxs-lookup"><span data-stu-id="15656-139">A Search box is used in Windows in these places:</span></span>

-   <span data-ttu-id="15656-140">Обозреватели</span><span class="sxs-lookup"><span data-stu-id="15656-140">Explorers</span></span>
-   <span data-ttu-id="15656-141">Взаимодействие (проигрыватель Microsoft Windows Media, фотоальбом Windows, Windows Internet Explorer)</span><span class="sxs-lookup"><span data-stu-id="15656-141">Experiences (Microsoft Windows Media Player, Windows Photo Gallery, Windows Internet Explorer)</span></span>
-   <span data-ttu-id="15656-142">Меню "Пуск" (для поиска программ и последних файлов)</span><span class="sxs-lookup"><span data-stu-id="15656-142">Start menu (to find programs and recent files)</span></span>
-   <span data-ttu-id="15656-143">Домашняя страница панели управления (для поиска элементов и задач панели управления)</span><span class="sxs-lookup"><span data-stu-id="15656-143">Control Panel home page (to find control panel items and tasks)</span></span>
-   <span data-ttu-id="15656-144">Справка (для поиска соответствующих разделов справки)</span><span class="sxs-lookup"><span data-stu-id="15656-144">Help (to find relevant Help topics)</span></span>

### <a name="look-and-feel"></a><span data-ttu-id="15656-145">Внешний вид</span><span class="sxs-lookup"><span data-stu-id="15656-145">Look and feel</span></span>

<span data-ttu-id="15656-146">Возможность поиска в Windows значительно улучшена за счет поддержки мгновенного поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-146">The feel of Search in Windows is significantly enhanced by supporting Instant search.</span></span> <span data-ttu-id="15656-147">Мгновенные результаты делают Windows более мощными и прямыми.</span><span class="sxs-lookup"><span data-stu-id="15656-147">Having instant results makes Windows feel more powerful and direct.</span></span>

<span data-ttu-id="15656-148">В проводнике Windows и окнах приложений Поиск находится в правом верхнем углу, если это дополнительная точка входа.</span><span class="sxs-lookup"><span data-stu-id="15656-148">In Windows Explorer and application windows, Search is located in the upper-right corner if it is a supplemental entry point.</span></span> <span data-ttu-id="15656-149">В этом случае пользователи ищут механизм поиска, если не нашли то, что они ищут в окне.</span><span class="sxs-lookup"><span data-stu-id="15656-149">In this case, users look for a search mechanism when they don't find what they are looking for in the window.</span></span> <span data-ttu-id="15656-150">Однако, если поиск является основной точкой входа, он выравнивается по центру в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="15656-150">However, if Search is the primary entry point, it is centered at the top of the window.</span></span>

<span data-ttu-id="15656-151">Кнопка поиска визуально связана с полем поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-151">The Search button is visually connected to a Search box.</span></span> <span data-ttu-id="15656-152">Чтобы максимально ограничить пространство, в поле поиска используется необязательный [запрос](ctrl-text-boxes.md) , а не метка.</span><span class="sxs-lookup"><span data-stu-id="15656-152">To minimize space, an optional [prompt](ctrl-text-boxes.md) is used inside a Search box instead of a label.</span></span> <span data-ttu-id="15656-153">Запрос может быть инструкцией (например, введите текст для поиска) или указать область поиска (например, поиск изображений).</span><span class="sxs-lookup"><span data-stu-id="15656-153">The prompt may be an instruction (for example, Type to search) or indicate the scope of the search (for example, Search for pictures).</span></span>

![<span data-ttu-id="15656-154">снимок экрана поля мгновенного поиска</span><span class="sxs-lookup"><span data-stu-id="15656-154">screen shot of an instant search box</span></span> ](images/ctrl-search-boxes-image3.png)

<span data-ttu-id="15656-155">Без меток и отдельных кнопок мгновенный поиск в Windows имеет упрощенный вид.</span><span class="sxs-lookup"><span data-stu-id="15656-155">Without labels and separate buttons, Instant search in Windows has a lightweight look.</span></span>

<span data-ttu-id="15656-156">При успешном выполнении поиска создается виртуальная страница результатов поиска, которая добавляется в стек назад и адресную строку.</span><span class="sxs-lookup"><span data-stu-id="15656-156">Performing a successful search creates a virtual page of the search results and adds it to the Back stack and Address bar.</span></span> <span data-ttu-id="15656-157">У пользователей есть несколько способов восстановить исходную страницу и очистить поле поиска, в том числе нажать кнопку назад, щелкнуть исходную страницу в адресной строке, нажать клавишу ESC или очистить поле поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-157">Users have several ways to restore the original page and clear a Search box, including clicking Back, clicking the original page in the Address bar, pressing Esc, or clearing the Search box.</span></span>

<span data-ttu-id="15656-158">Пользователи также могут просто очистить поле поиска, не восстанавливая предыдущую страницу результатов.</span><span class="sxs-lookup"><span data-stu-id="15656-158">Users can also simply clear the Search box without restoring a previous page of results.</span></span> <span data-ttu-id="15656-159">В режиме мгновенного поиска Кнопка Clear появляется после начала ввода пользователем. "x" заменяет символ поиска лупы.</span><span class="sxs-lookup"><span data-stu-id="15656-159">In Instant search mode, a clear button appears after the user starts typing; an "x" replaces the magnifying glass search symbol.</span></span> <span data-ttu-id="15656-160">При наведении курсор «x» получает вид кнопки и может быть нажат.</span><span class="sxs-lookup"><span data-stu-id="15656-160">On hover, the "x" gets a button look and can be clicked.</span></span>

![<span data-ttu-id="15656-161">снимок экрана поля поиска со значком "x"</span><span class="sxs-lookup"><span data-stu-id="15656-161">screen shot of a search box with an 'x' icon</span></span> ](images/ctrl-search-boxes-image4.png)

<span data-ttu-id="15656-162">Пользователь может очистить поле поиска, щелкнув "x" справа от элемента управления.</span><span class="sxs-lookup"><span data-stu-id="15656-162">The user can clear the Search box by clicking "x" at the right end of the control.</span></span>

<span data-ttu-id="15656-163">В обычном режиме поиска Кнопка Clear необязательна.</span><span class="sxs-lookup"><span data-stu-id="15656-163">In regular search mode, the clear button is optional.</span></span> <span data-ttu-id="15656-164">Пользователи могут оказаться полезными, например, если поиск занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="15656-164">Users may find it useful, for example, if a search is taking a long time to complete.</span></span> <span data-ttu-id="15656-165">Чтобы прерывать выполнение поиска, пользователи могут нажать кнопку «x».</span><span class="sxs-lookup"><span data-stu-id="15656-165">Users can click the "x" to stop the search in progress.</span></span> <span data-ttu-id="15656-166">Если поиск уже завершен, пользователи могут нажать кнопку «x», чтобы очистить поле поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-166">If a search has already completed, users can click the "x" to clear the Search box.</span></span>

## <a name="guidelines"></a><span data-ttu-id="15656-167">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="15656-167">Guidelines</span></span>

### <a name="location"></a><span data-ttu-id="15656-168">Расположение</span><span class="sxs-lookup"><span data-stu-id="15656-168">Location</span></span>

-   <span data-ttu-id="15656-169">Для окон приложений найдите Поиск в правом верхнем углу.</span><span class="sxs-lookup"><span data-stu-id="15656-169">For application windows, locate Search in the upper-right corner.</span></span>
-   <span data-ttu-id="15656-170">Для всплывающих окон Поиск в любом удобном месте.</span><span class="sxs-lookup"><span data-stu-id="15656-170">For popup windows, locate Search wherever is most sensible and convenient.</span></span>
-   <span data-ttu-id="15656-171">**Исключение:** Если поиск, как правило, выполняется первыми в окне (основной точке входа), по центру в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="15656-171">**Exception:** If Search is usually the first thing users do in a window (the primary entry point), center it at the top of the window.</span></span>

### <a name="look"></a><span data-ttu-id="15656-172">Взглян</span><span class="sxs-lookup"><span data-stu-id="15656-172">Look</span></span>

-   <span data-ttu-id="15656-173">Используйте стандартную графику кнопки поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-173">Use the standard search button graphics.</span></span> <span data-ttu-id="15656-174">Существует три версии:</span><span class="sxs-lookup"><span data-stu-id="15656-174">There are three versions:</span></span>
    -   <span data-ttu-id="15656-175">**Только символ поиска лупы (кнопка не наводится на наведение).**</span><span class="sxs-lookup"><span data-stu-id="15656-175">**Magnifying glass search symbol only (no button on hover).**</span></span> <span data-ttu-id="15656-176">Используется для мгновенного поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-176">Use for Instant search.</span></span>
    -   <span data-ttu-id="15656-177">**Символ поиска лупы с кнопкой.**</span><span class="sxs-lookup"><span data-stu-id="15656-177">**Magnifying glass search symbol with button.**</span></span> <span data-ttu-id="15656-178">Используйте, когда необходимо щелкнуть кнопку, чтобы начать поиск.</span><span class="sxs-lookup"><span data-stu-id="15656-178">Use when button needs to be clicked to start the search.</span></span>
    -   <span data-ttu-id="15656-179">**Символ поиска лупы с кнопкой и стрелкой раскрывающегося списка.**</span><span class="sxs-lookup"><span data-stu-id="15656-179">**Magnifying glass search symbol with button and drop-down arrow.**</span></span> <span data-ttu-id="15656-180">Добавьте стрелку раскрывающегося списка, если пользователи могут изменить область или если доступны другие параметры.</span><span class="sxs-lookup"><span data-stu-id="15656-180">Add a drop-down arrow when users can change the scope or when other settings are available.</span></span>
        -   <span data-ttu-id="15656-181">Для мгновенного поиска используйте только стрелку раскрывающегося списка и покажите кнопку при наведении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="15656-181">For Instant search, use a drop-down arrow only, and show a button on hover.</span></span>
        -   <span data-ttu-id="15656-182">Для обычного поиска покажите стрелку раскрывающегося списка на кнопке.</span><span class="sxs-lookup"><span data-stu-id="15656-182">For regular search, show the drop-down arrow on a button.</span></span>

![<span data-ttu-id="15656-183">Рисунок полей с мгновенным поиском в разных состояниях</span><span class="sxs-lookup"><span data-stu-id="15656-183">figure of instant search boxes in different states</span></span> ](images/ctrl-search-boxes-image5.png)

<span data-ttu-id="15656-184">Визуальные спецификации для мгновенного поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-184">Visual specifications for Instant search.</span></span>

![<span data-ttu-id="15656-185">Рисунок обычных полей поиска в разных состояниях</span><span class="sxs-lookup"><span data-stu-id="15656-185">figure of regular search boxes in different states</span></span> ](images/ctrl-search-boxes-image6.png)

<span data-ttu-id="15656-186">Визуальные спецификации для обычного поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-186">Visual specifications for regular search.</span></span>

-   <span data-ttu-id="15656-187">Не используйте метку. Вместо этого используйте необязательный запрос.</span><span class="sxs-lookup"><span data-stu-id="15656-187">Don't use a label; use an optional prompt instead.</span></span> <span data-ttu-id="15656-188">Если пользователи считают, что поиск является универсальным поиском файлов, используйте запрос для предоставления области.</span><span class="sxs-lookup"><span data-stu-id="15656-188">If users tend to assume that the search is a generic file search, use the prompt to give the scope.</span></span> <span data-ttu-id="15656-189">В противном случае используйте тип для поиска или аналогичную краткую фразу.</span><span class="sxs-lookup"><span data-stu-id="15656-189">Otherwise, use Type to search or a similar, concise phrase.</span></span>

    ![<span data-ttu-id="15656-190">снимок экрана с приглашением "Ввод в Поиск"</span><span class="sxs-lookup"><span data-stu-id="15656-190">screen shot of 'type to search' prompt</span></span> ](images/ctrl-search-boxes-image7.png)

    ![<span data-ttu-id="15656-191">снимок экрана с приглашением "Поиск всех мини-приложений"</span><span class="sxs-lookup"><span data-stu-id="15656-191">screen shot of 'search all gadgets' prompt</span></span> ](images/ctrl-search-boxes-image8.png)

    <span data-ttu-id="15656-192">В этих примерах краткие текстовые запросы помогают пользователям работать с поиском.</span><span class="sxs-lookup"><span data-stu-id="15656-192">In these examples, brief textual prompts help users work with Search.</span></span>

### <a name="interaction"></a><span data-ttu-id="15656-193">Взаимодействие</span><span class="sxs-lookup"><span data-stu-id="15656-193">Interaction</span></span>

-   <span data-ttu-id="15656-194">**При фокусе ввода автоматически выбирайте любой ранее введенный текст.**</span><span class="sxs-lookup"><span data-stu-id="15656-194">**On input focus, automatically select any previously entered text.**</span></span> <span data-ttu-id="15656-195">Это позволит пользователям вводить новый поиск, вводя или изменяя предыдущий поиск, размещая курсор с помощью клавиш со стрелками.</span><span class="sxs-lookup"><span data-stu-id="15656-195">Doing so allows users to enter a new search by typing, or to modify the previous search by positioning the caret using the arrow keys.</span></span>

    ![<span data-ttu-id="15656-196">снимок экрана поля поиска с выделенным текстом</span><span class="sxs-lookup"><span data-stu-id="15656-196">screen shot of search box with highlighted text</span></span> ](images/ctrl-search-boxes-image9.png)

    <span data-ttu-id="15656-197">В этом примере в фокусе ввода выбирается ранее введенный текст.</span><span class="sxs-lookup"><span data-stu-id="15656-197">In this example, previously entered text is selected on input focus.</span></span>

-   <span data-ttu-id="15656-198">**Назначьте сочетание клавиш для поля поиска Ctrl + E.**</span><span class="sxs-lookup"><span data-stu-id="15656-198">**Assign the keyboard shortcut for the Search box to be Ctrl+E.**</span></span>

### <a name="functionality"></a><span data-ttu-id="15656-199">Функциональность</span><span class="sxs-lookup"><span data-stu-id="15656-199">Functionality</span></span>

-   <span data-ttu-id="15656-200">**Поддержка мгновенного поиска, когда это возможно.**</span><span class="sxs-lookup"><span data-stu-id="15656-200">**Support Instant search whenever possible.**</span></span> <span data-ttu-id="15656-201">Предоставьте как обычный, так и мгновенный поиск в ситуациях, когда регулярный поиск стоит за дополнительным временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="15656-201">Provide both regular and Instant searches if there are scenarios where regular searching is worth the extra wait time.</span></span>
-   <span data-ttu-id="15656-202">Обычные поисковые запросы должны возвращать соответствующие результаты в течение пяти секунд, а мгновенный поиск должен возвращать результаты в течение двух секунд.</span><span class="sxs-lookup"><span data-stu-id="15656-202">Regular searches must return relevant results within five seconds and Instant search must return results within two seconds.</span></span> <span data-ttu-id="15656-203">После этого Поиск может продолжать заполнять менее релевантные результаты с течением времени, пока программа отвечает и пользователи могут выполнять другие задачи.</span><span class="sxs-lookup"><span data-stu-id="15656-203">After this point, Search may continue to fill in less relevant results over time as long as the program is responsive and users can perform other tasks.</span></span> <span data-ttu-id="15656-204">Чтобы обеспечить эту скорость реагирования, может потребоваться индексирование данных поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-204">You may have to index your search data to ensure this responsiveness.</span></span>
-   <span data-ttu-id="15656-205">При предоставлении режима обычного и мгновенного поиска результаты мгновенного поиска должны быть подмножеством обычных результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-205">If you provide both regular and Instant search modes, the Instant search results must be a subset of the regular search results.</span></span>
-   <span data-ttu-id="15656-206">Все поисковые запросы основаны на префиксе (без поиска подстрок или суффиксов).</span><span class="sxs-lookup"><span data-stu-id="15656-206">All searching is prefix-based (no substring or suffix searching).</span></span> <span data-ttu-id="15656-207">Использование конечных подстановочных знаков является необязательным и не влияет на результаты.</span><span class="sxs-lookup"><span data-stu-id="15656-207">The use of trailing wildcard characters is optional and doesn't affect the results.</span></span> <span data-ttu-id="15656-208">Если введено несколько слов, используйте или выполните поиск.</span><span class="sxs-lookup"><span data-stu-id="15656-208">If multiple words are entered, use OR searching.</span></span>
-   <span data-ttu-id="15656-209">Успешный поиск добавляет виртуальную страницу с результатами поиска в стек назад и адресную строку.</span><span class="sxs-lookup"><span data-stu-id="15656-209">A successful search adds a virtual page with the search results to the Back stack and Address bar.</span></span> <span data-ttu-id="15656-210">Несколько поисков приводят к одной виртуальной странице, поэтому при нажатии кнопки назад всегда возвращается исходная страница.</span><span class="sxs-lookup"><span data-stu-id="15656-210">Multiple searches result in a single virtual page, so clicking Back always returns the original page.</span></span>
-   <span data-ttu-id="15656-211">Если это необходимо для масштабирования, ранжирование результатов поиска по релевантности.</span><span class="sxs-lookup"><span data-stu-id="15656-211">If necessary for scale, rank the search results by relevance.</span></span>
-   <span data-ttu-id="15656-212">Пустой Поиск Возвращает исходную страницу.</span><span class="sxs-lookup"><span data-stu-id="15656-212">A blank search returns the original page.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="15656-213">Рекомендуемое изменение размера и расстояния</span><span class="sxs-lookup"><span data-stu-id="15656-213">Recommended sizing and spacing</span></span>

![<span data-ttu-id="15656-214">Рисунок поля для быстрого поиска с изменением размера и расстояния</span><span class="sxs-lookup"><span data-stu-id="15656-214">figure of instant search box sizing and spacing</span></span> ](images/ctrl-search-boxes-image10.png)

<span data-ttu-id="15656-215">Рекомендуемое изменение размера и расстояния для мгновенного поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-215">Recommended sizing and spacing for Instant search.</span></span>

![<span data-ttu-id="15656-216">Рисунок обычного размера поля поиска и интервала</span><span class="sxs-lookup"><span data-stu-id="15656-216">figure of regular search box sizing and spacing</span></span> ](images/ctrl-search-boxes-image11.png)

<span data-ttu-id="15656-217">Рекомендуемый размер и интервал для обычного поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-217">Recommended sizing and spacing for regular search.</span></span>

## <a name="text"></a><span data-ttu-id="15656-218">Текст</span><span class="sxs-lookup"><span data-stu-id="15656-218">Text</span></span>

-   <span data-ttu-id="15656-219">Для слова запроса в поле поиска либо сделайте его инструкцией (например, введите для поиска), либо укажите область поиска (например, поиск изображений).</span><span class="sxs-lookup"><span data-stu-id="15656-219">For the wording of the prompt in the Search box, either make it an instruction (for example, Type to search) or indicate the scope of the search (for example, Search for pictures).</span></span>
-   <span data-ttu-id="15656-220">Текст подсказки должен быть кратким.</span><span class="sxs-lookup"><span data-stu-id="15656-220">Prompt text should be brief.</span></span> <span data-ttu-id="15656-221">Должно быть достаточно одного слова или короткой фразы.</span><span class="sxs-lookup"><span data-stu-id="15656-221">A single word or short phrase should suffice.</span></span>
-   <span data-ttu-id="15656-222">Используйте выделение прописных букв, как в предложении.</span><span class="sxs-lookup"><span data-stu-id="15656-222">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="15656-223">Не используйте закрывающие знаки препинания или многоточие.</span><span class="sxs-lookup"><span data-stu-id="15656-223">Don't use ending punctuation or ellipsis.</span></span>

## <a name="documentation"></a><span data-ttu-id="15656-224">Документация</span><span class="sxs-lookup"><span data-stu-id="15656-224">Documentation</span></span>

-   <span data-ttu-id="15656-225">Ссылка на этот элемент управления в качестве поля поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-225">Refer to this control as the Search box.</span></span> <span data-ttu-id="15656-226">Заменять начальную букву первого слова на прописную; не заменяйте начальную букву поля прописной.</span><span class="sxs-lookup"><span data-stu-id="15656-226">Capitalize the initial letter of the first word; don't capitalize the initial letter of box.</span></span>
-   <span data-ttu-id="15656-227">Используйте два типа поиска: Мгновенный поиск и обычный поиск.</span><span class="sxs-lookup"><span data-stu-id="15656-227">Refer to the two types of search as Instant search and regular search.</span></span> <span data-ttu-id="15656-228">Изменяйте начальную букву для быстрого поиска. не используйте прописные буквы для обычного поиска.</span><span class="sxs-lookup"><span data-stu-id="15656-228">Capitalize the initial letter of Instant search; don't capitalize the initial letter of regular search.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15656-229">См. также</span><span class="sxs-lookup"><span data-stu-id="15656-229">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15656-230">Словарь терминов</span><span class="sxs-lookup"><span data-stu-id="15656-230">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 