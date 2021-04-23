---
title: Элемент дуги VML
description: Элемент дуги VML
ms.assetid: 46b5b78a-9a69-432b-9008-0ce7a658b9dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd35d59349e10f38495807ceb3f08dc254c117e2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339025"
---
# <a name="vml-arc-element"></a><span data-ttu-id="edb51-103">Элемент дуги VML</span><span class="sxs-lookup"><span data-stu-id="edb51-103">VML Arc Element</span></span>

<span data-ttu-id="edb51-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="edb51-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="edb51-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="edb51-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="edb51-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="edb51-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="edb51-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="edb51-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="edb51-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="edb51-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="edb51-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="edb51-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="edb51-110">Предопределенная фигура дуги.</span><span class="sxs-lookup"><span data-stu-id="edb51-110">Predefined arc shape.</span></span>

<span data-ttu-id="edb51-111">**Дуга** использует атрибуты [startAngle](msdn-online-vml-startangle-attribute.md) и [ендангле](msdn-online-vml-endangle-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="edb51-111">**Arc** uses the [startangle](msdn-online-vml-startangle-attribute.md) and [endangle](msdn-online-vml-endangle-attribute.md) attributes.</span></span>

<span data-ttu-id="edb51-112">Ниже приведен минимальный код, необходимый для создания образа.</span><span class="sxs-lookup"><span data-stu-id="edb51-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:arc
   style="top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```





 

 