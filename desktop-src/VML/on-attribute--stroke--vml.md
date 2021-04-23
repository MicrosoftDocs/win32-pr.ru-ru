---
title: Атрибут on (Stroke) (VML)
description: Атрибут on (Stroke) (VML)
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e418857db22ee1ac12a35e9b81840b89e06c00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691601"
---
# <a name="on-attribute-strokevml"></a><span data-ttu-id="71f4a-103">Атрибут on (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="71f4a-103">On Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="71f4a-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="71f4a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="71f4a-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="71f4a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="71f4a-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="71f4a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="71f4a-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71f4a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="71f4a-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="71f4a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="71f4a-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="71f4a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="71f4a-110">Определяет, будет ли отображаться штрих.</span><span class="sxs-lookup"><span data-stu-id="71f4a-110">Determines whether the stroke will be displayed.</span></span> <span data-ttu-id="71f4a-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="71f4a-111">Read/write.</span></span> <span data-ttu-id="71f4a-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="71f4a-112">**VgTriState**.</span></span>

<span data-ttu-id="71f4a-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="71f4a-113">**Applies To**</span></span>

[<span data-ttu-id="71f4a-114">Водок</span><span class="sxs-lookup"><span data-stu-id="71f4a-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="71f4a-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="71f4a-115">**Tag Syntax**</span></span>

<span data-ttu-id="71f4a-116"><v: *element* on = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="71f4a-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="71f4a-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="71f4a-117">**Script Syntax**</span></span>

<span data-ttu-id="71f4a-118">*element* . on = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="71f4a-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="71f4a-119">*выражение* = *element*. on</span><span class="sxs-lookup"><span data-stu-id="71f4a-119">*expression*=*element*.on</span></span>

<span data-ttu-id="71f4a-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="71f4a-120">**Remarks**</span></span>

<span data-ttu-id="71f4a-121">Если **значение равно false**, штрих не отображается.</span><span class="sxs-lookup"><span data-stu-id="71f4a-121">If **False**, the stroke is not displayed.</span></span> <span data-ttu-id="71f4a-122">Значение по умолчанию равно **True**.</span><span class="sxs-lookup"><span data-stu-id="71f4a-122">The default is **True**.</span></span>

<span data-ttu-id="71f4a-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="71f4a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="71f4a-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="71f4a-124">**Example**</span></span>

<span data-ttu-id="71f4a-125">Штрих не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="71f4a-125">The stroke will not be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 