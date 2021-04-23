---
title: Элемент Шапетипе VML
description: Элемент Шапетипе VML
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260910"
---
# <a name="vml-shapetype-element"></a><span data-ttu-id="300a4-103">Элемент Шапетипе VML</span><span class="sxs-lookup"><span data-stu-id="300a4-103">VML ShapeType Element</span></span>

<span data-ttu-id="300a4-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="300a4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="300a4-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="300a4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="300a4-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="300a4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="300a4-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="300a4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="300a4-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="300a4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="300a4-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="300a4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="300a4-110">Определяет фигуру, которую можно использовать для создания других фигур.</span><span class="sxs-lookup"><span data-stu-id="300a4-110">Defines a shape that can be used to create other shapes.</span></span>

<span data-ttu-id="300a4-111">Следующий атрибут изменяет **шапетипе**.</span><span class="sxs-lookup"><span data-stu-id="300a4-111">The following attribute modifies a **ShapeType**.</span></span>



| <span data-ttu-id="300a4-112">attribute</span><span class="sxs-lookup"><span data-stu-id="300a4-112">Attribute</span></span>                                      | <span data-ttu-id="300a4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="300a4-113">Description</span></span>                                             |
|------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="300a4-114">Master</span><span class="sxs-lookup"><span data-stu-id="300a4-114">Master</span></span>](msdn-online-vml-master-attribute.md) | <span data-ttu-id="300a4-115">Определяет, является ли **шапетипе** главным элементом.</span><span class="sxs-lookup"><span data-stu-id="300a4-115">Determines whether a **ShapeType** is a master element.</span></span> |



 

<span data-ttu-id="300a4-116">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="300a4-116">**Remarks**</span></span>

<span data-ttu-id="300a4-117">**Шапетипе** идентичен элементу **Shape** , за исключением того, что он не может ссылаться на другой элемент **шапетипе** .</span><span class="sxs-lookup"><span data-stu-id="300a4-117">**ShapeType** is identical to the **Shape** element except it cannot reference another **ShapeType** element.</span></span>

<span data-ttu-id="300a4-118">Если элемент **Shape** ссылается на **шапетипе**, **фигура** может дублировать некоторые свойства, уже указанные в **шапетипе**.</span><span class="sxs-lookup"><span data-stu-id="300a4-118">When a **Shape** element makes reference to a **ShapeType**, the **Shape** may duplicate some of the properties that have already been specified in the **ShapeType**.</span></span> <span data-ttu-id="300a4-119">В этих случаях атрибуты в **фигуре** переопределяют значения **шапетипе**.</span><span class="sxs-lookup"><span data-stu-id="300a4-119">In these cases, the attributes in the **Shape** override those of the **ShapeType**.</span></span>

<span data-ttu-id="300a4-120">Атрибут **Type** не может использоваться с **шапетипе**.</span><span class="sxs-lookup"><span data-stu-id="300a4-120">The **Type** attribute may not be used with **ShapeType**.</span></span>

<span data-ttu-id="300a4-121">Атрибуты позиционирования CSS (например, " **Top**", " **Left**" и т. д.) не передаются в **фигуру** из **шапетипе**.</span><span class="sxs-lookup"><span data-stu-id="300a4-121">CSS positioning attributes (such as **Top**, **Left**, etc.) are not passed to a **Shape** from a **ShapeType**.</span></span>

<span data-ttu-id="300a4-122">Чтобы использовать этот элемент, создайте **шапетипе** с указанным атрибутом [ID](id-attribute--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="300a4-122">To use this element, create a **ShapeType** with a specific [ID](id-attribute--vml.md) attribute.</span></span> <span data-ttu-id="300a4-123">Затем создайте **фигуру** и сослаться на **шапетипе** с помощью атрибута **Type** .</span><span class="sxs-lookup"><span data-stu-id="300a4-123">Then create a **Shape** and reference the **ShapeType** with the **Type** attribute.</span></span> <span data-ttu-id="300a4-124">Дополнительные сведения см. в описании атрибута [Type](type-attribute--shape--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="300a4-124">See the [Type](type-attribute--shape--vml.md) attribute for more information.</span></span>

 

 