---
title: Фреймы окна
description: Большинство программ должны использовать стандартные рамки окон. Иммерсивное приложение может иметь полноэкранный режим, который скрывает рамку окна. Рассмотрите возможность использования "стратегического" для упрощения, более простого и более единообразного вида.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104551322"
---
# <a name="window-frames"></a><span data-ttu-id="127df-105">Фреймы окна</span><span class="sxs-lookup"><span data-stu-id="127df-105">Window Frames</span></span>

> [!NOTE]
> <span data-ttu-id="127df-106">Это руководство по проектированию было создано для Windows 7 и не Обновлено для более новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="127df-106">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="127df-107">Многие рекомендации по-прежнему применяются в принципе, но презентация и примеры не соответствуют нашим [текущим руководствам по проектированию](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="127df-107">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="127df-108">Большинство программ должны использовать стандартные рамки окон.</span><span class="sxs-lookup"><span data-stu-id="127df-108">Most programs should use standard window frames.</span></span> <span data-ttu-id="127df-109">Иммерсивное приложение может иметь полноэкранный режим, который скрывает рамку окна.</span><span class="sxs-lookup"><span data-stu-id="127df-109">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="127df-110">Рассмотрите возможность использования "стратегического" для упрощения, более простого и более единообразного вида.</span><span class="sxs-lookup"><span data-stu-id="127df-110">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span>

<span data-ttu-id="127df-111">С помощью рамки окна пользователи могут управлять окном и просматривать заголовок и значок для поиска его содержимого.</span><span class="sxs-lookup"><span data-stu-id="127df-111">With a window frame, users can manipulate a window and view the title and icon to identify its contents.</span></span>

![<span data-ttu-id="127df-112">снимок экрана рамки окна Блокнота</span><span class="sxs-lookup"><span data-stu-id="127df-112">screen shot of window frame around notepad window</span></span> ](images/win-window-frames-image1.png)

<span data-ttu-id="127df-113">Типичная рамка окна.</span><span class="sxs-lookup"><span data-stu-id="127df-113">A typical window frame.</span></span>

<span data-ttu-id="127df-114">**Примечание.** Рекомендации, связанные с [управлением окнами](win-window-mgt.md) и [фирменной символикой](exper-branding.md) , представлены в отдельных статьях.</span><span class="sxs-lookup"><span data-stu-id="127df-114">**Note:** Guidelines related to [window management](win-window-mgt.md) and [branding](exper-branding.md) are presented in separate articles.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="127df-115">Принципы проектирования</span><span class="sxs-lookup"><span data-stu-id="127df-115">Design concepts</span></span>

### <a name="glass-window-frames"></a><span data-ttu-id="127df-116">Стеклянные рамки окна</span><span class="sxs-lookup"><span data-stu-id="127df-116">Glass window frames</span></span>

<span data-ttu-id="127df-117">Рамки стеклянного окна — это новый аспект Microsoft Windows Aesthetic, надежде как привлекательный и облегченный.</span><span class="sxs-lookup"><span data-stu-id="127df-117">The glass window frames are a striking new aspect of the Microsoft Windows aesthetic, aiming to be both attractive and lightweight.</span></span> <span data-ttu-id="127df-118">Эти полупрозрачные кадры придают Windows открытой, менее функциональный вид, помогая пользователям сосредоточиться на содержимом и функциональности, а не на окружающем его интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="127df-118">These translucent frames give windows an open, less intrusive appearance, helping users focus on content and functionality rather than the interface surrounding it.</span></span>

![<span data-ttu-id="127df-119">снимок экрана со стеклянным фреймом вокруг калькулятора</span><span class="sxs-lookup"><span data-stu-id="127df-119">screen shot of glass frame around calculator</span></span> ](images/win-window-frames-image2.png)

<span data-ttu-id="127df-120">Стеклянные рамки окна.</span><span class="sxs-lookup"><span data-stu-id="127df-120">Glass window frames.</span></span>

<span data-ttu-id="127df-121">Вы можете использовать для стратегического стекла в небольших регионах в окне, которое используется для управления рамкой окна.</span><span class="sxs-lookup"><span data-stu-id="127df-121">You can use glass strategically in small regions within a window that touch the window frame.</span></span> <span data-ttu-id="127df-122">Такие регионы выглядят как часть рамки окна, хотя технически они являются частью клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="127df-122">Such regions appear to be part of the window frame, even though technically they are part of the window's client area.</span></span>

![<span data-ttu-id="127df-123">снимок экрана окна с полупрозрачной границей</span><span class="sxs-lookup"><span data-stu-id="127df-123">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)

<span data-ttu-id="127df-124">В этом примере в клиентской области используется стекло, чтобы оно было похоже на часть кадра.</span><span class="sxs-lookup"><span data-stu-id="127df-124">In this example, glass is used in the client area to make it look like part of the frame.</span></span>

### <a name="hidden-frames"></a><span data-ttu-id="127df-125">Скрытые кадры</span><span class="sxs-lookup"><span data-stu-id="127df-125">Hidden frames</span></span>

<span data-ttu-id="127df-126">Иногда лучшим кадром окна не является фрейм.</span><span class="sxs-lookup"><span data-stu-id="127df-126">Sometimes the best window frame is no frame at all.</span></span> <span data-ttu-id="127df-127">Часто это происходит для [основного окна](glossary.md) впечатляющих [полноэкранных](glossary.md) приложений, которые не используются совместно с другими программами, такими как проигрыватели мультимедиа, игры и приложения киоска.</span><span class="sxs-lookup"><span data-stu-id="127df-127">This is often the case for the [primary window](glossary.md) of immersive [full screen](glossary.md) applications that aren't used in conjunction with other programs, such as media players, games, and kiosk applications.</span></span>

<span data-ttu-id="127df-128">Средства просмотра содержимого часто получают возможность отображать содержимое во весь экран.</span><span class="sxs-lookup"><span data-stu-id="127df-128">Content viewers often benefit from having the option to show content full screen.</span></span> <span data-ttu-id="127df-129">К примерам относятся Windows Internet Explorer, фотоальбом Windows Live, Windows Movie Maker HD, Microsoft PowerPoint и Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="127df-129">Examples include Windows Internet Explorer , Windows Live Photo Gallery, Windows Movie Maker HD, Microsoft PowerPoint , and Microsoft Word.</span></span>

![<span data-ttu-id="127df-130">снимок экрана проигрывателя мультимедиа в полноэкранном режиме</span><span class="sxs-lookup"><span data-stu-id="127df-130">screen shot of media player in full-screen view</span></span> ](images/win-window-frames-image4.png)

<span data-ttu-id="127df-131">В этом примере проигрыватель Windows Media может отображать свое содержимое в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="127df-131">In this example, Windows Media Player can display its content full screen.</span></span>

### <a name="custom-frames"></a><span data-ttu-id="127df-132">Пользовательские рамки</span><span class="sxs-lookup"><span data-stu-id="127df-132">Custom frames</span></span>

<span data-ttu-id="127df-133">Большинство приложений Windows должны использовать стандартные рамки окон.</span><span class="sxs-lookup"><span data-stu-id="127df-133">Most Windows applications should use the standard window frames.</span></span> <span data-ttu-id="127df-134">Однако для впечатляющих, полноэкранных, автономных приложений, таких как игры и приложения киоска, может быть целесообразно использовать пользовательские рамки для всех окон, которые не отображаются в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="127df-134">However, for immersive, full screen, stand-alone applications like games and kiosk applications, it may be appropriate to use custom frames for any windows that aren't shown full screen.</span></span> <span data-ttu-id="127df-135">Целью использования пользовательских рамок должно быть предоставление уникального поведения, а не только [фирменной символики](exper-branding.md).</span><span class="sxs-lookup"><span data-stu-id="127df-135">The motivation to use custom frames should be to give the overall experience a unique feel, not just for [branding](exper-branding.md).</span></span>

![<span data-ttu-id="127df-136">Иллюстрация головоломки и кадра с зашифрованными изображениями</span><span class="sxs-lookup"><span data-stu-id="127df-136">illustration of scrambled picture puzzle and frame</span></span> ](images/win-window-frames-image5.png)

<span data-ttu-id="127df-137">Пользовательские фреймы подходят для иммерсивного, полноэкранного режима, автономных приложений, таких как игры.</span><span class="sxs-lookup"><span data-stu-id="127df-137">Custom frames are appropriate for immersive, full screen, stand-alone applications such as games.</span></span>

## <a name="guidelines"></a><span data-ttu-id="127df-138">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="127df-138">Guidelines</span></span>

### <a name="window-frames"></a><span data-ttu-id="127df-139">Фреймы окна</span><span class="sxs-lookup"><span data-stu-id="127df-139">Window frames</span></span>

-   <span data-ttu-id="127df-140">Использовать стандартные рамки окон.</span><span class="sxs-lookup"><span data-stu-id="127df-140">Use standard window frames.</span></span>
    -   <span data-ttu-id="127df-141">**Исключение:** Чтобы обеспечить полноценное Полноэкранное представление, самостоятельные приложения являются уникальными:</span><span class="sxs-lookup"><span data-stu-id="127df-141">**Exception:** To give immersive full screen, stand-alone applications a unique feel:</span></span>
        -   <span data-ttu-id="127df-142">Рассмотрите возможность скрытия рамки окна [основного окна](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="127df-142">Consider hiding the window frame of the [primary window](glossary.md).</span></span>
        -   <span data-ttu-id="127df-143">Рассмотрите возможность использования пользовательских рамок для [дополнительного окна](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="127df-143">Consider using custom frames for [secondary window](glossary.md).</span></span>
        -   <span data-ttu-id="127df-144">Если пользовательская рамка подходит, выберите упрощенную конструкцию и не Нарисуйте слишком много внимания.</span><span class="sxs-lookup"><span data-stu-id="127df-144">If a custom frame is appropriate, choose a design that is lightweight and doesn't draw too much attention to itself.</span></span>

            <span data-ttu-id="127df-145">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="127df-145">**Incorrect:**</span></span>

            ![<span data-ttu-id="127df-146">снимок экрана с отвлекаетем рамки</span><span class="sxs-lookup"><span data-stu-id="127df-146">screen shot of distracting frame</span></span> ](images/win-window-frames-image6.png)

            <span data-ttu-id="127df-147">В этом примере пользовательская рамка имеет слишком много внимания.</span><span class="sxs-lookup"><span data-stu-id="127df-147">In this example, the custom frame draws too much attention to itself.</span></span>
-   <span data-ttu-id="127df-148">Не добавляйте элементы управления в рамку окна.</span><span class="sxs-lookup"><span data-stu-id="127df-148">Don't add controls to a window frame.</span></span> <span data-ttu-id="127df-149">Вместо этого Разместите элементы управления в окне.</span><span class="sxs-lookup"><span data-stu-id="127df-149">Put the controls within the window instead.</span></span>

    <span data-ttu-id="127df-150">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="127df-150">**Incorrect:**</span></span>

    ![<span data-ttu-id="127df-151">снимок экрана элемента управления в рамке окна</span><span class="sxs-lookup"><span data-stu-id="127df-151">screen shot of control in window frame</span></span> ](images/win-window-frames-image7.png)

    <span data-ttu-id="127df-152">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="127df-152">**Correct:**</span></span>

    ![<span data-ttu-id="127df-153">снимок экрана элемента управления в клиентской области</span><span class="sxs-lookup"><span data-stu-id="127df-153">screen shot of control in client area</span></span> ](images/win-window-frames-image8.png)

    <span data-ttu-id="127df-154">В правильном примере элемент управления находится в области клиента, а не в рамке окна.</span><span class="sxs-lookup"><span data-stu-id="127df-154">In the correct example, the control is within the client area instead of the window frame.</span></span>

### <a name="full-screen-mode"></a><span data-ttu-id="127df-155">Полноэкранный режим</span><span class="sxs-lookup"><span data-stu-id="127df-155">Full screen mode</span></span>

-   <span data-ttu-id="127df-156">Для программ с необязательным полноэкранным режимом для включения полноэкранного режима:</span><span class="sxs-lookup"><span data-stu-id="127df-156">For programs that have an optional full screen mode, to enable full screen mode:</span></span>
    -   <span data-ttu-id="127df-157">Отображение модального полноэкранного команды в строке меню или на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="127df-157">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="127df-158">Когда пользователь щелкает команду, команда показывает команду в выбранном состоянии.</span><span class="sxs-lookup"><span data-stu-id="127df-158">When the user clicks the command, show the command in its selected state.</span></span>

        ![<span data-ttu-id="127df-159">снимок экрана окна с пунктом меню "полный экран"</span><span class="sxs-lookup"><span data-stu-id="127df-159">screen shot of window with full screen menu item</span></span> ](images/win-window-frames-image9.png)

        <span data-ttu-id="127df-160">В этом примере показана команда во весь экран вместе со стандартным сочетанием клавиш.</span><span class="sxs-lookup"><span data-stu-id="127df-160">This example shows the full screen command along with its standard shortcut key.</span></span>

-   <span data-ttu-id="127df-161">Используйте клавишу F11 для быстрого вызова в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="127df-161">Use F11 for the full screen shortcut key.</span></span>
-   <span data-ttu-id="127df-162">Если часто используется панель инструментов и полноэкранный режим, то также имеется кнопка на панели инструментов с изображением во весь экран.</span><span class="sxs-lookup"><span data-stu-id="127df-162">If there is a toolbar and full screen mode is commonly used, also have a graphic toolbar button with a Full screen tooltip.</span></span>

    ![<span data-ttu-id="127df-163">снимок экрана с кнопками "во весь экран" и "восстановить"</span><span class="sxs-lookup"><span data-stu-id="127df-163">screen shot of full screen and revert buttons</span></span> ](images/win-window-frames-image10.png)

    <span data-ttu-id="127df-164">Примеры кнопок на панели инструментов в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="127df-164">Examples of full screen toolbar buttons.</span></span>

-   <span data-ttu-id="127df-165">Возврат из полноэкранного режима:</span><span class="sxs-lookup"><span data-stu-id="127df-165">To revert back from full screen mode:</span></span>
    -   <span data-ttu-id="127df-166">Отображение модального полноэкранного команды в строке меню или на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="127df-166">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="127df-167">Когда пользователь щелкнет команду, команда отобразится в состоянии очистки.</span><span class="sxs-lookup"><span data-stu-id="127df-167">When the user clicks the command, show the command in its cleared state.</span></span>
    -   <span data-ttu-id="127df-168">Используйте клавишу F11 для быстрого вызова в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="127df-168">Use F11 for the full screen shortcut key.</span></span> <span data-ttu-id="127df-169">Если это еще не было назначено, для этой цели также можно использовать клавишу ESC.</span><span class="sxs-lookup"><span data-stu-id="127df-169">If not already assigned, Esc can also be used for this purpose.</span></span>

### <a name="glass"></a><span data-ttu-id="127df-170">Стекло</span><span class="sxs-lookup"><span data-stu-id="127df-170">Glass</span></span>

<span data-ttu-id="127df-171">Стандартные рамки окон автоматически используют стекло в Windows, но можно также использовать стекло в регионах, которые касаются рамки окна.</span><span class="sxs-lookup"><span data-stu-id="127df-171">Standard window frames use glass automatically in Windows, but you can also use glass in regions that touch the window frame.</span></span>

-   <span data-ttu-id="127df-172">**Рассмотрите возможность использования «стратегичеического» стекла в небольших регионах, чтобы кадрировать окно без текста.**</span><span class="sxs-lookup"><span data-stu-id="127df-172">**Consider using glass strategically in small regions touching the window frame without text.**</span></span> <span data-ttu-id="127df-173">Это может сделать программу более простым, светлым и более согласованным, делая ее частью кадра.</span><span class="sxs-lookup"><span data-stu-id="127df-173">Doing so can give a program a simpler, lighter, more cohesive look by making the region appear to be part of the frame.</span></span>
-   ![<span data-ttu-id="127df-174">снимок экрана окна с полупрозрачной границей</span><span class="sxs-lookup"><span data-stu-id="127df-174">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)
-   <span data-ttu-id="127df-175">В этом примере стекло фокусирует внимание пользователя на содержимом, а не на элементах управления.</span><span class="sxs-lookup"><span data-stu-id="127df-175">In this example, glass focuses the user's attention on the content instead of the controls.</span></span>
-   <span data-ttu-id="127df-176">**Не используйте стекла в ситуациях, когда обычный фон окна будет более привлекательным или простым в использовании.**</span><span class="sxs-lookup"><span data-stu-id="127df-176">**Don't use glass in situations where a plain window background would be more attractive or easier to use.**</span></span>

<span data-ttu-id="127df-177">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="127df-177">**Correct:**</span></span>

![<span data-ttu-id="127df-178">снимок экрана окна с четырьмя рисунками и метками</span><span class="sxs-lookup"><span data-stu-id="127df-178">screen shot of window with four graphics and label</span></span> ](images/win-window-frames-image11.png)

<span data-ttu-id="127df-179">В этом примере стекло используется для того, чтобы окно Alt + Tab было простым видом.</span><span class="sxs-lookup"><span data-stu-id="127df-179">In this example, glass is used to give the Alt+Tab window a lightweight appearance.</span></span> <span data-ttu-id="127df-180">Для этого окна работает стекло, так как оно состоит из графики и одной строгой метки текста.</span><span class="sxs-lookup"><span data-stu-id="127df-180">Glass works for this window because it consists of graphics and a single, strong text label.</span></span>

<span data-ttu-id="127df-181">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="127df-181">**Incorrect:**</span></span>

![<span data-ttu-id="127df-182">снимок экрана окна с 12 графическим графиком</span><span class="sxs-lookup"><span data-stu-id="127df-182">screen shot of window with twelve graphics</span></span> ](images/win-window-frames-image12.png)

<span data-ttu-id="127df-183">В этом неверном примере использование стекла отвлекается от использования.</span><span class="sxs-lookup"><span data-stu-id="127df-183">In this incorrect example, the use of glass is distracting.</span></span> <span data-ttu-id="127df-184">Лучше выбрать обычный фон окна.</span><span class="sxs-lookup"><span data-stu-id="127df-184">A plain window background would be a better choice.</span></span>

 

 