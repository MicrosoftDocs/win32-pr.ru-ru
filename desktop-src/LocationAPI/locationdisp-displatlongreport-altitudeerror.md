---
description: Ошибка высоты, в метрах.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: Локатиондисп. Дисплатлонгрепорт. Алтитудиррор, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92fd71b133912a57e6ed4ef034dda6fe92ef9b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910991"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a><span data-ttu-id="eee57-103">Локатиондисп. Дисплатлонгрепорт. Алтитудиррор, свойство</span><span class="sxs-lookup"><span data-stu-id="eee57-103">LocationDisp.DispLatLongReport.AltitudeError property</span></span>

<span data-ttu-id="eee57-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="eee57-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eee57-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="eee57-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="eee57-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eee57-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="eee57-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="eee57-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="eee57-108">Ошибка высоты, в метрах.</span><span class="sxs-lookup"><span data-stu-id="eee57-108">Altitude error, in meters.</span></span>

<span data-ttu-id="eee57-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eee57-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eee57-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eee57-110">Syntax</span></span>


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a><span data-ttu-id="eee57-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="eee57-111">Property value</span></span>

<span data-ttu-id="eee57-112">Это свойство доступно только для чтения ( **число** с плавающей запятой двойной точности).</span><span class="sxs-lookup"><span data-stu-id="eee57-112">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="eee57-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eee57-113">Remarks</span></span>

<span data-ttu-id="eee57-114">Датчики расположения не являются обязательными для предоставления этого свойства.</span><span class="sxs-lookup"><span data-stu-id="eee57-114">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="eee57-115">При попытке доступа к этому свойству следует обращаться к исключениям.</span><span class="sxs-lookup"><span data-stu-id="eee57-115">You should handle exceptions when attempting to access this property.</span></span>

## <a name="examples"></a><span data-ttu-id="eee57-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="eee57-116">Examples</span></span>

<span data-ttu-id="eee57-117">Пример использования этого свойства см. [в примере простого отчета LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="eee57-117">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="eee57-118">Требования</span><span class="sxs-lookup"><span data-stu-id="eee57-118">Requirements</span></span>



| <span data-ttu-id="eee57-119">Требование</span><span class="sxs-lookup"><span data-stu-id="eee57-119">Requirement</span></span> | <span data-ttu-id="eee57-120">Значение</span><span class="sxs-lookup"><span data-stu-id="eee57-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="eee57-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eee57-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eee57-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eee57-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="eee57-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eee57-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eee57-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="eee57-124">None supported</span></span><br/>                  |



 

