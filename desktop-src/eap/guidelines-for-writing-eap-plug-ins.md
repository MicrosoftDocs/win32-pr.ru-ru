---
title: Рекомендации по написанию DLL-библиотек EAP
description: Библиотеки DLL или подключаемые модули EAP можно использовать для оптимизации производительности в различных сценариях.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc2d437df61811e6fb24b3a9b4ff406ced4905
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105710217"
---
# <a name="guidelines-for-writing-eap-dlls"></a><span data-ttu-id="9f9aa-103">Рекомендации по написанию DLL-библиотек EAP</span><span class="sxs-lookup"><span data-stu-id="9f9aa-103">Guidelines for Writing EAP DLLs</span></span>

<span data-ttu-id="9f9aa-104">Библиотеки DLL или подключаемые модули EAP можно использовать для оптимизации производительности в различных сценариях.</span><span class="sxs-lookup"><span data-stu-id="9f9aa-104">EAP DLLs or Plug-ins can be written to optimize their performance in different scenarios.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="9f9aa-105">Общие рекомендации</span><span class="sxs-lookup"><span data-stu-id="9f9aa-105">General Guidelines</span></span>

-   <span data-ttu-id="9f9aa-106">Чтобы создать зашифрованное соединение, подключаемые модули EAP должны создавать ключи шифрования и возвращать их через атрибуты RADIUS, относящиеся к вендору Майкрософт MS-MPPE-Send-Keys и MS-MPPE-recv-Keys.</span><span class="sxs-lookup"><span data-stu-id="9f9aa-106">In order to create an encrypted connection, EAP plug-ins must generate encryption keys and return them through the Microsoft vendor-specific RADIUS Attributes MS-MPPE-Send-Keys and MS-MPPE-Recv-Keys.</span></span> <span data-ttu-id="9f9aa-107">Дополнительные сведения см. в разделе "Примечания" в [**\_ \_ выходных данных PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) .</span><span class="sxs-lookup"><span data-stu-id="9f9aa-107">See the Remarks section in [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) for more information.</span></span>

## <a name="wireless-guidelines"></a><span data-ttu-id="9f9aa-108">Рекомендации по беспроводному соединению</span><span class="sxs-lookup"><span data-stu-id="9f9aa-108">Wireless Guidelines</span></span>

<span data-ttu-id="9f9aa-109">Ниже приведены рекомендации и рекомендации по написанию подключаемого модуля EAP, поддерживающего проверку подлинности компьютеров в беспроводных сценариях (802.1 X).</span><span class="sxs-lookup"><span data-stu-id="9f9aa-109">The following are guidelines and recommendations for writing an EAP Plug-in that supports authenticating machines in wireless (802.1X) scenarios.</span></span> <span data-ttu-id="9f9aa-110">Этот раздел не относится к сценариям VPN и коммутируемого подключения.</span><span class="sxs-lookup"><span data-stu-id="9f9aa-110">This section does not apply to VPN and Dial-up scenarios.</span></span>

-   <span data-ttu-id="9f9aa-111">Чтобы не блокировать выполнение автоматических систем, подключаемые модули EAP не должны выполнять вызовы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9f9aa-111">In order not to block unattended systems' execution, EAP plug-ins must not make any user interface calls.</span></span>
-   <span data-ttu-id="9f9aa-112">Реализация подключаемого модуля аутентификации EAP для проверки подлинности компьютера должна быть выполнена как можно быстрее, поэтому она не мешает загрузке операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9f9aa-112">The EAP Plug-in implementation of the machine authentication step must complete as quickly as possible so it does not hinder operating system startup.</span></span>
    > [!Note]  
    > <span data-ttu-id="9f9aa-113">Если ваш протокол EAP не поддерживает проверку подлинности компьютера, он должен проверить флаг проверки подлинности на компьютере, использующий аутентификацию **\_ \_ \_ \_ EAP** в поле **ффлагс** в [**\_ \_ входе PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), и вернуть ошибку.</span><span class="sxs-lookup"><span data-stu-id="9f9aa-113">If your EAP protocol does not support machine authentication, it must check for the machine authentication flag, **RAS\_EAP\_FLAG\_MACHINE\_AUTH** used in the **fFlags** field in [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), and return an error.</span></span>

     

 

 




