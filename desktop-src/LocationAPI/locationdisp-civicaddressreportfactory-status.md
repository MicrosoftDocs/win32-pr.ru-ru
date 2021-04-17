---
description: Текущее состояние отчета.
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: Локатиондисп. Цивикаддрессрепортфактори. status, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: ff937b11fbb64e0ec1596f9b3b9d85b33528eb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684550"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a><span data-ttu-id="dbc04-103">Локатиондисп. Цивикаддрессрепортфактори. status, свойство</span><span class="sxs-lookup"><span data-stu-id="dbc04-103">LocationDisp.CivicAddressReportFactory.Status property</span></span>

<span data-ttu-id="dbc04-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="dbc04-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dbc04-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="dbc04-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="dbc04-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbc04-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="dbc04-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="dbc04-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="dbc04-108">Текущее состояние отчета.</span><span class="sxs-lookup"><span data-stu-id="dbc04-108">The current report status.</span></span>

<span data-ttu-id="dbc04-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dbc04-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc04-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbc04-110">Syntax</span></span>


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="dbc04-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dbc04-111">Property value</span></span>

<span data-ttu-id="dbc04-112">Это свойство является **числом** только для чтения (длинное целое).</span><span class="sxs-lookup"><span data-stu-id="dbc04-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="dbc04-113">Состояние</span><span class="sxs-lookup"><span data-stu-id="dbc04-113">Status</span></span>                                                                                               | <span data-ttu-id="dbc04-114">Значение</span><span class="sxs-lookup"><span data-stu-id="dbc04-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="dbc04-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="dbc04-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="dbc04-116">Отчет не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dbc04-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="dbc04-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dbc04-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dbc04-118">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="dbc04-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="dbc04-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dbc04-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dbc04-120">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="dbc04-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="dbc04-121"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="dbc04-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="dbc04-122">Инициализация.</span><span class="sxs-lookup"><span data-stu-id="dbc04-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="dbc04-123"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="dbc04-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="dbc04-124">Выполняется.</span><span class="sxs-lookup"><span data-stu-id="dbc04-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="dbc04-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="dbc04-125">Examples</span></span>

<span data-ttu-id="dbc04-126">Пример использования этого свойства см. в разделе [прослушивание событий административного адреса](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="dbc04-126">For an example of how to use this property, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc04-127">Требования</span><span class="sxs-lookup"><span data-stu-id="dbc04-127">Requirements</span></span>



| <span data-ttu-id="dbc04-128">Требование</span><span class="sxs-lookup"><span data-stu-id="dbc04-128">Requirement</span></span> | <span data-ttu-id="dbc04-129">Значение</span><span class="sxs-lookup"><span data-stu-id="dbc04-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="dbc04-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbc04-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc04-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dbc04-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dbc04-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbc04-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc04-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dbc04-133">None supported</span></span><br/>                  |



 

