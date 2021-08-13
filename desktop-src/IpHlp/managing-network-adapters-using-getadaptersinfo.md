---
description: Функция Жетадаптерсинфо заполняет указатель на информационную структуру IP- \_ адаптера \_ информацией о сетевых адаптерах, связанных с системой.
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: Управление сетевыми адаптерами с помощью Жетадаптерсинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da19541572af89e9429b9deba68efd4f4670324ffd9ff824e6c123295108f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644634"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a>Управление сетевыми адаптерами с помощью Жетадаптерсинфо

Функция [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) заполняет указатель на информационную структуру [**IP \_ - \_ адаптера**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) информацией о сетевых адаптерах, связанных с системой.

**Использование Жетадаптерсинфо**

1.  Объявите указатель на переменную [**\_ \_ сведений об адаптере IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) с именем *падаптеринфо* и переменную **ulong** с именем *улаутбуфлен*. Эти переменные передаются в качестве параметров функции [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) . Также создайте переменную **типа DWORD** с именем *двретвал* (для проверки ошибок).
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  Выделение памяти для структур.
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  Выполните начальный вызов [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , чтобы получить размер, необходимый для переменной *улаутбуфлен* .
    > [!Note]  
    > Этот вызов функции завершается ошибкой и используется, чтобы гарантировать, что переменная *улаутбуфлен* задает размер, достаточный для хранения всей информации, возвращенной в *падаптеринфо*. Это общая модель программирования для структур данных и функций этого типа.

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  Выполните второй вызов [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), передав *падаптеринфо* и *улаутбуфлен* в качестве параметров и выполнив общую проверку ошибок. Верните свое значение в переменную **DWORD** *двретвал* (для более обширной проверки ошибок).
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  Если вызов выполнен успешно, обратитесь к некоторым данным в структуре *падаптеринфо* .
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

    

6.  Освободите память, выделенную для структуры *падаптеринфо* .
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

Следующий шаг: [Управление интерфейсами с помощью жетинтерфацеинфо](managing-interfaces-using-getinterfaceinfo.md)

Предыдущий шаг: [Получение сведений с помощью жетнетворкпарамс](retrieving-information-using-getnetworkparams.md)

 

 



