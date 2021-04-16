---
title: Вопросы безопасности узла устройства
description: При использовании узла устройства создаются проблемы безопасности.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5a51b90bff33949a33cd9fa1046deb1916ab30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487864"
---
# <a name="device-host-security-considerations"></a><span data-ttu-id="ed968-103">Вопросы безопасности узла устройства</span><span class="sxs-lookup"><span data-stu-id="ed968-103">Device Host Security Considerations</span></span>

<span data-ttu-id="ed968-104">Использование узла устройства создает проблемы безопасности из-за следующих причин:</span><span class="sxs-lookup"><span data-stu-id="ed968-104">Using the device host creates security issues because of the following:</span></span>

-   <span data-ttu-id="ed968-105">Устройства, размещенные на компьютере под управлением Windows XP, отправляют объявления по всем сетям.</span><span class="sxs-lookup"><span data-stu-id="ed968-105">Devices hosted on a computer running Windows XP sends announcements on all networks.</span></span>
-   <span data-ttu-id="ed968-106">Устройства, размещенные на компьютере под управлением Windows XP, позволяют управлять устройствами из всех сетей.</span><span class="sxs-lookup"><span data-stu-id="ed968-106">Devices hosted on a computer running Windows XP allow control of devices from all networks.</span></span>

<span data-ttu-id="ed968-107">Это повышает риск для домашних потребителей, так как такие устройства, как проигрыватель мультимедиа или система с мостом или КОНДИЦИОНИРОВАНие, размещенные на компьютере под управлением Windows XP, являются видимыми и могут контролироваться с контрольных точек, находящихся за пределами дома.</span><span class="sxs-lookup"><span data-stu-id="ed968-107">This increases the risk to home consumers, because devices such as a media player or a bridged lighting or HVAC system hosted on a computer running Windows XP are visible and can be controlled from control points outside the home.</span></span>

<span data-ttu-id="ed968-108">При создании размещенного устройства необходимо принять во внимание некоторые проблемы безопасности.</span><span class="sxs-lookup"><span data-stu-id="ed968-108">When you are creating a hosted device, you need to take into consideration some security issues.</span></span>

-   <span data-ttu-id="ed968-109">Чтобы сократить область обнаружения и атаки устройств на основе UPnP, срок жизни сообщений SSDP составляет 1.</span><span class="sxs-lookup"><span data-stu-id="ed968-109">To reduce the scope of discovery and attack of UPnP-based devices, the TTL of all SSDP messages is 1.</span></span> <span data-ttu-id="ed968-110">Это означает, что зарегистрированное устройство обнаруживается только контрольными точками в той же сети.</span><span class="sxs-lookup"><span data-stu-id="ed968-110">This means that a registered device is only discovered by control points on the same network.</span></span> <span data-ttu-id="ed968-111">В реестре можно настроить более высокий срок жизни.</span><span class="sxs-lookup"><span data-stu-id="ed968-111">You can configure a higher TTL in the registry.</span></span>
-   <span data-ttu-id="ed968-112">Для регистрации неработающего устройства требуется предварительная регистрация библиотеки DLL устройства с COM, для которой требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="ed968-112">Registering a non-running device requires pre-registering the device .dll with COM, which requires administrator privilege.</span></span>
-   <span data-ttu-id="ed968-113">Для регистрации работающего устройства требуется привилегия администратора, локальной службы или локальной системы.</span><span class="sxs-lookup"><span data-stu-id="ed968-113">Registering a running device requires Administrator, Local Service, or Local System privilege.</span></span>
-   <span data-ttu-id="ed968-114">При запуске узел устройства запускается как [LocalService](/windows/desktop/Services/localservice-account).</span><span class="sxs-lookup"><span data-stu-id="ed968-114">When the device host is started, it is run as [LocalService](/windows/desktop/Services/localservice-account).</span></span> <span data-ttu-id="ed968-115">Это дает устройству возможность создавать аудиты и читать раздел реестра **hKey \_ Local \_ Machine** .</span><span class="sxs-lookup"><span data-stu-id="ed968-115">This gives the device the ability to generate audits and read the **HKEY\_LOCAL\_MACHINE** registry key.</span></span> <span data-ttu-id="ed968-116">Устройство имеет доступ к **hKey \_ текущего \_ пользователя**.</span><span class="sxs-lookup"><span data-stu-id="ed968-116">The device does have access to **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="ed968-117">Учетная запись LocalService может использовать ресурсы, к которым локальная служба предоставляет доступ, а также те, которые предоставляют доступ к Аусентикатедусер.</span><span class="sxs-lookup"><span data-stu-id="ed968-117">The LocalService account can use resources to which LocalService has been granted access, as well as those that grant access to AuthenticatedUser.</span></span> <span data-ttu-id="ed968-118">Устройство имеет ограниченный доступ к файловой системе.</span><span class="sxs-lookup"><span data-stu-id="ed968-118">The device has restricted file system access.</span></span>
-   <span data-ttu-id="ed968-119">Списки управления доступом файловой системы должны быть обновлены, чтобы разрешить доступ к каталогу ресурсов для [локальной](/windows/desktop/Services/localservice-account) службы.</span><span class="sxs-lookup"><span data-stu-id="ed968-119">The file system ACLs must be updated to allow [LocalService](/windows/desktop/Services/localservice-account) access to the resource directory.</span></span>
-   <span data-ttu-id="ed968-120">Если устройство должно иметь более безопасный доступ, можно создать собственный процесс для устройства и зарегистрировать его с помощью [**иупнпрегистрар:: регистерруннингдевице**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).</span><span class="sxs-lookup"><span data-stu-id="ed968-120">If your device must have more security access, you can create your own process for the device and register it by using [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).</span></span>

 

 