---
description: Заполняет указатель ФИКСИРОВАНной \_ структурой сведений данными о текущих параметрах сети.
ms.assetid: d377951f-e7d4-4482-9182-2c3b153cb325
title: Получение сведений с помощью Жетнетворкпарамс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20aed9b1ffa761ec53637d4d5b165e3fd2c2673d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264863"
---
# <a name="retrieving-information-using-getnetworkparams"></a><span data-ttu-id="6c0a5-103">Получение сведений с помощью Жетнетворкпарамс</span><span class="sxs-lookup"><span data-stu-id="6c0a5-103">Retrieving Information Using GetNetworkParams</span></span>

<span data-ttu-id="6c0a5-104">Функция [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) заполняет указатель на [**фиксированную \_ информационную**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) структуру данными о текущих параметрах сети.</span><span class="sxs-lookup"><span data-stu-id="6c0a5-104">The [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function fills a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) structure with data about the current network settings.</span></span>

<span data-ttu-id="6c0a5-105">**Использование Жетнетворкпарамс**</span><span class="sxs-lookup"><span data-stu-id="6c0a5-105">**To use GetNetworkParams**</span></span>

1.  <span data-ttu-id="6c0a5-106">Объявите указатель на объект [**фиксированной \_ информации**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) с именем *пфиксединфо* и объект **ulong** с именем *улаутбуфлен*.</span><span class="sxs-lookup"><span data-stu-id="6c0a5-106">Declare a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) object called *pFixedInfo*, and a **ULONG** object called *ulOutBufLen*.</span></span> <span data-ttu-id="6c0a5-107">Эти переменные передаются в качестве параметров функции [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) .</span><span class="sxs-lookup"><span data-stu-id="6c0a5-107">These variables are passed as parameters to the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="6c0a5-108">Также создайте переменную **типа DWORD** *двретвал* (используется для проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="6c0a5-108">Also create a **DWORD** variable *dwRetVal* (used for error checking).</span></span>
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  <span data-ttu-id="6c0a5-109">Выделение памяти для структур.</span><span class="sxs-lookup"><span data-stu-id="6c0a5-109">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="6c0a5-110">Размер *улаутбуфлен* недостаточно для хранения информации.</span><span class="sxs-lookup"><span data-stu-id="6c0a5-110">The size of *ulOutBufLen* is not sufficient to hold the information.</span></span> <span data-ttu-id="6c0a5-111">См. следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="6c0a5-111">See the next step.</span></span>

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  <span data-ttu-id="6c0a5-112">Выполните начальный вызов [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , чтобы получить размер, необходимый для переменной *улаутбуфлен* .</span><span class="sxs-lookup"><span data-stu-id="6c0a5-112">Make an initial call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) to get the size required for the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="6c0a5-113">Эта функция функции завершится ошибкой и будет использоваться, чтобы гарантировать, что переменная *улаутбуфлен* задает размер, достаточный для хранения всех данных, возвращаемых в *пфиксединфо*.</span><span class="sxs-lookup"><span data-stu-id="6c0a5-113">This function function will fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the data returned to *pFixedInfo*.</span></span> <span data-ttu-id="6c0a5-114">Это общая модель программирования для структур данных и функций этого типа.</span><span class="sxs-lookup"><span data-stu-id="6c0a5-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  <span data-ttu-id="6c0a5-115">Выполните второй вызов [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , используя общую проверку ошибок и возвращая его значение в переменную **DWORD** *двретвал*; используется для более сложных проверок ошибок.</span><span class="sxs-lookup"><span data-stu-id="6c0a5-115">Make a second call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) using general error checking and returning its value to the **DWORD** variable *dwRetVal*; used for more advanced error checking.</span></span>
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  <span data-ttu-id="6c0a5-116">Если вызов выполнен успешно, получите доступ к данным из структуры данных *пфиксединфо* .</span><span class="sxs-lookup"><span data-stu-id="6c0a5-116">If the call was successful, access the data from the *pFixedInfo* data structure.</span></span>
    ```C++
            printf("\tHost Name: %s\n", pFixedInfo->HostName);
            printf("\tDomain Name: %s\n", pFixedInfo->DomainName);
            printf("\tDNS Servers:\n");
            printf("\t\t%s\n", pFixedInfo->DnsServerList.IpAddress.String);

            pIPAddr = pFixedInfo->DnsServerList.Next;
            while (pIPAddr) {
                printf("\t\t%s\n", pIPAddr->IpAddress.String);
                pIPAddr = pIPAddr->Next;
            }

            printf("\tNode Type: ");
            switch (pFixedInfo->NodeType) {
            case 1:
                printf("%s\n", "Broadcast");
                break;
            case 2:
                printf("%s\n", "Peer to peer");
                break;
            case 4:
                printf("%s\n", "Mixed");
                break;
            case 8:
                printf("%s\n", "Hybrid");
                break;
            default:
                printf("\n");
            }

            printf("\tNetBIOS Scope ID: %s\n", pFixedInfo->ScopeId);

            if (pFixedInfo->EnableRouting)
                printf("\tIP Routing Enabled: Yes\n");
            else
                printf("\tIP Routing Enabled: No\n");

            if (pFixedInfo->EnableProxy)
                printf("\tWINS Proxy Enabled: Yes\n");
            else
                printf("\tWINS Proxy Enabled: No\n");

            if (pFixedInfo->EnableDns)
                printf("\tNetBIOS Resolution Uses DNS: Yes\n");
            else
                printf("\tNetBIOS Resolution Uses DNS: No\n");
    ```

    

6.  <span data-ttu-id="6c0a5-117">Освободите память, выделенную для структуры *пфиксединфо* .</span><span class="sxs-lookup"><span data-stu-id="6c0a5-117">Free any memory allocated for the *pFixedInfo* structure.</span></span>
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

<span data-ttu-id="6c0a5-118">Следующий шаг: [Управление сетевыми адаптерами с помощью жетадаптерсинфо](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="6c0a5-118">Next Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

<span data-ttu-id="6c0a5-119">Предыдущий шаг: [Создание базового вспомогательного приложения IP-адресов](creating-a-basic-ip-helper-application.md)</span><span class="sxs-lookup"><span data-stu-id="6c0a5-119">Previous Step: [Creating a Basic IP Helper Application](creating-a-basic-ip-helper-application.md)</span></span>

 

 



