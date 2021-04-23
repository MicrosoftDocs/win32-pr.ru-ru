---
description: Функция Жетипстатистикс заполняет указатель на \_ структуру MIB ипстатс, используя сведения о текущей статистике IP, связанной с системой.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Получение сведений с помощью Жетипстатистикс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6267c3939548c8f8ea9ab2705ea1769360748e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673906"
---
# <a name="retrieving-information-using-getipstatistics"></a><span data-ttu-id="8fa3f-103">Получение сведений с помощью Жетипстатистикс</span><span class="sxs-lookup"><span data-stu-id="8fa3f-103">Retrieving Information Using GetIpStatistics</span></span>

<span data-ttu-id="8fa3f-104">Функция [**жетипстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) заполняет указатель на структуру [**MIB \_ ипстатс**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) , используя сведения о текущей статистике IP, связанной с системой.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-104">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function fills a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure with information about the current IP statistics associated with the system.</span></span>

<span data-ttu-id="8fa3f-105">**Использование Жетипстатистикс**</span><span class="sxs-lookup"><span data-stu-id="8fa3f-105">**To use GetIpStatistics**</span></span>

1.  <span data-ttu-id="8fa3f-106">Объявите некоторые необходимые переменные.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="8fa3f-107">Объявите переменную **типа DWORD** `dwRetval` , которая будет использоваться для вызовов функций проверки ошибок.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-107">Declare a **DWORD** variable `dwRetval` that will be using for error checking function calls.</span></span> <span data-ttu-id="8fa3f-108">Объявите указатель на переменную [**MIB \_ ипстатс**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) с именем *пстатс* и выделите память для структуры.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-108">Declare a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) variable called *pStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="8fa3f-109">Убедитесь, что память может быть выделена.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-109">Check that memory could be allocated.</span></span>

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  <span data-ttu-id="8fa3f-110">Вызовите функцию [**жетипстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) с параметром *пстатс* , чтобы получить статистику IP-адресов для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-110">Call the [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function with the *pStats* parameter to retrieve IP statistics for the local computer.</span></span> <span data-ttu-id="8fa3f-111">Проверьте наличие ошибок и верните значение ошибки в переменную **типа DWORD** `dwRetval` .</span><span class="sxs-lookup"><span data-stu-id="8fa3f-111">Check for errors and return the error value in the **DWORD** variable `dwRetval`.</span></span> <span data-ttu-id="8fa3f-112">При возникновении ошибки `dwRetval` переменную можно использовать для более обширной проверки ошибок и создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-112">If an error occurs, the `dwRetval` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  <span data-ttu-id="8fa3f-113">Если вызов [**жетипстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) был успешным, распечатайте некоторые данные в структуре [**MIB \_ ипстатс**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) , на которую указывает параметр *пстатс* .</span><span class="sxs-lookup"><span data-stu-id="8fa3f-113">If the call to [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) was successful, print out some of the data in the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span>
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  <span data-ttu-id="8fa3f-114">Освободите память, выделенную для структуры [**MIB \_ ипстатс**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) , на которую указывает параметр *пстатс* .</span><span class="sxs-lookup"><span data-stu-id="8fa3f-114">Free the memory allocated for the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span> <span data-ttu-id="8fa3f-115">Это необходимо сделать, когда приложению больше не требуются данные, возвращенные параметром *пстатс* .</span><span class="sxs-lookup"><span data-stu-id="8fa3f-115">This should be done once the application no longer needs the data returned by the *pStats* parameter.</span></span>
    ```C++
    if (pStats)
        free(pStats);
    ```

    

<span data-ttu-id="8fa3f-116">Следующий шаг: [Получение сведений с помощью жетткпстатистикс](retrieving-information-using-gettcpstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="8fa3f-116">Next Step: [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span></span>

<span data-ttu-id="8fa3f-117">Предыдущий шаг: [Управление IP-адресами с помощью аддипаддресс и делетеипаддресс](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="8fa3f-117">Previous Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

 

 
