---
title: Атрибут color2 (shadow) (VML)
description: Атрибут color2 (shadow) (VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e735d7672457153881d384c7b625199cf4a202e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793045"
---
# <a name="color2-attribute-shadowvml"></a><span data-ttu-id="13f78-103">Атрибут color2 (shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="13f78-103">Color2 Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="13f78-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="13f78-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="13f78-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="13f78-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="13f78-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="13f78-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="13f78-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="13f78-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="13f78-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="13f78-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="13f78-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="13f78-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="13f78-110">Определяет второй цвет тени.</span><span class="sxs-lookup"><span data-stu-id="13f78-110">Defines the second color of a shadow.</span></span> <span data-ttu-id="13f78-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="13f78-111">Read/write.</span></span> <span data-ttu-id="13f78-112">**Вгколор**.</span><span class="sxs-lookup"><span data-stu-id="13f78-112">**VgColor**.</span></span>

<span data-ttu-id="13f78-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="13f78-113">**Applies To**</span></span>

[<span data-ttu-id="13f78-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="13f78-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="13f78-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="13f78-115">**Tag Syntax**</span></span>

<span data-ttu-id="13f78-116"><v: *element* color2 = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="13f78-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="13f78-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="13f78-117">**Script Syntax**</span></span>

<span data-ttu-id="13f78-118">*element* . color2 = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="13f78-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="13f78-119">*выражение* = *element*. color2</span><span class="sxs-lookup"><span data-stu-id="13f78-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="13f78-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="13f78-120">**Remarks**</span></span>

<span data-ttu-id="13f78-121">Используйте второй цвет для создания специальных эффектов тени.</span><span class="sxs-lookup"><span data-stu-id="13f78-121">Use a second color to create special shadow effects.</span></span> <span data-ttu-id="13f78-122">Дополнительные сведения о втором цветах см. в описании атрибута [Type](type-attribute--shadow--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="13f78-122">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second colors.</span></span>

<span data-ttu-id="13f78-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="13f78-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="13f78-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="13f78-124">**Example**</span></span>

<span data-ttu-id="13f78-125">Тень имеет синий цвет для второго цвета.</span><span class="sxs-lookup"><span data-stu-id="13f78-125">The shadow has blue for a second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 