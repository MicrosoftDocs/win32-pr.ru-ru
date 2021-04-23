---
description: Функция Жетткпстатистикс заполняет указатель на \_ структуру MIB ткпстатс, используя сведения о статистике протокола TCP для локального компьютера.
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: Получение сведений с помощью Жетткпстатистикс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f4d4d42c2716d258ff72e3dd91ab750baaed20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673905"
---
# <a name="retrieving-information-using-gettcpstatistics"></a><span data-ttu-id="48999-103">Получение сведений с помощью Жетткпстатистикс</span><span class="sxs-lookup"><span data-stu-id="48999-103">Retrieving Information Using GetTcpStatistics</span></span>

<span data-ttu-id="48999-104">Функция [**жетткпстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) заполняет указатель на структуру [**MIB \_ ткпстатс**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) , используя сведения о статистике протокола TCP для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="48999-104">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function fills a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure with information on the TCP protocol statistics for the local computer.</span></span>

<span data-ttu-id="48999-105">**Использование Жетткпстатистикс**</span><span class="sxs-lookup"><span data-stu-id="48999-105">**To use GetTcpStatistics**</span></span>

1.  <span data-ttu-id="48999-106">Объявите некоторые необходимые переменные.</span><span class="sxs-lookup"><span data-stu-id="48999-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="48999-107">Объявите переменную **типа DWORD** `dwRetVal` , которая будет использоваться для вызовов функций проверки ошибок.</span><span class="sxs-lookup"><span data-stu-id="48999-107">Declare a **DWORD** variable `dwRetVal` that will be using for error checking function calls.</span></span> <span data-ttu-id="48999-108">Объявите указатель на переменную [**MIB \_ ткпстатс**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) с именем *пткпстатс* и выделите память для структуры.</span><span class="sxs-lookup"><span data-stu-id="48999-108">Declare a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) variable called *pTCPStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="48999-109">Убедитесь, что память может быть выделена.</span><span class="sxs-lookup"><span data-stu-id="48999-109">Check that memory could be allocated.</span></span>

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  <span data-ttu-id="48999-110">Вызовите функцию [**жетткпстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) с параметром *пткпстатс* , чтобы получить статистику TCP для IPv4 на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="48999-110">Call the [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function with the *pTCPStats* parameter to retrieve TCP statistics for IPv4 on the local computer.</span></span> <span data-ttu-id="48999-111">Проверьте наличие ошибок и верните значение ошибки в переменную **типа DWORD** `dwRetVal` .</span><span class="sxs-lookup"><span data-stu-id="48999-111">Check for errors and return the error value in the **DWORD** variable `dwRetVal`.</span></span> <span data-ttu-id="48999-112">При возникновении ошибки `dwRetVal` переменную можно использовать для более обширной проверки ошибок и создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="48999-112">If an error occurs, the `dwRetVal` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  <span data-ttu-id="48999-113">Если вызов выполнен успешно, получите доступ к данным, возвращенным в базе [**MIB \_ ткпстатс**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) , на которую указывает параметр *пткпстатс* .</span><span class="sxs-lookup"><span data-stu-id="48999-113">If the call was successful, access the data returned in the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) pointed to by the *pTCPStats* parameter.</span></span>
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  <span data-ttu-id="48999-114">Освободите память, выделенную для структуры [**MIB \_ ткпстатс**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) , на которую указывает параметр *пткпстатс* .</span><span class="sxs-lookup"><span data-stu-id="48999-114">Free the memory allocated for the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure pointed to by the *pTCPStats* parameter.</span></span> <span data-ttu-id="48999-115">Это необходимо сделать, когда приложению больше не требуются данные, возвращенные параметром *пткпстатс* .</span><span class="sxs-lookup"><span data-stu-id="48999-115">This should be done once the application no longer needs the data returned by the *pTCPStats* parameter.</span></span>
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

<span data-ttu-id="48999-116">Следующий шаг: [Получение сведений с помощью жетипстатистикс](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="48999-116">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="48999-117">Предыдущий шаг: [Получение сведений с помощью жетипстатистикс](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="48999-117">Previous Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

## <a name="complete-source-code"></a><span data-ttu-id="48999-118">Полный исходный код</span><span class="sxs-lookup"><span data-stu-id="48999-118">Complete Source Code</span></span>

-   [<span data-ttu-id="48999-119">Полный исходный код приложения модуля поддержки IP-адресов</span><span class="sxs-lookup"><span data-stu-id="48999-119">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

 

 
