---
title: Атрибут Инвкс VML
description: Атрибут Инвкс VML
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792205"
---
# <a name="vml-invx-attribute"></a><span data-ttu-id="70876-103">Атрибут Инвкс VML</span><span class="sxs-lookup"><span data-stu-id="70876-103">VML InvX Attribute</span></span>

<span data-ttu-id="70876-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="70876-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="70876-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="70876-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="70876-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="70876-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="70876-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="70876-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="70876-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="70876-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="70876-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="70876-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="70876-110">Определяет, инвертирована ли Координата x маркера.</span><span class="sxs-lookup"><span data-stu-id="70876-110">Determines whether the x position of the handle is inverted.</span></span> <span data-ttu-id="70876-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="70876-111">Read/write.</span></span> <span data-ttu-id="70876-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="70876-112">**VgTriState**.</span></span>

<span data-ttu-id="70876-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="70876-113">**Applies To**</span></span>

<span data-ttu-id="70876-114">[H](msdn-online-vml-h-element.md) (вложенный элемент [дескрипторов](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="70876-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="70876-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="70876-115">**Tag Syntax**</span></span>

<span data-ttu-id="70876-116"><v: *element* инвкс = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="70876-116"><v: *element* invx=" *expression* "></span></span>

<span data-ttu-id="70876-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="70876-117">**Remarks**</span></span>

<span data-ttu-id="70876-118">Если **значение равно true**, то Координата x для маркера инвертирована путем вычитания значения x из значения x **курдоригин** , добавленного к значению x объекта **курдсизе**.</span><span class="sxs-lookup"><span data-stu-id="70876-118">If **True**, the x position of the handle is inverted by subtracting the x value from the x value of **CoordOrigin** added to the x value of **CoordSize**.</span></span> <span data-ttu-id="70876-119">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="70876-119">The default value is **False**.</span></span>

<span data-ttu-id="70876-120">Этот атрибут эквивалентен</span><span class="sxs-lookup"><span data-stu-id="70876-120">This attribute is the equivalent of</span></span>

<span data-ttu-id="70876-121">курдоригин. x + курдсизе. x-h. позиционирование. x</span><span class="sxs-lookup"><span data-stu-id="70876-121">coordorigin.x + coordsize.x - h.position.x</span></span>

<span data-ttu-id="70876-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="70876-122">*VML Standard Attribute*</span></span>

 

 