---
title: Атрибут ИНВИ VML
description: Атрибут ИНВИ VML
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338009"
---
# <a name="vml-invy-attribute"></a><span data-ttu-id="6f8b9-103">Атрибут ИНВИ VML</span><span class="sxs-lookup"><span data-stu-id="6f8b9-103">VML InvY Attribute</span></span>

<span data-ttu-id="6f8b9-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6f8b9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6f8b9-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="6f8b9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6f8b9-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="6f8b9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6f8b9-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6f8b9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6f8b9-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6f8b9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6f8b9-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6f8b9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6f8b9-110">Определяет, инвертирована ли координата y маркера.</span><span class="sxs-lookup"><span data-stu-id="6f8b9-110">Determines whether the y position of the handle is inverted.</span></span> <span data-ttu-id="6f8b9-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="6f8b9-111">Read/write.</span></span> <span data-ttu-id="6f8b9-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="6f8b9-112">**VgTriState**.</span></span>

<span data-ttu-id="6f8b9-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="6f8b9-113">**Applies To**</span></span>

<span data-ttu-id="6f8b9-114">[H](msdn-online-vml-h-element.md) (вложенный элемент [дескрипторов](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="6f8b9-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="6f8b9-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="6f8b9-115">**Tag Syntax**</span></span>

<span data-ttu-id="6f8b9-116"><v: *element* ИНВИ = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="6f8b9-116"><v: *element* invy=" *expression* "></span></span>

<span data-ttu-id="6f8b9-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="6f8b9-117">**Remarks**</span></span>

<span data-ttu-id="6f8b9-118">Если **значение равно true**, то y-координата маркера инвертирована путем вычитания значения y из значения y **курдоригин** , добавленного к значению y **курдсизе**.</span><span class="sxs-lookup"><span data-stu-id="6f8b9-118">If **True**, the y position of the handle is inverted by subtracting the y value from the y value of **CoordOrigin** added to the y value of **CoordSize**.</span></span> <span data-ttu-id="6f8b9-119">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="6f8b9-119">The default value is **False**.</span></span>

<span data-ttu-id="6f8b9-120">Этот атрибут эквивалентен</span><span class="sxs-lookup"><span data-stu-id="6f8b9-120">This attribute is the equivalent of</span></span>


```HTML
coordorigin.y + coordsize.y - h.position.y
```



<span data-ttu-id="6f8b9-121">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="6f8b9-121">*VML Standard Attribute*</span></span>

 

 