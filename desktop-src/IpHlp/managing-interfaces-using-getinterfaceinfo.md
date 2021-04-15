---
description: Функция Жетинтерфацеинфо заполняет указатель на информационную структуру IP- \_ интерфейса \_ с информацией о интерфейсах, связанных с системой.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Управление интерфейсами с помощью Жетинтерфацеинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8ad420f8a2d4fdbacc2bf01e65f5d9fbc9d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682615"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a><span data-ttu-id="6818b-103">Управление интерфейсами с помощью Жетинтерфацеинфо</span><span class="sxs-lookup"><span data-stu-id="6818b-103">Managing Interfaces Using GetInterfaceInfo</span></span>

<span data-ttu-id="6818b-104">Функция [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) заполняет указатель на информационную структуру [**IP \_ - \_ интерфейса**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) с информацией о интерфейсах, связанных с системой.</span><span class="sxs-lookup"><span data-stu-id="6818b-104">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function fills a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) structure with information about the interfaces associated with the system.</span></span>

<span data-ttu-id="6818b-105">**Использование Жетинтерфацеинфо**</span><span class="sxs-lookup"><span data-stu-id="6818b-105">**To use GetInterfaceInfo**</span></span>

1.  <span data-ttu-id="6818b-106">Объявите указатель на объект [**\_ \_ сведений об интерфейсе IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) с именем `pInfo` и объект **ulong** с именем `ulOutBufLen` .</span><span class="sxs-lookup"><span data-stu-id="6818b-106">Declare a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) object called `pInfo`, and a **ULONG** object called `ulOutBufLen`.</span></span> <span data-ttu-id="6818b-107">Также объявите объект **DWORD** с именем `dwRetVal` (используется для проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="6818b-107">Also declare a **DWORD** object called `dwRetVal` (used for error checking).</span></span>
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  <span data-ttu-id="6818b-108">Выделение памяти для структур.</span><span class="sxs-lookup"><span data-stu-id="6818b-108">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="6818b-109">Размер недостаточно `ulOutBufLen` для хранения информации.</span><span class="sxs-lookup"><span data-stu-id="6818b-109">The size of `ulOutBufLen` is not sufficient to hold the information.</span></span> <span data-ttu-id="6818b-110">См. следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="6818b-110">See the next step.</span></span>

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  <span data-ttu-id="6818b-111">Выполните начальный вызов [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) , чтобы получить размер, необходимый для `ulOutBufLen` переменной.</span><span class="sxs-lookup"><span data-stu-id="6818b-111">Make an initial call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) to get the size needed into the `ulOutBufLen` variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="6818b-112">Этот вызов функции должен завершиться ошибкой и использоваться, чтобы гарантировать, что `ulOutBufLen` переменная задает размер, достаточный для хранения всех данных, возвращаемых в `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="6818b-112">This call to the function is meant to fail, and is used to ensure that the `ulOutBufLen` variable specifies a size sufficient for holding all the information returned to `pInfo`.</span></span> <span data-ttu-id="6818b-113">Это общая модель программирования в модуле поддержки IP для структур данных и функций этого типа.</span><span class="sxs-lookup"><span data-stu-id="6818b-113">This is a common programming model in IP Helper for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  <span data-ttu-id="6818b-114">Создайте второй вызов [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) с общей проверкой ошибок и верните его значение в переменную **DWORD** `dwRetVal` (для более расширенной проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="6818b-114">Make a second call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) with general error checking and return its value to the **DWORD** variable `dwRetVal` (for more advanced error checking).</span></span>
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  <span data-ttu-id="6818b-115">Если вызов выполнен успешно, получите доступ к данным из `pInfo` структуры данных.</span><span class="sxs-lookup"><span data-stu-id="6818b-115">If the call was successful, access the data from the `pInfo` data structure.</span></span>

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
    > <span data-ttu-id="6818b-116">% WS в первой строке обозначает расширенную строку.</span><span class="sxs-lookup"><span data-stu-id="6818b-116">The %ws in the first line denotes a wide string.</span></span> <span data-ttu-id="6818b-117">Это используется потому, что атрибут **Name** структуры [**\_ \_ \_ карты индекса IP-адаптера**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` имеет значение типа **WCHAR**, которое представляет собой строку в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="6818b-117">This is used because the **Name** attribute of the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure `Adapter` is a **WCHAR**, which is a Unicode string.</span></span>

     

6.  <span data-ttu-id="6818b-118">Освободите память, выделенную для структуры *пинфо* .</span><span class="sxs-lookup"><span data-stu-id="6818b-118">Free any memory allocated for the *pInfo* structure.</span></span>
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

<span data-ttu-id="6818b-119">Следующий шаг: [Управление IP-адресами с помощью жетипаддртабле](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="6818b-119">Next Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

<span data-ttu-id="6818b-120">Предыдущий шаг: [Управление сетевыми адаптерами с помощью жетадаптерсинфо](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="6818b-120">Previous Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

 

 



