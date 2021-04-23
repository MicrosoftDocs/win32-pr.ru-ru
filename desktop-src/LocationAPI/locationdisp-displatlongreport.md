---
description: Представляет отчет широты и долготы.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: Локатиондисп. Дисплатлонгрепорт, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684546"
---
# <a name="locationdispdisplatlongreport-object"></a><span data-ttu-id="95605-103">Локатиондисп. Дисплатлонгрепорт, объект</span><span class="sxs-lookup"><span data-stu-id="95605-103">LocationDisp.DispLatLongReport object</span></span>

<span data-ttu-id="95605-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="95605-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="95605-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="95605-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="95605-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="95605-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="95605-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="95605-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="95605-108">Представляет отчет широты и долготы.</span><span class="sxs-lookup"><span data-stu-id="95605-108">Represents a latitude/longitude report.</span></span>

## <a name="members"></a><span data-ttu-id="95605-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="95605-109">Members</span></span>

<span data-ttu-id="95605-110">Объект **локатиондисп. дисплатлонгрепорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="95605-110">The **LocationDisp.DispLatLongReport** object has these types of members:</span></span>

-   [<span data-ttu-id="95605-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="95605-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95605-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="95605-112">Properties</span></span>

<span data-ttu-id="95605-113">Объект **локатиондисп. дисплатлонгрепорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="95605-113">The **LocationDisp.DispLatLongReport** object has these properties.</span></span>



| <span data-ttu-id="95605-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="95605-114">Property</span></span>                                                                         | <span data-ttu-id="95605-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="95605-115">Access type</span></span>          | <span data-ttu-id="95605-116">Описание</span><span class="sxs-lookup"><span data-stu-id="95605-116">Description</span></span>                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95605-117">**Высота над уровнем моря**</span><span class="sxs-lookup"><span data-stu-id="95605-117">**Altitude**</span></span>](locationdisp-displatlongreport-altitude.md)<br/>           | <span data-ttu-id="95605-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="95605-118">Read-only</span></span><br/> | <span data-ttu-id="95605-119">Текущая высота (в метрах).</span><span class="sxs-lookup"><span data-stu-id="95605-119">Current altitude, in meters.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="95605-120">**алтитудиррор**</span><span class="sxs-lookup"><span data-stu-id="95605-120">**AltitudeError**</span></span>](locationdisp-displatlongreport-altitudeerror.md)<br/> | <span data-ttu-id="95605-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="95605-121">Read-only</span></span><br/> | <span data-ttu-id="95605-122">Ошибка высоты, в метрах.</span><span class="sxs-lookup"><span data-stu-id="95605-122">Altitude error, in meters.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="95605-123">**ерроррадиус**</span><span class="sxs-lookup"><span data-stu-id="95605-123">**ErrorRadius**</span></span>](locationdisp-displatlongreport-errorradius.md)<br/>     | <span data-ttu-id="95605-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="95605-124">Read-only</span></span><br/> | <span data-ttu-id="95605-125">Расстояние от сообщаемого места в метрах.</span><span class="sxs-lookup"><span data-stu-id="95605-125">A distance from the reported location, in meters.</span></span> <span data-ttu-id="95605-126">В сочетании с исходным расположением в качестве источника этот радиус описывает круг, в котором находится фактическое расположение проабли.</span><span class="sxs-lookup"><span data-stu-id="95605-126">Combined with the reported location as the origin, this radius describes the circle in which the actual location is proably located.</span></span><br/> |
| [<span data-ttu-id="95605-127">**Широта**</span><span class="sxs-lookup"><span data-stu-id="95605-127">**Latitude**</span></span>](locationdisp-displatlongreport-latitude.md)<br/>           | <span data-ttu-id="95605-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="95605-128">Read-only</span></span><br/> | <span data-ttu-id="95605-129">Текущая Широта в градусах.</span><span class="sxs-lookup"><span data-stu-id="95605-129">Current latitude, in degrees.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="95605-130">**Долгот**</span><span class="sxs-lookup"><span data-stu-id="95605-130">**Longitude**</span></span>](locationdisp-displatlongreport-longitude.md)<br/>         | <span data-ttu-id="95605-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="95605-131">Read-only</span></span><br/> | <span data-ttu-id="95605-132">Текущая Долгота (в градусах).</span><span class="sxs-lookup"><span data-stu-id="95605-132">Current longitude, in degrees.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="95605-133">**Отметка времени**</span><span class="sxs-lookup"><span data-stu-id="95605-133">**Timestamp**</span></span>](locationdisp-displatlongreport-timestamp.md)<br/>         | <span data-ttu-id="95605-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="95605-134">Read-only</span></span><br/> | <span data-ttu-id="95605-135">Дата и время создания отчета.</span><span class="sxs-lookup"><span data-stu-id="95605-135">The date and time when the report was generated.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="95605-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95605-136">Remarks</span></span>

<span data-ttu-id="95605-137">Этот объект можно получить с помощью свойства [**латлонгрепорт**](locationdisp-latlongreportfactory-latlongreport.md) объекта [**латлонгрепортфактори**](locationdisp-latlongreportfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="95605-137">You can retrieve this object through the [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) property of the [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) object.</span></span> <span data-ttu-id="95605-138">Этот объект можно получить с помощью события [**невлатлонгрепорт**](newlatlongreport.md) .</span><span class="sxs-lookup"><span data-stu-id="95605-138">You can receive this object through the [**NewLatLongReport**](newlatlongreport.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="95605-139">Требования</span><span class="sxs-lookup"><span data-stu-id="95605-139">Requirements</span></span>



| <span data-ttu-id="95605-140">Требование</span><span class="sxs-lookup"><span data-stu-id="95605-140">Requirement</span></span> | <span data-ttu-id="95605-141">Значение</span><span class="sxs-lookup"><span data-stu-id="95605-141">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="95605-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95605-142">Minimum supported client</span></span><br/> | <span data-ttu-id="95605-143">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="95605-143">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="95605-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95605-144">Minimum supported server</span></span><br/> | <span data-ttu-id="95605-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="95605-145">None supported</span></span><br/>                  |



 

