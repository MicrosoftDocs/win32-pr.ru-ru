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
# <a name="required-firewall-exceptions-for-teredo"></a>Требуемые исключения брандмауэра для Teredo

Чтобы приложение получало трафик Teredo, приложению должно быть разрешено получать трафик IPv6 в брандмауэре узла, а приложению требуется установить для параметра сокета [ \_ защиты \_ IPv6](/windows/desktop/WinSock/ipv6-protection-level) значение " \_ \_ Неограниченный уровень защиты". Чтобы включить этот тип сценария, необходимо реализовать исключения брандмауэра, описанные в этом документе.

Для обеспечения беспрепятственной взаимодействия между брандмауэром и Teredo необходимы следующие конфигурации брандмауэра:

-   Брандмауэр клиента должен разрешать разрешение teredo.ipv6.microsoft.com.
-   Чтобы клиенты Teredo могли успешно взаимодействовать с сервером Teredo, необходимо открыть UDP-порт 3544.
-   Брандмауэр должен получить динамические UDP-порты, используемые службой Teredo на локальном компьютере, вызвав функцию [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) . соответствующие порты имеют тип ФВПМ \_ системный \_ порт \_ TEREDO. Функция **FwpmSystemPortsGet0** должна быть реализована вместо устаревших функций [**жеттередопорт**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) или [**нотифитередопортчанже**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) .
-   Брандмауэр позволяет системе отправлять и получать пакеты UDP/IPv4 на UDP-порт 1900 в локальной подсети, так как это позволяет подавать трафик обнаружения UPnP и может повысить скорость подключения.
    > [!Note]  
    > Если это условие не выполняется, то возможны ситуации, когда возникают проблемы совместимости, связанные с взаимодействием между определенными типами NAT. в частности, между симметричным NAT и ограниченным NAT. Хотя симметричное преобразование сетевых адресов (NAT) широко распространено в общественных точках, а в жилых подключениях широко используются ограниченные устройства NAT, взаимодействие между ними может привести к сбою на стороне ограниченного NAT.

     

-   Должны быть включены входящие и исходящие ICMPv6 "эхо-запросы" и "Эхо-ответ". Эти исключения необходимы для того, чтобы клиент Teredo мог действовать в качестве ретранслятора для конкретного узла Teredo. Ретранслятор, относящийся к конкретному узлу Teredo, может идентифицироваться по дополнительному собственному IPv6-адресу или адресу 6to4, указанному с помощью адреса Teredo.

Клиентские брандмауэры должны поддерживать следующие сообщения об ошибках ICMPv6 и функции обнаружения на RFC 4443:



| Код    | Описание                                    |
|---------|------------------------------------------------|
| 135/136 | Запрос на соседок ICMPV6 и объявление |
| 133/134 | Запрос маршрутизатора и объявление          |
| 128/129 | Эхо-запрос и ответ ICMPV6                  |
| 1       | Объект назначения недоступен                        |
| 2       | Пакет слишком велик                               |
| 3       | Превышение времени                                  |
| 4       | Недопустимый параметр                              |



 

Если эти сообщения не могут быть разрешены специально, то исключение всех сообщений ICMPv6 должно быть включено в брандмауэре. Кроме того, брандмауэр узла может заметить, что пакеты, классифицированные кодами 135/136 или 133/134, исходят от или предназначены для службы пользовательского режима **IpHlpSvc** , а не из стека. Эти пакеты не должны удаляться брандмауэром узла. Служба Teredo реализована в основном в службе поддержки IP в пользовательском режиме.

С помощью API брандмауэра Windows [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) для перечисления всех правил с установленным флагом обхода ребра все приложения, которые хотят прослушивать незапрошенный трафик, перечисляются для исключения брандмауэра. Конкретные сведения об использовании параметра обхода узлов [см. в](receiving-unsolicited-traffic-over-teredo.md)этой статьи.

Обратные вызовы не связаны со следующим образцом кода перечисления. настоятельно рекомендуется периодически выполнять перечисление с помощью брандмауэров сторонних производителей или при обнаружении брандмауэром нового приложения, пытающегося пройти через брандмауэр.


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



 

 