---
title: Уровень представления
description: Презентация — это заключительный этап процесса UPnP.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195399316882de71c148f2369dd2978c4cfbd728
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888195"
---
# <a name="presentation"></a><span data-ttu-id="15287-103">Уровень представления</span><span class="sxs-lookup"><span data-stu-id="15287-103">Presentation</span></span>

<span data-ttu-id="15287-104">Презентация — это заключительный этап процесса UPnP.</span><span class="sxs-lookup"><span data-stu-id="15287-104">Presentation is the final step in the UPnP process.</span></span> <span data-ttu-id="15287-105">Если у устройства есть URL-адрес для представления, контрольная точка может получить страницу с этого URL-адреса и загрузить страницу в браузер.</span><span class="sxs-lookup"><span data-stu-id="15287-105">If a device has a URL for presentation, a control point can retrieve a page from this URL and load the page into a browser.</span></span> <span data-ttu-id="15287-106">В зависимости от возможностей страницы презентации и устройства контрольная точка может управлять устройством и просматривать состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="15287-106">Depending on the capabilities of the presentation page and the device, the control point can control the device and view the status of the device.</span></span>

<span data-ttu-id="15287-107">Путь к ресурсу, который передается в [**иупнпрегистрар**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) во время регистрации, — это место, где находятся все файлы, относящиеся к презентации устройства.</span><span class="sxs-lookup"><span data-stu-id="15287-107">The resource path, which is passed to [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) during registration, is where all the files relevant to the presentation of the device are located.</span></span> <span data-ttu-id="15287-108">Разработчики устройств могут предоставлять отдельные страницы для каждого встраиваемого устройства.</span><span class="sxs-lookup"><span data-stu-id="15287-108">Device developers can provide separate pages for each embedded device.</span></span> <span data-ttu-id="15287-109">URL-адрес презентации в шаблоне описания устройства может быть абсолютным или относительным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="15287-109">The presentation URL in the device description template can either be an absolute URL or a relative URL.</span></span> <span data-ttu-id="15287-110">Для относительных URL-адресов, которые относятся к пути ресурса, шаблон описания устройства должен содержать имя файла.</span><span class="sxs-lookup"><span data-stu-id="15287-110">For relative URLs, which are relative to the resource path, the device description template should contain a file name.</span></span> <span data-ttu-id="15287-111">**Иупнпрегистрар** преобразует это значение в URL-адрес с фактическим расположением.</span><span class="sxs-lookup"><span data-stu-id="15287-111">**IUPnPRegistrar** converts this to a URL with the actual location.</span></span> <span data-ttu-id="15287-112">Для абсолютных URL-адресов расположение не изменяется.</span><span class="sxs-lookup"><span data-stu-id="15287-112">For absolute URLs, the location is not modified.</span></span>

<span data-ttu-id="15287-113">Для поддержки клиентских сценариев на странице презентации дополнительные сведения обычно добавляются к URL-адресу в форме строки запроса.</span><span class="sxs-lookup"><span data-stu-id="15287-113">To support client side scripts within a presentation page, extra information is normally appended to the URL in the form of a "query string".</span></span> <span data-ttu-id="15287-114">Дополнительные сведения, которые добавляются, — это URL-адрес документа описания устройства, а также УДН устройства или встроенного устройства.</span><span class="sxs-lookup"><span data-stu-id="15287-114">The extra information that is appended is the URL to the device description document, and the UDN of the device or embedded device.</span></span> <span data-ttu-id="15287-115">URL-адрес описания устройства можно использовать для загрузки документа описания в скрипт, а затем управлять устройством с помощью его служб.</span><span class="sxs-lookup"><span data-stu-id="15287-115">The device description URL can be used to load a description document in the script, and then control the device through its services.</span></span> <span data-ttu-id="15287-116">УДН используется для выбора встроенного устройства из корневого устройства.</span><span class="sxs-lookup"><span data-stu-id="15287-116">The UDN is used to select an embedded device from the root device.</span></span>

<span data-ttu-id="15287-117">Измененный URL-адрес презентации имеет следующий формат: фактический URL-адрес презентации, вопросительный знак ("?"), URL-адрес описания устройства, знак "плюс" ("+"), УДН устройства.</span><span class="sxs-lookup"><span data-stu-id="15287-117">The format of the modified presentation URL is: the actual presentation URL, a question mark ("?"), the device description URL, a plus sign ("+"), the device UDN.</span></span> <span data-ttu-id="15287-118">Вопросительный знак обозначает начало строки запроса.</span><span class="sxs-lookup"><span data-stu-id="15287-118">The question mark denotes the start of the query string.</span></span>

<span data-ttu-id="15287-119">Если URL-адрес презентации в шаблоне описания устройства был абсолютным URL-адресом и уже содержал вопросительный знак ("?"), дополнительные сведения не добавляются в URL-адрес презентации.</span><span class="sxs-lookup"><span data-stu-id="15287-119">If the presentation URL in the device description template was an absolute URL and it already contained a question mark ("?"), then the extra information is not added to the presentation URL.</span></span>



| <span data-ttu-id="15287-120">Описание</span><span class="sxs-lookup"><span data-stu-id="15287-120">Description</span></span>                        | <span data-ttu-id="15287-121">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="15287-121">URL</span></span>                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15287-122">В шаблоне описания устройства</span><span class="sxs-lookup"><span data-stu-id="15287-122">In the device description template</span></span> | <span data-ttu-id="15287-123">**пресентатионурл** MyDevice.html **/пресентатионурл**</span><span class="sxs-lookup"><span data-stu-id="15287-123">**presentationURL** MyDevice.html **/presentationURL**</span></span>                                                                                              |
| <span data-ttu-id="15287-124">Создано узлом устройства</span><span class="sxs-lookup"><span data-stu-id="15287-124">Generated by the device host</span></span>       | <span data-ttu-id="15287-125">**пресентатионурл** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ...</span><span class="sxs-lookup"><span data-stu-id="15287-125">**presentationURL**https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394…</span></span> <span data-ttu-id="15287-126">+ УДН **/пресентатионурл**</span><span class="sxs-lookup"><span data-stu-id="15287-126">+ UDN **/presentationURL**</span></span> |



 

<span data-ttu-id="15287-127">Для загрузки объекта [**иупнпдескриптиондокумент**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) клиентскому сценарию может потребоваться извлечь URL-адрес описания устройства из URL-адреса презентации.</span><span class="sxs-lookup"><span data-stu-id="15287-127">A client-side script may have to extract the device description URL from the presentation URL to load the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) object.</span></span> <span data-ttu-id="15287-128">Это делается путем получения строки запроса и ее завершения по знаку «плюс» («+»).</span><span class="sxs-lookup"><span data-stu-id="15287-128">This is done by taking the query string, and terminating it at the plus sign ("+").</span></span>


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



<span data-ttu-id="15287-129">В случае страницы презентации для встроенного устройства требуется дополнительная работа.</span><span class="sxs-lookup"><span data-stu-id="15287-129">In the case of a presentation page for an embedded device, some additional work is required.</span></span> <span data-ttu-id="15287-130">После загрузки [**упнпдескриптиондокумент**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)сценарий должен получить коллекцию встраиваемых устройств, а затем выбрать устройство, соответствующее УДН в строке запроса.</span><span class="sxs-lookup"><span data-stu-id="15287-130">After loading the [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), the script must obtain the collection of embedded devices, then select the device that matches the UDN in the query string.</span></span> <span data-ttu-id="15287-131">В следующем сценарии показано, как выбрать встроенное устройство для текущей страницы презентации.</span><span class="sxs-lookup"><span data-stu-id="15287-131">The following script shows how to select the embedded device for the current presentation page.</span></span> <span data-ttu-id="15287-132">Предполагается, что Лигхтдеск уже загружен.</span><span class="sxs-lookup"><span data-stu-id="15287-132">It assumes LightDesc is already loaded.</span></span>


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




