---
title: Атрибут ID (Вмлфраме) (VML)
description: Атрибут ID (Вмлфраме) (VML)
ms.assetid: 3580fad7-b49e-44d7-b266-90fbfc2a02c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f9c5254a2dca186651bb49b677febe747f37c4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070218"
---
# <a name="id-attribute-vmlframevml"></a><span data-ttu-id="6c655-103">Атрибут ID (Вмлфраме) (VML)</span><span class="sxs-lookup"><span data-stu-id="6c655-103">ID Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="6c655-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6c655-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6c655-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="6c655-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6c655-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="6c655-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6c655-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6c655-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6c655-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6c655-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6c655-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6c655-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6c655-110">Определяет уникальный идентификатор для кадра.</span><span class="sxs-lookup"><span data-stu-id="6c655-110">Defines a unique identifier for the frame.</span></span> <span data-ttu-id="6c655-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="6c655-111">Read/write.</span></span> <span data-ttu-id="6c655-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="6c655-112">**String**.</span></span>

<span data-ttu-id="6c655-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="6c655-113">**Applies To**</span></span>

[<span data-ttu-id="6c655-114">вмлфраме</span><span class="sxs-lookup"><span data-stu-id="6c655-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="6c655-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="6c655-115">**Tag Syntax**</span></span>

<span data-ttu-id="6c655-116"><v: *element* ID = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="6c655-116"><v: *element* ID=" *expression* "></span></span>

<span data-ttu-id="6c655-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="6c655-117">**Script Syntax**</span></span>

<span data-ttu-id="6c655-118">*element* . ID = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="6c655-118">*element* .ID="*expression*"</span></span>

<span data-ttu-id="6c655-119">*выражение* = *element*. ID</span><span class="sxs-lookup"><span data-stu-id="6c655-119">*expression*=*element*.ID</span></span>

<span data-ttu-id="6c655-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="6c655-120">**Remarks**</span></span>

<span data-ttu-id="6c655-121">Используйте **идентификатор** для ссылки на кадр.</span><span class="sxs-lookup"><span data-stu-id="6c655-121">Use **ID** to reference a frame.</span></span> <span data-ttu-id="6c655-122">Например, можно переместить фрейм вокруг страницы, изменив положение кадра, на которое ссылается **идентификатор**.</span><span class="sxs-lookup"><span data-stu-id="6c655-122">For example, you can move the frame around on the page by changing the frame position referenced by the **ID**.</span></span>

<span data-ttu-id="6c655-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="6c655-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="6c655-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="6c655-124">**Example**</span></span>

<span data-ttu-id="6c655-125">**Идентификатор** кадра — "frame01".</span><span class="sxs-lookup"><span data-stu-id="6c655-125">The **ID** of the frame is "frame01".</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 