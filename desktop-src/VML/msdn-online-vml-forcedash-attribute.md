---
title: Атрибут Форцедаш VML
description: Атрибут Форцедаш VML
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070314"
---
# <a name="vml-forcedash-attribute"></a><span data-ttu-id="576f1-103">Атрибут Форцедаш VML</span><span class="sxs-lookup"><span data-stu-id="576f1-103">VML ForceDash Attribute</span></span>

<span data-ttu-id="576f1-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="576f1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="576f1-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="576f1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="576f1-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="576f1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="576f1-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="576f1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="576f1-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="576f1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="576f1-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="576f1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="576f1-110">Определяет, используется ли пунктирная структура для рисования фигуры, если фигура не имеет линии или заливки.</span><span class="sxs-lookup"><span data-stu-id="576f1-110">Determines whether a dashed outline is used to draw a shape when a shape has no line or fill.</span></span> <span data-ttu-id="576f1-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="576f1-111">Read/write.</span></span> <span data-ttu-id="576f1-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="576f1-112">**VgTriState**.</span></span>

<span data-ttu-id="576f1-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="576f1-113">**Applies To**</span></span>

[<span data-ttu-id="576f1-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="576f1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="576f1-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="576f1-115">**Tag Syntax**</span></span>

<span data-ttu-id="576f1-116"><v: *element* о:форцедаш = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="576f1-116"><v: *element* o:forcedash=" *expression* "></span></span>

<span data-ttu-id="576f1-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="576f1-117">**Remarks**</span></span>

<span data-ttu-id="576f1-118">Используется заполнителями Microsoft PowerPoint для рисования пунктирного контура, если нет линий и заливка для фигуры.</span><span class="sxs-lookup"><span data-stu-id="576f1-118">Used by Microsoft PowerPoint placeholders to draw a dashed outline when there is no line and no fill for a shape.</span></span> <span data-ttu-id="576f1-119">Значение по умолчанию — **False**.</span><span class="sxs-lookup"><span data-stu-id="576f1-119">Default is **False**.</span></span> <span data-ttu-id="576f1-120">Если **значение равно true**, то для обозначения заполнителя будет использоваться пунктирная структура.</span><span class="sxs-lookup"><span data-stu-id="576f1-120">If **True**, a dashed outline will be used to indicate a placeholder.</span></span>

<span data-ttu-id="576f1-121">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="576f1-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="576f1-122">**Пример**</span><span class="sxs-lookup"><span data-stu-id="576f1-122">**Example**</span></span>

<span data-ttu-id="576f1-123">Пунктирная линия будет использоваться для отрисовки фигуры при отсутствии линии или заливки.</span><span class="sxs-lookup"><span data-stu-id="576f1-123">A dashed line will be used to render the shape if there is no line or fill.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 