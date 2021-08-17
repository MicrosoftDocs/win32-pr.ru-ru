---
description: Функция Жетинтерфацеинфо заполняет указатель на информационную структуру IP- \_ интерфейса \_ с информацией о интерфейсах, связанных с системой.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Управление интерфейсами с помощью Жетинтерфацеинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc2afa6fe0b520e1cc5f952b44bc94052b630f4335bd739b4d7c3582d16e277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146747"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a>Управление интерфейсами с помощью Жетинтерфацеинфо

Функция [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) заполняет указатель на информационную структуру [**IP \_ - \_ интерфейса**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) с информацией о интерфейсах, связанных с системой.

**Использование Жетинтерфацеинфо**

1.  Объявите указатель на объект [**\_ \_ сведений об интерфейсе IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) с именем `pInfo` и объект **ulong** с именем `ulOutBufLen` . Также объявите объект **DWORD** с именем `dwRetVal` (используется для проверки ошибок).
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  Выделение памяти для структур.
    > [!Note]  
    > Размер недостаточно `ulOutBufLen` для хранения информации. См. следующий шаг.

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  Выполните начальный вызов [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) , чтобы получить размер, необходимый для `ulOutBufLen` переменной.
    > [!Note]  
    > Этот вызов функции должен завершиться ошибкой и использоваться, чтобы гарантировать, что `ulOutBufLen` переменная задает размер, достаточный для хранения всех данных, возвращаемых в `pInfo` . Это общая модель программирования в модуле поддержки IP для структур данных и функций этого типа.

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  Создайте второй вызов [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) с общей проверкой ошибок и верните его значение в переменную **DWORD** `dwRetVal` (для более расширенной проверки ошибок).
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  Если вызов выполнен успешно, получите доступ к данным из `pInfo` структуры данных.

    ```C++
            printf("  GetInterfaceInfo succeeded.\n");

            printf("  Num Adapters: %ld\n\n", pInterfaceInfo->NumAdapters);
            for (i = 0; i < (unsigned int) pInterfaceInfo->NumAdapters; i++) {
                printf("  Adapter Index[%d]: %ld\n", i,
                       pInterfaceInfo->Adapter[i].Index);
                printf("  Adapter Name[%d]:  %ws\n\n", i,
                       pInterfaceInfo->Adapter[i].Name);
            }
        }
    ```

    

    > [!Note]  
    > % WS в первой строке обозначает расширенную строку. Это используется потому, что атрибут **Name** структуры [**\_ \_ \_ карты индекса IP-адаптера**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` имеет значение типа **WCHAR**, которое представляет собой строку в Юникоде.

     

6.  Освободите память, выделенную для структуры *пинфо* .
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

Следующий шаг: [Управление IP-адресами с помощью жетипаддртабле](managing-ip-addresses-using-getipaddrtable.md)

Предыдущий шаг: [Управление сетевыми адаптерами с помощью жетадаптерсинфо](managing-network-adapters-using-getadaptersinfo.md)

 

 



