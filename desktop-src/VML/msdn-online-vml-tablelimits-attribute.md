---
title: Атрибут Таблелимитс VML
description: Атрибут Таблелимитс VML
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b35a7449cc2f348e6040161c1fb599c29972803
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791833"
---
# <a name="vml-tablelimits-attribute"></a><span data-ttu-id="9bb8b-103">Атрибут Таблелимитс VML</span><span class="sxs-lookup"><span data-stu-id="9bb8b-103">VML TableLimits Attribute</span></span>

<span data-ttu-id="9bb8b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9bb8b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9bb8b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9bb8b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9bb8b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9bb8b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9bb8b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9bb8b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9bb8b-110">Список значений минимальной высоты для каждой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-110">List of minimum height values for each row in a table.</span></span> <span data-ttu-id="9bb8b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-111">Read/write.</span></span> <span data-ttu-id="9bb8b-112">**Вгленгсаррай**.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-112">**VgLengthArray**.</span></span>

<span data-ttu-id="9bb8b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="9bb8b-113">**Applies To**</span></span>

[<span data-ttu-id="9bb8b-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="9bb8b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="9bb8b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="9bb8b-115">**Tag Syntax**</span></span>

<span data-ttu-id="9bb8b-116"><v: *element* о:таблелимитс = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="9bb8b-116"><v: *element* o:tablelimits=" *expression* "></span></span>

<span data-ttu-id="9bb8b-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="9bb8b-117">**Remarks**</span></span>

<span data-ttu-id="9bb8b-118">Используется в Microsoft PowerPoint для собственных таблиц.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="9bb8b-119">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-119">Default value is **Null**.</span></span>

<span data-ttu-id="9bb8b-120">Несмотря на то, что значение хранится в фигуре, атрибут полезен только в том случае, если таблица состоит из сгруппированных фигур.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-120">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.</span></span> <span data-ttu-id="9bb8b-121">Когда текст добавляется в ячейки таблицы, высота строки может увеличиться.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-121">When text is added to table cells, the row height may increase.</span></span> <span data-ttu-id="9bb8b-122">Атрибут **таблелимитс** сохраняет исходную высоту строки таким образом, что при удалении текста высота строки не попадает под исходным значением.</span><span class="sxs-lookup"><span data-stu-id="9bb8b-122">The **TableLimits** attribute stores the original row height so that if text is deleted, the row height will not fall below the original value.</span></span>

<span data-ttu-id="9bb8b-123">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="9bb8b-123">*Microsoft Office Extensions Attribute*</span></span>

 

 