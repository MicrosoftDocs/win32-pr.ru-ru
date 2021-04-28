---
description: Свойство Локатиондисп. Цивикаддрессрепортфактори. Десиредаккураци — текущее значение точности.
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: Локатиондисп. Цивикаддрессрепортфактори. Десиредаккураци, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a18a363c2f24e9b17e16064b7375a4f075a1a8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110922"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a><span data-ttu-id="13113-103">Локатиондисп. Цивикаддрессрепортфактори. Десиредаккураци, свойство</span><span class="sxs-lookup"><span data-stu-id="13113-103">LocationDisp.CivicAddressReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="13113-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="13113-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="13113-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="13113-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="13113-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="13113-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="13113-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="13113-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="13113-108">Текущее значение требуемой точности.</span><span class="sxs-lookup"><span data-stu-id="13113-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="13113-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="13113-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="13113-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13113-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="13113-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="13113-111">Property value</span></span>

<span data-ttu-id="13113-112">Это свойство является **ulong** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="13113-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="13113-113">Значение</span><span class="sxs-lookup"><span data-stu-id="13113-113">Value</span></span>                                                                        | <span data-ttu-id="13113-114">Значение</span><span class="sxs-lookup"><span data-stu-id="13113-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13113-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="13113-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="13113-116">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="13113-116">Default.</span></span> <span data-ttu-id="13113-117">Датчик должен использовать точность, для которой он может оптимизировать энергопотребление и другие аспекты затрат.</span><span class="sxs-lookup"><span data-stu-id="13113-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="13113-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="13113-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="13113-119">Датчик должен предоставлять наиболее точный возможный отчет.</span><span class="sxs-lookup"><span data-stu-id="13113-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="13113-120">Это касается использования услуг по взиманию средств, потребления высокого уровня мощности батарей или пропускной способности подключения.</span><span class="sxs-lookup"><span data-stu-id="13113-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="13113-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="13113-121">Remarks</span></span>

<span data-ttu-id="13113-122">Это значение является запросом к поставщику расположения.</span><span class="sxs-lookup"><span data-stu-id="13113-122">This value is a request to the location provider.</span></span> <span data-ttu-id="13113-123">Поставщик расположения не требуется для предоставления точности, которую вы запрашиваете.</span><span class="sxs-lookup"><span data-stu-id="13113-123">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="13113-124">Прочтите значение этого свойства, чтобы определить значение параметра точности.</span><span class="sxs-lookup"><span data-stu-id="13113-124">Read the value of this property to discover the true accuracy setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="13113-125">Требования</span><span class="sxs-lookup"><span data-stu-id="13113-125">Requirements</span></span>



| <span data-ttu-id="13113-126">Требование</span><span class="sxs-lookup"><span data-stu-id="13113-126">Requirement</span></span> | <span data-ttu-id="13113-127">Значение</span><span class="sxs-lookup"><span data-stu-id="13113-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="13113-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13113-128">Minimum supported client</span></span><br/> | <span data-ttu-id="13113-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="13113-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="13113-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13113-130">Minimum supported server</span></span><br/> | <span data-ttu-id="13113-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="13113-131">None supported</span></span><br/>                  |



 

