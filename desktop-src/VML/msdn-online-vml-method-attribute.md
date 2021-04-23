---
title: Атрибут метода VML
description: Атрибут метода VML
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691604"
---
# <a name="vml-method-attribute"></a><span data-ttu-id="807bb-103">Атрибут метода VML</span><span class="sxs-lookup"><span data-stu-id="807bb-103">VML Method Attribute</span></span>

<span data-ttu-id="807bb-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="807bb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="807bb-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="807bb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="807bb-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="807bb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="807bb-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="807bb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="807bb-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="807bb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="807bb-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="807bb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="807bb-110">Определяет метод, используемый для создания градиентной заливки.</span><span class="sxs-lookup"><span data-stu-id="807bb-110">Defines the method used to generate a gradient fill.</span></span> <span data-ttu-id="807bb-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="807bb-111">Read/write.</span></span> <span data-ttu-id="807bb-112">**Вгсигматипе**.</span><span class="sxs-lookup"><span data-stu-id="807bb-112">**VgSigmaType**.</span></span>

<span data-ttu-id="807bb-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="807bb-113">**Applies To**</span></span>

[<span data-ttu-id="807bb-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="807bb-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="807bb-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="807bb-115">**Tag Syntax**</span></span>

<span data-ttu-id="807bb-116"><v: *element* method = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="807bb-116"><v: *element* method=" *expression* "></span></span>

<span data-ttu-id="807bb-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="807bb-117">**Script Syntax**</span></span>

<span data-ttu-id="807bb-118">*element* . Method = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="807bb-118">*element* .method="*expression*"</span></span>

<span data-ttu-id="807bb-119">*выражение* = *element*. Method</span><span class="sxs-lookup"><span data-stu-id="807bb-119">*expression*=*element*.method</span></span>

<span data-ttu-id="807bb-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="807bb-120">**Remarks**</span></span>

<span data-ttu-id="807bb-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="807bb-121">Values include:</span></span>



| <span data-ttu-id="807bb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="807bb-122">Value</span></span>  | <span data-ttu-id="807bb-123">Описание</span><span class="sxs-lookup"><span data-stu-id="807bb-123">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="807bb-124">Нет</span><span class="sxs-lookup"><span data-stu-id="807bb-124">None</span></span>   | <span data-ttu-id="807bb-125">Заполнение без сигм.</span><span class="sxs-lookup"><span data-stu-id="807bb-125">No sigma fill.</span></span>       |
| <span data-ttu-id="807bb-126">Линейная</span><span class="sxs-lookup"><span data-stu-id="807bb-126">Linear</span></span> | <span data-ttu-id="807bb-127">Заливка линейной Сигма.</span><span class="sxs-lookup"><span data-stu-id="807bb-127">Linear sigma fill.</span></span>   |
| <span data-ttu-id="807bb-128">Sigma</span><span class="sxs-lookup"><span data-stu-id="807bb-128">Sigma</span></span>  | <span data-ttu-id="807bb-129">Сигма (Заливка).</span><span class="sxs-lookup"><span data-stu-id="807bb-129">Sigma fill.</span></span> <span data-ttu-id="807bb-130">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="807bb-130">Default.</span></span> |
| <span data-ttu-id="807bb-131">Любой</span><span class="sxs-lookup"><span data-stu-id="807bb-131">Any</span></span>    | <span data-ttu-id="807bb-132">Любое заполнение Сигма.</span><span class="sxs-lookup"><span data-stu-id="807bb-132">Any sigma fill.</span></span>      |



 

<span data-ttu-id="807bb-133">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="807bb-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="807bb-134">**Пример**</span><span class="sxs-lookup"><span data-stu-id="807bb-134">**Example**</span></span>

<span data-ttu-id="807bb-135">Фигура будет иметь красную линейную градиентную заливку.</span><span class="sxs-lookup"><span data-stu-id="807bb-135">The shape will have a red linear gradient fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 