---
title: Разделы реестра WCS
description: WCS использует разделы реестра для сигнализации о возникновении определенных событий цветового профиля. Приложения должны запрашивать эти разделы реестра для обновленного состояния системного профиля цвета.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Цветовая система Windows (WCS), разделы реестра
- WCS (цветовая система Windows), разделы реестра
- Управление цветом изображений, разделы реестра
- Управление цветом, разделы реестра
- цвета, разделы реестра
- Справочник по WCS, разделы реестра
- Справочник по параметру WCS, разделам реестра
- Цветовая система Windows (WCS), реестр
- WCS (цветовая система Windows), реестр
- Управление цветом изображений, реестр
- Управление цветом, реестр
- цвета, реестр
- Справочник по WCS, реестр
- Справочник по WCS, реестру
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058ec839b226e96542604f151f06e2654a4180d5
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444675"
---
# <a name="wcs-registry-keys"></a><span data-ttu-id="4faf7-118">Разделы реестра WCS</span><span class="sxs-lookup"><span data-stu-id="4faf7-118">WCS Registry Keys</span></span>

<span data-ttu-id="4faf7-119">WCS использует разделы реестра для сигнализации о возникновении определенных событий цветового профиля.</span><span class="sxs-lookup"><span data-stu-id="4faf7-119">WCS uses registry keys to signal that certain color profile events have occurred.</span></span> <span data-ttu-id="4faf7-120">Приложения должны запрашивать эти разделы реестра для обновленного состояния системного профиля цвета.</span><span class="sxs-lookup"><span data-stu-id="4faf7-120">Apps should query these registry keys for updated system color profile state.</span></span>

## <a name="active-color-profile-changed"></a><span data-ttu-id="4faf7-121">Активный цветовой профиль изменен</span><span class="sxs-lookup"><span data-stu-id="4faf7-121">Active color profile changed</span></span>

<span data-ttu-id="4faf7-122">Приложениям может потребоваться реагирование на события изменения цветового профиля для устройства мониторинга. Это гарантирует, что у них всегда будет точная информация о цвете для целевого объекта, даже если пользователь или другое приложение изменило активный профиль для устройства.</span><span class="sxs-lookup"><span data-stu-id="4faf7-122">Apps may want to respond to color profile change events for a monitor device; this ensures that they always have accurate color information for their target, even if the user or another app has changed the active profile for the device.</span></span>

### <a name="desktop-applications"></a><span data-ttu-id="4faf7-123">Классические приложения</span><span class="sxs-lookup"><span data-stu-id="4faf7-123">Desktop applications</span></span>

<span data-ttu-id="4faf7-124">Классические приложения должны прослушивать изменения в реестре, чтобы определить, когда изменились связи цветового профиля с помощью [**регнотифичанжекэйвалуе**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span><span class="sxs-lookup"><span data-stu-id="4faf7-124">Desktop apps should listen for changes to the registry to determine when a color profile associations has changed using [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span></span> <span data-ttu-id="4faf7-125">Приложение должно регистрировать как для каждого пользователя, так и для изменения взаимосвязей профилей на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="4faf7-125">An app should register both for per-user profile association changes, and for system-wide changes.</span></span>

<span data-ttu-id="4faf7-126">[**Регнотифичанжекэйвалуе**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) следует инициализировать с помощью hKey, предоставленного функцией [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span><span class="sxs-lookup"><span data-stu-id="4faf7-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) should be initialized with an HKEY provided by [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span></span> <span data-ttu-id="4faf7-127">Параметр **RegOpenKeyEx** должен быть инициализирован с помощью следующих расположений в дереве реестра:</span><span class="sxs-lookup"><span data-stu-id="4faf7-127">**RegOpenKeyEx** should be initialized using the following registry tree locations:</span></span>



|    &nbsp;  |  &nbsp;      | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4faf7-128">Связи профилей отдельных пользователей</span><span class="sxs-lookup"><span data-stu-id="4faf7-128">Per-user profile associations</span></span>    | <span data-ttu-id="4faf7-129">**HKEY \_ текущее \_ ПОЛЬЗОВАТЕЛЬское программное обеспечение \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ профилеассоЦиатионс \\ Отображение \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}**</span><span class="sxs-lookup"><span data-stu-id="4faf7-129">**HKEY\_CURRENT\_USER SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ProfileAssociations\\Display\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span> |
| <span data-ttu-id="4faf7-130">Сопоставления профилей на уровне системы</span><span class="sxs-lookup"><span data-stu-id="4faf7-130">System-wide profile associations</span></span> | <span data-ttu-id="4faf7-131">**\_ \_ \\ Класс управления CurrentControlSet системы hKey локального компьютера \\ \\ \\ \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}**</span><span class="sxs-lookup"><span data-stu-id="4faf7-131">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Class\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span>                                        |



 

<span data-ttu-id="4faf7-132">Когда приложение уведомляется об изменении раздела реестра, сначала необходимо запросить, используются ли ассоциации для каждого пользователя или для всей системы, вызвав [**вксжетусеперусерпрофилес**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span><span class="sxs-lookup"><span data-stu-id="4faf7-132">When the app is notified of a registry key change, it should first query whether per-user or system-wide associations are being used by calling [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span></span> <span data-ttu-id="4faf7-133">Затем следует вызвать [**вксжетдефаултколорпрофиле**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) с правильным значением [**\_ \_ \_ области управления профилями WCS**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) , чтобы получить новый активный цветовой профиль для монитора.</span><span class="sxs-lookup"><span data-stu-id="4faf7-133">It should then call [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) with the right [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value to obtain the new active color profile for the monitor.</span></span> <span data-ttu-id="4faf7-134">Обратите внимание, что не все изменения разделов реестра соответствуют фактическому изменению текущего активного цветового профиля. приложение должен проверяет, действительно ли изменился профиль, возвращенный **вксжетдефаултколорпрофиле** .</span><span class="sxs-lookup"><span data-stu-id="4faf7-134">Note that not all registry key changes will correspond to an actual change in the currently active color profile; the app mush check whether the profile returned by **WcsGetDefaultColorProfile** has actually changed.</span></span>

### <a name="universal-windows-uwp-apps"></a><span data-ttu-id="4faf7-135">Приложения универсальной платформы Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="4faf7-135">Universal Windows (UWP) apps</span></span>

<span data-ttu-id="4faf7-136">Универсальные приложения для Windows не имеют доступа к указанным выше разделам реестра.</span><span class="sxs-lookup"><span data-stu-id="4faf7-136">Universal Windows Apps do not have access to the above registry keys.</span></span> <span data-ttu-id="4faf7-137">Вместо этого они должны зарегистрировать обработчик для события [**DisplayInformation. колорпрофилечанжед**](/uwp/api/Windows.Graphics.Display.DisplayInformation) .</span><span class="sxs-lookup"><span data-stu-id="4faf7-137">Instead, they should register a handler for the [**DisplayInformation.ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) event.</span></span> <span data-ttu-id="4faf7-138">Это событие вызывается при каждом изменении активного цветового профиля монитора, на котором выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="4faf7-138">This event fires whenever the active color profile for the monitor on which the application is running has changed.</span></span> <span data-ttu-id="4faf7-139">Колорпрофилечанжед учитывает, используются ли сопоставления профилей на уровне пользователя или системы. Эти сведения являются абстрактными от приложений UWP.</span><span class="sxs-lookup"><span data-stu-id="4faf7-139">ColorProfileChanged takes into account whether per-user or system-wide profile associations are being used; this information is abstracted from UWP apps.</span></span>

<span data-ttu-id="4faf7-140">При ответе на событие Колорпрофилечанжед приложение должно запрашивать текущий активный профиль с помощью [**DisplayInformation. жетколорпрофилеасинк**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span><span class="sxs-lookup"><span data-stu-id="4faf7-140">When responding to the ColorProfileChanged event, the app should query the currently active profile using [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span></span>

 

 