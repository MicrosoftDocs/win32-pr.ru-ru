---
description: Функция Жетипаддртабле заполняет указатель на \_ структуру MIB ипаддртабле, используя сведения о текущих IP-адресах, связанных с системой.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Управление IP-адресами с помощью Жетипаддртабле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3d94eb4de22a428e20a4cb0fdc8970d7f65fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909492"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a><span data-ttu-id="81658-103">Управление IP-адресами с помощью Жетипаддртабле</span><span class="sxs-lookup"><span data-stu-id="81658-103">Managing IP Addresses Using GetIpAddrTable</span></span>

<span data-ttu-id="81658-104">Функция [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) заполняет указатель на структуру [**MIB \_ ипаддртабле**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) , используя сведения о текущих IP-адресах, связанных с системой.</span><span class="sxs-lookup"><span data-stu-id="81658-104">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function fills a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) structure with information about the current IP addresses associated with the system.</span></span>

<span data-ttu-id="81658-105">**Использование Жетипаддртабле**</span><span class="sxs-lookup"><span data-stu-id="81658-105">**To use GetIpAddrTable**</span></span>

1.  <span data-ttu-id="81658-106">Объявите указатель на объект [**MIB \_ ипаддртабле**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) , именуемый *Пипаддртабле*, и объект **DWORD** с именем *двсизе*.</span><span class="sxs-lookup"><span data-stu-id="81658-106">Declare a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) object called *pIPAddrTable*, and a **DWORD** object called *dwSize*.</span></span> <span data-ttu-id="81658-107">Эти переменные передаются в качестве параметров функции [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) .</span><span class="sxs-lookup"><span data-stu-id="81658-107">These variables are passed as parameters to the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="81658-108">Также создайте переменную **типа DWORD** с именем *двретвал* (используется для проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="81658-108">Also create a **DWORD** variable called *dwRetVal* (used for error checking).</span></span>
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="81658-109">Выделение памяти для структуры.</span><span class="sxs-lookup"><span data-stu-id="81658-109">Allocate memory for the structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="81658-110">Размер *двсизе* недостаточно для хранения информации.</span><span class="sxs-lookup"><span data-stu-id="81658-110">The size of *dwSize* is not sufficient to hold the information.</span></span> <span data-ttu-id="81658-111">См. следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="81658-111">See the next step.</span></span>

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  <span data-ttu-id="81658-112">Выполните начальный вызов [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , чтобы получить размер, необходимый для переменной *двсизе* .</span><span class="sxs-lookup"><span data-stu-id="81658-112">Make an initial call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) to get the size needed into the *dwSize* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="81658-113">Этот вызов функции завершается ошибкой и используется, чтобы гарантировать, что переменная *двсизе* задает размер, достаточный для хранения всей информации, возвращенной в *пипаддртабле*.</span><span class="sxs-lookup"><span data-stu-id="81658-113">This call to the function is meant to fail, and is used to ensure that the *dwSize* variable specifies a size sufficient for holding all the information returned to *pIPAddrTable*.</span></span> <span data-ttu-id="81658-114">Это общая модель программирования для структур данных и функций этого типа.</span><span class="sxs-lookup"><span data-stu-id="81658-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  <span data-ttu-id="81658-115">Создайте второй вызов [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) с общей проверкой ошибок и верните его значение в переменную **DWORD** *двретвал* (для более расширенной проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="81658-115">Make a second call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) with general error checking and return its value to the **DWORD** variable *dwRetVal* (for more advanced error checking).</span></span>
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  <span data-ttu-id="81658-116">Если вызов выполнен успешно, получите доступ к данным из структуры данных *пипаддртабле* .</span><span class="sxs-lookup"><span data-stu-id="81658-116">If the call was successful, access the data from the *pIPAddrTable* data structure.</span></span>
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  <span data-ttu-id="81658-117">Освободите память, выделенную для структуры *пипаддртабле* .</span><span class="sxs-lookup"><span data-stu-id="81658-117">Free any memory allocated for the *pIPAddrTable* structure.</span></span>
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> <span data-ttu-id="81658-118">Объекты **DWORD** *дваддр* и *двмаск* возвращаются в виде числовых значений в порядке байтов узла, а не в сетевом порядке байтов.</span><span class="sxs-lookup"><span data-stu-id="81658-118">The **DWORD** objects *dwAddr* and *dwMask* are returned as numerical values in host byte order, not network byte order.</span></span> <span data-ttu-id="81658-119">Эти значения не являются точками IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="81658-119">These values are not dotted IP addresses.</span></span>

 

<span data-ttu-id="81658-120">Следующий шаг: [Управление арендой DHCP с помощью ипрелеасеаддресс и ипреневаддресс](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="81658-120">Next Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

<span data-ttu-id="81658-121">Предыдущий шаг: [Управление интерфейсами с помощью жетинтерфацеинфо](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="81658-121">Previous Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

 

 
