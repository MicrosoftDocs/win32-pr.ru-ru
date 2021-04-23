---
title: Атрибут Филлок VML
description: Атрибут Филлок VML
ms.assetid: 6855544d-0f12-4e21-8101-1bbf45795777
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667524be103b7c641643a52a85368a82a1289e5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339177"
---
# <a name="vml-fillok-attribute"></a><span data-ttu-id="f5ca0-103">Атрибут Филлок VML</span><span class="sxs-lookup"><span data-stu-id="f5ca0-103">VML FillOK Attribute</span></span>

<span data-ttu-id="f5ca0-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f5ca0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f5ca0-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="f5ca0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f5ca0-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="f5ca0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f5ca0-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f5ca0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f5ca0-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f5ca0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f5ca0-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f5ca0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f5ca0-110">Определяет, будет ли отображаться заливка.</span><span class="sxs-lookup"><span data-stu-id="f5ca0-110">Determines whether a fill will be displayed.</span></span> <span data-ttu-id="f5ca0-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="f5ca0-111">Read/write.</span></span> <span data-ttu-id="f5ca0-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="f5ca0-112">**VgTriState**.</span></span>

<span data-ttu-id="f5ca0-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="f5ca0-113">**Applies To**</span></span>

[<span data-ttu-id="f5ca0-114">Путь</span><span class="sxs-lookup"><span data-stu-id="f5ca0-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="f5ca0-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="f5ca0-115">**Tag Syntax**</span></span>

<span data-ttu-id="f5ca0-116"><v: *element* филлок = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="f5ca0-116"><v: *element* fillok=" *expression* "></span></span>

<span data-ttu-id="f5ca0-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="f5ca0-117">**Script Syntax**</span></span>

<span data-ttu-id="f5ca0-118">*element* . филлок = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="f5ca0-118">*element* .fillok="*expression*"</span></span>

<span data-ttu-id="f5ca0-119">*выражение* = *element*. филлок</span><span class="sxs-lookup"><span data-stu-id="f5ca0-119">*expression*=*element*.fillok</span></span>

<span data-ttu-id="f5ca0-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="f5ca0-120">**Remarks**</span></span>

<span data-ttu-id="f5ca0-121">Если **значение равно false**, то путь не может быть заполнен.</span><span class="sxs-lookup"><span data-stu-id="f5ca0-121">If **False**, the path cannot be filled.</span></span> <span data-ttu-id="f5ca0-122">Значение по умолчанию равно **True**.</span><span class="sxs-lookup"><span data-stu-id="f5ca0-122">The default is **True**.</span></span> <span data-ttu-id="f5ca0-123">Этот атрибут переопределяет все остальные атрибуты заливки в родительском элементе или элементе **Fill** .</span><span class="sxs-lookup"><span data-stu-id="f5ca0-123">This attribute overrides all other fill attributes in the parent or **Fill** element.</span></span>

<span data-ttu-id="f5ca0-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="f5ca0-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="f5ca0-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="f5ca0-125">**Example**</span></span>

<span data-ttu-id="f5ca0-126">Путь не будет заполнен.</span><span class="sxs-lookup"><span data-stu-id="f5ca0-126">The path will not be filled.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" fillok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 