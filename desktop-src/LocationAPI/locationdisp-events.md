---
description: Объектная модель API расположения предоставляет следующие события.
ms.assetid: c7ac0d81-ce36-4991-a0fb-6d3c6cc8efe8
title: События Локатиондисп
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 55dae79305547bf4e41ee27c727ab9204eb561cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674380"
---
# <a name="locationdisp-events"></a><span data-ttu-id="b2b54-103">События Локатиондисп</span><span class="sxs-lookup"><span data-stu-id="b2b54-103">LocationDisp Events</span></span>

<span data-ttu-id="b2b54-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b2b54-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b2b54-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="b2b54-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b2b54-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b2b54-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="b2b54-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="b2b54-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="b2b54-108">Объектная модель API расположения предоставляет следующие события.</span><span class="sxs-lookup"><span data-stu-id="b2b54-108">The Location API object model provides the following events.</span></span>



| <span data-ttu-id="b2b54-109">Событие</span><span class="sxs-lookup"><span data-stu-id="b2b54-109">Event</span></span>                                                  | <span data-ttu-id="b2b54-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b2b54-110">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="b2b54-111">**невЦивикаддрессрепорт**</span><span class="sxs-lookup"><span data-stu-id="b2b54-111">**NewCivicAddressReport**</span></span>](newcivicaddressreport.md) | <span data-ttu-id="b2b54-112">Происходит при создании отчета об использовании нового административного адреса.</span><span class="sxs-lookup"><span data-stu-id="b2b54-112">Occurs when a new civic address report is generated.</span></span>      |
| [<span data-ttu-id="b2b54-113">**невлатлонгрепорт**</span><span class="sxs-lookup"><span data-stu-id="b2b54-113">**NewLatLongReport**</span></span>](newlatlongreport.md)           | <span data-ttu-id="b2b54-114">Происходит при формировании нового отчета широты/долготы.</span><span class="sxs-lookup"><span data-stu-id="b2b54-114">Occurs when a new latitude/longitude report is generated.</span></span> |
| [<span data-ttu-id="b2b54-115">**статусчанжед**</span><span class="sxs-lookup"><span data-stu-id="b2b54-115">**StatusChanged**</span></span>](statuschanged.md)                 | <span data-ttu-id="b2b54-116">Происходит при изменении оперативного состояния отчета.</span><span class="sxs-lookup"><span data-stu-id="b2b54-116">Occurs when the operational status of a report changes.</span></span>   |



 

 

 
