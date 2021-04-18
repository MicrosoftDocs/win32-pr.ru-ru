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
# <a name="retrieving-information-using-gettcpstatistics"></a>Получение сведений с помощью Жетткпстатистикс

Функция [**жетткпстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) заполняет указатель на структуру [**MIB \_ ткпстатс**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) , используя сведения о статистике протокола TCP для локального компьютера.

**Использование Жетткпстатистикс**

1.  Объявите некоторые необходимые переменные.

    Объявите переменную **типа DWORD** `dwRetVal` , которая будет использоваться для вызовов функций проверки ошибок. Объявите указатель на переменную [**MIB \_ ткпстатс**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) с именем *пткпстатс* и выделите память для структуры. Убедитесь, что память может быть выделена.

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  Вызовите функцию [**жетткпстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) с параметром *пткпстатс* , чтобы получить статистику TCP для IPv4 на локальном компьютере. Проверьте наличие ошибок и верните значение ошибки в переменную **типа DWORD** `dwRetVal` . При возникновении ошибки `dwRetVal` переменную можно использовать для более обширной проверки ошибок и создания отчетов.
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  Если вызов выполнен успешно, получите доступ к данным, возвращенным в базе [**MIB \_ ткпстатс**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) , на которую указывает параметр *пткпстатс* .
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  Освободите память, выделенную для структуры [**MIB \_ ткпстатс**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) , на которую указывает параметр *пткпстатс* . Это необходимо сделать, когда приложению больше не требуются данные, возвращенные параметром *пткпстатс* .
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

Следующий шаг: [Получение сведений с помощью жетипстатистикс](retrieving-information-using-getipstatistics.md)

Предыдущий шаг: [Получение сведений с помощью жетипстатистикс](retrieving-information-using-getipstatistics.md)

## <a name="complete-source-code"></a>Полный исходный код

-   [Полный исходный код приложения модуля поддержки IP-адресов](complete-ip-helper-application-source-code.md)

 

 
