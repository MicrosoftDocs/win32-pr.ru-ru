---
title: Атрибут ext (объемная) (VML)
description: Атрибут ext (объемная) (VML)
ms.assetid: 5c7b2137-ddb6-422c-a202-6de494dc993f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19721ebe03198485b7f43ff671cfd3c45b236c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413192"
---
# <a name="ext-attribute-extrusionvml"></a><span data-ttu-id="7df85-103">Атрибут ext (объемная) (VML)</span><span class="sxs-lookup"><span data-stu-id="7df85-103">Ext Attribute (Extrusion)(VML)</span></span>

<span data-ttu-id="7df85-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7df85-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7df85-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="7df85-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7df85-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="7df85-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7df85-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7df85-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7df85-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7df85-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7df85-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7df85-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7df85-110">Определяет поведение по умолчанию для графических редакторов.</span><span class="sxs-lookup"><span data-stu-id="7df85-110">Defines the default extrusion behavior for graphical editors.</span></span> <span data-ttu-id="7df85-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="7df85-111">Read/write.</span></span> <span data-ttu-id="7df85-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="7df85-112">**String**.</span></span>

<span data-ttu-id="7df85-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="7df85-113">**Applies To**</span></span>

[<span data-ttu-id="7df85-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="7df85-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="7df85-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="7df85-115">**Tag Syntax**</span></span>

<span data-ttu-id="7df85-116"><o: *element* в:екст = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="7df85-116"><o: *element* v:ext=" *expression* "></span></span>

<span data-ttu-id="7df85-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="7df85-117">**Script Syntax**</span></span>

<span data-ttu-id="7df85-118">*element* . ext = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="7df85-118">*element* .ext="*expression*"</span></span>

<span data-ttu-id="7df85-119">*выражение* = *element*. ext</span><span class="sxs-lookup"><span data-stu-id="7df85-119">*expression*=*element*.ext</span></span>

<span data-ttu-id="7df85-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="7df85-120">**Remarks**</span></span>

<span data-ttu-id="7df85-121">Инструктирует графический редактор для отрисовки элемента.</span><span class="sxs-lookup"><span data-stu-id="7df85-121">Instructs a graphical editor to render the element.</span></span> <span data-ttu-id="7df85-122">Если не удается отобразить элемент, вместо него следует использовать растровое представление.</span><span class="sxs-lookup"><span data-stu-id="7df85-122">If it can't render the element, the bitmap representation should be used instead.</span></span> <span data-ttu-id="7df85-123">Значение по умолчанию — **View**.</span><span class="sxs-lookup"><span data-stu-id="7df85-123">The default value is **view**.</span></span>

<span data-ttu-id="7df85-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="7df85-124">*VML Standard Attribute*</span></span>

 

 