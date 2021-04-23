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
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a><span data-ttu-id="a7c20-103">Управление арендой DHCP с помощью Ипрелеасеаддресс, Ипреневаддресс</span><span class="sxs-lookup"><span data-stu-id="a7c20-103">Manage DHCP leases with IpReleaseAddress, IpRenewAddress</span></span>

<span data-ttu-id="a7c20-104">Функции [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) и [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) используются для освобождения и продления текущей аренды протокола динамической настройки узла (DHCP).</span><span class="sxs-lookup"><span data-stu-id="a7c20-104">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions are used to release and renew the current Dynamic Host Configuration Protocol (DHCP) lease.</span></span> <span data-ttu-id="a7c20-105">Функция **ипрелеасеаддресс** освобождает IPv4-адрес, который ранее был получен с помощью DHCP.</span><span class="sxs-lookup"><span data-stu-id="a7c20-105">The **IpReleaseAddress** function releases an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="a7c20-106">Функция **ипреневаддресс** обновляет аренду на IPv4-адресе, ранее полученном с помощью DHCP.</span><span class="sxs-lookup"><span data-stu-id="a7c20-106">The **IpRenewAddress** function renews a lease on an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="a7c20-107">Обычно эти две функции используются совместно, сначала освобождайте аренду вызовом **ипрелеасеаддресс**, а затем продлите аренду, вызвав функцию **ипреневаддресс** .</span><span class="sxs-lookup"><span data-stu-id="a7c20-107">It is common to use these two functions together, first releasing the lease with a call to **IpReleaseAddress**, and then renewing the lease with a call to the **IpRenewAddress** function.</span></span>

<span data-ttu-id="a7c20-108">Когда DHCP-клиент ранее получил аренду DHCP и [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) не вызывается до функции [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , запрос DHCP-клиента отправляется на DHCP-сервер, ВЫДАВШИЙ начальную аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="a7c20-108">When a DHCP client has previously obtained a DHCP lease and [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) is not called before the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, the DHCP client request is sent to the DHCP server that issued the initial DHCP lease.</span></span> <span data-ttu-id="a7c20-109">Возможно, этот DHCP-сервер недоступен, или DHCP-запрос может завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a7c20-109">This DHCP server may not available or the DHCP request may fail.</span></span> <span data-ttu-id="a7c20-110">Когда узел ранее получил аренду DHCP и **ипрелеасеаддресс** вызывается перед функцией **ипреневаддресс** , DHCP-клиент сначала освобождает полученный IP-адрес и отправляет запрос DHCP-клиента на ответ от любого доступного DHCP-сервера.</span><span class="sxs-lookup"><span data-stu-id="a7c20-110">When a host has previously obtained a DHCP lease and **IpReleaseAddress** is called before the **IpRenewAddress** function, the DHCP client first releases the IP address obtained and sends a DHCP client request for a response from any available DHCP server.</span></span>

> [!Note]  
> <span data-ttu-id="a7c20-111">Для выполнения функций [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) и [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) требуется, чтобы DHCP был включен правильно.</span><span class="sxs-lookup"><span data-stu-id="a7c20-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require that DHCP be enabled to perform correctly.</span></span>

 

<span data-ttu-id="a7c20-112">Функция [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) принимает указатель на структуру [**\_ \_ \_ карты индекса адаптера IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) в качестве единственного параметра.</span><span class="sxs-lookup"><span data-stu-id="a7c20-112">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function takes a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure as its only parameter.</span></span> <span data-ttu-id="a7c20-113">Чтобы получить этот параметр, сначала вызовите [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span><span class="sxs-lookup"><span data-stu-id="a7c20-113">To obtain this parameter, first call [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span></span> <span data-ttu-id="a7c20-114">Справку по функции **жетинтерфацеинфо** см. в разделе [Управление интерфейсами с помощью жетинтерфацеинфо](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="a7c20-114">For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="a7c20-115">**Использование Ипрелеасеаддресс**</span><span class="sxs-lookup"><span data-stu-id="a7c20-115">**To use IpReleaseAddress**</span></span>

1.  <span data-ttu-id="a7c20-116">Получите указатель на структуру [**\_ \_ \_ карты индекса адаптера IP-адресов**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) с помощью функции [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) .</span><span class="sxs-lookup"><span data-stu-id="a7c20-116">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="a7c20-117">(Дополнительные сведения о функции Жетинтерфацеинфо см. в разделе [Управление интерфейсами с помощью жетинтерфацеинфо](managing-interfaces-using-getinterfaceinfo.md)).</span><span class="sxs-lookup"><span data-stu-id="a7c20-117">(For help with the GetInterfaceInfo function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="a7c20-118">Создайте объект **типа DWORD** `dwRetVal` (используется для проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="a7c20-118">Create a **DWORD** object `dwRetVal` (used for error checking).</span></span> <span data-ttu-id="a7c20-119">Предполагается, что переменная, возвращаемая функцией **жетинтерфацеинфо** , называется `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="a7c20-119">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="a7c20-120">Если DHCP включен, вызовите функцию [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) , передав переменную [**\_ \_ \_ карты индекса IP-адаптера**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) в `Adapter` качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="a7c20-120">If DHCP is enabled, call the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="a7c20-121">Проверьте наличие общих ошибок и верните его значение переменной **DWORD** `dwRetVal` (для более обширной проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="a7c20-121">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    > [!Note]  
    > <span data-ttu-id="a7c20-122">Функция [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) возвращает параметр, который можно использовать для проверки того, включен ли протокол DHCP перед вызовом этих функций.</span><span class="sxs-lookup"><span data-stu-id="a7c20-122">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns a parameter that can be used to check whether DHCP is enabled before calling these functions.</span></span> <span data-ttu-id="a7c20-123">Справку по **жетадаптерсинфо** см. в разделе [Управление сетевыми адаптерами с помощью жетадаптерсинфо](managing-network-adapters-using-getadaptersinfo.md).</span><span class="sxs-lookup"><span data-stu-id="a7c20-123">For help with **GetAdaptersInfo**, see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> <span data-ttu-id="a7c20-124">Обычно эти две функции используются совместно, вызывая функцию [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) и вызывая функцию [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , передавая ту же структуру, что и параметр, в обе функции.</span><span class="sxs-lookup"><span data-stu-id="a7c20-124">It is common to use these two functions together, calling the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function and then calling the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the same structure as the parameter to both functions.</span></span> <span data-ttu-id="a7c20-125">В следующей процедуре предполагается, что функции не используются вместе. Однако если функции используются совместно, пропустите шаг 1.</span><span class="sxs-lookup"><span data-stu-id="a7c20-125">The following procedure assumes that the functions are not used together; however, if the functions are used together, skip step 1.</span></span>

 

<span data-ttu-id="a7c20-126">**Использование Ипреневаддресс**</span><span class="sxs-lookup"><span data-stu-id="a7c20-126">**To use IpRenewAddress**</span></span>

1.  <span data-ttu-id="a7c20-127">Получите указатель на структуру [**\_ \_ \_ карты индекса адаптера IP-адресов**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) с помощью функции [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) .</span><span class="sxs-lookup"><span data-stu-id="a7c20-127">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="a7c20-128">(Дополнительные сведения о функции **жетинтерфацеинфо** см. в разделе [Управление интерфейсами с помощью жетинтерфацеинфо](managing-interfaces-using-getinterfaceinfo.md)).</span><span class="sxs-lookup"><span data-stu-id="a7c20-128">(For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="a7c20-129">Объявите  объект DWORD `dwRetVal` (используемый для проверки ошибок), если эта переменная не была объявлена.</span><span class="sxs-lookup"><span data-stu-id="a7c20-129">Declare a **DWORD** object `dwRetVal` (used for error checking) if this variable has not been declared.</span></span> <span data-ttu-id="a7c20-130">Предполагается, что переменная, возвращаемая функцией **жетинтерфацеинфо** , называется `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="a7c20-130">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="a7c20-131">Вызовите функцию [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , передав в качестве параметра переменную [**\_ \_ \_ карты индекса IP-адаптера**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` .</span><span class="sxs-lookup"><span data-stu-id="a7c20-131">Call the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="a7c20-132">Проверьте наличие общих ошибок и верните его значение переменной **DWORD** `dwRetVal` (для более обширной проверки ошибок).</span><span class="sxs-lookup"><span data-stu-id="a7c20-132">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

<span data-ttu-id="a7c20-133">Следующий шаг: [Управление IP-адресами с помощью аддипаддресс и делетеипаддресс](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="a7c20-133">Next Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

<span data-ttu-id="a7c20-134">Предыдущий шаг: [Управление IP-адресами с помощью жетипаддртабле](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="a7c20-134">Previous Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

 

 



