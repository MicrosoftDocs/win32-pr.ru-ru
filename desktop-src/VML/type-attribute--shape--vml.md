---
title: Атрибут Type (Shape) (VML)
description: Атрибут Type (Shape) (VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e53b275d6b6327b3d3783704dbd06156e643f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070162"
---
# <a name="type-attribute-shapevml"></a><span data-ttu-id="541c6-103">Атрибут Type (Shape) (VML)</span><span class="sxs-lookup"><span data-stu-id="541c6-103">Type Attribute (Shape)(VML)</span></span>

<span data-ttu-id="541c6-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="541c6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="541c6-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="541c6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="541c6-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="541c6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="541c6-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="541c6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="541c6-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="541c6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="541c6-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="541c6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="541c6-110">Определяет ссылку на идентификатор элемента [шапетипе](msdn-online-vml-shapetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="541c6-110">Defines a reference to the ID of a [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span> <span data-ttu-id="541c6-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="541c6-111">Read/write.</span></span> <span data-ttu-id="541c6-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="541c6-112">**String**.</span></span>

<span data-ttu-id="541c6-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="541c6-113">**Applies To**</span></span>

[<span data-ttu-id="541c6-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="541c6-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="541c6-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="541c6-115">**Tag Syntax**</span></span>

``` syntax
<v:
          element 
          type=" expression ">
```

<span data-ttu-id="541c6-116">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="541c6-116">**Script Syntax**</span></span>

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

<span data-ttu-id="541c6-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="541c6-117">**Remarks**</span></span>

<span data-ttu-id="541c6-118">Если атрибут **Type** ссылается на идентификатор элемента **шапетипе** , то заливки, контуры и штрихи **шапетипе** используются в качестве шаблонов для создания фигуры.</span><span class="sxs-lookup"><span data-stu-id="541c6-118">If the **Type** attribute references the ID of a **ShapeType** element, the fills, paths, and strokes of the **ShapeType** are used as templates to create the shape.</span></span> <span data-ttu-id="541c6-119">Значения, производные от **шапетипе** , могут быть переопределены отдельными значениями фигур.</span><span class="sxs-lookup"><span data-stu-id="541c6-119">Values derived from **ShapeType** can be overridden by individual shape values.</span></span>

<span data-ttu-id="541c6-120">При использовании в тегах строковое значение должно начинаться с символа решетки ( \# ).</span><span class="sxs-lookup"><span data-stu-id="541c6-120">If used in tags, the string value must begin with a number sign (\#) symbol.</span></span>

<span data-ttu-id="541c6-121">**Стандартный атрибут VML**</span><span class="sxs-lookup"><span data-stu-id="541c6-121">**VML Standard Attribute**</span></span>

<span data-ttu-id="541c6-122">**Пример**</span><span class="sxs-lookup"><span data-stu-id="541c6-122">**Example**</span></span>

<span data-ttu-id="541c6-123">Фигура **шапетипе** создается с именем "MyType" в качестве идентификатора.</span><span class="sxs-lookup"><span data-stu-id="541c6-123">A **ShapeType** shape is created with the "mytype" as an ID.</span></span>


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



<span data-ttu-id="541c6-124">Затем, если создать фигуру с использованием значений **шапетипе** , фигура будет иметь атрибуты «MyType» **шапетипе**; то есть "shape01" будет иметь красную заливку с синей штриховкой.</span><span class="sxs-lookup"><span data-stu-id="541c6-124">Then if you create a shape using the **ShapeType** values, the shape will have the attributes of the "mytype" **ShapeType**; that is, "shape01" will have a red fill with a blue stroke.</span></span>


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="541c6-125">Можно переопределить наследуемые значения, например, изменив цвет на зеленый.</span><span class="sxs-lookup"><span data-stu-id="541c6-125">You can override the inherited values, for example, by changing the color to green.</span></span>


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="541c6-126">[Пример атрибута Type](/previous-versions/bb264099(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="541c6-126">[Type Attribute Example](/previous-versions/bb264099(v=vs.85)).</span></span> <span data-ttu-id="541c6-127">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="541c6-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 