---
description: Расстояние от сообщаемого места в метрах. В сочетании с исходным расположением в качестве источника этот радиус описывает круг, в котором может находиться фактическое расположение.
ms.assetid: a9565bd5-d1e0-45f8-abeb-3191b16480fa
title: Локатиондисп. Дисплатлонгрепорт. Ерроррадиус, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.ErrorRadius
api_type:
- COM
api_location: ''
ms.openlocfilehash: f99ff9b03451738158a98541bfae0e67a8827717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683608"
---
# <a name="locationdispdisplatlongreporterrorradius-property"></a><span data-ttu-id="f3faa-104">Локатиондисп. Дисплатлонгрепорт. Ерроррадиус, свойство</span><span class="sxs-lookup"><span data-stu-id="f3faa-104">LocationDisp.DispLatLongReport.ErrorRadius property</span></span>

<span data-ttu-id="f3faa-105">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f3faa-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f3faa-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f3faa-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f3faa-107">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3faa-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="f3faa-108">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="f3faa-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="f3faa-109">Расстояние от сообщаемого места в метрах.</span><span class="sxs-lookup"><span data-stu-id="f3faa-109">A distance from the reported location, in meters.</span></span> <span data-ttu-id="f3faa-110">В сочетании с исходным расположением в качестве источника этот радиус описывает круг, в котором может находиться фактическое расположение.</span><span class="sxs-lookup"><span data-stu-id="f3faa-110">Combined with the reported location as the origin, this radius describes the circle in which the actual location is probably located.</span></span>

<span data-ttu-id="f3faa-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f3faa-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3faa-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3faa-112">Syntax</span></span>


```JScript
ErrorRadius = LocationDisp.DispLatLongReport.ErrorRadius
```



## <a name="property-value"></a><span data-ttu-id="f3faa-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f3faa-113">Property value</span></span>

<span data-ttu-id="f3faa-114">Это свойство доступно только для чтения ( **число** с плавающей запятой двойной точности).</span><span class="sxs-lookup"><span data-stu-id="f3faa-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="f3faa-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="f3faa-115">Examples</span></span>

<span data-ttu-id="f3faa-116">Пример использования этого свойства см. [в примере простого отчета LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="f3faa-116">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3faa-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f3faa-117">Requirements</span></span>



| <span data-ttu-id="f3faa-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f3faa-118">Requirement</span></span> | <span data-ttu-id="f3faa-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f3faa-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="f3faa-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3faa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3faa-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f3faa-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f3faa-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3faa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3faa-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f3faa-123">None supported</span></span><br/>                  |



 

