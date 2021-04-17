---
description: 'Чтобы зарегистрировать одноранговое имя, приложение должно предоставить следующие сведения: IP-адрес Листпир Идентитипир Намеиф. имя однорангового узла не защищено. удостоверение является необязательным.'
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: Регистрация имени однорангового узла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0944c4a41c02ff221aa1cc6a0b84ed881a9453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663967"
---
# <a name="registering-a-peer-name"></a><span data-ttu-id="c705b-103">Регистрация имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="c705b-103">Registering a Peer Name</span></span>

<span data-ttu-id="c705b-104">Чтобы зарегистрировать одноранговое имя, приложение должно предоставить следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="c705b-104">To register a peer name, an application must provide the following information:</span></span>

-   <span data-ttu-id="c705b-105">Список IP-адресов</span><span class="sxs-lookup"><span data-stu-id="c705b-105">IP address list</span></span>
-   [<span data-ttu-id="c705b-106">Одноранговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="c705b-106">Peer identity</span></span>](creating-a-peer-identity.md)
-   [<span data-ttu-id="c705b-107">Имя однорангового узла</span><span class="sxs-lookup"><span data-stu-id="c705b-107">Peer name</span></span>](peer-names.md)

<span data-ttu-id="c705b-108">Если имя однорангового узла не защищено, то удостоверение является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c705b-108">If a peer name is unsecured, an identity is optional.</span></span> <span data-ttu-id="c705b-109">Если для однорангового узла задано **значение NULL**, протокол PNRP использует внутреннее удостоверение однорангового узла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c705b-109">If a peer identity is specified as **NULL**, the Peer Name Resolution Protocol (PNRP) uses an internal, default peer identity.</span></span>

## <a name="registering-a-peer-name"></a><span data-ttu-id="c705b-110">Регистрация имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="c705b-110">Registering a Peer Name</span></span>

<span data-ttu-id="c705b-111">После определения списка IP-адресов, однорангового узла и имени однорангового узла приложение может зарегистрировать имя однорангового узла, вызвав [**всасетсервице**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="c705b-111">After the IP address list, peer identity, and peer name are identified, the application can register a peer name by calling [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="c705b-112">Используйте рекомендации в следующих разделах этого раздела, чтобы внести необходимые настройки в параметры **всасетсервице** и структуру [**всакуерисет**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="c705b-112">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

### <a name="configuring-wsasetservice"></a><span data-ttu-id="c705b-113">Настройка Всасетсервице</span><span class="sxs-lookup"><span data-stu-id="c705b-113">Configuring WSASetService</span></span>

<span data-ttu-id="c705b-114">Когда приложение вызывает [**всасетсервице**](pnrp-and-wsasetservice.md), параметры должны быть настроены в соответствии со следующими спецификациями:</span><span class="sxs-lookup"><span data-stu-id="c705b-114">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="c705b-115">*ессоператион* должно иметь значение **рнрсервице \_ Register**.</span><span class="sxs-lookup"><span data-stu-id="c705b-115">*essOperation* must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="c705b-116">*dwFlags* должен быть равен нулю (0).</span><span class="sxs-lookup"><span data-stu-id="c705b-116">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="c705b-117">*лпксрегинфо* должен указывать на структуру [**всакуерисет**](pnrp-and-wsaqueryset.md) , которая должна быть настроена с помощью правил, описанных в разделе **Настройка всакуерисет** этой статьи.</span><span class="sxs-lookup"><span data-stu-id="c705b-117">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following **Configuring WSAQUERYSET** section of this topic.</span></span>

### <a name="configuring-wsaqueryset"></a><span data-ttu-id="c705b-118">Настройка ВСАКУЕРИСЕТ</span><span class="sxs-lookup"><span data-stu-id="c705b-118">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="c705b-119">Структура [**всакуерисет**](pnrp-and-wsaqueryset.md) должна быть настроена в соответствии со следующими спецификациями:</span><span class="sxs-lookup"><span data-stu-id="c705b-119">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="c705b-120">**двсизе** должен указывать размер структуры [**всакуерисет**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="c705b-120">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="c705b-121">**лпсзсервицеинстанценаме** должен указывать на Регистрируемое имя однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="c705b-121">**lpszServiceInstanceName** must point to the peer name that is being registered.</span></span>
-   <span data-ttu-id="c705b-122">**лпблоб** должен указывать на структуру [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="c705b-122">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="c705b-123">**лпксабуффер** должен указывать на список адресов.</span><span class="sxs-lookup"><span data-stu-id="c705b-123">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="c705b-124">Остальные члены описаны в разделе [**PNRP и всасетсервице**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="c705b-124">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

<span data-ttu-id="c705b-125">После регистрации имени однорангового узла сведения доступны для одноранговой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="c705b-125">After a peer name is registered, the information is available to the Peer Infrastructure.</span></span> <span data-ttu-id="c705b-126">Однако между временем регистрации и распространением сведений о регистрации на другие узлы существует задержка.</span><span class="sxs-lookup"><span data-stu-id="c705b-126">However, there is a delay between the registration time and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="c705b-127">В течение этого времени другие узлы, возможно, не смогут разрешить только что зарегистрированный одноранговый узел.</span><span class="sxs-lookup"><span data-stu-id="c705b-127">During that time, other nodes may not be able to resolve the newly registered peer.</span></span>

## <a name="example-of-registering-a-peer-name"></a><span data-ttu-id="c705b-128">Пример регистрации имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="c705b-128">Example of Registering a Peer Name</span></span>

<span data-ttu-id="c705b-129">В следующем фрагменте кода показано, как зарегистрировать имя однорангового узла, предоставив правильные сведения при вызове [**всасетсервице**](pnrp-and-wsasetservice.md) с помощью структуры [**всакуерисет**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="c705b-129">The following code snippet shows you how to register a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpRegister
//
// Purpose:  Register the given name in the PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string created using PeerIdentityCreate
//   pwzName     : name to register in PNRP
//   pwzCloud    : name of the cloud to register in, NULL = global cloud
//   pNodeInfo   : local node info returned from 

//
// Returns:  HRESULT
//
HRESULT PnrpRegister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddress)
{
    HRESULT         hr = S_OK;
    CSADDR_INFO     csaAddr = {0};
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // fill a CSADDR_INFO structure from the address
    //
    csaAddr.iProtocol = IPPROTO_TCP;
    csaAddr.iSocketType = SOCK_STREAM;
    csaAddr.LocalAddr.iSockaddrLength = sizeof(SOCKADDR_IN6);
    csaAddr.LocalAddr.lpSockaddr = (LPSOCKADDR)pAddress; 

    //
    // build the WSAQUERYSET required to register
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; //8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.dwNumberOfCsAddrs = 1; // one address
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpszComment = L"SomeComment";
    querySet.lpcsaBuffer = &csaAddr;
    querySet.lpBlob = &blPnrpData;

    // register the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_REGISTER, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }
    
    return hr;
}
```



 

 



