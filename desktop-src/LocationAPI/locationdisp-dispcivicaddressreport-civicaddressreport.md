---
description: Текущий отчет об административном адресе.
ms.assetid: a58dd612-bc54-42d1-9960-8c3de1c4fa83
title: Свойство Локатиондисп. Цивикаддрессрепортфактори. Цивикаддрессрепорт (Локатионапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.CivicAddressReport
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: c8be6e03861f1c5b2abffcb4b23d4845defa494e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684022"
---
# <a name="locationdispcivicaddressreportfactorycivicaddressreport-property"></a><span data-ttu-id="12fb3-103">Локатиондисп. Цивикаддрессрепортфактори. Цивикаддрессрепорт, свойство</span><span class="sxs-lookup"><span data-stu-id="12fb3-103">LocationDisp.CivicAddressReportFactory.CivicAddressReport property</span></span>

<span data-ttu-id="12fb3-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="12fb3-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="12fb3-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="12fb3-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="12fb3-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="12fb3-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="12fb3-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="12fb3-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="12fb3-108">Текущий отчет об административном адресе.</span><span class="sxs-lookup"><span data-stu-id="12fb3-108">The current civic address report.</span></span>

<span data-ttu-id="12fb3-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="12fb3-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fb3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12fb3-110">Syntax</span></span>


```JScript
objCivicAddressReport = LocationDisp.CivicAddressReportFactory.CivicAddressReport
```



## <a name="property-value"></a><span data-ttu-id="12fb3-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="12fb3-111">Property value</span></span>

<span data-ttu-id="12fb3-112">Это свойство доступно только для чтения [**локатиондисп. Цивикаддрессрепортфактори**](locationdisp-civicaddressreportfactory.md).</span><span class="sxs-lookup"><span data-stu-id="12fb3-112">This property is a read-only [**LocationDisp.CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="12fb3-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="12fb3-113">Examples</span></span>

<span data-ttu-id="12fb3-114">Пример использования этого свойства см. [в примере простого отчета об использовании административного адреса](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="12fb3-114">For an example of how to use this property, see [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="12fb3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="12fb3-115">Requirements</span></span>



| <span data-ttu-id="12fb3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="12fb3-116">Requirement</span></span> | <span data-ttu-id="12fb3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="12fb3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12fb3-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12fb3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="12fb3-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="12fb3-119">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="12fb3-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12fb3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="12fb3-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="12fb3-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="12fb3-122">Header</span><span class="sxs-lookup"><span data-stu-id="12fb3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="12fb3-123"><dt>Локатионапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="12fb3-123"><dt>Locationapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12fb3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12fb3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12fb3-125">**Локатиондисп. Цивикаддрессрепортфактори**</span><span class="sxs-lookup"><span data-stu-id="12fb3-125">**LocationDisp.CivicAddressReportFactory**</span></span>](locationdisp-civicaddressreportfactory.md)
</dt> </dl>

 

