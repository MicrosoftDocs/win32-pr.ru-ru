---
description: Управляет отчетами широты и долготы.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: Локатиондисп. Латлонгрепортфактори, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913511"
---
# <a name="locationdisplatlongreportfactory-object"></a><span data-ttu-id="70c30-103">Локатиондисп. Латлонгрепортфактори, объект</span><span class="sxs-lookup"><span data-stu-id="70c30-103">LocationDisp.LatLongReportFactory object</span></span>

<span data-ttu-id="70c30-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="70c30-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="70c30-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="70c30-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="70c30-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70c30-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="70c30-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="70c30-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="70c30-108">Управляет отчетами широты и долготы.</span><span class="sxs-lookup"><span data-stu-id="70c30-108">Manages latitude/longitude reports.</span></span>

## <a name="members"></a><span data-ttu-id="70c30-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="70c30-109">Members</span></span>

<span data-ttu-id="70c30-110">Объект **локатиондисп. латлонгрепортфактори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="70c30-110">The **LocationDisp.LatLongReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="70c30-111">Методы</span><span class="sxs-lookup"><span data-stu-id="70c30-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="70c30-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="70c30-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="70c30-113">Методы</span><span class="sxs-lookup"><span data-stu-id="70c30-113">Methods</span></span>

<span data-ttu-id="70c30-114">Объект **локатиондисп. латлонгрепортфактори** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="70c30-114">The **LocationDisp.LatLongReportFactory** object has these methods.</span></span>



| <span data-ttu-id="70c30-115">Метод</span><span class="sxs-lookup"><span data-stu-id="70c30-115">Method</span></span>                                                                                       | <span data-ttu-id="70c30-116">Описание</span><span class="sxs-lookup"><span data-stu-id="70c30-116">Description</span></span>                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70c30-117">**листенфоррепортс**</span><span class="sxs-lookup"><span data-stu-id="70c30-117">**ListenForReports**</span></span>](locationdisp-latlongreportfactory-listenforreports.md)               | <span data-ttu-id="70c30-118">Запрашивает события отчета широты и долготы.</span><span class="sxs-lookup"><span data-stu-id="70c30-118">Requests latitude/longitude report events.</span></span><br/>                                         |
| [<span data-ttu-id="70c30-119">**рекуестпермиссионс**</span><span class="sxs-lookup"><span data-stu-id="70c30-119">**RequestPermissions**</span></span>](locationdisp-latlongreportfactory-requestpermissions.md)           | <span data-ttu-id="70c30-120">Открывает диалоговое окно системы, в котором запрашиваются разрешения пользователя для устройств с поддержкой расположения.</span><span class="sxs-lookup"><span data-stu-id="70c30-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| <span data-ttu-id="70c30-121">[**стоплистенингфоррепортс**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="70c30-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span></span> | <span data-ttu-id="70c30-122">Отменяет запросы на события отчета широты и долготы.</span><span class="sxs-lookup"><span data-stu-id="70c30-122">Cancels requests for latitude/longitude report events.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="70c30-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="70c30-123">Properties</span></span>

<span data-ttu-id="70c30-124">Объект **локатиондисп. латлонгрепортфактори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="70c30-124">The **LocationDisp.LatLongReportFactory** object has these properties.</span></span>



| <span data-ttu-id="70c30-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="70c30-125">Property</span></span>                                                                                | <span data-ttu-id="70c30-126">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="70c30-126">Access type</span></span>           | <span data-ttu-id="70c30-127">Описание</span><span class="sxs-lookup"><span data-stu-id="70c30-127">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70c30-128">**десиредаккураци**</span><span class="sxs-lookup"><span data-stu-id="70c30-128">**DesiredAccuracy**</span></span>](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | <span data-ttu-id="70c30-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="70c30-129">Read/write</span></span><br/> | <span data-ttu-id="70c30-130">Текущее значение требуемой точности.</span><span class="sxs-lookup"><span data-stu-id="70c30-130">The current desired-accuracy value.</span></span><br/>                                                   |
| [<span data-ttu-id="70c30-131">**латлонгрепорт**</span><span class="sxs-lookup"><span data-stu-id="70c30-131">**LatLongReport**</span></span>](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | <span data-ttu-id="70c30-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70c30-132">Read-only</span></span><br/>  | <span data-ttu-id="70c30-133">Текущий [**локатиондисп. дисплатлонгрепорт**](locationdisp-displatlongreport.md).</span><span class="sxs-lookup"><span data-stu-id="70c30-133">The current [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span><br/> |
| [<span data-ttu-id="70c30-134">**репортинтервал**</span><span class="sxs-lookup"><span data-stu-id="70c30-134">**ReportInterval**</span></span>](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | <span data-ttu-id="70c30-135">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="70c30-135">Read/write</span></span><br/> | <span data-ttu-id="70c30-136">Текущий интервал событий для отчета широты и долготы в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="70c30-136">The current latitude/longitude report event interval in milliseconds.</span></span><br/>                 |
| [<span data-ttu-id="70c30-137">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="70c30-137">**Status**</span></span>](locationdisp-latlongreportfactory-status.md)<br/>                   | <span data-ttu-id="70c30-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70c30-138">Read-only</span></span><br/>  | <span data-ttu-id="70c30-139">Текущее состояние отчета.</span><span class="sxs-lookup"><span data-stu-id="70c30-139">The current report status.</span></span><br/>                                                            |



 

## <a name="examples"></a><span data-ttu-id="70c30-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="70c30-140">Examples</span></span>

<span data-ttu-id="70c30-141">В следующем примере кода показано, как создать этот объект в HTML-коде.</span><span class="sxs-lookup"><span data-stu-id="70c30-141">The following example code shows how to create this object in HTML code.</span></span>


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="70c30-142">В следующем примере кода показано, как создать этот объект в JScript с помощью сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="70c30-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



<span data-ttu-id="70c30-143">В следующем примере кода показано, как создать этот объект в VBScript с помощью сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="70c30-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="70c30-144">Требования</span><span class="sxs-lookup"><span data-stu-id="70c30-144">Requirements</span></span>



| <span data-ttu-id="70c30-145">Требование</span><span class="sxs-lookup"><span data-stu-id="70c30-145">Requirement</span></span> | <span data-ttu-id="70c30-146">Значение</span><span class="sxs-lookup"><span data-stu-id="70c30-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="70c30-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70c30-147">Minimum supported client</span></span><br/> | <span data-ttu-id="70c30-148">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="70c30-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="70c30-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70c30-149">Minimum supported server</span></span><br/> | <span data-ttu-id="70c30-150">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="70c30-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="70c30-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70c30-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c30-152">**Локатиондисп. Дисплатлонгрепорт**</span><span class="sxs-lookup"><span data-stu-id="70c30-152">**LocationDisp.DispLatLongReport**</span></span>](locationdisp-displatlongreport.md)
</dt> </dl>

 

