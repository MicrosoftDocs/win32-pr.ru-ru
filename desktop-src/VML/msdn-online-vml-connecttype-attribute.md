---
title: Атрибут Коннекттипе VML
description: Атрибут Коннекттипе VML
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a54135dcb4ffe0a86f781d68b8babe1259029be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133898"
---
# <a name="vml-connecttype-attribute"></a><span data-ttu-id="81145-103">Атрибут Коннекттипе VML</span><span class="sxs-lookup"><span data-stu-id="81145-103">VML ConnectType Attribute</span></span>

<span data-ttu-id="81145-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="81145-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="81145-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="81145-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="81145-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="81145-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="81145-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="81145-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="81145-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="81145-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="81145-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="81145-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="81145-110">Определяет тип точек соединения, используемых для присоединения фигур к другим фигурам.</span><span class="sxs-lookup"><span data-stu-id="81145-110">Defines the type of connection points used for attaching shapes to other shapes.</span></span> <span data-ttu-id="81145-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="81145-111">Read/write.</span></span> <span data-ttu-id="81145-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="81145-112">**String**.</span></span>

<span data-ttu-id="81145-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="81145-113">**Applies To**</span></span>

[<span data-ttu-id="81145-114">Путь</span><span class="sxs-lookup"><span data-stu-id="81145-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="81145-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="81145-115">**Tag Syntax**</span></span>

<span data-ttu-id="81145-116"><v: *element* о:коннекттипе = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="81145-116"><v: *element* o:connecttype=" *expression* "></span></span>

<span data-ttu-id="81145-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="81145-117">**Remarks**</span></span>

<span data-ttu-id="81145-118">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="81145-118">Values include:</span></span>



| <span data-ttu-id="81145-119">Значение</span><span class="sxs-lookup"><span data-stu-id="81145-119">Value</span></span>    | <span data-ttu-id="81145-120">Описание</span><span class="sxs-lookup"><span data-stu-id="81145-120">Description</span></span>                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81145-121">нет</span><span class="sxs-lookup"><span data-stu-id="81145-121">none</span></span>     | <span data-ttu-id="81145-122">Нет сайтов подключения.</span><span class="sxs-lookup"><span data-stu-id="81145-122">No connection sites.</span></span> <span data-ttu-id="81145-123">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="81145-123">Default.</span></span>                                                                                                         |
| <span data-ttu-id="81145-124">rect</span><span class="sxs-lookup"><span data-stu-id="81145-124">rect</span></span>     | <span data-ttu-id="81145-125">Стандартные четыре точки соединения, расположенные в средней части сверху, снизу, слева и справа.</span><span class="sxs-lookup"><span data-stu-id="81145-125">Standard four connection points at midpoints of top, bottom, left, and right sides.</span></span>                                                   |
| <span data-ttu-id="81145-126">сегменты</span><span class="sxs-lookup"><span data-stu-id="81145-126">segments</span></span> | <span data-ttu-id="81145-127">Используются точки редактирования фигуры.</span><span class="sxs-lookup"><span data-stu-id="81145-127">The edit points of the shape are used.</span></span> <span data-ttu-id="81145-128">Точки редактирования — это черные точки в графическом редакторе, используемые для выбора частей фигуры.</span><span class="sxs-lookup"><span data-stu-id="81145-128">Edit points are the black dots in a graphical editor that are used to select parts of a shape.</span></span> |
| <span data-ttu-id="81145-129">пользовательский</span><span class="sxs-lookup"><span data-stu-id="81145-129">custom</span></span>   | <span data-ttu-id="81145-130">Настраиваемый массив расположений соединений.</span><span class="sxs-lookup"><span data-stu-id="81145-130">A custom array of connection locations.</span></span>                                                                                               |



 

<span data-ttu-id="81145-131">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="81145-131">*Microsoft Office Extensions Attribute*</span></span>

 

 