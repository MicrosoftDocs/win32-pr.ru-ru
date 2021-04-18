---
description: Пользовательские значения HRESULT для интерфейса записи диагностики графики.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление HRESULT
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3d5419feb0acb5967132fbb804a9bbc11bfa4248
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537328"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span data-ttu-id="4b29d-103"><span id="vspixengine.hresult"></span>Перечисление HRESULT</span><span class="sxs-lookup"><span data-stu-id="4b29d-103"><span id="vspixengine.hresult"></span>Hresult enumeration</span></span>

<span data-ttu-id="4b29d-104">Пользовательские значения HRESULT для интерфейса записи диагностики графики.</span><span class="sxs-lookup"><span data-stu-id="4b29d-104">Custom HRESULT values for the graphics diagnostics capture interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b29d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b29d-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="4b29d-106">Константы</span><span class="sxs-lookup"><span data-stu-id="4b29d-106">Constants</span></span>

<span data-ttu-id="4b29d-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="4b29d-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX\_S\_OK**</span></span>  
<span data-ttu-id="4b29d-108">Общее значение HRESULT, указывающее, что операция завершилась правильно.</span><span class="sxs-lookup"><span data-stu-id="4b29d-108">A common HRESULT which indicates that the operation succeeded as expected.</span></span>

<span data-ttu-id="4b29d-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ false**</span><span class="sxs-lookup"><span data-stu-id="4b29d-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX\_S\_FALSE**</span></span>  
<span data-ttu-id="4b29d-110">Общее значение HRESULT, указывающее, что операция выполнена успешно, но отличается от ожидаемой.</span><span class="sxs-lookup"><span data-stu-id="4b29d-110">A common HRESULT which indicates that the operation succeeded, but in a different way than was expected.</span></span>

<span data-ttu-id="4b29d-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**\_файл ошибок \_ PIX \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="4b29d-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**PIX\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="4b29d-112">Пользовательское значение HRESULT, которое отображает \_ файл ошибок, \_ не \_ найден.</span><span class="sxs-lookup"><span data-stu-id="4b29d-112">A custom HRESULT that echos ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="4b29d-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**Ошибка PIX "сбой \_ \_ \_ среды"**</span><span class="sxs-lookup"><span data-stu-id="4b29d-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**PIX\_ERROR\_BAD\_ENVIRONMENT**</span></span>  
<span data-ttu-id="4b29d-114">Пользовательское значение HRESULT, которое возвращает ошибку о \_ неправильной \_ среде.</span><span class="sxs-lookup"><span data-stu-id="4b29d-114">A custom HRESULT that echos ERROR\_BAD\_ENVIRONMENT.</span></span>

<span data-ttu-id="4b29d-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**\_ \_ неправильный формат ошибки \_ PIX**</span><span class="sxs-lookup"><span data-stu-id="4b29d-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**PIX\_ERROR\_BAD\_FORMAT**</span></span>  
<span data-ttu-id="4b29d-116">Пользовательское значение HRESULT, которое отображает ошибочный \_ \_ Формат ошибки.</span><span class="sxs-lookup"><span data-stu-id="4b29d-116">A custom HRESULT that echos ERROR\_BAD\_FORMAT.</span></span>

<span data-ttu-id="4b29d-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**\_ \_ нарушение общего доступа к ОШИБКАм PIX \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**PIX\_ERROR\_SHARING\_VIOLATION**</span></span>  
<span data-ttu-id="4b29d-118">Пользовательское значение HRESULT, которое выводит на экран \_ нарушение общего доступа к ошибкам \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-118">A custom HRESULT that echos ERROR\_SHARING\_VIOLATION.</span></span>

<span data-ttu-id="4b29d-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**\_диск с ошибкой PIX \_ \_ полон**</span><span class="sxs-lookup"><span data-stu-id="4b29d-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**PIX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="4b29d-120">Пользовательское значение HRESULT, которое отображает \_ диск с ошибкой \_ Full.</span><span class="sxs-lookup"><span data-stu-id="4b29d-120">A custom HRESULT that echos ERROR\_DISK\_FULL.</span></span>

<span data-ttu-id="4b29d-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**Ошибка PIX. \_ \_ Дополнительные \_ данные**</span><span class="sxs-lookup"><span data-stu-id="4b29d-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**PIX\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="4b29d-122">Пользовательское значение HRESULT, которое отображает \_ Дополнительные данные об ошибке \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-122">A custom HRESULT that echos ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="4b29d-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**\_Политика PIX E \_ Missing \_ \_ комплекты отладки \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**PIX\_E\_MISSING\_DEBUG\_KITS\_POLICY**</span></span>  
<span data-ttu-id="4b29d-124">Пользовательское значение HRESULT, которое указывает на отсутствие политики комплектов отладки.</span><span class="sxs-lookup"><span data-stu-id="4b29d-124">A custom HRESULT which indicates that the Debug Kits policy is missing.</span></span>

<span data-ttu-id="4b29d-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**\_ \_ Недопустимая версия PIX E \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX\_E\_INVALID\_VERSION**</span></span>  
<span data-ttu-id="4b29d-126">Пользовательское значение HRESULT, указывающее, что используется недопустимая версия.</span><span class="sxs-lookup"><span data-stu-id="4b29d-126">A custom HRESULT which indicates that an invalid version is being used.</span></span>

<span data-ttu-id="4b29d-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX \_ E \_ с использованием \_ дкомп**</span><span class="sxs-lookup"><span data-stu-id="4b29d-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX\_E\_USING\_DCOMP**</span></span>  
<span data-ttu-id="4b29d-128">Пользовательское значение HRESULT, которое указывает, что DirectComposition используется (захват DirectComposition не поддерживается).</span><span class="sxs-lookup"><span data-stu-id="4b29d-128">A custom HRESULT which indicates that DirectComposition is in use (capture of DirectComposition is not supported.)</span></span>

<span data-ttu-id="4b29d-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX \_ E \_ с использованием \_ DIRECTWRITE**</span><span class="sxs-lookup"><span data-stu-id="4b29d-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX\_E\_USING\_DIRECTWRITE**</span></span>  
<span data-ttu-id="4b29d-130">Пользовательское значение HRESULT, которое указывает, что DirectWrite используется (захват DirectWrite не поддерживается).</span><span class="sxs-lookup"><span data-stu-id="4b29d-130">A custom HRESULT which indicates that DirectWrite is in use (capture of DirectWrite is not supported.)</span></span>

<span data-ttu-id="4b29d-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX \_ E \_ с использованием \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="4b29d-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX\_E\_USING\_D3D9**</span></span>  
<span data-ttu-id="4b29d-132">Пользовательское значение HRESULT, которое указывает, что Direct3D9 используется (захват Direct3D9 не поддерживается в Windows 10).</span><span class="sxs-lookup"><span data-stu-id="4b29d-132">A custom HRESULT which indicates that Direct3D9 is in use (capture of Direct3D9 is not supported in Windows 10.)</span></span>

<span data-ttu-id="4b29d-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**не \_ \_ удается \_ создать \_ шейдер PIX E**</span><span class="sxs-lookup"><span data-stu-id="4b29d-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX\_E\_CANT\_CREATE\_SHADER**</span></span>  
<span data-ttu-id="4b29d-134">Пользовательское значение HRESULT, указывающее, что невозможно создать заданный шейдер.</span><span class="sxs-lookup"><span data-stu-id="4b29d-134">A custom HRESULT which indicates that a specified shader can't be created.</span></span>

<span data-ttu-id="4b29d-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX \_ E \_ использование \_ D2D**</span><span class="sxs-lookup"><span data-stu-id="4b29d-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX\_E\_USING\_D2D**</span></span>  
<span data-ttu-id="4b29d-136">Пользовательское значение HRESULT, которое указывает, что Direct2D используется (захват Direct2D не поддерживается).</span><span class="sxs-lookup"><span data-stu-id="4b29d-136">A custom HRESULT which indicates that Direct2D is in use (capture of Direct2D is not supported.)</span></span>

<span data-ttu-id="4b29d-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX \_ E \_ без \_ кадров**</span><span class="sxs-lookup"><span data-stu-id="4b29d-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX\_E\_NO\_FRAMES**</span></span>  
<span data-ttu-id="4b29d-138">Пользовательское значение HRESULT, указывающее, что никакие кадры не были записаны.</span><span class="sxs-lookup"><span data-stu-id="4b29d-138">A custom HRESULT which indicates that no frames have been captured.</span></span>

<span data-ttu-id="4b29d-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ Отключить \_ Spy**</span><span class="sxs-lookup"><span data-stu-id="4b29d-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX\_E\_DISABLE\_SPY**</span></span>  

<span data-ttu-id="4b29d-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX \_ E \_ WIN8LOG \_ в \_ win7**</span><span class="sxs-lookup"><span data-stu-id="4b29d-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX\_E\_WIN8LOG\_ON\_WIN7**</span></span>  
<span data-ttu-id="4b29d-141">Пользовательское значение HRESULT, указывающее, что vsglog Windows 8 невозможно воспроизвести в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4b29d-141">A custom HRESULT which indicates that a Windows 8 vsglog cannot be played back on Windows 7.</span></span>

<span data-ttu-id="4b29d-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**\_ \_ \_ Трассировка шейдера сборки PIX E \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**PIX\_E\_BUILD\_SHADER\_TRACE**</span></span>  
<span data-ttu-id="4b29d-143">Пользовательское значение HRESULT, указывающее, что при построении трассировки шейдера произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="4b29d-143">A custom HRESULT which indicates that there was an error building the shader trace.</span></span>

<span data-ttu-id="4b29d-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX \_ E \_ без \_ \_ представления данных \_ CS**</span><span class="sxs-lookup"><span data-stu-id="4b29d-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX\_E\_NO\_CS\_DATA\_VISUALIZATION**</span></span>  
<span data-ttu-id="4b29d-145">Пользовательское значение HRESULT, указывающее на отсутствие визуализации данных шейдера вычислений.</span><span class="sxs-lookup"><span data-stu-id="4b29d-145">A custom HRESULT which indicates that there is no compute shader data visualization.</span></span>

<span data-ttu-id="4b29d-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**\_ \_ пакет SDK для несоответствия PIX E \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**PIX\_E\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="4b29d-147">Пользовательское значение HRESULT, которое указывает на несоответствие текущего пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="4b29d-147">A custom HRESULT which indicates that there is a mismatch with the current SDK.</span></span>

<span data-ttu-id="4b29d-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**\_ \_ возможный \_ пакет SDK для несоответствия PIX E \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**PIX\_E\_POSSIBLE\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="4b29d-149">Пользовательское значение HRESULT, указывающее на возможное несоответствие текущего пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="4b29d-149">A custom HRESULT which indicates that there is a possible mismatch with the current SDK.</span></span>

<span data-ttu-id="4b29d-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**\_ \_ необнаруживаемый пиксель PIX \_ E**</span><span class="sxs-lookup"><span data-stu-id="4b29d-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIX\_E\_UNDETECTABLE\_PIXEL**</span></span>  
<span data-ttu-id="4b29d-151">Пользовательское значение HRESULT, указывающее на наличие необнаруживаемого пикселя.</span><span class="sxs-lookup"><span data-stu-id="4b29d-151">A custom HRESULT which indicates that there is an undetectable pixel.</span></span>

<span data-ttu-id="4b29d-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**не \_ \_ удается выполнить \_ отладку \_ шейдера PIX E \_ с использованием \_ \_ \_ семантики системных значений**</span><span class="sxs-lookup"><span data-stu-id="4b29d-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX\_E\_CANT\_DEBUG\_SHADER\_USING\_SYSTEM\_VALUE\_SEMANTICS**</span></span>  
<span data-ttu-id="4b29d-153">Пользовательское значение HRESULT, указывающее, что сахдер нельзя отлаживать с помощью семантики системных значений.</span><span class="sxs-lookup"><span data-stu-id="4b29d-153">A custom HRESULT which indicates that the sahder can't be debugged using system value semantics.</span></span>

<span data-ttu-id="4b29d-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**\_УПДАТЕАВАИЛАБЛЕ PIX S \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX\_S\_UPDATEAVAILABLE**</span></span>  
<span data-ttu-id="4b29d-155">Пользовательское значение HRESULT, указывающее, что доступно обновление.</span><span class="sxs-lookup"><span data-stu-id="4b29d-155">A custom HRESULT which indicates that there is an update available.</span></span>

<span data-ttu-id="4b29d-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**состояние DXGI (PIX) \_ \_ \_ без \_ перенаправления**</span><span class="sxs-lookup"><span data-stu-id="4b29d-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**PIX\_DXGI\_STATUS\_NO\_REDIRECTION**</span></span>  
<span data-ttu-id="4b29d-157">Пользовательское значение HRESULT, которое отображает \_ состояние DXGI \_ без \_ перенаправления.</span><span class="sxs-lookup"><span data-stu-id="4b29d-157">A custom HRESULT that echos DXGI\_STATUS\_NO\_REDIRECTION.</span></span>

<span data-ttu-id="4b29d-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**\_ \_ состояние классической версии \_ PIX \_ без \_ доступа к рабочему столу**</span><span class="sxs-lookup"><span data-stu-id="4b29d-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**PIX\_DXGI\_STATUS\_NO\_DESKTOP\_ACCESS**</span></span>  
<span data-ttu-id="4b29d-159">Пользовательское значение HRESULT, которое отображает \_ состояние DXGI \_ без \_ доступа к рабочему столу \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-159">A custom HRESULT that echos DXGI\_STATUS\_NO\_DESKTOP\_ACCESS.</span></span>

<span data-ttu-id="4b29d-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ \_ используемая Исходная графическая система \_ \_ PIX "состояние DXGI"**</span><span class="sxs-lookup"><span data-stu-id="4b29d-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="4b29d-161">Пользовательское значение HRESULT, которое отображает \_ изображение состояния DXGI, \_ \_ \_ \_ \_ используемое источником VIDPN.</span><span class="sxs-lookup"><span data-stu-id="4b29d-161">A custom HRESULT that echos DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="4b29d-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**\_ \_ \_ изменился режим состояния в режиме DXGI. \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGED**</span></span>  
<span data-ttu-id="4b29d-163">Пользовательское значение HRESULT, которое \_ \_ изменяет режим состояния DXGI \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-163">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGED.</span></span>

<span data-ttu-id="4b29d-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ \_ выполняется изменение режима состояния \_ \_ в режиме \_ DXGI.**</span><span class="sxs-lookup"><span data-stu-id="4b29d-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="4b29d-165">Пользовательское значение HRESULT, которое отображает \_ \_ изменение режима состояния DXGI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-165">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="4b29d-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**\_состояние DXGI \_ в \_ унокклудед**</span><span class="sxs-lookup"><span data-stu-id="4b29d-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**PIX\_DXGI\_STATUS\_UNOCCLUDED**</span></span>  
<span data-ttu-id="4b29d-167">Пользовательское значение HRESULT, которое отображает \_ состояние DXGI \_ унокклудед.</span><span class="sxs-lookup"><span data-stu-id="4b29d-167">A custom HRESULT that echos DXGI\_STATUS\_UNOCCLUDED.</span></span>

<span data-ttu-id="4b29d-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**\_ \_ \_ \_ \_ по-прежнему \_ рисуется состояние "PIX DXGI" ДДА**</span><span class="sxs-lookup"><span data-stu-id="4b29d-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**PIX\_DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="4b29d-169">Пользовательское значение HRESULT, которое выводит на экран \_ состояние DXGI \_ ДДА \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-169">A custom HRESULT that echos DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="4b29d-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX \_ E \_ нотимпл**</span><span class="sxs-lookup"><span data-stu-id="4b29d-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX\_E\_NOTIMPL**</span></span>  
<span data-ttu-id="4b29d-171">Пользовательское значение HRESULT, которое отображает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="4b29d-171">A custom HRESULT that echos E\_NOTIMPL.</span></span>

<span data-ttu-id="4b29d-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**неменяющий \_ интерфейс PIX E \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX\_E\_NOINTERFACE**</span></span>  
<span data-ttu-id="4b29d-173">Пользовательское значение HRESULT, которое отображает \_ интерфейс E.</span><span class="sxs-lookup"><span data-stu-id="4b29d-173">A custom HRESULT that echos E\_NOINTERFACE.</span></span>

<span data-ttu-id="4b29d-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**\_указатель электронной почты PIX \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**PIX\_E\_POINTER**</span></span>  
<span data-ttu-id="4b29d-175">Пользовательское значение HRESULT, которое возвращает \_ указатель E.</span><span class="sxs-lookup"><span data-stu-id="4b29d-175">A custom HRESULT that echos E\_POINTER.</span></span>

<span data-ttu-id="4b29d-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**\_прерывание от PIX E \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX\_E\_ABORT**</span></span>  
<span data-ttu-id="4b29d-177">Пользовательское значение HRESULT, которое выводит на экран электронное \_ прерывание.</span><span class="sxs-lookup"><span data-stu-id="4b29d-177">A custom HRESULT that echos E\_ABORT.</span></span>

<span data-ttu-id="4b29d-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**\_сбой PIX E \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX\_E\_FAIL**</span></span>  
<span data-ttu-id="4b29d-179">Пользовательское значение HRESULT, которое возвращает E \_ Failed.</span><span class="sxs-lookup"><span data-stu-id="4b29d-179">A custom HRESULT that echos E\_FAIL.</span></span>

<span data-ttu-id="4b29d-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**\_ \_ непредвиденная E PIX**</span><span class="sxs-lookup"><span data-stu-id="4b29d-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX\_E\_UNEXPECTED**</span></span>  
<span data-ttu-id="4b29d-181">Пользовательское значение HRESULT, которое отображает \_ непредвиденные результаты в E.</span><span class="sxs-lookup"><span data-stu-id="4b29d-181">A custom HRESULT that echos E\_UNEXPECTED.</span></span>

<span data-ttu-id="4b29d-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX \_ E \_ ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="4b29d-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX\_E\_ACCESSDENIED**</span></span>  
<span data-ttu-id="4b29d-183">Пользовательское значение HRESULT, которое отображает E \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="4b29d-183">A custom HRESULT that echos E\_ACCESSDENIED.</span></span>

<span data-ttu-id="4b29d-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**\_описатель E \_ PIX**</span><span class="sxs-lookup"><span data-stu-id="4b29d-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**PIX\_E\_HANDLE**</span></span>  
<span data-ttu-id="4b29d-185">Пользовательское значение HRESULT, которое отображает E- \_ маркер.</span><span class="sxs-lookup"><span data-stu-id="4b29d-185">A custom HRESULT that echos E\_HANDLE.</span></span>

<span data-ttu-id="4b29d-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX \_ E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="4b29d-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX\_E\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="4b29d-187">Пользовательское значение HRESULT, которое отображает E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4b29d-187">A custom HRESULT that echos E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="4b29d-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="4b29d-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX\_E\_INVALIDARG**</span></span>  
<span data-ttu-id="4b29d-189">Пользовательское значение HRESULT, которое отображает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="4b29d-189">A custom HRESULT that echos E\_INVALIDARG.</span></span>

<span data-ttu-id="4b29d-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**диск "PIX", \_ \_ Ошибка Xbox \_ \_ полон**</span><span class="sxs-lookup"><span data-stu-id="4b29d-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**PIX\_XBOX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="4b29d-191">Пользовательское значение HRESULT, указывающее на то, что диск заполнен.</span><span class="sxs-lookup"><span data-stu-id="4b29d-191">A custom HRESULT which indicates that the disk is full.</span></span>

<span data-ttu-id="4b29d-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_ \_ \_ используемый адрес PIX WS \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**PIX\_WS\_E\_ADDRESS\_IN\_USE**</span></span>  
<span data-ttu-id="4b29d-193">Пользовательское значение HRESULT, указывающее, что адрес уже используется.</span><span class="sxs-lookup"><span data-stu-id="4b29d-193">A custom HRESULT which indicates that the address is already in use.</span></span>

<span data-ttu-id="4b29d-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**\_ \_ \_ Политика отсутствующих \_ наборов \_ пакетов PIX WS E**</span><span class="sxs-lookup"><span data-stu-id="4b29d-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**PIX\_WS\_E\_MISSING\_KITS\_POLICY**</span></span>  
<span data-ttu-id="4b29d-195">Пользовательское значение HRESULT, указывающее, что адрес недоступен.</span><span class="sxs-lookup"><span data-stu-id="4b29d-195">A custom HRESULT which indicates that the address is not available.</span></span>

<span data-ttu-id="4b29d-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX \_ TE \_ фаиледтолоадсофтваремодуле**</span><span class="sxs-lookup"><span data-stu-id="4b29d-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX\_TE\_FAILEDTOLOADSOFTWAREMODULE**</span></span>  
<span data-ttu-id="4b29d-197">Пользовательское значение HRESULT, указывающее, что не удалось загрузить необходимый программный модуль.</span><span class="sxs-lookup"><span data-stu-id="4b29d-197">A custom HRESULT which indicates that a necessary software module failed to load.</span></span>

<span data-ttu-id="4b29d-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX \_ TE \_ уседсофтваремодулесатваснтварпорреф**</span><span class="sxs-lookup"><span data-stu-id="4b29d-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX\_TE\_USEDSOFTWAREMODULETHATWASNTWARPORREF**</span></span>  
<span data-ttu-id="4b29d-199">Пользовательское значение HRESULT, указывающее, что используемый программный модуль не является драйвером деформации или ссылки.</span><span class="sxs-lookup"><span data-stu-id="4b29d-199">A custom HRESULT which indicates that the used software module was not the WARP or REF driver.</span></span>

<span data-ttu-id="4b29d-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX \_ TE \_ корруптедфиле**</span><span class="sxs-lookup"><span data-stu-id="4b29d-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX\_TE\_CORRUPTEDFILE**</span></span>  
<span data-ttu-id="4b29d-201">Пользовательское значение HRESULT, указывающее, что файл поврежден.</span><span class="sxs-lookup"><span data-stu-id="4b29d-201">A custom HRESULT which indicates that the file is corrupted.</span></span>

<span data-ttu-id="4b29d-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX \_ TE \_ фаиледтупенфиле**</span><span class="sxs-lookup"><span data-stu-id="4b29d-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX\_TE\_FAILEDTOOPENFILE**</span></span>  
<span data-ttu-id="4b29d-203">Пользовательское значение HRESULT, указывающее, что не удалось открыть файл.</span><span class="sxs-lookup"><span data-stu-id="4b29d-203">A custom HRESULT which indicates that the file failed to open.</span></span>

<span data-ttu-id="4b29d-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX \_ TE \_ каллфаиледонплайбакк**</span><span class="sxs-lookup"><span data-stu-id="4b29d-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX\_TE\_CALLFAILEDONPLAYBACK**</span></span>  
<span data-ttu-id="4b29d-205">Пользовательское значение HRESULT, указывающее на сбой вызова во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4b29d-205">A custom HRESULT which indicates that a call failed during playback.</span></span>

<span data-ttu-id="4b29d-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX \_ TE \_ ункновнууид**</span><span class="sxs-lookup"><span data-stu-id="4b29d-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX\_TE\_UNKNOWNUUID**</span></span>  
<span data-ttu-id="4b29d-207">Пользовательское значение HRESULT, указывающее, что обнаружен неизвестный идентификатор UUID; Это не должно происходить.</span><span class="sxs-lookup"><span data-stu-id="4b29d-207">A custom HRESULT which indicates that an unknown UUID was encountered; this should never occur.</span></span>

<span data-ttu-id="4b29d-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX \_ TE \_ ноткаптурефилеоркорруптед**</span><span class="sxs-lookup"><span data-stu-id="4b29d-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX\_TE\_NOTCAPTUREFILEORCORRUPTED**</span></span>  
<span data-ttu-id="4b29d-209">Пользовательское значение HRESULT, указывающее, что файл не является файлом записи или поврежден.</span><span class="sxs-lookup"><span data-stu-id="4b29d-209">A custom HRESULT which indicates that the file is not a capture file or is corrupted.</span></span>

<span data-ttu-id="4b29d-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX \_ TE \_ неверфиле**</span><span class="sxs-lookup"><span data-stu-id="4b29d-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX\_TE\_NEWERFILE**</span></span>  

<span data-ttu-id="4b29d-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX \_ TE \_ олдерфиле**</span><span class="sxs-lookup"><span data-stu-id="4b29d-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX\_TE\_OLDERFILE**</span></span>  

<span data-ttu-id="4b29d-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX \_ TE \_ инвалидмомент**</span><span class="sxs-lookup"><span data-stu-id="4b29d-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX\_TE\_INVALIDMOMENT**</span></span>  

<span data-ttu-id="4b29d-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**\_ \_ неверный драйвер PIX TE \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**PIX\_TE\_BAD\_DRIVER**</span></span>  
<span data-ttu-id="4b29d-214">Пользовательское значение HRESULT, указывающее, что драйвер является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="4b29d-214">A custom HRESULT which indicates that the driver is bad.</span></span>

<span data-ttu-id="4b29d-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**Ошибка PIX не \_ \_ удается \_ получить доступ к \_ депсстенЦил \_ в \_ ЦП**</span><span class="sxs-lookup"><span data-stu-id="4b29d-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**PIX\_ERROR\_CANT\_ACCESS\_DEPTHSTENCIL\_IN\_CPU**</span></span>  
<span data-ttu-id="4b29d-216">Пользовательское значение HRESULT, указывающее, что ЦП попытался получить доступ к буферу шаблона глубины, что привело к ошибке.</span><span class="sxs-lookup"><span data-stu-id="4b29d-216">A custom HRESULT which indicates that the CPU attempted to access the depth-stencil buffer, resulting in an error.</span></span>

<span data-ttu-id="4b29d-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**Ошибка PIX не \_ \_ удается \_ Разрешить \_ многовыборочную \_ текстуру**</span><span class="sxs-lookup"><span data-stu-id="4b29d-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**PIX\_ERROR\_CANT\_RESOLVE\_MULTISAMPLED\_TEXTURE**</span></span>  
<span data-ttu-id="4b29d-218">Пользовательское значение HRESULT, указывающее, что была предпринята попытка разрешить многовыборочную текстуру, что привело к ошибке.</span><span class="sxs-lookup"><span data-stu-id="4b29d-218">A custom HRESULT which indicates that there was an attempt to resolve a multi-sampled texture, resulting in an error.</span></span>

<span data-ttu-id="4b29d-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**\_ \_ Ошибка \_ неправильного \_ вызова PIX DXGI**</span><span class="sxs-lookup"><span data-stu-id="4b29d-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**PIX\_DXGI\_ERROR\_INVALID\_CALL**</span></span>  
<span data-ttu-id="4b29d-220">Пользовательское значение HRESULT, которое отображает \_ \_ недопустимый вызов ошибки DXGI \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-220">A custom HRESULT that echos DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="4b29d-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**\_ \_ \_ не \_ удалось найти ошибку DXGI PIX**</span><span class="sxs-lookup"><span data-stu-id="4b29d-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**PIX\_DXGI\_ERROR\_NOT\_FOUND**</span></span>  
<span data-ttu-id="4b29d-222">Пользовательское значение HRESULT, которое отображает \_ ошибку DXGI, \_ не \_ найдено.</span><span class="sxs-lookup"><span data-stu-id="4b29d-222">A custom HRESULT that echos DXGI\_ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="4b29d-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**\_ \_ \_ Дополнительные данные об ошибке PIX DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**PIX\_DXGI\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="4b29d-224">Пользовательское значение HRESULT, которое отображает \_ Дополнительные данные об ошибке DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-224">A custom HRESULT that echos DXGI\_ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="4b29d-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**Ошибка "PIX \_ DXGI" \_ \_ не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="4b29d-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**PIX\_DXGI\_ERROR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="4b29d-226">Пользовательское значение HRESULT, которое \_ не поддерживает вывод ошибок DXGI \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-226">A custom HRESULT that echos DXGI\_ERROR\_UNSUPPORTED.</span></span>

<span data-ttu-id="4b29d-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**\_устройство с ошибкой PIX DXGI \_ \_ \_ удалено**</span><span class="sxs-lookup"><span data-stu-id="4b29d-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**PIX\_DXGI\_ERROR\_DEVICE\_REMOVED**</span></span>  
<span data-ttu-id="4b29d-228">Пользовательское значение HRESULT, которое отображает \_ устройство с ошибкой DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-228">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_REMOVED.</span></span>

<span data-ttu-id="4b29d-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**\_Ошибка в \_ устройстве DXGI для устройства с \_ \_ зависанием**</span><span class="sxs-lookup"><span data-stu-id="4b29d-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**PIX\_DXGI\_ERROR\_DEVICE\_HUNG**</span></span>  
<span data-ttu-id="4b29d-230">Пользовательское значение HRESULT, которое отображает \_ \_ \_ зависание устройства DXGI.</span><span class="sxs-lookup"><span data-stu-id="4b29d-230">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_HUNG.</span></span>

<span data-ttu-id="4b29d-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**\_ \_ Восстановление устройства с ошибками PIX DXGI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**PIX\_DXGI\_ERROR\_DEVICE\_RESET**</span></span>  
<span data-ttu-id="4b29d-232">Пользовательское значение HRESULT, которое отображает \_ Сброс устройства с ошибкой DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-232">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_RESET.</span></span>

<span data-ttu-id="4b29d-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**Ошибка в PIX \_ DXGI \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**PIX\_DXGI\_ERROR\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="4b29d-234">Пользовательское значение HRESULT, которое \_ \_ \_ по-прежнему отображает ошибку DXGI \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-234">A custom HRESULT that echos DXGI\_ERROR\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="4b29d-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**несвязанная \_ \_ \_ Статистика кадра ошибок \_ \_ DXGI PIX**</span><span class="sxs-lookup"><span data-stu-id="4b29d-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**PIX\_DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT**</span></span>  
<span data-ttu-id="4b29d-236">Пользовательское значение HRESULT, которое отображает несвязанную \_ \_ статистику кадра ошибок DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-236">A custom HRESULT that echos DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT.</span></span>

<span data-ttu-id="4b29d-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ \_ используемый источник VIDPN \_ для \_ графики ошибок DXGI PIX**</span><span class="sxs-lookup"><span data-stu-id="4b29d-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="4b29d-238">Пользовательское значение HRESULT, которое отображает \_ \_ \_ используемый источник VIDPN для графики ошибок DXGI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-238">A custom HRESULT that echos DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="4b29d-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_ \_ \_ \_ Внутренняя ошибка в драйвере системы PIX DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**PIX\_DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR**</span></span>  
<span data-ttu-id="4b29d-240">Пользовательское значение HRESULT, которое отображает \_ \_ внутреннюю ошибку драйвера DXGI Error \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-240">A custom HRESULT that echos DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR.</span></span>

<span data-ttu-id="4b29d-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**\_Ошибка PIX DXGI — \_ \_ Немонопольная**</span><span class="sxs-lookup"><span data-stu-id="4b29d-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**PIX\_DXGI\_ERROR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="4b29d-242">Пользовательское значение HRESULT, которое отображает ошибку DXGI, не \_ \_ исключающее.</span><span class="sxs-lookup"><span data-stu-id="4b29d-242">A custom HRESULT that echos DXGI\_ERROR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="4b29d-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**\_ \_ Ошибка \_ \_ в недоступном в настоящий момент в \_ PIX DXGI**</span><span class="sxs-lookup"><span data-stu-id="4b29d-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**PIX\_DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE**</span></span>  
<span data-ttu-id="4b29d-244">Пользовательское значение HRESULT, которое отображает \_ ошибку \_ DXGI \_ в данный момент \_ недоступно.</span><span class="sxs-lookup"><span data-stu-id="4b29d-244">A custom HRESULT that echos DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE.</span></span>

<span data-ttu-id="4b29d-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**Ошибка в PIX \_ DXGI " \_ \_ Удаленный \_ клиент \_ отключен"**</span><span class="sxs-lookup"><span data-stu-id="4b29d-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**PIX\_DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED**</span></span>  
<span data-ttu-id="4b29d-246">Пользовательское значение HRESULT, которое отображает \_ ошибку DXGI \_ Remote \_ Client \_ disconnected.</span><span class="sxs-lookup"><span data-stu-id="4b29d-246">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED.</span></span>

<span data-ttu-id="4b29d-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**\_Ошибка PIX \_ DXGI \_ Remote \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="4b29d-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**PIX\_DXGI\_ERROR\_REMOTE\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="4b29d-248">Пользовательское значение HRESULT, которое отображает \_ ошибку DXGI \_ Remote \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4b29d-248">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_OUTOFMEMORY.</span></span>

<span data-ttu-id="4b29d-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**\_ \_ \_ выполняется изменение режима ошибок \_ DXGI \_ в режиме ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**PIX\_DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="4b29d-250">Пользовательское значение HRESULT, которое отображает \_ \_ изменение режима ошибок DXGI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-250">A custom HRESULT that echos DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="4b29d-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**\_ \_ \_ потеряна доступ к ошибке PIX DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**PIX\_DXGI\_ERROR\_ACCESS\_LOST**</span></span>  
<span data-ttu-id="4b29d-252">Пользовательское значение HRESULT, которое выводит на экран \_ доступ к ошибке DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-252">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_LOST.</span></span>

<span data-ttu-id="4b29d-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**\_ \_ \_ время ожидания при ошибке PIX DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**PIX\_DXGI\_ERROR\_WAIT\_TIMEOUT**</span></span>  
<span data-ttu-id="4b29d-254">Пользовательское значение HRESULT, которое отображает \_ \_ \_ время ожидания ошибки DXGI.</span><span class="sxs-lookup"><span data-stu-id="4b29d-254">A custom HRESULT that echos DXGI\_ERROR\_WAIT\_TIMEOUT.</span></span>

<span data-ttu-id="4b29d-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**\_ \_ сеанс ошибки DXGI \_ PIX \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="4b29d-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**PIX\_DXGI\_ERROR\_SESSION\_DISCONNECTED**</span></span>  
<span data-ttu-id="4b29d-256">Пользовательское значение HRESULT, которое отображает \_ сеанс с ошибкой DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-256">A custom HRESULT that echos DXGI\_ERROR\_SESSION\_DISCONNECTED.</span></span>

<span data-ttu-id="4b29d-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**Ошибка "PIX \_ DXGI" \_ \_ \_ , ограничение на \_ вывод \_ устаревшей**</span><span class="sxs-lookup"><span data-stu-id="4b29d-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**PIX\_DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE**</span></span>  
<span data-ttu-id="4b29d-258">Пользовательское значение HRESULT, которое отображает \_ ошибку \_ DXGI \_ с ограничением в \_ OUTPUT \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-258">A custom HRESULT that echos DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE.</span></span>

<span data-ttu-id="4b29d-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**Ошибка в PIX \_ DXGI \_ \_ не может \_ защитить \_ содержимое**</span><span class="sxs-lookup"><span data-stu-id="4b29d-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**PIX\_DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT**</span></span>  
<span data-ttu-id="4b29d-260">Пользовательское значение HRESULT, которое возвращает \_ ошибку DXGI, \_ не может \_ защитить \_ содержимое.</span><span class="sxs-lookup"><span data-stu-id="4b29d-260">A custom HRESULT that echos DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT.</span></span>

<span data-ttu-id="4b29d-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**\_ \_ \_ отказано в доступе к ошибке PIX DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**PIX\_DXGI\_ERROR\_ACCESS\_DENIED**</span></span>  
<span data-ttu-id="4b29d-262">Пользовательское значение HRESULT, которое отображает \_ ошибку в \_ доступе к DXGI \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-262">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="4b29d-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**\_ \_ имя ошибки PIX \_ DXGI \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="4b29d-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**PIX\_DXGI\_ERROR\_NAME\_ALREADY\_EXISTS**</span></span>  
<span data-ttu-id="4b29d-264">Пользовательское значение HRESULT, которое отображает \_ имя ошибки DXGI, \_ \_ уже \_ существует.</span><span class="sxs-lookup"><span data-stu-id="4b29d-264">A custom HRESULT that echos DXGI\_ERROR\_NAME\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="4b29d-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**\_ \_ \_ отсутствует компонент пакета SDK для ошибки \_ DXGI PIX \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**PIX\_DXGI\_ERROR\_SDK\_COMPONENT\_MISSING**</span></span>  
<span data-ttu-id="4b29d-266">Пользовательское значение HRESULT, которое выводит на экран \_ \_ компонент пакета SDK ошибок DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-266">A custom HRESULT that echos DXGI\_ERROR\_SDK\_COMPONENT\_MISSING.</span></span>

<span data-ttu-id="4b29d-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**\_ \_ васстиллдравинг Err для DDI DXGI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**PIX\_DXGI\_DDI\_ERR\_WASSTILLDRAWING**</span></span>  
<span data-ttu-id="4b29d-268">Пользовательское значение HRESULT, которое выводит на экран DXGI \_ \_ \_ васстиллдравинг Err.</span><span class="sxs-lookup"><span data-stu-id="4b29d-268">A custom HRESULT that echos DXGI\_DDI\_ERR\_WASSTILLDRAWING.</span></span>

<span data-ttu-id="4b29d-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**\_ \_ \_ неподдерживаемая ошибка в DDI DXGI PIX \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**PIX\_DXGI\_DDI\_ERR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="4b29d-270">Пользовательское значение HRESULT, которое выводит на экран \_ ошибку DDI DXGI \_ \_ не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4b29d-270">A custom HRESULT that echos DXGI\_DDI\_ERR\_UNSUPPORTED.</span></span>

<span data-ttu-id="4b29d-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**\_ \_ \_ неисключительная ошибка в DDI DXGI PIX \_**</span><span class="sxs-lookup"><span data-stu-id="4b29d-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**PIX\_DXGI\_DDI\_ERR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="4b29d-272">Пользовательское значение HRESULT, которое выводит на экран \_ ошибку DDI DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-272">A custom HRESULT that echos DXGI\_DDI\_ERR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="4b29d-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**\_Ошибка PIX D3D10. \_ \_ слишком \_ много \_ уникальных \_ \_ объектов состояния**</span><span class="sxs-lookup"><span data-stu-id="4b29d-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**PIX\_D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="4b29d-274">Пользовательское значение HRESULT, которое выводит на экран D3D10 \_ ошибку \_ слишком \_ много \_ уникальных \_ \_ объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="4b29d-274">A custom HRESULT that echos D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="4b29d-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_ \_ Файл ошибки PIX \_ D3D10 \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="4b29d-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**PIX\_D3D10\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="4b29d-276">Пользовательское значение HRESULT, которое \_ \_ \_ не удалось найти, D3D10 файл ошибок \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-276">A custom HRESULT that echos D3D10\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="4b29d-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**\_Ошибка PIX D3D11. \_ \_ слишком \_ много \_ уникальных \_ \_ объектов состояния**</span><span class="sxs-lookup"><span data-stu-id="4b29d-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="4b29d-278">Пользовательское значение HRESULT, которое выводит на экран D3D11 \_ ошибку \_ слишком \_ много \_ уникальных \_ \_ объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="4b29d-278">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="4b29d-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_ \_ Файл ошибки PIX \_ D3D11 \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="4b29d-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**PIX\_D3D11\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="4b29d-280">Пользовательское значение HRESULT, которое \_ \_ \_ не удалось найти, D3D11 файл ошибок \_ .</span><span class="sxs-lookup"><span data-stu-id="4b29d-280">A custom HRESULT that echos D3D11\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="4b29d-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**\_Ошибка PIX D3D11 \_ при \_ слишком \_ большом количестве \_ уникальных \_ \_ объектов представления**</span><span class="sxs-lookup"><span data-stu-id="4b29d-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS**</span></span>  
<span data-ttu-id="4b29d-282">Пользовательское значение HRESULT, которое выводит на экран D3D11 \_ ошибку \_ слишком \_ много \_ уникальных \_ \_ объектов представления.</span><span class="sxs-lookup"><span data-stu-id="4b29d-282">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS.</span></span>

<span data-ttu-id="4b29d-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**PIX \_ D3D11 \_ Error \_ Отложенная \_ \_ схема контекста \_ без \_ начального \_ удаления**</span><span class="sxs-lookup"><span data-stu-id="4b29d-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**PIX\_D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD**</span></span>  
<span data-ttu-id="4b29d-284">Пользовательское значение HRESULT, которое выводит на экран D3D11 \_ \_ отложенную \_ \_ карту контекста \_ без \_ начального \_ удаления.</span><span class="sxs-lookup"><span data-stu-id="4b29d-284">A custom HRESULT that echos D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD.</span></span>

<span data-ttu-id="4b29d-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**\_Ошибка PIX \_ перекрыто \_ \_ вызов Draw**</span><span class="sxs-lookup"><span data-stu-id="4b29d-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**PIX\_ERROR\_OCCLUDED\_DRAW\_CALL**</span></span>  
<span data-ttu-id="4b29d-286">Пользовательское значение HRESULT, указывающее, что вызов Draw был полностью перекрыто, что привело к ошибке.</span><span class="sxs-lookup"><span data-stu-id="4b29d-286">A custom HRESULT which indicates that a draw call was entirely occluded, resulting in an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b29d-287">Требования</span><span class="sxs-lookup"><span data-stu-id="4b29d-287">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4b29d-288">Header</span><span class="sxs-lookup"><span data-stu-id="4b29d-288">Header</span></span></p></td><td><span data-ttu-id="4b29d-289">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="4b29d-289">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



