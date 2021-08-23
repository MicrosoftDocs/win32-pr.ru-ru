---
description: 'Чтобы зарегистрировать одноранговое имя, приложение должно предоставить следующие сведения: IP-адрес Листпир Идентитипир Намеиф. имя однорангового узла не защищено. удостоверение является необязательным.'
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: Регистрация имени однорангового узла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcedbe3e405e21ec9709289e8a9237179703b1b8e81f40b449479373524beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011492"
---
# <a name="registering-a-peer-name"></a>Регистрация имени однорангового узла

Чтобы зарегистрировать одноранговое имя, приложение должно предоставить следующие сведения:

-   Список IP-адресов
-   [Одноранговый идентификатор](creating-a-peer-identity.md)
-   [Имя однорангового узла](peer-names.md)

Если имя однорангового узла не защищено, то удостоверение является необязательным. Если для однорангового узла задано **значение NULL**, протокол PNRP использует внутреннее удостоверение однорангового узла по умолчанию.

## <a name="registering-a-peer-name"></a>Регистрация имени однорангового узла

После определения списка IP-адресов, однорангового узла и имени однорангового узла приложение может зарегистрировать имя однорангового узла, вызвав [**всасетсервице**](pnrp-and-wsasetservice.md). Используйте рекомендации в следующих разделах этого раздела, чтобы внести необходимые настройки в параметры **всасетсервице** и структуру [**всакуерисет**](pnrp-and-wsaqueryset.md) .

### <a name="configuring-wsasetservice"></a>Настройка Всасетсервице

Когда приложение вызывает [**всасетсервице**](pnrp-and-wsasetservice.md), параметры должны быть настроены в соответствии со следующими спецификациями:

-   *ессоператион* должно иметь значение **рнрсервице \_ Register**.
-   *dwFlags* должен быть равен нулю (0).
-   *лпксрегинфо* должен указывать на структуру [**всакуерисет**](pnrp-and-wsaqueryset.md) , которая должна быть настроена с помощью правил, описанных в разделе **Настройка всакуерисет** этой статьи.

### <a name="configuring-wsaqueryset"></a>Настройка ВСАКУЕРИСЕТ

Структура [**всакуерисет**](pnrp-and-wsaqueryset.md) должна быть настроена в соответствии со следующими спецификациями:

-   **двсизе** должен указывать размер структуры [**всакуерисет**](pnrp-and-wsaqueryset.md) .
-   **лпсзсервицеинстанценаме** должен указывать на Регистрируемое имя однорангового узла.
-   **лпблоб** должен указывать на структуру [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .
-   **лпксабуффер** должен указывать на список адресов.

> [!Note]  
> Остальные члены описаны в разделе [**PNRP и всасетсервице**](pnrp-and-wsasetservice.md).

 

После регистрации имени однорангового узла сведения доступны для одноранговой инфраструктуры. Однако между временем регистрации и распространением сведений о регистрации на другие узлы существует задержка. В течение этого времени другие узлы, возможно, не смогут разрешить только что зарегистрированный одноранговый узел.

## <a name="example-of-registering-a-peer-name"></a>Пример регистрации имени однорангового узла

В следующем фрагменте кода показано, как зарегистрировать имя однорангового узла, предоставив правильные сведения при вызове [**всасетсервице**](pnrp-and-wsasetservice.md) с помощью структуры [**всакуерисет**](pnrp-and-wsaqueryset.md) .


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



 

 



