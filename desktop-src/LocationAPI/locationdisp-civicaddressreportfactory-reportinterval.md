---
description: Текущий интервал событий для отчета об административном адресе в миллисекундах.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: Локатиондисп. Цивикаддрессрепортфактори. Репортинтервал, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: 47f7840be20ac640b5a8e7014f8401bc2350d328
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684551"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a><span data-ttu-id="e4e27-103">Локатиондисп. Цивикаддрессрепортфактори. Репортинтервал, свойство</span><span class="sxs-lookup"><span data-stu-id="e4e27-103">LocationDisp.CivicAddressReportFactory.ReportInterval property</span></span>

<span data-ttu-id="e4e27-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="e4e27-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e4e27-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="e4e27-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e4e27-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4e27-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="e4e27-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="e4e27-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="e4e27-108">Текущий интервал событий для отчета об административном адресе в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="e4e27-108">The current civic address report event interval in milliseconds.</span></span>

<span data-ttu-id="e4e27-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e4e27-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4e27-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4e27-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="e4e27-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e4e27-111">Property value</span></span>

<span data-ttu-id="e4e27-112">Это свойство является **ulong** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e4e27-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4e27-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4e27-113">Remarks</span></span>

<span data-ttu-id="e4e27-114">Это значение является запросом для поставщика расположения.</span><span class="sxs-lookup"><span data-stu-id="e4e27-114">This value is a request for the location provider.</span></span> <span data-ttu-id="e4e27-115">Поставщик расположения не требуется для предоставления отчетов по запрошенному вами интервалу.</span><span class="sxs-lookup"><span data-stu-id="e4e27-115">The location provider is not required to provide reports at the interval that you requested.</span></span> <span data-ttu-id="e4e27-116">Прочтите значение этого свойства, чтобы определить значение параметра интервала true Report.</span><span class="sxs-lookup"><span data-stu-id="e4e27-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e27-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e4e27-117">Requirements</span></span>



| <span data-ttu-id="e4e27-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e4e27-118">Requirement</span></span> | <span data-ttu-id="e4e27-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e4e27-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="e4e27-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4e27-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e27-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e4e27-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e4e27-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4e27-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e27-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e4e27-123">None supported</span></span><br/>                  |



 

