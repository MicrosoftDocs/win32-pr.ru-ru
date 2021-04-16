---
description: Идентификаторы GUID параметров питания обозначают события изменения питания.
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: Идентификаторы GUID параметров питания (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67dfd619d93f4318dbcfe2b44b5f8ba24460bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679836"
---
# <a name="power-setting-guids"></a><span data-ttu-id="9265d-103">Идентификаторы GUID параметров питания</span><span class="sxs-lookup"><span data-stu-id="9265d-103">Power Setting GUIDs</span></span>

<span data-ttu-id="9265d-104">**Идентификатор GUID** параметра питания определяет события изменения питания.</span><span class="sxs-lookup"><span data-stu-id="9265d-104">Power setting **GUID** s identify power change events.</span></span> <span data-ttu-id="9265d-105">В этом разделе перечислены **идентификаторы GUID** параметров питания для уведомлений, наиболее полезных для приложений.</span><span class="sxs-lookup"><span data-stu-id="9265d-105">This topic lists power setting **GUID** s for notifications that are most useful to applications.</span></span> <span data-ttu-id="9265d-106">Приложение должно регистрироваться для каждого события изменения питания, которое может повлиять на его поведение.</span><span class="sxs-lookup"><span data-stu-id="9265d-106">An application should register for each power change event that might impact its behavior.</span></span> <span data-ttu-id="9265d-107">Уведомление отправляется каждый раз при изменении параметра.</span><span class="sxs-lookup"><span data-stu-id="9265d-107">Notification is sent each time a setting changes.</span></span>

<span data-ttu-id="9265d-108">**Идентификаторы GUID** параметров питания определены в Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="9265d-108">Power setting **GUID** s are defined in WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="9265d-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**\_ \_ источник питания GUID \_ акдк**</span><span class="sxs-lookup"><span data-stu-id="9265d-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID\_ACDC\_POWER\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9265d-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span><span class="sxs-lookup"><span data-stu-id="9265d-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span></span>
</dt> <dt>



<span data-ttu-id="9265d-111">Источник питания системы изменился.</span><span class="sxs-lookup"><span data-stu-id="9265d-111">The system power source has changed.</span></span> <span data-ttu-id="9265d-112">Элемент **данных** — это **DWORD** со значениями из перечисления [**системных \_ \_ условий питания**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) , которые указывают текущий источник питания.</span><span class="sxs-lookup"><span data-stu-id="9265d-112">The **Data** member is a **DWORD** with values from the [**SYSTEM\_POWER\_CONDITION**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) enumeration that indicates the current power source.</span></span>

<dl> <dt>

<span data-ttu-id="9265d-113">**Поак** (0) — компьютер питается с помощью источника питания (или аналогичного), например ноутбука, включенного в автомобильный адаптер 12В.</span><span class="sxs-lookup"><span data-stu-id="9265d-113">**PoAc** (0) - The computer is powered by an AC power source (or similar, such as a laptop powered by a 12V automotive adapter).</span></span>
</dt> <dt>

<span data-ttu-id="9265d-114">**Подк** (1) — компьютер питается от встроенного источника питания от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="9265d-114">**PoDc** (1) - The computer is powered by an onboard battery power source.</span></span>
</dt> <dt>

<span data-ttu-id="9265d-115">**Похот** (2) — компьютер работает под управлением краткосрочного источника питания, например устройства ИБП.</span><span class="sxs-lookup"><span data-stu-id="9265d-115">**PoHot** (2) - The computer is powered by a short-term power source such as a UPS device.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="9265d-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**\_оставшееся время заряда батареи (GUID) \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9265d-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**GUID\_BATTERY\_PERCENTAGE\_REMAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9265d-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span><span class="sxs-lookup"><span data-stu-id="9265d-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span></span>
</dt> <dt>



<span data-ttu-id="9265d-118">Оставшаяся емкость аккумулятора изменилась.</span><span class="sxs-lookup"><span data-stu-id="9265d-118">The remaining battery capacity has changed.</span></span> <span data-ttu-id="9265d-119">Гранулярность зависит от системы к системе, но степень гранулярности Finest составляет 1%.</span><span class="sxs-lookup"><span data-stu-id="9265d-119">The granularity varies from system to system but the finest granularity is 1 percent.</span></span> <span data-ttu-id="9265d-120">Элемент **данных** — это **DWORD** , который указывает, что текущая емкость батареи остается в процентах от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="9265d-120">The **Data** member is a **DWORD** that indicates the current battery capacity remaining as a percentage from 0 through 100.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9265d-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**\_ \_ состояние отображения консоли \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="9265d-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**GUID\_CONSOLE\_DISPLAY\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9265d-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span><span class="sxs-lookup"><span data-stu-id="9265d-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span></span>
</dt> <dt>



<span data-ttu-id="9265d-123">Состояние отображения текущего монитора изменилось.</span><span class="sxs-lookup"><span data-stu-id="9265d-123">The current monitor's display state has changed.</span></span>

<span data-ttu-id="9265d-124">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это уведомление доступно начиная с Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="9265d-124">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="9265d-125">Элемент **данных** является **DWORD** с одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9265d-125">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9265d-126">0x0 — экран отключен.</span><span class="sxs-lookup"><span data-stu-id="9265d-126">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="9265d-127">0x1 — дисплей включен.</span><span class="sxs-lookup"><span data-stu-id="9265d-127">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="9265d-128">0x2 — дисплей недоступен.</span><span class="sxs-lookup"><span data-stu-id="9265d-128">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="9265d-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**Глобальный уникальный идентификатор GUID \_ \_ \_ присутствия пользователя**</span><span class="sxs-lookup"><span data-stu-id="9265d-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**GUID\_GLOBAL\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9265d-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span><span class="sxs-lookup"><span data-stu-id="9265d-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span></span>
</dt> <dt>



<span data-ttu-id="9265d-131">Изменилось состояние пользователя, связанное с любым сеансом.</span><span class="sxs-lookup"><span data-stu-id="9265d-131">The user status associated with any session has changed.</span></span> <span data-ttu-id="9265d-132">Представляет собой объединенное состояние присутствия пользователя во всех локальных и удаленных сеансах в системе.</span><span class="sxs-lookup"><span data-stu-id="9265d-132">This represents the combined status of user presence across all local and remote sessions on the system.</span></span>

<span data-ttu-id="9265d-133">Это уведомление отправляется только в службы и другие программы, запущенные в сеансе 0.</span><span class="sxs-lookup"><span data-stu-id="9265d-133">This notification is sent only services and other programs running in session 0.</span></span> <span data-ttu-id="9265d-134">Приложения пользовательского режима должны регистрироваться для **определения \_ \_ \_ присутствия пользователя сеанса GUID** .</span><span class="sxs-lookup"><span data-stu-id="9265d-134">User-mode applications should register for **GUID\_SESSION\_USER\_PRESENCE** instead.</span></span>

<span data-ttu-id="9265d-135">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это уведомление доступно начиная с Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="9265d-135">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="9265d-136">Элемент **данных** является **DWORD** с одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9265d-136">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9265d-137">**Поверусерпресент** (0) — пользователь находится в любом локальном или удаленном сеансе в системе.</span><span class="sxs-lookup"><span data-stu-id="9265d-137">**PowerUserPresent** (0) - The user is present in any local or remote session on the system.</span></span>
</dt> <dt>

<span data-ttu-id="9265d-138">**Поверусеринактиве** (2) — пользователь отсутствует в локальном или удаленном сеансе в системе.</span><span class="sxs-lookup"><span data-stu-id="9265d-138">**PowerUserInactive** (2) - The user is not present in any local or remote session on the system.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="9265d-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**\_ \_ Фоновая задача БЕЗдействия GUID \_**</span><span class="sxs-lookup"><span data-stu-id="9265d-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**GUID\_IDLE\_BACKGROUND\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9265d-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span><span class="sxs-lookup"><span data-stu-id="9265d-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span></span>
</dt> <dt>



<span data-ttu-id="9265d-141">Система занята.</span><span class="sxs-lookup"><span data-stu-id="9265d-141">The system is busy.</span></span> <span data-ttu-id="9265d-142">Это означает, что система не будет переноситься в состояние простоя в ближайшем будущем, и текущее время будет хорошим временем для выполнения компонентами фоновых или бездействующих задач, которые в противном случае препятствуют переходу компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="9265d-142">This indicates that the system will not be moving into an idle state in the near future and that the current time is a good time for components to perform background or idle tasks that would otherwise prevent the computer from entering an idle state.</span></span>

<span data-ttu-id="9265d-143">Если система может перейти в состояние простоя, уведомления не выявляются.</span><span class="sxs-lookup"><span data-stu-id="9265d-143">There is no notification when the system is able to move into an idle state.</span></span> <span data-ttu-id="9265d-144">Уведомление о фоновой задаче простоя не указывает, имеется ли на компьютере пользователь.</span><span class="sxs-lookup"><span data-stu-id="9265d-144">The idle background task notification does not indicate whether a user is present at the computer.</span></span> <span data-ttu-id="9265d-145">Элемент **данных** не содержит сведений и может быть проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="9265d-145">The **Data** member has no information and can be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9265d-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_Включить монитор \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="9265d-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**GUID\_MONITOR\_POWER\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9265d-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span><span class="sxs-lookup"><span data-stu-id="9265d-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span></span>
</dt> <dt>



<span data-ttu-id="9265d-148">Основной системный монитор включен или отключен.</span><span class="sxs-lookup"><span data-stu-id="9265d-148">The primary system monitor has been powered on or off.</span></span> <span data-ttu-id="9265d-149">Это уведомление полезно для компонентов, которые активно отображают содержимое на устройстве отображения, например визуализация мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9265d-149">This notification is useful for components that actively render content to the display device, such as media visualization.</span></span> <span data-ttu-id="9265d-150">Эти приложения должны регистрироваться для этого уведомления и прерывать отрисовку графического содержимого, когда монитор отключен, чтобы сократить энергопотребление системы.</span><span class="sxs-lookup"><span data-stu-id="9265d-150">These applications should register for this notification and stop rendering graphics content when the monitor is off to reduce system power consumption.</span></span> <span data-ttu-id="9265d-151">Элемент **данных** — это **DWORD** , указывающий текущее состояние монитора.</span><span class="sxs-lookup"><span data-stu-id="9265d-151">The **Data** member is a **DWORD** that indicates the current monitor state.</span></span>

<dl> <dt>

<span data-ttu-id="9265d-152">0x0 — монитор отключен.</span><span class="sxs-lookup"><span data-stu-id="9265d-152">0x0 - The monitor is off.</span></span>
</dt> <dt>

<span data-ttu-id="9265d-153">0x1 — монитор включен.</span><span class="sxs-lookup"><span data-stu-id="9265d-153">0x1 - The monitor is on.</span></span>
</dt> </dl>

<span data-ttu-id="9265d-154">**Windows 8 и Windows Server 2012:** Новые приложения должны использовать **\_ \_ \_ состояние отображения консоли GUID** вместо этого уведомления.</span><span class="sxs-lookup"><span data-stu-id="9265d-154">**Windows 8 and Windows Server 2012:** New applications should use **GUID\_CONSOLE\_DISPLAY\_STATE** instead of this notification.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="9265d-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**\_ \_ состояние ЭНЕРГОсбережения \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="9265d-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**GUID\_POWER\_SAVING\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9265d-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span><span class="sxs-lookup"><span data-stu-id="9265d-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span></span>
</dt> <dt>



<span data-ttu-id="9265d-157">Экономия заряда отключена или включена в ответ на изменение состояния электропитания.</span><span class="sxs-lookup"><span data-stu-id="9265d-157">Battery saver has been turned off or on in response to changing power conditions.</span></span> <span data-ttu-id="9265d-158">Это уведомление полезно для компонентов, участвующих в энергосбережении.</span><span class="sxs-lookup"><span data-stu-id="9265d-158">This notification is useful for components that participate in energy conservation.</span></span> <span data-ttu-id="9265d-159">Эти приложения должны зарегистрироваться для получения уведомлений и сэкономить питание при включенной экономии заряда.</span><span class="sxs-lookup"><span data-stu-id="9265d-159">These applications should register for this notification and save power when battery saver is on.</span></span>

<span data-ttu-id="9265d-160">Элемент **данных** — это **DWORD** , который указывает состояние экономии заряда.</span><span class="sxs-lookup"><span data-stu-id="9265d-160">The **Data** member is a **DWORD** that indicates battery saver state.</span></span>

<dl> <dt>

<span data-ttu-id="9265d-161">0x0 — экономия заряда батареи отключена.</span><span class="sxs-lookup"><span data-stu-id="9265d-161">0x0 - Battery saver is off.</span></span>
</dt> <dt>

<span data-ttu-id="9265d-162">0x1 — экономия заряда батареи включена.</span><span class="sxs-lookup"><span data-stu-id="9265d-162">0x1 - Battery saver is on.</span></span> <span data-ttu-id="9265d-163">Сэкономьте энергию, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="9265d-163">Save energy where possible.</span></span>
</dt> </dl>

<span data-ttu-id="9265d-164">Общие сведения о экономии заряда батареи см. [в разделе Заставка аккумулятора (в руководстве по компонентам оборудования)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="9265d-164">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

</dl> </dd> <dt>

<span data-ttu-id="9265d-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID \_ поверсчеме \_**</span><span class="sxs-lookup"><span data-stu-id="9265d-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID\_POWERSCHEME\_PERSONALITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9265d-166">245d8541-3943-4422-b025-13A784F679B7</span><span class="sxs-lookup"><span data-stu-id="9265d-166">245d8541-3943-4422-b025-13A784F679B7</span></span>
</dt> <dt>



<span data-ttu-id="9265d-167">Активная схема управления питанием изменена.</span><span class="sxs-lookup"><span data-stu-id="9265d-167">The active power scheme personality has changed.</span></span> <span data-ttu-id="9265d-168">Все схемы управления питанием сопоставляются с одним из этих личных настроек.</span><span class="sxs-lookup"><span data-stu-id="9265d-168">All power schemes map to one of these personalities.</span></span> <span data-ttu-id="9265d-169">Элемент **данных** — это **идентификатор GUID** , указывающий на новую активную схему управления питанием.</span><span class="sxs-lookup"><span data-stu-id="9265d-169">The **Data** member is a **GUID** that indicates the new active power scheme personality.</span></span>

<dl> <dt>



<span data-ttu-id="9265d-170">**Идентификатор GUID \_ Минимальная \_ \_ экономия энергии** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)</span><span class="sxs-lookup"><span data-stu-id="9265d-170">**GUID\_MIN\_POWER\_SAVINGS** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)</span></span>

<span data-ttu-id="9265d-171">Высокая производительность. Схема разработана для обеспечения максимальной производительности за счет экономии энергии.</span><span class="sxs-lookup"><span data-stu-id="9265d-171">High Performance - The scheme is designed to deliver maximum performance at the expense of power consumption savings.</span></span>


</dt> <dt>



<span data-ttu-id="9265d-172">**Идентификатор GUID \_ Максимальная \_ \_ экономия энергии** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span><span class="sxs-lookup"><span data-stu-id="9265d-172">**GUID\_MAX\_POWER\_SAVINGS** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span></span>

<span data-ttu-id="9265d-173">Power экономия — схема предназначена для обеспечения максимальной экономии энергии за счет снижения производительности и скорости реагирования системы.</span><span class="sxs-lookup"><span data-stu-id="9265d-173">Power Saver - The scheme is designed to deliver maximum power consumption savings at the expense of system performance and responsiveness.</span></span>


</dt> <dt>



<span data-ttu-id="9265d-174">**Идентификатор GUID \_ ТИПИЧная \_ \_ экономия энергии** (381B4222-F694-41F0-9685-FF5BB260DF2E)</span><span class="sxs-lookup"><span data-stu-id="9265d-174">**GUID\_TYPICAL\_POWER\_SAVINGS** (381B4222-F694-41F0-9685-FF5BB260DF2E)</span></span>

<span data-ttu-id="9265d-175">Автоматически. Эта схема предназначена для автоматического распределения производительности и экономии энергии.</span><span class="sxs-lookup"><span data-stu-id="9265d-175">Automatic - The scheme is designed to automatically balance performance and power consumption savings.</span></span>


</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="9265d-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**\_ \_ состояние отображаемого сеанса GUID \_**</span><span class="sxs-lookup"><span data-stu-id="9265d-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**GUID\_SESSION\_DISPLAY\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9265d-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span><span class="sxs-lookup"><span data-stu-id="9265d-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span></span>
</dt> <dt>



<span data-ttu-id="9265d-178">Дисплей, связанный с сеансом приложения, включен или выключен.</span><span class="sxs-lookup"><span data-stu-id="9265d-178">The display associated with the application's session has been powered on or off.</span></span>

<span data-ttu-id="9265d-179">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это уведомление доступно начиная с Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="9265d-179">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="9265d-180">Это уведомление отправляется только в приложения пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="9265d-180">This notification is sent only to user-mode applications.</span></span> <span data-ttu-id="9265d-181">Службы и другие программы, запущенные в сеансе 0, не получают это уведомление.</span><span class="sxs-lookup"><span data-stu-id="9265d-181">Services and other programs running in session 0 do not receive this notification.</span></span> <span data-ttu-id="9265d-182">Элемент **данных** является **DWORD** с одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9265d-182">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9265d-183">0x0 — экран отключен.</span><span class="sxs-lookup"><span data-stu-id="9265d-183">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="9265d-184">0x1 — дисплей включен.</span><span class="sxs-lookup"><span data-stu-id="9265d-184">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="9265d-185">0x2 — дисплей недоступен.</span><span class="sxs-lookup"><span data-stu-id="9265d-185">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="9265d-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**GUID \_ \_ присутствия пользователя \_ сеанса**</span><span class="sxs-lookup"><span data-stu-id="9265d-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**GUID\_SESSION\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9265d-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span><span class="sxs-lookup"><span data-stu-id="9265d-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span></span>
</dt> <dt>



<span data-ttu-id="9265d-188">Изменено состояние пользователя, связанное с сеансом приложения.</span><span class="sxs-lookup"><span data-stu-id="9265d-188">The user status associated with the application's session has changed.</span></span>

<span data-ttu-id="9265d-189">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это уведомление доступно начиная с Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="9265d-189">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="9265d-190">Это уведомление отправляется только в приложения пользовательского режима, выполняющиеся в интерактивном сеансе.</span><span class="sxs-lookup"><span data-stu-id="9265d-190">This notification is sent only to user-mode applications running in an interactive session.</span></span> <span data-ttu-id="9265d-191">Службы и другие программы, запущенные в сеансе 0, должны регистрироваться для **\_ глобального \_ \_ присутствия пользователя GUID**.</span><span class="sxs-lookup"><span data-stu-id="9265d-191">Services and other programs running in session 0 should register for **GUID\_GLOBAL\_USER\_PRESENCE**.</span></span> <span data-ttu-id="9265d-192">Элемент **данных** является **DWORD** с одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9265d-192">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9265d-193">**Поверусерпресент** (0) — пользователь предоставляет входные данные для сеанса.</span><span class="sxs-lookup"><span data-stu-id="9265d-193">**PowerUserPresent** (0) - The user is providing input to the session.</span></span>
</dt> <dt>

<span data-ttu-id="9265d-194">**Поверусеринактиве** (2) — время ожидания действия пользователя истекло без взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="9265d-194">**PowerUserInactive** (2) - The user activity timeout has elapsed with no interaction from the user.</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="9265d-195">Этот параметр следует использовать для всех приложений, выполняемых в интерактивном сеансе пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="9265d-195">All applications that run in an interactive user-mode session should use this setting.</span></span> <span data-ttu-id="9265d-196">Когда приложения в режиме ядра регистрируются в состоянии монитора, они должны использовать **\_ \_ \_ состояние отображения консоли GUID** .</span><span class="sxs-lookup"><span data-stu-id="9265d-196">When kernel mode applications register for monitor status they should use **GUID\_CONSOLE\_DISPLAY\_STATUS** instead.</span></span>

 

</dl> </dd> <dt>

<span data-ttu-id="9265d-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**Идентификатор GUID \_ системы \_ AWAYMODE**</span><span class="sxs-lookup"><span data-stu-id="9265d-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID\_SYSTEM\_AWAYMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9265d-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span><span class="sxs-lookup"><span data-stu-id="9265d-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span></span>
</dt> <dt>



<span data-ttu-id="9265d-199">Система выполняет вход или выход из режима отсутствия.</span><span class="sxs-lookup"><span data-stu-id="9265d-199">The system is entering or exiting away mode.</span></span> <span data-ttu-id="9265d-200">Элемент **данных** — это **DWORD** , указывающий состояние текущего режима отсутствия.</span><span class="sxs-lookup"><span data-stu-id="9265d-200">The **Data** member is a **DWORD** that indicates the current away mode state.</span></span>

<dl> <dt>

<span data-ttu-id="9265d-201">0x0 — компьютер выходит из режима отсутствия.</span><span class="sxs-lookup"><span data-stu-id="9265d-201">0x0 - The computer is exiting away mode.</span></span>
</dt> <dt>

<span data-ttu-id="9265d-202">0x1 — компьютер переходит в режим отсутствия на месте.</span><span class="sxs-lookup"><span data-stu-id="9265d-202">0x1 - The computer is entering away mode.</span></span>
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9265d-203">Требования</span><span class="sxs-lookup"><span data-stu-id="9265d-203">Requirements</span></span>



| <span data-ttu-id="9265d-204">Требование</span><span class="sxs-lookup"><span data-stu-id="9265d-204">Requirement</span></span> | <span data-ttu-id="9265d-205">Значение</span><span class="sxs-lookup"><span data-stu-id="9265d-205">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9265d-206">Header</span><span class="sxs-lookup"><span data-stu-id="9265d-206">Header</span></span><br/> | <dl> <span data-ttu-id="9265d-207"><dt>Файл WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9265d-207"><dt>WinNT.h</dt></span></span> </dl> |



 

