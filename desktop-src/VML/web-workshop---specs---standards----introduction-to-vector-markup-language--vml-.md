---
title: Язык VML (VML)
description: Язык VML (VML)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Язык VML (VML), сведения
- VML (язык VML), сведения
- Векторная графика, сведения
- Векторная графика, язык VML (VML)
- Язык VML (VML), консорциум W3C (W3C)
- VML (язык VML), консорциум W3C (W3C)
- Векторная графика, консорциум W3C (W3C)
- Векторная графика, преимущества VML
- Язык VML (VML), преимущества
- VML (язык VML), преимущества
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ba51fd041f36915eaafe20201876653f597e04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105674520"
---
# <a name="vector-markup-language-vml"></a><span data-ttu-id="baa99-113">Язык VML (VML)</span><span class="sxs-lookup"><span data-stu-id="baa99-113">Vector Markup Language (VML)</span></span>

<span data-ttu-id="baa99-114">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="baa99-114">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="baa99-115">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="baa99-115">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!NOTE]
> <span data-ttu-id="baa99-116">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="baa99-116">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="baa99-117">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="baa99-117">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="baa99-118">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="baa99-118">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="baa99-119">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="baa99-119">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

<span data-ttu-id="baa99-120">Язык VML (VML) — это формат обмена, редактирования и доставки на основе XML для высококачественной векторной графики в Интернете, который соответствует потребностям пользователей, работающих с производительностью, и специалистов по проектированию графики.</span><span class="sxs-lookup"><span data-stu-id="baa99-120">Vector Markup Language (VML) is an XML-based exchange, editing, and delivery format for high-quality vector graphics on the Web that meets the needs of both productivity users and graphic design professionals.</span></span> <span data-ttu-id="baa99-121">XML — это простой, гибкий и открытый текстовый язык, дополняющий HTML.</span><span class="sxs-lookup"><span data-stu-id="baa99-121">XML is an emerging simple, flexible, and open text-based language that complements HTML.</span></span> <span data-ttu-id="baa99-122">(Подробные сведения о XML см. в [разделе XML](/documentation/?frame=true) библиотеки MSDN.)</span><span class="sxs-lookup"><span data-stu-id="baa99-122">(See the [XML section](/documentation/?frame=true) of the MSDN Library for detailed information on XML.)</span></span>

<span data-ttu-id="baa99-123">В настоящее время в Microsoft Internet Explorer версии 5,0 или более поздней поддерживается VML.</span><span class="sxs-lookup"><span data-stu-id="baa99-123">VML is currently supported by Microsoft Internet Explorer version 5.0 or later.</span></span>

<span data-ttu-id="baa99-124">В соответствии с консорциумом W3C в качестве стандарта для векторной графики в Интернете предложено значение VML (см. [язык VML (VML)](https://www.w3.org/TR/NOTE-VML)).</span><span class="sxs-lookup"><span data-stu-id="baa99-124">VML has been proposed to the W3C as a standard for vector graphics on the Web (see [Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-VML)).</span></span> <span data-ttu-id="baa99-125">Корпорация Майкрософт продолжает издержки в разработке и реализации технологий на основе XML, работая с ведущими отраслевыми партнерами (AutoDesk, Hewlett-Packard, Macromedia, Visio) и консорциумом W3C для улучшения веб-стандартов.</span><span class="sxs-lookup"><span data-stu-id="baa99-125">Microsoft is continuing to lead the charge in the development and implementation of XML-based technologies, working with leading industry partners (AutoDesk, Hewlett-Packard, Macromedia, Visio) and the W3C to advance Web-based standards.</span></span> <span data-ttu-id="baa99-126">Мы планируем работать с консорциумом W3C, чтобы в конце концов применялись к одному стандартному формату для векторной графики в Интернете.</span><span class="sxs-lookup"><span data-stu-id="baa99-126">We expect to work with the W3C to ultimately drive to one standard format for vector graphics on the Web.</span></span>

<span data-ttu-id="baa99-127">VML также поддерживается Microsoft Office 2000 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="baa99-127">VML is also supported by Microsoft Office 2000 or later.</span></span> <span data-ttu-id="baa99-128">Microsoft Word, Microsoft Excel и Microsoft PowerPoint можно использовать для создания графики VML.</span><span class="sxs-lookup"><span data-stu-id="baa99-128">Microsoft Word, Microsoft Excel, and Microsoft PowerPoint can be used to create VML graphics.</span></span>

### <a name="using-vml"></a><span data-ttu-id="baa99-129">Использование VML</span><span class="sxs-lookup"><span data-stu-id="baa99-129">Using VML</span></span>

<span data-ttu-id="baa99-130">Чтобы использовать VML на веб-страницах, используйте элемент Style для импорта поведения VML, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="baa99-130">To use VML in your web pages, use a style element to import the VML behavior, as shown in the following code.</span></span>

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

<span data-ttu-id="baa99-131">Затем объявите пространство имен VML, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="baa99-131">Next, declare the VML namespace, as shown in the following code sample.</span></span>

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

<span data-ttu-id="baa99-132">Наконец, добавьте элементы VML для определения эффектов визуализации.</span><span class="sxs-lookup"><span data-stu-id="baa99-132">Finally, add VML elements to define visuals effects.</span></span> <span data-ttu-id="baa99-133">Например, следующий код VML создает красный овал.</span><span class="sxs-lookup"><span data-stu-id="baa99-133">For example, the following VML code creates a red oval.</span></span>

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> <span data-ttu-id="baa99-134">Для получения наилучших результатов при использовании документов в строгом режиме убедитесь, что разметка является допустимой и правильно сформированной.</span><span class="sxs-lookup"><span data-stu-id="baa99-134">For best results when using strict mode documents, be sure that your markup is valid and well-formed.</span></span> <span data-ttu-id="baa99-135">Дополнительные сведения см. в разделе! Страница ссылки DOCTYPE.</span><span class="sxs-lookup"><span data-stu-id="baa99-135">For more information, please see the !DOCTYPE reference page.</span></span>


### <a name="benefits-of-vml"></a><span data-ttu-id="baa99-136">Преимущества VML</span><span class="sxs-lookup"><span data-stu-id="baa99-136">Benefits of VML</span></span>

-   <span data-ttu-id="baa99-137">VML упрощает разработку для пользователей и разработчиков.</span><span class="sxs-lookup"><span data-stu-id="baa99-137">VML makes authoring easier for productivity users and authors.</span></span> <span data-ttu-id="baa99-138">Он упрощает обмен данными (посредством вырезания и вставки) и последующее редактирование векторной графики между широким спектром производительности и разработки приложений.</span><span class="sxs-lookup"><span data-stu-id="baa99-138">It facilitates the exchange (via cut and paste) and subsequent editing of vector graphics between a wide variety of productivity and design applications.</span></span>
-   <span data-ttu-id="baa99-139">VML обеспечивает более быструю загрузку изображений и улучшает взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="baa99-139">VML provides faster graphic downloads and a better user experience.</span></span> <span data-ttu-id="baa99-140">Она позволяет доставлять высококачественную, полностью интегрированную векторную графику в Интернете, используя открытый текстовый формат.</span><span class="sxs-lookup"><span data-stu-id="baa99-140">It allows the delivery of high-quality, fully integrated, scalable vector graphics to the Web, in an open text-based format.</span></span> <span data-ttu-id="baa99-141">Вместо того, чтобы ссылаться на графики как на внешние файлы, рисунки VML доставляются вместе с HTML-страницей, что позволяет им взаимодействовать и масштабировать их с помощью взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="baa99-141">Rather than referencing graphics as external files, VML graphics are delivered inline with the HTML page, allowing them to interact and scale with user interaction.</span></span>
-   <span data-ttu-id="baa99-142">VML открыт и основан на стандартах.</span><span class="sxs-lookup"><span data-stu-id="baa99-142">VML is open and standards-based.</span></span> <span data-ttu-id="baa99-143">Это формат на основе XML.</span><span class="sxs-lookup"><span data-stu-id="baa99-143">It is an XML-based format.</span></span> <span data-ttu-id="baa99-144">XML 1,0 — это открытый, простой текстовый язык, который описывает структурированные данные в Интернете и дополняет HTML для вывода.</span><span class="sxs-lookup"><span data-stu-id="baa99-144">XML 1.0 is an open, simple, text-based language for describing structured data on the Web, and complements HTML for display.</span></span> <span data-ttu-id="baa99-145">VML также поддерживает другие стандарты W3C, такие как каскадные таблицы стилей 2,0 (CSS), которые задают сведения о стиле и 2-D положении, а также модель DOM (DOM), что позволяет разработчикам единообразно взаимодействовать с элементами страницы в виде объектов.</span><span class="sxs-lookup"><span data-stu-id="baa99-145">VML also supports other W3C standards, such as Cascading Style Sheets 2.0 (CSS), which specifies style information and 2-D positioning, as well as the Document Object Model (DOM), which allows developers to interact consistently with page elements as objects.</span></span>

### <a name="for-additional-information"></a><span data-ttu-id="baa99-146">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="baa99-146">For additional information</span></span>

<span data-ttu-id="baa99-147">См. следующие ссылки:</span><span class="sxs-lookup"><span data-stu-id="baa99-147">See the links below:</span></span>

-   <span data-ttu-id="baa99-148">Ответы на часто задаваемые вопросы о VML см. в разделе [вопросы и ответы о VML](frequently-asked-questions-about-vml.md).</span><span class="sxs-lookup"><span data-stu-id="baa99-148">For answers to frequently asked questions about VML, see the [VML FAQ](frequently-asked-questions-about-vml.md).</span></span>
-   <span data-ttu-id="baa99-149">Руководство по использованию VML на веб-страницах см. в разделе [использование VML на веб-страницах](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), дополняющих [спецификацию VML](https://www.w3.org/TR/NOTE-datetime.html) , отправленную консорциуму W3C.</span><span class="sxs-lookup"><span data-stu-id="baa99-149">For a tutorial on using VML on Web pages, see [How to Use VML on Web Pages](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), which complements the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) submitted to the W3C.</span></span>
-   <span data-ttu-id="baa99-150">Сведения о типах данных VML см. в документе [основные типы VML](basic-vml-types.md) .</span><span class="sxs-lookup"><span data-stu-id="baa99-150">For information on VML data types, see the [Basic VML Types](basic-vml-types.md) document.</span></span>
-   <span data-ttu-id="baa99-151">Полный справочник по VML, в том числе сведения об использовании VML с тегами, а также в написании сценариев см. в [справочнике по VML](msdn-online-vml-introduction.md).</span><span class="sxs-lookup"><span data-stu-id="baa99-151">For the complete reference on VML, including information on how to use VML with tags as well as scripting, see the [VML Reference](msdn-online-vml-introduction.md).</span></span>