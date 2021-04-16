---
title: Элемент пути VML
description: Элемент пути VML
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1de9440761479d6b3dc6cb10c96b00ea48626247
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672301"
---
# <a name="vml-path-element"></a><span data-ttu-id="29292-103">Элемент пути VML</span><span class="sxs-lookup"><span data-stu-id="29292-103">VML Path Element</span></span>

<span data-ttu-id="29292-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="29292-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="29292-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="29292-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="29292-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="29292-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="29292-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="29292-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="29292-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="29292-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="29292-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="29292-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="29292-110">Определяет контур для фигуры.</span><span class="sxs-lookup"><span data-stu-id="29292-110">Defines a path for a shape.</span></span>

<span data-ttu-id="29292-111">Следующие атрибуты изменяют тень.</span><span class="sxs-lookup"><span data-stu-id="29292-111">The following attributes modify a shadow.</span></span>



| <span data-ttu-id="29292-112">attribute</span><span class="sxs-lookup"><span data-stu-id="29292-112">Attribute</span></span>                                                        | <span data-ttu-id="29292-113">Описание</span><span class="sxs-lookup"><span data-stu-id="29292-113">Description</span></span>                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="29292-114">арровок</span><span class="sxs-lookup"><span data-stu-id="29292-114">Arrowok</span></span>](msdn-online-vml-arrowok-attribute.md)                 | <span data-ttu-id="29292-115">Определяет, будут ли отображаться стрелки.</span><span class="sxs-lookup"><span data-stu-id="29292-115">Determines whether arrowheads will be displayed.</span></span>                                |
| [<span data-ttu-id="29292-116">коннектанглес</span><span class="sxs-lookup"><span data-stu-id="29292-116">ConnectAngles</span></span>](msdn-online-vml-connectangles-attribute.md)     | <span data-ttu-id="29292-117">Указывает, как кривая будет подключаться к точке соединения.</span><span class="sxs-lookup"><span data-stu-id="29292-117">Specifies how a curve will connect to a connection point.</span></span>                       |
| [<span data-ttu-id="29292-118">коннектлокс</span><span class="sxs-lookup"><span data-stu-id="29292-118">ConnectLocs</span></span>](msdn-online-vml-connectlocs-attribute.md)         | <span data-ttu-id="29292-119">Определяет расположение точек соединения по пути.</span><span class="sxs-lookup"><span data-stu-id="29292-119">Defines the location of connection points on a path.</span></span>                            |
| [<span data-ttu-id="29292-120">коннекттипе</span><span class="sxs-lookup"><span data-stu-id="29292-120">ConnectType</span></span>](msdn-online-vml-connecttype-attribute.md)         | <span data-ttu-id="29292-121">Определяет тип точки соединения, используемый для присоединения фигур к другим фигурам.</span><span class="sxs-lookup"><span data-stu-id="29292-121">Defines the type of connection point used for attaching shapes to other shapes.</span></span> |
| [<span data-ttu-id="29292-122">екструсионок</span><span class="sxs-lookup"><span data-stu-id="29292-122">ExtrusionOK</span></span>](msdn-online-vml-extrusionok-attribute.md)         | <span data-ttu-id="29292-123">Определяет, будет ли отображаться объем на объеме.</span><span class="sxs-lookup"><span data-stu-id="29292-123">Determines whether an extrusion will be displayed.</span></span>                              |
| [<span data-ttu-id="29292-124">филлок</span><span class="sxs-lookup"><span data-stu-id="29292-124">FillOK</span></span>](msdn-online-vml-fillok-attribute.md)                   | <span data-ttu-id="29292-125">Определяет, будет ли отображаться заливка.</span><span class="sxs-lookup"><span data-stu-id="29292-125">Determines whether a fill will be displayed.</span></span>                                    |
| [<span data-ttu-id="29292-126">градиентшапеок</span><span class="sxs-lookup"><span data-stu-id="29292-126">GradientShapeOK</span></span>](msdn-online-vml-gradientshapeok-attribute.md) | <span data-ttu-id="29292-127">Определяет, будет ли отображаться фигура градиента.</span><span class="sxs-lookup"><span data-stu-id="29292-127">Determines whether a gradient shape will be displayed.</span></span>                          |
| [<span data-ttu-id="29292-128">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="29292-128">ID</span></span>](id-attribute--path--vml.md)                                | <span data-ttu-id="29292-129">Определяет уникальный идентификатор для пути.</span><span class="sxs-lookup"><span data-stu-id="29292-129">Defines a unique identifier for a path.</span></span>                                         |
| [<span data-ttu-id="29292-130">лимо</span><span class="sxs-lookup"><span data-stu-id="29292-130">Limo</span></span>](msdn-online-vml-limo-attribute.md)                       | <span data-ttu-id="29292-131">Определяет точку растяжения на пути.</span><span class="sxs-lookup"><span data-stu-id="29292-131">Defines a stretch point on the path.</span></span>                                            |
| [<span data-ttu-id="29292-132">шадовок</span><span class="sxs-lookup"><span data-stu-id="29292-132">ShadowOK</span></span>](msdn-online-vml-shadowok-attribute.md)               | <span data-ttu-id="29292-133">Определяет, будет ли отображаться тень.</span><span class="sxs-lookup"><span data-stu-id="29292-133">Determines whether a shadow will be displayed.</span></span>                                  |
| [<span data-ttu-id="29292-134">строкеок</span><span class="sxs-lookup"><span data-stu-id="29292-134">StrokeOK</span></span>](msdn-online-vml-strokeok-attribute.md)               | <span data-ttu-id="29292-135">Определяет, будет ли отображаться штрих.</span><span class="sxs-lookup"><span data-stu-id="29292-135">Determines whether a stroke will be displayed.</span></span>                                  |
| [<span data-ttu-id="29292-136">текстбоксрект</span><span class="sxs-lookup"><span data-stu-id="29292-136">TextBoxRect</span></span>](msdn-online-vml-textboxrect-attribute.md)         | <span data-ttu-id="29292-137">Определяет одно или несколько текстовых полей внутри фигуры.</span><span class="sxs-lookup"><span data-stu-id="29292-137">Defines one or more textboxes inside a shape.</span></span>                                   |
| [<span data-ttu-id="29292-138">текстпасок</span><span class="sxs-lookup"><span data-stu-id="29292-138">TextPathOK</span></span>](msdn-online-vml-textpathok-attribute.md)           | <span data-ttu-id="29292-139">Определяет, будет ли отображаться текстпас.</span><span class="sxs-lookup"><span data-stu-id="29292-139">Determines whether a textpath will be displayed.</span></span>                                |
| [<span data-ttu-id="29292-140">V</span><span class="sxs-lookup"><span data-stu-id="29292-140">V</span></span>](msdn-online-vml-v-attribute.md)                             | <span data-ttu-id="29292-141">Определяет команды, составляющие путь.</span><span class="sxs-lookup"><span data-stu-id="29292-141">Defines the commands that make up a path.</span></span>                                       |



 

<span data-ttu-id="29292-142">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="29292-142">**Remarks**</span></span>

<span data-ttu-id="29292-143">Этот элемент должен быть определен внутри элемента [Shape](shape-element--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="29292-143">This element must be defined within a [Shape](shape-element--vml.md) element.</span></span>

<span data-ttu-id="29292-144">В следующем коде показано, как определить фигуру с путем.</span><span class="sxs-lookup"><span data-stu-id="29292-144">The following code shows how to define a shape with a path.</span></span>


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



<span data-ttu-id="29292-145">Обратите внимание, что атрибут [V](msdn-online-vml-v-attribute.md) **пути** заменяет атрибут [path](msdn-online-vml-path-attribute.md) [фигуры](shape-element--vml.md).</span><span class="sxs-lookup"><span data-stu-id="29292-145">Note that the [V](msdn-online-vml-v-attribute.md) attribute of **Path** replaces the [Path](msdn-online-vml-path-attribute.md) attribute of [Shape](shape-element--vml.md).</span></span>

<span data-ttu-id="29292-146">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="29292-146">**Examples**</span></span>

-   <span data-ttu-id="29292-147">[Пример дочернего элемента простого пути](/previous-versions/bb229545(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="29292-147">[Simple Path Child Element Example](/previous-versions/bb229545(v=vs.85))</span></span>
-   [<span data-ttu-id="29292-148">Пример дочернего элемента динамического пути</span><span class="sxs-lookup"><span data-stu-id="29292-148">Dynamic Path Child Element Example</span></span>](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 