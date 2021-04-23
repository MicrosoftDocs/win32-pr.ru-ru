---
description: Настройка выходных данных отладки с помощью ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Настройка выходных данных отладки с помощью ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ac7dd34b19cfe1fc7835a2026ae2dd28b9dcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072482"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a><span data-ttu-id="41b3f-103">Настройка выходных данных отладки с помощью ID3D10InfoQueue (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="41b3f-103">Customize Debug Output with ID3D10InfoQueue (Direct3D 10)</span></span>

<span data-ttu-id="41b3f-104">Информационная очередь управляется интерфейсом (см. [**интерфейс ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)), который хранит, извлекает и фильтрует сообщения отладки.</span><span class="sxs-lookup"><span data-stu-id="41b3f-104">The information queue is managed by an interface (see [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) that stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="41b3f-105">Очередь состоит из: очереди сообщений, дополнительного стека фильтра хранилища и дополнительного стека фильтров получения.</span><span class="sxs-lookup"><span data-stu-id="41b3f-105">The queue consists of: a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> <span data-ttu-id="41b3f-106">Стек фильтра хранения можно использовать для фильтрации сообщений, которые нужно сохранить. стек получения и фильтрации можно использовать для фильтрации сообщений, которые нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="41b3f-106">The storage-filter stack can be used to filter the messages you want stored; the retrieval-filter stack can be used to filter the messages you want stored.</span></span> <span data-ttu-id="41b3f-107">После фильтрации сообщения сообщение будет напечатано в окне отладки и сохранено в соответствующем стеке.</span><span class="sxs-lookup"><span data-stu-id="41b3f-107">Once you have filtered a message, the message will be printed out to the debug window and stored in the appropriate stack.</span></span>

<span data-ttu-id="41b3f-108">а именно:</span><span class="sxs-lookup"><span data-stu-id="41b3f-108">In general:</span></span>

-   <span data-ttu-id="41b3f-109">Вызов [**ID3D10InfoQueue:: аддаппликатионмессаже**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) для создания определяемых пользователем сообщений</span><span class="sxs-lookup"><span data-stu-id="41b3f-109">Call [**ID3D10InfoQueue::AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) to generate user-defined messages</span></span>
-   <span data-ttu-id="41b3f-110">Вызов [**ID3D10InfoQueue::**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) an используется для получения сообщений (которые передают необязательный фильтр извлечения).</span><span class="sxs-lookup"><span data-stu-id="41b3f-110">Call [**ID3D10InfoQueue::GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) is used to get messages (that pass an optional retrieval filter).</span></span>

## <a name="registry-controls"></a><span data-ttu-id="41b3f-111">Элементы управления реестра</span><span class="sxs-lookup"><span data-stu-id="41b3f-111">Registry Controls</span></span>

<span data-ttu-id="41b3f-112">Используйте разделы реестра для настройки параметров фильтра, настройки точек останова и отключения вывода отладочных данных.</span><span class="sxs-lookup"><span data-stu-id="41b3f-112">Use registry keys to adjust filter settings, adjust break points, and to mute the debug output.</span></span> <span data-ttu-id="41b3f-113">Отладочный слой проверит эти пути в разделах реестра. будет использован первый найденный путь.</span><span class="sxs-lookup"><span data-stu-id="41b3f-113">The debug layer will check these paths for registry keys; the first path found will be used.</span></span>

1.  <span data-ttu-id="41b3f-114">HKCU \\ Software \\ Microsoft \\ Direct3D \\<определяемый пользователем подраздел></span><span class="sxs-lookup"><span data-stu-id="41b3f-114">HKCU\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
2.  <span data-ttu-id="41b3f-115">HKLM \\ Software \\ Microsoft \\ Direct3D \\<определяемый пользователем подраздел></span><span class="sxs-lookup"><span data-stu-id="41b3f-115">HKLM\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
3.  <span data-ttu-id="41b3f-116">HKCU \\ Software \\ Microsoft \\ Direct3D</span><span class="sxs-lookup"><span data-stu-id="41b3f-116">HKCU\\Software\\Microsoft\\Direct3D</span></span>

<span data-ttu-id="41b3f-117">Где:</span><span class="sxs-lookup"><span data-stu-id="41b3f-117">Where:</span></span>

-   <span data-ttu-id="41b3f-118">Подставка HKCU для \_ текущего \_ пользователя hKey и раздел реестра HKLM для \_ локального \_ компьютера hKey.</span><span class="sxs-lookup"><span data-stu-id="41b3f-118">HKCU stand for HKEY\_CURRENT\_USER, and HKLM stand for HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="41b3f-119"><определяемого пользователем подраздела> является произвольным именем для хранения параметров отладки для приложения.</span><span class="sxs-lookup"><span data-stu-id="41b3f-119"><user-defined subkey> is an arbitrary name to store debug settings for an application</span></span>

### <a name="filtering-debug-messages-using-registry-keys"></a><span data-ttu-id="41b3f-120">Фильтрация отладочных сообщений с помощью разделов реестра</span><span class="sxs-lookup"><span data-stu-id="41b3f-120">Filtering Debug Messages using Registry Keys</span></span>

<span data-ttu-id="41b3f-121">Если реестр содержит ключ Инфокуеуесторажефилтероверриде (и не равен нулю), то сообщения (и выходные данные отладки) могут быть отфильтрованы путем добавления следующих элементов управления реестром.</span><span class="sxs-lookup"><span data-stu-id="41b3f-121">If the registry contains an InfoQueueStorageFilterOverride key (and is non-zero), then messages (and debug output) can be filtered by adding the following registry controls.</span></span>

-   <span data-ttu-id="41b3f-122">Параметр DWORD \_ выкл \_ \* ., если этот ключ не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="41b3f-122">DWORD Mute\_CATEGORY\_\* - Debug output if this key is non-zero.</span></span>
-   <span data-ttu-id="41b3f-123">Параметр DWORD \_ без звука \_ \* — отладочный вывод отключен, если этот ключ не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="41b3f-123">DWORD Mute\_SEVERITY\_\* - Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="41b3f-124">Параметр DWORD \_ \_ \* без звука — имя или номер сообщения можно использовать для \* (точно так же, как для \_ идентификатора бреакон \_ \* , описанного выше).</span><span class="sxs-lookup"><span data-stu-id="41b3f-124">DWORD Mute\_ID\_\* - Message name or number can be used for \* (just like for BreakOn\_ID\_\* described earlier).</span></span> <span data-ttu-id="41b3f-125">Если этот ключ не равен нулю, выходные данные отладки отключаются.</span><span class="sxs-lookup"><span data-stu-id="41b3f-125">Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="41b3f-126">DWORD без звука \_ \_ сведения об уровне серьезности — выходные данные отладки включаются, если этот ключ не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="41b3f-126">DWORD Unmute\_SEVERITY\_INFO - Debug output is ENABLED if this key is non-zero.</span></span> <span data-ttu-id="41b3f-127">По умолчанию при включении Инфокуеуесторажефилтероверриде сообщения отладки со сведениями о серьезности отключаются, поэтому для этого параметра можно снова включить данные.</span><span class="sxs-lookup"><span data-stu-id="41b3f-127">By default when InfoQueueStorageFilterOverride is enabled, debug messages with severity INFO are muted - therefore for this key allows INFO to be turned back on.</span></span>

<span data-ttu-id="41b3f-128">Эти элементы управления изменяют, будет ли сообщение записано или отображено. они не влияют на то, проходит ли API успешно или нет.</span><span class="sxs-lookup"><span data-stu-id="41b3f-128">These controls change whether a message is recorded or displayed; they do not affect whether an API passes or fails.</span></span>

### <a name="setting-break-conditions-using-registry-keys"></a><span data-ttu-id="41b3f-129">Настройка условий останова с помощью разделов реестра</span><span class="sxs-lookup"><span data-stu-id="41b3f-129">Setting Break Conditions using Registry Keys</span></span>

<span data-ttu-id="41b3f-130">Приложения могут принудительно прерывать работу на сообщении, используя следующие разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="41b3f-130">Applications can be forced to break on a message using the following registry keys.</span></span>

<span data-ttu-id="41b3f-131">**Енаблебреаконмессаже** — этот ключ позволяет прерывать работу на сообщениях (и вызывает игнорирование параметров сетбреаконкатегори ()/сетбреаконсеверити ()/сетбреаконид ().</span><span class="sxs-lookup"><span data-stu-id="41b3f-131">**EnableBreakOnMessage** - This key enables breaking on messages (and causes i's SetBreakOnCategory()/SetBreakOnSeverity()/SetBreakOnID() settings to be ignored).</span></span> <span data-ttu-id="41b3f-132">Фактические сообщения, подходящие для прерывания, определяются с помощью одного или нескольких значений Бреакон, \_ \* определенных ниже.</span><span class="sxs-lookup"><span data-stu-id="41b3f-132">The actual messages to break on are defined using one or more BreakOn\_\* values defined below.</span></span>

-   <span data-ttu-id="41b3f-133">\**Бреакон \_ \_Категория \** _ — прервать на любом сообщении, проходящем через фильтры хранилища.</span><span class="sxs-lookup"><span data-stu-id="41b3f-133">\**BreakOn\_CATEGORY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="41b3f-134">\_ одно из \_ сообщений категории сообщений D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="41b3f-134">\_ is one of the D3D10\_MESSAGE\_CATEGORY messages.</span></span>
-   <span data-ttu-id="41b3f-135">\**Бреакон \_ \_ \* Серьезность* _ — прерывание любого сообщения, переданного через фильтры хранилища.</span><span class="sxs-lookup"><span data-stu-id="41b3f-135">\**BreakOn\_SEVERITY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="41b3f-136">\_ одно из \_ \_ сообщений серьезности сообщения D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="41b3f-136">\_ is one of the D3D10\_MESSAGE\_SEVERITY\_ messages.</span></span>
-   <span data-ttu-id="41b3f-137">\**Бреакон \_ \_Идентификатор \** _ — прервать на любом сообщении, проходящем через фильтры хранилища.</span><span class="sxs-lookup"><span data-stu-id="41b3f-137">\**BreakOn\_ID\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="41b3f-138">\_ одно из \_ \_ сообщений с идентификатором сообщения D3D10 \_ или может быть числовым значением перечисления ошибок.</span><span class="sxs-lookup"><span data-stu-id="41b3f-138">\_ is one of the D3D10\_MESSAGE\_ID\_ messages or can be the numerical value of the error enumeration.</span></span> <span data-ttu-id="41b3f-139">Например, предположим, что сообщение с ИДЕНТИФИКАТОРом "D3D10 сообщения с идентификатором \_ \_ \_ гипотетически" имеет значение 123 в \_ \_ перечислении идентификаторов сообщений D3D10.</span><span class="sxs-lookup"><span data-stu-id="41b3f-139">For example, Suppose the message with ID "D3D10\_MESSAGE\_ID\_HYPOTHETICAL" had the value 123 in the D3D10\_MESSAGE\_ID enumeration.</span></span> <span data-ttu-id="41b3f-140">В этом случае создание значения Бреакон с \_ идентификатором \_ гипотетические = 1 или \_ бреакон \_ с идентификатором 123 = 1 приведет к тому же прерыванию, когда \_ будет обнаружено сообщение с идентификатором D3D10 с идентификатором " \_ \_ гипотетический".</span><span class="sxs-lookup"><span data-stu-id="41b3f-140">In this case, creating the value BreakOn\_ID\_HYPOTHETICAL=1 or BreakOn\_ID\_123=1 would both accomplish the same thing - break when a message having ID D3D10\_MESSAGE\_ID\_HYPOTHETICAL is encountered.</span></span>

### <a name="muting-debug-output-using-registry-keys"></a><span data-ttu-id="41b3f-141">Вывод отладки с отключением звука с помощью разделов реестра</span><span class="sxs-lookup"><span data-stu-id="41b3f-141">Muting Debug Output using Registry Keys</span></span>

<span data-ttu-id="41b3f-142">Выходные данные отладки можно отключить с помощью ключа Мутедебугаутпут.</span><span class="sxs-lookup"><span data-stu-id="41b3f-142">Debug output can be muted using a MuteDebugOutput key.</span></span> <span data-ttu-id="41b3f-143">Наличие этого значения в реестре приводит к переопределению метода [**ID3D10InfoQueue:: Сетмутедебугаутпут**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) инфокуеуе.</span><span class="sxs-lookup"><span data-stu-id="41b3f-143">The presence of this value in the registry forces override of the InfoQueue's [**ID3D10InfoQueue::SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) method.</span></span> <span data-ttu-id="41b3f-144">Мутедебугаутпут останавливает передачу сообщений, передаваемых фильтру хранилища, в выходные данные отладки.</span><span class="sxs-lookup"><span data-stu-id="41b3f-144">MuteDebugOutput stops messages that pass the storage filter from being sent to debug output.</span></span>

## <a name="disabling-debug-layer-messages"></a><span data-ttu-id="41b3f-145">Отключение сообщений уровня отладки</span><span class="sxs-lookup"><span data-stu-id="41b3f-145">Disabling Debug Layer Messages</span></span>

<span data-ttu-id="41b3f-146">Сообщения уровня отладки можно отключить отдельно или как группу во время выполнения, указав фильтры с помощью [**ID3D10InfoQueue:: аддсторажефилтерентриес**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span><span class="sxs-lookup"><span data-stu-id="41b3f-146">Debug layer messages can be disabled individualy or as a group at runtime by specifying filters using [**ID3D10InfoQueue::AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span></span> <span data-ttu-id="41b3f-147">Аргумент *пфилтер* для **ID3D10InfoQueue:: аддсторажефилтерентриес** принимает структуру [**\_ \_ \_ фильтра очереди D3D10 info**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) , содержащую список разрешений и список запретов.</span><span class="sxs-lookup"><span data-stu-id="41b3f-147">The *pFilter* argument to **ID3D10InfoQueue::AddStorageFilterEntries** takes a [**D3D10\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) structure that contains an allow list and a deny list.</span></span> <span data-ttu-id="41b3f-148">Списки разрешений и запретов описываются структурами [**D3D10 \_ info \_ \_ \_**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) , которые позволяют задавать фильтрацию с помощью категории, серьезности и идентификатора отдельного сообщения.</span><span class="sxs-lookup"><span data-stu-id="41b3f-148">The allow and deny lists are described by [**D3D10\_INFO\_QUEUE\_FILTER\_DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) structures that allow filtering to be specified by catergory, severity and individual message ID.</span></span>

<span data-ttu-id="41b3f-149">В следующем коде приведен пример настройки [**интерфейса ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) для запрета сообщения D3D10 с \_ \_ идентификатором устройства, \_ что \_ \_ \_ буфер \_ слишком \_ мал.</span><span class="sxs-lookup"><span data-stu-id="41b3f-149">The following code is an example of setting up the [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) to deny the D3D10\_MESSAGE\_ID\_DEVICE\_DRAW\_INDEX\_BUFFER\_TOO\_SMALL message.</span></span>


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a><span data-ttu-id="41b3f-150">См. также</span><span class="sxs-lookup"><span data-stu-id="41b3f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41b3f-151">Уровни API</span><span class="sxs-lookup"><span data-stu-id="41b3f-151">API Layers</span></span>](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[<span data-ttu-id="41b3f-152">Функции API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="41b3f-152">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



