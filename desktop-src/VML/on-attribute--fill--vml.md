---
title: Атрибут on (Fill) (VML)
description: Атрибут on (Fill) (VML)
ms.assetid: 9b7d42e5-4fd9-402d-8d1f-af01f6577475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e25e805be23b4678b1be828b711365a8624f10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691630"
---
# <a name="on-attribute-fillvml"></a><span data-ttu-id="cb901-103">Атрибут on (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="cb901-103">On Attribute (Fill)(VML)</span></span>

<span data-ttu-id="cb901-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cb901-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cb901-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="cb901-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cb901-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="cb901-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cb901-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cb901-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cb901-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cb901-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cb901-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cb901-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cb901-110">Определяет, будет ли отображаться заливка.</span><span class="sxs-lookup"><span data-stu-id="cb901-110">Determines whether the fill will be displayed.</span></span> <span data-ttu-id="cb901-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="cb901-111">Read/write.</span></span> <span data-ttu-id="cb901-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="cb901-112">**VgTriState**.</span></span>

<span data-ttu-id="cb901-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="cb901-113">**Applies To**</span></span>

[<span data-ttu-id="cb901-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="cb901-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="cb901-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="cb901-115">**Tag Syntax**</span></span>

<span data-ttu-id="cb901-116"><v: *element* on = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="cb901-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="cb901-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="cb901-117">**Script Syntax**</span></span>

<span data-ttu-id="cb901-118">*element* . on = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="cb901-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="cb901-119">*выражение* = *element*. on</span><span class="sxs-lookup"><span data-stu-id="cb901-119">*expression*=*element*.on</span></span>

<span data-ttu-id="cb901-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="cb901-120">**Remarks**</span></span>

<span data-ttu-id="cb901-121">Если **значение равно false**, заливка не отображается.</span><span class="sxs-lookup"><span data-stu-id="cb901-121">If **False**, the fill is not displayed.</span></span> <span data-ttu-id="cb901-122">Значение по умолчанию равно **True**.</span><span class="sxs-lookup"><span data-stu-id="cb901-122">The default is **True**.</span></span>

<span data-ttu-id="cb901-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="cb901-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="cb901-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="cb901-124">**Example**</span></span>

<span data-ttu-id="cb901-125">Несмотря на то, что заливка определена как красная, она не отображается.</span><span class="sxs-lookup"><span data-stu-id="cb901-125">Even though the fill is defined to be red, it is not displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" on="False"/>
   </v:shape>
```



 

 