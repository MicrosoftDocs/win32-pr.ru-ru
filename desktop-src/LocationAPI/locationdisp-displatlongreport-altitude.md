---
description: Текущая высота (в метрах). Высота задается относительно ссылки на эллипсоида.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: Локатиондисп. Дисплатлонгрепорт. Высота, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910096"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a><span data-ttu-id="6ceab-104">Локатиондисп. Дисплатлонгрепорт. Высота, свойство</span><span class="sxs-lookup"><span data-stu-id="6ceab-104">LocationDisp.DispLatLongReport.Altitude property</span></span>

<span data-ttu-id="6ceab-105">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="6ceab-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6ceab-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="6ceab-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6ceab-107">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6ceab-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="6ceab-108">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="6ceab-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="6ceab-109">Текущая высота (в метрах).</span><span class="sxs-lookup"><span data-stu-id="6ceab-109">Current altitude, in meters.</span></span> <span data-ttu-id="6ceab-110">Высота задается относительно ссылки на эллипсоида.</span><span class="sxs-lookup"><span data-stu-id="6ceab-110">Altitude is relative to the reference ellipsoid.</span></span>

<span data-ttu-id="6ceab-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6ceab-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ceab-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ceab-112">Syntax</span></span>


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a><span data-ttu-id="6ceab-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6ceab-113">Property value</span></span>

<span data-ttu-id="6ceab-114">Это свойство доступно только для чтения ( **число** с плавающей запятой двойной точности).</span><span class="sxs-lookup"><span data-stu-id="6ceab-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="6ceab-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ceab-115">Remarks</span></span>

<span data-ttu-id="6ceab-116">Датчики расположения не являются обязательными для предоставления этого свойства.</span><span class="sxs-lookup"><span data-stu-id="6ceab-116">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="6ceab-117">При попытке доступа к этому свойству следует обращаться к исключениям.</span><span class="sxs-lookup"><span data-stu-id="6ceab-117">You should handle exceptions when attempting to access this property.</span></span>

<span data-ttu-id="6ceab-118">Метод **высоты** Получает высоту, отличную от ссылочной эллипсоида, которая определяется последней редакцией геодезическийной системы (WGS 84), а не высотой, отличной от уровня Sea.</span><span class="sxs-lookup"><span data-stu-id="6ceab-118">The **Altitude** method retrieves the altitude relative to the reference ellipsoid that is defined by the latest revision of the World Geodetic System (WGS 84), rather than the altitude relative to sea level.</span></span>

## <a name="examples"></a><span data-ttu-id="6ceab-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="6ceab-119">Examples</span></span>

<span data-ttu-id="6ceab-120">Пример использования этого свойства см. [в примере простого отчета LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="6ceab-120">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ceab-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6ceab-121">Requirements</span></span>



| <span data-ttu-id="6ceab-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6ceab-122">Requirement</span></span> | <span data-ttu-id="6ceab-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceab-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="6ceab-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ceab-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6ceab-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6ceab-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6ceab-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ceab-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6ceab-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6ceab-127">None supported</span></span><br/>                  |



 

