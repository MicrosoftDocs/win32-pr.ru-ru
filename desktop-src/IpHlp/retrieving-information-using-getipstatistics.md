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
# <a name="retrieving-information-using-getipstatistics"></a>Получение сведений с помощью Жетипстатистикс

Функция [**жетипстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) заполняет указатель на структуру [**MIB \_ ипстатс**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) , используя сведения о текущей статистике IP, связанной с системой.

**Использование Жетипстатистикс**

1.  Объявите некоторые необходимые переменные.

    Объявите переменную **типа DWORD** `dwRetval` , которая будет использоваться для вызовов функций проверки ошибок. Объявите указатель на переменную [**MIB \_ ипстатс**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) с именем *пстатс* и выделите память для структуры. Убедитесь, что память может быть выделена.

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  Вызовите функцию [**жетипстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) с параметром *пстатс* , чтобы получить статистику IP-адресов для локального компьютера. Проверьте наличие ошибок и верните значение ошибки в переменную **типа DWORD** `dwRetval` . При возникновении ошибки `dwRetval` переменную можно использовать для более обширной проверки ошибок и создания отчетов.
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  Если вызов [**жетипстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) был успешным, распечатайте некоторые данные в структуре [**MIB \_ ипстатс**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) , на которую указывает параметр *пстатс* .
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  Освободите память, выделенную для структуры [**MIB \_ ипстатс**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) , на которую указывает параметр *пстатс* . Это необходимо сделать, когда приложению больше не требуются данные, возвращенные параметром *пстатс* .
    ```C++
    if (pStats)
        free(pStats);
    ```

    

Следующий шаг: [Получение сведений с помощью жетткпстатистикс](retrieving-information-using-gettcpstatistics.md)

Предыдущий шаг: [Управление IP-адресами с помощью аддипаддресс и делетеипаддресс](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

 

 
