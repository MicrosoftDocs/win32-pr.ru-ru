---
title: Элемент кривой VML
description: Элемент кривой VML
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b9e04086652bf9dde7d7e7f5ebdea0992f774c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260918"
---
# <a name="vml-curve-element"></a><span data-ttu-id="eb428-103">Элемент кривой VML</span><span class="sxs-lookup"><span data-stu-id="eb428-103">VML Curve Element</span></span>

<span data-ttu-id="eb428-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="eb428-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eb428-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="eb428-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eb428-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="eb428-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eb428-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eb428-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eb428-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="eb428-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eb428-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="eb428-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eb428-110">Стандартная фигура кривой.</span><span class="sxs-lookup"><span data-stu-id="eb428-110">Predefined curve shape.</span></span>

<span data-ttu-id="eb428-111">**Кривая** использует атрибуты [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [Control1](msdn-online-vml-control1-attribute.md)и [control2](msdn-online-vml-control2-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="eb428-111">**Curve** uses the [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [control1](msdn-online-vml-control1-attribute.md), and [control2](msdn-online-vml-control2-attribute.md) attributes.</span></span>

<span data-ttu-id="eb428-112">Ниже приведен минимальный код, необходимый для создания образа.</span><span class="sxs-lookup"><span data-stu-id="eb428-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 