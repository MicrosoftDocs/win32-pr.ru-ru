---
description: Работа с видеоустройствами USB DV
ms.assetid: 6244f006-db9f-42b2-81cd-26eba583613e
title: Работа с видеоустройствами USB DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75647aa7b53bac45c155b4e0a9283418c9af58b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263478"
---
# <a name="working-with-usb-dv-video-devices"></a><span data-ttu-id="ade56-103">Работа с видеоустройствами USB DV</span><span class="sxs-lookup"><span data-stu-id="ade56-103">Working with USB DV Video Devices</span></span>

<span data-ttu-id="ade56-104">В этом разделе описывается написание приложений для видеоустройств с универсальной последовательной шиной (USB), записывающих видео в формате DV.</span><span class="sxs-lookup"><span data-stu-id="ade56-104">This topic describes how to write applications for Universal Serial Bus (USB) video devices that capture DV video.</span></span>

<span data-ttu-id="ade56-105">Скорость передачи данных в стандартном DV-формате составляет около 25 мегабит в секунду (Мбит/с).</span><span class="sxs-lookup"><span data-stu-id="ade56-105">Standard DV format has a data rate of about 25 megabits per second (Mbps).</span></span> <span data-ttu-id="ade56-106">Когда USB впервые появился, у него недостаточно пропускной способности для поддержки видео в DV.</span><span class="sxs-lookup"><span data-stu-id="ade56-106">When USB was first introduced, it did not have enough bandwidth to support DV video.</span></span> <span data-ttu-id="ade56-107">Однако USB 2,0 может поддерживать до 480 Мбит/с, что больше, чем достаточно для видео в DV.</span><span class="sxs-lookup"><span data-stu-id="ade56-107">However, USB 2.0 can support up to 480 Mbps, which is more than sufficient for DV video.</span></span> <span data-ttu-id="ade56-108">Спецификация класса USB Video Device (УВК), выпущенная в 2003, определяет формат полезных данных для видеоадаптеров USB DV.</span><span class="sxs-lookup"><span data-stu-id="ade56-108">The USB Video Device Class (UVC) specification, released in 2003, defines the payload format for USB DV video devices.</span></span> <span data-ttu-id="ade56-109">Драйвер класса WDM (WDM) для устройств УВК был представлен в пакете обновления 2 (SP2) для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ade56-109">A Windows Driver Model (WDM) class driver for UVC devices was introduced in Windows XP Service Pack 2.</span></span>

<span data-ttu-id="ade56-110">В большинстве случаев драйвер УВК поддерживает ту же модель программирования, что и драйвер МСДВ для устройств IEEE 1394.</span><span class="sxs-lookup"><span data-stu-id="ade56-110">In most respects, the UVC driver supports the same programming model as the MSDV driver for IEEE 1394 devices.</span></span> <span data-ttu-id="ade56-111">Приложения, написанные для МСДВ, должны иметь только небольшие изменения для поддержки устройств УВК.</span><span class="sxs-lookup"><span data-stu-id="ade56-111">Applications written for MSDV should require only minor modifications to support UVC devices.</span></span>

<span data-ttu-id="ade56-112">Драйвер УВК ведет себя иначе, чем драйвер МСДВ в следующих областях:</span><span class="sxs-lookup"><span data-stu-id="ade56-112">The UVC driver behaves differently from the MSDV driver in the following areas:</span></span>

-   [<span data-ttu-id="ade56-113">Режим устройства</span><span class="sxs-lookup"><span data-stu-id="ade56-113">Device Mode</span></span>](device-mode.md)
-   [<span data-ttu-id="ade56-114">Формат потока</span><span class="sxs-lookup"><span data-stu-id="ade56-114">Stream Format</span></span>](stream-format.md)
-   [<span data-ttu-id="ade56-115">Формат сигнала</span><span class="sxs-lookup"><span data-stu-id="ade56-115">Signal Format</span></span>](signal-format.md)
-   [<span data-ttu-id="ade56-116">Поиск расположения на ленте</span><span class="sxs-lookup"><span data-stu-id="ade56-116">Tape Location Search</span></span>](tape-location-search.md)
-   <span data-ttu-id="ade56-117">[Передача DV из файла на ленту](transmit-dv-from-file-to-tape.md).</span><span class="sxs-lookup"><span data-stu-id="ade56-117">[Transmit DV from File to Tape](transmit-dv-from-file-to-tape.md).</span></span>

<span data-ttu-id="ade56-118">Чтобы определить, какой драйвер используется, вызовите [**иамекстдевице:: Get \_ девицепорт**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport).</span><span class="sxs-lookup"><span data-stu-id="ade56-118">To determine which driver is being used, call [**IAMExtDevice::get\_DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport).</span></span> <span data-ttu-id="ade56-119">Драйвер МСДВ возвращает \_ флаг порта dev \_ 1394, а драйвер УВК возвращает \_ \_ флаг USB-порта dev.</span><span class="sxs-lookup"><span data-stu-id="ade56-119">The MSDV driver returns the DEV\_PORT\_1394 flag, and the UVC driver returns the DEV\_PORT\_USB flag.</span></span>

<span data-ttu-id="ade56-120">**Узлы устройств**</span><span class="sxs-lookup"><span data-stu-id="ade56-120">**Device Nodes**</span></span>

<span data-ttu-id="ade56-121">В терминологии USB конечные точки — это точки, в которых данные перемещаются или остаются на устройстве.</span><span class="sxs-lookup"><span data-stu-id="ade56-121">In USB terminology, endpoints are the points where data enters or leaves the device.</span></span> <span data-ttu-id="ade56-122">Конечная точка имеет направление потока данных: вход (с устройства на узел) или выход (от узла к устройству).</span><span class="sxs-lookup"><span data-stu-id="ade56-122">An endpoint has a direction of data flow, either input (from device to host) or output (from host to device).</span></span> <span data-ttu-id="ade56-123">Это может помочь понять эти направления относительно узла.</span><span class="sxs-lookup"><span data-stu-id="ade56-123">It may help to think of these directions as being relative to the host.</span></span> <span data-ttu-id="ade56-124">Вход переходит на узел; выходные данные поступают от узла.</span><span class="sxs-lookup"><span data-stu-id="ade56-124">Input goes to the host; output comes from the host.</span></span> <span data-ttu-id="ade56-125">На следующей схеме показаны две конечные точки.</span><span class="sxs-lookup"><span data-stu-id="ade56-125">The following diagram illustrates the two endpoints.</span></span>

![конечные точки USB](images/ksnodes01.png)

<span data-ttu-id="ade56-127">На устройстве УВК функции устройства логически делятся на компоненты, называемые единицами и терминалами.</span><span class="sxs-lookup"><span data-stu-id="ade56-127">In a UVC device, the functions of the device are logically divided into components called units and terminals.</span></span> <span data-ttu-id="ade56-128">Единица получает один или несколько потоков данных как входные и предоставляет в качестве выходных данных ровно один поток.</span><span class="sxs-lookup"><span data-stu-id="ade56-128">A unit receives one or more data streams as input and delivers exactly one stream as output.</span></span> <span data-ttu-id="ade56-129">Терминал — это начальная точка или конечная точка потока данных.</span><span class="sxs-lookup"><span data-stu-id="ade56-129">A terminal is the starting point or ending point for a data stream.</span></span> <span data-ttu-id="ade56-130">Конечные точки USB соответствуют терминалам, но направления обращены к ним: входная конечная точка представлена выходным терминалом и наоборот.</span><span class="sxs-lookup"><span data-stu-id="ade56-130">USB endpoints correspond to terminals, but the directions are reversed: an input endpoint is represented by an output terminal, and vice versa.</span></span> <span data-ttu-id="ade56-131">На следующей схеме показана связь между терминалами и конечными точками.</span><span class="sxs-lookup"><span data-stu-id="ade56-131">The following diagram shows the relation between terminals and endpoints.</span></span>

![единицы и терминалы УВК](images/ksnodes02.png)

<span data-ttu-id="ade56-133">Кроме того, не каждый терминал соответствует конечной точке USB.</span><span class="sxs-lookup"><span data-stu-id="ade56-133">Also, not every terminal corresponds to a USB endpoint.</span></span> <span data-ttu-id="ade56-134">Термин конечная точка относится только к USB-подключениям, а устройство может отправлять или получать данные через подключения, не связанные с USB.</span><span class="sxs-lookup"><span data-stu-id="ade56-134">The term endpoint refers specifically to USB connections, and a device may send or receive data through non-USB connections.</span></span> <span data-ttu-id="ade56-135">Например, видеокамера — это входной терминал, а ЖК-экран — выходной терминал.</span><span class="sxs-lookup"><span data-stu-id="ade56-135">For example, a video camera is an input terminal and an LCD screen is an output terminal.</span></span>

<span data-ttu-id="ade56-136">В фильтре прокси-сервера KS единицы и терминалы представлены как узлы внутри фильтра.</span><span class="sxs-lookup"><span data-stu-id="ade56-136">In the KS Proxy filter, units and terminals are represented as nodes inside the filter.</span></span> <span data-ttu-id="ade56-137">Термин «узел» является более общим, чем термины «единица» и «терминал», так как устройства, отличные от USB, также могут иметь узлы.</span><span class="sxs-lookup"><span data-stu-id="ade56-137">The term node is more general than the terms unit and terminal because non-USB devices can also have nodes.</span></span> <span data-ttu-id="ade56-138">Чтобы получить сведения об узлах в фильтре, запросите фильтр для интерфейса [**икстопологинфо**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) .</span><span class="sxs-lookup"><span data-stu-id="ade56-138">To get information about the nodes in a filter, query the filter for the [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) interface.</span></span> <span data-ttu-id="ade56-139">Типы узлов идентифицируются по идентификаторам GUID.</span><span class="sxs-lookup"><span data-stu-id="ade56-139">Node types are identified by GUIDs.</span></span> <span data-ttu-id="ade56-140">Узлы Selector — это узлы, которые могут переключаться между двумя или более входными данными.</span><span class="sxs-lookup"><span data-stu-id="ade56-140">Selector nodes are nodes that can switch between two or more inputs.</span></span> <span data-ttu-id="ade56-141">Узлы Selector [**предоставляют интерфейс для**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) выбора.</span><span class="sxs-lookup"><span data-stu-id="ade56-141">Selector nodes expose the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface.</span></span>

<span data-ttu-id="ade56-142">Следующий код проверяет, получает ли выходной ПИН-код на фильтре входные данные с узла заданного типа.</span><span class="sxs-lookup"><span data-stu-id="ade56-142">The following code tests whether an output pin on a filter receives input from a node of a given type.</span></span>


```C++
// Structure to hold topology information.
struct TopologyConnections
{
    KSTOPOLOGY_CONNECTION *connections; // Array of connections
    DWORD count;  // Number of elements in the array
};

/////////////////////////////////////////////////////////////////////
// Name: GetTopologyConnections
// Desc: Gets the topology information from a filter.
//
// pTopo:       Pointer to the filter's IKsTopologyInfo interface.
// connectInfo: Pointer to a TopologyConnections structure. The 
//              function fills in this structure.
//
// Note: If the function succeeds, call CoTaskMemFree to free the
//       pConnectInfo->connections array.
/////////////////////////////////////////////////////////////////////

HRESULT GetTopologyConnections(
    IKsTopologyInfo *pTopo, 
    TopologyConnections *pConnectInfo
    )
{
    DWORD count;
    HRESULT hr = pTopo->get_NumConnections(&count);
    if (FAILED(hr))
    {
        return hr;
    }

    pConnectInfo->count = count;
    pConnectInfo->connections = NULL;
    if (count > 0)
    {
        // Allocate an array for the connection information.
        SIZE_T cb = sizeof(KSTOPOLOGY_CONNECTION) * count;
        KSTOPOLOGY_CONNECTION *pConnections = 
            (KSTOPOLOGY_CONNECTION*) CoTaskMemAlloc(cb);
        if (pConnections == NULL)
        {
            return E_OUTOFMEMORY;
        }
        // Fill the array.
        for (DWORD ix = 0; ix < count; ix++)
        {
            hr = pTopo->get_ConnectionInfo(ix, &pConnections[ix]);
            if (FAILED(hr))
            {
                break;
            }
        }
        if (SUCCEEDED(hr))
        {
            pConnectInfo->connections = pConnections;
        }
        else
        {
           CoTaskMemFree(pConnections);
        }
    }
    return hr;
}

/////////////////////////////////////////////////////////////////////
// Name: IsNodeDownstreamFromNode
// Desc: Searches upstream from a node for a specified node type.
//
// pTopo:        Pointer to the filter's IKsTopologyInfo interface.
// connectInfo:  Contains toplogy information. To fill in this
//               structure, call GetTopologyConnections.
// nodeID:       ID of the starting node in the search.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected, or false otherwise.
//
// Note: If the source node matches the type, this function returns 
//       true without searching upstream.
/////////////////////////////////////////////////////////////////////

HRESULT IsNodeDownstreamFromNode(
    IKsTopologyInfo *pTopo,
    const TopologyConnections& connectInfo, 
    DWORD nodeID,
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    *pIsConnected = false;
    // Base case for recursion: check the source node.
    GUID type;
    HRESULT hr = pTopo->get_NodeType(nodeID, &type);
    if (FAILED(hr))
    {
        return hr;
    }
    if (type == nodeType)
    {
        *pIsConnected = true;
        return S_OK;
    }

    // If the source node is a selector, get the input node.
    CComPtr<ISelector> pSelector;
    hr = pTopo->CreateNodeInstance(nodeID, __uuidof(ISelector), 
        (void**)&pSelector);
    if (SUCCEEDED(hr))
    {
        DWORD sourceNodeID;
        hr = pSelector->get_SourceNodeId(&sourceNodeID);
        if (SUCCEEDED(hr))
        {
            // Recursive call with the selector's input node.
            return IsNodeDownstreamFromNode(pTopo, connectInfo, 
                       sourceNodeID, nodeType, pIsConnected);
        }
    }
    else if (hr == E_NOINTERFACE)
    {
        hr = S_OK;  // This node is not a selector. Not a failure.
    }
    else
    {
        return hr;
    }

    // Test all of the upstream connections on this pin. 
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == nodeID) &&
            (connectInfo.connections[ix].FromNode != KSFILTER_NODE))
        {
            // FromNode is connected to the source node.
            DWORD fromNode = connectInfo.connections[ix].FromNode;

            // Recursive call with the upstream node.
            bool bIsConnected;
            hr = IsNodeDownstreamFromNode(pTopo, connectInfo, 
                fromNode, nodeType, &bIsConnected);
            if (FAILED(hr))
            {
                break;
            }
            if (bIsConnected)
            {
                *pIsConnected = true;
                break;
            }
        }
    }
    return hr;
}


/////////////////////////////////////////////////////////////////////
// Name: GetNodeUpstreamFromPin
// Desc: Finds the node connected to an output pin.
//
// connectInfo: Contains toplogy information. To fill in this
//              structure, call GetTopologyConnections.
// nPinIndex:   Index of the output pin.
// pNodeID:     Receives the ID of the connected node.
/////////////////////////////////////////////////////////////////////

HRESULT GetNodeUpstreamFromPin(
    const TopologyConnections& connectInfo, 
    UINT nPinIndex, 
    DWORD *pNodeID
    )
{
    bool bFound = false;
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == KSFILTER_NODE) &&
            (connectInfo.connections[ix].ToNodePin == nPinIndex))
        {
            *pNodeID = connectInfo.connections[ix].FromNode;
            bFound = true;
            break;
        }
    }
    if (bFound)
    {
        return S_OK;
    }
    else
    {
        return E_FAIL;
    }
}


/////////////////////////////////////////////////////////////////////
// Name: IsPinDownstreamFromNode
// Desc: Tests whether an output pin gets data from a node of
//       a specified type.
// 
// pFilter:      Pointer to the filter's IBaseFilter interface.
// UINT:         Index of the output pin to test.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected; false otherwise.
/////////////////////////////////////////////////////////////////////

HRESULT IsPinDownstreamFromNode(
    IBaseFilter *pFilter, 
    UINT nPinIndex, 
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    CComQIPtr<IKsTopologyInfo> pTopo(pFilter);
    if (pTopo == NULL)
    {
        return E_NOINTERFACE;
    }

    // Get the topology connection information.
    TopologyConnections connectionInfo;
    HRESULT hr = GetTopologyConnections(pTopo, &connectionInfo);
    if (FAILED(hr))
    {
        return hr;
    }

    // Find the node upstream from this pin.
    DWORD nodeID;
    hr = GetNodeUpstreamFromPin(connectionInfo, nPinIndex, &nodeID);
    if (SUCCEEDED(hr))
    {
        bool isConnected;
        hr = IsNodeDownstreamFromNode(pTopo, connectionInfo, 
            nodeID, nodeType, &isConnected);
        if (SUCCEEDED(hr))
        {
            *pIsConnected = isConnected;
        }
    }
    CoTaskMemFree(connectionInfo.connections);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ade56-143">См. также</span><span class="sxs-lookup"><span data-stu-id="ade56-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ade56-144">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="ade56-144">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



