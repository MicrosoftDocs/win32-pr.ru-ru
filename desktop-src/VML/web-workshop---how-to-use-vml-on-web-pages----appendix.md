---
title: Приложение (VML)
description: В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Веб-семинар, пространства имен
- Веб-семинар, стили поведения
- Разработка веб-страниц, пространства имен
- Разработка веб-страниц, стили поведения
- Язык VML (VML), пространства имен
- VML (язык VML), пространства имен
- Векторная графика, пространства имен
- Язык VML (VML), стили поведения
- VML (язык VML), стили поведения
- Векторная графика, стили поведения
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d4e7a6a7e44671b7ee835eea263d9ce36a27d8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414556"
---
# <a name="appendix-vml"></a><span data-ttu-id="add2a-114">Приложение (VML)</span><span class="sxs-lookup"><span data-stu-id="add2a-114">Appendix (VML)</span></span>

<span data-ttu-id="add2a-115">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="add2a-115">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="add2a-116">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="add2a-116">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="add2a-117">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="add2a-117">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="add2a-118">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="add2a-118">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="add2a-119">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="add2a-119">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="add2a-120">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="add2a-120">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="add2a-121">Чтобы обозреватели могли передавать данные в процессор, характерный для VML, необходимо ввести некоторую информацию, например пространства имен и стили поведения.</span><span class="sxs-lookup"><span data-stu-id="add2a-121">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as namespaces and behavior styles.</span></span> <span data-ttu-id="add2a-122">Затем можно использовать VML для ввода графики в `<BODY>` регион.</span><span class="sxs-lookup"><span data-stu-id="add2a-122">You can then use VML to type graphics in the `<BODY>` region.</span></span>

<span data-ttu-id="add2a-123">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="add2a-123">In this topic:</span></span>

-   [<span data-ttu-id="add2a-124">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="add2a-124">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="add2a-125">Стили поведения</span><span class="sxs-lookup"><span data-stu-id="add2a-125">Behavior Styles</span></span>](#behavior-styles)

## <a name="namespaces"></a><span data-ttu-id="add2a-126">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="add2a-126">Namespaces</span></span>

<span data-ttu-id="add2a-127">Механизм XML указывает пространство имен, откуда берется элемент.</span><span class="sxs-lookup"><span data-stu-id="add2a-127">An XML mechanism indicates the namespace that an element comes from.</span></span> <span data-ttu-id="add2a-128">При переключении из синтаксического анализа в HTML для синтаксического анализа в XML этот механизм обозначает параметр в HTML.</span><span class="sxs-lookup"><span data-stu-id="add2a-128">If you switch from parsing in HTML to parsing in XML, this mechanism indicates the switch within HTML.</span></span>

<span data-ttu-id="add2a-129">Попросите поставщика обработчика VML, какие сведения требуются для пространства имен XML.</span><span class="sxs-lookup"><span data-stu-id="add2a-129">Ask the vender of your VML processor what information is required for the XML namespace.</span></span>

<span data-ttu-id="add2a-130">Если для визуализации VML используется Microsoft Internet Explorer, всегда вводите в тег следующую строку `<HTML>` :</span><span class="sxs-lookup"><span data-stu-id="add2a-130">If you use Microsoft Internet Explorer to render VML, always type the following line in the `<HTML>` tag:</span></span>


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



<span data-ttu-id="add2a-131">Эта информация указывает Internet Explorer переключиться на пространство имен urn: schemas-microsoft-com: VML при синтаксическом анализе XML-тега с префиксом `v:` и передать полученные данные в обработчик VML.</span><span class="sxs-lookup"><span data-stu-id="add2a-131">This information tells Internet Explorer to switch to namespace "urn:schemas-microsoft-com:vml" when parsing an XML tag with a prefix `v:`, and to hand off the resulting data to the VML processor.</span></span>

<span data-ttu-id="add2a-132">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="add2a-132">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="behavior-styles"></a><span data-ttu-id="add2a-133">Стили поведения</span><span class="sxs-lookup"><span data-stu-id="add2a-133">Behavior Styles</span></span>

<span data-ttu-id="add2a-134">VML определяется в Microsoft Internet Explorer как поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="add2a-134">VML is defined in Microsoft Internet Explorer as a default behavior.</span></span>

<span data-ttu-id="add2a-135">Для визуализации VML всегда вводите следующие строки в `<HEAD>` области:</span><span class="sxs-lookup"><span data-stu-id="add2a-135">To render VML, always type the following lines in the `<HEAD>` region:</span></span>


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



<span data-ttu-id="add2a-136">VML реализован в Internet Explorer с помощью VGX.DLL.</span><span class="sxs-lookup"><span data-stu-id="add2a-136">VML is implemented in Internet Explorer through VGX.DLL.</span></span> <span data-ttu-id="add2a-137">Если начальная установка браузера не включала в себя поведение VML, может потребоваться добавить ее в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="add2a-137">If your initial installation of the browser did not include VML behavior, you may need to add it as an option.</span></span> <span data-ttu-id="add2a-138">Добавлять тег не нужно `<object>` .</span><span class="sxs-lookup"><span data-stu-id="add2a-138">You do not need to add an `<object>` tag.</span></span>

 

 
