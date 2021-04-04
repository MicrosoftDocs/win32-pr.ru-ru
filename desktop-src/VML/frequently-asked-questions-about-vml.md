---
title: Часто задаваемые вопросы о VML
description: Часто задаваемые вопросы о VML
ms.assetid: f7f2ce12-facf-4042-b2a7-acaa3e25816a
keywords:
- Язык VML (VML), часто задаваемые вопросы
- VML (язык VML), вопросы и ответы
- Векторная графика, часто задаваемые вопросы
- Язык VML (VML), часто задаваемые вопросы
- VML (язык VML), часто задаваемые вопросы
- Векторная графика, часто задаваемые вопросы
- Язык VML (VML), различия в GIF
- VML (язык VML), различия в GIF
- Язык VML (VML), различия PNG
- VML (язык VML), различия PNG
- Векторная графика, различия в растровых форматах
- Язык VML (VML), XML
- VML (язык VML), XML
- Векторная графика, XML
- Язык VML (VML), анимация
- VML (язык VML), анимация
- Векторная графика, анимация
- Язык VML (VML), Macromedia Flash
- VML (язык VML), Macromedia Flash
- Векторная графика, Macromedia Flash
- растровые форматы
- анимация
- Macromedia Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e108f2055e7a0fbae1c5ed542fe68c59ec9b212b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987724"
---
# <a name="frequently-asked-questions-about-vml"></a><span data-ttu-id="15dea-126">Часто задаваемые вопросы о VML</span><span class="sxs-lookup"><span data-stu-id="15dea-126">Frequently Asked Questions About VML</span></span>

<span data-ttu-id="15dea-127">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="15dea-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="15dea-128">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="15dea-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="15dea-129">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="15dea-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="15dea-130">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="15dea-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="15dea-131">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="15dea-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="15dea-132">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="15dea-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="does-vml-compete-with-gif-and-png"></a><span data-ttu-id="15dea-133">Конкурирует ли VML с GIF и PNG?</span><span class="sxs-lookup"><span data-stu-id="15dea-133">Does VML compete with GIF and PNG?</span></span>

<span data-ttu-id="15dea-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="15dea-134">No.</span></span> <span data-ttu-id="15dea-135">GIF и PNG являются растровыми (или битовыми) форматами, которые можно использовать для хранения векторной графики.</span><span class="sxs-lookup"><span data-stu-id="15dea-135">Both GIF and PNG are raster (or bit-mapped) formats that can be used to store vector graphics.</span></span> <span data-ttu-id="15dea-136">Растровые форматы хранят каждый пиксель, тогда как векторные форматы, такие как VML, используют математические описания или контуры для описания графики.</span><span class="sxs-lookup"><span data-stu-id="15dea-136">Raster formats store every pixel, whereas vector formats such as VML use mathematical descriptions or outlines to describe the graphics.</span></span> <span data-ttu-id="15dea-137">Векторная графика, хранящаяся в векторном формате, более компактнее, чем в растровых форматах, что приводит к ускоренному времени загрузки для веб-пользователей.</span><span class="sxs-lookup"><span data-stu-id="15dea-137">Vector graphics stored in a vector-based format are more compact than those stored in raster formats, resulting in faster download times for Web users.</span></span>

<span data-ttu-id="15dea-138">Кроме того, графика VML доставляется в HTML-страницу, а не на внешние файлы, как в случае с GIF и PNG уже сегодня.</span><span class="sxs-lookup"><span data-stu-id="15dea-138">In addition, VML graphics are delivered inline to the HTML page rather than relying on external files, as is the case with GIF and PNG today.</span></span> <span data-ttu-id="15dea-139">Это позволяет графикам VML масштабироваться и взаимодействовать с другими элементами веб-страницы при изменении размера страницы, тем самым улучшая взаимодействие с конечными пользователями.</span><span class="sxs-lookup"><span data-stu-id="15dea-139">This allows VML graphics to scale and interact with other Web page elements as the page is resized, thus improving the end-user experience.</span></span>

<span data-ttu-id="15dea-140">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="15dea-140">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="why-is-microsoft-supporting-another-xml-based-standard-when-xml-is-hardly-in-use-and-is-young-enough-as-it-is"></a><span data-ttu-id="15dea-141">Почему корпорация Майкрософт поддерживает другой стандарт на основе XML, когда XML вряд ли используется и достаточно велик, чем это?</span><span class="sxs-lookup"><span data-stu-id="15dea-141">Why is Microsoft supporting another XML-based standard when XML is hardly in use and is young enough as it is?</span></span>

<span data-ttu-id="15dea-142">XML — это мощный, но простой способ представления структурированных данных в Интернете и полностью дополняющий HTML для отображения.</span><span class="sxs-lookup"><span data-stu-id="15dea-142">XML is a powerful yet simple way to represent structured data on the Web, and fully complements HTML for display.</span></span> <span data-ttu-id="15dea-143">VML — это один из примеров многих зависящих от приложения форматов на основе XML, которые будут разработаны и реализованы в ближайшие месяцы.</span><span class="sxs-lookup"><span data-stu-id="15dea-143">VML is one example of the many application-specific, XML-based formats that will be developed and implemented in the coming months.</span></span> <span data-ttu-id="15dea-144">Например, в следующей версии Office язык VML будет использоваться для добавления заметка к документам HTML, чтобы сохранять сведения о форматировании графических элементов Office в формате HTML, а значит, пользователи Office могут легко переключаться между двумя форматами.</span><span class="sxs-lookup"><span data-stu-id="15dea-144">For instance, in the next version of Office, VML will be used to annotate HTML documents -- to preserve formatting information of Office Art graphics between the native Office file format and HTML, thus enabling Office users to switch seamlessly between the two formats.</span></span>

<span data-ttu-id="15dea-145">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="15dea-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="who-will-support-vml"></a><span data-ttu-id="15dea-146">Кто будет поддерживать VML?</span><span class="sxs-lookup"><span data-stu-id="15dea-146">Who will support VML?</span></span>

<span data-ttu-id="15dea-147">Мы планируем, чтобы многие поставщики поддерживали VML.</span><span class="sxs-lookup"><span data-stu-id="15dea-147">We expect many vendors to support VML.</span></span> <span data-ttu-id="15dea-148">Например, для Autodesk, Hewlett-Packard, Macromedia и VISIO предусмотрена поддержка VML в будущих версиях своих продуктов.</span><span class="sxs-lookup"><span data-stu-id="15dea-148">For example, Autodesk, Hewlett-Packard, Macromedia, and VISIO have pledged support for VML in future versions of their products.</span></span> <span data-ttu-id="15dea-149">Корпорация Майкрософт приработала поддержку VML в будущих версиях своих платформ, таких как Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="15dea-149">Microsoft has pledged support for VML in future versions of its platforms such as Internet Explorer.</span></span> <span data-ttu-id="15dea-150">Кроме того, VML будет использоваться в следующем поколении Office, чтобы включить циклическое преобразование между форматом Office и HTML.</span><span class="sxs-lookup"><span data-stu-id="15dea-150">In addition, VML will be used in the next generation of Office to enable "round-tripping" between the Office format and HTML.</span></span>

<span data-ttu-id="15dea-151">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="15dea-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-support-animation"></a><span data-ttu-id="15dea-152">Поддерживает ли VML анимацию?</span><span class="sxs-lookup"><span data-stu-id="15dea-152">Does VML support animation?</span></span>

<span data-ttu-id="15dea-153">Нет, сейчас нет.</span><span class="sxs-lookup"><span data-stu-id="15dea-153">No, it currently doesn't.</span></span> <span data-ttu-id="15dea-154">Однако мы работаем с нашими партнерами VML, чтобы добавить возможности анимации в формат VML.</span><span class="sxs-lookup"><span data-stu-id="15dea-154">However, we are working with our VML partners to add animation capability into the VML format.</span></span> <span data-ttu-id="15dea-155">Поскольку VML основан на XML, набор тегов можно легко расширить для дополнительных функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="15dea-155">Since VML is based on XML, the tag set can be easily extended for additional functionality.</span></span>

<span data-ttu-id="15dea-156">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="15dea-156">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-replace-macromedia-flash-didnt-macromedia-just-submit-their-flash-format-for-vector-graphics-to-the-w3c"></a><span data-ttu-id="15dea-157">Заменяет ли VML Macromedia Flash?</span><span class="sxs-lookup"><span data-stu-id="15dea-157">Does VML replace Macromedia Flash?</span></span> <span data-ttu-id="15dea-158">Не только компания Macromedia отправила свой формат Flash для векторной графики в консорциум W3C?</span><span class="sxs-lookup"><span data-stu-id="15dea-158">Didn't Macromedia just submit their Flash format for vector graphics to the W3C?</span></span>

<span data-ttu-id="15dea-159">Нет.</span><span class="sxs-lookup"><span data-stu-id="15dea-159">No.</span></span> <span data-ttu-id="15dea-160">VML — это текстовый формат обмена данными и доставки для векторной графики, тогда как Flash — это двоичный формат для доставки векторной графики и анимации.</span><span class="sxs-lookup"><span data-stu-id="15dea-160">VML is a text-based interchange and delivery format for vector graphics, whereas Flash is a binary format for the delivery of vector-based graphics and animation.</span></span>

<span data-ttu-id="15dea-161">Компания Macromedia не отправила свой формат файла консорциуму W3C.</span><span class="sxs-lookup"><span data-stu-id="15dea-161">Macromedia did not submit their file format to the W3C.</span></span> <span data-ttu-id="15dea-162">Однако они открывали свои форматы файлов для разработчиков приложений, веб-разработчиков и конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="15dea-162">However, they did open their file format up for application developers, Web developers and end users.</span></span> <span data-ttu-id="15dea-163">Подробнее см. в разделе <https://www.macromedia.com>.</span><span class="sxs-lookup"><span data-stu-id="15dea-163">See <https://www.macromedia.com> for more information.</span></span>

[<span data-ttu-id="15dea-164">Назад к обзору VML</span><span class="sxs-lookup"><span data-stu-id="15dea-164">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

 