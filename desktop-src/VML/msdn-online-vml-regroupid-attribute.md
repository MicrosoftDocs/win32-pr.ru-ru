---
title: Атрибут Реграупид VML
description: Атрибут Реграупид VML
ms.assetid: 2fbcc8c5-6e31-4301-9fb8-c2618bb17a1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384703d3fc5675013de09c4e3b5dec7505cf4164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413077"
---
# <a name="vml-regroupid-attribute"></a><span data-ttu-id="1d7f1-103">Атрибут Реграупид VML</span><span class="sxs-lookup"><span data-stu-id="1d7f1-103">VML ReGroupID Attribute</span></span>

<span data-ttu-id="1d7f1-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1d7f1-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1d7f1-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1d7f1-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1d7f1-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1d7f1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1d7f1-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1d7f1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1d7f1-110">Определяет предыдущую группу для фигуры.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-110">Defines a previous group for a shape.</span></span> <span data-ttu-id="1d7f1-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-111">Read/write.</span></span> <span data-ttu-id="1d7f1-112">**Вгинтежер**.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-112">**VgInteger**.</span></span>

<span data-ttu-id="1d7f1-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="1d7f1-113">**Applies To**</span></span>

[<span data-ttu-id="1d7f1-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="1d7f1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="1d7f1-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="1d7f1-115">**Tag Syntax**</span></span>

<span data-ttu-id="1d7f1-116"><v: *element* о:реграупид = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="1d7f1-116"><v: *element* o:regroupid=" *expression* "></span></span>

<span data-ttu-id="1d7f1-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="1d7f1-117">**Remarks**</span></span>

<span data-ttu-id="1d7f1-118">ИДЕНТИФИКАЦИОНный номер используется для идентификации групп фигур, которые больше не группируются.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-118">An ID number is used to identify groups of shapes that are no longer grouped.</span></span> <span data-ttu-id="1d7f1-119">Позволяет программно перегруппировку фигур.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-119">Allows shapes to be regrouped programmatically.</span></span>

<span data-ttu-id="1d7f1-120">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="1d7f1-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="1d7f1-121">**Пример**</span><span class="sxs-lookup"><span data-stu-id="1d7f1-121">**Example**</span></span>

<span data-ttu-id="1d7f1-122">Фигура была частью группы, обозначенной ИДЕНТИФИКАТОРом группы 040754.</span><span class="sxs-lookup"><span data-stu-id="1d7f1-122">The shape was part of a group denoted by the group ID 040754.</span></span>


```HTML
   <v:shape id="rect01" ReGroupID="040754"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 