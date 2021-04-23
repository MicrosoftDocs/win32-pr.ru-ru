---
description: Останавливает события административного адреса.
ms.assetid: 6efe26bc-842d-49fc-aec2-e0dfa7f1eb0a
title: Метод Локатиондисп. Цивикаддрессрепортфактори. Стоплистенингфоррепортс (Локатионапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.StopListeningForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 36c58e9db0edb66735dcbd58c8e1968cfa8b1fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684549"
---
# <a name="locationdispcivicaddressreportfactorystoplisteningforreports-method"></a><span data-ttu-id="0bb7e-103">Локатиондисп. Цивикаддрессрепортфактори. Стоплистенингфоррепортс, метод</span><span class="sxs-lookup"><span data-stu-id="0bb7e-103">LocationDisp.CivicAddressReportFactory.StopListeningForReports method</span></span>

<span data-ttu-id="0bb7e-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0bb7e-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0bb7e-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="0bb7e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0bb7e-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0bb7e-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="0bb7e-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="0bb7e-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="0bb7e-108">Останавливает события административного адреса.</span><span class="sxs-lookup"><span data-stu-id="0bb7e-108">Stops civic address report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb7e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bb7e-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.StopListeningForReports()
```



## <a name="parameters"></a><span data-ttu-id="0bb7e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bb7e-110">Parameters</span></span>

<span data-ttu-id="0bb7e-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0bb7e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0bb7e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bb7e-112">Return value</span></span>

<span data-ttu-id="0bb7e-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0bb7e-113">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="0bb7e-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="0bb7e-114">Examples</span></span>

<span data-ttu-id="0bb7e-115">Пример использования этого метода см. в разделе [прослушивание событий административного адреса](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="0bb7e-115">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb7e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0bb7e-116">Requirements</span></span>



| <span data-ttu-id="0bb7e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0bb7e-117">Requirement</span></span> | <span data-ttu-id="0bb7e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0bb7e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb7e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0bb7e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb7e-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0bb7e-120">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0bb7e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0bb7e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb7e-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0bb7e-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0bb7e-123">Header</span><span class="sxs-lookup"><span data-stu-id="0bb7e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bb7e-124"><dt>Локатионапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bb7e-124"><dt>Locationapi.h</dt></span></span> </dl> |



 

