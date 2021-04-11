---
title: Объект страница свойств
description: Объект страница свойств
ms.assetid: 9d15d198-a4fe-4c05-a7be-0807a179cd9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ae4ded2625440ba34170df605b60287f105800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132907"
---
# <a name="the-propertysheet-object"></a><span data-ttu-id="eae8c-103">Объект страница свойств</span><span class="sxs-lookup"><span data-stu-id="eae8c-103">The PropertySheet Object</span></span>

<span data-ttu-id="eae8c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eae8c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="eae8c-105">Объект [**Страница свойств**](https://www.bing.com/search?q=**PropertySheet**) предоставляет несколько свойств, которые можно использовать, если требуется манипулировать символом относительно страницы свойств Microsoft Agent (также известной как окно дополнительных параметров символов).</span><span class="sxs-lookup"><span data-stu-id="eae8c-105">The [**PropertySheet**](https://www.bing.com/search?q=**PropertySheet**) object provides several properties you can use if you want to manipulate the character relative to the Microsoft Agent property sheet (also known as the Advanced Character Options window).</span></span>

-   [<span data-ttu-id="eae8c-106">**Высота**</span><span class="sxs-lookup"><span data-stu-id="eae8c-106">**Height**</span></span>](height-property-pso.md)
-   [<span data-ttu-id="eae8c-107">**Слева**</span><span class="sxs-lookup"><span data-stu-id="eae8c-107">**Left**</span></span>](left-property-pso.md)
-   [<span data-ttu-id="eae8c-108">**Страниц**</span><span class="sxs-lookup"><span data-stu-id="eae8c-108">**Page**</span></span>](page-property.md)
-   [<span data-ttu-id="eae8c-109">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eae8c-109">**Top**</span></span>](top-property-pso.md)
-   [<span data-ttu-id="eae8c-110">**Visible**</span><span class="sxs-lookup"><span data-stu-id="eae8c-110">**Visible**</span></span>](visible-property.md)
-   [<span data-ttu-id="eae8c-111">**Ширина**</span><span class="sxs-lookup"><span data-stu-id="eae8c-111">**Width**</span></span>](width-property-pso.md)

<span data-ttu-id="eae8c-112">Если вы запрашиваете свойства [**высоты**](height-property-pso.md), [**левого**](left-property-pso.md), [**верхнего**](top-property-pso.md)и [**ширины**](width-property-pso.md) до того, как страница свойств когда-либо отображалась, их значения возвращаются как нули (0).</span><span class="sxs-lookup"><span data-stu-id="eae8c-112">If you query [**Height**](height-property-pso.md), [**Left**](left-property-pso.md), [**Top**](top-property-pso.md), and [**Width**](width-property-pso.md) properties before the property sheet has ever been shown, their values return as zero (0).</span></span> <span data-ttu-id="eae8c-113">После отображения эти свойства возвращают последнюю расположение и размер окна (относительно текущего разрешения экрана).</span><span class="sxs-lookup"><span data-stu-id="eae8c-113">Once shown, these properties return the last position and size of the window (relative to your current screen resolution).</span></span>

 

 




