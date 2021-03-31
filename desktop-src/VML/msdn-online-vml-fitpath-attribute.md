---
title: Атрибут Фитпас VML
description: Атрибут Фитпас VML
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1805e59a50c63248ed936f6a849869057a34a6e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104261007"
---
# <a name="vml-fitpath-attribute"></a><span data-ttu-id="ad1e6-103">Атрибут Фитпас VML</span><span class="sxs-lookup"><span data-stu-id="ad1e6-103">VML FitPath Attribute</span></span>

<span data-ttu-id="ad1e6-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ad1e6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ad1e6-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ad1e6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ad1e6-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ad1e6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ad1e6-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad1e6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ad1e6-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ad1e6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ad1e6-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ad1e6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ad1e6-110">Определяет, соответствует ли текст контуру фигуры.</span><span class="sxs-lookup"><span data-stu-id="ad1e6-110">Defines whether the text fits the path of a shape.</span></span> <span data-ttu-id="ad1e6-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="ad1e6-111">Read/write.</span></span> <span data-ttu-id="ad1e6-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="ad1e6-112">**VgTriState**.</span></span>

<span data-ttu-id="ad1e6-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="ad1e6-113">**Applies To**</span></span>

[<span data-ttu-id="ad1e6-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="ad1e6-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="ad1e6-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="ad1e6-115">**Tag Syntax**</span></span>

<span data-ttu-id="ad1e6-116"><v: *element* фитпас = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="ad1e6-116"><v: *element* fitpath=" *expression* "></span></span>

<span data-ttu-id="ad1e6-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="ad1e6-117">**Script Syntax**</span></span>

<span data-ttu-id="ad1e6-118">*element* . фитпас = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="ad1e6-118">*element* .fitpath="*expression*"</span></span>

<span data-ttu-id="ad1e6-119">*выражение* = *element*. фитпас</span><span class="sxs-lookup"><span data-stu-id="ad1e6-119">*expression*=*element*.fitpath</span></span>

<span data-ttu-id="ad1e6-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="ad1e6-120">**Remarks**</span></span>

<span data-ttu-id="ad1e6-121">При **значении true** изменяет размер текста для заполнения пути, на котором он находится.</span><span class="sxs-lookup"><span data-stu-id="ad1e6-121">If **True**, sizes the text to fill the path it lies out on.</span></span> <span data-ttu-id="ad1e6-122">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="ad1e6-122">The default is **False**.</span></span>

<span data-ttu-id="ad1e6-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="ad1e6-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="ad1e6-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="ad1e6-124">**Example**</span></span>

<span data-ttu-id="ad1e6-125">Текст будет соответствовать пути.</span><span class="sxs-lookup"><span data-stu-id="ad1e6-125">The text will fit the path.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitpath="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 