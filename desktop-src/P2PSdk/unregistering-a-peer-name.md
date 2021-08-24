---
description: При отмене регистрации имени однорангового узла зарегистрированное имя удаляется из облака PNRP.
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Отмена регистрации имени однорангового узла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ee0bd03e881f93321c31dfccd03cc71459b323f1ed356a88f829489c578a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675014"
---
# <a name="unregistering-a-peer-name"></a>Отмена регистрации имени однорангового узла

При отмене регистрации имени однорангового узла зарегистрированное имя удаляется из облака PNRP.

## <a name="unregistering-a-peer-name"></a>Отмена регистрации имени однорангового узла

Чтобы отменить регистрацию имени однорангового узла, вызовите [**всасетсервице**](pnrp-and-wsasetservice.md). Параметр *ессоператион* должен иметь значение **рнрсервице \_ Delete**. Используйте рекомендации в следующих разделах этого раздела, чтобы внести необходимые настройки в параметры **всасетсервице** и структуру [**всакуерисет**](pnrp-and-wsaqueryset.md) .

## <a name="configuring-wsasetservice"></a>Настройка Всасетсервице

Когда приложение вызывает [**всасетсервице**](pnrp-and-wsasetservice.md), параметры должны быть настроены в соответствии со следующими спецификациями:

-   *ессоператион* должно иметь значение **рнрсервице \_ Delete**.
-   *dwFlags* должен быть равен нулю (0).
-   *лпксрегинфо* должен указывать на структуру [**всакуерисет**](pnrp-and-wsaqueryset.md) , которая должна быть настроена с помощью правил, описанных в следующем разделе этой статьи.

## <a name="configuring-wsaqueryset"></a>Настройка ВСАКУЕРИСЕТ

Структура [**всакуерисет**](pnrp-and-wsaqueryset.md) должна быть настроена в соответствии со следующими спецификациями:

-   **двсизе** должен указывать размер структуры [**всакуерисет**](pnrp-and-wsaqueryset.md) .
-   **лпсзсервицеинстанценаме** должен указывать на имя однорангового узла, для которого выполняется отмена регистрации.
-   **лпблоб** должен указывать на структуру [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .
-   **лпксабуффер** должен указывать на список адресов.

> [!Note]  
> Остальные члены описаны в разделе [**PNRP и всасетсервице**](pnrp-and-wsasetservice.md).

 

## <a name="an-example-of-unregistering-a-peer-name"></a>Пример отмены регистрации имени однорангового узла

В следующем фрагменте кода показано, как отменить регистрацию имени однорангового узла, предоставив правильные сведения при вызове [**всасетсервице**](pnrp-and-wsasetservice.md) с помощью структуры [**всакуерисет**](pnrp-and-wsaqueryset.md) .


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpUnregister
//
// Purpose:  Unregister the given name from a PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string originally used to register the name
//   pwzName     : name to unregister from PNRP
//   pwzCloud    : name of the cloud to unregister from, NULL = global cloud
//
// Returns:  HRESULT
//
HRESULT PnrpUnregister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // build the WSAQUERYSET required to unregister
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; // 8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;

    // unregister the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_DELETE, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    return hr;
}
```



 

 



