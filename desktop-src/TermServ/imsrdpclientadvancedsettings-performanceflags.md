---
title: Имсрдпклиентадванцедсеттингс Перформанцефлагс, свойство
description: Указывает набор компонентов, которые могут быть установлены на сервере для повышения производительности.
ms.assetid: dbbc7c13-ad8a-461d-9d2e-c454bf4b9dea
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Перформанцефлагс
- Службы удаленных рабочих столов свойства Перформанцефлагс, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Перформанцефлагс
- Службы удаленных рабочих столов свойства Перформанцефлагс, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Перформанцефлагс
- Службы удаленных рабочих столов свойства Перформанцефлагс, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Перформанцефлагс
- Службы удаленных рабочих столов свойства Перформанцефлагс, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Перформанцефлагс
- Службы удаленных рабочих столов свойства Перформанцефлагс, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Перформанцефлагс
- Службы удаленных рабочих столов свойства Перформанцефлагс, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Перформанцефлагс
- Службы удаленных рабочих столов свойства Перформанцефлагс, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Перформанцефлагс
- Службы удаленных рабочих столов свойства Перформанцефлагс, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Перформанцефлагс
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PerformanceFlags
- IMsRdpClientAdvancedSettings.get_PerformanceFlags
- IMsRdpClientAdvancedSettings.put_PerformanceFlags
- IMsRdpClientAdvancedSettings2.PerformanceFlags
- IMsRdpClientAdvancedSettings2.get_PerformanceFlags
- IMsRdpClientAdvancedSettings2.put_PerformanceFlags
- IMsRdpClientAdvancedSettings3.PerformanceFlags
- IMsRdpClientAdvancedSettings3.get_PerformanceFlags
- IMsRdpClientAdvancedSettings3.put_PerformanceFlags
- IMsRdpClientAdvancedSettings4.PerformanceFlags
- IMsRdpClientAdvancedSettings4.get_PerformanceFlags
- IMsRdpClientAdvancedSettings4.put_PerformanceFlags
- IMsRdpClientAdvancedSettings5.PerformanceFlags
- IMsRdpClientAdvancedSettings5.get_PerformanceFlags
- IMsRdpClientAdvancedSettings5.put_PerformanceFlags
- IMsRdpClientAdvancedSettings6.PerformanceFlags
- IMsRdpClientAdvancedSettings6.get_PerformanceFlags
- IMsRdpClientAdvancedSettings6.put_PerformanceFlags
- IMsRdpClientAdvancedSettings7.PerformanceFlags
- IMsRdpClientAdvancedSettings7.get_PerformanceFlags
- IMsRdpClientAdvancedSettings7.put_PerformanceFlags
- IMsRdpClientAdvancedSettings8.PerformanceFlags
- IMsRdpClientAdvancedSettings8.get_PerformanceFlags
- IMsRdpClientAdvancedSettings8.put_PerformanceFlags
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1731afc6d58cede5da055da8cacaf11c8712d3c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415176"
---
# <a name="imsrdpclientadvancedsettingsperformanceflags-property"></a><span data-ttu-id="686cb-120">Имсрдпклиентадванцедсеттингс: свойство Ерформанцефлагс:P</span><span class="sxs-lookup"><span data-stu-id="686cb-120">IMsRdpClientAdvancedSettings::PerformanceFlags property</span></span>

<span data-ttu-id="686cb-121">Указывает набор компонентов, которые могут быть установлены на сервере для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="686cb-121">Specifies a set of features that can be set at the server to improve performance.</span></span>

<span data-ttu-id="686cb-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="686cb-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="686cb-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="686cb-123">Syntax</span></span>


```C++
HRESULT put_PerformanceFlags(
  [in]  LONG DisableList = TS_PERF_DISABLE_NOTHING
);

HRESULT get_PerformanceFlags(
  [out] LONG *pDisableList
);
```



## <a name="property-value"></a><span data-ttu-id="686cb-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="686cb-124">Property value</span></span>

<span data-ttu-id="686cb-125">Новые флаги.</span><span class="sxs-lookup"><span data-stu-id="686cb-125">The new flags.</span></span> <span data-ttu-id="686cb-126">Значение по умолчанию — 0 (**TS \_ PERF \_ отключает \_ ничего**).</span><span class="sxs-lookup"><span data-stu-id="686cb-126">The default is 0 (**TS\_PERF\_DISABLE\_NOTHING**.)</span></span>

<dt>

<span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>

<span data-ttu-id="686cb-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS \_ Производительность \_ — \_ ничего не отключать** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="686cb-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS\_PERF\_DISABLE\_NOTHING** (0x00000000)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-128">Компоненты отключены.</span><span class="sxs-lookup"><span data-stu-id="686cb-128">No features are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>

<span data-ttu-id="686cb-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS \_ \_ \_ Фоновый рисунок отключения производительности** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="686cb-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS\_PERF\_DISABLE\_WALLPAPER** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-130">Фоновый рисунок на рабочем столе не отображается.</span><span class="sxs-lookup"><span data-stu-id="686cb-130">Wallpaper on the desktop is not displayed.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>

<span data-ttu-id="686cb-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS \_ \_ \_ ФУЛЛВИНДОВДРАГ отключения производительности** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="686cb-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS\_PERF\_DISABLE\_FULLWINDOWDRAG** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-132">Перетаскивание в полном окне отключено; При перемещении окна отображается только структура окна.</span><span class="sxs-lookup"><span data-stu-id="686cb-132">Full-window drag is disabled; only the window outline is displayed when the window is moved.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>

<span data-ttu-id="686cb-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS \_ \_ \_ МЕНУАНИМАТИОНС отключения производительности** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="686cb-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS\_PERF\_DISABLE\_MENUANIMATIONS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-134">Анимация меню отключена.</span><span class="sxs-lookup"><span data-stu-id="686cb-134">Menu animations are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>

<span data-ttu-id="686cb-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS \_ \_ \_ Их отключение от производительности** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="686cb-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS\_PERF\_DISABLE\_THEMING** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-136">Темы отключены.</span><span class="sxs-lookup"><span data-stu-id="686cb-136">Themes are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>

<span data-ttu-id="686cb-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS \_ Производительность \_ Включение \_ расширенной графики** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="686cb-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS\_PERF\_ENABLE\_ENHANCED GRAPHICS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-138">Включить улучшенную графику.</span><span class="sxs-lookup"><span data-stu-id="686cb-138">Enable enhanced graphics.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>

<span data-ttu-id="686cb-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS \_ Производительность \_ отключение \_ \_ теневого курсора** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="686cb-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS\_PERF\_DISABLE\_CURSOR\_SHADOW** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-140">Для курсора не отображается тень.</span><span class="sxs-lookup"><span data-stu-id="686cb-140">No shadow is displayed for the cursor.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>

<span data-ttu-id="686cb-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS \_ \_ \_ КУРСОРСЕТТИНГС отключения производительности** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="686cb-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS\_PERF\_DISABLE\_CURSORSETTINGS** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-142">Мерцание курсора отключено.</span><span class="sxs-lookup"><span data-stu-id="686cb-142">Cursor blinking is disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>

<span data-ttu-id="686cb-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS \_ \_Включение \_ \_ сглаживания шрифтов** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="686cb-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS\_PERF\_ENABLE\_FONT\_SMOOTHING** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-144">Включить сглаживание шрифтов.</span><span class="sxs-lookup"><span data-stu-id="686cb-144">Enable font smoothing.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>

<span data-ttu-id="686cb-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS \_ Создание \_ \_ рабочего стола \_ для включения производительности** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="686cb-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS\_PERF\_ENABLE\_DESKTOP\_COMPOSITION** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-146">Включить композицию рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="686cb-146">Enable desktop composition.</span></span>

</dd> <dt>

<span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>

<span data-ttu-id="686cb-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS \_ \_Параметр PERF \_ нонперфклиент \_ по умолчанию** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="686cb-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS\_PERF\_DEFAULT\_NONPERFCLIENT\_SETTING** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-148">Задается внутренне для клиентов, не знающих об этом параметре.</span><span class="sxs-lookup"><span data-stu-id="686cb-148">Set internally for clients not aware of this setting.</span></span>

</dd> <dt>

<span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>

<span data-ttu-id="686cb-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS \_ \_RESERVED1 производительности** (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="686cb-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS\_PERF\_RESERVED1** (0x80000000)</span></span>


</dt> <dd>

<span data-ttu-id="686cb-150">Зарезервировано и используется клиентом для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="686cb-150">Reserved and used internally by the client.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="686cb-151">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="686cb-151">Error codes</span></span>

<span data-ttu-id="686cb-152">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="686cb-152">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="686cb-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="686cb-153">Remarks</span></span>

<span data-ttu-id="686cb-154">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="686cb-154">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="686cb-155">Требования</span><span class="sxs-lookup"><span data-stu-id="686cb-155">Requirements</span></span>



| <span data-ttu-id="686cb-156">Требование</span><span class="sxs-lookup"><span data-stu-id="686cb-156">Requirement</span></span> | <span data-ttu-id="686cb-157">Значение</span><span class="sxs-lookup"><span data-stu-id="686cb-157">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="686cb-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="686cb-158">Minimum supported client</span></span><br/> | <span data-ttu-id="686cb-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="686cb-159">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="686cb-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="686cb-160">Minimum supported server</span></span><br/> | <span data-ttu-id="686cb-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="686cb-161">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="686cb-162">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="686cb-162">Type library</span></span><br/>             | <dl> <span data-ttu-id="686cb-163"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="686cb-163"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="686cb-164">DLL</span><span class="sxs-lookup"><span data-stu-id="686cb-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="686cb-165"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="686cb-165"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="686cb-166">IID</span><span class="sxs-lookup"><span data-stu-id="686cb-166">IID</span></span><br/>                      | <span data-ttu-id="686cb-167">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="686cb-167">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="686cb-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="686cb-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="686cb-169">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="686cb-169">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="686cb-170">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="686cb-170">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="686cb-171">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="686cb-171">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="686cb-172">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="686cb-172">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="686cb-173">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="686cb-173">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="686cb-174">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="686cb-174">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="686cb-175">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="686cb-175">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="686cb-176">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="686cb-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





