---
description: Текущий отчет широты и долготы.
ms.assetid: d2bb305f-911e-46f7-abde-56e9fba9182b
title: Свойство Локатиондисп. Латлонгрепортфактори. Латлонгрепорт (Локатионапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.LatLongReport
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: c44582c01685431e9b5dfa4820735728dd2a9cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264861"
---
# <a name="locationdisplatlongreportfactorylatlongreport-property"></a><span data-ttu-id="79251-103">Локатиондисп. Латлонгрепортфактори. Латлонгрепорт, свойство</span><span class="sxs-lookup"><span data-stu-id="79251-103">LocationDisp.LatLongReportFactory.LatLongReport property</span></span>

<span data-ttu-id="79251-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="79251-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="79251-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="79251-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="79251-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79251-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="79251-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="79251-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="79251-108">Текущий отчет широты и долготы.</span><span class="sxs-lookup"><span data-stu-id="79251-108">The current latitude/longitude report.</span></span>

<span data-ttu-id="79251-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="79251-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="79251-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79251-110">Syntax</span></span>


```JScript
objLatLongReport = LocationDisp.LatLongReportFactory.LatLongReport
```



## <a name="property-value"></a><span data-ttu-id="79251-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="79251-111">Property value</span></span>

<span data-ttu-id="79251-112">Это свойство доступно только для чтения [**локатиондисп. дисплатлонгрепорт**](locationdisp-displatlongreport.md).</span><span class="sxs-lookup"><span data-stu-id="79251-112">This property is a read-only [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span>

## <a name="examples"></a><span data-ttu-id="79251-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="79251-113">Examples</span></span>

<span data-ttu-id="79251-114">Пример использования этого свойства см. [в примере простого отчета LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="79251-114">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="79251-115">Требования</span><span class="sxs-lookup"><span data-stu-id="79251-115">Requirements</span></span>



| <span data-ttu-id="79251-116">Требование</span><span class="sxs-lookup"><span data-stu-id="79251-116">Requirement</span></span> | <span data-ttu-id="79251-117">Значение</span><span class="sxs-lookup"><span data-stu-id="79251-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79251-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79251-118">Minimum supported client</span></span><br/> | <span data-ttu-id="79251-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="79251-119">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="79251-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79251-120">Minimum supported server</span></span><br/> | <span data-ttu-id="79251-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="79251-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="79251-122">Header</span><span class="sxs-lookup"><span data-stu-id="79251-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="79251-123"><dt>Локатионапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="79251-123"><dt>Locationapi.h</dt></span></span> </dl> |



 

