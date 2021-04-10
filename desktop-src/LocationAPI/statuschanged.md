---
description: Происходит при изменении оперативного состояния отчета.
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: Событие Статусчанжед
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273117"
---
# <a name="statuschanged-event"></a><span data-ttu-id="4dda8-103">Событие Статусчанжед</span><span class="sxs-lookup"><span data-stu-id="4dda8-103">StatusChanged event</span></span>

<span data-ttu-id="4dda8-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4dda8-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4dda8-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="4dda8-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="4dda8-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4dda8-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="4dda8-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="4dda8-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="4dda8-108">Происходит при изменении оперативного состояния отчета.</span><span class="sxs-lookup"><span data-stu-id="4dda8-108">Occurs when the operational status of a report changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dda8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4dda8-109">Syntax</span></span>


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a><span data-ttu-id="4dda8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4dda8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dda8-111">*status*</span><span class="sxs-lookup"><span data-stu-id="4dda8-111">*status*</span></span> 
</dt> <dd>

<span data-ttu-id="4dda8-112">Новое состояние.</span><span class="sxs-lookup"><span data-stu-id="4dda8-112">The new status.</span></span>



| <span data-ttu-id="4dda8-113">Состояние</span><span class="sxs-lookup"><span data-stu-id="4dda8-113">Status</span></span>                                                                                               | <span data-ttu-id="4dda8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4dda8-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="4dda8-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="4dda8-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="4dda8-116">Отчет не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4dda8-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="4dda8-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4dda8-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4dda8-118">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="4dda8-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="4dda8-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4dda8-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4dda8-120">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="4dda8-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="4dda8-121"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="4dda8-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="4dda8-122">Инициализация.</span><span class="sxs-lookup"><span data-stu-id="4dda8-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="4dda8-123"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="4dda8-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4dda8-124">Выполняется.</span><span class="sxs-lookup"><span data-stu-id="4dda8-124">Running.</span></span><br/>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dda8-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4dda8-125">Return value</span></span>

<span data-ttu-id="4dda8-126">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4dda8-126">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dda8-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4dda8-127">Remarks</span></span>

<span data-ttu-id="4dda8-128">Необходимо реализовать отдельные обработчики отчетов об изменении состояния для отчетов об административном адресе и в отчетах широты и долготы.</span><span class="sxs-lookup"><span data-stu-id="4dda8-128">You should implement separate status change report handlers for civic address reports and latitude/longitude reports.</span></span>

## <a name="examples"></a><span data-ttu-id="4dda8-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="4dda8-129">Examples</span></span>

<span data-ttu-id="4dda8-130">Пример использования этого события см. в разделе [Listening for LatLong Reports Events](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="4dda8-130">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="4dda8-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4dda8-131">Requirements</span></span>



| <span data-ttu-id="4dda8-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4dda8-132">Requirement</span></span> | <span data-ttu-id="4dda8-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4dda8-133">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="4dda8-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4dda8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4dda8-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4dda8-135">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4dda8-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4dda8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4dda8-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4dda8-137">None supported</span></span><br/>                  |



 

