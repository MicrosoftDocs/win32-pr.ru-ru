---
title: Атрибут on (Текстпас) (VML)
description: Атрибут on (Текстпас) (VML)
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ae791b1144046a1c29e92d11663cd15d696bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533476"
---
# <a name="on-attribute-textpathvml"></a><span data-ttu-id="7e95b-103">Атрибут on (Текстпас) (VML)</span><span class="sxs-lookup"><span data-stu-id="7e95b-103">On Attribute (TextPath)(VML)</span></span>

<span data-ttu-id="7e95b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7e95b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7e95b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="7e95b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7e95b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="7e95b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7e95b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7e95b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7e95b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7e95b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7e95b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7e95b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7e95b-110">Определяет, отображается ли текст.</span><span class="sxs-lookup"><span data-stu-id="7e95b-110">Defines whether the text is displayed.</span></span> <span data-ttu-id="7e95b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="7e95b-111">Read/write.</span></span> <span data-ttu-id="7e95b-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="7e95b-112">**VgTriState**.</span></span>

<span data-ttu-id="7e95b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="7e95b-113">**Applies To**</span></span>

[<span data-ttu-id="7e95b-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="7e95b-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="7e95b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="7e95b-115">**Tag Syntax**</span></span>

<span data-ttu-id="7e95b-116"><v: *element* on = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="7e95b-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="7e95b-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="7e95b-117">**Script Syntax**</span></span>

<span data-ttu-id="7e95b-118">*element* . on = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="7e95b-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="7e95b-119">*выражение* = *element*. on</span><span class="sxs-lookup"><span data-stu-id="7e95b-119">*expression*=*element*.on</span></span>

<span data-ttu-id="7e95b-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="7e95b-120">**Remarks**</span></span>

<span data-ttu-id="7e95b-121">Значение по умолчанию — **False**.</span><span class="sxs-lookup"><span data-stu-id="7e95b-121">Default is **False**.</span></span> <span data-ttu-id="7e95b-122">Это значение должно быть равно **true** , чтобы отображать текст на текстовом пути.</span><span class="sxs-lookup"><span data-stu-id="7e95b-122">This value must be set to **True** to display text on a text path.</span></span>

<span data-ttu-id="7e95b-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="7e95b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="7e95b-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="7e95b-124">**Example**</span></span>

<span data-ttu-id="7e95b-125">Отобразится текст для текстового пути.</span><span class="sxs-lookup"><span data-stu-id="7e95b-125">The text on the text path will be displayed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 