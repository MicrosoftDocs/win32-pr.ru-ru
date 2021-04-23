---
title: Атрибут Таблепропертиес VML
description: Атрибут Таблепропертиес VML
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691516"
---
# <a name="vml-tableproperties-attribute"></a><span data-ttu-id="f92f7-103">Атрибут Таблепропертиес VML</span><span class="sxs-lookup"><span data-stu-id="f92f7-103">VML TableProperties Attribute</span></span>

<span data-ttu-id="f92f7-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f92f7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f92f7-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="f92f7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f92f7-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="f92f7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f92f7-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f92f7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f92f7-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f92f7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f92f7-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f92f7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f92f7-110">Определяет свойства таблицы.</span><span class="sxs-lookup"><span data-stu-id="f92f7-110">Determines table properties.</span></span> <span data-ttu-id="f92f7-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="f92f7-111">Read/write.</span></span> <span data-ttu-id="f92f7-112">**Integer**.</span><span class="sxs-lookup"><span data-stu-id="f92f7-112">**Integer**.</span></span>

<span data-ttu-id="f92f7-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="f92f7-113">**Applies To**</span></span>

[<span data-ttu-id="f92f7-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="f92f7-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f92f7-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="f92f7-115">**Tag Syntax**</span></span>

<span data-ttu-id="f92f7-116"><v: *element* о:таблепропертиес = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="f92f7-116"><v: *element* o:tableproperties=" *expression* "></span></span>

<span data-ttu-id="f92f7-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="f92f7-117">**Remarks**</span></span>

<span data-ttu-id="f92f7-118">Используется в Microsoft PowerPoint для собственных таблиц.</span><span class="sxs-lookup"><span data-stu-id="f92f7-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="f92f7-119">По умолчанию установлено значение 0.</span><span class="sxs-lookup"><span data-stu-id="f92f7-119">Default value is 0.</span></span> <span data-ttu-id="f92f7-120">Используются только первые три бита этого целого числа.</span><span class="sxs-lookup"><span data-stu-id="f92f7-120">Only the first three bits of this integer are used.</span></span>

<span data-ttu-id="f92f7-121">Несмотря на то, что значение хранится в фигуре, атрибут полезен только в том случае, если таблица состоит из сгруппированных фигур. Биты могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="f92f7-121">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.Bits may be combined.</span></span>

<span data-ttu-id="f92f7-122">Включаются следующие битовые значения.</span><span class="sxs-lookup"><span data-stu-id="f92f7-122">The following bit values are included.</span></span>



| <span data-ttu-id="f92f7-123">bit</span><span class="sxs-lookup"><span data-stu-id="f92f7-123">Bit</span></span> | <span data-ttu-id="f92f7-124">Описание</span><span class="sxs-lookup"><span data-stu-id="f92f7-124">Description</span></span>                              |
|-----|------------------------------------------|
| <span data-ttu-id="f92f7-125">1</span><span class="sxs-lookup"><span data-stu-id="f92f7-125">1</span></span>   | <span data-ttu-id="f92f7-126">Задайте, если группа фигур является таблицей.</span><span class="sxs-lookup"><span data-stu-id="f92f7-126">Set if the group of shapes is a table.</span></span>   |
| <span data-ttu-id="f92f7-127">2</span><span class="sxs-lookup"><span data-stu-id="f92f7-127">2</span></span>   | <span data-ttu-id="f92f7-128">Установите, если фигура является заполнителем.</span><span class="sxs-lookup"><span data-stu-id="f92f7-128">Set if the shape is a placeholder.</span></span>       |
| <span data-ttu-id="f92f7-129">3</span><span class="sxs-lookup"><span data-stu-id="f92f7-129">3</span></span>   | <span data-ttu-id="f92f7-130">Установите, если текст таблицы является двунаправленным.</span><span class="sxs-lookup"><span data-stu-id="f92f7-130">Set if the table text is bi-directional.</span></span> |



 

<span data-ttu-id="f92f7-131">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="f92f7-131">*Microsoft Office Extensions Attribute*</span></span>

 

 