---
title: Управление IP-адресами с помощью Аддипаддресс, Делетеипаддресс
description: Функция Аддипаддресс добавляет указанный IPv4-адрес к указанному адаптеру.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683358"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a><span data-ttu-id="ea0fc-103">Управление IP-адресами с помощью Аддипаддресс, Делетеипаддресс</span><span class="sxs-lookup"><span data-stu-id="ea0fc-103">Manage IP addresses with AddIPAddress, DeleteIPAddress</span></span>

<span data-ttu-id="ea0fc-104">Функция [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) добавляет указанный IPv4-адрес к указанному адаптеру.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-104">The [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function adds the specified IPv4 address to the specified adapter.</span></span> <span data-ttu-id="ea0fc-105">Функция [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) удаляет указанный IPv4-адрес из указанного адаптера.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-105">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function deletes the specified IPv4 address from the specified adapter.</span></span> <span data-ttu-id="ea0fc-106">Эти функции можно использовать для добавления и удаления IPv4-адресов в сетевом адаптере.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-106">These functions can be used to add and delete IPv4 addresses to a network adapter.</span></span>

<span data-ttu-id="ea0fc-107">IPv4-адрес, добавленный функцией [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) , не является постоянным.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-107">An IPv4 address added by the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function is not persistent.</span></span> <span data-ttu-id="ea0fc-108">IPv4-адрес существует, только если существует объект адаптера.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-108">The IPv4 address exists only as long as the adapter object exists.</span></span> <span data-ttu-id="ea0fc-109">Перезагрузка компьютера приводит к уничтожению IPv4-адреса, как и вручную сброс сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-109">Restarting the computer destroys the IPv4 address, as does manually resetting the network interface card (NIC).</span></span>

<span data-ttu-id="ea0fc-110">После успешного вызова [**АДДИПАДДРЕСС**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) DHCP будет отключен для ДОБАВЛЕННОГО IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-110">After [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) has been called successfully, DHCP will be disabled for the IP address that was added.</span></span> <span data-ttu-id="ea0fc-111">Таким образом, такие функции, как [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), требующие включения DHCP, не будут работать на ДОБАВЛЕННОМ IP-адресе.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-111">Therefore, functions such as [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), which require DHCP to be enabled, will not be functional on the added IP address.</span></span> <span data-ttu-id="ea0fc-112">Для удаления добавленного IPv4-адреса можно использовать функцию [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .</span><span class="sxs-lookup"><span data-stu-id="ea0fc-112">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function can be used to delete the added IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="ea0fc-113">Групповые политики, политики предприятия и другие ограничения сети могут препятствовать успешному завершению этих функций.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-113">Group policies, enterprise policies, and other restrictions on the network may prevent these functions from completing successfully.</span></span> <span data-ttu-id="ea0fc-114">Прежде чем пытаться использовать эти функции, убедитесь, что приложение имеет необходимые сетевые разрешения.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-114">Ensure that the application has the necessary network permissions before attempting to use these functions.</span></span>

 

<span data-ttu-id="ea0fc-115">**Использование Аддипаддресс**</span><span class="sxs-lookup"><span data-stu-id="ea0fc-115">**To use AddIPAddress**</span></span>

1.  <span data-ttu-id="ea0fc-116">Объявите переменные **ulong** с именами `NTEContext` и `NTEInstance` , инициализируются нулем.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-116">Declare **ULONG** variables named `NTEContext` and `NTEInstance`, both initialized to zero.</span></span>
    > [!Note]  
    > <span data-ttu-id="ea0fc-117">`NTEContext`Переменная является единственным параметром функции [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) . чтобы удалить добавленный IP-адрес, он `NTEContext` должен быть сохранен и не изменен.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-117">The `NTEContext` variable is the only parameter to the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function; to delete the IP address that is added, `NTEContext` must be stored and unchanged.</span></span>

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  <span data-ttu-id="ea0fc-118">Объявите переменные для структур reduce и Ипмаск с именами `iaIPAddress` и `iaIPMask` соответственно.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-118">Declare variables for the IPAddr and IPMask structures named `iaIPAddress` and `iaIPMask`, respectively.</span></span> <span data-ttu-id="ea0fc-119">Эти значения представляют собой целые числа без знака.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-119">These values are simply unsigned integers.</span></span> <span data-ttu-id="ea0fc-120">Инициализируйте `iaIPAddress` `iaIPMask` переменные и с помощью функции [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) .</span><span class="sxs-lookup"><span data-stu-id="ea0fc-120">Initialize the `iaIPAddress` and `iaIPMask` variables using the [**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) function.</span></span>
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  <span data-ttu-id="ea0fc-121">Чтобы добавить IPv4-адрес, вызовите функцию [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) .</span><span class="sxs-lookup"><span data-stu-id="ea0fc-121">Call the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add the IPv4 address.</span></span> <span data-ttu-id="ea0fc-122">Проверьте наличие ошибок и верните значение ошибки в переменную **DWORD** `dwRetVal` (для более обширной проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="ea0fc-122">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > <span data-ttu-id="ea0fc-123">Третий параметр — это индекс адаптера, который можно получить, вызвав функцию [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) .</span><span class="sxs-lookup"><span data-stu-id="ea0fc-123">The third parameter is the adapter index, which can be obtained by calling the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="ea0fc-124">Предполагается, что переменная, возвращаемая этой функцией, называется `pIPAddrTable` .</span><span class="sxs-lookup"><span data-stu-id="ea0fc-124">It is assumed that the variable returned by this function is named `pIPAddrTable`.</span></span> <span data-ttu-id="ea0fc-125">Справку по функции **жетипаддртабле** см. в разделе [Управление IP-адресами с помощью жетипаддртабле](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="ea0fc-125">For help with the **GetIpAddrTable** function, see [Managing IP Address Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

     

<span data-ttu-id="ea0fc-126">**Использование Делетеипаддресс**</span><span class="sxs-lookup"><span data-stu-id="ea0fc-126">**To use DeleteIpAddress**</span></span>

-   <span data-ttu-id="ea0fc-127">Вызовите функцию [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) , передав `NTEContext` переменную в качестве ее параметра.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-127">Call the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function, passing the `NTEContext` variable as its parameter.</span></span> <span data-ttu-id="ea0fc-128">Проверьте наличие ошибок и верните значение ошибки в переменную **DWORD** `dwRetVal` (для более обширной проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="ea0fc-128">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> <span data-ttu-id="ea0fc-129">Чтобы использовать [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), необходимо сначала вызвать [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) для получения маркера `NTEContext` .</span><span class="sxs-lookup"><span data-stu-id="ea0fc-129">To use [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) must first be called to get the handle `NTEContext`.</span></span> <span data-ttu-id="ea0fc-130">В предыдущей процедуре предполагается, что **аддипаддресс** уже вызван где-то в коде и `NTEContext` сохранен и остается неповрежденным.</span><span class="sxs-lookup"><span data-stu-id="ea0fc-130">The previous procedure assumes that **AddIPAddress** has already been called somewhere in the code, and `NTEContext` has been saved and remains uncorrupted.</span></span>

 

<span data-ttu-id="ea0fc-131">Следующий шаг: [Получение сведений с помощью жетипстатистикс](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="ea0fc-131">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="ea0fc-132">Предыдущий шаг: [Управление арендой DHCP с помощью ипрелеасеаддресс и ипреневаддресс](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="ea0fc-132">Previous Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

 

 
