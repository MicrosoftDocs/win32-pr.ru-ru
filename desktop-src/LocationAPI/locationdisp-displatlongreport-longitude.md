---
description: Текущая Долгота (в градусах).
ms.assetid: f4fa1cbb-d682-42ab-9dd8-dff636ea4c8a
title: Свойство Локатиондисп. Дисплатлонгрепорт. долготы
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Longitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: c705ebd9476582f05b6dc87233dcc8e8990c5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684548"
---
# <a name="locationdispdisplatlongreportlongitude-property"></a><span data-ttu-id="152af-103">Свойство Локатиондисп. Дисплатлонгрепорт. долготы</span><span class="sxs-lookup"><span data-stu-id="152af-103">LocationDisp.DispLatLongReport.Longitude property</span></span>

<span data-ttu-id="152af-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="152af-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="152af-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="152af-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="152af-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="152af-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="152af-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="152af-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="152af-108">Текущая Долгота (в градусах).</span><span class="sxs-lookup"><span data-stu-id="152af-108">Current longitude, in degrees.</span></span> <span data-ttu-id="152af-109">Долгота находится в диапазоне от-180 до 180, где Восток — положительное значение.</span><span class="sxs-lookup"><span data-stu-id="152af-109">The longitude is between -180 and 180, where east is positive.</span></span>

<span data-ttu-id="152af-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="152af-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="152af-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="152af-111">Syntax</span></span>


```JScript
Longitude = LocationDisp.DispLatLongReport.Longitude
```



## <a name="property-value"></a><span data-ttu-id="152af-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="152af-112">Property value</span></span>

<span data-ttu-id="152af-113">Это свойство доступно только для чтения ( **число** с плавающей запятой двойной точности).</span><span class="sxs-lookup"><span data-stu-id="152af-113">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="152af-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="152af-114">Examples</span></span>

<span data-ttu-id="152af-115">Пример использования этого свойства см. [в примере простого отчета LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="152af-115">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="152af-116">Требования</span><span class="sxs-lookup"><span data-stu-id="152af-116">Requirements</span></span>



| <span data-ttu-id="152af-117">Требование</span><span class="sxs-lookup"><span data-stu-id="152af-117">Requirement</span></span> | <span data-ttu-id="152af-118">Значение</span><span class="sxs-lookup"><span data-stu-id="152af-118">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="152af-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="152af-119">Minimum supported client</span></span><br/> | <span data-ttu-id="152af-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="152af-120">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="152af-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="152af-121">Minimum supported server</span></span><br/> | <span data-ttu-id="152af-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="152af-122">None supported</span></span><br/>                  |



 

