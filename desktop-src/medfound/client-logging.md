---
description: Дополнительные сведения о ведении журнала клиента для Microsoft Media Foundation. Ведение журнала позволяет серверу мультимедиа отвести наблюдение за активностью клиентов, подключающихся к нему.
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Ведение журнала клиента (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d994531ff16466054ca0645a35082a4845e4aa4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409937"
---
# <a name="client-logging-microsoft-media-foundation"></a><span data-ttu-id="1c917-104">Ведение журнала клиента (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="1c917-104">Client Logging (Microsoft Media Foundation)</span></span>

<span data-ttu-id="1c917-105">Сетевой источник поддерживает ведение журнала клиента, что позволяет серверу мультимедиа отвести наблюдение за активностью клиентов, подключающихся к нему.</span><span class="sxs-lookup"><span data-stu-id="1c917-105">The network source supports client logging, which provides a way for the media server to track the activity of the clients that connect to it.</span></span> <span data-ttu-id="1c917-106">Журналы клиента позволяют серверу записывать статистику подключения, подготовки к просмотру и потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="1c917-106">Client logs enable a server to record connection, rendering, and streaming statistics.</span></span> <span data-ttu-id="1c917-107">Эти журналы могут использоваться поставщиками содержимого в различных сценариях, например, для трассировки использования сервера мультимедиа и формирования счетов, а также для предоставления подходящего содержимого в зависимости от скорости сети клиента.</span><span class="sxs-lookup"><span data-stu-id="1c917-107">These logs can be used by content providers in various scenarios, such as, to trace media server usage and generate billing, or to deliver suitable-quality content depending on the speed of the client's network.</span></span>

<span data-ttu-id="1c917-108">Файл журнала содержит несколько записей о клиентских событиях.</span><span class="sxs-lookup"><span data-stu-id="1c917-108">A log file contains several client event entries.</span></span> <span data-ttu-id="1c917-109">Каждая запись журнала содержит несколько полей, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="1c917-109">Each log entry contains a number of space-delimited fields.</span></span> <span data-ttu-id="1c917-110">Существует два типа журналов клиента: *отрисовка* (воспроизведение) и *потоковая передача* (получение).</span><span class="sxs-lookup"><span data-stu-id="1c917-110">There are two types of client logs: *rendering* (playing) and *streaming* (receiving).</span></span> <span data-ttu-id="1c917-111">Так как содержимое может воспроизводиться и передаваться одновременно, клиент может отправить сочетание обоих типов данных журнала.</span><span class="sxs-lookup"><span data-stu-id="1c917-111">Because content can be played and streamed simultaneously, the client can send a combination of both types of log data.</span></span> <span data-ttu-id="1c917-112">В некоторых случаях для одного сеанса могут существовать две записи журнала.</span><span class="sxs-lookup"><span data-stu-id="1c917-112">In certain cases, two log entries can exist for the same session.</span></span> <span data-ttu-id="1c917-113">Например, если включен быстрый кэш, клиент может завершить получение потокового содержимого до завершения его подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="1c917-113">For example, when Fast Cache is enabled, the client can finish receiving the streamed content before it finishes rendering it.</span></span> <span data-ttu-id="1c917-114">В этом случае данные журнала потоковой передачи будут отправляться перед отрисовкой данных журнала.</span><span class="sxs-lookup"><span data-stu-id="1c917-114">In that case, the streaming log data would be sent before the rendering log data.</span></span>

<span data-ttu-id="1c917-115">Клиент отправляет данные журнала отрисовки на сервер, когда клиент меняется с любого воспроизводимого состояния (воспроизведение, перемотка вперед или назад) на воспроизводимое состояние (остановка, пауза, конец потока и начало потока).</span><span class="sxs-lookup"><span data-stu-id="1c917-115">The client sends rendering log data to the server when the client changes from any playing state (play, fast-forward, or rewind) to a non-playing state (stop, pause, end of stream, and beginning of stream).</span></span> <span data-ttu-id="1c917-116">При отправке данных для журнала отрисовки подключение устанавливается непосредственно на сервер мультимедиа или настроенный прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="1c917-116">When data for a rendering log is submitted, a connection is made directly to the media server or a configured proxy server.</span></span>

<span data-ttu-id="1c917-117">Если содержимое хранится во временном локальном кэше на компьютере, на котором выполняется клиент, клиент может прочитать файл из своего локального кэша и отправить данные журнала отрисовки, чтобы указать, что он воспроизводил содержимое.</span><span class="sxs-lookup"><span data-stu-id="1c917-117">If the content is stored in a temporary local cache file on the computer that is running the client, the client can read a file from its local cache and submit the rendering log data to indicate that it has played the content.</span></span> <span data-ttu-id="1c917-118">В этом случае клиент считывает файл из своего локального кэша, запись журнала подготовки отчетов не содержит никакой статистики сети, а для протокола задано значение Cache.</span><span class="sxs-lookup"><span data-stu-id="1c917-118">In this case, the client reads a file from its local cache, the rendering log entry does not contain any network statistics, and the protocol is set to Cache.</span></span>

<span data-ttu-id="1c917-119">Клиент отправляет потоковые данные журнала на сервер, чтобы указать, как клиент получил содержимое, но не как он был визуализирован.</span><span class="sxs-lookup"><span data-stu-id="1c917-119">The client sends streaming log data to the server to indicate how the client received the content, but not how it was rendered.</span></span> <span data-ttu-id="1c917-120">Клиент может отправить журнал потоковой передачи до тех пор, пока клиент не завершит отрисовку содержимого.</span><span class="sxs-lookup"><span data-stu-id="1c917-120">The client can send the streaming log long before the client finishes rendering the content.</span></span>

<span data-ttu-id="1c917-121">В этом разделе не приводятся сведения обо всех полях журнала.</span><span class="sxs-lookup"><span data-stu-id="1c917-121">This topic does not provide information about all the log fields.</span></span> <span data-ttu-id="1c917-122">Полный справочник см. в разделе [Структура данных журнала Windows Media](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span><span class="sxs-lookup"><span data-stu-id="1c917-122">For a complete reference, see [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span></span>

## <a name="configuring-log-fields"></a><span data-ttu-id="1c917-123">Настройка полей журнала</span><span class="sxs-lookup"><span data-stu-id="1c917-123">Configuring Log Fields</span></span>

<span data-ttu-id="1c917-124">Media Foundation позволяет клиенту настроить сетевой источник с помощью свойств.</span><span class="sxs-lookup"><span data-stu-id="1c917-124">Media Foundation enables the client to configure the network source by using properties.</span></span> <span data-ttu-id="1c917-125">Приложение должно задать соответствующие свойства в хранилище свойств и передать его одному из методов сопоставителя источника.</span><span class="sxs-lookup"><span data-stu-id="1c917-125">The application must set the appropriate properties in a property store and pass it to one of the source resolver methods.</span></span> <span data-ttu-id="1c917-126">Сопоставитель источника создает сетевой источник по запросу и открывает подключение к серверу.</span><span class="sxs-lookup"><span data-stu-id="1c917-126">The source resolver creates the network source as requested and opens a connection with the server.</span></span> <span data-ttu-id="1c917-127">Если соединение прошло успешно, клиент отправляет сведения о себе.</span><span class="sxs-lookup"><span data-stu-id="1c917-127">If the connection is successful, the client sends information about itself.</span></span>

<span data-ttu-id="1c917-128">В следующей таблице описаны поля журнала и соответствующие свойства, которые приложение может установить с помощью сопоставителя источников.</span><span class="sxs-lookup"><span data-stu-id="1c917-128">The following table describes the log fields and the corresponding properties that an application can set through the source resolver.</span></span> <span data-ttu-id="1c917-129">Эти сведения не изменяются во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="1c917-129">This information does not change during the session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c917-130">Поле ведения журнала</span><span class="sxs-lookup"><span data-stu-id="1c917-130">Logging field</span></span></th>
<th><span data-ttu-id="1c917-131">Описание</span><span class="sxs-lookup"><span data-stu-id="1c917-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c917-132">c-плайерид</span><span class="sxs-lookup"><span data-stu-id="1c917-132">c-playerid</span></span></td>
<td><span data-ttu-id="1c917-133">Уникальная идентификация проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="1c917-133">Unique identification of the player.</span></span> <span data-ttu-id="1c917-134">Эти сведения отправляются в начале соединения.</span><span class="sxs-lookup"><span data-stu-id="1c917-134">This information is sent at the beginning of the connection.</span></span> <span data-ttu-id="1c917-135">Как правило, это идентификатор GUID клиента.</span><span class="sxs-lookup"><span data-stu-id="1c917-135">Typically, this is a GUID of the client.</span></span> <span data-ttu-id="1c917-136">Клиент может отправить эти сведения на сервер в свойстве <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1c917-136">The client can send this information to the server in the <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> property.</span></span><br/> <span data-ttu-id="1c917-137">Клиент отправляет эти сведения на сервер в начале соединения.</span><span class="sxs-lookup"><span data-stu-id="1c917-137">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="1c917-138">Пример значения: &quot; {c579d042-CECC-11D1-bb31-00a0c9603954}&quot;</span><span class="sxs-lookup"><span data-stu-id="1c917-138">Sample value: &quot;{c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c917-139">c-плайерверсион</span><span class="sxs-lookup"><span data-stu-id="1c917-139">c-playerversion</span></span></td>
<td><span data-ttu-id="1c917-140">Номер версии проигрывателя, который отправляется в начале соединения.</span><span class="sxs-lookup"><span data-stu-id="1c917-140">The version number of the player that is sent at the beginning of the connection.</span></span> <span data-ttu-id="1c917-141">Клиент может отправить эти сведения на сервер в свойстве <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1c917-141">The client can send this information to the server in the <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="1c917-142">Клиент отправляет эти сведения на сервер в начале соединения.</span><span class="sxs-lookup"><span data-stu-id="1c917-142">The client sends this information to the server at the beginning of the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c917-143">CS (User-Agent)</span><span class="sxs-lookup"><span data-stu-id="1c917-143">cs(User-Agent)</span></span></td>
<td><span data-ttu-id="1c917-144">Тип браузера, используемый, если проигрыватель внедрен в браузер.</span><span class="sxs-lookup"><span data-stu-id="1c917-144">Browser type used if the player was embedded in a browser.</span></span> <span data-ttu-id="1c917-145">Это значение может быть задано клиентом в свойстве <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1c917-145">This value can be set by the client in the <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="1c917-146">Если проигрыватель не был внедрен, это поле относится к агенту пользователя клиента, который создал журнал.</span><span class="sxs-lookup"><span data-stu-id="1c917-146">If the player was not embedded, this field refers to the user agent of the client that generated the log.</span></span> <span data-ttu-id="1c917-147">В этом случае клиент должен задать свойство <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1c917-147">In this case, the client must set the <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="1c917-148">Клиент отправляет эти сведения на сервер в начале соединения.</span><span class="sxs-lookup"><span data-stu-id="1c917-148">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="1c917-149">Пример значения: &quot; Mozilla/4.0 _ (совместимый; _MSIE_4.01; _Windows_98)&quot;</span><span class="sxs-lookup"><span data-stu-id="1c917-149">Sample value: &quot;Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c917-150">CS (ссылка)</span><span class="sxs-lookup"><span data-stu-id="1c917-150">cs(Referer)</span></span></td>
<td><span data-ttu-id="1c917-151">URL-адрес веб-страницы, в которой был внедрен проигрыватель (если он был внедрен).</span><span class="sxs-lookup"><span data-stu-id="1c917-151">URL of the webpage in which the player was embedded (if it was embedded).</span></span> <span data-ttu-id="1c917-152">Клиент может отправить эти сведения на сервер в свойстве <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1c917-152">The client can send this information to the server in the <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> property.</span></span><br/> <span data-ttu-id="1c917-153">Клиент отправляет эти сведения на сервер в конце соединения.</span><span class="sxs-lookup"><span data-stu-id="1c917-153">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="1c917-154">Пример значения: &quot; https://www.example.microsoft.com&quot ;</span><span class="sxs-lookup"><span data-stu-id="1c917-154">Sample value: &quot;https://www.example.microsoft.com&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c917-155">c-хостексе</span><span class="sxs-lookup"><span data-stu-id="1c917-155">c-hostexe</span></span></td>
<td><span data-ttu-id="1c917-156">Для записей журнала проигрывателя — выполняемая управляющая программа (.exe).</span><span class="sxs-lookup"><span data-stu-id="1c917-156">For player log entries, the host program (.exe) that was run.</span></span> <span data-ttu-id="1c917-157">Например, веб-страница в браузере, приложение Microsoft Visual Basic или автономный проигрыватель.</span><span class="sxs-lookup"><span data-stu-id="1c917-157">For example, a webpage in a browser, a Microsoft Visual Basic applet, or a stand-alone player.</span></span> <span data-ttu-id="1c917-158">Клиент может отправить эти сведения на сервер в свойстве <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1c917-158">The client can send this information to the server in the <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> property.</span></span><br/> <span data-ttu-id="1c917-159">Клиент отправляет эти сведения на сервер в конце соединения.</span><span class="sxs-lookup"><span data-stu-id="1c917-159">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="1c917-160">Примеры значений:</span><span class="sxs-lookup"><span data-stu-id="1c917-160">Sample values:</span></span><br/>
<ul>
<li><span data-ttu-id="1c917-161">&quot;iexplore.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="1c917-161">&quot;iexplore.exe&quot;</span></span></li>
<li><span data-ttu-id="1c917-162">&quot;myplayer.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="1c917-162">&quot;myplayer.exe&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c917-163">c-хостексевер</span><span class="sxs-lookup"><span data-stu-id="1c917-163">c-hostexever</span></span></td>
<td><span data-ttu-id="1c917-164">Номер версии основной программы (.exe).</span><span class="sxs-lookup"><span data-stu-id="1c917-164">Host program (.exe) version number.</span></span> <span data-ttu-id="1c917-165">Клиент может отправить эти сведения на сервер в свойстве <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1c917-165">The client can send this information to the server in the <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="1c917-166">Клиент отправляет эти сведения на сервер в конце соединения.</span><span class="sxs-lookup"><span data-stu-id="1c917-166">The client sends this information to the server at the end of the connection.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1c917-167">В следующем примере кода показано, как клиентское приложение настраивает сетевой источник.</span><span class="sxs-lookup"><span data-stu-id="1c917-167">The following code example shows how a client application configures the network source.</span></span> <span data-ttu-id="1c917-168">В этом примере задается поле журнала c-хостексе.</span><span class="sxs-lookup"><span data-stu-id="1c917-168">This example sets the "c-hostexe" log field.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a><span data-ttu-id="1c917-169">Получение статистики сети</span><span class="sxs-lookup"><span data-stu-id="1c917-169">Retrieving Network Statistics</span></span>

<span data-ttu-id="1c917-170">Когда приложение вызывает один из методов сопоставителя источника, он создает источник сети, устанавливает свойства, указанные в хранилище свойств, и открывает сеанс на сервере мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1c917-170">When the application calls one of the source resolver methods, it creates the network source, sets the properties specified in the property store, and opens a session with the media server.</span></span> <span data-ttu-id="1c917-171">Помимо настраиваемых сведений, описанных в предыдущем разделе, дополнительные данные передаются между сервером и клиентом в начале сеанса, во время потоковой передачи и при закрытии сеанса.</span><span class="sxs-lookup"><span data-stu-id="1c917-171">In addition to the configurable information described in the previous section, additional data is transferred between the server and the client at the beginning of the session, during streaming, and when the session is closed.</span></span>

<span data-ttu-id="1c917-172">Приложение может получить сетевую статистику с помощью идентификатора службы **мфнетсаурце \_ Statistics \_ Service** .</span><span class="sxs-lookup"><span data-stu-id="1c917-172">The application can retrieve network statistics by using the **MFNETSOURCE\_STATISTICS\_SERVICE** service identifier.</span></span> <span data-ttu-id="1c917-173">Чтобы использовать эту службу, приложение может вызвать функцию [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) для получения хранилища свойств, содержащего сетевую статистику, в свойстве [**\_ статистики мфнетсаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) .</span><span class="sxs-lookup"><span data-stu-id="1c917-173">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store that contains network statistics in the [**MFNETSOURCE\_STATISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) property.</span></span> <span data-ttu-id="1c917-174">Конкретные значения можно получить, предоставив соответствующий идентификатор, определенный в перечислении **мфнетсаурце \_ Statistics \_ ID** .</span><span class="sxs-lookup"><span data-stu-id="1c917-174">Specific values can be retrieved by providing the corresponding identifier defined in the **MFNETSOURCE\_STATISTICS\_IDS** enumeration.</span></span>

<span data-ttu-id="1c917-175">В следующем примере кода показано, как использовать службу для получения числа пакетов, полученных клиентом.</span><span class="sxs-lookup"><span data-stu-id="1c917-175">The following code example shows how to use the service to get the number of packets received by the client.</span></span>


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



<span data-ttu-id="1c917-176">В следующем списке описаны некоторые идентификаторы сетевой статистики, определенные в [**мфнетсаурце \_ Statistics \_ ID**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="1c917-176">The following list describes some of the network statistics identifiers defined in [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>



| <span data-ttu-id="1c917-177">Идентификатор сетевой статистики</span><span class="sxs-lookup"><span data-stu-id="1c917-177">Network statistics identifier</span></span>              | <span data-ttu-id="1c917-178">Описание</span><span class="sxs-lookup"><span data-stu-id="1c917-178">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c917-179">**\_идентификатор АВГБАНДВИДСБПС \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-179">**MFNETSOURCE\_AVGBANDWIDTHBPS\_ID**</span></span>       | <span data-ttu-id="1c917-180">Средняя пропускная способность (в битах в секунду), с которой клиент был подключен к серверу.</span><span class="sxs-lookup"><span data-stu-id="1c917-180">Average bandwidth (in bits per second) at which the client was connected to the server.</span></span> <span data-ttu-id="1c917-181">Значение вычисляется в течение всей продолжительности соединения.</span><span class="sxs-lookup"><span data-stu-id="1c917-181">The value is calculated across the entire duration of the connection.</span></span>                                                              |
| <span data-ttu-id="1c917-182">**\_идентификатор БУФФЕРИНГКАУНТ \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-182">**MFNETSOURCE\_BUFFERINGCOUNT\_ID**</span></span>        | <span data-ttu-id="1c917-183">Количество раз, которое клиент буферизован во время воспроизведения потока.</span><span class="sxs-lookup"><span data-stu-id="1c917-183">Number of times the client buffered while playing the stream.</span></span>                                                                                                                                                              |
| <span data-ttu-id="1c917-184">**\_идентификатор БИТЕСРЕЦЕИВЕД \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-184">**MFNETSOURCE\_BYTESRECEIVED\_ID**</span></span>         | <span data-ttu-id="1c917-185">Число байтов, полученных клиентом с сервера.</span><span class="sxs-lookup"><span data-stu-id="1c917-185">Number of bytes received by the client from the server.</span></span> <span data-ttu-id="1c917-186">Это значение не включает дополнительные издержки, добавленные сетевым стеком.</span><span class="sxs-lookup"><span data-stu-id="1c917-186">The value does not include any overhead that is added by the network stack.</span></span> <span data-ttu-id="1c917-187">То же содержимое, переданное с помощью разных протоколов, может привести к различным значениям.</span><span class="sxs-lookup"><span data-stu-id="1c917-187">The same content streamed by using different protocols can result in different values.</span></span> |
| <span data-ttu-id="1c917-188">**\_идентификатор ЛИНКБАНДВИДС \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-188">**MFNETSOURCE\_LINKBANDWIDTH\_ID**</span></span>         | <span data-ttu-id="1c917-189">Максимальная доступная пропускная способность клиента в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="1c917-189">Maximum available bandwidth of the client in bits per second.</span></span>                                                                                                                                                              |
| <span data-ttu-id="1c917-190">**\_идентификатор ЛОСТПАККЕТС \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-190">**MFNETSOURCE\_LOSTPACKETS\_ID**</span></span>           | <span data-ttu-id="1c917-191">Число пакетов, отправленных сервером, но потерянных при передаче, и никогда не воспроизводился клиентом.</span><span class="sxs-lookup"><span data-stu-id="1c917-191">Number of packets sent by the server but lost during transmission, and never played by the client.</span></span> <span data-ttu-id="1c917-192">Значение не включает пакеты TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="1c917-192">The value does not include TCP or UDP packets.</span></span>                                                                          |
| <span data-ttu-id="1c917-193">**\_идентификатор РЕКВПАККЕТС \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-193">**MFNETSOURCE\_RECVPACKETS\_ID**</span></span>           | <span data-ttu-id="1c917-194">Число пакетов, полученных с сервера. значение не включает пакеты TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="1c917-194">Number of packets received from the server The value does not include TCP or UDP packets.</span></span>                                                                                                                                  |
| <span data-ttu-id="1c917-195">**\_идентификатор РЕКОВЕРЕДБЕККПАККЕТС \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-195">**MFNETSOURCE\_RECOVEREDBYECCPACKETS\_ID**</span></span> | <span data-ttu-id="1c917-196">Потерянные в сети пакеты, которые были восстановлены и восстановлены на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="1c917-196">Packets lost in the network that were repaired and recovered at the client layer.</span></span> <span data-ttu-id="1c917-197">Это значение не включает пакеты TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="1c917-197">This value does not include TCP or UDP packets.</span></span>                                                                                          |
| <span data-ttu-id="1c917-198">**\_идентификатор РЕСЕНДСРЕКУЕСТЕД \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-198">**MFNETSOURCE\_RESENDSREQUESTED\_ID**</span></span>      | <span data-ttu-id="1c917-199">Число запросов, отправленных клиентом для получения новых пакетов.</span><span class="sxs-lookup"><span data-stu-id="1c917-199">The number of requests made by the client to receive new packets.</span></span> <span data-ttu-id="1c917-200">Это значение не включает пакеты TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="1c917-200">This value does not include TCP or UDP packets.</span></span>                                                                                                          |
| <span data-ttu-id="1c917-201">**\_идентификатор РЕКОВЕРЕДПАККЕТС \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-201">**MFNETSOURCE\_RECOVEREDPACKETS\_ID**</span></span>      | <span data-ttu-id="1c917-202">Число восстановленных пакетов, так как они были отправлены по протоколу UDP.</span><span class="sxs-lookup"><span data-stu-id="1c917-202">Number of packets recovered because they were resent through UDP.</span></span> <span data-ttu-id="1c917-203">Это значение не включает пакеты TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="1c917-203">This value does not include TCP or UDP packets.</span></span> <span data-ttu-id="1c917-204">Это поле содержит нуль, если клиент не использует повторную отправку UDP.</span><span class="sxs-lookup"><span data-stu-id="1c917-204">This field contains a zero unless the client is using UDP resend.</span></span>                                        |
| <span data-ttu-id="1c917-205">**\_идентификатор БУФФЕРПРОГРЕСС \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-205">**MFNETSOURCE\_BUFFERPROGRESS\_ID**</span></span>        | <span data-ttu-id="1c917-206">Процент буферов воспроизведения, заполненный во время буферизации.</span><span class="sxs-lookup"><span data-stu-id="1c917-206">The percentage of the playout buffer filled during buffering.</span></span>                                                                                                                                                              |
| <span data-ttu-id="1c917-207">**\_идентификатор протокола \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-207">**MFNETSOURCE\_PROTOCOL\_ID**</span></span>              | <span data-ttu-id="1c917-208">Протокол, используемый для доступа к потоку.</span><span class="sxs-lookup"><span data-stu-id="1c917-208">Protocol used to access the stream.</span></span> <span data-ttu-id="1c917-209">Это может отличаться от протокола, запрошенного клиентом.</span><span class="sxs-lookup"><span data-stu-id="1c917-209">This may differ from the protocol requested by the client.</span></span>                                                                                                                             |
| <span data-ttu-id="1c917-210">**\_идентификатор транспорта \_ мфнетсаурце**</span><span class="sxs-lookup"><span data-stu-id="1c917-210">**MFNETSOURCE\_TRANSPORT\_ID**</span></span>             | <span data-ttu-id="1c917-211">Транспортный протокол, используемый для доставки потока.</span><span class="sxs-lookup"><span data-stu-id="1c917-211">Transport protocol used to deliver the stream.</span></span> <span data-ttu-id="1c917-212">Это должен быть либо UDP, либо TCP.</span><span class="sxs-lookup"><span data-stu-id="1c917-212">This must be either UDP or TCP.</span></span>                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="1c917-213">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1c917-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c917-214">Компоненты сетевого источника</span><span class="sxs-lookup"><span data-stu-id="1c917-214">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="1c917-215">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c917-215">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

