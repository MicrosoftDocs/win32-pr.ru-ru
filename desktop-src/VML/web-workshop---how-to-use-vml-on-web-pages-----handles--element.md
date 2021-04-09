---
title: Использование элемента Handles
description: Использование элемента Handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Веб-семинар, обрабатывает элемент
- Разработка веб-страниц, обработка элемента
- Язык VML (VML), обрабатывает элемент
- VML (язык VML), обрабатывает элемент
- Векторная графика, Handles, элемент
- обрабатывает элемент
- Элементы VML, дескрипторы
- Фигуры VML, обработка элемента
- Язык VML (VML), присоединение текста к фигурам
- VML (язык VML), присоединение текста к фигурам
- Векторная графика, присоединение текста к фигурам
- Фигуры VML, присоединение текста
- присоединение текста к фигурам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54c721d50f51c46cd4bf08393e85ad83307fc1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070062"
---
# <a name="using-the-handles-element"></a><span data-ttu-id="a61bd-116">Использование элемента Handles</span><span class="sxs-lookup"><span data-stu-id="a61bd-116">Using the Handles Element</span></span>

<span data-ttu-id="a61bd-117">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a61bd-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a61bd-118">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="a61bd-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a61bd-119">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="a61bd-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a61bd-120">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a61bd-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a61bd-121">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a61bd-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a61bd-122">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a61bd-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a61bd-123">В этом разделе будет показано, как использовать `<handles>` элемент для присоединения текста к фигуре.</span><span class="sxs-lookup"><span data-stu-id="a61bd-123">In this topic, we will illustrate how to use the `<handles>` element to attach text to a shape.</span></span>

<span data-ttu-id="a61bd-124">`<handles>`Вложенный элемент можно поместить внутри `<shape>` или `<shapetype>` , чтобы определить элементы пользовательского интерфейса, которые могут варьировать значения  назначений в фигуре.</span><span class="sxs-lookup"><span data-stu-id="a61bd-124">You can place the `<handles>` sub-element inside `<shape>` or `<shapetype>` to define user interface elements that can vary the **adj** values on the shape.</span></span>

<span data-ttu-id="a61bd-125">Например, как показано в следующем представлении VML, можно задать маркер регулировки (желтый квадрат), который пользователи могут просто перетаскивать для изменения формы.</span><span class="sxs-lookup"><span data-stu-id="a61bd-125">For example, as shown the following VML representation, you can provide an adjust handle (yellow box) that users can simply drag to adjust the shape.</span></span>

<span data-ttu-id="a61bd-126">Примечание. маркеры доступны при просмотре этой фигуры VML в Microsoft Office приложениях, где фигура должна быть манипулабле.</span><span class="sxs-lookup"><span data-stu-id="a61bd-126">Note: the handles are available when this VML shape is viewed in Microsoft Office applications, where the shape is intended to be manipulable.</span></span>

![shape1.gif (564 байт)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="a61bd-128">Обратите внимание, что единственным различием между предыдущим представлением VML и следующим является значение **года** .</span><span class="sxs-lookup"><span data-stu-id="a61bd-128">Notice that the only difference between the preceding VML representation and the following one is the **adj** value.</span></span>

![shape2.gif (1361 байт)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="a61bd-130">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span><span class="sxs-lookup"><span data-stu-id="a61bd-130">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span></span>

 

 