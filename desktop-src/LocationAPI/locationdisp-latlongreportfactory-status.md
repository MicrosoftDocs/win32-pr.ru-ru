---
description: Свойство Локатиондисп. Латлонгрепортфактори. status — текущее состояние отчета.
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: Локатиондисп. Латлонгрепортфактори. status, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 37e66c3f289f5376b31ffe516f45d79f2fef51e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088902"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a><span data-ttu-id="c071f-103">Локатиондисп. Латлонгрепортфактори. status, свойство</span><span class="sxs-lookup"><span data-stu-id="c071f-103">LocationDisp.LatLongReportFactory.Status property</span></span>

<span data-ttu-id="c071f-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="c071f-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c071f-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="c071f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c071f-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c071f-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="c071f-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="c071f-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="c071f-108">Текущее состояние отчета.</span><span class="sxs-lookup"><span data-stu-id="c071f-108">The current report status.</span></span>

<span data-ttu-id="c071f-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c071f-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c071f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c071f-110">Syntax</span></span>


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="c071f-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c071f-111">Property value</span></span>

<span data-ttu-id="c071f-112">Это свойство является **числом** только для чтения (длинное целое).</span><span class="sxs-lookup"><span data-stu-id="c071f-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="c071f-113">Состояние</span><span class="sxs-lookup"><span data-stu-id="c071f-113">Status</span></span>                                                                                               | <span data-ttu-id="c071f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c071f-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="c071f-115"><dt>**0,0**</dt></span><span class="sxs-lookup"><span data-stu-id="c071f-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="c071f-116">Отчет не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c071f-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="c071f-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c071f-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c071f-118">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="c071f-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="c071f-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c071f-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c071f-120">Access denied. (Недопустимое значение {значение_утверждения} для утверждения {имя_утверждения}. Доступ запрещен.)</span><span class="sxs-lookup"><span data-stu-id="c071f-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="c071f-121"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="c071f-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c071f-122">Инициализация.</span><span class="sxs-lookup"><span data-stu-id="c071f-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="c071f-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c071f-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c071f-124">Выполняется.</span><span class="sxs-lookup"><span data-stu-id="c071f-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="c071f-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="c071f-125">Examples</span></span>

<span data-ttu-id="c071f-126">Пример использования этого свойства см. в разделе [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="c071f-126">For an example of how to use this property, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="c071f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c071f-127">Requirements</span></span>



| <span data-ttu-id="c071f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c071f-128">Requirement</span></span> | <span data-ttu-id="c071f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c071f-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="c071f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c071f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c071f-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c071f-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c071f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c071f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c071f-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c071f-133">None supported</span></span><br/>                  |



 

