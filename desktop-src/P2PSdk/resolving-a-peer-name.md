---
description: В этом разделе обсуждаются методы разрешения имени однорангового узла с помощью API-интерфейсов поставщика пространства имен PNRP.
ms.assetid: 7b21ec52-bc29-447e-9c46-34b9115574e0
title: Разрешение имени однорангового узла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7f3aa59d3dc3be89f35ce9d6eca58bed1ce137
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911623"
---
# <a name="resolving-a-peer-name"></a><span data-ttu-id="bb6e8-103">Разрешение имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="bb6e8-103">Resolving a Peer Name</span></span>

<span data-ttu-id="bb6e8-104">В этом разделе обсуждаются методы разрешения имени однорангового узла с помощью API-интерфейсов поставщика пространства имен PNRP.</span><span class="sxs-lookup"><span data-stu-id="bb6e8-104">This topic discusses methods for resolving a peer name using the PNRP Namespace Provider APIs.</span></span>

<span data-ttu-id="bb6e8-105">При разрешении имени однорангового узла необходимо указать следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="bb6e8-105">When you resolve a peer name, you must provide the following information:</span></span>

-   [<span data-ttu-id="bb6e8-106">Имя однорангового узла</span><span class="sxs-lookup"><span data-stu-id="bb6e8-106">Peer name</span></span>](peer-names.md)
-   [<span data-ttu-id="bb6e8-107">Разрешить критерии</span><span class="sxs-lookup"><span data-stu-id="bb6e8-107">Resolve criteria</span></span>](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)
-   <span data-ttu-id="bb6e8-108">Имя облака, в котором нужно разрешить имя однорангового узла</span><span class="sxs-lookup"><span data-stu-id="bb6e8-108">Cloud name in which to resolve the peer name</span></span>
-   <span data-ttu-id="bb6e8-109">IP-адрес, который является необязательным и используется как подсказка</span><span class="sxs-lookup"><span data-stu-id="bb6e8-109">IP address, which is optional and is used as a hint</span></span>

## <a name="resolving-a-peer-name"></a><span data-ttu-id="bb6e8-110">Разрешение имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="bb6e8-110">Resolving a Peer Name</span></span>

<span data-ttu-id="bb6e8-111">После указания имени однорангового узла, критериев разрешения, имени облака и дополнительного IP-адреса необходимо выполнить следующие действия, чтобы завершить разрешение имени однорангового узла:</span><span class="sxs-lookup"><span data-stu-id="bb6e8-111">After you provide a peer name, resolve criteria, cloud name, and the optional IP address, the following steps must be taken to complete the resolution of a peer name:</span></span>

-   <span data-ttu-id="bb6e8-112">Вызовите [**всалукупсервицебегин**](pnrp-and-wsalookupservicebegin.md) , чтобы начать процесс и вернуть маркер.</span><span class="sxs-lookup"><span data-stu-id="bb6e8-112">Call [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) to begin the process and return a handle.</span></span>
-   <span data-ttu-id="bb6e8-113">Вызовите [**всалукупсервиценекст**](pnrp-and-wsalookupservicenext.md) , чтобы разрешить имя однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="bb6e8-113">Call [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) to resolve the peer name.</span></span>
-   <span data-ttu-id="bb6e8-114">Вызовите [**всалукупсервицеенд**](pnrp-and-wsalookupserviceend.md) , чтобы завершить процесс.</span><span class="sxs-lookup"><span data-stu-id="bb6e8-114">Call [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) to complete the process.</span></span>

## <a name="an-example-of-resolving-a-peer-name"></a><span data-ttu-id="bb6e8-115">Пример разрешения имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="bb6e8-115">An Example of Resolving a Peer Name</span></span>

<span data-ttu-id="bb6e8-116">В следующем фрагменте кода показано, как разрешить имя однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="bb6e8-116">The following code snippet shows you how to resolve a peer name.</span></span> <span data-ttu-id="bb6e8-117">В примере предполагается, что будет возвращен адрес TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="bb6e8-117">There is an assumption in the sample that a TCP/IP address will be returned.</span></span>


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment( lib, "ws2_32.lib")

// Function: PnrpResolve
//
// Purpose:  Resolve the given name within a PNRP cloud
//
// Arguments:
//   pwzName  : name to resolve in PNRP, generally the graph id
//   pwzCloud : name of cloud to resolve in, NULL = global cloud
//   pAddr    : pointer to result buffer
//
// Returns:  HRESULT
//
HRESULT PnrpResolve(PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddr)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    WSAQUERYSET*    pResults = NULL;
    WSAQUERYSET     tempResultSet = {0};
    HANDLE          hLookup = NULL;
    BOOL            fFound = FALSE;
    DWORD           dwError;
    INT             iRet;
    ULONG           i;
    DWORD           dwSize = 0;

    //
    // fill in the WSAQUERYSET
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.nMaxResolve = 1;
    pnrpInfo.dwTimeout = 30;
    pnrpInfo.enResolveCriteria = PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;
    // start resolve
    iRet = WSALookupServiceBegin(
            &querySet,
            LUP_RETURN_NAME | LUP_RETURN_ADDR | LUP_RETURN_COMMENT,
            &hLookup);


    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    if (SUCCEEDED(hr))
    {
        dwSize = sizeof(tempResultSet);

        // retrieve the required size
        iRet = WSALookupServiceNext(hLookup, 0, &dwSize, &tempResultSet);
        dwError = WSAGetLastError();

        if (dwError == WSAEFAULT)
        {
            // allocate space for the results
            pResults = (WSAQUERYSET*)malloc(dwSize);
            if (pResults == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }
        else
        {
            hr = HRESULT_FROM_WIN32(dwError);
        }
    }

    if (SUCCEEDED(hr))
    {
        // retrieve the addresses
        iRet = WSALookupServiceNext(hLookup, 0, &dwSize, pResults);
        if (iRet != 0)
        {
            hr = HRESULT_FROM_WIN32(WSAGetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        // return the first IPv6 address found
        for (i = 0; i < pResults->dwNumberOfCsAddrs; i++)
        {
            if (pResults->lpcsaBuffer[i].iProtocol == IPPROTO_TCP &&
                pResults->lpcsaBuffer[i].RemoteAddr.iSockaddrLength == sizeof(SOCKADDR_IN6))
            {
                CopyMemory(pAddr, pResults->lpcsaBuffer[i].RemoteAddr.lpSockaddr, sizeof(SOCKADDR_IN6));
                fFound = TRUE;
                break;
            }
        }

        if (!fFound)
        {
            // unable to find an IPv6 address
            hr = HRESULT_FROM_WIN32(WSA_E_NO_MORE);
        }
    }

    if (hLookup != NULL)
    {
        WSALookupServiceEnd(hLookup);
    }

    if (pResults != NULL)
    {
        free(pResults);
    }

    return hr;
}
```



 

 



