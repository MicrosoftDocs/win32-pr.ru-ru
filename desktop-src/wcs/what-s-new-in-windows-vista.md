---
title: Что нового в Windows Vista
description: Версия 1,0 для управления цветом изображений (ICM) была предоставлена в Microsoft Windows 95 и предоставляет базовые возможности управления цветом в контекстах устройств Windows.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Цветовая система Windows (WCS), Windows Vista
- WCS (цветовая система Windows), Windows Vista
- Управление цветом изображений, Windows Vista
- Управление цветом, Windows Vista
- цвета, Windows Vista
- Цветовая система Windows (WCS), операционные системы
- WCS (цветовая система Windows), операционные системы
- Управление цветом изображений, операционные системы
- Управление цветом, операционные системы
- цвета, операционные системы
- ICM (Image Color Management — управление цветом изображений)
- ICM (Управление цветом изображений)
- Управление цветом Windows Vista
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "105719865"
---
# <a name="whats-new-in-windows-vista"></a><span data-ttu-id="52cc3-116">Что нового в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52cc3-116">What's New in Windows Vista</span></span>

<span data-ttu-id="52cc3-117">Версия 1,0 для управления цветом изображений (ICM) была предоставлена в Microsoft Windows 95 и предоставляет базовые возможности управления цветом в контекстах устройств Windows.</span><span class="sxs-lookup"><span data-stu-id="52cc3-117">Version 1.0 of Image Color Management (ICM) was delivered in Microsoft Windows 95, and provides basic color management capabilities within Windows device contexts.</span></span>

<span data-ttu-id="52cc3-118">ICM версии 2,0 была предоставлена в Windows 98, Windows Millennium Edition, Windows 2000 и WindowsXP и включал ряд новых функций, реализующих управление цветом за пределами контекстов устройств.</span><span class="sxs-lookup"><span data-stu-id="52cc3-118">ICM version 2.0 was delivered in Windows 98, Windows Millennium Edition, Windows 2000, and WindowsXP and included a variety of new functions that implemented color management outside of device contexts.</span></span> <span data-ttu-id="52cc3-119">Эти новые функции подходят для более требовательных требований к управлению цветом, а приложения имеют больший контроль над процессом управления цветом.</span><span class="sxs-lookup"><span data-stu-id="52cc3-119">These new functions were suitable for more demanding color management requirements, and gave applications greater control over the color-management process.</span></span>

<span data-ttu-id="52cc3-120">С выпуском Windows Vista ICM 2,0 теперь включен в цветовую систему Windows (WCS) 1,0, что расширяет функциональность.</span><span class="sxs-lookup"><span data-stu-id="52cc3-120">With the release of Windows Vista, ICM 2.0 is now included in Windows Color System (WCS) 1.0, which adds more functionality.</span></span> <span data-ttu-id="52cc3-121">В следующей таблице перечислены новые прикладные программные интерфейсы (API), поставляемые в составе Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52cc3-121">The following table lists new application programming interfaces (API) that ship in Windows Vista.</span></span>

## <a name="new-api-shipping-in-windows-vista"></a><span data-ttu-id="52cc3-122">Новая доставка API в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52cc3-122">New API Shipping in Windows Vista</span></span>



<span data-ttu-id="52cc3-123">Перечисления</span><span class="sxs-lookup"><span data-stu-id="52cc3-123">Enumerations</span></span>

<span data-ttu-id="52cc3-124">Имя API</span><span class="sxs-lookup"><span data-stu-id="52cc3-124">API Name</span></span>

<span data-ttu-id="52cc3-125">Header</span><span class="sxs-lookup"><span data-stu-id="52cc3-125">Header</span></span>

<span data-ttu-id="52cc3-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="52cc3-126">Library</span></span>

[<span data-ttu-id="52cc3-127">**колордататипе**</span><span class="sxs-lookup"><span data-stu-id="52cc3-127">**COLORDATATYPE**</span></span>](/windows/win32/api/icm/ne-icm-colordatatype)

<span data-ttu-id="52cc3-128">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-128">icm.h</span></span>

<span data-ttu-id="52cc3-129">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-129">mscms.lib</span></span>

[<span data-ttu-id="52cc3-130">**колорпрофилесубтипе**</span><span class="sxs-lookup"><span data-stu-id="52cc3-130">**COLORPROFILESUBTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

<span data-ttu-id="52cc3-131">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-131">icm.h</span></span>

<span data-ttu-id="52cc3-132">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-132">mscms.lib</span></span>

[<span data-ttu-id="52cc3-133">**колорпрофилетипе**</span><span class="sxs-lookup"><span data-stu-id="52cc3-133">**COLORPROFILETYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofiletype)

<span data-ttu-id="52cc3-134">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-134">icm.h</span></span>

<span data-ttu-id="52cc3-135">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-135">mscms.lib</span></span>

[<span data-ttu-id="52cc3-136">**\_область управления профилями WCS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52cc3-136">**WCS\_PROFILE\_MANAGEMENT\_SCOPE**</span></span>](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

<span data-ttu-id="52cc3-137">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-137">icm.h</span></span>

<span data-ttu-id="52cc3-138">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-138">mscms.lib</span></span>



 



<span data-ttu-id="52cc3-139">Функции</span><span class="sxs-lookup"><span data-stu-id="52cc3-139">Functions</span></span>

<span data-ttu-id="52cc3-140">Имя API</span><span class="sxs-lookup"><span data-stu-id="52cc3-140">API Name</span></span>

<span data-ttu-id="52cc3-141">Header</span><span class="sxs-lookup"><span data-stu-id="52cc3-141">Header</span></span>

<span data-ttu-id="52cc3-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="52cc3-142">Library</span></span>

[<span data-ttu-id="52cc3-143">**вксассоЦиатеколорпрофилевисдевице**</span><span class="sxs-lookup"><span data-stu-id="52cc3-143">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="52cc3-144">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-144">icm.h</span></span>

<span data-ttu-id="52cc3-145">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-145">mscms.lib</span></span>

[<span data-ttu-id="52cc3-146">**вксчеккколорс**</span><span class="sxs-lookup"><span data-stu-id="52cc3-146">**WcsCheckColors**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="52cc3-147">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-147">icm.h</span></span>

<span data-ttu-id="52cc3-148">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-148">mscms.lib</span></span>

[<span data-ttu-id="52cc3-149">**вкскреатеиккпрофиле**</span><span class="sxs-lookup"><span data-stu-id="52cc3-149">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

<span data-ttu-id="52cc3-150">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-150">icm.h</span></span>

<span data-ttu-id="52cc3-151">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-151">mscms.lib</span></span>

[<span data-ttu-id="52cc3-152">**вксдисассоЦиатеколорпрофилефромдевице**</span><span class="sxs-lookup"><span data-stu-id="52cc3-152">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

<span data-ttu-id="52cc3-153">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-153">icm.h</span></span>

<span data-ttu-id="52cc3-154">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-154">mscms.lib</span></span>

[<span data-ttu-id="52cc3-155">**вксенумколорпрофилес**</span><span class="sxs-lookup"><span data-stu-id="52cc3-155">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

<span data-ttu-id="52cc3-156">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-156">icm.h</span></span>

<span data-ttu-id="52cc3-157">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-157">mscms.lib</span></span>

[<span data-ttu-id="52cc3-158">**вксенумколорпрофилессизе**</span><span class="sxs-lookup"><span data-stu-id="52cc3-158">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

<span data-ttu-id="52cc3-159">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-159">icm.h</span></span>

<span data-ttu-id="52cc3-160">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-160">mscms.lib</span></span>

[<span data-ttu-id="52cc3-161">**вксжетдефаултколорпрофиле**</span><span class="sxs-lookup"><span data-stu-id="52cc3-161">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

<span data-ttu-id="52cc3-162">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-162">icm.h</span></span>

<span data-ttu-id="52cc3-163">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-163">mscms.lib</span></span>

[<span data-ttu-id="52cc3-164">**вксжетдефаултколорпрофилесизе**</span><span class="sxs-lookup"><span data-stu-id="52cc3-164">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

<span data-ttu-id="52cc3-165">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-165">icm.h</span></span>

<span data-ttu-id="52cc3-166">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-166">mscms.lib</span></span>

[<span data-ttu-id="52cc3-167">**вксжетдефаултрендерингинтент**</span><span class="sxs-lookup"><span data-stu-id="52cc3-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="52cc3-168">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-168">icm.h</span></span>

<span data-ttu-id="52cc3-169">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-169">mscms.lib</span></span>

[<span data-ttu-id="52cc3-170">**вксжетусеперусерпрофилес**</span><span class="sxs-lookup"><span data-stu-id="52cc3-170">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="52cc3-171">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-171">icm.h</span></span>

<span data-ttu-id="52cc3-172">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-172">mscms.lib</span></span>

[<span data-ttu-id="52cc3-173">**вксопенколорпрофилев**</span><span class="sxs-lookup"><span data-stu-id="52cc3-173">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

<span data-ttu-id="52cc3-174">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-174">icm.h</span></span>

<span data-ttu-id="52cc3-175">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-175">mscms.lib</span></span>

[<span data-ttu-id="52cc3-176">**вкссетдефаултколорпрофиле**</span><span class="sxs-lookup"><span data-stu-id="52cc3-176">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

<span data-ttu-id="52cc3-177">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-177">icm.h</span></span>

<span data-ttu-id="52cc3-178">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-178">mscms.lib</span></span>

[<span data-ttu-id="52cc3-179">**вкссетдефаултрендерингинтент**</span><span class="sxs-lookup"><span data-stu-id="52cc3-179">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

<span data-ttu-id="52cc3-180">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-180">icm.h</span></span>

<span data-ttu-id="52cc3-181">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-181">mscms.lib</span></span>

[<span data-ttu-id="52cc3-182">**вкссетусеперусерпрофилес**</span><span class="sxs-lookup"><span data-stu-id="52cc3-182">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

<span data-ttu-id="52cc3-183">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-183">icm.h</span></span>

<span data-ttu-id="52cc3-184">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-184">mscms.lib</span></span>

[<span data-ttu-id="52cc3-185">**вкстранслатеколорс**</span><span class="sxs-lookup"><span data-stu-id="52cc3-185">**WcsTranslateColors**</span></span>](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

<span data-ttu-id="52cc3-186">ICM. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-186">icm.h</span></span>

<span data-ttu-id="52cc3-187">мскмс. lib</span><span class="sxs-lookup"><span data-stu-id="52cc3-187">mscms.lib</span></span>



 



<span data-ttu-id="52cc3-188">Интерфейсы и их функции</span><span class="sxs-lookup"><span data-stu-id="52cc3-188">Interfaces and Their Functions</span></span>

<span data-ttu-id="52cc3-189">Имя API</span><span class="sxs-lookup"><span data-stu-id="52cc3-189">API Name</span></span>

<span data-ttu-id="52cc3-190">Header</span><span class="sxs-lookup"><span data-stu-id="52cc3-190">Header</span></span>

<span data-ttu-id="52cc3-191">Библиотека</span><span class="sxs-lookup"><span data-stu-id="52cc3-191">Library</span></span>

[<span data-ttu-id="52cc3-192">**идевицемоделплугин**</span><span class="sxs-lookup"><span data-stu-id="52cc3-192">**IDeviceModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

<span data-ttu-id="52cc3-193">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-193">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-194">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-194">N/A</span></span>

[<span data-ttu-id="52cc3-195">**Идевицемоделплугин:: Колориметриктодевицеколорс**</span><span class="sxs-lookup"><span data-stu-id="52cc3-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

<span data-ttu-id="52cc3-196">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-196">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-197">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-197">N/A</span></span>

[<span data-ttu-id="52cc3-198">**Идевицемоделплугин:: Колориметриктодевицеколорсвисблакк**</span><span class="sxs-lookup"><span data-stu-id="52cc3-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

<span data-ttu-id="52cc3-199">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-199">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-200">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-200">N/A</span></span>

[<span data-ttu-id="52cc3-201">**Идевицемоделплугин::D Евицетоколориметрикколорс**</span><span class="sxs-lookup"><span data-stu-id="52cc3-201">**IDeviceModelPlugin::DeviceToColorimetricColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

<span data-ttu-id="52cc3-202">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-202">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-203">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-203">N/A</span></span>

[<span data-ttu-id="52cc3-204">**Идевицемоделплугин:: Жетгамутбаундаримеш**</span><span class="sxs-lookup"><span data-stu-id="52cc3-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

<span data-ttu-id="52cc3-205">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-205">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-206">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-206">N/A</span></span>

[<span data-ttu-id="52cc3-207">**Идевицемоделплугин:: Жетгамутбаундаримешсизе**</span><span class="sxs-lookup"><span data-stu-id="52cc3-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

<span data-ttu-id="52cc3-208">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-208">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-209">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-209">N/A</span></span>

[<span data-ttu-id="52cc3-210">**Идевицемоделплугин:: Жетнеутралаксис**</span><span class="sxs-lookup"><span data-stu-id="52cc3-210">**IDeviceModelPlugin::GetNeutralAxis**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

<span data-ttu-id="52cc3-211">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-211">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-212">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-212">N/A</span></span>

[<span data-ttu-id="52cc3-213">**Идевицемоделплугин:: Жетнеутралаксиссизе**</span><span class="sxs-lookup"><span data-stu-id="52cc3-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

<span data-ttu-id="52cc3-214">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-214">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-215">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-215">N/A</span></span>

[<span data-ttu-id="52cc3-216">**Идевицемоделплугин:: Жетнумчаннелс**</span><span class="sxs-lookup"><span data-stu-id="52cc3-216">**IDeviceModelPlugin::GetNumChannels**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

<span data-ttu-id="52cc3-217">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-217">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-218">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-218">N/A</span></span>

[<span data-ttu-id="52cc3-219">**Идевицемоделплугин:: Жетпримарисамплес**</span><span class="sxs-lookup"><span data-stu-id="52cc3-219">**IDeviceModelPlugin::GetPrimarySamples**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

<span data-ttu-id="52cc3-220">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-220">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-221">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-221">N/A</span></span>

[<span data-ttu-id="52cc3-222">**Идевицемоделплугин:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="52cc3-222">**IDeviceModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

<span data-ttu-id="52cc3-223">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-223">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-224">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-224">N/A</span></span>

[<span data-ttu-id="52cc3-225">**Идевицемоделплугин:: Сеттрансформдевицемоделинфо**</span><span class="sxs-lookup"><span data-stu-id="52cc3-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

<span data-ttu-id="52cc3-226">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-226">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-227">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-227">N/A</span></span>

[<span data-ttu-id="52cc3-228">**игамутмапмоделплугин**</span><span class="sxs-lookup"><span data-stu-id="52cc3-228">**IGamutMapModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

<span data-ttu-id="52cc3-229">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-229">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-230">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-230">N/A</span></span>

[<span data-ttu-id="52cc3-231">**Игамутмапмоделплугин:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="52cc3-231">**IGamutMapModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

<span data-ttu-id="52cc3-232">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-232">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-233">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-233">N/A</span></span>

[<span data-ttu-id="52cc3-234">**Игамутмапмоделплугин:: Саурцетодестинатионаппеаранцеколорс**</span><span class="sxs-lookup"><span data-stu-id="52cc3-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

<span data-ttu-id="52cc3-235">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-235">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-236">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-236">N/A</span></span>



 



<span data-ttu-id="52cc3-237">Структуры</span><span class="sxs-lookup"><span data-stu-id="52cc3-237">Structures</span></span>

<span data-ttu-id="52cc3-238">Имя API</span><span class="sxs-lookup"><span data-stu-id="52cc3-238">API Name</span></span>

<span data-ttu-id="52cc3-239">Header</span><span class="sxs-lookup"><span data-stu-id="52cc3-239">Header</span></span>

<span data-ttu-id="52cc3-240">Библиотека</span><span class="sxs-lookup"><span data-stu-id="52cc3-240">Library</span></span>

[<span data-ttu-id="52cc3-241">**блаккинформатион**</span><span class="sxs-lookup"><span data-stu-id="52cc3-241">**BlackInformation**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

<span data-ttu-id="52cc3-242">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-242">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-243">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-243">N/A</span></span>

[<span data-ttu-id="52cc3-244">**гамутбаундаридескриптион**</span><span class="sxs-lookup"><span data-stu-id="52cc3-244">**GamutBoundaryDescription**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

<span data-ttu-id="52cc3-245">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-245">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-246">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-246">N/A</span></span>

[<span data-ttu-id="52cc3-247">**ксизколорф**</span><span class="sxs-lookup"><span data-stu-id="52cc3-247">**XYZColorF**</span></span>](https://www.bing.com/search?q=**XYZColorF**)

<span data-ttu-id="52cc3-248">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-248">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-249">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-249">N/A</span></span>

[<span data-ttu-id="52cc3-250">**жчколорф**</span><span class="sxs-lookup"><span data-stu-id="52cc3-250">**JChColorF**</span></span>](https://www.bing.com/search?q=**JChColorF**)

<span data-ttu-id="52cc3-251">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-251">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-252">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-252">N/A</span></span>

[<span data-ttu-id="52cc3-253">**жабколорф**</span><span class="sxs-lookup"><span data-stu-id="52cc3-253">**JabColorF**</span></span>](https://www.bing.com/search?q=**JabColorF**)

<span data-ttu-id="52cc3-254">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-254">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-255">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-255">N/A</span></span>

[<span data-ttu-id="52cc3-256">**гамутшелл**</span><span class="sxs-lookup"><span data-stu-id="52cc3-256">**GamutShell**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

<span data-ttu-id="52cc3-257">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-257">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-258">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-258">N/A</span></span>

[<span data-ttu-id="52cc3-259">**гамутшеллтриангле**</span><span class="sxs-lookup"><span data-stu-id="52cc3-259">**GamutShellTriangle**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

<span data-ttu-id="52cc3-260">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-260">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-261">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-261">N/A</span></span>

[<span data-ttu-id="52cc3-262">**примарижабколорс**</span><span class="sxs-lookup"><span data-stu-id="52cc3-262">**PrimaryJabColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

<span data-ttu-id="52cc3-263">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-263">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-264">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-264">N/A</span></span>

[<span data-ttu-id="52cc3-265">**примариксизколорс**</span><span class="sxs-lookup"><span data-stu-id="52cc3-265">**PrimaryXYZColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

<span data-ttu-id="52cc3-266">Вксплугин. h</span><span class="sxs-lookup"><span data-stu-id="52cc3-266">WcsPlugIn.h</span></span>

<span data-ttu-id="52cc3-267">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52cc3-267">N/A</span></span>



 

 

 