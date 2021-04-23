---
title: Атрибут Колормоде VML
description: Атрибут Колормоде VML
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7126a3f5a95910eb85007fe9a80d500c5233e5e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413178"
---
# <a name="vml-colormode-attribute"></a><span data-ttu-id="afe16-103">Атрибут Колормоде VML</span><span class="sxs-lookup"><span data-stu-id="afe16-103">VML ColorMode Attribute</span></span>

<span data-ttu-id="afe16-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="afe16-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="afe16-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="afe16-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="afe16-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="afe16-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="afe16-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="afe16-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="afe16-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="afe16-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="afe16-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="afe16-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="afe16-110">Определяет режим цвета объемной фигуры.</span><span class="sxs-lookup"><span data-stu-id="afe16-110">Determines the mode of extrusion color.</span></span> <span data-ttu-id="afe16-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="afe16-111">Read/write.</span></span> <span data-ttu-id="afe16-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="afe16-112">**VgTriState**.</span></span>

<span data-ttu-id="afe16-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="afe16-113">**Applies To**</span></span>

[<span data-ttu-id="afe16-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="afe16-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="afe16-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="afe16-115">**Tag Syntax**</span></span>

<span data-ttu-id="afe16-116"><o: *element* колормоде = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="afe16-116"><o: *element* colormode=" *expression* "></span></span>

<span data-ttu-id="afe16-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="afe16-117">**Script Syntax**</span></span>

<span data-ttu-id="afe16-118">*element* . колормоде = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="afe16-118">*element* .colormode="*expression*"</span></span>

<span data-ttu-id="afe16-119">*выражение* = *element*. колормоде</span><span class="sxs-lookup"><span data-stu-id="afe16-119">*expression*=*element*.colormode</span></span>

<span data-ttu-id="afe16-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="afe16-120">**Remarks**</span></span>

<span data-ttu-id="afe16-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="afe16-121">Values include:</span></span>



| <span data-ttu-id="afe16-122">Значение</span><span class="sxs-lookup"><span data-stu-id="afe16-122">Value</span></span>  | <span data-ttu-id="afe16-123">Описание</span><span class="sxs-lookup"><span data-stu-id="afe16-123">Description</span></span>                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afe16-124">auto</span><span class="sxs-lookup"><span data-stu-id="afe16-124">auto</span></span>   | <span data-ttu-id="afe16-125">Указывает, что цвет объема совпадает с цветом заливки фигуры.</span><span class="sxs-lookup"><span data-stu-id="afe16-125">Specifies that the color of the extrusion is the same as the fill color of the shape.</span></span> <span data-ttu-id="afe16-126">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="afe16-126">Default.</span></span>                |
| <span data-ttu-id="afe16-127">пользовательский</span><span class="sxs-lookup"><span data-stu-id="afe16-127">custom</span></span> | <span data-ttu-id="afe16-128">Указывает, что объемом будет цвет атрибута [цвета](color-attribute--extrusion--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="afe16-128">Specifies that the extrusion will be the color of the [Color](color-attribute--extrusion--vml.md) attribute.</span></span> |



 

<span data-ttu-id="afe16-129">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="afe16-129">*Microsoft Office Extensions Attribute*</span></span>

 

 