---
description: Работа с видеоустройствами USB DV
ms.assetid: 6244f006-db9f-42b2-81cd-26eba583613e
title: Работа с видеоустройствами USB DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1f83fb490f4bd1e71714dcb0658d01a41d6e45af6f3e89436f6e32c1cdc985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071754"
---
# <a name="working-with-usb-dv-video-devices"></a>Работа с видеоустройствами USB DV

В этом разделе описывается написание приложений для видеоустройств с универсальной последовательной шиной (USB), записывающих видео в формате DV.

Скорость передачи данных в стандартном DV-формате составляет около 25 мегабит в секунду (Мбит/с). Когда USB впервые появился, у него недостаточно пропускной способности для поддержки видео в DV. Однако USB 2,0 может поддерживать до 480 Мбит/с, что больше, чем достаточно для видео в DV. Спецификация класса USB Video Device (УВК), выпущенная в 2003, определяет формат полезных данных для видеоадаптеров USB DV. драйвер класса WDM (WDM) для устройств увк был введен в Windows XP с пакетом обновления 2 (sp2).

В большинстве случаев драйвер УВК поддерживает ту же модель программирования, что и драйвер МСДВ для устройств IEEE 1394. Приложения, написанные для МСДВ, должны иметь только небольшие изменения для поддержки устройств УВК.

Драйвер УВК ведет себя иначе, чем драйвер МСДВ в следующих областях:

-   [Режим устройства](device-mode.md)
-   [Формат потока](stream-format.md)
-   [Формат сигнала](signal-format.md)
-   [Поиск расположения на ленте](tape-location-search.md)
-   [Передача DV из файла на ленту](transmit-dv-from-file-to-tape.md).

Чтобы определить, какой драйвер используется, вызовите [**иамекстдевице:: Get \_ девицепорт**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport). Драйвер МСДВ возвращает \_ флаг порта dev \_ 1394, а драйвер УВК возвращает \_ \_ флаг USB-порта dev.

**Узлы устройств**

В терминологии USB конечные точки — это точки, в которых данные перемещаются или остаются на устройстве. Конечная точка имеет направление потока данных: вход (с устройства на узел) или выход (от узла к устройству). Это может помочь понять эти направления относительно узла. Вход переходит на узел; выходные данные поступают от узла. На следующей схеме показаны две конечные точки.

![конечные точки USB](images/ksnodes01.png)

На устройстве УВК функции устройства логически делятся на компоненты, называемые единицами и терминалами. Единица получает один или несколько потоков данных как входные и предоставляет в качестве выходных данных ровно один поток. Терминал — это начальная точка или конечная точка потока данных. Конечные точки USB соответствуют терминалам, но направления обращены к ним: входная конечная точка представлена выходным терминалом и наоборот. На следующей схеме показана связь между терминалами и конечными точками.

![единицы и терминалы УВК](images/ksnodes02.png)

Кроме того, не каждый терминал соответствует конечной точке USB. Термин конечная точка относится только к USB-подключениям, а устройство может отправлять или получать данные через подключения, не связанные с USB. Например, видеокамера — это входной терминал, а ЖК-экран — выходной терминал.

В фильтре прокси-сервера KS единицы и терминалы представлены как узлы внутри фильтра. Термин «узел» является более общим, чем термины «единица» и «терминал», так как устройства, отличные от USB, также могут иметь узлы. Чтобы получить сведения об узлах в фильтре, запросите фильтр для интерфейса [**икстопологинфо**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) . Типы узлов идентифицируются по идентификаторам GUID. Узлы Selector — это узлы, которые могут переключаться между двумя или более входными данными. Узлы Selector [**предоставляют интерфейс для**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) выбора.

Следующий код проверяет, получает ли выходной ПИН-код на фильтре входные данные с узла заданного типа.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Цифровое видео в DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



