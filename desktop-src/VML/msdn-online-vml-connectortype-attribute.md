---
title: Атрибут Коннектортипе VML
description: Атрибут Коннектортипе VML
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672295"
---
# <a name="vml-connectortype-attribute"></a><span data-ttu-id="f2163-103">Атрибут Коннектортипе VML</span><span class="sxs-lookup"><span data-stu-id="f2163-103">VML ConnectorType Attribute</span></span>

<span data-ttu-id="f2163-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f2163-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f2163-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="f2163-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f2163-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="f2163-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f2163-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f2163-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f2163-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f2163-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f2163-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f2163-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f2163-110">Указывает тип соединителя, используемого для объединения фигур.</span><span class="sxs-lookup"><span data-stu-id="f2163-110">Indicates the type of connector used for joining shapes.</span></span> <span data-ttu-id="f2163-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="f2163-111">Read/write.</span></span> <span data-ttu-id="f2163-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="f2163-112">**String**.</span></span>

<span data-ttu-id="f2163-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="f2163-113">**Applies To**</span></span>

[<span data-ttu-id="f2163-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="f2163-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f2163-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="f2163-115">**Tag Syntax**</span></span>

<span data-ttu-id="f2163-116"><v: *element* о:коннектортипе = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="f2163-116"><v: *element* o:connectortype=" *expression* "></span></span>

<span data-ttu-id="f2163-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="f2163-117">**Remarks**</span></span>

<span data-ttu-id="f2163-118">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="f2163-118">Values include:</span></span>



| <span data-ttu-id="f2163-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f2163-119">Value</span></span>    | <span data-ttu-id="f2163-120">Описание</span><span class="sxs-lookup"><span data-stu-id="f2163-120">Description</span></span>                    |
|----------|--------------------------------|
| <span data-ttu-id="f2163-121">нет</span><span class="sxs-lookup"><span data-stu-id="f2163-121">none</span></span>     | <span data-ttu-id="f2163-122">Нет соединителя.</span><span class="sxs-lookup"><span data-stu-id="f2163-122">No connector.</span></span>                  |
| <span data-ttu-id="f2163-123">линия</span><span class="sxs-lookup"><span data-stu-id="f2163-123">straight</span></span> | <span data-ttu-id="f2163-124">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2163-124">Default.</span></span> <span data-ttu-id="f2163-125">Прямой соединитель.</span><span class="sxs-lookup"><span data-stu-id="f2163-125">A straight connector.</span></span> |
| <span data-ttu-id="f2163-126">расталкивая</span><span class="sxs-lookup"><span data-stu-id="f2163-126">elbow</span></span>    | <span data-ttu-id="f2163-127">Соединитель с уступом.</span><span class="sxs-lookup"><span data-stu-id="f2163-127">An elbow-shaped connector.</span></span>     |
| <span data-ttu-id="f2163-128">кругл</span><span class="sxs-lookup"><span data-stu-id="f2163-128">curved</span></span>   | <span data-ttu-id="f2163-129">Криволинейный соединитель.</span><span class="sxs-lookup"><span data-stu-id="f2163-129">A curved connector.</span></span>            |



 

<span data-ttu-id="f2163-130">Этот атрибут может также использоваться обработчиком правил графического редактора.</span><span class="sxs-lookup"><span data-stu-id="f2163-130">This attribute may also be used by a rules engine of a graphical editor.</span></span>

<span data-ttu-id="f2163-131">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="f2163-131">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="f2163-132">**Пример**</span><span class="sxs-lookup"><span data-stu-id="f2163-132">**Example**</span></span>

<span data-ttu-id="f2163-133">Фигура использует прямую линию в качестве соединителя.</span><span class="sxs-lookup"><span data-stu-id="f2163-133">The shape uses a straight line as a connector.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 