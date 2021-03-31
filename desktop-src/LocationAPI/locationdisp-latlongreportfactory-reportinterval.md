---
description: Текущий интервал событий для отчета широты и долготы в миллисекундах.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: Локатиондисп. Латлонгрепортфактори. Репортинтервал, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265051"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a><span data-ttu-id="31379-103">Локатиондисп. Латлонгрепортфактори. Репортинтервал, свойство</span><span class="sxs-lookup"><span data-stu-id="31379-103">LocationDisp.LatLongReportFactory.ReportInterval property</span></span>

<span data-ttu-id="31379-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="31379-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="31379-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="31379-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="31379-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="31379-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="31379-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="31379-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="31379-108">Текущий интервал событий для отчета широты и долготы в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="31379-108">The current latitude/longitude report event interval in milliseconds.</span></span>

<span data-ttu-id="31379-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="31379-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="31379-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31379-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="31379-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="31379-111">Property value</span></span>

<span data-ttu-id="31379-112">Это свойство является **ulong** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="31379-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="31379-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31379-113">Remarks</span></span>

<span data-ttu-id="31379-114">Это значение является запросом к поставщику расположения.</span><span class="sxs-lookup"><span data-stu-id="31379-114">This value is a request to the location provider.</span></span> <span data-ttu-id="31379-115">Поставщик расположения не требуется для предоставления отчетов на запрошенный интервал.</span><span class="sxs-lookup"><span data-stu-id="31379-115">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="31379-116">Прочтите значение этого свойства, чтобы определить значение параметра интервала true Report.</span><span class="sxs-lookup"><span data-stu-id="31379-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="31379-117">Требования</span><span class="sxs-lookup"><span data-stu-id="31379-117">Requirements</span></span>



| <span data-ttu-id="31379-118">Требование</span><span class="sxs-lookup"><span data-stu-id="31379-118">Requirement</span></span> | <span data-ttu-id="31379-119">Значение</span><span class="sxs-lookup"><span data-stu-id="31379-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="31379-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31379-120">Minimum supported client</span></span><br/> | <span data-ttu-id="31379-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="31379-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="31379-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31379-122">Minimum supported server</span></span><br/> | <span data-ttu-id="31379-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="31379-123">None supported</span></span><br/>                  |



 

