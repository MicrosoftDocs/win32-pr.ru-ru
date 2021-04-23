---
description: Текущая Широта в градусах.
ms.assetid: 24a4e75c-5162-406a-bf34-471387bff5d9
title: Локатиондисп. Дисплатлонгрепорт. Широта, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Latitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7f1bb6e7441b4e007c972f43bb45f59236ebe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674221"
---
# <a name="locationdispdisplatlongreportlatitude-property"></a><span data-ttu-id="87e7e-103">Локатиондисп. Дисплатлонгрепорт. Широта, свойство</span><span class="sxs-lookup"><span data-stu-id="87e7e-103">LocationDisp.DispLatLongReport.Latitude property</span></span>

<span data-ttu-id="87e7e-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="87e7e-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="87e7e-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="87e7e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="87e7e-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="87e7e-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="87e7e-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="87e7e-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="87e7e-108">Текущая Широта в градусах.</span><span class="sxs-lookup"><span data-stu-id="87e7e-108">Current latitude, in degrees.</span></span> <span data-ttu-id="87e7e-109">Широта находится в диапазоне от-90 до 90, где Север является положительным.</span><span class="sxs-lookup"><span data-stu-id="87e7e-109">The latitude is between -90 and 90, where north is positive.</span></span>

<span data-ttu-id="87e7e-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="87e7e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e7e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87e7e-111">Syntax</span></span>


```JScript
Latitude = LocationDisp.DispLatLongReport.Latitude
```



## <a name="property-value"></a><span data-ttu-id="87e7e-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="87e7e-112">Property value</span></span>

<span data-ttu-id="87e7e-113">Это свойство доступно только для чтения ( **число** с плавающей запятой двойной точности).</span><span class="sxs-lookup"><span data-stu-id="87e7e-113">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="87e7e-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="87e7e-114">Examples</span></span>

<span data-ttu-id="87e7e-115">Пример использования этого свойства см. [в примере простого отчета LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="87e7e-115">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="87e7e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="87e7e-116">Requirements</span></span>



| <span data-ttu-id="87e7e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="87e7e-117">Requirement</span></span> | <span data-ttu-id="87e7e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="87e7e-118">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="87e7e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87e7e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="87e7e-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="87e7e-120">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="87e7e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87e7e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="87e7e-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="87e7e-122">None supported</span></span><br/>                  |



 

