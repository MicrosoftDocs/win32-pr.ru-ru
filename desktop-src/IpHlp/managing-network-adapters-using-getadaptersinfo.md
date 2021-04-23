---
description: Функция Жетадаптерсинфо заполняет указатель на информационную структуру IP- \_ адаптера \_ информацией о сетевых адаптерах, связанных с системой.
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: Управление сетевыми адаптерами с помощью Жетадаптерсинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470e0ce7682a86b29df912fa4d4b1297c2263382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081142"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a><span data-ttu-id="0bc22-103">Управление сетевыми адаптерами с помощью Жетадаптерсинфо</span><span class="sxs-lookup"><span data-stu-id="0bc22-103">Managing Network Adapters Using GetAdaptersInfo</span></span>

<span data-ttu-id="0bc22-104">Функция [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) заполняет указатель на информационную структуру [**IP \_ - \_ адаптера**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) информацией о сетевых адаптерах, связанных с системой.</span><span class="sxs-lookup"><span data-stu-id="0bc22-104">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function fills a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structure with information about the network adapters associated with the system.</span></span>

<span data-ttu-id="0bc22-105">**Использование Жетадаптерсинфо**</span><span class="sxs-lookup"><span data-stu-id="0bc22-105">**To use GetAdaptersInfo**</span></span>

1.  <span data-ttu-id="0bc22-106">Объявите указатель на переменную [**\_ \_ сведений об адаптере IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) с именем *падаптеринфо* и переменную **ulong** с именем *улаутбуфлен*.</span><span class="sxs-lookup"><span data-stu-id="0bc22-106">Declare a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) variable called *pAdapterInfo*, and a **ULONG** variable called *ulOutBufLen*.</span></span> <span data-ttu-id="0bc22-107">Эти переменные передаются в качестве параметров функции [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) .</span><span class="sxs-lookup"><span data-stu-id="0bc22-107">These variables are passed as parameters to the [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function.</span></span> <span data-ttu-id="0bc22-108">Также создайте переменную **типа DWORD** с именем *двретвал* (для проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="0bc22-108">Also create a **DWORD** variable called *dwRetVal* (for error checking).</span></span>
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="0bc22-109">Выделение памяти для структур.</span><span class="sxs-lookup"><span data-stu-id="0bc22-109">Allocate memory for the structures.</span></span>
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  <span data-ttu-id="0bc22-110">Выполните начальный вызов [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , чтобы получить размер, необходимый для переменной *улаутбуфлен* .</span><span class="sxs-lookup"><span data-stu-id="0bc22-110">Make an initial call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) to get the size needed into the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="0bc22-111">Этот вызов функции завершается ошибкой и используется, чтобы гарантировать, что переменная *улаутбуфлен* задает размер, достаточный для хранения всей информации, возвращенной в *падаптеринфо*.</span><span class="sxs-lookup"><span data-stu-id="0bc22-111">This call to the function is meant to fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the information returned to *pAdapterInfo*.</span></span> <span data-ttu-id="0bc22-112">Это общая модель программирования для структур данных и функций этого типа.</span><span class="sxs-lookup"><span data-stu-id="0bc22-112">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  <span data-ttu-id="0bc22-113">Выполните второй вызов [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), передав *падаптеринфо* и *улаутбуфлен* в качестве параметров и выполнив общую проверку ошибок.</span><span class="sxs-lookup"><span data-stu-id="0bc22-113">Make a second call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), passing *pAdapterInfo* and *ulOutBufLen* as parameters and doing general error checking.</span></span> <span data-ttu-id="0bc22-114">Верните свое значение в переменную **DWORD** *двретвал* (для более обширной проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="0bc22-114">Return its value to the **DWORD** variable *dwRetVal* (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  <span data-ttu-id="0bc22-115">Если вызов выполнен успешно, обратитесь к некоторым данным в структуре *падаптеринфо* .</span><span class="sxs-lookup"><span data-stu-id="0bc22-115">If the call was successful, access some of the data in the *pAdapterInfo* structure.</span></span>
    ```C++
    PIP_ADAPTER_INFO pAdapter = pAdapterInfo;
    while (pAdapter) {
        printf("Adapter Name: %s\n", pAdapter->AdapterName);
        printf("Adapter Desc: %s\n", pAdapter->Description);
        printf("\tAdapter Addr: \t");
        for (UINT i = 0; i < pAdapter->AddressLength; i++) {
            if (i == (pAdapter->AddressLength - 1))
                printf("%.2X\n",(int)pAdapter->Address[i]);
            else
                printf("%.2X-",(int)pAdapter->Address[i]);
        }
        printf("IP Address: %s\n", pAdapter->IpAddressList.IpAddress.String);
        printf("IP Mask: %s\n", pAdapter->IpAddressList.IpMask.String);
        printf("\tGateway: \t%s\n", pAdapter->GatewayList.IpAddress.String);
        printf("\t***\n");
        if (pAdapter->DhcpEnabled) {
            printf("\tDHCP Enabled: Yes\n");
            printf("\t\tDHCP Server: \t%s\n", pAdapter->DhcpServer.IpAddress.String);
        }
        else
          printf("\tDHCP Enabled: No\n");

      pAdapter = pAdapter->Next;
    }
    
    ```

    

6.  <span data-ttu-id="0bc22-116">Освободите память, выделенную для структуры *падаптеринфо* .</span><span class="sxs-lookup"><span data-stu-id="0bc22-116">Free any memory allocated for the *pAdapterInfo* structure.</span></span>
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

<span data-ttu-id="0bc22-117">Следующий шаг: [Управление интерфейсами с помощью жетинтерфацеинфо](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="0bc22-117">Next Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

<span data-ttu-id="0bc22-118">Предыдущий шаг: [Получение сведений с помощью жетнетворкпарамс](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="0bc22-118">Previous Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 



