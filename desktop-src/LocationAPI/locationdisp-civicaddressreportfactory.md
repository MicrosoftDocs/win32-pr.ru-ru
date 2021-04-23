---
description: Управляет отчетами об административном адресе.
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: Локатиондисп. Цивикаддрессрепортфактори, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 451bb21822d1b56e4c7a45f1587df04761b67690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816064"
---
# <a name="locationdispcivicaddressreportfactory-object"></a><span data-ttu-id="9ad65-103">Локатиондисп. Цивикаддрессрепортфактори, объект</span><span class="sxs-lookup"><span data-stu-id="9ad65-103">LocationDisp.CivicAddressReportFactory object</span></span>

<span data-ttu-id="9ad65-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9ad65-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9ad65-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="9ad65-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9ad65-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9ad65-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="9ad65-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="9ad65-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="9ad65-108">Управляет отчетами об административном адресе.</span><span class="sxs-lookup"><span data-stu-id="9ad65-108">Manages civic address reports.</span></span>

## <a name="members"></a><span data-ttu-id="9ad65-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="9ad65-109">Members</span></span>

<span data-ttu-id="9ad65-110">Объект **локатиондисп. Цивикаддрессрепортфактори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9ad65-110">The **LocationDisp.CivicAddressReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="9ad65-111">Методы</span><span class="sxs-lookup"><span data-stu-id="9ad65-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9ad65-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ad65-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9ad65-113">Методы</span><span class="sxs-lookup"><span data-stu-id="9ad65-113">Methods</span></span>

<span data-ttu-id="9ad65-114">Объект **локатиондисп. Цивикаддрессрепортфактори** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9ad65-114">The **LocationDisp.CivicAddressReportFactory** object has these methods.</span></span>



| <span data-ttu-id="9ad65-115">Метод</span><span class="sxs-lookup"><span data-stu-id="9ad65-115">Method</span></span>                                                                                            | <span data-ttu-id="9ad65-116">Описание</span><span class="sxs-lookup"><span data-stu-id="9ad65-116">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ad65-117">**листенфоррепортс**</span><span class="sxs-lookup"><span data-stu-id="9ad65-117">**ListenForReports**</span></span>](locationdisp-civicaddressreportfactory-listenforreports.md)               | <span data-ttu-id="9ad65-118">Запрашивает события об административном адресе.</span><span class="sxs-lookup"><span data-stu-id="9ad65-118">Requests civic address report events.</span></span><br/>                                              |
| [<span data-ttu-id="9ad65-119">**рекуестпермиссионс**</span><span class="sxs-lookup"><span data-stu-id="9ad65-119">**RequestPermissions**</span></span>](locationdisp-civicaddressreportfactory-requestpermissions.md)           | <span data-ttu-id="9ad65-120">Открывает диалоговое окно системы, в котором запрашиваются разрешения пользователя для устройств с поддержкой расположения.</span><span class="sxs-lookup"><span data-stu-id="9ad65-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| [<span data-ttu-id="9ad65-121">**стоплистенингфоррепортс**</span><span class="sxs-lookup"><span data-stu-id="9ad65-121">**StopListeningForReports**</span></span>](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | <span data-ttu-id="9ad65-122">Отменяет запросы событий для отчетов об административном адресе.</span><span class="sxs-lookup"><span data-stu-id="9ad65-122">Cancels civic address report event requests.</span></span><br/>                                       |



 

### <a name="properties"></a><span data-ttu-id="9ad65-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ad65-123">Properties</span></span>

<span data-ttu-id="9ad65-124">Объект **локатиондисп. Цивикаддрессрепортфактори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9ad65-124">The **LocationDisp.CivicAddressReportFactory** object has these properties.</span></span>



| <span data-ttu-id="9ad65-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="9ad65-125">Property</span></span>                                                                                        | <span data-ttu-id="9ad65-126">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="9ad65-126">Access type</span></span>           | <span data-ttu-id="9ad65-127">Описание</span><span class="sxs-lookup"><span data-stu-id="9ad65-127">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ad65-128">**Цивикаддрессрепорт**</span><span class="sxs-lookup"><span data-stu-id="9ad65-128">**CivicAddressReport**</span></span>](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | <span data-ttu-id="9ad65-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ad65-129">Read-only</span></span><br/>  | <span data-ttu-id="9ad65-130">Текущий [**локатиондисп. диспЦивикаддрессрепорт**](locationdisp-dispcivicaddressreport.md).</span><span class="sxs-lookup"><span data-stu-id="9ad65-130">The current [**LocationDisp.DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md).</span></span><br/> |
| [<span data-ttu-id="9ad65-131">**десиредаккураци**</span><span class="sxs-lookup"><span data-stu-id="9ad65-131">**DesiredAccuracy**</span></span>](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | <span data-ttu-id="9ad65-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9ad65-132">Read/write</span></span><br/> | <span data-ttu-id="9ad65-133">Текущее значение требуемой точности.</span><span class="sxs-lookup"><span data-stu-id="9ad65-133">The current desired-accuracy setting.</span></span><br/>                                                           |
| [<span data-ttu-id="9ad65-134">**репортинтервал**</span><span class="sxs-lookup"><span data-stu-id="9ad65-134">**ReportInterval**</span></span>](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | <span data-ttu-id="9ad65-135">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9ad65-135">Read/write</span></span><br/> | <span data-ttu-id="9ad65-136">Текущий интервал событий для отчета об административном адресе в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="9ad65-136">The current civic address report event interval in milliseconds.</span></span><br/>                                |
| [<span data-ttu-id="9ad65-137">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9ad65-137">**Status**</span></span>](locationdisp-civicaddressreportfactory-status.md)<br/>                      | <span data-ttu-id="9ad65-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ad65-138">Read-only</span></span><br/>  | <span data-ttu-id="9ad65-139">Текущее состояние отчета.</span><span class="sxs-lookup"><span data-stu-id="9ad65-139">The current report status.</span></span><br/>                                                                      |



 

## <a name="examples"></a><span data-ttu-id="9ad65-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="9ad65-140">Examples</span></span>

<span data-ttu-id="9ad65-141">В следующем примере кода показано, как создать этот объект в HTML-коде.</span><span class="sxs-lookup"><span data-stu-id="9ad65-141">The following example code shows how to create this object in HTML code.</span></span>


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="9ad65-142">В следующем примере кода показано, как создать этот объект в JScript с помощью сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="9ad65-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



<span data-ttu-id="9ad65-143">В следующем примере кода показано, как создать этот объект в VBScript с помощью сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="9ad65-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="9ad65-144">Требования</span><span class="sxs-lookup"><span data-stu-id="9ad65-144">Requirements</span></span>



| <span data-ttu-id="9ad65-145">Требование</span><span class="sxs-lookup"><span data-stu-id="9ad65-145">Requirement</span></span> | <span data-ttu-id="9ad65-146">Значение</span><span class="sxs-lookup"><span data-stu-id="9ad65-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="9ad65-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ad65-147">Minimum supported client</span></span><br/> | <span data-ttu-id="9ad65-148">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9ad65-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9ad65-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ad65-149">Minimum supported server</span></span><br/> | <span data-ttu-id="9ad65-150">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9ad65-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="9ad65-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ad65-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ad65-152">**Локатиондисп. Цивикаддрессрепорт**</span><span class="sxs-lookup"><span data-stu-id="9ad65-152">**LocationDisp.CivicAddressReport**</span></span>](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

