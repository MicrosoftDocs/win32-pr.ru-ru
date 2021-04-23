---
description: Запрашивает события отчета широты и долготы.
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: Метод Локатиондисп. Латлонгрепортфактори. Листенфоррепортс (Локатионапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814808"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a><span data-ttu-id="cc691-103">Локатиондисп. Латлонгрепортфактори. Листенфоррепортс, метод</span><span class="sxs-lookup"><span data-stu-id="cc691-103">LocationDisp.LatLongReportFactory.ListenForReports method</span></span>

<span data-ttu-id="cc691-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="cc691-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cc691-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="cc691-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="cc691-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cc691-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="cc691-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="cc691-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="cc691-108">Запрашивает события отчета широты и долготы.</span><span class="sxs-lookup"><span data-stu-id="cc691-108">Requests latitude/longitude report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc691-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc691-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="cc691-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc691-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc691-111">*рекуестедрепортинтервал*</span><span class="sxs-lookup"><span data-stu-id="cc691-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="cc691-112">Число (**двойное слово**), представляющее запрошенное время между событиями отчета широты и долготы в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="cc691-112">Number (**double word**) representing the requested time between latitude/longitude report events, in milliseconds.</span></span> <span data-ttu-id="cc691-113">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="cc691-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc691-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc691-114">Return value</span></span>

<span data-ttu-id="cc691-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cc691-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc691-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc691-116">Remarks</span></span>

<span data-ttu-id="cc691-117">Поставщик расположения не требуется для предоставления отчетов на запрошенный интервал.</span><span class="sxs-lookup"><span data-stu-id="cc691-117">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="cc691-118">Прочитайте значение свойства [**репортинтервал**](locationdisp-latlongreportfactory-reportinterval.md) , чтобы определить значение параметра интервала true Report.</span><span class="sxs-lookup"><span data-stu-id="cc691-118">Read the value of the [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="cc691-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="cc691-119">Examples</span></span>

<span data-ttu-id="cc691-120">Пример использования этого метода см. в разделе [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="cc691-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc691-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cc691-121">Requirements</span></span>



| <span data-ttu-id="cc691-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cc691-122">Requirement</span></span> | <span data-ttu-id="cc691-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cc691-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc691-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc691-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cc691-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cc691-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cc691-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc691-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cc691-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cc691-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="cc691-128">Header</span><span class="sxs-lookup"><span data-stu-id="cc691-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc691-129"><dt>Локатионапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc691-129"><dt>Locationapi.h</dt></span></span> </dl> |



 

