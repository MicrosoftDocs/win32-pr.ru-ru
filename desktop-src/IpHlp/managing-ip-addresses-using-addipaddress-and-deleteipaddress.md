---
title: Управление IP-адресами с помощью Аддипаддресс, Делетеипаддресс
description: Функция Аддипаддресс добавляет указанный IPv4-адрес к указанному адаптеру.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e726a2e5785641532abb739d61143f9fabfdd10c38e4b51fcd529f20d92503d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870094"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a>Управление IP-адресами с помощью Аддипаддресс, Делетеипаддресс

Функция [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) добавляет указанный IPv4-адрес к указанному адаптеру. Функция [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) удаляет указанный IPv4-адрес из указанного адаптера. Эти функции можно использовать для добавления и удаления IPv4-адресов в сетевом адаптере.

IPv4-адрес, добавленный функцией [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) , не является постоянным. IPv4-адрес существует, только если существует объект адаптера. Перезагрузка компьютера приводит к уничтожению IPv4-адреса, как и вручную сброс сетевого адаптера.

После успешного вызова [**АДДИПАДДРЕСС**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) DHCP будет отключен для ДОБАВЛЕННОГО IP-адреса. Таким образом, такие функции, как [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), требующие включения DHCP, не будут работать на ДОБАВЛЕННОМ IP-адресе. Для удаления добавленного IPv4-адреса можно использовать функцию [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .

> [!Note]  
> Групповые политики, политики предприятия и другие ограничения сети могут препятствовать успешному завершению этих функций. Прежде чем пытаться использовать эти функции, убедитесь, что приложение имеет необходимые сетевые разрешения.

 

**Использование Аддипаддресс**

1.  Объявите переменные **ulong** с именами `NTEContext` и `NTEInstance` , инициализируются нулем.
    > [!Note]  
    > `NTEContext`Переменная является единственным параметром функции [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) . чтобы удалить добавленный IP-адрес, он `NTEContext` должен быть сохранен и не изменен.

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  Объявите переменные для структур reduce и Ипмаск с именами `iaIPAddress` и `iaIPMask` соответственно. Эти значения представляют собой целые числа без знака. Инициализируйте `iaIPAddress` `iaIPMask` переменные и с помощью функции [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) .
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  Чтобы добавить IPv4-адрес, вызовите функцию [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) . Проверьте наличие ошибок и верните значение ошибки в переменную **DWORD** `dwRetVal` (для более обширной проверки ошибок).
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > Третий параметр — это индекс адаптера, который можно получить, вызвав функцию [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) . Предполагается, что переменная, возвращаемая этой функцией, называется `pIPAddrTable` . Справку по функции **жетипаддртабле** см. в разделе [Управление IP-адресами с помощью жетипаддртабле](managing-ip-addresses-using-getipaddrtable.md).

     

**Использование Делетеипаддресс**

-   Вызовите функцию [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) , передав `NTEContext` переменную в качестве ее параметра. Проверьте наличие ошибок и верните значение ошибки в переменную **DWORD** `dwRetVal` (для более обширной проверки ошибок).
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> Чтобы использовать [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), необходимо сначала вызвать [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) для получения маркера `NTEContext` . В предыдущей процедуре предполагается, что **аддипаддресс** уже вызван где-то в коде и `NTEContext` сохранен и остается неповрежденным.

 

Следующий шаг: [Получение сведений с помощью жетипстатистикс](retrieving-information-using-getipstatistics.md)

Предыдущий шаг: [Управление арендой DHCP с помощью ипрелеасеаддресс и ипреневаддресс](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

 

 
