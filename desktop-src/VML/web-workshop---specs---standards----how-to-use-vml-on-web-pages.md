---
title: Использование VML на веб-страницах
description: Использование VML на веб-страницах
ms.assetid: ae20b789-1890-4560-bcc0-536f126c5a41
keywords:
- Язык VML (VML), веб-семинар
- VML (язык VML), веб-семинар
- Векторная графика, веб-семинар
- Язык VML (VML), разработка веб-страниц
- VML (язык VML), разработка веб-страниц
- Векторная графика, проектирование веб-страниц
- Разработка веб-страниц, задачи VML
- Веб-семинар, задачи VML
- Разработка веб-страниц, язык VML (VML)
- Веб-семинар, язык VML (VML)
- Язык VML (VML), консорциум W3C (W3C)
- VML (язык VML), консорциум W3C (W3C)
- Векторная графика, консорциум W3C (W3C)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189353fd5a6c50ffbdcf3fe2ad3efe7e82b8e219
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672341"
---
# <a name="how-to-use-vml-on-webpages"></a><span data-ttu-id="8c880-116">Использование VML на веб-страницах</span><span class="sxs-lookup"><span data-stu-id="8c880-116">How to Use VML on Webpages</span></span>

<span data-ttu-id="8c880-117">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8c880-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8c880-118">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="8c880-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8c880-119">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="8c880-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8c880-120">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8c880-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8c880-121">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8c880-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8c880-122">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8c880-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8c880-123">Этот документ дополняет [спецификацию язык VML (VML)](https://www.w3.org/TR/NOTE-datetime.html) , которая была отправлена в консорциум W3C (W3C).</span><span class="sxs-lookup"><span data-stu-id="8c880-123">This document supplements the [Vector Markup Language (VML) specification](https://www.w3.org/TR/NOTE-datetime.html) that was submitted to the World Wide Web Consortium (W3C).</span></span> <span data-ttu-id="8c880-124">С этим документом и полной спецификацией VML вы сможете использовать VML для проектирования веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="8c880-124">With this document and the complete VML specification, you should be able to use VML to design webpages.</span></span> <span data-ttu-id="8c880-125">Предполагается, что у вас уже есть опыт работы с HTML.</span><span class="sxs-lookup"><span data-stu-id="8c880-125">We have assumed that you already have a working knowledge of HTML.</span></span>

## <a name="part-i-basic-topics"></a><span data-ttu-id="8c880-126">Часть 1. Основные разделы</span><span class="sxs-lookup"><span data-stu-id="8c880-126">Part I: Basic Topics</span></span>

-   [<span data-ttu-id="8c880-127">Рисование базовых фигур</span><span class="sxs-lookup"><span data-stu-id="8c880-127">Drawing Basic Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----drawing-basic-shapes.md)
-   [<span data-ttu-id="8c880-128">Использование предопределенных фигур</span><span class="sxs-lookup"><span data-stu-id="8c880-128">Using Predefined Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----using-predefined-shapes.md)
-   [<span data-ttu-id="8c880-129">Цветовые фигуры</span><span class="sxs-lookup"><span data-stu-id="8c880-129">Coloring Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----coloring-shapes.md)
-   [<span data-ttu-id="8c880-130">Масштабирование фигур</span><span class="sxs-lookup"><span data-stu-id="8c880-130">Scaling Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md)
-   [<span data-ttu-id="8c880-131">Позиционирование фигур</span><span class="sxs-lookup"><span data-stu-id="8c880-131">Positioning Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----positioning-shapes.md)
-   [<span data-ttu-id="8c880-132">Группирование фигур</span><span class="sxs-lookup"><span data-stu-id="8c880-132">Grouping Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----grouping-shapes.md)

## <a name="part-ii-advanced-topics"></a><span data-ttu-id="8c880-133">Часть II. Дополнительные разделы</span><span class="sxs-lookup"><span data-stu-id="8c880-133">Part II: Advanced Topics</span></span>

-   [<span data-ttu-id="8c880-134">Использование элемента Шапетипе</span><span class="sxs-lookup"><span data-stu-id="8c880-134">Using the Shapetype Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----shapetype--element.md)
-   [<span data-ttu-id="8c880-135">Использование элемента Stroke</span><span class="sxs-lookup"><span data-stu-id="8c880-135">Using the Stroke Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----stroke--element.md)
-   [<span data-ttu-id="8c880-136">Использование элемента заливки</span><span class="sxs-lookup"><span data-stu-id="8c880-136">Using the Fill Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)
-   [<span data-ttu-id="8c880-137">Использование элемента Image</span><span class="sxs-lookup"><span data-stu-id="8c880-137">Using the Image Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----image--element.md)
-   [<span data-ttu-id="8c880-138">Использование элемента Background</span><span class="sxs-lookup"><span data-stu-id="8c880-138">Using the Background Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----background--element.md)
-   [<span data-ttu-id="8c880-139">Использование элемента Shadow</span><span class="sxs-lookup"><span data-stu-id="8c880-139">Using the Shadow Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----shadow--element.md)
-   [<span data-ttu-id="8c880-140">Использование элемента Path</span><span class="sxs-lookup"><span data-stu-id="8c880-140">Using the Path Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----path--element.md)
-   [<span data-ttu-id="8c880-141">Использование элемента TextBox</span><span class="sxs-lookup"><span data-stu-id="8c880-141">Using the Textbox Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----textbox--element.md)
-   [<span data-ttu-id="8c880-142">Использование локального пространства координат</span><span class="sxs-lookup"><span data-stu-id="8c880-142">Using Local Coordinate Space</span></span>](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md)
-   [<span data-ttu-id="8c880-143">Использование элемента «формулы»</span><span class="sxs-lookup"><span data-stu-id="8c880-143">Using the Formulas Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----formulas--element.md)
-   [<span data-ttu-id="8c880-144">Использование элемента Handles</span><span class="sxs-lookup"><span data-stu-id="8c880-144">Using the Handles Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----handles--element.md)
-   [<span data-ttu-id="8c880-145">Использование элемента Текстпас</span><span class="sxs-lookup"><span data-stu-id="8c880-145">Using the Textpath Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----textpath--element.md)

> [!Note]  
> <span data-ttu-id="8c880-146">Примеры, приведенные в этом справочнике, предназначены для Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8c880-146">The samples provided in this reference are designed for Internet Explorer.</span></span> <span data-ttu-id="8c880-147">Мы также предоставили иллюстрации, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="8c880-147">We have also provided illustrations where possible.</span></span>

 

 

 