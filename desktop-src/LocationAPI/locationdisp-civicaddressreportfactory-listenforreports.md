---
description: Запрашивает события об административном адресе.
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: Метод Локатиондисп. Цивикаддрессрепортфактори. Листенфоррепортс (Локатионапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 02315f8b2f7fced76c3d0d1330df246af6bad4b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999599"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a><span data-ttu-id="f0ff0-103">Локатиондисп. Цивикаддрессрепортфактори. Листенфоррепортс, метод</span><span class="sxs-lookup"><span data-stu-id="f0ff0-103">LocationDisp.CivicAddressReportFactory.ListenForReports method</span></span>

<span data-ttu-id="f0ff0-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f0ff0-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f0ff0-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f0ff0-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f0ff0-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0ff0-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="f0ff0-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="f0ff0-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="f0ff0-108">Запрашивает события об административном адресе.</span><span class="sxs-lookup"><span data-stu-id="f0ff0-108">Requests civic address report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ff0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0ff0-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="f0ff0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0ff0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ff0-111">*рекуестедрепортинтервал*</span><span class="sxs-lookup"><span data-stu-id="f0ff0-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="f0ff0-112">Число (**двойное слово**), представляющее запрошенное время между событиями отчета об административном адресе (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="f0ff0-112">Number (**double word**) representing the requested time between civic address report events, in milliseconds.</span></span> <span data-ttu-id="f0ff0-113">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="f0ff0-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0ff0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0ff0-114">Return value</span></span>

<span data-ttu-id="f0ff0-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f0ff0-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0ff0-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0ff0-116">Remarks</span></span>

<span data-ttu-id="f0ff0-117">Поставщик расположения не требуется для предоставления точности, которую вы запрашиваете.</span><span class="sxs-lookup"><span data-stu-id="f0ff0-117">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="f0ff0-118">Прочитайте значение свойства [**репортинтервал**](locationdisp-civicaddressreportfactory-reportinterval.md) , чтобы определить значение параметра интервала true Report.</span><span class="sxs-lookup"><span data-stu-id="f0ff0-118">Read the value of the [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="f0ff0-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="f0ff0-119">Examples</span></span>

<span data-ttu-id="f0ff0-120">Пример использования этого метода см. в разделе [прослушивание событий административного адреса](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="f0ff0-120">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ff0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f0ff0-121">Requirements</span></span>



| <span data-ttu-id="f0ff0-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f0ff0-122">Requirement</span></span> | <span data-ttu-id="f0ff0-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f0ff0-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ff0-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0ff0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ff0-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f0ff0-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f0ff0-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0ff0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ff0-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f0ff0-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f0ff0-128">Header</span><span class="sxs-lookup"><span data-stu-id="f0ff0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ff0-129"><dt>Локатионапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0ff0-129"><dt>Locationapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ff0-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0ff0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ff0-131">**Событие НевЦивикаддрессрепорт**</span><span class="sxs-lookup"><span data-stu-id="f0ff0-131">**NewCivicAddressReport Event**</span></span>](newcivicaddressreport.md)
</dt> </dl>

 

