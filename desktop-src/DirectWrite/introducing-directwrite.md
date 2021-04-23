---
title: Знакомство с DirectWrite
description: Люди взаимодействуют с текстом все время в повседневной жизни.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite, о программе
- DirectWrite, типографские функции
- оформление
- DirectWrite, Международный текст
- DirectWrite, шрифты OpenType
- Шрифты OpenType
- DirectWrite, ClearType
- ClearType
- DirectWrite, общие сведения об API
- DirectWrite, Идвритефонтфаце
- идвритефонтфаце
- DirectWrite, отрисовка текста
- DirectWrite, режимы рендеринга
- DirectWrite, взаимодействие GDI
- DirectWrite, взаимодействие
- взаимодействие, DirectWrite
- взаимодействие, интерфейс графических устройств (GDI)
- Интерфейс графических устройств (GDI)
- GDI (интерфейс графических устройств)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103891029"
---
# <a name="introducing-directwrite"></a><span data-ttu-id="94d6a-122">Знакомство с DirectWrite</span><span class="sxs-lookup"><span data-stu-id="94d6a-122">Introducing DirectWrite</span></span>

<span data-ttu-id="94d6a-123">Люди взаимодействуют с текстом все время в повседневной жизни.</span><span class="sxs-lookup"><span data-stu-id="94d6a-123">People communicate with text all the time in their daily lives.</span></span> <span data-ttu-id="94d6a-124">Это основной способ, с помощью которого люди могут использовать увеличивающийся объем информации.</span><span class="sxs-lookup"><span data-stu-id="94d6a-124">It is the primary way for people to consume an increasing volume of information.</span></span> <span data-ttu-id="94d6a-125">В прошлом он использовался для печати содержимого, в первую очередь документы, газеты, книги и т. д.</span><span class="sxs-lookup"><span data-stu-id="94d6a-125">In the past, it used to be through printed content, primarily documents, newspapers, books, and so on.</span></span> <span data-ttu-id="94d6a-126">Все чаще это Интернет-содержимое на компьютере под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="94d6a-126">Increasingly, it is online content on their Windows PC.</span></span> <span data-ttu-id="94d6a-127">Обычный пользователь Windows тратит много времени на чтение с экрана компьютера.</span><span class="sxs-lookup"><span data-stu-id="94d6a-127">A typical Windows user spends a lot of time reading from their computer screen.</span></span> <span data-ttu-id="94d6a-128">Они могут работать в Интернете, проверять электронную почту, создавать отчеты, заполнять электронную таблицу или писать программное обеспечение, но что на самом деле выполняется чтение.</span><span class="sxs-lookup"><span data-stu-id="94d6a-128">They might be surfing the Web, scanning e-mail, composing a report, filling in a spreadsheet, or writing software, but what they're really doing is reading.</span></span> <span data-ttu-id="94d6a-129">Несмотря на то, что текст и шрифты перейти почти каждую часть взаимодействия с пользователем в Windows, для большинства пользователей чтение на экране не так удобно, как чтение напечатанных данных.</span><span class="sxs-lookup"><span data-stu-id="94d6a-129">Even though text and fonts permeate nearly every part of the user experience in Windows, for most users, reading on the screen is not as enjoyable as reading printed output.</span></span>

<span data-ttu-id="94d6a-130">Для разработчиков приложений Windows написание кода обработки текста является сложной задачей из-за повышенных требований к повышению удобочитаемости, расширенному форматированию и применению элементов управления макета, а также поддержке нескольких языков, которые приложение должно отобразить.</span><span class="sxs-lookup"><span data-stu-id="94d6a-130">For Windows application developers, writing text-handling code is a challenge because of the increased requirements for better readability, sophisticated formatting and layout control, and support for the multiple languages the application must display.</span></span> <span data-ttu-id="94d6a-131">Даже основная система обработки текста должна разрешать текстовые вводы, макеты, отображение, редактирование, копирование и вставлять.</span><span class="sxs-lookup"><span data-stu-id="94d6a-131">Even the most basic text-handling system must allow for text input, layout, display, editing, and copying and pasting.</span></span> <span data-ttu-id="94d6a-132">Пользователи Windows обычно предполагают даже больше, чем эти основные функции, и требуют даже простых редакторов для поддержки нескольких шрифтов, различных стилей абзацев, внедренных изображений, проверки орфографии и других функций.</span><span class="sxs-lookup"><span data-stu-id="94d6a-132">Windows users commonly expect even more than these basic features, requiring even simple editors to support multiple fonts, various paragraph styles, embedded images, spell checking, and other features.</span></span> <span data-ttu-id="94d6a-133">Современная модель пользовательского интерфейса также больше не ограничена одним форматом, обычным текстом, но должна обеспечить лучшую работу с богатыми шрифтами и макетами текста.</span><span class="sxs-lookup"><span data-stu-id="94d6a-133">Modern UI design is also no longer confined to single format, plain text, but needs to present a better experience with rich fonts and text layouts.</span></span>

<span data-ttu-id="94d6a-134">Это введение в то, как [DirectWrite](direct-write-portal.md) позволяет приложениям Windows расширять возможности текста для пользовательского интерфейса и документов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-134">This is an introduction to how [DirectWrite](direct-write-portal.md) enables Windows applications to enhance the text experience for UI and documents.</span></span>

## <a name="improving-the-text-experience"></a><span data-ttu-id="94d6a-135">Улучшение текстового интерфейса</span><span class="sxs-lookup"><span data-stu-id="94d6a-135">Improving the Text Experience</span></span>

<span data-ttu-id="94d6a-136">Современные приложения Windows имеют сложные требования к тексту в пользовательском интерфейсе и документах.</span><span class="sxs-lookup"><span data-stu-id="94d6a-136">Modern Windows applications have sophisticated requirements for text in their UI and documents.</span></span> <span data-ttu-id="94d6a-137">К ним относится более удобочитаемость, поддержка большого спектра языков и сценариев и высокая производительность отрисовки.</span><span class="sxs-lookup"><span data-stu-id="94d6a-137">These include better readability, support for a large variety of languages and scripts, and superior rendering performance.</span></span> <span data-ttu-id="94d6a-138">Кроме того, для большинства существующих приложений требуется способ переноса существующих вложений в базу кода WindowsWin32.</span><span class="sxs-lookup"><span data-stu-id="94d6a-138">In addition, most existing applications require a way to carry forward existing investments in the WindowsWin32 code base.</span></span>

<span data-ttu-id="94d6a-139">[DirectWrite](direct-write-portal.md) предоставляет следующие три функции, позволяющие разработчикам приложений Windows улучшать текст в своих приложениях: независимость от системы отрисовки, качественное типографское Оформление и несколько уровней функциональности.</span><span class="sxs-lookup"><span data-stu-id="94d6a-139">[DirectWrite](direct-write-portal.md) provides the following three features that enable Windows application developers to improve the text experience within their applications: independence from the rendering system, high-quality typography, and multiple layers of functionality.</span></span>

## <a name="rendering-system-independence"></a><span data-ttu-id="94d6a-140">Независимость от Rendering-System</span><span class="sxs-lookup"><span data-stu-id="94d6a-140">Rendering-System Independence</span></span>

<span data-ttu-id="94d6a-141">[DirectWrite](direct-write-portal.md) не зависит от какой-либо конкретной графической технологии.</span><span class="sxs-lookup"><span data-stu-id="94d6a-141">[DirectWrite](direct-write-portal.md) is independent of any particular graphics technology.</span></span> <span data-ttu-id="94d6a-142">Приложения могут использовать технологию отрисовки, которая лучше всего подходит для их нужд.</span><span class="sxs-lookup"><span data-stu-id="94d6a-142">Applications are free to use the rendering technology best suited to their needs.</span></span> <span data-ttu-id="94d6a-143">Это дает приложениям возможность по-прежнему выполнять визуализацию некоторых частей приложения через GDI и другие компоненты с помощью Direct3D или [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="94d6a-143">This gives applications the flexibility to continue rendering some parts of their application through GDI and other parts through Direct3D or [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="94d6a-144">На самом деле, приложение может выбрать визуализацию DirectWrite через собственный стек отрисовки.</span><span class="sxs-lookup"><span data-stu-id="94d6a-144">In fact, an application could choose to render DirectWrite through a proprietary rendering stack.</span></span>

## <a name="high-quality-typography"></a><span data-ttu-id="94d6a-145">High-Quality оформления</span><span class="sxs-lookup"><span data-stu-id="94d6a-145">High-Quality Typography</span></span>

<span data-ttu-id="94d6a-146">[DirectWrite](direct-write-portal.md) использует преимущества технологии шрифтов [OpenType](../intl/opentype-font-format.md) для обеспечения высокого качества типографской работы в приложениях Windows.</span><span class="sxs-lookup"><span data-stu-id="94d6a-146">[DirectWrite](direct-write-portal.md) takes advantage of the advances in [OpenType](../intl/opentype-font-format.md) Font technology to enable high quality typography within a Windows application.</span></span> <span data-ttu-id="94d6a-147">Система шрифтов DirectWrite предоставляет службы для работы с перечислением шрифтов, откатом шрифтов и кэшированием шрифтов, которые необходимы приложениям для обработки шрифтов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-147">The DirectWrite font system provides services for dealing with font enumeration, font fallback, and font caching, which are all needed by applications for handling fonts.</span></span>

<span data-ttu-id="94d6a-148">Поддержка [OpenType](../intl/opentype-font-format.md) , предоставляемая [DirectWrite](direct-write-portal.md) , позволяет разработчикам добавлять в свои приложения дополнительные типографские функции и поддержку международного текста.</span><span class="sxs-lookup"><span data-stu-id="94d6a-148">The [OpenType](../intl/opentype-font-format.md) support provided by [DirectWrite](direct-write-portal.md) enables developers to add to their applications advanced typographic features and support for international text.</span></span>

## <a name="support-for-advanced-typographic-features"></a><span data-ttu-id="94d6a-149">Поддержка расширенных типографских функций</span><span class="sxs-lookup"><span data-stu-id="94d6a-149">Support for Advanced Typographic Features</span></span>

<span data-ttu-id="94d6a-150">[DirectWrite](direct-write-portal.md) позволяет разработчикам приложений разблокирование функций шрифтов OpenType, которые они не могут использовать в WinForms или GDI.</span><span class="sxs-lookup"><span data-stu-id="94d6a-150">[DirectWrite](direct-write-portal.md) enables application developers to unlock the features of OpenType fonts that they couldn't use in WinForms or GDI.</span></span> <span data-ttu-id="94d6a-151">Объект DirectWrite [**идвритетипографи**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) предоставляет множество дополнительных возможностей шрифтов OpenType, таких как стилистические варианты и глифы.</span><span class="sxs-lookup"><span data-stu-id="94d6a-151">The DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) object exposes many of the advanced features of OpenType fonts, such as stylistic alternates and swashes.</span></span> <span data-ttu-id="94d6a-152">Пакет средств разработки программного обеспечения Microsoft Windows (SDK) предоставляет набор образцов шрифтов [OpenType](../intl/opentype-font-format.md) , разработанных с широкими возможностями, такими как шрифты Pericles и Pescadero.</span><span class="sxs-lookup"><span data-stu-id="94d6a-152">The Microsoft Windows Software Development Kit (SDK) provides a set of sample [OpenType](../intl/opentype-font-format.md) fonts that are designed with rich features, such as the Pericles and Pescadero fonts.</span></span> <span data-ttu-id="94d6a-153">Дополнительные сведения о функциях OpenType см. в разделе [функции шрифтов OpenType](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94d6a-153">For more details on OpenType features, see [OpenType Font Features](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span></span>

## <a name="support-for-international-text"></a><span data-ttu-id="94d6a-154">Поддержка международного текста</span><span class="sxs-lookup"><span data-stu-id="94d6a-154">Support for International Text</span></span>

<span data-ttu-id="94d6a-155">[DirectWrite](direct-write-portal.md) использует шрифты [OpenType](../intl/opentype-font-format.md) , чтобы обеспечить широкую поддержку международного текста.</span><span class="sxs-lookup"><span data-stu-id="94d6a-155">[DirectWrite](direct-write-portal.md) uses [OpenType](../intl/opentype-font-format.md) fonts to enable broad support for international text.</span></span> <span data-ttu-id="94d6a-156">Поддерживаются такие функции Юникода, как суррогаты, BIDI, перенос строк и UVS.</span><span class="sxs-lookup"><span data-stu-id="94d6a-156">Unicode features such as surrogates, BIDI, line breaking, and UVS are supported.</span></span> <span data-ttu-id="94d6a-157">Языковая настройка элементов скрипта, подстановки чисел и формирования глифов гарантирует, что текст в любом скрипте будет иметь правильный макет и отрисовку.</span><span class="sxs-lookup"><span data-stu-id="94d6a-157">Language-guided script itemization, number substitution, and glyph shaping ensure that text in any script has the correct layout and rendering.</span></span>

<span data-ttu-id="94d6a-158">В настоящее время поддерживаются следующие скрипты.</span><span class="sxs-lookup"><span data-stu-id="94d6a-158">The following scripts are currently supported:</span></span>

> [!Note]  
> <span data-ttu-id="94d6a-159">Для сценариев, помеченных атрибутом \* , системные шрифты по умолчанию отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="94d6a-159">For scripts marked with an \*, there are no default system fonts.</span></span> <span data-ttu-id="94d6a-160">Приложения должны устанавливать шрифты, поддерживающие эти скрипты.</span><span class="sxs-lookup"><span data-stu-id="94d6a-160">Applications must install fonts that support these scripts.</span></span>

 

-   <span data-ttu-id="94d6a-161">Арабский</span><span class="sxs-lookup"><span data-stu-id="94d6a-161">Arabic</span></span>
-   <span data-ttu-id="94d6a-162">Армянский</span><span class="sxs-lookup"><span data-stu-id="94d6a-162">Armenian</span></span>
-   <span data-ttu-id="94d6a-163">бенгала</span><span class="sxs-lookup"><span data-stu-id="94d6a-163">Bengala</span></span>
-   <span data-ttu-id="94d6a-164">Бопомофо</span><span class="sxs-lookup"><span data-stu-id="94d6a-164">Bopomofo</span></span>
-   <span data-ttu-id="94d6a-165">Брайля\*</span><span class="sxs-lookup"><span data-stu-id="94d6a-165">Braille\*</span></span>
-   <span data-ttu-id="94d6a-166">Канадский слоговое письмо слогового письма</span><span class="sxs-lookup"><span data-stu-id="94d6a-166">Canadian aboriginal syllabics</span></span>
-   <span data-ttu-id="94d6a-167">Чероки</span><span class="sxs-lookup"><span data-stu-id="94d6a-167">Cherokee</span></span>
-   <span data-ttu-id="94d6a-168">Китайский (упрощенное & традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="94d6a-168">Chinese (Simplified & Traditional)</span></span>
-   <span data-ttu-id="94d6a-169">Кириллица</span><span class="sxs-lookup"><span data-stu-id="94d6a-169">Cyrillic</span></span>
-   <span data-ttu-id="94d6a-170">Коптский\*</span><span class="sxs-lookup"><span data-stu-id="94d6a-170">Coptic\*</span></span>
-   <span data-ttu-id="94d6a-171">Девангари</span><span class="sxs-lookup"><span data-stu-id="94d6a-171">Devanagari</span></span>
-   <span data-ttu-id="94d6a-172">Эфиопского</span><span class="sxs-lookup"><span data-stu-id="94d6a-172">Ethiopic</span></span>
-   <span data-ttu-id="94d6a-173">Грузинский</span><span class="sxs-lookup"><span data-stu-id="94d6a-173">Georgian</span></span>
-   <span data-ttu-id="94d6a-174">глаголитик\*</span><span class="sxs-lookup"><span data-stu-id="94d6a-174">Glagolitic\*</span></span>
-   <span data-ttu-id="94d6a-175">Греческий</span><span class="sxs-lookup"><span data-stu-id="94d6a-175">Greek</span></span>
-   <span data-ttu-id="94d6a-176">Гуджарати</span><span class="sxs-lookup"><span data-stu-id="94d6a-176">Gujarati</span></span>
-   <span data-ttu-id="94d6a-177">Гурмукхи</span><span class="sxs-lookup"><span data-stu-id="94d6a-177">Gurmukhi</span></span>
-   <span data-ttu-id="94d6a-178">Иврит</span><span class="sxs-lookup"><span data-stu-id="94d6a-178">Hebrew</span></span>
-   <span data-ttu-id="94d6a-179">Японский</span><span class="sxs-lookup"><span data-stu-id="94d6a-179">Japanese</span></span>
-   <span data-ttu-id="94d6a-180">Каннада</span><span class="sxs-lookup"><span data-stu-id="94d6a-180">Kannada</span></span>
-   <span data-ttu-id="94d6a-181">Кхмерский</span><span class="sxs-lookup"><span data-stu-id="94d6a-181">Khmer</span></span>
-   <span data-ttu-id="94d6a-182">Корейский</span><span class="sxs-lookup"><span data-stu-id="94d6a-182">Korean</span></span>
-   <span data-ttu-id="94d6a-183">Лаосский</span><span class="sxs-lookup"><span data-stu-id="94d6a-183">Lao</span></span>
-   <span data-ttu-id="94d6a-184">Латиница</span><span class="sxs-lookup"><span data-stu-id="94d6a-184">Latin</span></span>
-   <span data-ttu-id="94d6a-185">Малаялам</span><span class="sxs-lookup"><span data-stu-id="94d6a-185">Malayalam</span></span>
-   <span data-ttu-id="94d6a-186">Монгольский</span><span class="sxs-lookup"><span data-stu-id="94d6a-186">Mongolian</span></span>
-   <span data-ttu-id="94d6a-187">Мьянма</span><span class="sxs-lookup"><span data-stu-id="94d6a-187">Myanmar</span></span>
-   <span data-ttu-id="94d6a-188">Новая письменность тай-лю</span><span class="sxs-lookup"><span data-stu-id="94d6a-188">New Tai Lue</span></span>
-   <span data-ttu-id="94d6a-189">Блок\*</span><span class="sxs-lookup"><span data-stu-id="94d6a-189">Ogham\*</span></span>
-   <span data-ttu-id="94d6a-190">Ория</span><span class="sxs-lookup"><span data-stu-id="94d6a-190">Odia</span></span>
-   <span data-ttu-id="94d6a-191">' Блок-PA</span><span class="sxs-lookup"><span data-stu-id="94d6a-191">'Phags-pa</span></span>
-   <span data-ttu-id="94d6a-192">руник\*</span><span class="sxs-lookup"><span data-stu-id="94d6a-192">Runic\*</span></span>
-   <span data-ttu-id="94d6a-193">Сингальский</span><span class="sxs-lookup"><span data-stu-id="94d6a-193">Sinhala</span></span>
-   <span data-ttu-id="94d6a-194">Сирийский</span><span class="sxs-lookup"><span data-stu-id="94d6a-194">Syriac</span></span>
-   <span data-ttu-id="94d6a-195">Тай Le</span><span class="sxs-lookup"><span data-stu-id="94d6a-195">Tai Le</span></span>
-   <span data-ttu-id="94d6a-196">Тамильский</span><span class="sxs-lookup"><span data-stu-id="94d6a-196">Tamil</span></span>
-   <span data-ttu-id="94d6a-197">Телугу</span><span class="sxs-lookup"><span data-stu-id="94d6a-197">Telugu</span></span>
-   <span data-ttu-id="94d6a-198">мальдивский</span><span class="sxs-lookup"><span data-stu-id="94d6a-198">Thaana</span></span>
-   <span data-ttu-id="94d6a-199">Тайский</span><span class="sxs-lookup"><span data-stu-id="94d6a-199">Thai</span></span>
-   <span data-ttu-id="94d6a-200">Тибетский</span><span class="sxs-lookup"><span data-stu-id="94d6a-200">Tibetan</span></span>
-   <span data-ttu-id="94d6a-201">Носу</span><span class="sxs-lookup"><span data-stu-id="94d6a-201">Yi</span></span>

## <a name="multiple-layers-of-functionality"></a><span data-ttu-id="94d6a-202">Несколько уровней функциональности</span><span class="sxs-lookup"><span data-stu-id="94d6a-202">Multiple Layers of Functionality</span></span>

<span data-ttu-id="94d6a-203">[DirectWrite](direct-write-portal.md) предоставляет многоуровневые уровни функциональности, каждый из которых тесно взаимодействует со следующим.</span><span class="sxs-lookup"><span data-stu-id="94d6a-203">[DirectWrite](direct-write-portal.md) provides factored layers of functionality, with each layer interacting seamlessly with the next.</span></span> <span data-ttu-id="94d6a-204">Структура API предоставляет разработчикам приложений свободу и гибкость при внедрении отдельных слоев в зависимости от их потребностей и расписания.</span><span class="sxs-lookup"><span data-stu-id="94d6a-204">The API design gives application developers the freedom and flexibility to adopt individual layers depending on their needs and schedule.</span></span> <span data-ttu-id="94d6a-205">На следующей схеме показана связь между этими слоями.</span><span class="sxs-lookup"><span data-stu-id="94d6a-205">The following diagram shows the relationship between these layers.</span></span>

![Схема DirectWrite слоев и взаимодействие с приложением или платформой пользовательского интерфейса и API графики](images/intro-01.png)

<span data-ttu-id="94d6a-207">API макета текста предоставляет функции высшего уровня, доступные в [DirectWrite](direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="94d6a-207">The text layout API provides the highest level functionality available from [DirectWrite](direct-write-portal.md).</span></span> <span data-ttu-id="94d6a-208">Она предоставляет службам приложения возможность измерять, отображать и взаимодействовать с форматированными текстовыми строками.</span><span class="sxs-lookup"><span data-stu-id="94d6a-208">It provides services for the application to measure, display, and interact with richly formatted text strings.</span></span> <span data-ttu-id="94d6a-209">Этот текстовый API можно использовать в приложениях, которые в настоящее время используют Win32's DrawText для создания современного пользовательского интерфейса с форматированным текстом.</span><span class="sxs-lookup"><span data-stu-id="94d6a-209">This text API can be used in applications that currently use Win32's DrawText to build a modern UI with richly formatted text.</span></span>

<span data-ttu-id="94d6a-210">Приложения с большим объемом текста, реализующие собственный обработчик макета, могут использовать следующий слой ниже: обработчик скриптов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-210">Text-intensive applications that implement their own layout engine may use the next layer down: the script processor.</span></span> <span data-ttu-id="94d6a-211">Обработчик скриптов разбивает фрагмент текста на блоки сценариев и обрабатывает сопоставление между представлениями Юникода с соответствующим представлением глифа в шрифте, чтобы текст скрипта правильно отображался на правильном языке.</span><span class="sxs-lookup"><span data-stu-id="94d6a-211">The script processor breaks down a chunk of text into script blocks and handles the mapping between Unicode representations to the appropriate glyph representation in the font so the text of the script can be correctly displayed in the correct language.</span></span> <span data-ttu-id="94d6a-212">Система макета, используемая слоем API макета текста, строится на основе шрифта и системы обработки сценариев.</span><span class="sxs-lookup"><span data-stu-id="94d6a-212">The layout system used by the text layout API layer is built upon the font and script processing system.</span></span>

<span data-ttu-id="94d6a-213">Уровень визуализации глифов — это самый нижний уровень функциональности, обеспечивающий функции визуализации глифов для приложений, реализующих собственный обработчик макетов текста.</span><span class="sxs-lookup"><span data-stu-id="94d6a-213">The glyph-rendering layer is the lowest layer of functionality and provides glyph-rendering functionality for applications that implement their own text layout engine.</span></span> <span data-ttu-id="94d6a-214">Слой рендеринга глифов также полезен для приложений, реализующих пользовательский модуль подготовки отчетов для изменения поведения рисования глифов с помощью функции обратного вызова в API форматирования текста [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="94d6a-214">The glyph rendering layer is also useful for applications that implement a custom renderer to modify the glyph-drawing behavior through the callback function in the [DirectWrite](direct-write-portal.md) text-formatting API.</span></span>

<span data-ttu-id="94d6a-215">Система шрифтов [DirectWrite](direct-write-portal.md) доступна для всех функциональных уровней DirectWrite и позволяет приложению получать доступ к сведениям о шрифтах и глифах.</span><span class="sxs-lookup"><span data-stu-id="94d6a-215">The [DirectWrite](direct-write-portal.md) font system is available to all the DirectWrite functional layers and enables an application to access font and glyph information.</span></span> <span data-ttu-id="94d6a-216">Он предназначен для работы с общими технологиями шрифтов и форматов данных.</span><span class="sxs-lookup"><span data-stu-id="94d6a-216">It is designed to handle common font technologies and data formats.</span></span> <span data-ttu-id="94d6a-217">Модель шрифтов DirectWrite соответствует стандартной типографской методике поддержки любого количества весов, стилей и растянутости в одном семействе шрифтов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-217">The DirectWrite font model follows the common typographic practice of supporting any number of weights, styles, and stretches in the same font family.</span></span> <span data-ttu-id="94d6a-218">Эта модель, та же самая модель, за которой следуют WPF и CSS, указывает, что шрифты, которые отличаются только по весу (полужирный, светло-и т. д.), стиль (вертикальный, курсив или наклонный) или растяжение (узкие, сжатые, широкие и т. д.) считаются членами одного семейства шрифтов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-218">This model, the same model followed by WPF and CSS, specifies that fonts differing only in weight (bold, light, and so on), style (upright, italic, or oblique) or stretch (narrow, condensed, wide, and so on) are considered to be members of a single font family.</span></span>

### <a name="improved-text-rendering-with-cleartype"></a><span data-ttu-id="94d6a-219">Улучшенная визуализация текста с помощью технологии ClearType</span><span class="sxs-lookup"><span data-stu-id="94d6a-219">Improved Text Rendering with ClearType</span></span>

<span data-ttu-id="94d6a-220">Улучшение удобочитаемости на экране является ключевым требованием для всех приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="94d6a-220">Improving readability on the screen is a key requirement for all Windows applications.</span></span> <span data-ttu-id="94d6a-221">Свидетельство от исследования в окне «научный психологии» указывает, что нам нужно уметь распознать каждую букву точно, и что даже интервал между буквами очень важен для быстрой обработки.</span><span class="sxs-lookup"><span data-stu-id="94d6a-221">The evidence from research in cognitive psychology indicates that we need to be able to recognize every letter accurately and that even spacing between letters is critical for fast processing.</span></span> <span data-ttu-id="94d6a-222">Буквы и слова, которые не являются симметричными, воспринимается как некрасивое и снижают удобство чтения.</span><span class="sxs-lookup"><span data-stu-id="94d6a-222">Letters and words that are not symmetrical are perceived as ugly and degrade the reading experience.</span></span> <span data-ttu-id="94d6a-223">Кевин Ларсон (, Microsoft Advanced Read Technologies Group, написала статью о теме, опубликованной в спектре IEEE.</span><span class="sxs-lookup"><span data-stu-id="94d6a-223">Kevin Larson, Microsoft Advanced Reading Technologies group, wrote an article on the subject that was published in Spectrum IEEE.</span></span> <span data-ttu-id="94d6a-224">Статья называется «технология текста» ( https://www.spectrum.ieee.org/print/5049) .</span><span class="sxs-lookup"><span data-stu-id="94d6a-224">The article is called "The Technology of Text" (https://www.spectrum.ieee.org/print/5049).</span></span>

<span data-ttu-id="94d6a-225">Текст в [DirectWrite](direct-write-portal.md) отображается с помощью технологии Microsoft ClearType, что повышает четкость и удобочитаемость текста.</span><span class="sxs-lookup"><span data-stu-id="94d6a-225">Text in [DirectWrite](direct-write-portal.md) is rendered using Microsoft ClearType, which enhances the clarity and readability of text.</span></span> <span data-ttu-id="94d6a-226">Технология ClearType использует преимущества того факта, что современные ЖК-дисплеи имеют полосы RGB для каждого пикселя, который можно контролировать по отдельности.</span><span class="sxs-lookup"><span data-stu-id="94d6a-226">ClearType takes advantage of the fact that modern LCD displays have RGB stripes for each pixel that can be controlled individually.</span></span> <span data-ttu-id="94d6a-227">DirectWrite использует новейшие усовершенствования технологии ClearType, впервые включенные в Windows Vista с Windows Presentation Foundation, что позволяет ему оценивать не только отдельные буквы, но и интервалы между буквами.</span><span class="sxs-lookup"><span data-stu-id="94d6a-227">DirectWrite uses the latest enhancements to ClearType, first included with Windows Vista with Windows Presentation Foundation, that enables it to evaluate not just the individual letters but also the spacing between letters.</span></span> <span data-ttu-id="94d6a-228">До этих улучшений ClearType текст с размером "10 или 12 точек" был сложен для отображения: можно поместить 1 пиксель между буквами, которые часто слишком маленькие, или 2 пиксела, что часто бывает слишком много.</span><span class="sxs-lookup"><span data-stu-id="94d6a-228">Before these ClearType enhancements, text with a "reading" size of 10 or 12 points was difficult to display: we could place either 1 pixel in between letters, which was often too little, or 2 pixels, which was often too much.</span></span> <span data-ttu-id="94d6a-229">Использование дополнительного разрешения в подпикселях дает нам дробные промежутки, что улучшает однородность и симметрию всей страницы.</span><span class="sxs-lookup"><span data-stu-id="94d6a-229">Using the extra resolution in the subpixels provides us with fractional spacing, which improves the evenness and symmetry of the entire page.</span></span>

<span data-ttu-id="94d6a-230">На следующих двух иллюстрациях показано, как могут начинаться глифы на любой границе области во время использования позиционирования в пикселах.</span><span class="sxs-lookup"><span data-stu-id="94d6a-230">The following two illustration show how glyphs may begin on any sub-pixel boundary when sub-pixel positioning is used.</span></span>

<span data-ttu-id="94d6a-231">Следующая иллюстрация отображается с помощью версии GDI визуализатора ClearType, который не применяет позиционирование в пикселях.</span><span class="sxs-lookup"><span data-stu-id="94d6a-231">The following illustration is rendered using the GDI version of the ClearType renderer, which did not employ sub-pixel positioning.</span></span>

![изображение "технология", отображаемая без позиционирования в пикселах](images/intro-03.png)

<span data-ttu-id="94d6a-233">Следующая иллюстрация отображается с использованием [DirectWrite](direct-write-portal.md) версии визуализатора ClearType, в которой используется позиционирование в пикселях.</span><span class="sxs-lookup"><span data-stu-id="94d6a-233">The following illustration is rendered using the [DirectWrite](direct-write-portal.md) version of the ClearType renderer, which uses sub-pixel positioning.</span></span>

![Иллюстрация визуализации "технология" с позиционированием в пикселах](images/intro-04.png)

<span data-ttu-id="94d6a-235">Обратите внимание, что пробелы между буквами h и n являются более четными на втором изображении, а буква o больше, чем буква n, больше, даже с буквой l.</span><span class="sxs-lookup"><span data-stu-id="94d6a-235">Note that the spacing between the letters h and n is more even in the second image and the letter o is spaced further from the letter n, more even with the letter l.</span></span> <span data-ttu-id="94d6a-236">Также обратите внимание на то, что области буквы l являются более естественными.</span><span class="sxs-lookup"><span data-stu-id="94d6a-236">Also note how the stems on the letters l are more natural looking.</span></span>

<span data-ttu-id="94d6a-237">Положение ClearType в подпикселях предлагает наиболее точные пробелы на экране, особенно небольшие размеры, в которых разница между подпикселем и целым пикселем представляет значительную долю ширины глифа.</span><span class="sxs-lookup"><span data-stu-id="94d6a-237">The subpixel ClearType positioning offers the most accurate spacing of characters on screen, especially at small sizes where the difference between a sub-pixel and a whole pixel represents a significant proportion of glyph width.</span></span> <span data-ttu-id="94d6a-238">Он позволяет измерять текст в идеальном пространстве разрешения и визуализировать его естественное расположение на ЖК-полосе цветов с детализацией по подпикселям.</span><span class="sxs-lookup"><span data-stu-id="94d6a-238">It enables text to be measured in ideal resolution space and rendered at its natural position at the LCD color stripe, with subpixel granularity.</span></span> <span data-ttu-id="94d6a-239">Текст, измеряемый и визуализированный с помощью этой технологии, определяется по определению, не зависит от разрешения, что означает, что точно такой же макет текста достигается в пределах различных способов разрешения экрана.</span><span class="sxs-lookup"><span data-stu-id="94d6a-239">Text measured and rendered using this technology is, by definition, resolution-independent, meaning that the exact same layout of text is achieved across the range of various display resolutions.</span></span>

<span data-ttu-id="94d6a-240">В отличие от любого из типов отрисовки с помощью технологии GDI, технология ClearType обеспечивает наиболее точную ширину символов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-240">Unlike either type of GDI ClearType rendering, sub-pixel ClearType offers the most accurate width of characters.</span></span>

<span data-ttu-id="94d6a-241">API текстовой строки применяет отрисовку текста в виде вложенных пикселов по умолчанию, что означает, что она измеряет текст в идеальном разрешении независимо от текущего разрешения экрана и выдает результат позиционирования глифов на основе действительно масштабируемых ширины и смещений для глифов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-241">The Text String API adopts sub-pixel text rendering by default, which means it measures text at its ideal resolution independent of the current display resolution, and produces the glyph positioning result based on the truly scaled glyph advance widths and positioning offsets.</span></span>

<span data-ttu-id="94d6a-242">Для больших объемов текста [DirectWrite](direct-write-portal.md) также позволяет использовать сглаживание вдоль оси y, чтобы сделать края более гладкими и отрисовывать письма как предназначенные для работы в конструкторе шрифтов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-242">For large-sized text, [DirectWrite](direct-write-portal.md) also enables anti-aliasing along the y-axis to make the edges smoother and render letters as the font designer intended.</span></span> <span data-ttu-id="94d6a-243">На следующем рисунке показано сглаживание по оси y.</span><span class="sxs-lookup"><span data-stu-id="94d6a-243">The following illustration shows y-direction anti-aliasing.</span></span>

![изображение «ClearType», отображаемое как текст GDI, и DirectWrite текст с сглаживанием по оси y](images/intro-05.png)

<span data-ttu-id="94d6a-245">Несмотря на то, что [DirectWrite](direct-write-portal.md) текст размещается и визуализируется с использованием подразделов ClearType по умолчанию, доступны другие параметры отрисовки.</span><span class="sxs-lookup"><span data-stu-id="94d6a-245">Although [DirectWrite](direct-write-portal.md) text is positioned and rendered using sub-pixel ClearType by default, other rendering options are available.</span></span> <span data-ttu-id="94d6a-246">Многие существующие приложения используют GDI для отрисовки большей части своего пользовательского интерфейса, а некоторые приложения используют элементы управления для редактирования системы, которые продолжают использовать GDI для отрисовки текста.</span><span class="sxs-lookup"><span data-stu-id="94d6a-246">Many existing applications use GDI to render most of their UI, and some applications use system editing controls that continue to use GDI for text rendering.</span></span> <span data-ttu-id="94d6a-247">При добавлении DirectWrite текста в эти приложения может потребоваться пожертвировать возможности чтения, предоставляемые с помощью технологии ClearType, чтобы обеспечить единообразное отображение текста в приложении.</span><span class="sxs-lookup"><span data-stu-id="94d6a-247">When adding DirectWrite text to these applications, it may be necessary to sacrifice the reading experience improvements provided by sub-pixel ClearType so that text has a consistent appearance across the application.</span></span>

<span data-ttu-id="94d6a-248">Для удовлетворения этих требований [DirectWrite](direct-write-portal.md) также поддерживает следующие параметры визуализации:</span><span class="sxs-lookup"><span data-stu-id="94d6a-248">To meet these requirements, [DirectWrite](direct-write-portal.md) also supports the following rendering options:</span></span>

-   <span data-ttu-id="94d6a-249">Технология ClearType (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="94d6a-249">Sub-pixel ClearType (default).</span></span>
-   <span data-ttu-id="94d6a-250">Технология ClearType в подпикселях с сглаживанием как по горизонтали, так и по вертикали.</span><span class="sxs-lookup"><span data-stu-id="94d6a-250">Sub-pixel ClearType with anti-aliasing in both horizontal and vertical dimensions.</span></span>
-   <span data-ttu-id="94d6a-251">Текст с псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="94d6a-251">Aliased text.</span></span>
-   <span data-ttu-id="94d6a-252">Формат GDI (например, режим чтения, используемый Microsoft Word).</span><span class="sxs-lookup"><span data-stu-id="94d6a-252">GDI natural-width (used by Microsoft Word Reading View, for example).</span></span>
-   <span data-ttu-id="94d6a-253">Совместимость с GDI — ширина (включая Восточно-азиатское внедренное растровое изображение).</span><span class="sxs-lookup"><span data-stu-id="94d6a-253">GDI compatible-width (including East Asian embedded bitmap).</span></span>

<span data-ttu-id="94d6a-254">Каждый из этих режимов подготовки можно настроить с помощью API DirectWrite и с помощью нового тюнера «входящие» в Windows 7 Inbox.</span><span class="sxs-lookup"><span data-stu-id="94d6a-254">Each of these rendering modes can be fine-tuned through the DirectWrite API and through the new Windows 7 inbox ClearType tuner.</span></span>

> [!Note]  
> <span data-ttu-id="94d6a-255">Начиная с Windows 8, в большинстве случаев следует использовать сглаживание текста в оттенках серого.</span><span class="sxs-lookup"><span data-stu-id="94d6a-255">Starting with Windows 8, you should use greyscale text antialiasing in most cases.</span></span> <span data-ttu-id="94d6a-256">Этот процесс описан в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="94d6a-256">See the next section for more information.</span></span>

 

### <a name="support-for-natural-layout"></a><span data-ttu-id="94d6a-257">Поддержка естественного макета</span><span class="sxs-lookup"><span data-stu-id="94d6a-257">Support for Natural Layout</span></span>

<span data-ttu-id="94d6a-258">Естественное расположение не зависит от разрешения, поэтому пробелы в символах не меняются при изменении масштаба или в зависимости от DPI на дисплее.</span><span class="sxs-lookup"><span data-stu-id="94d6a-258">Natural layout is resolution-independent, so the spacing of characters doesn't change as you zoom in or out, or depending on the DPI of the display.</span></span> <span data-ttu-id="94d6a-259">Дополнительное преимущество заключается в том, что для создания шрифта используется параметр «промежуток».</span><span class="sxs-lookup"><span data-stu-id="94d6a-259">A secondary advantage is that spacing is true to the design of the font.</span></span> <span data-ttu-id="94d6a-260">Естественная структура становится возможной благодаря поддержке естественной отрисовки в DirectWrite, что означает, что отдельные глифы можно размещать в долях пикселя.</span><span class="sxs-lookup"><span data-stu-id="94d6a-260">Natural layout is made possible by DirectWrite's support for natural rendering, which means individual glyphs can be positioned to a fraction of a pixel.</span></span>

<span data-ttu-id="94d6a-261">Хотя естественное расположение используется по умолчанию, некоторые приложения должны визуализировать текст с тем же отступом и внешним видом, что и GDI.</span><span class="sxs-lookup"><span data-stu-id="94d6a-261">While natural layout is the default, some applications need to render text with the same spacing and appearance as GDI.</span></span> <span data-ttu-id="94d6a-262">Для таких приложений DirectWrite предоставляет классический и естественный режимы измерения GDI, а также соответствующие режимы рендеринга.</span><span class="sxs-lookup"><span data-stu-id="94d6a-262">For such applications, DirectWrite provides GDI classic and GDI natural measuring modes and corresponding rendering modes.</span></span>

<span data-ttu-id="94d6a-263">Любой из приведенных выше режимов рендеринга можно сочетать с любым из двух режимов сглаживания: ClearType или градации серого.</span><span class="sxs-lookup"><span data-stu-id="94d6a-263">Any of the above rendering modes can be combined with either of the two antialiasing modes: ClearType or grayscale.</span></span> <span data-ttu-id="94d6a-264">Сглаживание ClearType навязывает более высокое разрешение, по отдельности управляя красным, зеленым и синим значениями цвета каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="94d6a-264">ClearType antialiasing simulations a higher resolution by individually manipulating the red, green, and blue color values of each pixel.</span></span> <span data-ttu-id="94d6a-265">Сглаживание в оттенках серого рассчитывает только одно значение (или альфа) для каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="94d6a-265">Grayscale antialiasing computes only one coverage (or alpha) value for each pixel.</span></span> <span data-ttu-id="94d6a-266">По умолчанию используется технология ClearType, но сглаживание оттенков серого рекомендуется для приложений Магазина Windows, так как оно работает быстрее и совместимо со стандартным сглаживанием, в то же время обеспечивая высокую удобочитаемость.</span><span class="sxs-lookup"><span data-stu-id="94d6a-266">ClearType is the default, but grayscale antialiasing is recommended for Windows Store apps because it is faster and is compatible with standard antialiasing, while still being highly readable.</span></span>

## <a name="api-overview"></a><span data-ttu-id="94d6a-267">Обзор API</span><span class="sxs-lookup"><span data-stu-id="94d6a-267">API Overview</span></span>

<span data-ttu-id="94d6a-268">Интерфейс [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) является отправной точкой для использования функции DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="94d6a-268">The [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface is the starting point for using DirectWrite functionality.</span></span> <span data-ttu-id="94d6a-269">Фабрика — это корневой объект, который создает набор объектов, которые можно использовать вместе.</span><span class="sxs-lookup"><span data-stu-id="94d6a-269">The factory is the root object that creates a set of objects that can be used together.</span></span>

<span data-ttu-id="94d6a-270">Операция форматирования и макета является необходимым условием для операций, так как текст необходимо правильно отформатировать и определить в соответствии с заданным набором ограничений, прежде чем он может быть нарисован или проверен на попадание.</span><span class="sxs-lookup"><span data-stu-id="94d6a-270">The formatting and layout operation is a prerequisite to the operations, as text needs to be properly formatted and laid out to a specified set of constraints before it can be drawn or hit-tested.</span></span> <span data-ttu-id="94d6a-271">Для этой цели можно создать два ключевых объекта с [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) : [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) и [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="94d6a-271">Two key objects that you can create with an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) for this purpose are [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="94d6a-272">Объект **идвритетекстформат** представляет сведения о форматировании для абзаца текста.</span><span class="sxs-lookup"><span data-stu-id="94d6a-272">An **IDWriteTextFormat** object represents the formatting information for a paragraph of text.</span></span> <span data-ttu-id="94d6a-273">Функция [**идвритефактори:: креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) принимает входную строку, связанные с ней ограничения, такие как размер заполняемого пространства, и объект **идвритетекстформат** и помещает полностью проанализированный и отформатированный результат в **идвритетекстлайаут** для использования в последующих операциях.</span><span class="sxs-lookup"><span data-stu-id="94d6a-273">The [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) function takes the input string, the associated constraints such as the dimension of the space to be filled, and the **IDWriteTextFormat** object, and puts the fully analyzed and formatted result into **IDWriteTextLayout** to use in subsequent operations.</span></span>

<span data-ttu-id="94d6a-274">Приложение может затем визуализировать текст с помощью функции [**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , предоставляемой [Direct2D](../direct2d/direct2d-portal.md) , или путем реализации функции обратного вызова, которая может использовать GDI, Direct2D или другие графические системы для отрисовки глифов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-274">The application can then render the text using the [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) function provided by [Direct2D](../direct2d/direct2d-portal.md) or by implementing a callback function that can use GDI, Direct2D, or other graphics systems to render the glyphs.</span></span> <span data-ttu-id="94d6a-275">В одном тексте формата функция [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) в Direct2D предоставляет более простой способ рисования текста без необходимости создания объекта [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="94d6a-275">For a single format text, the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function on Direct2D provides a simpler way to draw text without having to first create a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a><span data-ttu-id="94d6a-276">Форматирование и Рисование "Hello World" с помощью DirectWrite</span><span class="sxs-lookup"><span data-stu-id="94d6a-276">Formatting and Drawing "Hello World" Using DirectWrite</span></span>

<span data-ttu-id="94d6a-277">В следующем примере кода показано, как приложение может отформатировать один абзац с помощью [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) и нарисовать его с помощью функции [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) .</span><span class="sxs-lookup"><span data-stu-id="94d6a-277">The following code example shows how an application can format a single paragraph using [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and draw it using the [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function.</span></span>


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a><span data-ttu-id="94d6a-278">Доступ к системе шрифтов</span><span class="sxs-lookup"><span data-stu-id="94d6a-278">Accessing the Font System</span></span>

<span data-ttu-id="94d6a-279">Помимо указания имени семейства шрифтов для текстовой строки с помощью интерфейса [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) в приведенном выше примере, [DirectWrite](direct-write-portal.md) предоставляет приложениям больший контроль над выбором шрифтов через перечисление шрифтов и возможность создания пользовательской коллекции шрифтов на основе внедренных шрифтов документа.</span><span class="sxs-lookup"><span data-stu-id="94d6a-279">In addition to specifying a font family name for the text string by using the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface in the example above, [DirectWrite](direct-write-portal.md) provides applications more control over font selection through font enumeration and the ability to create custom font collection based on embedded document fonts.</span></span>

<span data-ttu-id="94d6a-280">Объект [**идвритефонтколлектион**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) представляет собой коллекцию семейств шрифтов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-280">The [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) object is a collection of font families.</span></span> <span data-ttu-id="94d6a-281">DirectWrite предоставляет доступ к набору шрифтов, установленных в системе, с помощью специальной коллекции шрифтов, называемой коллекцией системных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-281">DirectWrite provides access to the set of fonts installed on the system through a special font collection called the system font collection.</span></span> <span data-ttu-id="94d6a-282">Это достигается путем вызова метода [**жетсистемфонтколлектион**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) объекта [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="94d6a-282">This is obtained by calling the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) object.</span></span> <span data-ttu-id="94d6a-283">Приложение также может создать коллекцию пользовательских шрифтов из набора шрифтов, перечисленных с помощью определяемого приложением обратного вызова, то есть закрытых шрифтов, установленных приложением, или внедренных в документ шрифтов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-283">An application can also create a custom font collection from a set of fonts enumerated by an application-defined callback, that is, private fonts installed by an application, or fonts embedded in a document.</span></span>

<span data-ttu-id="94d6a-284">Затем приложение может вызвать метод [**FontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) , чтобы получить конкретный объект FontFamily в коллекции, а затем вызвать метод [**Идвритефонтфамили:: жетфирстматчингфонт**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) , чтобы получить конкретный объект [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) .</span><span class="sxs-lookup"><span data-stu-id="94d6a-284">The application can then call [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) to get to a specific FontFamily object within the collection, and then call [**IDWriteFontFamily::GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) to get to a specific [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object.</span></span> <span data-ttu-id="94d6a-285">Объект **идвритефонт** представляет шрифт в коллекции шрифтов и предоставляет свойства и несколько базовых метрик шрифта.</span><span class="sxs-lookup"><span data-stu-id="94d6a-285">The **IDWriteFont** object represents a font in a font collection and exposes properties and a few basic font metrics.</span></span>

<span data-ttu-id="94d6a-286">[**Идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) — это еще один объект, который представляет шрифт и предоставляет полный набор метрик для шрифта.</span><span class="sxs-lookup"><span data-stu-id="94d6a-286">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) is another object that represents a font and exposes a full set of metrics on a font.</span></span> <span data-ttu-id="94d6a-287">**Идвритефонтфаце** можно создать непосредственно из имени шрифта. приложению не нужно получать коллекцию шрифтов для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="94d6a-287">The **IDWriteFontFace** can be created directly from a font name; an application does not have to get a font collection to access it.</span></span> <span data-ttu-id="94d6a-288">Это полезно для приложения текстового макета, такого как Microsoft Word, которое должно запрашивать подробные сведения о конкретном шрифте.</span><span class="sxs-lookup"><span data-stu-id="94d6a-288">It is useful for a text layout application such as Microsoft Word that needs to query the details for a specific font.</span></span>

<span data-ttu-id="94d6a-289">На следующей схеме показана связь между этими объектами.</span><span class="sxs-lookup"><span data-stu-id="94d6a-289">The following diagram illustrates the relationship between these objects.</span></span>

![Схема связи между коллекцией шрифтов, семейством шрифтов и начертанием шрифта](images/fontcollection.png)

### <a name="idwritefontface"></a><span data-ttu-id="94d6a-291">идвритефонтфаце</span><span class="sxs-lookup"><span data-stu-id="94d6a-291">IDWriteFontFace</span></span>

<span data-ttu-id="94d6a-292">Объект [**идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) представляет шрифт и предоставляет более подробные сведения о шрифте, чем делает объект [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) .</span><span class="sxs-lookup"><span data-stu-id="94d6a-292">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object represents a font and provides more detailed information about the font than the [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object does.</span></span> <span data-ttu-id="94d6a-293">Метрики шрифта и глифа из **идвритефонтфаце** полезны для приложений, которые реализуют макет текста.</span><span class="sxs-lookup"><span data-stu-id="94d6a-293">The font and glyph metrics from the **IDWriteFontFace** are useful for applications that implement text layout.</span></span>

<span data-ttu-id="94d6a-294">Самые распространенные приложения не будут использовать эти API напрямую, а вместо этого будут использовать [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) или указать имя семейства шрифтов напрямую.</span><span class="sxs-lookup"><span data-stu-id="94d6a-294">Most mainstream applications will not use these APIs directly, and instead will use [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) or specify the font family name directly.</span></span>

<span data-ttu-id="94d6a-295">В следующей таблице приведена сводка сценариев использования для двух объектов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-295">The following table summarizes the usage scenarios for the two objects.</span></span>



| <span data-ttu-id="94d6a-296">Категория</span><span class="sxs-lookup"><span data-stu-id="94d6a-296">Category</span></span>                                                                                                         | [<span data-ttu-id="94d6a-297">**идвритефонт**</span><span class="sxs-lookup"><span data-stu-id="94d6a-297">**IDWriteFont**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [<span data-ttu-id="94d6a-298">**идвритефонтфаце**</span><span class="sxs-lookup"><span data-stu-id="94d6a-298">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="94d6a-299">Интерфейсы API для поддержки взаимодействия с пользователем, таких как пользовательский интерфейс для выбора шрифта: описание и другие информационные API</span><span class="sxs-lookup"><span data-stu-id="94d6a-299">APIs to support user interaction such as a font-chooser user interface: description and other informational APIs</span></span> | <span data-ttu-id="94d6a-300">Да</span><span class="sxs-lookup"><span data-stu-id="94d6a-300">Yes</span></span>                                        | <span data-ttu-id="94d6a-301">Нет</span><span class="sxs-lookup"><span data-stu-id="94d6a-301">No</span></span>                                                 |
| <span data-ttu-id="94d6a-302">Интерфейсы API для поддержки сопоставления шрифтов: семейство, стиль, вес, растяжение, покрытие символов</span><span class="sxs-lookup"><span data-stu-id="94d6a-302">APIs to support font mapping: family, style, weight, stretch, character coverage</span></span>                                 | <span data-ttu-id="94d6a-303">Да</span><span class="sxs-lookup"><span data-stu-id="94d6a-303">Yes</span></span>                                        | <span data-ttu-id="94d6a-304">Нет</span><span class="sxs-lookup"><span data-stu-id="94d6a-304">No</span></span>                                                 |
| <span data-ttu-id="94d6a-305">API DrawText</span><span class="sxs-lookup"><span data-stu-id="94d6a-305">DrawText API</span></span>                                                                                                     | <span data-ttu-id="94d6a-306">Да</span><span class="sxs-lookup"><span data-stu-id="94d6a-306">Yes</span></span>                                        | <span data-ttu-id="94d6a-307">Нет</span><span class="sxs-lookup"><span data-stu-id="94d6a-307">No</span></span>                                                 |
| <span data-ttu-id="94d6a-308">API, используемые для отрисовки</span><span class="sxs-lookup"><span data-stu-id="94d6a-308">APIs used for rendering</span></span>                                                                                          | <span data-ttu-id="94d6a-309">Нет</span><span class="sxs-lookup"><span data-stu-id="94d6a-309">No</span></span>                                         | <span data-ttu-id="94d6a-310">Да</span><span class="sxs-lookup"><span data-stu-id="94d6a-310">Yes</span></span>                                                |
| <span data-ttu-id="94d6a-311">API, используемые для макета текста: метрики глифов и т. д.</span><span class="sxs-lookup"><span data-stu-id="94d6a-311">APIs used for text layout: glyph metrics, and so on</span></span>                                                              | <span data-ttu-id="94d6a-312">Нет</span><span class="sxs-lookup"><span data-stu-id="94d6a-312">No</span></span>                                         | <span data-ttu-id="94d6a-313">Да</span><span class="sxs-lookup"><span data-stu-id="94d6a-313">Yes</span></span>                                                |
| <span data-ttu-id="94d6a-314">Интерфейсы API для элементов управления ИП и текста: метрики на уровне шрифта</span><span class="sxs-lookup"><span data-stu-id="94d6a-314">APIs for UI control and text layout: font-wide metrics</span></span>                                                           | <span data-ttu-id="94d6a-315">Да</span><span class="sxs-lookup"><span data-stu-id="94d6a-315">Yes</span></span>                                        | <span data-ttu-id="94d6a-316">Да</span><span class="sxs-lookup"><span data-stu-id="94d6a-316">Yes</span></span>                                                |



 

<span data-ttu-id="94d6a-317">Ниже приведен пример приложения, которое перечисляет шрифты в коллекции системных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-317">The following is an example application that enumerates the fonts in the system font collection.</span></span>


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a><span data-ttu-id="94d6a-318">Отрисовка текста</span><span class="sxs-lookup"><span data-stu-id="94d6a-318">Text rendering</span></span>

<span data-ttu-id="94d6a-319">Интерфейсы API отрисовки текста позволяют подготавливать глифы в шрифте [DirectWrite](direct-write-portal.md) к [Direct2D](../direct2d/direct2d-portal.md) поверхности или к независимому точечному рисунку устройства GDI или преобразовывать их в кривые или точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="94d6a-319">The text rendering APIs enable glyphs in a [DirectWrite](direct-write-portal.md) font to be rendered to a [Direct2D](../direct2d/direct2d-portal.md) surface or to a GDI device independent bitmap, or to be converted to outlines or bitmaps.</span></span> <span data-ttu-id="94d6a-320">Технология визуализации ClearType в DirectWrite поддерживает позиционирование в подпикселях с повышенной четкостью и контрастностью по сравнению с предыдущими реализациями в Windows.</span><span class="sxs-lookup"><span data-stu-id="94d6a-320">The ClearType rendering in DirectWrite supports sub-pixel positioning with improved sharpness and contrast compared to previous implementations on Windows.</span></span> <span data-ttu-id="94d6a-321">DirectWrite также поддерживает черно-белый текст с псевдонимами для поддержки сценариев, включающих Восточно-азиатские шрифты с внедренными точечными рисунками или когда пользователь отключил сглаживание шрифтов любого типа.</span><span class="sxs-lookup"><span data-stu-id="94d6a-321">DirectWrite also supports aliased black-and-white text to support scenarios involving East Asian fonts with embedded bitmaps, or where the user has disabled font smoothing of any type.</span></span>

<span data-ttu-id="94d6a-322">Все параметры настраиваются всеми доступными регуляторами ClearType, доступными через API-интерфейсы [DirectWrite](direct-write-portal.md) , а также через новый апплет панели управления Windows 7 ClearType.</span><span class="sxs-lookup"><span data-stu-id="94d6a-322">All the options are adjustable by all the available ClearType knobs accessible through the [DirectWrite](direct-write-portal.md) APIs, and also exposed via the new Windows 7 ClearType tuner control panel applet.</span></span>

<span data-ttu-id="94d6a-323">Для отрисовки глифов доступны два API-интерфейса, один из которых обеспечивает визуализацию с аппаратным ускорением через [Direct2D](../direct2d/direct2d-portal.md) , а другой предоставляет программную отрисовку точечному рисунку GDI.</span><span class="sxs-lookup"><span data-stu-id="94d6a-323">There are two APIs available for rendering glyphs, one providing hardware-accelerated rendering through [Direct2D](../direct2d/direct2d-portal.md) and the other providing software rendering to a GDI bitmap.</span></span> <span data-ttu-id="94d6a-324">Приложение, использующее [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) и реализующий обратный вызов [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) , может вызывать любую из этих функций в ответ на обратный вызов [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="94d6a-324">An application using [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) and implementing the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) callback can call either of these functions in response to a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback.</span></span> <span data-ttu-id="94d6a-325">Кроме того, приложения, которые реализуют собственный макет или работают с данными на уровне глифов, могут использовать эти API.</span><span class="sxs-lookup"><span data-stu-id="94d6a-325">Also, applications that implement their own layout or deal with glyph-level data can use these APIs.</span></span>

1.  [<span data-ttu-id="94d6a-326">**ID2DRenderTarget::D Равглифрун**</span><span class="sxs-lookup"><span data-stu-id="94d6a-326">**ID2DRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    <span data-ttu-id="94d6a-327">Приложения могут использовать [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) API [Direct2D](../direct2d/direct2d-portal.md) для обеспечения аппаратного ускорения отрисовки текста с помощью GPU.</span><span class="sxs-lookup"><span data-stu-id="94d6a-327">Applications can use the [Direct2D](../direct2d/direct2d-portal.md) API [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) to provide hardware acceleration for text rendering using the GPU.</span></span> <span data-ttu-id="94d6a-328">Аппаратное ускорение влияет на все фазы конвейера отрисовки текста — от слияния глифов до глифов и фильтрации растрового изображения, чтобы применить алгоритм смешивания ClearType к окончательно отображаемым выходным данным.</span><span class="sxs-lookup"><span data-stu-id="94d6a-328">Hardware acceleration affects all phases of the text rendering pipeline—from merging glyphs into glyph runs and filtering the glyph-run bitmap, to applying the ClearType blending algorithm to the final displayed output.</span></span> <span data-ttu-id="94d6a-329">Это рекомендуемый API для получения наилучшей производительности отрисовки.</span><span class="sxs-lookup"><span data-stu-id="94d6a-329">This is the recommended API for getting the best rendering performance.</span></span>

2.  [<span data-ttu-id="94d6a-330">**Идвритебитмапрендертаржет::D Равглифрун**</span><span class="sxs-lookup"><span data-stu-id="94d6a-330">**IDWriteBitmapRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    <span data-ttu-id="94d6a-331">Приложения могут использовать метод [**идвритебитмапрендертаржет::D равглифрун**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) для выполнения программного отображения выполнения глифов до точечного рисунка 32 бит/с.</span><span class="sxs-lookup"><span data-stu-id="94d6a-331">Applications can use the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to perform a software-rendering of a run of glyphs to a 32-bpp bitmap.</span></span> <span data-ttu-id="94d6a-332">Объект [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) инкапсулирует растровое изображение и контекст устройства памяти, который можно использовать для отрисовки глифов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-332">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object encapsulates a bitmap and a memory device context that can be used for rendering glyphs.</span></span> <span data-ttu-id="94d6a-333">Этот API полезен, если вы хотите остаться в GDI, так как у вас есть существующая база кода, отображаемая в GDI.</span><span class="sxs-lookup"><span data-stu-id="94d6a-333">This API is useful if you want to stay with GDI because you have an existing code base that renders in GDI.</span></span>

<span data-ttu-id="94d6a-334">Если у вас есть приложение с существующим кодом макета текста, использующим GDI, и вы хотите сохранить существующий код макета, но использовать [DirectWrite](direct-write-portal.md) только для завершающего этапа отрисовки глифов, [**Идвритегдиинтероп:: креатефонтфацефромхдк**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) предоставляет мост между двумя API.</span><span class="sxs-lookup"><span data-stu-id="94d6a-334">If you have an application that has existing text layout code that uses GDI, and you want to preserve its existing layout code but use [DirectWrite](direct-write-portal.md) just for the final step of rendering glyphs, [**IDWriteGdiInterop::CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) provides the bridge between the two APIs.</span></span> <span data-ttu-id="94d6a-335">Перед вызовом этой функции приложение будет использовать функцию **идвритегдиинтероп:: креатефонтфацефромхдк** для получения ссылки Font-Face из контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="94d6a-335">Before calling this function, the application will use the **IDWriteGdiInterop::CreateFontFaceFromHdc** function to get a font-face reference from a device context.</span></span>

> [!Note]  
> <span data-ttu-id="94d6a-336">В большинстве случаев приложениям может не потребоваться использовать эти API-интерфейсы для отрисовки глифов.</span><span class="sxs-lookup"><span data-stu-id="94d6a-336">For most scenarios, applications may not need to use these glyph-rendering APIs.</span></span> <span data-ttu-id="94d6a-337">После того как приложение создало объект [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , он может использовать метод [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) для отрисовки текста.</span><span class="sxs-lookup"><span data-stu-id="94d6a-337">After an application has created an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, it can use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method to render the text.</span></span>

 

## <a name="custom-rendering-modes"></a><span data-ttu-id="94d6a-338">Пользовательские режимы отрисовки</span><span class="sxs-lookup"><span data-stu-id="94d6a-338">Custom Rendering Modes</span></span>

<span data-ttu-id="94d6a-339">Ряд параметров влияет на отрисовку текста, например гамма, уровень ClearType, геометрию в пикселях и улучшенную контрастность.</span><span class="sxs-lookup"><span data-stu-id="94d6a-339">A number of parameters affect text rendering, such as gamma, ClearType level, pixel geometry, and enhanced contrast.</span></span> <span data-ttu-id="94d6a-340">Параметры отрисовки инкапсулированы объектом, который реализует открытый интерфейс [**идвритерендерингпарамс**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) .</span><span class="sxs-lookup"><span data-stu-id="94d6a-340">Rendering parameters are encapsulated by an object, which implements the public [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) interface.</span></span> <span data-ttu-id="94d6a-341">Объект параметров отрисовки автоматически инициализируется на основе свойств оборудования и (или) пользовательских настроек, заданных в приложении ClearType панели управления в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="94d6a-341">The rendering parameters object is automatically initialized based on hardware properties and/or user preferences specified through the ClearType control panel applet in Windows 7.</span></span> <span data-ttu-id="94d6a-342">Как правило, если клиент использует API макета [DirectWrite](direct-write-portal.md) , то DirectWrite автоматически выбирает режим рендеринга, соответствующий указанному режиму измерения.</span><span class="sxs-lookup"><span data-stu-id="94d6a-342">Generally, if a client uses the [DirectWrite](direct-write-portal.md) layout API, DirectWrite will automatically select a rendering mode that corresponds to the specified measuring mode.</span></span>

<span data-ttu-id="94d6a-343">Приложения, которым требуется больший контроль, могут использовать [**идвритефактори:: креатекустомрендерингпарамс**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) для реализации различных параметров отрисовки.</span><span class="sxs-lookup"><span data-stu-id="94d6a-343">Applications that want more control can use [**IDWriteFactory::CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) to implement the different rendering options.</span></span> <span data-ttu-id="94d6a-344">Эта функция также может использоваться для установки гаммы, геометрии в пикселях и улучшенной контрастности.</span><span class="sxs-lookup"><span data-stu-id="94d6a-344">This function can also be used to set the gamma, pixel geometry, and enhanced contrast.</span></span>

<span data-ttu-id="94d6a-345">Ниже приведены различные доступные параметры отрисовки.</span><span class="sxs-lookup"><span data-stu-id="94d6a-345">The following are the various rendering options available:</span></span>

-   <span data-ttu-id="94d6a-346">Сглаживание в дочерних точках</span><span class="sxs-lookup"><span data-stu-id="94d6a-346">Sub-pixel anti-aliasing</span></span>

    <span data-ttu-id="94d6a-347">Приложение задает для параметра *рендерингмоде* значение дврите \_ режима рендеринга \_ \_ естественное, чтобы указать отрисовку с сглаживанием только в горизонтальном измерении.</span><span class="sxs-lookup"><span data-stu-id="94d6a-347">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL to specify rendering with anti-aliasing in the horizontal dimension only.</span></span>

-   <span data-ttu-id="94d6a-348">Сглаживание для дочерних точек в горизонтальных и вертикальных измерениях.</span><span class="sxs-lookup"><span data-stu-id="94d6a-348">Sub-pixel anti-aliasing in both horizontal and vertical dimensions.</span></span>

    <span data-ttu-id="94d6a-349">Приложение задает для параметра *рендерингмоде* значение дврите \_ режима рендеринга \_ \_ Natural \_ симметрично, чтобы указать отрисовку с сглаживанием как по горизонтали, так и по вертикали.</span><span class="sxs-lookup"><span data-stu-id="94d6a-349">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL\_SYMMETRIC to specify rendering with anti-aliasing in both horizontal and vertical dimensions.</span></span> <span data-ttu-id="94d6a-350">Таким образом, кривые и диагональные линии выглядят более гладко за счет некоторого мягкости и обычно используются с размерами выше 16 ппем.</span><span class="sxs-lookup"><span data-stu-id="94d6a-350">This makes curves and diagonal lines look smoother at the expense of some softness, and is typically used at sizes above 16 ppem.</span></span>

-   <span data-ttu-id="94d6a-351">Текст с псевдонимом</span><span class="sxs-lookup"><span data-stu-id="94d6a-351">Aliased Text</span></span>

    <span data-ttu-id="94d6a-352">Приложение устанавливает параметр *рендерингмоде* в \_ режим рендеринга дврите \_ , \_ чтобы указать текст с псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="94d6a-352">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_ALIASED to specify aliased text.</span></span>

-   <span data-ttu-id="94d6a-353">Текст в градациях серого</span><span class="sxs-lookup"><span data-stu-id="94d6a-353">Grayscale Text</span></span>

    <span data-ttu-id="94d6a-354">Приложение задает для параметра *пикселжеометри* значение дврите \_ пиксельной \_ геометрии \_ Flat, чтобы указать текст в градациях серого.</span><span class="sxs-lookup"><span data-stu-id="94d6a-354">The application sets the *pixelGeometry* parameter to DWRITE\_PIXEL\_GEOMETRY\_FLAT to specify grayscale text.</span></span>

-   <span data-ttu-id="94d6a-355">Совместимый с GDI-ширина (включая Восточно-азиатское внедренное изображение)</span><span class="sxs-lookup"><span data-stu-id="94d6a-355">GDI compatible-width (including East Asian embedded bitmap)</span></span>

    <span data-ttu-id="94d6a-356">Приложение задает для параметра *рендерингмоде* значение дврите \_ режима рендеринга \_ \_ \_ классическая, чтобы задать сглаживание, совместимое с GDI.</span><span class="sxs-lookup"><span data-stu-id="94d6a-356">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC to specify GDI compatible-width anti-aliasing.</span></span>

-   <span data-ttu-id="94d6a-357">Естественная толщина GDI</span><span class="sxs-lookup"><span data-stu-id="94d6a-357">GDI natural-width</span></span>

    <span data-ttu-id="94d6a-358">Приложение задает для параметра *рендерингмоде* значение дврите \_ режима отрисовки \_ \_ GDI \_ Natural, чтобы задать совместимое сглаживание GDI.</span><span class="sxs-lookup"><span data-stu-id="94d6a-358">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_NATURAL to specify GDI natural-width compatible anti-aliasing.</span></span>

-   <span data-ttu-id="94d6a-359">Текст контура</span><span class="sxs-lookup"><span data-stu-id="94d6a-359">Outline text</span></span>

    <span data-ttu-id="94d6a-360">Для отрисовки крупного размера разработчик приложения может предпочесть визуализироваться с помощью контура шрифта, а не с помощью растрирования растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="94d6a-360">For rendering at large sizes, an application developer might prefer to render by using the font outline rather than by rasterizing into a bitmap.</span></span> <span data-ttu-id="94d6a-361">Приложение устанавливает параметр *рендерингмоде* в **\_ \_ \_ структуру режима рендеринга дврите** , чтобы указать, что отрисовка должна обходить средство программной прорисовки и использовать контуры напрямую.</span><span class="sxs-lookup"><span data-stu-id="94d6a-361">The application sets the *renderingMode* parameter to **DWRITE\_RENDERING\_MODE\_OUTLINE** to specify that rendering should bypass the rasterizer and use the outlines directly.</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="94d6a-362">Взаимодействие GDI</span><span class="sxs-lookup"><span data-stu-id="94d6a-362">GDI Interoperability</span></span>

<span data-ttu-id="94d6a-363">Интерфейс [**идвритегдиинтероп**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) обеспечивает взаимодействие с GDI.</span><span class="sxs-lookup"><span data-stu-id="94d6a-363">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface provides interoperability with GDI.</span></span> <span data-ttu-id="94d6a-364">Это позволяет приложениям продолжить существующие инвестиции в базовые модули кода GDI и выборочно использовать [DirectWrite](direct-write-portal.md) для отрисовки или разметки.</span><span class="sxs-lookup"><span data-stu-id="94d6a-364">This enables applications to continue their existing investment in GDI code bases and selectively use [DirectWrite](direct-write-portal.md) for either rendering or layout.</span></span>

<span data-ttu-id="94d6a-365">Ниже приведены API-интерфейсы, которые позволяют приложению переходить на систему шрифтов GDI или из нее:</span><span class="sxs-lookup"><span data-stu-id="94d6a-365">The following are the APIs that enable an application to migrate to or from the GDI font system:</span></span>

-   [<span data-ttu-id="94d6a-366">**креатефонтфромлогфонт**</span><span class="sxs-lookup"><span data-stu-id="94d6a-366">**CreateFontFromLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    <span data-ttu-id="94d6a-367">Создает объект [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) , соответствующий свойствам, указанным в структуре [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="94d6a-367">Creates an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object that matches the properties specified by the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

-   [<span data-ttu-id="94d6a-368">**конвертфонттологфонт**</span><span class="sxs-lookup"><span data-stu-id="94d6a-368">**ConvertFontToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    <span data-ttu-id="94d6a-369">Инициализирует структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) на основе свойств, совместимых с GDI, для указанного [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont).</span><span class="sxs-lookup"><span data-stu-id="94d6a-369">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont).</span></span>

-   [<span data-ttu-id="94d6a-370">**конвертфонтфацетологфонт**</span><span class="sxs-lookup"><span data-stu-id="94d6a-370">**ConvertFontFaceToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    <span data-ttu-id="94d6a-371">Инициализирует структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) на основе свойств, совместимых с GDI, для указанного [**идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface).</span><span class="sxs-lookup"><span data-stu-id="94d6a-371">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface).</span></span>

-   [<span data-ttu-id="94d6a-372">**креатефонтфацефромхдк**</span><span class="sxs-lookup"><span data-stu-id="94d6a-372">**CreateFontFaceFromHdc**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    <span data-ttu-id="94d6a-373">Создает объект [**идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , соответствующий выбранному в данный момент **хфонт**.</span><span class="sxs-lookup"><span data-stu-id="94d6a-373">Creates an [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object that corresponds to the currently selected **HFONT**.</span></span>

## <a name="conclusion"></a><span data-ttu-id="94d6a-374">Заключение</span><span class="sxs-lookup"><span data-stu-id="94d6a-374">Conclusion</span></span>

<span data-ttu-id="94d6a-375">Улучшение возможностей чтения — это отличная ценность для пользователей, будь то экран или на бумаге.</span><span class="sxs-lookup"><span data-stu-id="94d6a-375">Improving the reading experience is of great value to users whether it is on the screen or on paper.</span></span> <span data-ttu-id="94d6a-376">[DirectWrite](direct-write-portal.md) обеспечивает простоту использования и многоуровневую модель программирования для разработчиков приложений, чтобы улучшить работу с текстом для приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="94d6a-376">[DirectWrite](direct-write-portal.md) provides the ease of use and the layered programming model for application developers to improve the text experience for their Windows applications.</span></span> <span data-ttu-id="94d6a-377">Приложения могут использовать DirectWrite для отображения форматированного текста для пользовательского интерфейса и документов с помощью API макета.</span><span class="sxs-lookup"><span data-stu-id="94d6a-377">Applications can use DirectWrite to render richly formatted text for their UI and documents with the layout API.</span></span> <span data-ttu-id="94d6a-378">В более сложных сценариях приложение может работать непосредственно с глифами, получить доступ к шрифтам и т. д., а также использовать возможности DirectWrite для предоставления высокого качества типографского оформления.</span><span class="sxs-lookup"><span data-stu-id="94d6a-378">For more complex scenarios, an application can work directly with glyphs, access fonts, and so on, and harness the power of DirectWrite to deliver high-quality typography.</span></span>

<span data-ttu-id="94d6a-379">Возможности взаимодействия [DirectWrite](direct-write-portal.md) позволяют разработчикам приложений переносить существующие базы кода Win32 и внедрять DirectWrite в своих приложениях выборочно.</span><span class="sxs-lookup"><span data-stu-id="94d6a-379">The interoperability capabilities of [DirectWrite](direct-write-portal.md) enable application developers to carry forward their existing Win32 codebases and adopt DirectWrite selectively within their applications.</span></span>

 

 