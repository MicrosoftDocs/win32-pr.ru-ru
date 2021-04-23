---
title: Использование функций настройки монитора Low-Level
description: Использование функций настройки монитора Low-Level
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- монитор, функции
- мониторинг, низкоуровневые функции настройки
- мониторинг, DDC/CI
- монитор, отображение интерфейса команды для канала данных
- Конфигурация мониторинга, низкоуровневые функции конфигурации
- мониторинг конфигурации, функции
- мониторинг конфигурации, DDC/CI
- Настройка монитора, отображение интерфейса команды для канала данных
- функции конфигурации низкого уровня
- Отображение интерфейса команд канала данных
- DDC/CI
- Набор команд управления монитором VESA (MCCS)
- Набор команд управления монитором (MCCS)
- MCCS (набор команд управления монитором)
- Виртуальная панель управления (перерис.)
- (Виртуальный) (панель управления)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987454"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a><span data-ttu-id="4cd0b-119">Использование функций настройки монитора Low-Level</span><span class="sxs-lookup"><span data-stu-id="4cd0b-119">Using the Low-Level Monitor Configuration Functions</span></span>

<span data-ttu-id="4cd0b-120">Прежде чем использовать функции конфигурации монитора низкого уровня, необходимо ознакомиться с этими стандартами:</span><span class="sxs-lookup"><span data-stu-id="4cd0b-120">Before using the low-level monitor configuration functions, you should be familiar with these standards:</span></span>

-   <span data-ttu-id="4cd0b-121">Отображение интерфейса команд канала данных (DDC/CI)</span><span class="sxs-lookup"><span data-stu-id="4cd0b-121">Display Data Channel Command Interface (DDC/CI)</span></span>
-   <span data-ttu-id="4cd0b-122">Набор команд управления монитором VESA (MCCS)</span><span class="sxs-lookup"><span data-stu-id="4cd0b-122">VESA Monitor Control Command Set (MCCS)</span></span>

<span data-ttu-id="4cd0b-123">Низкоуровневые функции работают, получая и устанавливая значения для кодов панели управления виртуальных панелей.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-123">The low-level functions work by getting and setting the values of Virtual Control Panel (VCP) codes.</span></span> <span data-ttu-id="4cd0b-124">Код «новый» может быть *непрерывным* или *ненепрерывным*.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-124">A VCP code can be *continuous* or *noncontinuous*.</span></span> <span data-ttu-id="4cd0b-125">Непрерывные коды могут принимать любое значение от нуля до максимального значения, зависящего от поставщика.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-125">Continuous codes can assume any value between zero and a vendor-specific maximum value.</span></span> <span data-ttu-id="4cd0b-126">Ненепрерывные коды поддерживают определенный набор значений, который также относится к поставщику.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-126">Noncontinuous codes support a defined set of values, which is also specific to the vendor.</span></span>

<span data-ttu-id="4cd0b-127">Чтобы использовать функции конфигурации монитора низкого уровня, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-127">To use the low-level monitor configuration functions, perform the following steps:</span></span>

1.  <span data-ttu-id="4cd0b-128">Получите обработчик **хмонитор** , вызвав [**енумдисплаймониторс**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) или [**мониторфромвиндов**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span><span class="sxs-lookup"><span data-stu-id="4cd0b-128">Obtain an **HMONITOR** handle by calling [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) or [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span></span>
2.  <span data-ttu-id="4cd0b-129">Вызовите [**жетнумбероффисикалмониторсфромхмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) , чтобы получить количество физических мониторов, связанных с маркером **хмонитор** .</span><span class="sxs-lookup"><span data-stu-id="4cd0b-129">Call [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) to get the number of physical monitors associated with the **HMONITOR** handle.</span></span>
3.  <span data-ttu-id="4cd0b-130">Вызовите [**жетфисикалмониторсфромхмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) , чтобы получить список дескрипторов физических мониторов.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-130">Call [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) to get a list of handles to the physical monitors.</span></span>
4.  <span data-ttu-id="4cd0b-131">Вызовите [**жеткапабилитиесстрингленгс**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) , чтобы получить длину строки возможностей DDC/CI монитора.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-131">Call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) to get the length of a monitor's DDC/CI capabilities string.</span></span> <span data-ttu-id="4cd0b-132">Строка возможностей — это строка ASCII, содержащая статическую информацию о мониторе.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-132">The capabilities string is an ASCII string that contains static information about the monitor.</span></span> <span data-ttu-id="4cd0b-133">В одной части строки перечислены коды, поддерживаемые монитором.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-133">One part of the string lists the VCP codes that the monitor supports.</span></span> <span data-ttu-id="4cd0b-134">Строка также содержит поддерживаемые значения кодов ненепрерывного кода версии.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-134">The string also lists the supported values of the noncontinuous VCP codes.</span></span>
5.  <span data-ttu-id="4cd0b-135">Выделите буфер для хранения строки возможностей и вызовите [**капабилитиесрекуестандкапабилитиесрепли**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) , чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-135">Allocate a buffer to hold the capabilities string and call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) to get the string.</span></span>
6.  <span data-ttu-id="4cd0b-136">Проанализируйте строку возможностей, чтобы определить, какие коды кодов, поддерживаемых монитором.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-136">Parse the capabilities string to determine which VCP codes the monitor supports.</span></span>
7.  <span data-ttu-id="4cd0b-137">Для кода непрерывной версии, вызовите [**жетвкпфеатуреандвкпфеатуререпли**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) , чтобы получить текущие и максимальные значения кода.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-137">For a continuous VCP code, call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) to get the current and maximum values of the code.</span></span> <span data-ttu-id="4cd0b-138">Для кода ненепрерывной перебора следует проанализировать строку возможностей, чтобы получить поддерживаемые значения.</span><span class="sxs-lookup"><span data-stu-id="4cd0b-138">For a noncontinuous VCP code, parse the capabilities string to get the supported values.</span></span>
8.  <span data-ttu-id="4cd0b-139">Вызовите [**сетвкпфеатуре**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) , чтобы задать новое значение для кода «новый код».</span><span class="sxs-lookup"><span data-stu-id="4cd0b-139">Call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) to set a new value for a VCP code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cd0b-140">См. также</span><span class="sxs-lookup"><span data-stu-id="4cd0b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cd0b-141">**Использование конфигурации монитора**</span><span class="sxs-lookup"><span data-stu-id="4cd0b-141">**Using Monitor Configuration**</span></span>](using-monitor-configuration.md)
</dt> </dl>

 

 