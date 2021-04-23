---
title: Общие сведения о VML
description: Общие сведения о VML
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Язык VML (VML), ссылка
- VML (язык VML), ссылка
- Векторная графика, ссылка VML
- Векторная графика, язык VML (VML)
- Справочник по язык VML (VML)
- Справочник по VML
- Язык VML (VML), элемент Shape
- VML (язык VML), элемент Shape
- Векторная графика, элемент Shape
- Shape, элемент
- Элементы VML, Shape
- Язык VML (VML), VBScript
- VML (язык VML), VBScript
- Язык VML (VML), JavaScript
- VML (язык VML), JavaScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7a370519e3f173e7418f1aa0510cac768ff46c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413119"
---
# <a name="vml-introduction"></a><span data-ttu-id="63d15-118">Общие сведения о VML</span><span class="sxs-lookup"><span data-stu-id="63d15-118">VML Introduction</span></span>

<span data-ttu-id="63d15-119">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="63d15-119">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="63d15-120">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="63d15-120">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="63d15-121">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="63d15-121">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="63d15-122">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="63d15-122">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="63d15-123">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="63d15-123">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="63d15-124">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="63d15-124">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="63d15-125">Этот документ содержит полный подробный справочник по реализации язык VML (VML), поставляемой с Microsoft Office 2000.</span><span class="sxs-lookup"><span data-stu-id="63d15-125">This document gives a complete detailed reference to the implementation of the Vector Markup Language (VML) that is shipped with Microsoft Office 2000.</span></span> <span data-ttu-id="63d15-126">Другие реализации могут различаться.</span><span class="sxs-lookup"><span data-stu-id="63d15-126">Other implementations may vary.</span></span> <span data-ttu-id="63d15-127">Дополнительные сведения о стандарте VML см. в [спецификации VML](https://www.w3.org/TR/NOTE-datetime.html) .</span><span class="sxs-lookup"><span data-stu-id="63d15-127">Consult the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) for more information about VML as a standard.</span></span>

<span data-ttu-id="63d15-128">VML определяется как набор XML-элементов и соответствующие атрибуты для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="63d15-128">VML is defined as a set of XML elements and the corresponding attributes for each element.</span></span> <span data-ttu-id="63d15-129">Так как элемент **Shape** является базовым компоновочным блоком VML, щелкните [здесь](shape-element--vml.md) , чтобы начать ссылку.</span><span class="sxs-lookup"><span data-stu-id="63d15-129">Since the **Shape** element is the basic building block of VML, click [here](shape-element--vml.md) to begin the reference.</span></span>

<span data-ttu-id="63d15-130">Обратите внимание, что эта ссылка содержит несколько примеров и демонстраций.</span><span class="sxs-lookup"><span data-stu-id="63d15-130">Note that this reference contains several examples and demos.</span></span> <span data-ttu-id="63d15-131">Для просмотра динамической VML необходимо установить Microsoft Internet Explorer 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="63d15-131">You must have Microsoft Internet Explorer 5.0 or greater installed to view the live VML.</span></span>

<span data-ttu-id="63d15-132">В дополнение к сведениям об использовании элементов и атрибутов в качестве XML-тегов, расширяющих HTML, эта ссылка содержит синтаксис и примеры, демонстрирующие использование скриптов и модель DOM возможностей Internet Explorer 5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="63d15-132">In addition to the information about using elements and attributes as XML tags that extend HTML, this reference contains syntax and examples that show how to use the scripting and the Document Object Model features of Internet Explorer 5 or greater.</span></span> <span data-ttu-id="63d15-133">Использование скрипта с VML позволяет создавать элементы на лету и манипулировать атрибутами в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="63d15-133">Using script with VML enables you to create elements "on the fly" and manipulate attributes in real time.</span></span>

<span data-ttu-id="63d15-134">В этих примерах в этом справочнике используется VBScript и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="63d15-134">This examples in this reference uses VBScript and Javascript.</span></span> <span data-ttu-id="63d15-135">Если используется язык скрипта, отличный от языка, показанного в примере, необходимо сопоставить регистр всех имен элементов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="63d15-135">If you use use a different scripting language than the one shown in an example, you must match the case of all element and attribute names.</span></span> <span data-ttu-id="63d15-136">Ссылка предоставляет синтаксис сценариев, который подходит для языков с учетом регистра, таких как JavaScript.</span><span class="sxs-lookup"><span data-stu-id="63d15-136">The reference gives scripting syntax that is correct for case-sensitive languages such as JavaScript.</span></span> <span data-ttu-id="63d15-137">Если сомнения в отношении правильного регистра символов, используйте обозреватель объектов (например, OLEView) для изучения VGX.DLL, чтобы определить точный регистр элемента или атрибута.</span><span class="sxs-lookup"><span data-stu-id="63d15-137">If in doubt regarding the correct character case, use an object browser (such as OLEView) to explore the VGX.DLL to determine the exact case of an element or attribute.</span></span> <span data-ttu-id="63d15-138">Обратите внимание, что при использовании VML в качестве XML-тегов чувствительность к регистру зависит от типа документа базового документа.</span><span class="sxs-lookup"><span data-stu-id="63d15-138">Note that when VML is used as XML tags, case sensitivity depends on the document type of you underlying document.</span></span> <span data-ttu-id="63d15-139">Если используется режим с максимальным количеством! DOCTYPE, элементы и атрибуты будут учитываться с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="63d15-139">If you are using a strict mode !DOCTYPE, elements and attributes will be case sensitive.</span></span>

[<span data-ttu-id="63d15-140">Ссылка VML</span><span class="sxs-lookup"><span data-stu-id="63d15-140">The VML Reference</span></span>](shape-element--vml.md)

 

 