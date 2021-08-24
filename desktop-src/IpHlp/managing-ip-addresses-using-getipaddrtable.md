---
description: Функция Жетипаддртабле заполняет указатель на \_ структуру MIB ипаддртабле, используя сведения о текущих IP-адресах, связанных с системой.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Управление IP-адресами с помощью Жетипаддртабле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090bdb1e73d3f770eafb3a5e70893253918eb68573ebd05aa6ec40a609a7ba4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146687"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a>Управление IP-адресами с помощью Жетипаддртабле

Функция [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) заполняет указатель на структуру [**MIB \_ ипаддртабле**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) , используя сведения о текущих IP-адресах, связанных с системой.

**Использование Жетипаддртабле**

1.  Объявите указатель на объект [**MIB \_ ипаддртабле**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) , именуемый *Пипаддртабле*, и объект **DWORD** с именем *двсизе*. Эти переменные передаются в качестве параметров функции [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) . Также создайте переменную **типа DWORD** с именем *двретвал* (используется для проверки ошибок).
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  Выделение памяти для структуры.
    > [!Note]  
    > Размер *двсизе* недостаточно для хранения информации. См. следующий шаг.

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  Выполните начальный вызов [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , чтобы получить размер, необходимый для переменной *двсизе* .
    > [!Note]  
    > Этот вызов функции завершается ошибкой и используется, чтобы гарантировать, что переменная *двсизе* задает размер, достаточный для хранения всей информации, возвращенной в *пипаддртабле*. Это общая модель программирования для структур данных и функций этого типа.

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  Создайте второй вызов [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) с общей проверкой ошибок и верните его значение в переменную **DWORD** *двретвал* (для более расширенной проверки ошибок).
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  Если вызов выполнен успешно, получите доступ к данным из структуры данных *пипаддртабле* .
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  Освободите память, выделенную для структуры *пипаддртабле* .
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> Объекты **DWORD** *дваддр* и *двмаск* возвращаются в виде числовых значений в порядке байтов узла, а не в сетевом порядке байтов. Эти значения не являются точками IP-адресов.

 

Следующий шаг: [Управление арендой DHCP с помощью ипрелеасеаддресс и ипреневаддресс](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

Предыдущий шаг: [Управление интерфейсами с помощью жетинтерфацеинфо](managing-interfaces-using-getinterfaceinfo.md)

 

 
