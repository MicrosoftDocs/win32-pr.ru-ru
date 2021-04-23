---
title: Атрибут вершин VML
description: Атрибут вершин VML
ms.assetid: 3b887ecb-19e8-4ebf-9db6-bf3ed4f7d589
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a236be4b1496ceb938cc827692610a987cc2e9b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413564"
---
# <a name="vml-vertices-attribute"></a><span data-ttu-id="53958-103">Атрибут вершин VML</span><span class="sxs-lookup"><span data-stu-id="53958-103">VML Vertices Attribute</span></span>

<span data-ttu-id="53958-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="53958-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="53958-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="53958-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="53958-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="53958-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="53958-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="53958-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="53958-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="53958-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="53958-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="53958-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="53958-110">Определяет, можно ли изменить вершины пути редактором.</span><span class="sxs-lookup"><span data-stu-id="53958-110">Determines whether the vertices of a path can be changed by an editor.</span></span> <span data-ttu-id="53958-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="53958-111">Read/write.</span></span> <span data-ttu-id="53958-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="53958-112">**VgTriState**.</span></span>

<span data-ttu-id="53958-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="53958-113">**Applies To**</span></span>

[<span data-ttu-id="53958-114">Блокировки</span><span class="sxs-lookup"><span data-stu-id="53958-114">Locks</span></span>](msdn-online-vml-locks-element.md)

<span data-ttu-id="53958-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="53958-115">**Tag Syntax**</span></span>

<span data-ttu-id="53958-116"><o: *element* вершины = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="53958-116"><o: *element* vertices=" *expression* "></span></span>

<span data-ttu-id="53958-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="53958-117">**Remarks**</span></span>

<span data-ttu-id="53958-118">Если **значение — true**, точки редактирования вершин контура блокируются.</span><span class="sxs-lookup"><span data-stu-id="53958-118">If **True**, the edit points of the vertices of a path are locked.</span></span> <span data-ttu-id="53958-119">Значение по умолчанию — **true** для Microsoft Office автофигур, но в противном случае — значение **false**.</span><span class="sxs-lookup"><span data-stu-id="53958-119">The default value is **True** for Microsoft Office AutoShapes, but otherwise is **False**.</span></span>

<span data-ttu-id="53958-120">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="53958-120">*Microsoft Office Extensions Attribute*</span></span>

 

 