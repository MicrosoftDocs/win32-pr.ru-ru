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
# <a name="retrieving-information-using-getnetworkparams"></a>Получение сведений с помощью Жетнетворкпарамс

Функция [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) заполняет указатель на [**фиксированную \_ информационную**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) структуру данными о текущих параметрах сети.

**Использование Жетнетворкпарамс**

1.  Объявите указатель на объект [**фиксированной \_ информации**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) с именем *пфиксединфо* и объект **ulong** с именем *улаутбуфлен*. Эти переменные передаются в качестве параметров функции [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Также создайте переменную **типа DWORD** *двретвал* (используется для проверки ошибок).
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  Выделение памяти для структур.
    > [!Note]  
    > Размер *улаутбуфлен* недостаточно для хранения информации. См. следующий шаг.

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  Выполните начальный вызов [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , чтобы получить размер, необходимый для переменной *улаутбуфлен* .
    > [!Note]  
    > Эта функция функции завершится ошибкой и будет использоваться, чтобы гарантировать, что переменная *улаутбуфлен* задает размер, достаточный для хранения всех данных, возвращаемых в *пфиксединфо*. Это общая модель программирования для структур данных и функций этого типа.

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  Выполните второй вызов [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , используя общую проверку ошибок и возвращая его значение в переменную **DWORD** *двретвал*; используется для более сложных проверок ошибок.
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  Если вызов выполнен успешно, получите доступ к данным из структуры данных *пфиксединфо* .
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

    

6.  Освободите память, выделенную для структуры *пфиксединфо* .
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

Следующий шаг: [Управление сетевыми адаптерами с помощью жетадаптерсинфо](managing-network-adapters-using-getadaptersinfo.md)

Предыдущий шаг: [Создание базового вспомогательного приложения IP-адресов](creating-a-basic-ip-helper-application.md)

 

 



