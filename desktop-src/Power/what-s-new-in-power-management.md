---
description: Windows 10 помогает вашему приложению оптимизировать энергопотребление при работе на мобильном устройстве.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Новые возможности управления питанием
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673785"
---
# <a name="whats-new-in-power-management"></a><span data-ttu-id="31328-103">Новые возможности управления питанием</span><span class="sxs-lookup"><span data-stu-id="31328-103">What's New in Power Management</span></span>

<span data-ttu-id="31328-104">Windows 10 помогает приложению оптимизировать энергопотребление при работе на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="31328-104">Windows 10 helps your application optimize power consumption when it's running on a mobile device.</span></span>

## <a name="battery-saver"></a><span data-ttu-id="31328-105">Экономия заряда</span><span class="sxs-lookup"><span data-stu-id="31328-105">Battery saver</span></span>

<span data-ttu-id="31328-106">В этом выпуске приложение может получать уведомления при включении или отключении заставки аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="31328-106">In this release, your application can be notified when battery saver is turned on or off.</span></span> <span data-ttu-id="31328-107">Отвечая на изменение условий электропитания, приложение может работать совместно с заставкой аккумулятора для экономии энергии и увеличения времени работы аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="31328-107">By responding to changing power conditions, your application can work in concert with battery saver to save energy and help extend battery life.</span></span> <span data-ttu-id="31328-108">Общие сведения о экономии заряда батареи см. [в разделе Заставка аккумулятора (в руководстве по компонентам оборудования)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="31328-108">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="31328-109">[**Идентификатор GUID \_ \_ \_ Состояние энергосбережения**](power-setting-guids.md) . Используйте этот новый идентификатор GUID с функцией [**поверсеттингрегистернотификатион**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) , чтобы получать уведомления при включении или отключении заставки аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="31328-109">[**GUID\_POWER\_SAVING\_STATUS**](power-setting-guids.md) : Use this new GUID with the [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) function to be notified when battery saver is turned on or off.</span></span>

-   <span data-ttu-id="31328-110">[**Система \_ \_Состояние питания**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) . Эта структура была обновлена для поддержки экономии заряда.</span><span class="sxs-lookup"><span data-stu-id="31328-110">[**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : This structure has been updated to support battery saver.</span></span> <span data-ttu-id="31328-111">Четвертый элемент, **системстатусфлаг** (ранее именуемый **Reserved1**), теперь указывает, включена ли экономия заряда.</span><span class="sxs-lookup"><span data-stu-id="31328-111">The fourth member, **SystemStatusFlag** (previously named **Reserved1**), now indicates if battery saver is engaged or not.</span></span> <span data-ttu-id="31328-112">Используйте функцию [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) для получения указателя на эту структуру.</span><span class="sxs-lookup"><span data-stu-id="31328-112">Use the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve a pointer to this structure.</span></span>

 

 
