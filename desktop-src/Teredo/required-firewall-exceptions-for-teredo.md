---
title: Требуемые исключения брандмауэра для Teredo
description: Чтобы приложение получало трафик Teredo, приложению должно быть разрешено получать трафик IPv6 в брандмауэре узла, а приложению требуется установить для параметра сокета защиты IPV6 значение \_ \_ " \_ \_ Неограниченный уровень защиты".
ms.assetid: 2fc74d86-9696-4ba9-adbe-e5558ae7d7c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbc2fcf0f7c8b1f5fe51afc056dc8c8ff7c7916a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681682"
---
# <a name="required-firewall-exceptions-for-teredo"></a><span data-ttu-id="3f73c-103">Требуемые исключения брандмауэра для Teredo</span><span class="sxs-lookup"><span data-stu-id="3f73c-103">Required Firewall Exceptions for Teredo</span></span>

<span data-ttu-id="3f73c-104">Чтобы приложение получало трафик Teredo, приложению должно быть разрешено получать трафик IPv6 в брандмауэре узла, а приложению требуется установить для параметра сокета [ \_ защиты \_ IPv6](/windows/desktop/WinSock/ipv6-protection-level) значение " \_ \_ Неограниченный уровень защиты".</span><span class="sxs-lookup"><span data-stu-id="3f73c-104">For an application to receive Teredo traffic, the application must be permitted to receive IPv6 traffic in the host firewall, and the application is required to set the socket option [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) to 'PROTECTION\_LEVEL\_UNRESTRICTED'.</span></span> <span data-ttu-id="3f73c-105">Чтобы включить этот тип сценария, необходимо реализовать исключения брандмауэра, описанные в этом документе.</span><span class="sxs-lookup"><span data-stu-id="3f73c-105">To enable this type of scenario, the firewall exceptions detailed in this document must be implemented.</span></span>

<span data-ttu-id="3f73c-106">Для обеспечения беспрепятственной взаимодействия между брандмауэром и Teredo необходимы следующие конфигурации брандмауэра:</span><span class="sxs-lookup"><span data-stu-id="3f73c-106">The following firewall configurations are required to ensure smooth interoperation between a firewall and Teredo:</span></span>

-   <span data-ttu-id="3f73c-107">Брандмауэр клиента должен разрешать разрешение teredo.ipv6.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="3f73c-107">The client firewall must allow resolution of teredo.ipv6.microsoft.com.</span></span>
-   <span data-ttu-id="3f73c-108">Чтобы клиенты Teredo могли успешно взаимодействовать с сервером Teredo, необходимо открыть UDP-порт 3544.</span><span class="sxs-lookup"><span data-stu-id="3f73c-108">UDP Port 3544 must be open to ensure that Teredo clients can successfully communicate with the Teredo server.</span></span>
-   <span data-ttu-id="3f73c-109">Брандмауэр должен получить динамические UDP-порты, используемые службой Teredo на локальном компьютере, вызвав функцию [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) . соответствующие порты имеют тип ФВПМ \_ системный \_ порт \_ TEREDO.</span><span class="sxs-lookup"><span data-stu-id="3f73c-109">The firewall must retrieve dynamic UDP ports used by Teredo service on the local machine by calling the [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) function; relevant ports are of type FWPM\_SYSTEM\_PORT\_TEREDO.</span></span> <span data-ttu-id="3f73c-110">Функция **FwpmSystemPortsGet0** должна быть реализована вместо устаревших функций [**жеттередопорт**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) или [**нотифитередопортчанже**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) .</span><span class="sxs-lookup"><span data-stu-id="3f73c-110">The **FwpmSystemPortsGet0** function should be implemented in place of the now deprecated [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) or [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) functions.</span></span>
-   <span data-ttu-id="3f73c-111">Брандмауэр позволяет системе отправлять и получать пакеты UDP/IPv4 на UDP-порт 1900 в локальной подсети, так как это позволяет подавать трафик обнаружения UPnP и может повысить скорость подключения.</span><span class="sxs-lookup"><span data-stu-id="3f73c-111">The firewall permits the system to send and receive UDP/IPv4 packets to UDP port 1900 on the local subnet as this allows UPnP discovery traffic to flow and has the potential to improve connectivity rates.</span></span>
    > [!Note]  
    > <span data-ttu-id="3f73c-112">Если это условие не выполняется, то возможны ситуации, когда возникают проблемы совместимости, связанные с взаимодействием между определенными типами NAT. в частности, между симметричным NAT и ограниченным NAT.</span><span class="sxs-lookup"><span data-stu-id="3f73c-112">If this condition is not met, the potential for scenarios to encounter compatibility issues involving communication between certain NAT types is introduced; specifically between Symmetric NATs and Restricted NATs.</span></span> <span data-ttu-id="3f73c-113">Хотя симметричное преобразование сетевых адресов (NAT) широко распространено в общественных точках, а в жилых подключениях широко используются ограниченные устройства NAT, взаимодействие между ними может привести к сбою на стороне ограниченного NAT.</span><span class="sxs-lookup"><span data-stu-id="3f73c-113">While Symmetric NATs are popular in hotspots and Restricted NATs are popular in homes, communication between the two has the potential to fault on the side of the Restricted NAT.</span></span>

     

-   <span data-ttu-id="3f73c-114">Должны быть включены входящие и исходящие ICMPv6 "эхо-запросы" и "Эхо-ответ".</span><span class="sxs-lookup"><span data-stu-id="3f73c-114">Incoming and outgoing ICMPv6 "Echo Request" and "Echo Reply" exceptions must be enabled.</span></span> <span data-ttu-id="3f73c-115">Эти исключения необходимы для того, чтобы клиент Teredo мог действовать в качестве ретранслятора для конкретного узла Teredo.</span><span class="sxs-lookup"><span data-stu-id="3f73c-115">These exceptions are necessary to ensure that a Teredo client can act as a Teredo host-specific relay.</span></span> <span data-ttu-id="3f73c-116">Ретранслятор, относящийся к конкретному узлу Teredo, может идентифицироваться по дополнительному собственному IPv6-адресу или адресу 6to4, указанному с помощью адреса Teredo.</span><span class="sxs-lookup"><span data-stu-id="3f73c-116">A Teredo host-specific relay can be identified by the additional native IPv6 address or a 6to4 address supplied with the Teredo address.</span></span>

<span data-ttu-id="3f73c-117">Клиентские брандмауэры должны поддерживать следующие сообщения об ошибках ICMPv6 и функции обнаружения на RFC 4443:</span><span class="sxs-lookup"><span data-stu-id="3f73c-117">Client firewalls must support the following ICMPv6 error messages and discovery functions per RFC 4443:</span></span>



| <span data-ttu-id="3f73c-118">Код</span><span class="sxs-lookup"><span data-stu-id="3f73c-118">Code</span></span>    | <span data-ttu-id="3f73c-119">Описание</span><span class="sxs-lookup"><span data-stu-id="3f73c-119">Description</span></span>                                    |
|---------|------------------------------------------------|
| <span data-ttu-id="3f73c-120">135/136</span><span class="sxs-lookup"><span data-stu-id="3f73c-120">135/136</span></span> | <span data-ttu-id="3f73c-121">Запрос на соседок ICMPV6 и объявление</span><span class="sxs-lookup"><span data-stu-id="3f73c-121">ICMPV6 Neighbor Solicitation and Advertisement</span></span> |
| <span data-ttu-id="3f73c-122">133/134</span><span class="sxs-lookup"><span data-stu-id="3f73c-122">133/134</span></span> | <span data-ttu-id="3f73c-123">Запрос маршрутизатора и объявление</span><span class="sxs-lookup"><span data-stu-id="3f73c-123">Router Solicitation and Advertisement</span></span>          |
| <span data-ttu-id="3f73c-124">128/129</span><span class="sxs-lookup"><span data-stu-id="3f73c-124">128/129</span></span> | <span data-ttu-id="3f73c-125">Эхо-запрос и ответ ICMPV6</span><span class="sxs-lookup"><span data-stu-id="3f73c-125">ICMPV6 Echo Request and Reply</span></span>                  |
| <span data-ttu-id="3f73c-126">1</span><span class="sxs-lookup"><span data-stu-id="3f73c-126">1</span></span>       | <span data-ttu-id="3f73c-127">Объект назначения недоступен</span><span class="sxs-lookup"><span data-stu-id="3f73c-127">Destination Unreachable</span></span>                        |
| <span data-ttu-id="3f73c-128">2</span><span class="sxs-lookup"><span data-stu-id="3f73c-128">2</span></span>       | <span data-ttu-id="3f73c-129">Пакет слишком велик</span><span class="sxs-lookup"><span data-stu-id="3f73c-129">Packet Too Large</span></span>                               |
| <span data-ttu-id="3f73c-130">3</span><span class="sxs-lookup"><span data-stu-id="3f73c-130">3</span></span>       | <span data-ttu-id="3f73c-131">Превышение времени</span><span class="sxs-lookup"><span data-stu-id="3f73c-131">Time Exceeded</span></span>                                  |
| <span data-ttu-id="3f73c-132">4</span><span class="sxs-lookup"><span data-stu-id="3f73c-132">4</span></span>       | <span data-ttu-id="3f73c-133">Недопустимый параметр</span><span class="sxs-lookup"><span data-stu-id="3f73c-133">Invalid Parameter</span></span>                              |



 

<span data-ttu-id="3f73c-134">Если эти сообщения не могут быть разрешены специально, то исключение всех сообщений ICMPv6 должно быть включено в брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="3f73c-134">If these messages cannot be specifically allowed, then the exemption of all ICMPv6 messages should be enabled on the firewall.</span></span> <span data-ttu-id="3f73c-135">Кроме того, брандмауэр узла может заметить, что пакеты, классифицированные кодами 135/136 или 133/134, исходят от или предназначены для службы пользовательского режима **IpHlpSvc** , а не из стека.</span><span class="sxs-lookup"><span data-stu-id="3f73c-135">Additionally, the host firewall may notice that the packets classified by codes 135/136 or 133/134 originate from, or are targeted to, the user mode service **iphlpsvc** and not from the stack.</span></span> <span data-ttu-id="3f73c-136">Эти пакеты не должны удаляться брандмауэром узла.</span><span class="sxs-lookup"><span data-stu-id="3f73c-136">These packets must not be dropped by the host firewall.</span></span> <span data-ttu-id="3f73c-137">Служба Teredo реализована в основном в службе поддержки IP в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="3f73c-137">The Teredo service is implemented primarily within the 'user mode' IP Helper service.</span></span>

<span data-ttu-id="3f73c-138">С помощью API брандмауэра Windows [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) для перечисления всех правил с установленным флагом обхода ребра все приложения, которые хотят прослушивать незапрошенный трафик, перечисляются для исключения брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="3f73c-138">Using the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) Windows Firewall API to enumerate all rules with the Edge Traversal flag set, all applications that want to listen for unsolicited traffic are enumerated for the firewall exception.</span></span> <span data-ttu-id="3f73c-139">Конкретные сведения об использовании параметра обхода узлов [см. в](receiving-unsolicited-traffic-over-teredo.md)этой статьи.</span><span class="sxs-lookup"><span data-stu-id="3f73c-139">Specific information regarding the use of the Edge Traversal option is detailed in [Receiving Unsolicited Traffic Over Teredo](receiving-unsolicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="3f73c-140">Обратные вызовы не связаны со следующим образцом кода перечисления. настоятельно рекомендуется периодически выполнять перечисление с помощью брандмауэров сторонних производителей или при обнаружении брандмауэром нового приложения, пытающегося пройти через брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="3f73c-140">Callbacks are not associated with the following sample enumeration code; it is strongly recommended that third party firewalls perform the enumeration periodically, or whenever the firewall detects a new application attempting to go through the firewall.</span></span>


```C++
#include <windows.h>
#include <objbase.h>
#include <stdio.h>
#include <atlcomcli.h>
#include <strsafe.h>
#include <netfw.h>

#define NET_FW_IP_PROTOCOL_TCP_NAME L"TCP"
#define NET_FW_IP_PROTOCOL_UDP_NAME L"UDP"

#define NET_FW_RULE_DIR_IN_NAME L"In"
#define NET_FW_RULE_DIR_OUT_NAME L"Out"

#define NET_FW_RULE_ACTION_BLOCK_NAME L"Block"
#define NET_FW_RULE_ACTION_ALLOW_NAME L"Allow"

#define NET_FW_RULE_ENABLE_IN_NAME L"TRUE"
#define NET_FW_RULE_DISABLE_IN_NAME L"FALSE"

#import "netfw.tlb"

void DumpFWRulesInCollection(long Allprofiletypes, NetFwPublicTypeLib::INetFwRulePtr FwRule)
{
    variant_t InterfaceArray;
    variant_t InterfaceString;    

    if(FwRule->Profiles == Allprofiletypes)
    {
        wprintf(L"---------------------------------------------\n");
        wprintf(L"Name:             %s\n", (BSTR)FwRule->Name);        
        wprintf(L"Description:      %s\n", (BSTR)FwRule->Description);
        wprintf(L"Application Name: %s\n", (BSTR)FwRule->ApplicationName);
        wprintf(L"Service Name:     %s\n", (BSTR)FwRule->serviceName);

        switch(FwRule->Protocol)
        {
        case NET_FW_IP_PROTOCOL_TCP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_TCP_NAME);
            break;
        case NET_FW_IP_PROTOCOL_UDP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_UDP_NAME);
            break;
        default:
            break;
        }

        if(FwRule->Protocol != NET_FW_IP_VERSION_V4 && FwRule->Protocol != NET_FW_IP_VERSION_V6)
        {
            wprintf(L"Local Ports:      %s\n", (BSTR)FwRule->LocalPorts);
            wprintf(L"Remote Ports:     %s\n", (BSTR)FwRule->RemotePorts);
        }
        
        wprintf(L"LocalAddresses:   %s\n", (BSTR)FwRule->LocalAddresses);
        wprintf(L"RemoteAddresses:  %s\n", (BSTR)FwRule->RemoteAddresses);
        wprintf(L"Profile:          %d\n", Allprofiletypes);
        

        if(FwRule->Protocol == NET_FW_IP_VERSION_V4 || FwRule->Protocol == NET_FW_IP_VERSION_V6)
        {
            wprintf(L"ICMP TypeCode:    %s\n", (BSTR)FwRule->IcmpTypesAndCodes);
        }

        switch(FwRule->Direction)
        {
        case NET_FW_RULE_DIR_IN:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_IN_NAME);
            break;
        case NET_FW_RULE_DIR_OUT:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_OUT_NAME);
            break;
        default:
            break;
        }

        switch(FwRule->Action)
        {
        case NET_FW_ACTION_BLOCK:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_BLOCK_NAME);
            break;
        case NET_FW_ACTION_ALLOW:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_ALLOW_NAME);
            break;
        default:
            break;
        }
        
        InterfaceArray = FwRule->Interfaces;

        if(InterfaceArray.vt != VT_EMPTY)
        {
            SAFEARRAY    *pSa = NULL;
            long index = 0;

            pSa = InterfaceArray.parray;

            for(long index= pSa->rgsabound->lLbound; index < (long)pSa->rgsabound->cElements; index++)
            {
                SafeArrayGetElement(pSa, &index, &InterfaceString);
                wprintf(L"Interfaces:       %s\n", (BSTR)InterfaceString.bstrVal);
            }
        }
        wprintf(L"Interface Types:  %s\n", (BSTR)FwRule->InterfaceTypes);
        if(FwRule->Enabled)
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_ENABLE_IN_NAME);
        }
        else
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_DISABLE_IN_NAME);
        }
        wprintf(L"Grouping:         %s\n", (BSTR)FwRule->Grouping);
        wprintf(L"Edge:             %s\n", (BSTR)FwRule->EdgeTraversal);
    }
}

int __cdecl main()
{
    HRESULT hr;
    BOOL fComInitialized = FALSE;
    ULONG cFetched = 0; 
    CComVariant var;
    long Allprofiletypes = 0;

    try
    {
        IUnknownPtr pEnumerator = NULL;
        IEnumVARIANT* pVariant = NULL;
        NetFwPublicTypeLib::INetFwPolicy2Ptr sipFwPolicy2;

        //
        // Initialize the COM library on the current thread.
        //
        hr = CoInitialize(NULL);
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        fComInitialized = TRUE;
        
        hr = sipFwPolicy2.CreateInstance("HNetCfg.FwPolicy2");
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        Allprofiletypes = NET_FW_PROFILE2_ALL; // 0x7FFFFFFF
        
        printf("The number of rules in the Windows Firewall are %d\n", sipFwPolicy2->Rules->Count);

        pEnumerator = sipFwPolicy2->Rules->Get_NewEnum();

        if(pEnumerator)
        {
            hr = pEnumerator->QueryInterface(__uuidof(IEnumVARIANT), (void **) &pVariant);
        }

        while(SUCCEEDED(hr) && hr != S_FALSE)
        {        
            NetFwPublicTypeLib::INetFwRulePtr sipFwRule;

            var.Clear();
            hr = pVariant->Next(1, &var, &cFetched);
            if (S_FALSE != hr)
            {
                if (SUCCEEDED(hr))
                {
                    hr = var.ChangeType(VT_DISPATCH);
                }
                if (SUCCEEDED(hr))
                {
                    hr = (V_DISPATCH(&var))->QueryInterface(__uuidof(INetFwRule), reinterpret_cast<void**>(&sipFwRule));
                }

                if (SUCCEEDED(hr))
                {
                    DumpFWRulesInCollection(Allprofiletypes, sipFwRule);
                }
            }
        }
    }
    catch(_com_error& e)
    {
        printf ("Error. HRESULT message is: %s (0x%08lx)\n", e.ErrorMessage(), e.Error());
        if (e.ErrorInfo())
        {
            printf ("Description: %s\n", (char *)e.Description());
        }
    }
    if (fComInitialized)
    {
        CoUninitialize();
    }
    return 0;
}

```



 

 