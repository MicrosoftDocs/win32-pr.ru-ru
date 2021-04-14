---
title: Атрибут ID (VML)
description: Атрибут ID (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487901"
---
# <a name="id-attribute-vml"></a><span data-ttu-id="ffc91-103">Атрибут ID (VML)</span><span class="sxs-lookup"><span data-stu-id="ffc91-103">ID Attribute (VML)</span></span>

<span data-ttu-id="ffc91-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ffc91-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ffc91-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ffc91-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ffc91-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ffc91-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ffc91-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ffc91-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ffc91-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ffc91-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ffc91-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ffc91-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ffc91-110">Предоставляет уникальный идентификатор для элемента.</span><span class="sxs-lookup"><span data-stu-id="ffc91-110">Provides a unique identifier for an element.</span></span> <span data-ttu-id="ffc91-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="ffc91-111">Read/write.</span></span> <span data-ttu-id="ffc91-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="ffc91-112">**String**.</span></span>

<span data-ttu-id="ffc91-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="ffc91-113">**Applies To**</span></span>

<span data-ttu-id="ffc91-114">Все элементы VML.</span><span class="sxs-lookup"><span data-stu-id="ffc91-114">All VML elements.</span></span>

<span data-ttu-id="ffc91-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="ffc91-115">**Tag Syntax**</span></span>

<span data-ttu-id="ffc91-116"><v: *ElementName* ID = " *иднаме* " ></span><span class="sxs-lookup"><span data-stu-id="ffc91-116"><v: *elementname* id=" *idname* "></span></span>

<span data-ttu-id="ffc91-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="ffc91-117">**Script Syntax**</span></span>

<span data-ttu-id="ffc91-118">*ElementName* . ID = " *иднаме* "</span><span class="sxs-lookup"><span data-stu-id="ffc91-118">*elementname* .id =" *idname* "</span></span>

<span data-ttu-id="ffc91-119">*выражение* = *ElementName*. ID</span><span class="sxs-lookup"><span data-stu-id="ffc91-119">*expression*=*elementname*.id</span></span>

<span data-ttu-id="ffc91-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="ffc91-120">**Remarks**</span></span>

<span data-ttu-id="ffc91-121">Используйте **ID** для ссылки на конкретный элемент.</span><span class="sxs-lookup"><span data-stu-id="ffc91-121">Use **ID** to refer to a specific element.</span></span> <span data-ttu-id="ffc91-122">Создав фигуру и задавая ей идентификатор, можно использовать имя идентификатора, если требуется управлять элементом.</span><span class="sxs-lookup"><span data-stu-id="ffc91-122">Once you have created a shape and given it an ID, you can use the ID name when you want to manipulate the element.</span></span>

<span data-ttu-id="ffc91-123">Для использования элемента [шапетипе](msdn-online-vml-shapetype-element.md) требуется **идентификатор** .</span><span class="sxs-lookup"><span data-stu-id="ffc91-123">**ID** is required to use the [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span>

<span data-ttu-id="ffc91-124">При создании VML с помощью Microsoft Office, если фигуре назначено имя объектной модели, то для **идентификатора** задается это имя.</span><span class="sxs-lookup"><span data-stu-id="ffc91-124">When VML is generated by Microsoft Office, if an object model name is assigned to the shape, then **ID** is set to this name.</span></span> <span data-ttu-id="ffc91-125">Если имя объектной модели не задано, то имя создается с помощью *SPID* (внутренний идентификатор фигуры) и префикса (S для Shape, M для главной фигуры, T для шапетипе).</span><span class="sxs-lookup"><span data-stu-id="ffc91-125">If the object model name is not set, then the name is generated using the *Spid* (internal shape ID) plus a prefix (S for shape, M for master shape, T for shapetype).</span></span>

<span data-ttu-id="ffc91-126">*Стандартный атрибут VML*.</span><span class="sxs-lookup"><span data-stu-id="ffc91-126">*VML Standard Attribute*.</span></span>

<span data-ttu-id="ffc91-127">**Пример**</span><span class="sxs-lookup"><span data-stu-id="ffc91-127">**Example**</span></span>

<span data-ttu-id="ffc91-128">Чтобы изменить атрибуты фигуры, необходимо сначала присвоить ей идентификатор. Например, "мирект".</span><span class="sxs-lookup"><span data-stu-id="ffc91-128">To change the attributes of a shape, you must first give the shape an ID; for example, "myrect".</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



<span data-ttu-id="ffc91-129">[Пример атрибута ID](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span><span class="sxs-lookup"><span data-stu-id="ffc91-129">[ID Attribute Example](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span></span> <span data-ttu-id="ffc91-130">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="ffc91-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 