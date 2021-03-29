---
title: Управление арендой DHCP с помощью Ипрелеасеаддресс, Ипреневаддресс
description: Функции Ипрелеасеаддресс и Ипреневаддресс используются для освобождения и продления текущей аренды протокола динамической настройки узла (DHCP).
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897206"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a>Управление арендой DHCP с помощью Ипрелеасеаддресс, Ипреневаддресс

Функции [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) и [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) используются для освобождения и продления текущей аренды протокола динамической настройки узла (DHCP). Функция **ипрелеасеаддресс** освобождает IPv4-адрес, который ранее был получен с помощью DHCP. Функция **ипреневаддресс** обновляет аренду на IPv4-адресе, ранее полученном с помощью DHCP. Обычно эти две функции используются совместно, сначала освобождайте аренду вызовом **ипрелеасеаддресс**, а затем продлите аренду, вызвав функцию **ипреневаддресс** .

Когда DHCP-клиент ранее получил аренду DHCP и [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) не вызывается до функции [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , запрос DHCP-клиента отправляется на DHCP-сервер, ВЫДАВШИЙ начальную аренду DHCP. Возможно, этот DHCP-сервер недоступен, или DHCP-запрос может завершиться ошибкой. Когда узел ранее получил аренду DHCP и **ипрелеасеаддресс** вызывается перед функцией **ипреневаддресс** , DHCP-клиент сначала освобождает полученный IP-адрес и отправляет запрос DHCP-клиента на ответ от любого доступного DHCP-сервера.

> [!Note]  
> Для выполнения функций [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) и [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) требуется, чтобы DHCP был включен правильно.

 

Функция [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) принимает указатель на структуру [**\_ \_ \_ карты индекса адаптера IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) в качестве единственного параметра. Чтобы получить этот параметр, сначала вызовите [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo). Справку по функции **жетинтерфацеинфо** см. в разделе [Управление интерфейсами с помощью жетинтерфацеинфо](managing-interfaces-using-getinterfaceinfo.md).

**Использование Ипрелеасеаддресс**

1.  Получите указатель на структуру [**\_ \_ \_ карты индекса адаптера IP-адресов**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) с помощью функции [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) . (Дополнительные сведения о функции Жетинтерфацеинфо см. в разделе [Управление интерфейсами с помощью жетинтерфацеинфо](managing-interfaces-using-getinterfaceinfo.md)). Создайте объект **типа DWORD** `dwRetVal` (используется для проверки ошибок). Предполагается, что переменная, возвращаемая функцией **жетинтерфацеинфо** , называется `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Если DHCP включен, вызовите функцию [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) , передав переменную [**\_ \_ \_ карты индекса IP-адаптера**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) в `Adapter` качестве параметра. Проверьте наличие общих ошибок и верните его значение переменной **DWORD** `dwRetVal` (для более обширной проверки ошибок).
    > [!Note]  
    > Функция [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) возвращает параметр, который можно использовать для проверки того, включен ли протокол DHCP перед вызовом этих функций. Справку по **жетадаптерсинфо** см. в разделе [Управление сетевыми адаптерами с помощью жетадаптерсинфо](managing-network-adapters-using-getadaptersinfo.md).

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> Обычно эти две функции используются совместно, вызывая функцию [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) и вызывая функцию [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , передавая ту же структуру, что и параметр, в обе функции. В следующей процедуре предполагается, что функции не используются вместе. Однако если функции используются совместно, пропустите шаг 1.

 

**Использование Ипреневаддресс**

1.  Получите указатель на структуру [**\_ \_ \_ карты индекса адаптера IP-адресов**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) с помощью функции [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) . (Дополнительные сведения о функции **жетинтерфацеинфо** см. в разделе [Управление интерфейсами с помощью жетинтерфацеинфо](managing-interfaces-using-getinterfaceinfo.md)). Объявите  объект DWORD `dwRetVal` (используемый для проверки ошибок), если эта переменная не была объявлена. Предполагается, что переменная, возвращаемая функцией **жетинтерфацеинфо** , называется `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Вызовите функцию [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , передав в качестве параметра переменную [**\_ \_ \_ карты индекса IP-адаптера**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` . Проверьте наличие общих ошибок и верните его значение переменной **DWORD** `dwRetVal` (для более обширной проверки ошибок).
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

Следующий шаг: [Управление IP-адресами с помощью аддипаддресс и делетеипаддресс](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

Предыдущий шаг: [Управление IP-адресами с помощью жетипаддртабле](managing-ip-addresses-using-getipaddrtable.md)

 

 



