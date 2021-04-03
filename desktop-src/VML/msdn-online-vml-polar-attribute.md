---
title: Атрибут полярной VML
description: Атрибут полярной VML
ms.assetid: b7ea8764-057d-4c14-81ad-77ae82b1aa31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baea7a8c044436df7e6efbf178ddb0273d7fc59d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791976"
---
# <a name="vml-polar-attribute"></a><span data-ttu-id="b869c-103">Атрибут полярной VML</span><span class="sxs-lookup"><span data-stu-id="b869c-103">VML Polar Attribute</span></span>

<span data-ttu-id="b869c-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b869c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b869c-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b869c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b869c-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="b869c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b869c-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b869c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b869c-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b869c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b869c-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b869c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b869c-110">Задает центральную точку для полярных дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="b869c-110">Specifies the center position for polar handles.</span></span> <span data-ttu-id="b869c-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b869c-111">Read/write.</span></span> <span data-ttu-id="b869c-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="b869c-112">**VgVector2D**.</span></span>

<span data-ttu-id="b869c-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="b869c-113">**Applies To**</span></span>

<span data-ttu-id="b869c-114">[H](msdn-online-vml-h-element.md) (вложенный элемент [дескрипторов](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="b869c-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="b869c-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="b869c-115">**Tag Syntax**</span></span>

<span data-ttu-id="b869c-116"><v: *element* Полярное = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="b869c-116"><v: *element* polar=" *expression* "></span></span>

<span data-ttu-id="b869c-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="b869c-117">**Remarks**</span></span>

<span data-ttu-id="b869c-118">Значением по умолчанию является строка NULL.</span><span class="sxs-lookup"><span data-stu-id="b869c-118">The default value is a null string.</span></span> <span data-ttu-id="b869c-119">Если указаны значения, это означает, что измерение является полярным, а атрибут « [позиционирование](position-attribute--h--vml.md) » определяет значения радиуса и угла маркера, а не значения x и y.</span><span class="sxs-lookup"><span data-stu-id="b869c-119">If values are specified, this indicates that the measurement is polar and that the [Position](position-attribute--h--vml.md) attribute defines radius and angle values of the handle instead of x and y values.</span></span>

<span data-ttu-id="b869c-120">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="b869c-120">*VML Standard Attribute*</span></span>

 

 