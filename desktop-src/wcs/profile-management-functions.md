---
title: Функции управления профилями
description: Функции управления профилями
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Цветовая система Windows (WCS), функции
- WCS (цветовая система Windows), функции
- Управление цветом изображений, функции
- Управление цветом, функции
- цвета, функции
- Справочник по WCS, функции
- Справочник по WCS, функциям
- Цветовая система Windows (WCS), профили
- WCS (цветовая система Windows), профили
- Управление цветом изображений, профили
- Управление цветом, профили
- цвета, профили
- Справочник по WCS, профили
- Справочник по WCS, профилям
- Управление профилями
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0e80e300532b20148eef6d9dc362438b6714a3
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "105719866"
---
# <a name="profile-management-functions"></a><span data-ttu-id="06cc6-118">Функции управления профилями</span><span class="sxs-lookup"><span data-stu-id="06cc6-118">Profile Management Functions</span></span>

## <a name="profile-management-functions"></a><span data-ttu-id="06cc6-119">Функции управления профилями</span><span class="sxs-lookup"><span data-stu-id="06cc6-119">Profile Management Functions</span></span>

<span data-ttu-id="06cc6-120">В управлении профилями полезны следующие функции API.</span><span class="sxs-lookup"><span data-stu-id="06cc6-120">The following API functions are useful in profile management.</span></span>



| <span data-ttu-id="06cc6-121">Функция</span><span class="sxs-lookup"><span data-stu-id="06cc6-121">Function</span></span>                                                                               | <span data-ttu-id="06cc6-122">Описание</span><span class="sxs-lookup"><span data-stu-id="06cc6-122">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06cc6-123">**ассоЦиатеколорпрофилевисдевицев**</span><span class="sxs-lookup"><span data-stu-id="06cc6-123">**AssociateColorProfileWithDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | <span data-ttu-id="06cc6-124">Связывает указанный цветовой профиль с указанным устройством.</span><span class="sxs-lookup"><span data-stu-id="06cc6-124">Associates a specified color profile with a specified device.</span></span>                                                              |
| <span data-ttu-id="06cc6-125">[**Креатепрофилефромлогколорспацев**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span><span class="sxs-lookup"><span data-stu-id="06cc6-125">[**CreateProfileFromLogColorSpaceW**]((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span></span> | <span data-ttu-id="06cc6-126">Преобразует логическое [пространство цветов](c.md) в [профиль устройства](d.md).</span><span class="sxs-lookup"><span data-stu-id="06cc6-126">Converts a logical [color space](c.md) to a [device profile](d.md).</span></span> |
| [<span data-ttu-id="06cc6-127">**дисассоЦиатеколорпрофилефромдевицев**</span><span class="sxs-lookup"><span data-stu-id="06cc6-127">**DisassociateColorProfileFromDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | <span data-ttu-id="06cc6-128">Отменяет связь указанного цветового профиля с указанным устройством на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="06cc6-128">Disassociates a specified color profile with a specified device on a specified computer.</span></span> |
| [<span data-ttu-id="06cc6-129">**енумколорпрофилесв**</span><span class="sxs-lookup"><span data-stu-id="06cc6-129">**EnumColorProfilesW**</span></span>](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | <span data-ttu-id="06cc6-130">Перечисляет все профили, удовлетворяющие заданным критериям перечисления.</span><span class="sxs-lookup"><span data-stu-id="06cc6-130">Enumerates all the profiles satisfying the given enumeration criteria.</span></span> |
| [<span data-ttu-id="06cc6-131">**жетколордиректорив**</span><span class="sxs-lookup"><span data-stu-id="06cc6-131">**GetColorDirectoryW**</span></span>](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | <span data-ttu-id="06cc6-132">Извлекает путь к каталогу цветов Windows на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="06cc6-132">Retrieves the path of the Windows COLOR directory on a specified machine.</span></span> |
| [<span data-ttu-id="06cc6-133">**жетдевицегаммарамп**</span><span class="sxs-lookup"><span data-stu-id="06cc6-133">**GetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | <span data-ttu-id="06cc6-134">Возвращает гамма-цвет из экранных плат с прямыми цветами.</span><span class="sxs-lookup"><span data-stu-id="06cc6-134">Gets the gamma ramp from direct color display boards.</span></span>                                                                                                |
| [<span data-ttu-id="06cc6-135">**жетстандардколорспацепрофилев**</span><span class="sxs-lookup"><span data-stu-id="06cc6-135">**GetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | <span data-ttu-id="06cc6-136">Извлекает цветовой профиль, зарегистрированный для указанного стандартного [цветового пространства](c.md).</span><span class="sxs-lookup"><span data-stu-id="06cc6-136">Retrieves the color profile registered for the specified standard [color space](c.md).</span></span> |
| [<span data-ttu-id="06cc6-137">**инсталлколорпрофилев**</span><span class="sxs-lookup"><span data-stu-id="06cc6-137">**InstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-installcolorprofilew) | <span data-ttu-id="06cc6-138">Устанавливает заданный профиль для использования на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="06cc6-138">Installs a given profile for use on a specified machine.</span></span> <span data-ttu-id="06cc6-139">Профиль также копируется в каталог цветов.</span><span class="sxs-lookup"><span data-stu-id="06cc6-139">The profile is also copied to the COLOR directory.</span></span> |
| [<span data-ttu-id="06cc6-140">**регистеркммв**</span><span class="sxs-lookup"><span data-stu-id="06cc6-140">**RegisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-registercmmw) | <span data-ttu-id="06cc6-141">Связывает указанное идентификационное значение с заданной библиотекой динамической компоновки модуля управления цветом (библиотека DLL CMM).</span><span class="sxs-lookup"><span data-stu-id="06cc6-141">Associates a specified identification value with the specified color management module dynamic link library (CMM DLL).</span></span> <span data-ttu-id="06cc6-142">Если этот идентификатор отображается в цветом профиле, Windows может затем выбрать соответствующий CMM, чтобы создать преобразование.</span><span class="sxs-lookup"><span data-stu-id="06cc6-142">When this ID appears in a color profile, Windows can then locate the corresponding CMM so as to create a transform.</span></span> |
| [<span data-ttu-id="06cc6-143">**сетдевицегаммарамп**</span><span class="sxs-lookup"><span data-stu-id="06cc6-143">**SetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | <span data-ttu-id="06cc6-144">Задает гамма-шкалу на экранах с прямыми цветными платами.</span><span class="sxs-lookup"><span data-stu-id="06cc6-144">Sets the gamma ramp on direct color display boards.</span></span>                                                                                                  |
| [<span data-ttu-id="06cc6-145">**сетстандардколорспацепрофилев**</span><span class="sxs-lookup"><span data-stu-id="06cc6-145">**SetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | <span data-ttu-id="06cc6-146">Регистрирует указанный профиль для заданного стандартного [цветового пространства](c.md).</span><span class="sxs-lookup"><span data-stu-id="06cc6-146">Registers a specified profile for a given standard [color space](c.md).</span></span> <span data-ttu-id="06cc6-147">Этот профиль можно запросить с помощью [жетстандардколорспацепрофилев](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span><span class="sxs-lookup"><span data-stu-id="06cc6-147">The profile can be queried using [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span></span> |
| [<span data-ttu-id="06cc6-148">**унинсталлколорпрофилев**</span><span class="sxs-lookup"><span data-stu-id="06cc6-148">**UninstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | <span data-ttu-id="06cc6-149">Удаляет указанный цветовой профиль с указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="06cc6-149">Removes a specified color profile from a specified computer.</span></span> <span data-ttu-id="06cc6-150">Связанные файлы при необходимости удаляются из системы.</span><span class="sxs-lookup"><span data-stu-id="06cc6-150">Associated files are optionally deleted from the system.</span></span> |
| [<span data-ttu-id="06cc6-151">**унрегистеркммв**</span><span class="sxs-lookup"><span data-stu-id="06cc6-151">**UnregisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-unregistercmmw) | <span data-ttu-id="06cc6-152">Отменяет связь указанного значения идентификатора из заданной библиотеки динамической компоновки модуля управления цветом (библиотека DLL CMM).</span><span class="sxs-lookup"><span data-stu-id="06cc6-152">Dissociates a specified ID value from a given color management module dynamic-link library (CMM DLL).</span></span> |
| [<span data-ttu-id="06cc6-153">**вксассоЦиатеколорпрофилевисдевице**</span><span class="sxs-lookup"><span data-stu-id="06cc6-153">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | <span data-ttu-id="06cc6-154">Связывает указанный цветовой профиль WCS с указанным устройством.</span><span class="sxs-lookup"><span data-stu-id="06cc6-154">Associates a specified WCS color profile with a specified device.</span></span>                                                                                    |
| [<span data-ttu-id="06cc6-155">**вкскреатеиккпрофиле**</span><span class="sxs-lookup"><span data-stu-id="06cc6-155">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | <span data-ttu-id="06cc6-156">Преобразует профиль WCS в профиль ICC.</span><span class="sxs-lookup"><span data-stu-id="06cc6-156">Converts a WCS profile into an ICC profile.</span></span>                                                                                                          |
| [<span data-ttu-id="06cc6-157">**вксдисассоЦиатеколорпрофилефромдевице**</span><span class="sxs-lookup"><span data-stu-id="06cc6-157">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | <span data-ttu-id="06cc6-158">Отменяет связь указанного цветового профиля WCS с указанным устройством на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="06cc6-158">Disassociates a specified WCS color profile with a specified device on a specified computer.</span></span>                                                         |
| [<span data-ttu-id="06cc6-159">**вксенумколорпрофилес**</span><span class="sxs-lookup"><span data-stu-id="06cc6-159">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | <span data-ttu-id="06cc6-160">Перечисляет все цветовые профили, удовлетворяющие критериям перечисления в указанной области управления профилями.</span><span class="sxs-lookup"><span data-stu-id="06cc6-160">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                       |
| [<span data-ttu-id="06cc6-161">**вксенумколорпрофилессизе**</span><span class="sxs-lookup"><span data-stu-id="06cc6-161">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | <span data-ttu-id="06cc6-162">Возвращает размер (в байтах) буфера, необходимого функции [**вксенумколорпрофилес**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) для перечисления цветовых профилей.</span><span class="sxs-lookup"><span data-stu-id="06cc6-162">Returns the size, in bytes, of the buffer required by the [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) function to enumerate color profiles.</span></span> |
| [<span data-ttu-id="06cc6-163">**вксжетдефаултколорпрофиле**</span><span class="sxs-lookup"><span data-stu-id="06cc6-163">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | <span data-ttu-id="06cc6-164">Извлекает профиль цвета по умолчанию для устройства или аппаратно-независимое значение по умолчанию, если устройство не указано.</span><span class="sxs-lookup"><span data-stu-id="06cc6-164">Retrieves the default color profile for a device, or the device-independent default if the device is not specified.</span></span>                                  |
| [<span data-ttu-id="06cc6-165">**вксжетдефаултколорпрофилесизе**</span><span class="sxs-lookup"><span data-stu-id="06cc6-165">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | <span data-ttu-id="06cc6-166">Возвращает размер (в байтах) имени профиля цвета по умолчанию для устройства, включая знак завершения **null** .</span><span class="sxs-lookup"><span data-stu-id="06cc6-166">Returns the size, in bytes, of the default color profile name for a device, including the **NULL** terminator.</span></span>                                       |
| [<span data-ttu-id="06cc6-167">**вксжетдефаултрендерингинтент**</span><span class="sxs-lookup"><span data-stu-id="06cc6-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="06cc6-168">Извлекает цель отрисовки по умолчанию в указанной области управления профилями.</span><span class="sxs-lookup"><span data-stu-id="06cc6-168">Retrieves the default rendering intent in the specified profile management scope.</span></span>                                                                    |
| [<span data-ttu-id="06cc6-169">**вксжетусеперусерпрофилес**</span><span class="sxs-lookup"><span data-stu-id="06cc6-169">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="06cc6-170">Определяет, будет ли пользователь использовать список ассоциаций профилей для каждого пользователя для указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="06cc6-170">Determines whether the user has chosen to use a per-user profile association list for the specified device.</span></span>                                          |
| [<span data-ttu-id="06cc6-171">**вксопенколорпрофилев**</span><span class="sxs-lookup"><span data-stu-id="06cc6-171">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | <span data-ttu-id="06cc6-172">Создает маркер для указанного цветового профиля.</span><span class="sxs-lookup"><span data-stu-id="06cc6-172">Creates a handle to a specified color profile.</span></span>                                                                                                       |
| [<span data-ttu-id="06cc6-173">**вкссетдефаултколорпрофиле**</span><span class="sxs-lookup"><span data-stu-id="06cc6-173">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | <span data-ttu-id="06cc6-174">Задает имя профиля цвета по умолчанию для указанного типа профиля в указанной области управления профилями.</span><span class="sxs-lookup"><span data-stu-id="06cc6-174">Sets the default color profile name of the specified profile type in the specified profile management scope.</span></span>                                         |
| [<span data-ttu-id="06cc6-175">**вкссетдефаултрендерингинтент**</span><span class="sxs-lookup"><span data-stu-id="06cc6-175">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | <span data-ttu-id="06cc6-176">Задает цель отрисовки по умолчанию в указанной области управления профилями.</span><span class="sxs-lookup"><span data-stu-id="06cc6-176">Sets the default rendering intent in the specified profile management scope.</span></span>                                                                         |
| [<span data-ttu-id="06cc6-177">**вкссетусеперусерпрофилес**</span><span class="sxs-lookup"><span data-stu-id="06cc6-177">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | <span data-ttu-id="06cc6-178">Позволяет пользователю указать, следует ли использовать список ассоциаций профилей для каждого пользователя для указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="06cc6-178">Allows the user to specify whether to use a per-user profile association list for the specified device.</span></span>                                              |



 

## <a name="profile-consumption-functions"></a><span data-ttu-id="06cc6-179">Функции использования профиля</span><span class="sxs-lookup"><span data-stu-id="06cc6-179">Profile Consumption Functions</span></span>

<span data-ttu-id="06cc6-180">Интерфейсы API потребления профиля — это API-интерфейсы в ICM2, которые принимают профили XML ICC или WCS, дескрипторы профилей или отрисовки в качестве параметров, а также набор новых интерфейсов API для поддержки профиля WCS для кода управления цветом приложения.</span><span class="sxs-lookup"><span data-stu-id="06cc6-180">The profile consumption APIs are those APIs in ICM2 that take ICC or WCS XML profiles, profile handles, or rendering intents as parameters, and a set of new APIs for WCS profile support for application color management code.</span></span>

 

## <a name="profiles-and-profile-management-functions"></a><span data-ttu-id="06cc6-181">Профили и функции управления профилями</span><span class="sxs-lookup"><span data-stu-id="06cc6-181">Profiles and Profile Management Functions</span></span>

<span data-ttu-id="06cc6-182">Рабочий процесс управления профилями основан на существующих API-интерфейсах ICM2, которые дополняются для предоставления дополнительных функциональных возможностей для пересмотра кода приложения.</span><span class="sxs-lookup"><span data-stu-id="06cc6-182">The profile management workflow is based on existing ICM2 APIs that are augmented to provide additional functionality for revising application code.</span></span>

<span data-ttu-id="06cc6-183">Профили содержат сведения, используемые алгоритмами обработки цветов для преобразования цветов между разными цветовыми пространствами.</span><span class="sxs-lookup"><span data-stu-id="06cc6-183">Profiles contain information used by color processing algorithms to translate color between different color spaces.</span></span> <span data-ttu-id="06cc6-184">Управление профилями позволяет запрашивать и указывать, какие профили используются на разных стадиях в модели обработки цветов для управления выходными цветами различных периферийных устройств с различными цветовыми характеристиками.</span><span class="sxs-lookup"><span data-stu-id="06cc6-184">Profile management provides a way to query and specify which profiles get used at different stages by the color processing model to manage color output of various peripheral devices with diverse color characteristics.</span></span>

<span data-ttu-id="06cc6-185">Управление профилями обеспечивает следующий набор функций:</span><span class="sxs-lookup"><span data-stu-id="06cc6-185">Profile management provides the following set of functionalities:</span></span>

 

1. <span data-ttu-id="06cc6-186">Установка цветовых профилей для использования в системе.</span><span class="sxs-lookup"><span data-stu-id="06cc6-186">Installing color profiles for use in the system.</span></span>

 

2. <span data-ttu-id="06cc6-187">Связывание одного или нескольких установленных цветовых профилей с любым конкретным устройством.</span><span class="sxs-lookup"><span data-stu-id="06cc6-187">Associating one or more installed color profiles with any particular device.</span></span>

 

3. <span data-ttu-id="06cc6-188">Выбор цветового профиля по умолчанию для конкретного типа в профилях, доступных для использования на определенном этапе обработки цветов.</span><span class="sxs-lookup"><span data-stu-id="06cc6-188">Choosing a default color profile of a particular type among the profiles available for use in a particular stage of color processing.</span></span> <span data-ttu-id="06cc6-189">Это может быть для устройства в отношении профилей, связанных с ним, или из профилей, установленных в системе, а не для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="06cc6-189">This could be for a device among the profiles associated with it, or among the profiles installed in the system and not device specific.</span></span>

 

4. <span data-ttu-id="06cc6-190">Перечисление цветовых профилей, удовлетворяющих определенным условиям, между профилями, установленными в системе.</span><span class="sxs-lookup"><span data-stu-id="06cc6-190">Enumerating color profiles that satisfy particular criteria among the profiles installed in the system.</span></span>

<span data-ttu-id="06cc6-191">Расширения файлов профиля WCS — это ". КДМП" для Дмпс, ". Camp" для Camp и ". ГММП" для Гммпс.</span><span class="sxs-lookup"><span data-stu-id="06cc6-191">The WCS profile filename extensions are ".cdmp" for DMPs, ".camp" for CAMPs, and ".gmmp" for GMMPs.</span></span>

 

<span data-ttu-id="06cc6-192">**Управление профилями для отдельных пользователей и включение выполнения в контексте LUA**</span><span class="sxs-lookup"><span data-stu-id="06cc6-192">**Per-user profile management and enabling execution in LUA context**</span></span>

<span data-ttu-id="06cc6-193">Цель проектирования, описанная в текущем документе, выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="06cc6-193">The goal of the design described in the current document is as follows:</span></span>

 

1. <span data-ttu-id="06cc6-194">Устаревшая реализация ICM2 не обеспечивает поддержку управления профилями для отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="06cc6-194">Legacy ICM2 implementation does not provide support for per-user profile management.</span></span> <span data-ttu-id="06cc6-195">Разные пользователи не могут иметь собственные параметры профиля.</span><span class="sxs-lookup"><span data-stu-id="06cc6-195">Different users cannot have their own profile settings.</span></span> <span data-ttu-id="06cc6-196">В Vista инфраструктура управления профилями WCS позволяет пользователям настраивать индивидуальные параметры профиля для большинства функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="06cc6-196">In Vista, the WCS profile management infrastructure enables users to configure individual profile settings for most functionalities.</span></span>

 

2. <span data-ttu-id="06cc6-197">Все устаревшие API-интерфейсы ICM2 управления профилями изменяют параметры всей системы и требуют прав администратора.</span><span class="sxs-lookup"><span data-stu-id="06cc6-197">All legacy ICM2 profile management APIs modify settings system-wide and require administrative privileges.</span></span> <span data-ttu-id="06cc6-198">В Windows Vista все пользователи работают в параметрах учетной записи пользователя с минимальными правами (LUA) большую часть времени, и администраторы могут выборочно повышать привилегии для запуска приложений, изменяющих параметры на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="06cc6-198">In Windows Vista, all users run in Least-privileged User Account (LUA) settings most of the time, and administrators can elevate privilege selectively to run applications that modify system-wide settings.</span></span> <span data-ttu-id="06cc6-199">В управлении профилями WCS все параметры профиля для каждого пользователя можно настроить в контексте LUA.</span><span class="sxs-lookup"><span data-stu-id="06cc6-199">In WCS profile management, all per-user profile settings are configurable in LUA context.</span></span> <span data-ttu-id="06cc6-200">Приложения управления профилями могут работать как параметры LUA, увеличивая их область использования и гарантируя, что безопасность системы не будет скомпрометирована.</span><span class="sxs-lookup"><span data-stu-id="06cc6-200">Profile management applications can run as LUA settings, increasing their scope of use and ensuring that security of the system is not compromised.</span></span>

<span data-ttu-id="06cc6-201">Управление профилями в Vista обеспечивает следующие улучшения по сравнению с устаревшей инфраструктурой ICM2:</span><span class="sxs-lookup"><span data-stu-id="06cc6-201">Profile management in Vista provides the following enhancements over legacy ICM2 infrastructure:</span></span>

 

1. <span data-ttu-id="06cc6-202">Он обеспечивает связь профилей с устройствами, параметрами профиля по умолчанию и перечислением профилей в области для отдельных пользователей и на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="06cc6-202">It enables profile association with devices, default profile settings, and enumeration of profiles in both per-user and system-wide scope.</span></span>

 

2. <span data-ttu-id="06cc6-203">Установка профиля остается в масштабе всей системы и требует прав администратора.</span><span class="sxs-lookup"><span data-stu-id="06cc6-203">Installing a profile remains system wide and requires administrator privileges.</span></span> <span data-ttu-id="06cc6-204">Это согласуется с установкой профиля во время установки устройства, так как установка устройства является всей системой и требует прав администратора.</span><span class="sxs-lookup"><span data-stu-id="06cc6-204">This is consistent with profile installation during device installation because device installation is system wide and requires administrative privileges.</span></span>

 

<span data-ttu-id="06cc6-205">Можно ли устанавливать устройства из контекста LUA, особенно для того, что поддерживается для этого класса устройства.</span><span class="sxs-lookup"><span data-stu-id="06cc6-205">Whether devices can be installed from LUA context is particular to what is supported for that class of device.</span></span> <span data-ttu-id="06cc6-206">Например, в Vista можно выполнить установку принтера из контекста LUA, если пользователю были предоставлены права на копирование файлов в хранилище драйверов администратором домена с помощью политик хранилища драйверов.</span><span class="sxs-lookup"><span data-stu-id="06cc6-206">For example, in Vista, it is possible to do printer installation from LUA context if the user has been granted rights to copy files into the driver store by a domain administrator using driver store policies.</span></span> <span data-ttu-id="06cc6-207">Инфраструктуре управления цветовым профилем не требуется выполнять никаких специальных действий, так как установка происходит в контексте диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="06cc6-207">Color profile management infrastructure doesn't need to do anything special in this regard since the installation happens in spooler context.</span></span>

 

3. <span data-ttu-id="06cc6-208">Изменение параметров профиля в области "на пользователя" может осуществляться в контексте LUA; изменения, необходимые для всей системы, требуют прав администратора.</span><span class="sxs-lookup"><span data-stu-id="06cc6-208">Modifying profile settings in per-user scope can be done in LUA context; system-wide modifications required administrative privileges.</span></span> <span data-ttu-id="06cc6-209">Операции управления профилями, для которых требуется чтение сведений о конфигурации, можно выполнять в контексте LUA как для отдельных пользователей, так и для всей системы.</span><span class="sxs-lookup"><span data-stu-id="06cc6-209">Profile management operations that require reading configuration information can be done in LUA context for both per-user and system-wide settings.</span></span>

<span data-ttu-id="06cc6-210">Область управления профилями указывает область выполняемых операций. для каждого пользователя или для всей системы.</span><span class="sxs-lookup"><span data-stu-id="06cc6-210">Profile management scope indicates the scope of the operations performed; either per-user or system wide.</span></span>

<span data-ttu-id="06cc6-211">Для каждой операции указывается, можно ли выполнять из контекста LUA.</span><span class="sxs-lookup"><span data-stu-id="06cc6-211">For each operation, it is indicated whether it can be done from LUA context.</span></span> <span data-ttu-id="06cc6-212">Если операция не может быть выполнена в контексте LUA, соответствующий API управления профилями возвращает ошибку с отказом в доступе.</span><span class="sxs-lookup"><span data-stu-id="06cc6-212">If an operation cannot be performed in LUA context, the corresponding profile management API returns failure with access denied.</span></span> <span data-ttu-id="06cc6-213">Приложения, использующие API, например панель управления цветом, могут предоставить пользователю возможность повысить права до контекста администрирования (с помощью OTS-или пользовательского интерфейса согласия), а затем вызвать API из контекста с повышенными привилегиями, чтобы операция была выполнена.</span><span class="sxs-lookup"><span data-stu-id="06cc6-213">Applications using the API, such as Color Management Control Panel, can enable the user to elevate to administrative context (using OTS or Consent UI), and then call the API from the elevated context so that the operation will succeed.</span></span>



<span data-ttu-id="06cc6-214">Операция</span><span class="sxs-lookup"><span data-stu-id="06cc6-214">Operation</span></span>

<span data-ttu-id="06cc6-215">Область управления профилями</span><span class="sxs-lookup"><span data-stu-id="06cc6-215">Profile Management Scope</span></span>

<span data-ttu-id="06cc6-216">Предварительное условие</span><span class="sxs-lookup"><span data-stu-id="06cc6-216">Pre-condition</span></span>

<span data-ttu-id="06cc6-217">Условие после</span><span class="sxs-lookup"><span data-stu-id="06cc6-217">Post-condition</span></span>

<span data-ttu-id="06cc6-218">Исполняемый файл в контексте LUA</span><span class="sxs-lookup"><span data-stu-id="06cc6-218">Executable in LUA context</span></span>

<span data-ttu-id="06cc6-219">$ {ROWSPAN2} $Install профиль $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="06cc6-219">${ROWSPAN2}$Install profile${REMOVE}$</span></span>  

<span data-ttu-id="06cc6-220">Для всей системы</span><span class="sxs-lookup"><span data-stu-id="06cc6-220">System wide</span></span>

<span data-ttu-id="06cc6-221">Профиль скопирован, установлен в систему и доступен для использования.</span><span class="sxs-lookup"><span data-stu-id="06cc6-221">Profile copied, installed into the system, and available for use.</span></span> <span data-ttu-id="06cc6-222">Профиль является перечислимым в области всей системы и текущего пользователя для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="06cc6-222">Profile is enumerable in system-wide and current-user scope for all users.</span></span>

<span data-ttu-id="06cc6-223">Во время установки драйвера устройства регулируется политиками установки драйверов.</span><span class="sxs-lookup"><span data-stu-id="06cc6-223">During device driver installation, governed by driver installation policies.</span></span> <span data-ttu-id="06cc6-224">Нет, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="06cc6-224">No, otherwise.</span></span>

<span data-ttu-id="06cc6-225">Текущий пользователь</span><span class="sxs-lookup"><span data-stu-id="06cc6-225">Current user</span></span>

<span data-ttu-id="06cc6-226">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="06cc6-226">Not supported</span></span>

<span data-ttu-id="06cc6-227">$ {ROWSPAN2} $Uninstall профиль $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="06cc6-227">${ROWSPAN2}$Uninstall profile${REMOVE}$</span></span>  

<span data-ttu-id="06cc6-228">Для всей системы</span><span class="sxs-lookup"><span data-stu-id="06cc6-228">System wide</span></span>

<span data-ttu-id="06cc6-229">Профиль установлен в системе</span><span class="sxs-lookup"><span data-stu-id="06cc6-229">Profile is installed in the system</span></span>

<span data-ttu-id="06cc6-230">Профиль удаляется из системы и при необходимости удаляется из хранилища профилей.</span><span class="sxs-lookup"><span data-stu-id="06cc6-230">Profile uninstalled from the system and optionally deleted from the profile store.</span></span> <span data-ttu-id="06cc6-231">Профиль больше недоступен для использования и не является перечислимым в какой-либо области.</span><span class="sxs-lookup"><span data-stu-id="06cc6-231">Profile is no longer available for use and is not enumerable in any scope.</span></span>

<span data-ttu-id="06cc6-232">Нет</span><span class="sxs-lookup"><span data-stu-id="06cc6-232">No</span></span>

<span data-ttu-id="06cc6-233">Текущий пользователь</span><span class="sxs-lookup"><span data-stu-id="06cc6-233">Current user</span></span>

<span data-ttu-id="06cc6-234">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="06cc6-234">Not supported</span></span>

<span data-ttu-id="06cc6-235">$ {ROWSPAN2} $Associate профиль с устройством $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="06cc6-235">${ROWSPAN2}$Associate profile with device${REMOVE}$</span></span>  

<span data-ttu-id="06cc6-236">Для всей системы</span><span class="sxs-lookup"><span data-stu-id="06cc6-236">System wide</span></span>

<span data-ttu-id="06cc6-237">Профиль установлен и имеет тип ICC или КДМП</span><span class="sxs-lookup"><span data-stu-id="06cc6-237">Profile is installed and is of type ICC or CDMP</span></span>

<span data-ttu-id="06cc6-238">Профиль доступен для использования на устройстве всеми пользователями.</span><span class="sxs-lookup"><span data-stu-id="06cc6-238">Profile is available for use with the device by all users.</span></span> <span data-ttu-id="06cc6-239">Это перечислимое значение, в области всей системы, а также в области текущего пользователя для всех пользователей, связанных с устройством.</span><span class="sxs-lookup"><span data-stu-id="06cc6-239">It is enumerable, in system-wide scope and also current-user scope for all users, as associated with the device.</span></span>

<span data-ttu-id="06cc6-240">Нет</span><span class="sxs-lookup"><span data-stu-id="06cc6-240">No</span></span>

<span data-ttu-id="06cc6-241">Текущий пользователь</span><span class="sxs-lookup"><span data-stu-id="06cc6-241">Current user</span></span>

<span data-ttu-id="06cc6-242">Профиль установлен.</span><span class="sxs-lookup"><span data-stu-id="06cc6-242">Profile is installed.</span></span> <span data-ttu-id="06cc6-243">Не имеет значения, был ли профиль уже связан с устройством в области всей системы и имеет тип ICC или КДМП.</span><span class="sxs-lookup"><span data-stu-id="06cc6-243">It does not matter whether the profile is already associated to the device in system-wide scope and is of type ICC or CDMP.</span></span>

<span data-ttu-id="06cc6-244">Профиль доступен для использования с устройством текущим пользователем.</span><span class="sxs-lookup"><span data-stu-id="06cc6-244">Profile is available for use with the device by current user.</span></span> <span data-ttu-id="06cc6-245">Он передается только в области текущего пользователя (кроме случаев, когда отсутствует связь на уровне системы), связанная с устройством.</span><span class="sxs-lookup"><span data-stu-id="06cc6-245">It is enumerable only in current-user scope (unless there is a system-wide association as well) as associated with the device.</span></span>

<span data-ttu-id="06cc6-246">Да</span><span class="sxs-lookup"><span data-stu-id="06cc6-246">Yes</span></span>

<span data-ttu-id="06cc6-247">$ {ROWSPAN2} $Disassociate профиль с устройства $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="06cc6-247">${ROWSPAN2}$Disassociate profile from device${REMOVE}$</span></span>  

<span data-ttu-id="06cc6-248">Для всей системы</span><span class="sxs-lookup"><span data-stu-id="06cc6-248">System wide</span></span>

<span data-ttu-id="06cc6-249">Профиль связан с устройством в области всей системы и имеет тип ICC или КДМП</span><span class="sxs-lookup"><span data-stu-id="06cc6-249">Profile is associated with the device in system-wide scope and is of type ICC or CDMP</span></span>

<span data-ttu-id="06cc6-250">Профиль больше не доступен для использования (за исключением пользователей с этой связью в области текущего пользователя).</span><span class="sxs-lookup"><span data-stu-id="06cc6-250">Profile is no longer available for use (except for users who have this association in their current-user scope as well).</span></span> <span data-ttu-id="06cc6-251">Он не является перечислимым в области всей системы.</span><span class="sxs-lookup"><span data-stu-id="06cc6-251">It is not enumerable in system-wide scope.</span></span> <span data-ttu-id="06cc6-252">Это может быть перечислимое в области текущего пользователя, но для пользователя, имеющего эту ассоциацию в своей области.</span><span class="sxs-lookup"><span data-stu-id="06cc6-252">It could be enumerable in current-user scope though, for a user who has this association in its scope.</span></span>

<span data-ttu-id="06cc6-253">Нет</span><span class="sxs-lookup"><span data-stu-id="06cc6-253">No</span></span>

<span data-ttu-id="06cc6-254">Текущий пользователь</span><span class="sxs-lookup"><span data-stu-id="06cc6-254">Current user</span></span>

<span data-ttu-id="06cc6-255">Профиль связан с устройством в области текущего пользователя (независимо от того, связан ли он с областью на уровне системы) и имеет тип ICC или КДМП.</span><span class="sxs-lookup"><span data-stu-id="06cc6-255">Profile is associated with the device in current-user scope (irrespective of whether it is associated in system-wide scope) and is of type ICC or CDMP.</span></span>

<span data-ttu-id="06cc6-256">Профиль больше не доступен для использования или перечислимый, как связанный с устройством, текущим пользователем (если он не связан с устройством в области всей системы).</span><span class="sxs-lookup"><span data-stu-id="06cc6-256">Profile is no longer available for use, or enumerable as associated to the device, by current user (unless it is also associated in system-wide scope to the device).</span></span>

<span data-ttu-id="06cc6-257">Да</span><span class="sxs-lookup"><span data-stu-id="06cc6-257">Yes</span></span>

<span data-ttu-id="06cc6-258">$ {ROWSPAN2} $Set профиль для типа (DMP или ICC) в качестве значения по умолчанию для устройства $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="06cc6-258">${ROWSPAN2}$Set profile for a type (DMP or ICC) as default for a device${REMOVE}$</span></span>  

<span data-ttu-id="06cc6-259">Для всей системы</span><span class="sxs-lookup"><span data-stu-id="06cc6-259">System wide</span></span>

<span data-ttu-id="06cc6-260">Профиль имеет тип ICC или КДМП</span><span class="sxs-lookup"><span data-stu-id="06cc6-260">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="06cc6-261">Профиль используется по умолчанию для конкретного типа устройства для всех пользователей, за исключением тех, кто переопределил этот параметр в области текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="06cc6-261">The profile is used by default, for the particular type with the device, for all users except for those who have overridden this setting in their current-user scope.</span></span> <span data-ttu-id="06cc6-262">(Профиль устанавливается и связывается с системой устройства, если это еще не так.)</span><span class="sxs-lookup"><span data-stu-id="06cc6-262">(The profile is installed and associated to the device system wide, if that is not already the case.)</span></span>

<span data-ttu-id="06cc6-263">Нет</span><span class="sxs-lookup"><span data-stu-id="06cc6-263">No</span></span>

<span data-ttu-id="06cc6-264">Текущий пользователь</span><span class="sxs-lookup"><span data-stu-id="06cc6-264">Current user</span></span>

<span data-ttu-id="06cc6-265">Профиль имеет тип ICC или КДМП</span><span class="sxs-lookup"><span data-stu-id="06cc6-265">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="06cc6-266">Профиль используется по умолчанию для конкретного типа с устройством в случае текущего пользователя, независимо от значения по умолчанию для всей системы.</span><span class="sxs-lookup"><span data-stu-id="06cc6-266">The profile is used by default for the particular type with the device in case of current user, irrespective of the system-wide default for this.</span></span> <span data-ttu-id="06cc6-267">(Если это еще не так, профиль устанавливается и связывается с устройством для текущего пользователя.)</span><span class="sxs-lookup"><span data-stu-id="06cc6-267">(The profile is installed and associated to the device for current user, if that is not already the case.)</span></span>

<span data-ttu-id="06cc6-268">Да, если профиль уже установлен</span><span class="sxs-lookup"><span data-stu-id="06cc6-268">Yes, if the profile is already installed</span></span>

<span data-ttu-id="06cc6-269">$ {ROWSPAN2} $Set профиль для типа (ICC, DMP, CAMP, ГММП) и комбинации подтипов как глобальное по умолчанию $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="06cc6-269">${ROWSPAN2}$Set profile for a type (ICC, DMP, CAMP, GMMP) and subtype combination as global default${REMOVE}$</span></span>  

<span data-ttu-id="06cc6-270">Для всей системы</span><span class="sxs-lookup"><span data-stu-id="06cc6-270">System wide</span></span>

<span data-ttu-id="06cc6-271">С устройствами могут быть связаны только профили ICC и КДМП.</span><span class="sxs-lookup"><span data-stu-id="06cc6-271">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="06cc6-272">Профиль используется по умолчанию для конкретного типа.</span><span class="sxs-lookup"><span data-stu-id="06cc6-272">The profile is used by default for the particular type.</span></span> <span data-ttu-id="06cc6-273">Пользователи могут переопределить этот параметр в области текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="06cc6-273">Users can override this setting in the current-user scope.</span></span> <span data-ttu-id="06cc6-274">(Профиль устанавливается, если это еще не так.)</span><span class="sxs-lookup"><span data-stu-id="06cc6-274">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="06cc6-275">Нет</span><span class="sxs-lookup"><span data-stu-id="06cc6-275">No</span></span>

<span data-ttu-id="06cc6-276">Текущий пользователь</span><span class="sxs-lookup"><span data-stu-id="06cc6-276">Current user</span></span>

<span data-ttu-id="06cc6-277">С устройствами могут быть связаны только профили ICC и КДМП.</span><span class="sxs-lookup"><span data-stu-id="06cc6-277">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="06cc6-278">Профиль используется по умолчанию для конкретного типа текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="06cc6-278">The profile is used by default for the particular type for current user.</span></span> <span data-ttu-id="06cc6-279">(Профиль устанавливается, если это еще не так.)</span><span class="sxs-lookup"><span data-stu-id="06cc6-279">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="06cc6-280">Да, если профиль уже установлен.</span><span class="sxs-lookup"><span data-stu-id="06cc6-280">Yes, if the profile is already installed.</span></span>

<span data-ttu-id="06cc6-281">$ {ROWSPAN2} $Erase Переопределение текущего пользователя для определенного параметра профиля по умолчанию, чтобы система всегда использовалась по умолчанию (в качестве резервной), даже для текущей области пользователя. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="06cc6-281">${ROWSPAN2}$Erase the current-user override for a particular default profile setting, so that the system default always gets used (as fallback) even for current-user scope.${REMOVE}$</span></span>  

<span data-ttu-id="06cc6-282">Для всей системы</span><span class="sxs-lookup"><span data-stu-id="06cc6-282">System wide</span></span>

<span data-ttu-id="06cc6-283">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="06cc6-283">Not applicable</span></span>

<span data-ttu-id="06cc6-284">Текущий пользователь</span><span class="sxs-lookup"><span data-stu-id="06cc6-284">Current user</span></span>

<span data-ttu-id="06cc6-285">Даже для запросов текущего пользователя о параметрах профиля по умолчанию для использования возвращаются параметры на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="06cc6-285">Even for current-user queries on default profile settings, system-wide settings are returned for use.</span></span>

<span data-ttu-id="06cc6-286">Да</span><span class="sxs-lookup"><span data-stu-id="06cc6-286">Yes</span></span>

<span data-ttu-id="06cc6-287">$ {ROWSPAN2} $Enumerate установленные профили, удовлетворяющие определенным критериям (например, класс устройства, класс профиля и т. д.). $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="06cc6-287">${ROWSPAN2}$Enumerate installed profiles satisfying particular criteria (like device class, profile class, etc.)${REMOVE}$</span></span>  

<span data-ttu-id="06cc6-288">Для всей системы</span><span class="sxs-lookup"><span data-stu-id="06cc6-288">System wide</span></span>

<span data-ttu-id="06cc6-289">Только профили ICC и КДМП можно связать и перечислить для устройств.</span><span class="sxs-lookup"><span data-stu-id="06cc6-289">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="06cc6-290">Устанавливаются профили, удовлетворяющие заданным условиям в области всей системы, перечислены.</span><span class="sxs-lookup"><span data-stu-id="06cc6-290">Profiles that are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="06cc6-291">Да</span><span class="sxs-lookup"><span data-stu-id="06cc6-291">Yes</span></span>

<span data-ttu-id="06cc6-292">Текущий пользователь</span><span class="sxs-lookup"><span data-stu-id="06cc6-292">Current user</span></span>

<span data-ttu-id="06cc6-293">Только профили ICC и КДМП могут быть связаны с устройствами и, следовательно, перечисляются для устройств.</span><span class="sxs-lookup"><span data-stu-id="06cc6-293">Only ICC and CDMP profiles can be associated with devices and thus enumerated for devices.</span></span>

<span data-ttu-id="06cc6-294">Установленные профили, удовлетворяющие заданным критериям в области всей системы, перечислены.</span><span class="sxs-lookup"><span data-stu-id="06cc6-294">Profiles which are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="06cc6-295">Да</span><span class="sxs-lookup"><span data-stu-id="06cc6-295">Yes</span></span>

<span data-ttu-id="06cc6-296">$ {ROWSPAN2} $Enumerate профили, связанные с определенным устройством, удовлетворяющие определенным критериям, например класс устройства и класс профиля $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="06cc6-296">${ROWSPAN2}$Enumerate profiles associated with a particular device satisfying particular criteria, such as device class, and profile class${REMOVE}$</span></span>  

<span data-ttu-id="06cc6-297">Для всей системы</span><span class="sxs-lookup"><span data-stu-id="06cc6-297">System wide</span></span>

<span data-ttu-id="06cc6-298">Только профили ICC и КДМП можно связать и перечислить для устройств.</span><span class="sxs-lookup"><span data-stu-id="06cc6-298">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="06cc6-299">Профили, связанные с устройством в области всей системы и удовлетворяющие заданным критериям в области всей системы, перечисляются.</span><span class="sxs-lookup"><span data-stu-id="06cc6-299">Profiles that are associated with the device in system-wide scope and satisfies the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="06cc6-300">Да</span><span class="sxs-lookup"><span data-stu-id="06cc6-300">Yes</span></span>

<span data-ttu-id="06cc6-301">Текущий пользователь</span><span class="sxs-lookup"><span data-stu-id="06cc6-301">Current user</span></span>

<span data-ttu-id="06cc6-302">Только профили ICC и КДМП можно связать и перечислить для устройств.</span><span class="sxs-lookup"><span data-stu-id="06cc6-302">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="06cc6-303">Профили, которые доступны в соответствии с устройством в области текущего пользователя, включая сопоставления на уровне системы и удовлетворяющие заданным условиям в области текущего пользователя, перечислены.</span><span class="sxs-lookup"><span data-stu-id="06cc6-303">Profiles that are available as associated with the device in current-user scope, which includes the system-wide associations and satisfies the specified criteria in current-user scope are enumerated.</span></span>

<span data-ttu-id="06cc6-304">Да</span><span class="sxs-lookup"><span data-stu-id="06cc6-304">Yes</span></span>



 

<span data-ttu-id="06cc6-305">Допустимые типы цветовых профилей предоставляются перечислением КОЛОРПРОФИЛЕТИПЕ.</span><span class="sxs-lookup"><span data-stu-id="06cc6-305">The valid color profile types are provided by the COLORPROFILETYPE enumeration.</span></span>

<span data-ttu-id="06cc6-306">Допустимые подтипы цветового профиля предоставляются перечислением КОЛОРПРОФИЛЕСУБТИПЕ.</span><span class="sxs-lookup"><span data-stu-id="06cc6-306">The valid color profile subtypes are provided by the COLORPROFILESUBTYPE enumeration.</span></span>

<span data-ttu-id="06cc6-307">Допустимые сочетания типа или подтипа профиля показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="06cc6-307">The valid profile type/subtype combinations are shown in the following table.</span></span>



<span data-ttu-id="06cc6-308">COLORPROFILETYPE </span><span class="sxs-lookup"><span data-stu-id="06cc6-308">COLORPROFILETYPE</span></span>

<span data-ttu-id="06cc6-309">Допустимый КОЛОРПРОФИЛЕСУБТИПЕ</span><span class="sxs-lookup"><span data-stu-id="06cc6-309">Valid COLORPROFILESUBTYPE</span></span>

<span data-ttu-id="06cc6-310">Примечания</span><span class="sxs-lookup"><span data-stu-id="06cc6-310">Notes</span></span>

<span data-ttu-id="06cc6-311">По умолчанию для устройства</span><span class="sxs-lookup"><span data-stu-id="06cc6-311">Device Default</span></span>

<span data-ttu-id="06cc6-312">Глобальное значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="06cc6-312">Global Default</span></span>

<span data-ttu-id="06cc6-313">Предполагаемое использование</span><span class="sxs-lookup"><span data-stu-id="06cc6-313">Intended Use</span></span>

<span data-ttu-id="06cc6-314">Предполагаемое использование</span><span class="sxs-lookup"><span data-stu-id="06cc6-314">Intended Use</span></span>

<span data-ttu-id="06cc6-315">КПТ \_ ICC</span><span class="sxs-lookup"><span data-stu-id="06cc6-315">CPT\_ICC</span></span>

<span data-ttu-id="06cc6-316">КПСТ \_ None</span><span class="sxs-lookup"><span data-stu-id="06cc6-316">CPST\_NONE</span></span>

<span data-ttu-id="06cc6-317">Получить или задать профиль ICC по умолчанию, связанный с устройством</span><span class="sxs-lookup"><span data-stu-id="06cc6-317">Get/Set default ICC profile associated with a device</span></span>

<span data-ttu-id="06cc6-318">КПСТ \_ ргбворкингспаце или КПСТ \_ кустомворкингспаце</span><span class="sxs-lookup"><span data-stu-id="06cc6-318">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="06cc6-319">Возвращает или задает профиль ICC в качестве глобального RGB или пользовательского профиля рабочего пространства.</span><span class="sxs-lookup"><span data-stu-id="06cc6-319">Get/Set ICC profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="06cc6-320">См. примечание.</span><span class="sxs-lookup"><span data-stu-id="06cc6-320">See Note.</span></span>

<span data-ttu-id="06cc6-321">КОЛОРПРОФИЛЕТИПЕ КПТ \_ ICC и КПТ DMP являются взаимоисключающими \_ .</span><span class="sxs-lookup"><span data-stu-id="06cc6-321">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="06cc6-322">Цветовой профиль по умолчанию, заданный для данного рабочего пространства (RGB или Custom), может быть либо профиль ICC, либо профиль DMP, но не оба.</span><span class="sxs-lookup"><span data-stu-id="06cc6-322">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>

<span data-ttu-id="06cc6-323">КПТ \_ DMP</span><span class="sxs-lookup"><span data-stu-id="06cc6-323">CPT\_DMP</span></span>

<span data-ttu-id="06cc6-324">КПСТ \_ None</span><span class="sxs-lookup"><span data-stu-id="06cc6-324">CPST\_NONE</span></span>

<span data-ttu-id="06cc6-325">Получение или Установка профиля по умолчанию DMP, связанного с устройством</span><span class="sxs-lookup"><span data-stu-id="06cc6-325">Get/Set default DMP profile associated with a device</span></span>

<span data-ttu-id="06cc6-326">КПСТ \_ ргбворкингспаце или КПСТ \_ кустомворкингспаце</span><span class="sxs-lookup"><span data-stu-id="06cc6-326">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="06cc6-327">Скачайте или установите профиль DMP в качестве глобального RGB или пользовательского профиля рабочего пространства.</span><span class="sxs-lookup"><span data-stu-id="06cc6-327">Get/Set DMP profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="06cc6-328">См. примечание.</span><span class="sxs-lookup"><span data-stu-id="06cc6-328">See Note.</span></span>

<span data-ttu-id="06cc6-329">КОЛОРПРОФИЛЕТИПЕ КПТ \_ ICC и КПТ DMP являются взаимоисключающими \_ .</span><span class="sxs-lookup"><span data-stu-id="06cc6-329">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="06cc6-330">Цветовой профиль по умолчанию, заданный для данного рабочего пространства (RGB или Custom), может быть либо профиль ICC, либо профиль DMP, но не оба.</span><span class="sxs-lookup"><span data-stu-id="06cc6-330">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>



 

> [!Note]  
> <span data-ttu-id="06cc6-331">Когда Вкссетдефаултколорпрофиле вызывается для установки профиля DMP в качестве профиля по умолчанию для рабочего пространства RGB или пользовательского рабочего пространства, допустим только профиль DMP с типом Ргбвиртуалдевице, LCD или CRT.</span><span class="sxs-lookup"><span data-stu-id="06cc6-331">When WcsSetDefaultColorProfile is called to set a DMP profile as the default profile for the RGB working space or a custom working space, only a DMP profile that is of type RGBVirtualDevice, LCD, or CRT is valid.</span></span>
>
>  
>
> <span data-ttu-id="06cc6-332">Когда Вкссетдефаултколорпрофиле вызывается для задания ICC-профиля в качестве профиля по умолчанию для рабочего пространства RGB или пользовательского рабочего пространства, только ICC-профиль, класс которого имеет значение "Спак" или "Дозапись", а цветовое пространство "RGB" является допустимым.</span><span class="sxs-lookup"><span data-stu-id="06cc6-332">When WcsSetDefaultColorProfile is called to set an ICC profile as the default profile for the RGB working space or a custom working space, only an ICC profile whose class is "spac" or "disp," and whose color space is "RGB" is valid.</span></span>

 

<span data-ttu-id="06cc6-333">Архитектура разработана в соответствии с требованиями операций, описанными в перечисленных выше перечислениях и таблицах.</span><span class="sxs-lookup"><span data-stu-id="06cc6-333">The architecture is designed according to the requirements of the operations as mentioned in the enumerations and tables above.</span></span>

### <a name="profile-management-public-api-layer"></a><span data-ttu-id="06cc6-334">Уровень общедоступного API управления профилями</span><span class="sxs-lookup"><span data-stu-id="06cc6-334">Profile management public API layer</span></span>

<span data-ttu-id="06cc6-335">Так как область управления профилями не поддерживается устаревшими API ICM2, необходимо создать новый набор API-интерфейсов управления профилями WCS, который определяет область управления профилями как для всей системы, так и для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="06cc6-335">Because profile management scope is not supported by legacy ICM2 APIs, a new set of WCS profile management APIs is required that defines profile management scope as system wide or current user.</span></span> <span data-ttu-id="06cc6-336">?</span><span class="sxs-lookup"><span data-stu-id="06cc6-336">?</span></span> <span data-ttu-id="06cc6-337">Устаревшие API ICM2 по-прежнему поддерживаются для обратной совместимости и работают с областью управления профилями, которая является неявной для вызова.</span><span class="sxs-lookup"><span data-stu-id="06cc6-337">Legacy ICM2 APIs continue to be supported for backward compatibility, and work on profile management scope that is implicit for the call.</span></span> <span data-ttu-id="06cc6-338">o ICM2 API-интерфейсы, работающие с текущей областью пользователя?</span><span class="sxs-lookup"><span data-stu-id="06cc6-338">o ICM2 APIs that work on current-user scope ?</span></span> <span data-ttu-id="06cc6-339">Это относится к операциям, которые поддерживаются как для всей системы, так и для текущего пользователя в управлении профилями WCS.</span><span class="sxs-lookup"><span data-stu-id="06cc6-339">This is for operations that are supported for both system wide and current-user scope in WCS profile management.</span></span> <span data-ttu-id="06cc6-340">Устаревшие API ICM2 вызывают новые API-интерфейсы WCS с областью управления профилями в качестве текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="06cc6-340">Legacy ICM2 APIs call on new WCS APIs with profile management scope as current user.</span></span> <span data-ttu-id="06cc6-341">Это имеет смысл с точки зрения пользователя, так как это позволяет применять параметры для каждого пользователя из устаревших приложений, а также выполнять большинство операций в контексте LUA.</span><span class="sxs-lookup"><span data-stu-id="06cc6-341">This makes sense from user perspective because this enables per-user settings from legacy applications and also executing most of the operations in LUA context.</span></span> <span data-ttu-id="06cc6-342">o ICM2 API-интерфейсы, работающие в области всей системы?</span><span class="sxs-lookup"><span data-stu-id="06cc6-342">o ICM2 APIs that work on system-wide scope ?</span></span> <span data-ttu-id="06cc6-343">Это относится к операциям (Установка профилей и профилей удаления), поддерживающих только область всей системы.</span><span class="sxs-lookup"><span data-stu-id="06cc6-343">This is for operations (install profiles and uninstall profiles) that support only system-wide scope.</span></span> <span data-ttu-id="06cc6-344">Новые API-интерфейсы управления профилями WCS не создаются, и существующие API-интерфейсы могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="06cc6-344">No new WCS profile management APIs are created and existing APIs can be modified.</span></span>

<span data-ttu-id="06cc6-345">Базовые реализации операций управления профилями работают со следующими сущностями данных конфигурации для создания контекста для алгоритмов цветовой обработки, обеспечивающих функциональные возможности управления цветом.</span><span class="sxs-lookup"><span data-stu-id="06cc6-345">The underlying implementations of the profile management operations work on the following configuration data entities to create the context for color processing algorithms to provide color management functionalities.</span></span> <span data-ttu-id="06cc6-346">Они относятся либо к устройствам, либо к глобальным (независимо от устройства) параметрам.</span><span class="sxs-lookup"><span data-stu-id="06cc6-346">They are either device specific or global (device independent) settings.</span></span> <span data-ttu-id="06cc6-347">выводить данные конфигурации для конкретных устройств:?</span><span class="sxs-lookup"><span data-stu-id="06cc6-347">o Device specific configuration data: ?</span></span> <span data-ttu-id="06cc6-348">Список профилей, связанных с определенным устройством.</span><span class="sxs-lookup"><span data-stu-id="06cc6-348">List of profiles associated with a particular device.</span></span> <span data-ttu-id="06cc6-349">?</span><span class="sxs-lookup"><span data-stu-id="06cc6-349">?</span></span> <span data-ttu-id="06cc6-350">Профиль по умолчанию для различных типов профилей, связанных с устройством.</span><span class="sxs-lookup"><span data-stu-id="06cc6-350">Default profile for different profile types associated with a device.</span></span> <span data-ttu-id="06cc6-351">?</span><span class="sxs-lookup"><span data-stu-id="06cc6-351">?</span></span> <span data-ttu-id="06cc6-352">Режим сопоставления профилей, используемых для перечисления.</span><span class="sxs-lookup"><span data-stu-id="06cc6-352">Matching mode of profiles used for enumeration.</span></span> <span data-ttu-id="06cc6-353">o глобальные данные конфигурации:?</span><span class="sxs-lookup"><span data-stu-id="06cc6-353">o Global configuration data: ?</span></span> <span data-ttu-id="06cc6-354">Список профилей, установленных в системе.</span><span class="sxs-lookup"><span data-stu-id="06cc6-354">List of profiles installed in the system.</span></span> <span data-ttu-id="06cc6-355">?</span><span class="sxs-lookup"><span data-stu-id="06cc6-355">?</span></span> <span data-ttu-id="06cc6-356">Глобальный профиль по умолчанию для различных типов профилей.</span><span class="sxs-lookup"><span data-stu-id="06cc6-356">Global default profile for different profile types.</span></span> <span data-ttu-id="06cc6-357">?</span><span class="sxs-lookup"><span data-stu-id="06cc6-357">?</span></span> <span data-ttu-id="06cc6-358">Базовые реализации хранилища данных конфигурации занимают область хранения для данных конфигурации (независимо от устройства или конкретного устройства), который может быть либо общесистемным, либо текущим пользователем.</span><span class="sxs-lookup"><span data-stu-id="06cc6-358">The underlying implementations of configuration data storage take in storage scope for configuration data (either device independent or device specific), which can be either system wide or current user.</span></span> <span data-ttu-id="06cc6-359">Это отличается от области управления профилями.</span><span class="sxs-lookup"><span data-stu-id="06cc6-359">This is different from profile management scope.</span></span> <span data-ttu-id="06cc6-360">Операция с областью управления профилями текущего пользователя может вызвать чтение из области хранения на уровне системы, если параметр текущего пользователя для этой операции отсутствует.</span><span class="sxs-lookup"><span data-stu-id="06cc6-360">An operation with current-user profile management scope can cause a read from a system-wide storage scope if the current-user setting for that operation is not present.</span></span> <span data-ttu-id="06cc6-361">?</span><span class="sxs-lookup"><span data-stu-id="06cc6-361">?</span></span> <span data-ttu-id="06cc6-362">Уровень API ICM2/WCS вызывает на этом уровне хранилища для получения и настройки данных с соответствующей областью хранения.</span><span class="sxs-lookup"><span data-stu-id="06cc6-362">The ICM2/WCS API layer calls in this storage layer for getting and setting data with appropriate storage scope.</span></span> <span data-ttu-id="06cc6-363">Уровень хранилища прозрачен для области управления профилями.</span><span class="sxs-lookup"><span data-stu-id="06cc6-363">The storage layer is transparent to profile management scope.</span></span> <span data-ttu-id="06cc6-364">Логика для объединения данных из областей хранения текущего пользователя и всей системы для создания или обновления конфигурации в соответствии с областью управления профилями, заданной вызывающим объектом API.</span><span class="sxs-lookup"><span data-stu-id="06cc6-364">The logic for combining data from current-user and system-wide storage scopes to create or update a configuration according to the profile management scope specified by the API caller.</span></span> <span data-ttu-id="06cc6-365">Эта логика имеется на уровне API ICM2/WCS.</span><span class="sxs-lookup"><span data-stu-id="06cc6-365">This logic is present in the ICM2/WCS API layer.</span></span>

### <a name="device-specific-storage-layer"></a><span data-ttu-id="06cc6-366">Уровень хранилища для конкретного устройства</span><span class="sxs-lookup"><span data-stu-id="06cc6-366">Device-specific storage layer</span></span>

<span data-ttu-id="06cc6-367">Хранилище для различных классов устройств, таких как печать, захват или отображение, может отличаться друг от друга.</span><span class="sxs-lookup"><span data-stu-id="06cc6-367">The storage for different classes of devices like print, capture or display could be different from each other.</span></span> <span data-ttu-id="06cc6-368">Например, данные конфигурации для устройства печати должны храниться с помощью стандартных API печати, таких как Сетпринтердатаекс и Жетпринтердатаекс, чтобы включить копирование профилей и параметров для передачи на клиентский компьютер во время подключения «точка-печать».</span><span class="sxs-lookup"><span data-stu-id="06cc6-368">For example, configuration data for a print device must be stored using standard print APIs, such as SetPrinterDataEx and GetPrinterDataEx, to enable the profiles to be copied and settings to be transferred to a client machine during Point-and-Print connection.</span></span> <span data-ttu-id="06cc6-369">?</span><span class="sxs-lookup"><span data-stu-id="06cc6-369">?</span></span> <span data-ttu-id="06cc6-370">Этот слой экспортирует функциональные возможности для открытия хранилища, получения данных, настройки данных и закрытия хранилища с помощью стандартных предварительно определенных интерфейсов, чтобы уровень хранилища конфигурации управления профилями мог вызывать их, в то время как они прозрачны для сохранения данных для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="06cc6-370">This layer exports functionality to open store, get data, set data and close store using common pre-defined interfaces so that the profile management configuration storage layer can call into them while being transparent to the way the data gets stored for that device.</span></span>

<span data-ttu-id="06cc6-371">Эта архитектура показана на следующей диаграмме.</span><span class="sxs-lookup"><span data-stu-id="06cc6-371">The following diagram illustrates this architecture.</span></span>



<span data-ttu-id="06cc6-372">Уровень общедоступного API управления профилями</span><span class="sxs-lookup"><span data-stu-id="06cc6-372">Profile Management Public API Layer</span></span>

<span data-ttu-id="06cc6-373">$ {ROWSPAN2} $Legacy ICM2 API для операций, которые поддерживают только область управления профилем на уровне системы в Vista (установка, удаление и получение каталога цветов).</span><span class="sxs-lookup"><span data-stu-id="06cc6-373">${ROWSPAN2}$Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista (install, uninstall, and get color directory).</span></span> <span data-ttu-id="06cc6-374">Они вызывают уровень хранилища конфигурации с соответствующей областью хранения. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="06cc6-374">They call the configuration storage layer with appropriate storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="06cc6-375">Устаревший API ICM2 для операций, поддерживающих область управления профилями уровня системы и текущего пользователя в Vista (все операции, Кроме установки, удаления и получения каталога цветов).</span><span class="sxs-lookup"><span data-stu-id="06cc6-375">Legacy ICM2 API for operations that support both system-wide and current-user profile management scope in Vista (all operations other than install, uninstall, and get color directory).</span></span> <span data-ttu-id="06cc6-376">Они неявно работают с текущей областью действия пользователя и вызывают новый API WCS с областью управления профилями в качестве текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="06cc6-376">They implicitly work on current-user scope, and call into new WCS API with profile management scope as current user.</span></span>

<span data-ttu-id="06cc6-377">Новый API-интерфейс WCS с поддержкой области управления профилями на уровне системы и текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="06cc6-377">New WCS API with system-wide and current-user profile management scope support.</span></span> <span data-ttu-id="06cc6-378">Они вызывают уровень хранилища конфигурации с соответствующей областью хранения.</span><span class="sxs-lookup"><span data-stu-id="06cc6-378">They call the configuration storage layer with appropriate storage scope.</span></span>



 



<span data-ttu-id="06cc6-379">Уровень хранилища конфигурации управления профилями</span><span class="sxs-lookup"><span data-stu-id="06cc6-379">Profile Management Configuration Storage Layer</span></span>

<span data-ttu-id="06cc6-380">Универсальные программы глобальной конфигурации, независимые от устройства</span><span class="sxs-lookup"><span data-stu-id="06cc6-380">Device-independent global configuration routines</span></span>

<span data-ttu-id="06cc6-381">Подпрограммы конфигурации для конкретных устройств</span><span class="sxs-lookup"><span data-stu-id="06cc6-381">Device-specific configuration routines</span></span>

<span data-ttu-id="06cc6-382">$ {ROWSPAN3} $Profile Установка и аппаратно-независимое управление параметрами профиля, поддерживаемое в области хранения на уровне системы и текущего пользователя. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="06cc6-382">${ROWSPAN3}$Profile installation and device-independent default profile settings management, supported in system-wide and current-user storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="06cc6-383">Сопоставление устройств и управление параметрами профиля по умолчанию для конкретных устройств, поддерживаемое в масштабах всей системы и в области хранения текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="06cc6-383">Device association and device-specific default profile settings management, supported in system-wide and current-user storage scope.</span></span>

<span data-ttu-id="06cc6-384">Уровень хранилища Device-Specific</span><span class="sxs-lookup"><span data-stu-id="06cc6-384">Device-Specific Storage layer</span></span>

<span data-ttu-id="06cc6-385">Печать конкретного хранилища</span><span class="sxs-lookup"><span data-stu-id="06cc6-385">Print specific storage</span></span>

<span data-ttu-id="06cc6-386">Отображение конкретного хранилища</span><span class="sxs-lookup"><span data-stu-id="06cc6-386">Display specific storage</span></span>

<span data-ttu-id="06cc6-387">Записать определенное хранилище</span><span class="sxs-lookup"><span data-stu-id="06cc6-387">Capture specific storage</span></span>



 

<span data-ttu-id="06cc6-388">Устаревшие API ICM2 для операций, которые поддерживают только область управления профилем на уровне системы в Vista, не имеют изменений в поведении.</span><span class="sxs-lookup"><span data-stu-id="06cc6-388">Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista have no changes in behavior.</span></span> <span data-ttu-id="06cc6-389">Операции установки и удаления попадают в эту категорию.</span><span class="sxs-lookup"><span data-stu-id="06cc6-389">Install and uninstall operations fall in this category.</span></span>

<span data-ttu-id="06cc6-390">Устаревшие API-интерфейсы ICM2 для операций, которые поддерживают область управления профилями уровня системы и текущего пользователя, заменяют поведение для запроса и настройки текущих параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="06cc6-390">Legacy ICM2 APIs for operations that support both system-wide and current-user profile management scope have their behavior changed to query and configure current-user settings.</span></span> <span data-ttu-id="06cc6-391">Все операции, отличные от install и Uninstall, попадают в эту категорию.</span><span class="sxs-lookup"><span data-stu-id="06cc6-391">All operations other than install and uninstall fall in this category.</span></span>

 

 




