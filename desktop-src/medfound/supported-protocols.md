---
description: Поддерживаемые протоколы
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Поддерживаемые протоколы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e618f47a1ffc4a81c36e48407b93da54d7d532f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811530"
---
# <a name="supported-protocols"></a><span data-ttu-id="7cc83-103">Поддерживаемые протоколы</span><span class="sxs-lookup"><span data-stu-id="7cc83-103">Supported Protocols</span></span>

<span data-ttu-id="7cc83-104">Media Foundation поддерживает следующие протоколы:</span><span class="sxs-lookup"><span data-stu-id="7cc83-104">Media Foundation supports the following protocols:</span></span>

-   <span data-ttu-id="7cc83-105">Протокол передачи данных в реальном времени (RTSP)</span><span class="sxs-lookup"><span data-stu-id="7cc83-105">Real Time Streaming Protocol (RTSP)</span></span>

    <span data-ttu-id="7cc83-106">Протокол RTSP используется в основном для потоковой передачи мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="7cc83-106">RTSP is mainly used for streaming media content.</span></span> <span data-ttu-id="7cc83-107">Он может использовать UDP или TCP в качестве транспортных протоколов.</span><span class="sxs-lookup"><span data-stu-id="7cc83-107">It can use UDP or TCP as transport protocols.</span></span> <span data-ttu-id="7cc83-108">Протокол UDP наиболее эффективен для доставки содержимого, так как затраты на пропускную способность меньше, чем при использовании протоколов TCP.</span><span class="sxs-lookup"><span data-stu-id="7cc83-108">UDP is the most efficient for content delivery because the bandwidth overhead is less than with TCP-based protocols.</span></span> <span data-ttu-id="7cc83-109">Хотя протокол TCP гарантирует надежную доставку пакетов, протокол TCP не подходит для цифровых мультимедийных потоков, где эффективное использование пропускной способности является более важным, чем случайные потерянные пакеты.</span><span class="sxs-lookup"><span data-stu-id="7cc83-109">Even though the TCP protocol ensures reliable packet delivery, TCP is not well suited for digital media streams, where efficient use of bandwidth is more important than occasional lost packets.</span></span>

-   <span data-ttu-id="7cc83-110">Протокол HTTP</span><span class="sxs-lookup"><span data-stu-id="7cc83-110">Hypertext Transfer Protocol (HTTP)</span></span>

    <span data-ttu-id="7cc83-111">Протокол HTTP использует протокол TCP и используется веб-серверами.</span><span class="sxs-lookup"><span data-stu-id="7cc83-111">HTTP uses TCP and is used by web servers.</span></span> <span data-ttu-id="7cc83-112">Схема "httpd://" указывает, что источник доступен для загрузки с веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="7cc83-112">The "httpd://" scheme indicates that the source is downloadable from a web server.</span></span> <span data-ttu-id="7cc83-113">Протокол HTTP также используется в случае брандмауэров, которые обычно настроены для приема HTTP-запросов и обычно отклоняют другие протоколы потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="7cc83-113">HTTP is also used in case of firewalls, which are usually configured to accept HTTP requests and typically reject other streaming protocols.</span></span>

<span data-ttu-id="7cc83-114">Приложение может получать протоколы, поддерживаемые Media Foundation с помощью интерфейса [**имфнетсчемехандлерконфиг**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) .</span><span class="sxs-lookup"><span data-stu-id="7cc83-114">The application can get the protocols supported by Media Foundation by using the [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) interface.</span></span> <span data-ttu-id="7cc83-115">Для этого приложение должно сначала получить количество протоколов, вызвав [**имфнетсчемехандлерконфиг:: жетнумберофсуппортедпротоколс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) , а затем получить тип протокола на основе индекса, вызвав [**Имфнетсчемехандлерконфиг:: GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span><span class="sxs-lookup"><span data-stu-id="7cc83-115">To do this, the application must first retrieve the number of protocols, by calling [**IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) and then get the protocol type based on the index by calling [**IMFNetSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span></span> <span data-ttu-id="7cc83-116">Этот метод возвращает одно из значений, определенных в перечислении [**\_ \_ типа протокола мфнетсаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="7cc83-116">This method returns one of the values defined in the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>

<span data-ttu-id="7cc83-117">Приложение также может получить схемы, поддерживаемые распознавателем источников, вызвав функцию [**мфжетсуппортедсчемес**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) .</span><span class="sxs-lookup"><span data-stu-id="7cc83-117">The application can also get the schemes supported by the source resolver by calling the [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) function.</span></span>

## <a name="protocol-rollover"></a><span data-ttu-id="7cc83-118">Смена протокола</span><span class="sxs-lookup"><span data-stu-id="7cc83-118">Protocol Rollover</span></span>

<span data-ttu-id="7cc83-119">Если в приложении в качестве схемы URL-адреса указано "mms://", сопоставитель источника выполняет операцию *смены протокола* .</span><span class="sxs-lookup"><span data-stu-id="7cc83-119">When an application specifies "mms://" as the URL scheme, the source resolver performs a *protocol rollover* operation.</span></span> <span data-ttu-id="7cc83-120">В этом процессе сопоставитель источника определяет оптимальный протокол, используемый сетевым источником для получения содержимого.</span><span class="sxs-lookup"><span data-stu-id="7cc83-120">In this process, the source resolver determines the best protocol for the network source to use for getting the content.</span></span> <span data-ttu-id="7cc83-121">Как правило, для потоковой передаче мультимедиа протокол RTSP с UDP (РТСПУ) более эффективен, чем HTTP.</span><span class="sxs-lookup"><span data-stu-id="7cc83-121">Typically, for media steaming, RTSP with UDP (RTSPU) is more efficient than HTTP.</span></span> <span data-ttu-id="7cc83-122">Однако если содержимое размещено на веб-сервере, лучше выбрать HTTP.</span><span class="sxs-lookup"><span data-stu-id="7cc83-122">However, if the content is hosted on a web server, HTTP is a better choice.</span></span>

<span data-ttu-id="7cc83-123">Смена протокола также может возникать, если попытка использования протокола, указанного в схеме URL-адреса, завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7cc83-123">Protocol rollover can also occur when an attempt to use the protocol specified in the URL scheme fails.</span></span> <span data-ttu-id="7cc83-124">Например, протокол может завершиться ошибкой, если брандмауэр блокирует пакеты UDP.</span><span class="sxs-lookup"><span data-stu-id="7cc83-124">For example, a protocol can fail when a firewall blocks UDP packets.</span></span> <span data-ttu-id="7cc83-125">В этом случае сопоставитель источника переключается на HTTP.</span><span class="sxs-lookup"><span data-stu-id="7cc83-125">In this case, the source resolver switches to HTTP.</span></span>

<span data-ttu-id="7cc83-126">Переключение протокола не применяется, если схема URL-адресов содержит конкретный протокол, например "rtspu://".</span><span class="sxs-lookup"><span data-stu-id="7cc83-126">Protocol rollover does not apply if the URL scheme contains a specific protocol, such as "rtspu://".</span></span> <span data-ttu-id="7cc83-127">Кроме того, смена не выполняется в случае сбоя проверки подлинности или превышения сервером ограничения на количество клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="7cc83-127">Also, rollover is not performed if authentication fails or the server has reached a limit of client connections.</span></span> <span data-ttu-id="7cc83-128">Рекомендуется, чтобы приложения указали схему "mms://" и позволяли распознавателю источников выбрать оптимальный протокол для сценария.</span><span class="sxs-lookup"><span data-stu-id="7cc83-128">It is recommended that applications specify the "mms://" scheme and allow the source resolver to select the best protocol for the scenario.</span></span>

<span data-ttu-id="7cc83-129">В следующей таблице приводится порядок переключения.</span><span class="sxs-lookup"><span data-stu-id="7cc83-129">The following table lists the rollover order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cc83-130">Разрешенные схемы</span><span class="sxs-lookup"><span data-stu-id="7cc83-130">Schemes allowed</span></span></th>
<th><span data-ttu-id="7cc83-131">Порядок переключения протоколов</span><span class="sxs-lookup"><span data-stu-id="7cc83-131">Protocol rollover order</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cc83-132">mms://или rtsp://</span><span class="sxs-lookup"><span data-stu-id="7cc83-132">mms:// or rtsp://</span></span></td>
<td><span data-ttu-id="7cc83-133">Быстрый кэш включен:</span><span class="sxs-lookup"><span data-stu-id="7cc83-133">Fast Cache enabled:</span></span><br/>
<ol>
<li><span data-ttu-id="7cc83-134">Протокол RTSP с TCP (RTSP)</span><span class="sxs-lookup"><span data-stu-id="7cc83-134">RTSP with TCP (RTSPT)</span></span><br/></li>
<li><span data-ttu-id="7cc83-135">RTSP с UDP (РТСПУ)</span><span class="sxs-lookup"><span data-stu-id="7cc83-135">RTSP with UDP (RTSPU)</span></span><br/></li>
<li><span data-ttu-id="7cc83-136">Потоковая передача HTTP</span><span class="sxs-lookup"><span data-stu-id="7cc83-136">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="7cc83-137">Загрузка HTTP (HTTPD)</span><span class="sxs-lookup"><span data-stu-id="7cc83-137">HTTP download (HTTPD)</span></span><br/></li>
</ol>
<span data-ttu-id="7cc83-138">Быстрый кэш отключен:</span><span class="sxs-lookup"><span data-stu-id="7cc83-138">Fast Cache disabled:</span></span><br/>
<ol>
<li><span data-ttu-id="7cc83-139">ртспу</span><span class="sxs-lookup"><span data-stu-id="7cc83-139">RTSPU</span></span><br/></li>
<li><span data-ttu-id="7cc83-140">RTSP</span><span class="sxs-lookup"><span data-stu-id="7cc83-140">RTSPT</span></span><br/></li>
<li><span data-ttu-id="7cc83-141">Потоковая передача HTTP</span><span class="sxs-lookup"><span data-stu-id="7cc83-141">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="7cc83-142">Загрузка HTTP</span><span class="sxs-lookup"><span data-stu-id="7cc83-142">HTTP Download</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cc83-143">rtspu://</span><span class="sxs-lookup"><span data-stu-id="7cc83-143">rtspu://</span></span></td>
<td><span data-ttu-id="7cc83-144">ртспу</span><span class="sxs-lookup"><span data-stu-id="7cc83-144">RTSPU</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cc83-145">rtspt://</span><span class="sxs-lookup"><span data-stu-id="7cc83-145">rtspt://</span></span></td>
<td><span data-ttu-id="7cc83-146">RTSP</span><span class="sxs-lookup"><span data-stu-id="7cc83-146">RTSPT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cc83-147"> https://</span><span class="sxs-lookup"><span data-stu-id="7cc83-147">https://</span></span></td>
<td><ol>
<li><span data-ttu-id="7cc83-148">HTTP</span><span class="sxs-lookup"><span data-stu-id="7cc83-148">HTTP</span></span><br/></li>
<li><span data-ttu-id="7cc83-149">HTTPD</span><span class="sxs-lookup"><span data-stu-id="7cc83-149">HTTPD</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cc83-150">httpd://</span><span class="sxs-lookup"><span data-stu-id="7cc83-150">httpd://</span></span></td>
<td><span data-ttu-id="7cc83-151">HTTPD</span><span class="sxs-lookup"><span data-stu-id="7cc83-151">HTTPD</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a><span data-ttu-id="7cc83-152">Получение текущего протокола</span><span class="sxs-lookup"><span data-stu-id="7cc83-152">Retrieving the Current Protocol</span></span>

<span data-ttu-id="7cc83-153">После операции переключения протокола сетевой источник может использовать протокол, отличный от указанного приложением в схеме URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7cc83-153">After a protocol rollover operation, the network source might use a protocol other than the one specified by the application in the URL scheme.</span></span> <span data-ttu-id="7cc83-154">Результат переключения протокола будет доступен для приложения после того, как источник сети установит подключение к серверу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7cc83-154">The protocol rollover result is available to the application after the network source establishes the connection with the media server.</span></span>

<span data-ttu-id="7cc83-155">Чтобы получить протокол и транспорт, которые используются для получения содержимого, приложение может получить значения свойств [ \_ протокола мфнетсаурце](mfnetsource-protocol-property.md) и свойства [ \_ Transport мфнетсаурце](mfnetsource-transport-property.md) объекта **ипропертисторе** из сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="7cc83-155">To get the protocol and transport that are used for getting the content, the application can retrieve the property values for the [MFNETSOURCE\_PROTOCOL](mfnetsource-protocol-property.md) property and the [MFNETSOURCE\_TRANSPORT](mfnetsource-transport-property.md) property of an **IPropertyStore** object from the network source.</span></span>

<span data-ttu-id="7cc83-156">В следующем коде показано, как получить эти значения.</span><span class="sxs-lookup"><span data-stu-id="7cc83-156">The following code shows how to get these values.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



<span data-ttu-id="7cc83-157">В предыдущем примере кода **ипропертисторе:: GetValue** получает \_ значение протокола мфнетсаурце, которое является членом перечисления [**\_ \_ типа протокола мфнетсаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="7cc83-157">In the preceding example code, **IPropertyStore::GetValue** retrieves the MFNETSOURCE\_PROTOCOL value, which is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span> <span data-ttu-id="7cc83-158">Для \_ транспорта мфнетсаурце значение является членом перечисления [**\_ \_ типа транспорта мфнетсаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .</span><span class="sxs-lookup"><span data-stu-id="7cc83-158">For MFNETSOURCE\_TRANSPORT, the value is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>

<span data-ttu-id="7cc83-159">Кроме того, приложение может получить те же значения с помощью \_ службы статистики мфнетсаурце \_ .</span><span class="sxs-lookup"><span data-stu-id="7cc83-159">Alternately, the application can get the same values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span> <span data-ttu-id="7cc83-160">Чтобы использовать эту службу, приложение может вызвать функцию [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) для получения хранилища свойств из сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="7cc83-160">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store from the network source.</span></span> <span data-ttu-id="7cc83-161">Это хранилище свойств содержит статистику сети в свойстве [ \_ статистики мфнетсаурце](mfnetsource-statistics-property.md) .</span><span class="sxs-lookup"><span data-stu-id="7cc83-161">This property store contains network statistics in the [MFNETSOURCE\_STATISTICS](mfnetsource-statistics-property.md) property.</span></span> <span data-ttu-id="7cc83-162">Значения протокола и транспорта можно получить, указав \_ идентификатор протокола мфнетсаурце \_ и \_ идентификатор транспорта мфнетсаурце \_ , определенные в перечислении [**\_ \_ идентификаторов мфнетсаурце Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) .</span><span class="sxs-lookup"><span data-stu-id="7cc83-162">Protocol and transport values can be retrieved by specifying MFNETSOURCE\_PROTOCOL\_ID and MFNETSOURCE\_TRANSPORT\_ID—defined in the [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enumeration.</span></span> <span data-ttu-id="7cc83-163">В следующем коде показано, как получить значения протокола и транспорта с помощью \_ службы статистики мфнетсаурце \_ .</span><span class="sxs-lookup"><span data-stu-id="7cc83-163">The following code shows how to get the protocol and transport values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a><span data-ttu-id="7cc83-164">Включение и отключение протоколов</span><span class="sxs-lookup"><span data-stu-id="7cc83-164">Enabling and Disabling Protocols</span></span>

<span data-ttu-id="7cc83-165">Приложение может настроить источник сети таким образом, чтобы определенные протоколы пропускались в процессе переключения.</span><span class="sxs-lookup"><span data-stu-id="7cc83-165">The application can configure the network source so that certain protocols are skipped during the rollover process.</span></span> <span data-ttu-id="7cc83-166">Для этого свойства источника сети используются для отключения конкретных протоколов.</span><span class="sxs-lookup"><span data-stu-id="7cc83-166">To do this, network source properties are used to disable specific protocols.</span></span> <span data-ttu-id="7cc83-167">В следующей таблице показаны свойства и протоколы, которыми они управляют.</span><span class="sxs-lookup"><span data-stu-id="7cc83-167">The following table shows the properties and the protocols they control.</span></span>



| <span data-ttu-id="7cc83-168">Свойство</span><span class="sxs-lookup"><span data-stu-id="7cc83-168">Property</span></span>                                                                    | <span data-ttu-id="7cc83-169">Описание</span><span class="sxs-lookup"><span data-stu-id="7cc83-169">Description</span></span>                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="7cc83-170">МФНЕТСАУРЦЕ \_ включить \_ http</span><span class="sxs-lookup"><span data-stu-id="7cc83-170">MFNETSOURCE\_ENABLE\_HTTP</span></span>](mfnetsource-enable-http-property.md)           | <span data-ttu-id="7cc83-171">Включает или отключает протоколы HTTP и HTTPD.</span><span class="sxs-lookup"><span data-stu-id="7cc83-171">Enables or disables HTTP and HTTPD.</span></span>         |
| [<span data-ttu-id="7cc83-172">МФНЕТСАУРЦЕ \_ Включение \_ RTSP</span><span class="sxs-lookup"><span data-stu-id="7cc83-172">MFNETSOURCE\_ENABLE\_RTSP</span></span>](mfnetsource-enable-rtsp-property.md)           | <span data-ttu-id="7cc83-173">Включает или отключает РТСПУ и RTSP.</span><span class="sxs-lookup"><span data-stu-id="7cc83-173">Enables or disables RTSPU and RTSPT.</span></span>        |
| [<span data-ttu-id="7cc83-174">МФНЕТСАУРЦЕ \_ включить \_ TCP</span><span class="sxs-lookup"><span data-stu-id="7cc83-174">MFNETSOURCE\_ENABLE\_TCP</span></span>](mfnetsource-enable-tcp-property.md)             | <span data-ttu-id="7cc83-175">Включает или отключает протокол RTSP.</span><span class="sxs-lookup"><span data-stu-id="7cc83-175">Enables or disables RTSPT.</span></span>                  |
| [<span data-ttu-id="7cc83-176">МФНЕТСАУРЦЕ \_ включить \_ UDP</span><span class="sxs-lookup"><span data-stu-id="7cc83-176">MFNETSOURCE\_ENABLE\_UDP</span></span>](mfnetsource-enable-udp-property.md)             | <span data-ttu-id="7cc83-177">Включает или отключает РТСПУ.</span><span class="sxs-lookup"><span data-stu-id="7cc83-177">Enables or disables RTSPU.</span></span>                  |
| [<span data-ttu-id="7cc83-178">МФНЕТСАУРЦЕ \_ включить \_ скачивание</span><span class="sxs-lookup"><span data-stu-id="7cc83-178">MFNETSOURCE\_ENABLE\_DOWNLOAD</span></span>](mfnetsource-enable-download-property.md)   | <span data-ttu-id="7cc83-179">Включает или отключает HTTPD.</span><span class="sxs-lookup"><span data-stu-id="7cc83-179">Enables or disables HTTPD.</span></span>                  |
| [<span data-ttu-id="7cc83-180">МФНЕТСАУРЦЕ \_ включить \_ потоковую передачу</span><span class="sxs-lookup"><span data-stu-id="7cc83-180">MFNETSOURCE\_ENABLE\_STREAMING</span></span>](mfnetsource-enable-streaming-property.md) | <span data-ttu-id="7cc83-181">Включает или отключает РТСПУ, RTSP и HTTP.</span><span class="sxs-lookup"><span data-stu-id="7cc83-181">Enables or disables RTSPU, RTSPT, and HTTP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7cc83-182">См. также</span><span class="sxs-lookup"><span data-stu-id="7cc83-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cc83-183">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7cc83-183">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




