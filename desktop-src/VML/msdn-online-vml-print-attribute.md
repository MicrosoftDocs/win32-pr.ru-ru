---
title: Атрибут печати VML
description: Атрибут печати VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672299"
---
# <a name="vml-print-attribute"></a><span data-ttu-id="4aa38-103">Атрибут печати VML</span><span class="sxs-lookup"><span data-stu-id="4aa38-103">VML Print Attribute</span></span>

<span data-ttu-id="4aa38-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4aa38-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4aa38-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="4aa38-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4aa38-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="4aa38-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4aa38-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4aa38-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4aa38-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4aa38-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4aa38-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4aa38-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4aa38-110">Определяет, будет ли распечатана фигура.</span><span class="sxs-lookup"><span data-stu-id="4aa38-110">Determines whether the shape will be printed.</span></span> <span data-ttu-id="4aa38-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="4aa38-111">Read/write.</span></span> <span data-ttu-id="4aa38-112">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="4aa38-112">[VgTriState](msdn-online-vml-vgtristate.md).</span></span>

<span data-ttu-id="4aa38-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="4aa38-113">**Applies To**</span></span>

[<span data-ttu-id="4aa38-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="4aa38-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="4aa38-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="4aa38-115">**Tag Syntax**</span></span>

<span data-ttu-id="4aa38-116"><v: *элемент* Print = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="4aa38-116"><v: *element* print=" *expression* "></span></span>

<span data-ttu-id="4aa38-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="4aa38-117">**Script Syntax**</span></span>

<span data-ttu-id="4aa38-118">*элемент* . Print = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="4aa38-118">*element* .print="*expression*"</span></span>

<span data-ttu-id="4aa38-119">*выражение* = *элемент*. Print</span><span class="sxs-lookup"><span data-stu-id="4aa38-119">*expression*=*element*.print</span></span>

<span data-ttu-id="4aa38-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="4aa38-120">**Remarks**</span></span>

<span data-ttu-id="4aa38-121">Позволяет указать, будут ли напечатаны фигуры.</span><span class="sxs-lookup"><span data-stu-id="4aa38-121">Provided as a way to specify whether shapes will be printed.</span></span> <span data-ttu-id="4aa38-122">Обратите внимание, что фигура по-прежнему может отображаться на экране, даже если она не печатается в результате **ложного** этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="4aa38-122">Note that a shape can still be displayed on the screen, even if it is not printed as a result of this attribute being **False**.</span></span> <span data-ttu-id="4aa38-123">По умолчанию используется значение **True**.</span><span class="sxs-lookup"><span data-stu-id="4aa38-123">The default value is **True**.</span></span>

<span data-ttu-id="4aa38-124">Этот атрибут используется Microsoft Office но не используется обозревателем Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4aa38-124">This attribute is used by Microsoft Office but is not used by Microsoft Internet Explorer.</span></span>

<span data-ttu-id="4aa38-125">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="4aa38-125">*Microsoft Office Extensions Attribute*</span></span>

 

 