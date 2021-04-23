---
description: При отмене регистрации имени однорангового узла зарегистрированное имя удаляется из облака PNRP.
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Отмена регистрации имени однорангового узла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd482cc9cfd8c32d7bc95edd00e866e2d87b7a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998538"
---
# <a name="unregistering-a-peer-name"></a><span data-ttu-id="b6dd0-103">Отмена регистрации имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="b6dd0-103">Unregistering a Peer Name</span></span>

<span data-ttu-id="b6dd0-104">При отмене регистрации имени однорангового узла зарегистрированное имя удаляется из облака PNRP.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-104">When you unregister a peer name, a registered name is removed from a Peer Name Resolution Protocol (PNRP) cloud.</span></span>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="b6dd0-105">Отмена регистрации имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="b6dd0-105">Unregistering a Peer Name</span></span>

<span data-ttu-id="b6dd0-106">Чтобы отменить регистрацию имени однорангового узла, вызовите [**всасетсервице**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="b6dd0-106">To unregister a peer name, call [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="b6dd0-107">Параметр *ессоператион* должен иметь значение **рнрсервице \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-107">The *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span> <span data-ttu-id="b6dd0-108">Используйте рекомендации в следующих разделах этого раздела, чтобы внести необходимые настройки в параметры **всасетсервице** и структуру [**всакуерисет**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="b6dd0-108">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

## <a name="configuring-wsasetservice"></a><span data-ttu-id="b6dd0-109">Настройка Всасетсервице</span><span class="sxs-lookup"><span data-stu-id="b6dd0-109">Configuring WSASetService</span></span>

<span data-ttu-id="b6dd0-110">Когда приложение вызывает [**всасетсервице**](pnrp-and-wsasetservice.md), параметры должны быть настроены в соответствии со следующими спецификациями:</span><span class="sxs-lookup"><span data-stu-id="b6dd0-110">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="b6dd0-111">*ессоператион* должно иметь значение **рнрсервице \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-111">*essOperation* must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="b6dd0-112">*dwFlags* должен быть равен нулю (0).</span><span class="sxs-lookup"><span data-stu-id="b6dd0-112">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="b6dd0-113">*лпксрегинфо* должен указывать на структуру [**всакуерисет**](pnrp-and-wsaqueryset.md) , которая должна быть настроена с помощью правил, описанных в следующем разделе этой статьи.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-113">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following section of this topic.</span></span>

## <a name="configuring-wsaqueryset"></a><span data-ttu-id="b6dd0-114">Настройка ВСАКУЕРИСЕТ</span><span class="sxs-lookup"><span data-stu-id="b6dd0-114">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="b6dd0-115">Структура [**всакуерисет**](pnrp-and-wsaqueryset.md) должна быть настроена в соответствии со следующими спецификациями:</span><span class="sxs-lookup"><span data-stu-id="b6dd0-115">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="b6dd0-116">**двсизе** должен указывать размер структуры [**всакуерисет**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="b6dd0-116">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="b6dd0-117">**лпсзсервицеинстанценаме** должен указывать на имя однорангового узла, для которого выполняется отмена регистрации.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-117">**lpszServiceInstanceName** must point to the peer name that is being unregistered.</span></span>
-   <span data-ttu-id="b6dd0-118">**лпблоб** должен указывать на структуру [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="b6dd0-118">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="b6dd0-119">**лпксабуффер** должен указывать на список адресов.</span><span class="sxs-lookup"><span data-stu-id="b6dd0-119">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="b6dd0-120">Остальные члены описаны в разделе [**PNRP и всасетсервице**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="b6dd0-120">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

## <a name="an-example-of-unregistering-a-peer-name"></a><span data-ttu-id="b6dd0-121">Пример отмены регистрации имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="b6dd0-121">An Example of Unregistering a Peer Name</span></span>

<span data-ttu-id="b6dd0-122">В следующем фрагменте кода показано, как отменить регистрацию имени однорангового узла, предоставив правильные сведения при вызове [**всасетсервице**](pnrp-and-wsasetservice.md) с помощью структуры [**всакуерисет**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="b6dd0-122">The following code snippet shows you how to unregister a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


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



 

 



