---
title: Атрибут высоты VML V-and-Letter
description: Атрибут высоты VML V-and-Letter
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791971"
---
# <a name="vml-v-same-letter-heights-attribute"></a><span data-ttu-id="10810-103">Атрибут высоты VML V-and-Letter</span><span class="sxs-lookup"><span data-stu-id="10810-103">VML V-Same-Letter-Heights Attribute</span></span>

<span data-ttu-id="10810-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="10810-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="10810-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="10810-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="10810-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="10810-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="10810-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="10810-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="10810-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="10810-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="10810-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="10810-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="10810-110">Определяет, будут ли все буквы иметь одинаковую высоту независимо от начального варианта.</span><span class="sxs-lookup"><span data-stu-id="10810-110">Determines whether all letters will be the same height regardless of initial case.</span></span> <span data-ttu-id="10810-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="10810-111">Read/write.</span></span> <span data-ttu-id="10810-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="10810-112">**VgTriState**.</span></span>

<span data-ttu-id="10810-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="10810-113">**Applies To**</span></span>

[<span data-ttu-id="10810-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="10810-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="10810-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="10810-115">**Tag Syntax**</span></span>

<span data-ttu-id="10810-116"><v: Style *элемента* = "v-та же буква-высота: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="10810-116"><v: *element* style="v-same-letter-heights: *expression* "></span></span>

<span data-ttu-id="10810-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="10810-117">**Script Syntax**</span></span>

<span data-ttu-id="10810-118">*element* . Style. v-та же самая буква-высота = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="10810-118">*element* .style.v-same-letter-heights="*expression*"</span></span>

<span data-ttu-id="10810-119">*выражение* = Высота *элемента*. Style. v-та же буква</span><span class="sxs-lookup"><span data-stu-id="10810-119">*expression*=*element*.style.v-same-letter-heights</span></span>

<span data-ttu-id="10810-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="10810-120">**Remarks**</span></span>

<span data-ttu-id="10810-121">Если **значение равно true**, буквы в нижнем регистре растягиваются до высоты прописных букв.</span><span class="sxs-lookup"><span data-stu-id="10810-121">If **True**, the lowercase letters are stretched to the height of the uppercase letters.</span></span> <span data-ttu-id="10810-122">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="10810-122">The default value is **False**.</span></span>

<span data-ttu-id="10810-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="10810-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="10810-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="10810-124">**Example**</span></span>

<span data-ttu-id="10810-125">Все буквы будут одинаковой высотой, независимо от регистра.</span><span class="sxs-lookup"><span data-stu-id="10810-125">All letters will be the same height, regardless of case.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 