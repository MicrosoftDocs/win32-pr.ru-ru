---
title: Макет реестра маршрутизации и удаленного доступа
description: Следующий синтаксис показывает пример макета реестра для службы маршрутизатора.
ms.assetid: 5464c2f7-6bb8-4838-939d-d58508715505
keywords:
- Маршрутизация и удаленный доступ службы маршрутизации и удаленного доступа, макет реестра маршрутизации и удаленного доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed72b569a8fe2efe1423ce2429c31cd0a0a65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888335"
---
# <a name="routing-and-remote-access-registry-layout"></a><span data-ttu-id="68919-104">Макет реестра маршрутизации и удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="68919-104">Routing and Remote Access Registry Layout</span></span>

<span data-ttu-id="68919-105">Следующий синтаксис показывает пример макета реестра для службы маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="68919-105">The following syntax shows an example registry layout for the router service.</span></span>

``` syntax
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\RasMan 
    \PPP
        \ControlProtocols
            \Builtin
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\rasppp.dll
            \Chap
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\raschap.dll
        \EAP 
            \<typeID> 
                ConfigCLSID: REG_SZ: <guid> 
                ConfigUiPath: REG_EXPAND_SZ: %SystemRoot%\System32\rastls.dll 
                FriendlyName: REG_SZ: Public Key Based Authentication (EAP-TLS) 
                IdentityUIPath: REG_EXPAND_SZ: %SystemRoot%\System32\rastls.dll 
                InvokePasswordDialog: REG_DWORD: 0 
                InvokeUsernameDialog: REG_DWORD: 0 
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\rastls.dll 
            \<typeID> 
                FriendlyName: REG_SZ: MD5 CHAP 
                InvokePasswordDialog: REG_DWORD: 0x1 
                InvokeUsernameDialog: REG_DWORD: 0x1 
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\raschap.dll 
                StandaloneSupported: REG_DWORD: 0 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\RemoteAccess 
    \Accounting 
        \Providers 
            ActiveProvider: REG_SZ: . . .             \<guid>
                ConfigCLSID: REG_SZ: <guid>
                DisplayName: REG_SZ: Radius Accounting
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\rasrad.dll
                Vendor: REG_SZ: Microsoft
             . . . 
    \Authentication 
        \Providers 
            ActiveProvider: REG_SZ: . . .             \<guid>
                ConfigCLSID: REG_SZ: <guid>
                DisplayName: REG_SZ: Radius Authentication
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\rasrad.dll
                Vendor: REG_SZ: Microsoft
            \<guid>
                ConfigCLSID: REG_SZ: <guid>
                DisplayName: REG_SZ: NT Authentication
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\rasauth.dll
                Vendor: REG_SZ: Microsoft
             . . . 
    \DemandDialManager
        DLLPath: REG_EXPAND_SZ: . . . 
        < RAS parameters and DDM parameters > 
    \Interfaces
        \0
            Enabled: REG_DWORD: (0/1) 
            InterfaceName: REG_SZ: CorpHQ 
            Type: REG_DWORD: (Internal/Dedicated/Loopback) 
                \IP
                    InterfaceInfo: REG_BINARY: . . . 
                    ProtocolID: REG_DWORD: 0x0021 
                \IPX
                    InterfaceInfo: REG_BINARY: . . . 
                    ProtocolID: REG_DWORD: 0x002B
                . . . 
        \N
            InterfaceName: REG_SZ: IntelEtherExpressPro2 
            . . . 
    \Parameters 
        LANOnlyMode: REG_DWORD: (0/1) 
        ServerFlags: REG_DWORD: . . . 
        ServiceDLL: REG_EXPAND_SZ: %SystemRoot%\System32\mprdim.dll
    \RouterManagers 
        \IP 
            DLLPath: REG_SZ: . . . 
            GlobalInFilter: REG_BSZ: < filter set name > . . . 
            GlobalInfo: REG_BINARY: . . . 
            GlobalInterfaceInfo: REG_BINARY: . . . 
            ProtocolID: REG_DWORD: 0x0021 
            . . . 
            \IPX 
            DLLPath: REG_SZ: . . . 
            GlobalInFilter: REG_BSZ: < filter set name > . . . 
            GlobalInfo: REG_BINARY: . . . 
            GlobalInterfaceInfo: REG_BINARY: . . . 
            ProtocolID: REG_DWORD: 0x002B 
            . . . 
        . . .
 
HKEY_LOCAL_MACHINE\Software\Microsoft 
    \Router 
        \CurrentVersion 
            \RouterManagers 
                \IP 
                    \OSPF 
                        ConfigDll: REG_SZ: ipadmin.dll 
                        DllName: REG_SZ: ospf.dll 
                        ProtocolID: REG_DWORD: 0xD 
                        Title: REG_SZ: Open Shortest Path First 
                    \IPBOOTP
                        . . . 
                    \IPRIP
                        . . . 
                \IPX 
                    \IpxRip 
                        ConfigDll: REG_SZ: ipxadmin.dll 
                        DllName: REG_SZ: IPXRIP.DLL 
                        ProtocolID: REG_DWORD: 0x20000 
                        Title: REG_SZ: RIP for Ipx 
                    \IpxSap
                        . . . 
                    . . . 
            \UIConfigDlls 
                <guid1>: REG_SZ: ifadmin.dll 
                <guid2>: REG_SZ: ipadmin.dll 
                <guid3>: REG_SZ: ipxadmin.dll 
                <guid4>: REG_SZ: ddmadmin.dll
```

<span data-ttu-id="68919-106">Каждый диспетчер маршрутизаторов, установленный в системе, имеет раздел реестра, созданный в разделе ключа маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="68919-106">Every router manager installed in the system has a registry key created under the Router key.</span></span> <span data-ttu-id="68919-107">Переменная DLLPath указывает расположение библиотеки DLL, которая соответствует диспетчеру маршрутизации, а переменная Протоколид указывает идентификатор семейства протоколов для диспетчера маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="68919-107">The DLLPath variable specifies the location of the DLL that corresponds to the router manager and the ProtocolID variable specifies the protocol family identifier for the router manager.</span></span>

<span data-ttu-id="68919-108">Ключ интерфейсов заполняется интерфейсами, которые были добавлены в локальную систему из конфигурации маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="68919-108">The Interfaces key is populated with the interfaces that have been added to the local system from the Router configuration.</span></span> <span data-ttu-id="68919-109">Каждый интерфейс имеет связанный тип (внутренний, выделенный или динамический) и подразделы для каждого диспетчера маршрутизатора (например, IP-адрес и IPX).</span><span class="sxs-lookup"><span data-stu-id="68919-109">Each interface has an associated Type (Internal, Dedicated, or Dynamic) and subkeys for each router manager (IP and IPX, for example).</span></span>

 

 




