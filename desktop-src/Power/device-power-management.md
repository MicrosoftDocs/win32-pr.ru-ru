---
description: API управления питанием устройств позволяет легко определить, какие устройства могут пробудить систему из спящего режима, а также состояние спящего режима, в котором эти устройства поддерживают пробуждение. Дополнительные сведения о состояниях спящего режима см. в разделе Системные состояния питания.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Управление питанием устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998506"
---
# <a name="device-power-management"></a><span data-ttu-id="89154-104">Управление питанием устройств</span><span class="sxs-lookup"><span data-stu-id="89154-104">Device Power Management</span></span>

<span data-ttu-id="89154-105">API управления питанием устройств позволяет легко определить, какие устройства могут пробудить систему из спящего режима, а также состояние спящего режима, в котором эти устройства поддерживают пробуждение.</span><span class="sxs-lookup"><span data-stu-id="89154-105">The Device Power API makes it easy to determine which devices are able to wake the system from a sleep state, and which sleep states those devices support waking from.</span></span> <span data-ttu-id="89154-106">Дополнительные сведения о состояниях спящего режима см. в разделе [системные состояния питания](system-power-states.md).</span><span class="sxs-lookup"><span data-stu-id="89154-106">For more information about sleep states, see [System Power States](system-power-states.md).</span></span>

<span data-ttu-id="89154-107">Функцию [**девицеповеренумдевицес**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) можно использовать для поиска устройств, соответствующих указанным критериям, в списке устройств.</span><span class="sxs-lookup"><span data-stu-id="89154-107">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function can be used to search the device list for devices that match specified criteria.</span></span> <span data-ttu-id="89154-108">Критерии могут включать способность устройства поддерживать состояние системы или выходить из этого состояния.</span><span class="sxs-lookup"><span data-stu-id="89154-108">The criteria may include the device's ability to support a system state, or wake from that state.</span></span> <span data-ttu-id="89154-109">Текущие поддерживаемые флаги можно найти в WinNT. h и Девповер. h.</span><span class="sxs-lookup"><span data-stu-id="89154-109">Currently supported flags can be found in WinNT.h and DevPower.h.</span></span>

<span data-ttu-id="89154-110">Функция [**девицеповерсетдевицестате**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) включает или отключает пробуждение системы из состояния сна.</span><span class="sxs-lookup"><span data-stu-id="89154-110">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function enables or disables a specified device from waking the system from a sleep state.</span></span>

<span data-ttu-id="89154-111">API управления питанием устройств позволяет разработчикам повысить удобство работы пользователей, предоставляя пользователю дополнительные сведения о том, что делает система, и предоставляет больший контроль над устройствами в системе.</span><span class="sxs-lookup"><span data-stu-id="89154-111">The Device Power API allows developers to create a better user experience by giving the user more information about what the system is doing, and more control over the devices in the system.</span></span> <span data-ttu-id="89154-112">Мощность устройства полезна в ситуациях, когда потребление энергии является критически важным, например портативными устройствами, работающими на аккумуляторах.</span><span class="sxs-lookup"><span data-stu-id="89154-112">Device Power is useful in situations where power consumption is critical, such as in portable devices running on batteries.</span></span> <span data-ttu-id="89154-113">Например, схема управления питанием, используемая на настольном компьютере, может не быть оптимальной схемой для переносного компьютера, поэтому пользователю может потребоваться отключить пробуждение системы определенными устройствами.</span><span class="sxs-lookup"><span data-stu-id="89154-113">For example, the power management scheme used in a desktop computer may not be the optimal scheme for a laptop computer, so the user may want to disable certain devices from waking the system.</span></span> <span data-ttu-id="89154-114">Это может сэкономить энергию, так как отключенные устройства не смогут рисовать питание, а система находится в спящем режиме.</span><span class="sxs-lookup"><span data-stu-id="89154-114">This can conserve energy because the disabled devices will not draw power while the system is in sleep mode.</span></span>

<span data-ttu-id="89154-115">Пример см. в разделе [Использование API управления питанием устройства](using-the-device-power-api.md).</span><span class="sxs-lookup"><span data-stu-id="89154-115">For an example, see [Using the Device Power API](using-the-device-power-api.md).</span></span>

 

 



