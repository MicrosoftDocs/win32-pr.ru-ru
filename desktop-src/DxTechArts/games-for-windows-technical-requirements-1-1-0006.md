---
title: Советы и рекомендации в отношении технических требований к играм для Windows XP, Windows Vista, Windows 7 и Windows 8
description: В этой статье приводятся технические требования и рекомендации для игр, работающих в Windows.
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c7a0f52685b0b99247ebfd86af3727d834ca63
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120309"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="0f25c-103">Игры для технических требований Windows: рекомендации по работе с играми в Windows XP, Windows Vista, Windows 7 и Windows 8</span><span class="sxs-lookup"><span data-stu-id="0f25c-103">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="0f25c-104">В этой статье приводятся технические требования и рекомендации для игр, работающих в Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-104">This article provides technical requirements and best practices for games that run on Windows.</span></span> <span data-ttu-id="0f25c-105">Мы написали эти технические требования и рекомендации в основном для охвата Windows Vista и Windows 7, а также устаревшей операционной системы Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0f25c-105">We wrote these technical requirements and best practices primarily to cover Windows Vista and Windows 7, as well as the legacy Windows XP operating system.</span></span> <span data-ttu-id="0f25c-106">Эти рекомендации также обычно применяются к классическим играм Win32 в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0f25c-106">These best practices also generally apply to desktop Win32 games on Windows 8.</span></span>

<span data-ttu-id="0f25c-107">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="0f25c-107">This articles contains these sections:</span></span>

-   [<span data-ttu-id="0f25c-108">Различия в Windows 8</span><span class="sxs-lookup"><span data-stu-id="0f25c-108">Differences for Windows 8</span></span>](#differences-for-windows-8)
    -   [<span data-ttu-id="0f25c-109">Дополнительная информация</span><span class="sxs-lookup"><span data-stu-id="0f25c-109">Additional Information</span></span>](#additional-information)
-   [<span data-ttu-id="0f25c-110">Игры для Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-110">Games for Windows</span></span>](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [<span data-ttu-id="0f25c-111">1,1. Интеграция обозревателя игр</span><span class="sxs-lookup"><span data-stu-id="0f25c-111">1.1 Games Explorer Integration</span></span>](#11-games-explorer-integration)
    -   [<span data-ttu-id="0f25c-112">1,2. Поддержка семейной безопасности и родительского контроля</span><span class="sxs-lookup"><span data-stu-id="0f25c-112">1.2 Support Family Safety / Parental Controls</span></span>](/windows)
    -   [<span data-ttu-id="0f25c-113">1,3 поддержка полнофункциональных сохраненных игр</span><span class="sxs-lookup"><span data-stu-id="0f25c-113">1.3 Support Rich Saved Games</span></span>](#13-support-rich-saved-games)
    -   <span data-ttu-id="0f25c-114">[1,4. Поддержка общего контроллера Xbox 360 для \[ условного требования Windows\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)</span><span class="sxs-lookup"><span data-stu-id="0f25c-114">[1.4 Support the Xbox 360 Common Controller for Windows \[Conditional Requirement\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)</span></span>
    -   [<span data-ttu-id="0f25c-115">1,5 поддержка нескольких пропорций и разрешений</span><span class="sxs-lookup"><span data-stu-id="0f25c-115">1.5 Support Multiple Aspect Ratios and Resolutions</span></span>](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [<span data-ttu-id="0f25c-116">1,6. Поддержка запуска из Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="0f25c-116">1.6 Support Launch from Windows Media Center</span></span>](#16-support-launch-from-windows-media-center)
    -   [<span data-ttu-id="0f25c-117">1,7 поддержка Direct3D</span><span class="sxs-lookup"><span data-stu-id="0f25c-117">1.7 Direct3D Support</span></span>](#17-direct3d-support)
    -   [<span data-ttu-id="0f25c-118">1,8. Включение высокого разрешения</span><span class="sxs-lookup"><span data-stu-id="0f25c-118">1.8 Enable High-DPI-Aware</span></span>](#18-enable-high-dpi-aware)
-   [<span data-ttu-id="0f25c-119">Безопасность и совместимость</span><span class="sxs-lookup"><span data-stu-id="0f25c-119">Security and Compatibility</span></span>](#security-and-compatibility)
    -   [<span data-ttu-id="0f25c-120">2,1 Следуйте рекомендациям по контролю учетных записей пользователей</span><span class="sxs-lookup"><span data-stu-id="0f25c-120">2.1 Follow User Account Control Guidelines</span></span>](#21-follow-user-account-control-guidelines)
    -   [<span data-ttu-id="0f25c-121">2,2. Поддержка 64-разрядных версий Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-121">2.2 Support Windows x64 Versions</span></span>](#22-support-windows-x64-versions)
    -   [<span data-ttu-id="0f25c-122">2,3. входные файлы</span><span class="sxs-lookup"><span data-stu-id="0f25c-122">2.3 Sign Files</span></span>](#23-sign-files)
    -   [<span data-ttu-id="0f25c-123">2,4. подписывать драйверы</span><span class="sxs-lookup"><span data-stu-id="0f25c-123">2.4 Sign Drivers</span></span>](#24-sign-drivers)
    -   [<span data-ttu-id="0f25c-124">2,5. выполнение проверки правильности версий</span><span class="sxs-lookup"><span data-stu-id="0f25c-124">2.5 Perform Proper Version Checking</span></span>](#25-perform-proper-version-checking)
    -   [<span data-ttu-id="0f25c-125">2,6 Поддержка параллельных сеансов пользователей</span><span class="sxs-lookup"><span data-stu-id="0f25c-125">2.6 Support Concurrent User Sessions</span></span>](#26-support-concurrent-user-sessions)
    -   [<span data-ttu-id="0f25c-126">2,7. Поддержка длинных имен</span><span class="sxs-lookup"><span data-stu-id="0f25c-126">2.7 Support Long Names</span></span>](#27-support-long-names)
-   [<span data-ttu-id="0f25c-127">Установка</span><span class="sxs-lookup"><span data-stu-id="0f25c-127">Installation</span></span>](#32-support-user-account-control-for-installation)
    -   [<span data-ttu-id="0f25c-128">3,1. поддержка быстрой установки</span><span class="sxs-lookup"><span data-stu-id="0f25c-128">3.1 Support Easy Installation</span></span>](#31-support-easy-installation)
    -   [<span data-ttu-id="0f25c-129">3,2. Поддержка контроля учетных записей пользователей для установки</span><span class="sxs-lookup"><span data-stu-id="0f25c-129">3.2 Support User Account Control for Installation</span></span>](#32-support-user-account-control-for-installation)
    -   [<span data-ttu-id="0f25c-130">3,3. Установка для исправления папок</span><span class="sxs-lookup"><span data-stu-id="0f25c-130">3.3 Install to Correct Folders</span></span>](#33-install-to-correct-folders)
    -   [<span data-ttu-id="0f25c-131">3,4. Установка ресурсов Windows надлежащим образом</span><span class="sxs-lookup"><span data-stu-id="0f25c-131">3.4 Install Windows Resources Properly</span></span>](#34-install-windows-resources-properly)
    -   [<span data-ttu-id="0f25c-132">3,5. Предотвращение перезагрузки во время установки</span><span class="sxs-lookup"><span data-stu-id="0f25c-132">3.5 Avoid Reboots During Installation</span></span>](#35-avoid-reboots-during-installation)
    -   [<span data-ttu-id="0f25c-133">3,6. правильное использование управления версиями файлов</span><span class="sxs-lookup"><span data-stu-id="0f25c-133">3.6 Use File Versioning Correctly</span></span>](#36-use-file-versioning-correctly)
    -   <span data-ttu-id="0f25c-134">[3,7 поддержка \[ условного требования автозапуска\]](#37-support-autorun-conditional-requirement)</span><span class="sxs-lookup"><span data-stu-id="0f25c-134">[3.7 Support Autorun \[Conditional Requirement\]](#37-support-autorun-conditional-requirement)</span></span>
-   [<span data-ttu-id="0f25c-135">Надежность</span><span class="sxs-lookup"><span data-stu-id="0f25c-135">Reliability</span></span>](#reliability)
    -   [<span data-ttu-id="0f25c-136">4,1. Устраните ненужные перезагрузки</span><span class="sxs-lookup"><span data-stu-id="0f25c-136">4.1 Eliminate Unnecessary Reboots</span></span>](#41-eliminate-unnecessary-reboots)
    -   [<span data-ttu-id="0f25c-137">4,2 Устранение сбоев средство проверки приложений</span><span class="sxs-lookup"><span data-stu-id="0f25c-137">4.2 Eliminate Application Verifier Failures</span></span>](#42-eliminate-application-verifier-failures)
    -   [<span data-ttu-id="0f25c-138">4,3 поддержка отчеты об ошибках Windows и сведения о версии файла</span><span class="sxs-lookup"><span data-stu-id="0f25c-138">4.3 Support Windows Error Reporting and File Version Information</span></span>](#43-support-windows-error-reporting-and-file-version-information)
-   [<span data-ttu-id="0f25c-139">Стандартный контроллер Xbox 360 для терминологии Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-139">Xbox 360 Common Controller for Windows Terminology</span></span>](#xbox-360-common-controller-for-windows-terminology)
-   [<span data-ttu-id="0f25c-140">Рекомендации по промежуточному программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="0f25c-140">Guidelines for Game Middleware Products</span></span>](#guidelines-for-game-middleware-products)
    -   [<span data-ttu-id="0f25c-141">Введение</span><span class="sxs-lookup"><span data-stu-id="0f25c-141">Introduction</span></span>](#introduction)
    -   [<span data-ttu-id="0f25c-142">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="0f25c-142">Additional Recommendations</span></span>](#additional-recommendations)
    -   [<span data-ttu-id="0f25c-143">Игры для демонстрации Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-143">Games for Windows Showcases</span></span>](#games-for-windows-showcases)
-   [<span data-ttu-id="0f25c-144">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="0f25c-144">Resources</span></span>](#resources)

## <a name="differences-for-windows-8"></a><span data-ttu-id="0f25c-145">Различия в Windows 8</span><span class="sxs-lookup"><span data-stu-id="0f25c-145">Differences for Windows 8</span></span>

<span data-ttu-id="0f25c-146">Ниже приведена сводка основных отличий при применении этих технических требований и рекомендаций к Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0f25c-146">Here is a summary of the key differences when applying these technical requirements and best practices to Windows 8.</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-147"><span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**Пользовательский интерфейс обозревателя игр недоступен**</span><span class="sxs-lookup"><span data-stu-id="0f25c-147"><span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**The Games Explorer UI is not visible**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-148">Все игры, регистрируемые с помощью [обозревателя игр](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) , отображаются в виде плиток в новом пользовательском интерфейсе Windows, но большая часть метаданных, связанных с названием, больше не видна.</span><span class="sxs-lookup"><span data-stu-id="0f25c-148">All games that you register with the [Games Explorer](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) are surfaced as tiles in new Windows UI, but much of the metadata that is associated with the title is no longer visible.</span></span> <span data-ttu-id="0f25c-149">Вы по-прежнему используете средство студии файла определения игр (GDFMAKER.EXE), которое теперь доступно в пакете средств разработки программного обеспечения (SDK) для Windows, для создания метаданных.</span><span class="sxs-lookup"><span data-stu-id="0f25c-149">You still use the Games Definition File Maker tool (GDFMAKER.EXE), which is now available in the Windows Software Development Kit (SDK), to author the metadata.</span></span> <span data-ttu-id="0f25c-150">Вы также используете существующие механизмы для развертывания метаданных.</span><span class="sxs-lookup"><span data-stu-id="0f25c-150">You also use the existing mechanisms for deploying the metadata.</span></span> <span data-ttu-id="0f25c-151">Продолжайте протестировать регистрацию обозревателя игр с помощью Windows 7 и убедитесь, что новая плитка пользовательского интерфейса Windows отображается при установке в Windows 8 (см. раздел [Интеграция обозревателя игр 1,1](#11-games-explorer-integration)).</span><span class="sxs-lookup"><span data-stu-id="0f25c-151">Continue to test your Games Explorer registration by using Windows 7, and verify that the new Windows UI tile shows up when you install it on Windows 8 (see [1.1 Games Explorer Integration](#11-games-explorer-integration)).</span></span>

<span data-ttu-id="0f25c-152">Чтобы скачать пакет SDK для Windows 8, см. раздел [Downloads for Разработка классических приложений](https://msdn.microsoft.com/windows/desktop/aa904949).</span><span class="sxs-lookup"><span data-stu-id="0f25c-152">To download the Windows 8 SDK, see [Downloads for developing desktop apps](https://msdn.microsoft.com/windows/desktop/aa904949).</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-153"><span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**Регистрация с помощью API Game Explorer — это механизм регистрации игр с помощью функции родительского контроля Windows.**</span><span class="sxs-lookup"><span data-stu-id="0f25c-153"><span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**Registration with the Game Explorer APIs continues to be the mechanism for registering your game with Windows Parental Controls**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-154">Рекомендуется запустить Windows SDK версию ГДФМАКЕР в выпущенной версии Windows 8, чтобы гарантировать, что она сможет заполнить все поддерживаемые системы оценки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-154">We recommend that you run the Windows SDK version of GDFMAKER on the released version of Windows 8 to ensure that it can populate all currently supported rating systems.</span></span>

> [!Note]  
> <span data-ttu-id="0f25c-155">Для этой версии ГДФМАКЕР требуется .NET 4,0.</span><span class="sxs-lookup"><span data-stu-id="0f25c-155">This version of GDFMAKER requires .NET 4.0.</span></span>

 

<span data-ttu-id="0f25c-156">См. раздел [Поддержка безопасности и родительский контроль семейства поддержки 1,2](/windows).</span><span class="sxs-lookup"><span data-stu-id="0f25c-156">See [1.2 Support Family Safety / Parental Controls](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-157"><span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**Сейчас есть три варианта использования API КСИНПУТ в зависимости от ваших требований.**</span><span class="sxs-lookup"><span data-stu-id="0f25c-157"><span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**There are now three choices for using the XINPUT API depending on your requirements**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-158">КСИНПУТ 1,4 встроена в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0f25c-158">XINPUT 1.4 is built into Windows 8.</span></span> <span data-ttu-id="0f25c-159">Приложения для Магазина Windows и классические приложения Win32 могут использовать КСИНПУТ 1,4.</span><span class="sxs-lookup"><span data-stu-id="0f25c-159">Both Windows Store apps and desktop Win32 apps can use XINPUT 1.4.</span></span> <span data-ttu-id="0f25c-160">Все версии Windows могут использовать КСИНПУТ 9.1.0 для упрощенных распространенных контроллеров, но пакет распространения с КСИНПУТ 9.1.0 не существует.</span><span class="sxs-lookup"><span data-stu-id="0f25c-160">All versions of Windows can use XINPUT 9.1.0 for simplified common controllers, but there is no redistribution package with XINPUT 9.1.0.</span></span> <span data-ttu-id="0f25c-161">Все версии Windows также могут использовать существующий пакет SDK DirectX версии КСИНПУТ 1,3, который требует развертывания Директсетуп.</span><span class="sxs-lookup"><span data-stu-id="0f25c-161">All versions of Windows can also use the existing DirectX SDK version XINPUT 1.3, which requires DirectSetup to deploy.</span></span>

<span data-ttu-id="0f25c-162">См. раздел [1,4 поддержка общего контроллера Xbox 360 для Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).</span><span class="sxs-lookup"><span data-stu-id="0f25c-162">See [1.4 Support the Xbox 360 Common Controller for Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-163"><span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**В Windows RT поддерживается только ограниченный набор приложений Win32 для настольных систем**</span><span class="sxs-lookup"><span data-stu-id="0f25c-163"><span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**Only a limited set of desktop Win32 apps are supported on Windows RT**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-164">Игры, работающие в Windows 7, могут и должны правильно работать на платформах Windows 8 x86 и x64.</span><span class="sxs-lookup"><span data-stu-id="0f25c-164">Games that run on Windows 7 can and should run correctly on Windows 8 x86 and x64 platforms.</span></span>

<span data-ttu-id="0f25c-165">См. [2,2 Поддержка 64-разрядных версий Windows](#22-support-windows-x64-versions).</span><span class="sxs-lookup"><span data-stu-id="0f25c-165">See [2.2 Support Windows x64 Versions](#22-support-windows-x64-versions).</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-166"><span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Убедитесь, что все проверки ОС выполняются правильно.**</span><span class="sxs-lookup"><span data-stu-id="0f25c-166"><span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Ensure any OS checks are done correctly**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-167">Версия ОС Windows 8 — 6,2.</span><span class="sxs-lookup"><span data-stu-id="0f25c-167">The Windows 8 OS version is  6.2 .</span></span> <span data-ttu-id="0f25c-168">Windows 8 передает текущие минимальные тесты, которые мы рекомендуем использовать для развертывания игр.</span><span class="sxs-lookup"><span data-stu-id="0f25c-168">Windows 8 passes the current  minimum bar  tests that we recommend for game deployment.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-169"><span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**Пакет повторного распространения DirectX End-User успешно запускается в Windows 8, как и в Windows 7, для развертывания D3DX9, D3DX10, D3DX11, КСИНПУТ 1,3, КСАУДИО 2,7, Ксактенгине и т. д.**</span><span class="sxs-lookup"><span data-stu-id="0f25c-169"><span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**The  DirectX End-User Redistribution  package runs successfully on Windows 8, as it does on Windows 7, to deploy D3DX9, D3DX10, D3DX11, XINPUT 1.3, XAUDIO 2.7, XACTEngine, and so on**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-170">Но существует известная ошибка с Директсетуп в системах с установленным только .NET 4,0 из-за обработки развертывания устаревших сборок DirectX 1,1.</span><span class="sxs-lookup"><span data-stu-id="0f25c-170">But, a known issue exists with DirectSetup on systems with only .NET 4.0 installed due to the deployment handling of the legacy Managed DirectX 1.1 assemblies.</span></span> <span data-ttu-id="0f25c-171">Эта проблема относится как к Windows 8, которая поставляется с .NET 4,5 по умолчанию, так и к обновленным компьютерам Windows XP с установленной средой выполнения .NET 4,0.</span><span class="sxs-lookup"><span data-stu-id="0f25c-171">This issue applies to both Windows 8, which comes with .NET 4.5 by default, and  fresh  Windows XP computers with the .NET 4.0 runtime installed.</span></span> <span data-ttu-id="0f25c-172">Но эта проблема не относится к любой версии .NET до .NET 4,0.</span><span class="sxs-lookup"><span data-stu-id="0f25c-172">But, this issue does not apply to any version of .NET prior to .NET 4.0.</span></span> <span data-ttu-id="0f25c-173">Хотя Windows 8 обладает поведением совместимости приложений для автоматического устранения этой проблемы (для чего требуется сетевой доступ), рекомендуется, чтобы игры, которые продолжают развертывать обновление Директсетуп в пакете SDK DirectX (Июнь 2010), обновили версию РАСПРОСТРАНЯЕМых файлов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-173">While Windows 8 has an application compatibility behavior to resolve this issue automatically (which requires network access), we recommend that games that continue to deploy DirectSetup update to the DirectX SDK (June 2010) refreshed version of the REDIST files.</span></span> <span data-ttu-id="0f25c-174">Как всегда, если вы используете Директсетуп в качестве заголовка, Сократите заголовок до минимального необходимого набора CAB.</span><span class="sxs-lookup"><span data-stu-id="0f25c-174">As always, if you use DirectSetup for your title, trim your title down to the minimum required set of CABs.</span></span>

<span data-ttu-id="0f25c-175">См. статью [3,4. Установка ресурсов Windows правильно](#34-install-windows-resources-properly).</span><span class="sxs-lookup"><span data-stu-id="0f25c-175">See [3.4 Install Windows Resources Properly](#34-install-windows-resources-properly).</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-176"><span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Игры, для которых требуется совместимая с .NET 2,0 среда выполнения (2,0, 3,0, 3,5), продолжают использовать существующие механизмы развертывания.**</span><span class="sxs-lookup"><span data-stu-id="0f25c-176"><span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Games that require the .NET  2.0  compatible runtime (2.0, 3.0, 3.5) continue to use existing deployment mechanisms**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-177">Эти игры активируют поведение совместимости приложений в Windows 8 для автоматического включения среды выполнения .NET 3,5 (что требует сетевого доступа).</span><span class="sxs-lookup"><span data-stu-id="0f25c-177">These games trigger an application compatibility behavior on Windows 8 to enable the .NET 3.5 runtime automatically (which requires network access).</span></span> <span data-ttu-id="0f25c-178">Но мы рекомендуем разработчикам .NET перемещаться в среду выполнения .NET 4,0.</span><span class="sxs-lookup"><span data-stu-id="0f25c-178">But, we recommend that .NET developers move to the .NET 4.0 runtime.</span></span>

> [!Note]  
> <span data-ttu-id="0f25c-179">Устаревшие управляемые сборки DirectX 1,1 несовместимы со средой выполнения .NET 4. x.</span><span class="sxs-lookup"><span data-stu-id="0f25c-179">The legacy Managed DirectX 1.1 assemblies are not compatible with the .NET 4.x runtime.</span></span>

 

<span data-ttu-id="0f25c-180">См. статью [3,4. Установка ресурсов Windows правильно](#34-install-windows-resources-properly).</span><span class="sxs-lookup"><span data-stu-id="0f25c-180">See [3.4 Install Windows Resources Properly](#34-install-windows-resources-properly).</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-181"><span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**Не рекомендуется использовать средство автозапуска или другие предварительно установленные технологии, основанные на .NET.**</span><span class="sxs-lookup"><span data-stu-id="0f25c-181"><span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**Use of an  autorunner  or other pre-install technology that relies on .NET is not recommended**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-182">Вы можете предположить, что в Windows Vista и Windows 7 имеются только совместимые с .NET 2,0 среды выполнения (2,0, 3,0, 3,5).</span><span class="sxs-lookup"><span data-stu-id="0f25c-182">You can assume that only .NET 2.0 compatible runtimes (2.0, 3.0, 3.5) are present on Windows Vista and Windows 7.</span></span> <span data-ttu-id="0f25c-183">По умолчанию в Windows 8 имеется только совместимая среда выполнения .NET 4,0.</span><span class="sxs-lookup"><span data-stu-id="0f25c-183">Only the .NET 4.0 compatible runtime is present on Windows 8 by default.</span></span>

<span data-ttu-id="0f25c-184">См. раздел [Поддержка автозапуска в 3,7](#37-support-autorun-conditional-requirement).</span><span class="sxs-lookup"><span data-stu-id="0f25c-184">See [3.7 Support Autorun](#37-support-autorun-conditional-requirement).</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-185"><span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**Обновленная средство проверки приложений для Windows 8**</span><span class="sxs-lookup"><span data-stu-id="0f25c-185"><span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**There is an updated Application Verifier for Windows 8**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-186">Пакет SDK для Windows 8 включает этот обновленный средство проверки приложений.</span><span class="sxs-lookup"><span data-stu-id="0f25c-186">The Windows 8 SDK includes this updated Application Verifier.</span></span>

<span data-ttu-id="0f25c-187">См. раздел [4,2 Устранение сбоев средство проверки приложений](#42-eliminate-application-verifier-failures).</span><span class="sxs-lookup"><span data-stu-id="0f25c-187">See [4.2 Eliminate Application Verifier Failures](#42-eliminate-application-verifier-failures).</span></span>

</dd> </dl>

### <a name="additional-information"></a><span data-ttu-id="0f25c-188">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="0f25c-188">Additional Information</span></span>

<dl>

[<span data-ttu-id="0f25c-189">Совместимость с Windows 8 и Windows Server 2012 Cookbook</span><span class="sxs-lookup"><span data-stu-id="0f25c-189">Windows 8 and Windows Server 2012 compatibility cookbook</span></span>](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[<span data-ttu-id="0f25c-190">Где находится пакет SDK для DirectX?</span><span class="sxs-lookup"><span data-stu-id="0f25c-190">Where is the DirectX SDK?</span></span>](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a><span data-ttu-id="0f25c-191">Игры для Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-191">Games for Windows</span></span>

<span data-ttu-id="0f25c-192">**Общие сведения о требованиях к играм**</span><span class="sxs-lookup"><span data-stu-id="0f25c-192">**Summary of Games Requirements**</span></span>

<span data-ttu-id="0f25c-193">**Преимущества для клиентов**</span><span class="sxs-lookup"><span data-stu-id="0f25c-193">**Customer Benefits**</span></span>

<span data-ttu-id="0f25c-194">Компьютерные игры — это основные возможности для развлечений в Windows, но проблемы с простотой использования привели к тому, что клиенты будут разочарованы в течение нескольких лет.</span><span class="sxs-lookup"><span data-stu-id="0f25c-194">Computer games are a key entertainment experience on Windows, but ease-of-use concerns have caused customer frustration over the years.</span></span> <span data-ttu-id="0f25c-195">Обычно игры устанавливаются как приложения, но они используются более похоже на развлекательный мультимедиа (например, фильмы или песни).</span><span class="sxs-lookup"><span data-stu-id="0f25c-195">Traditionally, games are installed like applications, but they are utilized more like entertainment media (movies or songs, for example).</span></span> <span data-ttu-id="0f25c-196">Инновации, такие как Обозреватель игр, предоставляют играм единообразный способ, отличный от стандартных приложений.</span><span class="sxs-lookup"><span data-stu-id="0f25c-196">Innovations, such as Games Explorer, expose games in a consistent manner that is different from standard applications.</span></span> <span data-ttu-id="0f25c-197">Эти нововведения также предоставляют играм первый класс в Windows вместе с музыкой и изображениями.</span><span class="sxs-lookup"><span data-stu-id="0f25c-197">These innovations also give games first-class citizen status in Windows, together with Music and Pictures.</span></span> <span data-ttu-id="0f25c-198">Следующие требования помогают гарантировать, что Windows Vista и Windows 7 предоставляют улучшенную, более доступную и единую среду игр.</span><span class="sxs-lookup"><span data-stu-id="0f25c-198">The following requirements help ensure that Windows Vista and Windows 7 provide an improved, more accessible, and unified gaming experience.</span></span> <span data-ttu-id="0f25c-199">В то же время они обеспечивают совместимость с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0f25c-199">At the same time, they ensure compatibility with Windows XP.</span></span>

### <a name="11-games-explorer-integration"></a><span data-ttu-id="0f25c-200">1,1. Интеграция обозревателя игр</span><span class="sxs-lookup"><span data-stu-id="0f25c-200">1.1 Games Explorer Integration</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-201"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-201"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-202">Игра должна быть видима в обозревателе игр (папка « **игры** ») в Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-202">The game must be visible within Games Explorer (the **Games** folder) on Windows Vista and Windows 7.</span></span> <span data-ttu-id="0f25c-203">Если этот флажок установлен, игра также должна отображать правильные метаданные, включая издателя, разработчика, дату выпуска, версию, оценки индекса производительности Windows, оценку (если применимо) и связанные гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-203">When selected, the game must also display correct meta data, which includes publisher, developer, release date, version, Windows Experience Index scores, rating (if applicable), and associated hyperlinks.</span></span>

<span data-ttu-id="0f25c-204">Если игра выполняется в цифровом режиме через Интернет-игру, поставщик услуг также должен отображаться в обозревателе игр.</span><span class="sxs-lookup"><span data-stu-id="0f25c-204">If the game is digitally distributed through an online game service, then the service provider should also appear in Games Explorer.</span></span> <span data-ttu-id="0f25c-205">Чтобы обеспечить правильную обработку поставщика и включить использование RSS-каналов, следует использовать версию 2 схемы для файлов определения игры (Гдфс).</span><span class="sxs-lookup"><span data-stu-id="0f25c-205">To ensure proper handling of the provider and to enable use of RSS feeds, version 2 of the schema for game definition files (GDFs) should be used.</span></span> <span data-ttu-id="0f25c-206">(Дополнительные сведения о Гдфс см. в разделе Дополнительные сведения.)</span><span class="sxs-lookup"><span data-stu-id="0f25c-206">(For more information about GDFs, see Additional Information.)</span></span>

<span data-ttu-id="0f25c-207">Кроме того, при запуске в Windows Vista и Windows 7 установщики игр должны соблюдать следующие правила:</span><span class="sxs-lookup"><span data-stu-id="0f25c-207">In addition, game installers must observe the following rules when they run on Windows Vista and Windows 7:</span></span>

-   <span data-ttu-id="0f25c-208">Установка не должна создавать ярлыки для запуска игры на рабочем столе, в меню "Пуск" или в любом другом расположении.</span><span class="sxs-lookup"><span data-stu-id="0f25c-208">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span>
-   <span data-ttu-id="0f25c-209">Не следует создавать задачи и ярлыки для удаления.</span><span class="sxs-lookup"><span data-stu-id="0f25c-209">Tasks and shortcuts for removal must not be created.</span></span>
-   <span data-ttu-id="0f25c-210">Пользователи должны иметь возможность удалить игру с помощью компонента "программы и компоненты" панели управления в Windows Vista и Windows 7 или компонента "Установка и удаление программ" в панели управления в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0f25c-210">Users must be able to remove the game by using Programs and Features in Control Panel on Windows Vista and Windows 7, or Add or Remove Programs in Control Panel on Windows XP.</span></span>

<span data-ttu-id="0f25c-211">В Windows XP и в предыдущих версиях Windows установщик игр может создавать группы программ, значки рабочего стола или ярлыки по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="0f25c-211">On Windows XP, and on previous versions of Windows, the game installer is free to create program groups, desktop icons, or shortcuts as needed.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-212"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-212"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-213">Обозреватель игр Windows похож на концепцию папок « **Мои документы** » и « **Мои рисунки**» в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0f25c-213">Windows Games Explorer is similar in concept to the Windows XP folders **My Documents** or **My Pictures**.</span></span> <span data-ttu-id="0f25c-214">Идея состоит в том, чтобы централизовать аналогичное содержимое в одном месте и обеспечить более простые и контекстные действия.</span><span class="sxs-lookup"><span data-stu-id="0f25c-214">The idea is to centralize similar content in one place and allow for easier organization and context-sensitive activities.</span></span> <span data-ttu-id="0f25c-215">Обозреватель игр расширяет концепцию " **Мои документы** " или " **Мои рисунки** ", предоставляя более широкие возможности Организации и контроля над играми.</span><span class="sxs-lookup"><span data-stu-id="0f25c-215">Games Explorer extends the **My Documents** or **My Pictures** concept by allowing richer organization and control over games.</span></span> <span data-ttu-id="0f25c-216">Обозреватель игр позволяет играм просматривать, упорядочивать и взаимодействовать со всеми играми, установленными на их системах.</span><span class="sxs-lookup"><span data-stu-id="0f25c-216">Games Explorer allows gamers to view, organize, and interact with all the games installed on their systems.</span></span> <span data-ttu-id="0f25c-217">Он также позволяет издателям игр более эффективно обмениваться важными сведениями о игре.</span><span class="sxs-lookup"><span data-stu-id="0f25c-217">It also allows game publishers to communicate important game information more effectively.</span></span> <span data-ttu-id="0f25c-218">Система управляется данными, что позволяет издателю игр обновлять сведения о игре в течение жизненного цикла продукта.</span><span class="sxs-lookup"><span data-stu-id="0f25c-218">The system is data-driven, making it easy for a game publisher to update game information over the life of the product.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-219"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-219"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-220">Интеграция с обозревателем игр требует создания файла определения игры (ГДФ), который представляет собой текстовый XML-файл, внедренный в двоичный файл (исполняемый файл или DLL) в качестве ресурса вместе со значком Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-220">Integration with Games Explorer requires that you author a game definition file (GDF), which is an XML text file that is embedded within a binary file (an executable file or a DLL) as a resource, along with a Windows icon.</span></span> <span data-ttu-id="0f25c-221">После этого игра должна быть зарегистрирована в обозревателе игр.</span><span class="sxs-lookup"><span data-stu-id="0f25c-221">The game must then be registered with Games Explorer.</span></span> <span data-ttu-id="0f25c-222">ГДФ также позволяет раскрытие предоставленной информации, такой как название игры, издатель, разработчик, ссылки на веб-сайты и необязательные задачи.</span><span class="sxs-lookup"><span data-stu-id="0f25c-222">The GDF also enables the exposure of supplied information such as the game title, publisher, developer, links to websites and optional tasks.</span></span> <span data-ttu-id="0f25c-223">Обратите внимание, что задачи поддержки могут быть только ссылками на веб-сайты, но задачи воспроизведения можно использовать и для дополнительных задач поддержки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-223">Note that support tasks can be only links to Web sites, but play tasks can be used for optional support tasks as well.</span></span>

<span data-ttu-id="0f25c-224">Обозреватель игр может использовать растровое изображение эскиза, но рекомендуется вместо этого указать ресурс значка Windows с большими значками (256 256).</span><span class="sxs-lookup"><span data-stu-id="0f25c-224">Games Explorer can make use of a thumbnail bitmap image, but it is recommended that, instead, you provide a Windows icon resource with large icons (256 256).</span></span> <span data-ttu-id="0f25c-225">Ресурс значка должен включать размеры изображений 256 256 48 48, 32 32 и 16 16 в 24-разрядных (True Color) и 8-битных (256) цветах.</span><span class="sxs-lookup"><span data-stu-id="0f25c-225">The icon resource should include image sizes of 256 256 48 48, 32 32, and 16 16 in both 24-bit (True Color) and 8-bit (256) color depths.</span></span> <span data-ttu-id="0f25c-226">Редактор значков, предоставляемый в Visual Studio 2008 и 2010, поддерживает такие форматы крупных значков, как и Иконворкшоп Lite.</span><span class="sxs-lookup"><span data-stu-id="0f25c-226">The icon editor provided in Visual Studio 2008 and 2010 supports these large icon formats, as does IconWorkshop Lite.</span></span>

<span data-ttu-id="0f25c-227">Сведения об интеграции с **проводником игр Windows** приведены в пакете DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="0f25c-227">Details on integrating with **Windows Games Explorer** are provided in the DirectX SDK.</span></span> <span data-ttu-id="0f25c-228">Пакет SDK для DirectX включает редактор файла определения игры (ГДФ), а также пример ГДФ, включенный в Гдфексамплебинари — пример.</span><span class="sxs-lookup"><span data-stu-id="0f25c-228">The DirectX SDK includes a game definition file (GDF) editor, as well as an example GDF that is included in GDFExampleBinary, a sample.</span></span> <span data-ttu-id="0f25c-229">Другой пример, Гамеуксинсталлхелпер, предоставляет подпрограммы для интеграции требуемых функций в существующие системы установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-229">Another sample, GameUxInstallHelper, provides routines for integrating the required functionality into existing installation systems.</span></span> <span data-ttu-id="0f25c-230">Проверяющий элемент управления "файл определения игр" (gdftrace.exe) обеспечивает поддержку отладки для оценки ГДФ.</span><span class="sxs-lookup"><span data-stu-id="0f25c-230">The Game Definition File Validator (gdftrace.exe) provides debugging support for evaluating a GDF.</span></span> <span data-ttu-id="0f25c-231">См. также раздел "интеграция проводника игр Windows" в документации по пакету SDK DirectX для C++.</span><span class="sxs-lookup"><span data-stu-id="0f25c-231">Also see "Windows Games Explorer Integration" in the DirectX SDK Documentation for C++.</span></span>

<span data-ttu-id="0f25c-232">В Windows 7 появилась поддержка второй версии схемы для файлов ГДФ.</span><span class="sxs-lookup"><span data-stu-id="0f25c-232">Windows 7 introduces support for the second version of a schema for GDF files.</span></span> <span data-ttu-id="0f25c-233">Новая версия включает упрощенный способ создания задач воспроизведения и поддержки уведомлений об обновлениях, поставщиков услуг игры, статистики игры и RSS-каналов для поставщиков услуг игры.</span><span class="sxs-lookup"><span data-stu-id="0f25c-233">The new version includes a simplified method for creating play tasks and support for update notifications, game service providers, game statistics, and RSS feeds for game service providers.</span></span> <span data-ttu-id="0f25c-234">Последняя версия Гамеуксинсталлхелпер обрабатывает всю регистрацию и поддержку устаревших версий, необходимую для использования файла ГДФ версии 2 с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0f25c-234">The latest version of GameUxInstallHelper handles all of the registration and legacy support needed to use a version 2 GDF file with Windows Vista.</span></span> <span data-ttu-id="0f25c-235">Используйте средства и примеры кода из пакета SDK DirectX с 2009 августа или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0f25c-235">Use the tools and sample code from the DirectX SDK from August 2009 or later.</span></span> <span data-ttu-id="0f25c-236">Рекомендуется использовать файл ГДФ версии 2, чтобы обеспечить поддержку RSS-каналов, статистики игр и уведомлений об обновлениях.</span><span class="sxs-lookup"><span data-stu-id="0f25c-236">Using a version 2 GDF file is recommended to enable support for RSS feeds, game statistics, and update notifications.</span></span> <span data-ttu-id="0f25c-237">См. также примеры Провидергдфексамплебинари и Гаместатистиксексампле.</span><span class="sxs-lookup"><span data-stu-id="0f25c-237">Also, see the samples ProviderGDFExampleBinary and GameStatisticsExample.</span></span>

<span data-ttu-id="0f25c-238">В Windows Vista Business Edition, Windows 7 Профессиональная Edition и Enterprise Edition как Windows Vista, так и Windows 7, ссылка "игры" в меню "Пуск" скрыта.</span><span class="sxs-lookup"><span data-stu-id="0f25c-238">On Windows Vista Business Edition, Windows 7 Professional Edition, and Enterprise Edition of both Windows Vista and Windows 7, the Games link on the Start menu is hidden.</span></span> <span data-ttu-id="0f25c-239">Обозреватель игр по-прежнему доступен в меню Пуск, если щелкнуть **все программы**, а затем выбрать **игры**.</span><span class="sxs-lookup"><span data-stu-id="0f25c-239">Games Explorer is still available on the Start menu by clicking **All Programs**, and then clicking **Games**.</span></span>

<span data-ttu-id="0f25c-240">Для связанных приложений, установленных вместе с игрой, но не для игр, вы можете создавать группы программ меню «Пуск», ярлыки и значки рабочего стола во всех версиях Windows, включая Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-240">For associated applications that are installed with your game, but not themselves games, you are free to create Start menu program groups, shortcuts, and desktop icons on all versions of Windows, including Windows Vista and Windows 7.</span></span> <span data-ttu-id="0f25c-241">Такие связанные приложения должны передавать соответствующие игры для требований Windows. Дополнительные сведения см. в разделе [рекомендации по программному обеспечению для игр](#guidelines-for-game-middleware-products).</span><span class="sxs-lookup"><span data-stu-id="0f25c-241">Such associated applications should pass applicable Games for Windows requirements; for details, see [Guidelines for Game Middleware Products](#guidelines-for-game-middleware-products).</span></span> <span data-ttu-id="0f25c-242">Игровым службам рекомендуется зарегистрироваться в обозревателе игр как поставщик игр для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-242">Game services are encouraged to register with Games Explorer as a Game Provider for Windows 7.</span></span> <span data-ttu-id="0f25c-243">1</span><span class="sxs-lookup"><span data-stu-id="0f25c-243">1</span></span>

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a><span data-ttu-id="0f25c-244">1,2. Поддержка семейной безопасности и родительского контроля</span><span class="sxs-lookup"><span data-stu-id="0f25c-244">1.2 Support Family Safety / Parental Controls</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-245"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-245"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-246">Игры должны полностью поддерживать безопасность семейства Windows, применяя следующие правила.</span><span class="sxs-lookup"><span data-stu-id="0f25c-246">Games must fully support Windows Family Safety by adhering to the following rules:</span></span>

-   <span data-ttu-id="0f25c-247">Игры не должны требовать от пользователя наличия учетных данных администратора для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0f25c-247">Games must not require that the user have administrative credentials to play.</span></span> <span data-ttu-id="0f25c-248">Для установки, исправления и удаления могут потребоваться учетные данные администратора в соответствии с требованиями, описанными в разделе 3.</span><span class="sxs-lookup"><span data-stu-id="0f25c-248">Installation, patching, and removal can require administrative credentials, subject to the requirements in section 3.</span></span> <span data-ttu-id="0f25c-249">(Связанное с этим требованием 2,1, следуйте рекомендациям по контролю учетных записей пользователей.)</span><span class="sxs-lookup"><span data-stu-id="0f25c-249">(Related to this is requirement 2.1, Follow User Account Control Guidelines.)</span></span>
-   <span data-ttu-id="0f25c-250">Игры, оцененные с помощью поддерживаемых Windows плат оценки, таких как ЕСРБ и ПЕГИ, должны включать свои назначенные сведения о рейтингах в файл определения игры (ГДФ).</span><span class="sxs-lookup"><span data-stu-id="0f25c-250">Games rated by Windows-supported ratings boards, such as ESRB and PEGI, must include their assigned ratings information in their game definition file (GDF).</span></span> <span data-ttu-id="0f25c-251">Все доступные данные рейтинга должны включаться в каждую локализованную версию ГДФ, а также в версию, не зависящую от языка.</span><span class="sxs-lookup"><span data-stu-id="0f25c-251">All available ratings data must be included in every localized version of the GDF, as well as in the language-neutral version.</span></span>
-   <span data-ttu-id="0f25c-252">Игры должны перечислять свои исполняемые файлы в ГДФ, чтобы обеспечить удобство работы пользователей для общих ограничений приложений, если в игре не используется технология борьбы с пиратством, которая создает исполняемые файлы с произвольным именем во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="0f25c-252">Games must list their executables in the GDF to provide a good user experience for General Application Restrictions, unless the game uses an anti-piracy technology that creates randomly named executables at runtime.</span></span>
-   <span data-ttu-id="0f25c-253">Игры должны вызвать метод **VerifyAccess** интерфейса обозревателя игр во время запуска, если он доступен, и выйти, если он возвращает \* пфхасакцесс как false.</span><span class="sxs-lookup"><span data-stu-id="0f25c-253">Games must call the **VerifyAccess** method of the Games Explorer interface during startup, if available, and exit if it returns \*pfHasAccess as FALSE.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-254"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-254"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-255">Все игры должны выполняться в контексте учетной записи обычного пользователя, чтобы разрешить учетным записям, управляемым с помощью родительского контроля Windows, играть игру.</span><span class="sxs-lookup"><span data-stu-id="0f25c-255">All games must execute within the context of a Standard User account to allow accounts that are controlled by Windows Parental Controls to play the game.</span></span> <span data-ttu-id="0f25c-256">Родители хотят отслеживать и контролировать доступ детей к играм.</span><span class="sxs-lookup"><span data-stu-id="0f25c-256">Parents want the ability to monitor and control their children's access to games.</span></span> <span data-ttu-id="0f25c-257">Более того, многочисленные группы отраслей, правительственных учреждений и представительства хотят лучше разрешать родителям отслеживать и контролировать игры, к которым открываются их дети.</span><span class="sxs-lookup"><span data-stu-id="0f25c-257">Moreover, numerous industry, government and advocacy groups desire better ways to allow parents to monitor and control the games to which their children are exposed.</span></span> <span data-ttu-id="0f25c-258">В сочетании с архитектурой, предлагаемой обозревателем игр, корпорация Майкрософт предоставляет родителям эту возможность с помощью родительского контроля Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-258">In conjunction with the architecture offered by Games Explorer, Microsoft provides parents this ability through Windows Parental Controls.</span></span>

<span data-ttu-id="0f25c-259">Даже для игр, которые не участвуют в программе оценки, необходимость повышенных привилегий создает низкое качество воспроизведения для большинства учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="0f25c-259">Even for games that do not participate in a ratings board program, requiring elevated privileges creates a poor play experience for the majority of user accounts.</span></span> <span data-ttu-id="0f25c-260">Это особенно важно в том случае, если родительский контроль включен, что потребует от родительского входа вводить пароль администратора при каждом запуске игры.</span><span class="sxs-lookup"><span data-stu-id="0f25c-260">This is particularly the case if Parental Controls are enabled, which would require the parent to enter the administrator password every time the game is launched.</span></span>

<span data-ttu-id="0f25c-261">Система родительского контроля Windows позволяет родителям выбирать оценки, которые они считают подходящими для своих детей.</span><span class="sxs-lookup"><span data-stu-id="0f25c-261">The Windows Parental Controls system allows parents to select the ratings that they believe are appropriate for their children.</span></span> <span data-ttu-id="0f25c-262">Родительский контроль поддерживает многие системы оценок в разных странах мира.</span><span class="sxs-lookup"><span data-stu-id="0f25c-262">Parental Controls support many of the worldwide ratings systems.</span></span> <span data-ttu-id="0f25c-263">Родительский контроль также позволяет родителям ограничивать доступ к играм на основе дескрипторов содержимого (если соответствующая система оценки поддерживает их) и разрешает или запрещает доступ к отдельным играм.</span><span class="sxs-lookup"><span data-stu-id="0f25c-263">Parental Controls also allow parents to restrict access to games based on Content Descriptors (if the applicable rating system supports them) and to allow or disallow access to individual games.</span></span>

<span data-ttu-id="0f25c-264">Выбор системы оценок по умолчанию для родительского контроля Windows основан на параметрах национальной настройки системы, но может быть изменен пользователем в окне «Язык **и региональные стандарты** **» панели управления**.</span><span class="sxs-lookup"><span data-stu-id="0f25c-264">The default choice of rating system for Windows Parental Controls is based on the system's locale setting, but can be modified by the user in **Regional and Language Options** in **Control Panel**.</span></span> <span data-ttu-id="0f25c-265">Таким образом, каждый поддерживаемый язык должен предоставлять все доступные данные рейтинга, чтобы пользователь предоставил свободу выбора любой доски оценки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-265">Therefore, every supported language should provide all available ratings data so that the user has the freedom to select whatever ratings board they desire.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-266"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-266"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-267">Игры без оценки должны по-прежнему соответствовать требованиям к поддержке Play в качестве обычного пользователя и вызывать **VerifyAccess**.</span><span class="sxs-lookup"><span data-stu-id="0f25c-267">Games without a rating must still meet the requirements to support play as a Standard User and to call **VerifyAccess**.</span></span> <span data-ttu-id="0f25c-268">В таких играх по умолчанию используется категория категории без оценки, в обозревателе игр отображается текст "не указана оценка" и действуют **ограничения игры** в **родительских элементах управления** для игр без категорий.</span><span class="sxs-lookup"><span data-stu-id="0f25c-268">Such games default to the Unrated category, display the text "No Rating Provided" in Games Explorer, and are subject to the **Game Restrictions** setting in **Parental Controls** for unrated games.</span></span> <span data-ttu-id="0f25c-269">Значение **ограничений** по умолчанию — Allow.</span><span class="sxs-lookup"><span data-stu-id="0f25c-269">The default **Restrictions** setting is Allow.</span></span>

<span data-ttu-id="0f25c-270">Сведения о рейтинге в ГДФ будут пропущены, если содержащий их двоичный файл не подписан должным образом с помощью Authenticode.</span><span class="sxs-lookup"><span data-stu-id="0f25c-270">Rating information in the GDF will be ignored if the containing binary is not properly Authenticode signed.</span></span> <span data-ttu-id="0f25c-271">См. требование 2,3.</span><span class="sxs-lookup"><span data-stu-id="0f25c-271">See requirement 2.3.</span></span>

<span data-ttu-id="0f25c-272">Редактор файлов определения игр в пакете SDK DirectX включает все поддерживаемые системы оценок и правильно реплицирует эти сведения во все локализованные версии ГДФ, а также на языке, не зависящем от языка.</span><span class="sxs-lookup"><span data-stu-id="0f25c-272">The Game Definition File Editor in the DirectX SDK includes all supported ratings systems and will correctly replicate this information to all localized versions of the GDF, as well as a language neutral version.</span></span> <span data-ttu-id="0f25c-273">Средство Гдфтраце декодирует и проверяет все имеющиеся сведения об оценках.</span><span class="sxs-lookup"><span data-stu-id="0f25c-273">The GDFTrace tool will decode and verify all ratings information present.</span></span> <span data-ttu-id="0f25c-274">Используйте эти средства в качестве версии 2009 августа или более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="0f25c-274">Use the August 2009 version or later of these tools.</span></span>

<span data-ttu-id="0f25c-275">ГДФ для поставщика игр, как правило, не содержит сведений о рейтинге и подчиняется параметрам для содержимого без оценки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-275">The GDF for a game provider typically contains no rating information, and it is subject to the settings for unrated content.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0f25c-276">Операционная система</span><span class="sxs-lookup"><span data-stu-id="0f25c-276">Operating System</span></span></th>
<th><span data-ttu-id="0f25c-277">Поддерживаемые системы оценок</span><span class="sxs-lookup"><span data-stu-id="0f25c-277">Supported rating systems</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f25c-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f25c-278">Windows Vista</span></span></td>
<td><ul>
<li><span data-ttu-id="0f25c-279">ЦЕРО (Япония)</span><span class="sxs-lookup"><span data-stu-id="0f25c-279">CERO (Japan)</span></span></li>
<li><span data-ttu-id="0f25c-280">ЕСРБ (США)</span><span class="sxs-lookup"><span data-stu-id="0f25c-280">ESRB (USA)</span></span></li>
<li><span data-ttu-id="0f25c-281">ОФЛК (Австралия)</span><span class="sxs-lookup"><span data-stu-id="0f25c-281">OFLC (Australia)</span></span></li>
<li><span data-ttu-id="0f25c-282">ПЕГИ (Европа)</span><span class="sxs-lookup"><span data-stu-id="0f25c-282">PEGI (Europe)</span></span></li>
<li><span data-ttu-id="0f25c-283">ПЕГИ Финляндия (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="0f25c-283">PEGI Finland (deprecated)</span></span></li>
<li><span data-ttu-id="0f25c-284">ПЕГИ Португалия</span><span class="sxs-lookup"><span data-stu-id="0f25c-284">PEGI Portugal</span></span></li>
<li><span data-ttu-id="0f25c-285">ПЕГИ/ББФК (Великобритания)</span><span class="sxs-lookup"><span data-stu-id="0f25c-285">PEGI/BBFC (United Kingdom)</span></span></li>
<li><span data-ttu-id="0f25c-286">УСК (Германия)</span><span class="sxs-lookup"><span data-stu-id="0f25c-286">USK (Germany)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f25c-287">Windows Vista с пакетом обновления</span><span class="sxs-lookup"><span data-stu-id="0f25c-287">Windows Vista with a service pack</span></span></td>
<td><span data-ttu-id="0f25c-288">В пакетах обновления для Windows Vista добавлена поддержка следующих служб:</span><span class="sxs-lookup"><span data-stu-id="0f25c-288">Service packs for Windows Vista add support for the following:</span></span><br/>
<ul>
<li><span data-ttu-id="0f25c-289">ГРБ (Южная Корея)</span><span class="sxs-lookup"><span data-stu-id="0f25c-289">GRB (South Korea)</span></span></li>
<li><span data-ttu-id="0f25c-290">ЕСРБ, &quot; умеренные &quot; дескрипторы содержимого (умеренно)</span><span class="sxs-lookup"><span data-stu-id="0f25c-290">ESRB &quot;Mild&quot; variant content descriptors</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f25c-291">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f25c-291">Windows 7</span></span></td>
<td><span data-ttu-id="0f25c-292">Windows 7 поддерживает системы оценок, поддерживаемые Windows Vista, и добавляет поддержку следующих систем:</span><span class="sxs-lookup"><span data-stu-id="0f25c-292">Windows 7 supports the ratings systems supported by Windows Vista and adds support for the following:</span></span> <br/>
<ul>
<li><span data-ttu-id="0f25c-293">КСРР (Тайвань)</span><span class="sxs-lookup"><span data-stu-id="0f25c-293">CSRR (Taiwan)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f25c-294">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0f25c-294">Windows 8</span></span></td>
<td><span data-ttu-id="0f25c-295">Windows 8 поддерживает предыдущие системы оценок и добавляет поддержку следующих систем:</span><span class="sxs-lookup"><span data-stu-id="0f25c-295">Windows 8 supports the previous ratings systems and adds support for the following:</span></span><br/>
<ul>
<li><span data-ttu-id="0f25c-296">Коб — AU (Австралия)</span><span class="sxs-lookup"><span data-stu-id="0f25c-296">COB-AU (Australia)</span></span></li>
<li><span data-ttu-id="0f25c-297">ДЖКТК (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="0f25c-297">DJCTQ (Brazil)</span></span></li>
<li><span data-ttu-id="0f25c-298">ПФБ (Южная Африка)</span><span class="sxs-lookup"><span data-stu-id="0f25c-298">PFB (South Africa)</span></span></li>
<li><span data-ttu-id="0f25c-299">ОФЛК-NZ (Новая Зеландия)</span><span class="sxs-lookup"><span data-stu-id="0f25c-299">OFLC-NZ (New Zealand)</span></span></li>
</ul>
<span data-ttu-id="0f25c-300">Windows 8 отменяет поддержку следующих нерекомендуемых систем:</span><span class="sxs-lookup"><span data-stu-id="0f25c-300">Windows 8 retires support for the following now deprecated systems:</span></span><br/>
<ul>
<li><span data-ttu-id="0f25c-301">ПЕГИ-FI (Финляндия)</span><span class="sxs-lookup"><span data-stu-id="0f25c-301">PEGI-FI (Finland)</span></span></li>
<li><span data-ttu-id="0f25c-302">ОФЛК (Австралия)</span><span class="sxs-lookup"><span data-stu-id="0f25c-302">OFLC (Australia)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="0f25c-303">Любое название, включающее в себя новые дескрипторы содержимого ЕСРБ Windows Vista с пакетом обновления 1 (SP1), будет отображаться как неоцененное в Windows Vista без пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="0f25c-303">Any title that includes new ESRB Windows Vista Service Pack 1 (SP1) content descriptors will show as  Unrated  on Windows Vista without a service pack.</span></span>

 

<span data-ttu-id="0f25c-304">Более новые данные оценок игнорируются в версиях операционных систем без их поддержки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-304">Newer ratings data are ignored on versions of operating systems without support for them.</span></span> <span data-ttu-id="0f25c-305">Вариант ПЕГИ (Финляндии) теперь является нерекомендуемым в пользу стандартной системы оценки ПЕГИ (Европа).</span><span class="sxs-lookup"><span data-stu-id="0f25c-305">The PEGI (Finland) variant is now deprecated in favor of the standard PEGI (Europe) rating system.</span></span> <span data-ttu-id="0f25c-306">Теперь система ОФЛК нерекомендуема в пользу КОБ-AU для Австралии.</span><span class="sxs-lookup"><span data-stu-id="0f25c-306">The OFLC system is now deprecated in favor of COB-AU for Australia.</span></span>

<span data-ttu-id="0f25c-307">Дополнительные сведения о том, как сделать игру совместимой с правами обычного пользователя, см. в статье DirectX [Управление учетными записями пользователей для разработчиков игр](/windows/desktop/DxTechArts/user-account-control-for-game-developers).</span><span class="sxs-lookup"><span data-stu-id="0f25c-307">For more information about making a game compatible with standard user privileges, see the DirectX article [User Account Control for Game Developers](/windows/desktop/DxTechArts/user-account-control-for-game-developers).</span></span>

<span data-ttu-id="0f25c-308">Дополнительные сведения о файле определения игры (ГДФ) см. в описании требования 1,1.</span><span class="sxs-lookup"><span data-stu-id="0f25c-308">See requirement 1.1 for more details on the game definition file (GDF).</span></span>

</dd> </dl>

### <a name="13-support-rich-saved-games"></a><span data-ttu-id="0f25c-309">1,3 поддержка полнофункциональных сохраненных игр</span><span class="sxs-lookup"><span data-stu-id="0f25c-309">1.3 Support Rich Saved Games</span></span>

<span data-ttu-id="0f25c-310">\[Это требование было снято с учета\]</span><span class="sxs-lookup"><span data-stu-id="0f25c-310">\[This requirement has been retired\]</span></span>

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="0f25c-311">1,4. Поддержка общего контроллера Xbox 360 для \[ условного требования Windows\]</span><span class="sxs-lookup"><span data-stu-id="0f25c-311">1.4 Support the Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-312"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-312"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-313">Игры, поддерживающие контроллеры игровых устройств, должны поддерживать контроллер Xbox 360 для Windows с помощью API [ксинпут](/windows/desktop/xinput/xinput-game-controller-apis-portal) .</span><span class="sxs-lookup"><span data-stu-id="0f25c-313">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) API.</span></span> <span data-ttu-id="0f25c-314">Если также поддерживаются периферийные устройства Директинпут, можно также использовать Директинпут.</span><span class="sxs-lookup"><span data-stu-id="0f25c-314">If DirectInput peripherals are also supported, then DirectInput can also be used.</span></span> <span data-ttu-id="0f25c-315">Однако Ксинпут должен быть API по умолчанию, если используется устройство, совместимое с Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="0f25c-315">However, XInput must be the default API if an Xbox 360 compatible device is used.</span></span>

<span data-ttu-id="0f25c-316">Все ссылки на общие триггеры контроллера и кнопки должны использовать имена Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="0f25c-316">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span> <span data-ttu-id="0f25c-317">Дополнительные сведения см. в списке [терминология общего контроллера Xbox 360 для Windows](#xbox-360-common-controller-for-windows-terminology) .</span><span class="sxs-lookup"><span data-stu-id="0f25c-317">See the [Xbox 360 Common Controller for Windows Terminology](#xbox-360-common-controller-for-windows-terminology) list for details.</span></span>

<span data-ttu-id="0f25c-318">Вибрация контроллера необходимо отключить, если игра находится в приостановленном или приостановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="0f25c-318">Controller vibration must be turned off when the game is in a paused or suspended state.</span></span>

<span data-ttu-id="0f25c-319">Управление мышью и клавиатурой не может быть полностью отключено в любой момент.</span><span class="sxs-lookup"><span data-stu-id="0f25c-319">Mouse/keyboard control cannot be fully disabled at any time.</span></span> <span data-ttu-id="0f25c-320">Как минимум, должна быть доступна возможность вернуться в меню игры.</span><span class="sxs-lookup"><span data-stu-id="0f25c-320">At a minimum, an option to return to game menus must be available.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-321"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-321"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-322">Это требование дает игрокам свободу выбора контроллера Xbox 360 или клавиатуры и мыши в зависимости от того, какой метод ввода является более естественным и интуитивным интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="0f25c-322">This requirement gives gamers freedom of choice to use either the Xbox 360 controller or the keyboard and mouse, depending on which input method is more natural and intuitive interface.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-323"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-323"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-324">Это требование не относится к играм, использующим только мышь и (или) клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="0f25c-324">This requirement does not apply to games that use only the mouse and/or the keyboard.</span></span>

<span data-ttu-id="0f25c-325">Рекомендуется реализовать навигацию по меню для использования широко принятых кнопок стандартного контроллера:</span><span class="sxs-lookup"><span data-stu-id="0f25c-325">We recommend that menu navigation be implemented to use the widely accepted standard controller buttons:</span></span>

-   <span data-ttu-id="0f25c-326">A — принять</span><span class="sxs-lookup"><span data-stu-id="0f25c-326">A - Accept</span></span>
-   <span data-ttu-id="0f25c-327">B — Отмена</span><span class="sxs-lookup"><span data-stu-id="0f25c-327">B - Cancel</span></span>
-   <span data-ttu-id="0f25c-328">Начало — принять или приостановить</span><span class="sxs-lookup"><span data-stu-id="0f25c-328">Start - Accept or pause</span></span>
-   <span data-ttu-id="0f25c-329">Обратная Отмена, переход на один экран или вверх на уровне меню</span><span class="sxs-lookup"><span data-stu-id="0f25c-329">Back - Cancel, back one screen or up a menu level</span></span>

<span data-ttu-id="0f25c-330">Дополнительные сведения см. в разделе [ксинпут](/windows/desktop/xinput/xinput-game-controller-apis-portal).</span><span class="sxs-lookup"><span data-stu-id="0f25c-330">For more info, see [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal).</span></span>

<span data-ttu-id="0f25c-331">В разделе [ксинпут и директинпут](/windows/desktop/xinput/xinput-and-directinput) обсуждаются проблемы одновременного использования обоих API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-331">The topic [XInput and DirectInput](/windows/desktop/xinput/xinput-and-directinput) discusses issues with using both APIs at the same time.</span></span>

<span data-ttu-id="0f25c-332">Не рекомендуется использовать Директинпут для реализации элементов управления "клавиатура" или "мышь".</span><span class="sxs-lookup"><span data-stu-id="0f25c-332">It is recommended that DirectInput not be used to implement keyboard or mouse controls.</span></span> <span data-ttu-id="0f25c-333">Клавиши и элементы управления мыши должны быть реализованы только с помощью сообщений Windows и API-интерфейсов Win32.</span><span class="sxs-lookup"><span data-stu-id="0f25c-333">Keyboard and mouse controls should only be implemented using Windows messages and Win32 APIs.</span></span> <span data-ttu-id="0f25c-334">Дополнительные сведения о получении сведений о перемещении мыши с высоким разрешением без использования Директинпут см. в статье [использование преимуществ High-Definition перемещения мыши](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement).</span><span class="sxs-lookup"><span data-stu-id="0f25c-334">For details on getting high-resolution mouse movement information without using DirectInput, see [Taking Advantage of High-Definition Mouse Movement](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement).</span></span>

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="0f25c-335">1,5 поддержка нескольких пропорций и разрешений</span><span class="sxs-lookup"><span data-stu-id="0f25c-335">1.5 Support Multiple Aspect Ratios and Resolutions</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-336"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-336"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-337">Игра должна поддерживать по крайней мере следующие пропорции и связанные с ними разрешения экрана:</span><span class="sxs-lookup"><span data-stu-id="0f25c-337">The game must support at least the following aspect ratios and associated screen resolutions:</span></span>

-   <span data-ttu-id="0f25c-338">4:3 обычная (800 600 или 1024 768)</span><span class="sxs-lookup"><span data-stu-id="0f25c-338">4:3 normal (800 600 or 1024 768)</span></span>
-   <span data-ttu-id="0f25c-339">Широкоэкранный дисплей 16:9 (1280 720)</span><span class="sxs-lookup"><span data-stu-id="0f25c-339">16:9 widescreen (1280 720)</span></span>
-   <span data-ttu-id="0f25c-340">Широкоэкранный дисплей 16:10 (1152 720 или 1680 1050 или 800 480)</span><span class="sxs-lookup"><span data-stu-id="0f25c-340">16:10 widescreen (1152 720 or 1680 1050 or 800 480)</span></span>

<span data-ttu-id="0f25c-341">При настройке разрешения экрана и обнаружении игры должны соответствовать следующим правилам.</span><span class="sxs-lookup"><span data-stu-id="0f25c-341">For screen resolution configuration and detection, the game must adhere to the following rules:</span></span>

-   <span data-ttu-id="0f25c-342">В игре по умолчанию используется разрешение рабочего стола устройства дисплея, если это решение поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0f25c-342">The game uses the desktop resolution of the display device by default if it is a supported resolution.</span></span> <span data-ttu-id="0f25c-343">Пропорции рабочего стола должны использоваться в качестве критерия поиска, если игра выбирает другое разрешение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f25c-343">The desktop aspect ratio must be used as a search criterion if the game chooses a different default resolution.</span></span>
-   <span data-ttu-id="0f25c-344">Игра должна запрашивать у пользователя подтверждение новых параметров экрана при внесении изменений.</span><span class="sxs-lookup"><span data-stu-id="0f25c-344">The game must prompt the user to confirm new display settings when a change is made.</span></span> <span data-ttu-id="0f25c-345">Если пользователь не принимает значение в течение 15 секунд, он должен вернуться к предыдущему параметру.</span><span class="sxs-lookup"><span data-stu-id="0f25c-345">If the user does not accept within 15 seconds, the display must revert to the previous setting.</span></span>
-   <span data-ttu-id="0f25c-346">Игра не должна растягивать Пиксели или центрировать окно отрисовки 4:3 для поддержки широкоэкранных пропорций.</span><span class="sxs-lookup"><span data-stu-id="0f25c-346">The game must not stretch pixels or center a 4:3 render window to support widescreen aspect ratios.</span></span> <span data-ttu-id="0f25c-347">Однако пустых является приемлемым.</span><span class="sxs-lookup"><span data-stu-id="0f25c-347">However, letterboxing is acceptable.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-348"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-348"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-349">В Windows 3D Desktop можно предположить, что определенные пропорции или разрешение не могут быть приняты из-за следующих факторов:</span><span class="sxs-lookup"><span data-stu-id="0f25c-349">With the Windows 3D desktop, a particular aspect ratio or resolution cannot be assumed, because of the following factors:</span></span>

-   <span data-ttu-id="0f25c-350">Поддержка подробных экранов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-350">Support for high-detail displays.</span></span>
-   <span data-ttu-id="0f25c-351">Увеличенная доля рынка широкоэкранных мониторов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-351">Increased market share of widescreen monitors.</span></span>
-   <span data-ttu-id="0f25c-352">Развертывания ТВВЧ для Windows Media Center.</span><span class="sxs-lookup"><span data-stu-id="0f25c-352">HDTV deployments for Windows Media Center.</span></span>
-   <span data-ttu-id="0f25c-353">Требования к специальным возможностям.</span><span class="sxs-lookup"><span data-stu-id="0f25c-353">Accessibility requirements.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-354"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-354"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-355">В идеале в игре по умолчанию используется собственная пропорция экрана.</span><span class="sxs-lookup"><span data-stu-id="0f25c-355">Ideally, the game defaults to the native aspect ratio of the display.</span></span> <span data-ttu-id="0f25c-356">Тем не менее, надежное получение этих сведений может быть сложной задачей, поэтому в качестве более общего решения для игры можно предположить, что настольный компьютер работает с исходными пропорциями.</span><span class="sxs-lookup"><span data-stu-id="0f25c-356">However, obtaining this information reliably can be a challenge, so as a more general solution the game can assume that the desktop is running at the native aspect ratio.</span></span> <span data-ttu-id="0f25c-357">Разрешение рабочего стола можно получить, вызвав [**енумдисплайсеттингс**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) с \_ параметрами реестра Enum \_ .</span><span class="sxs-lookup"><span data-stu-id="0f25c-357">The desktop resolution can be obtained by calling [**EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) with ENUM\_REGISTRY\_SETTINGS.</span></span>

<span data-ttu-id="0f25c-358">Дополнительные сведения см. в разделах «пропорции» и «широкоэкранный дисплей» статьи DirectX [Введение в 10-футовый интерфейс для разработчиков игр Windows](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).</span><span class="sxs-lookup"><span data-stu-id="0f25c-358">For more details, see the Aspect Ratio and Widescreen sections of the DirectX article [Introduction to the 10-Foot Experience for Windows Game Developers](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).</span></span>

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a><span data-ttu-id="0f25c-359">1,6. Поддержка запуска из Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="0f25c-359">1.6 Support Launch from Windows Media Center</span></span>

<span data-ttu-id="0f25c-360">\[Это требование было снято с учета.\]</span><span class="sxs-lookup"><span data-stu-id="0f25c-360">\[This requirement has been retired.\]</span></span>

### <a name="17-direct3d-support"></a><span data-ttu-id="0f25c-361">1,7 поддержка Direct3D</span><span class="sxs-lookup"><span data-stu-id="0f25c-361">1.7 Direct3D Support</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-362"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-362"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-363">Если в игре используется Direct3D, минимальная поддерживаемая версия должна быть Direct3D 9, а Direct3D — модулем подготовки отчетов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f25c-363">If the game uses Direct3D, then the minimum version supported must be Direct3D 9, and Direct3D must be the default renderer selected.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-364"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-364"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-365">Базовая графическая архитектура Windows Vista и Windows 7 разработана на основе Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0f25c-365">The Windows Vista and Windows 7 core graphics architecture is designed around Direct3D.</span></span> <span data-ttu-id="0f25c-366">Direct3D 8 и более ранние версии поддерживаются путем повторного сопоставления устаревших интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-366">Direct3D 8 and earlier versions are supported by remapping legacy interfaces.</span></span>

<span data-ttu-id="0f25c-367">Настоятельно рекомендуется использовать более новые версии Direct3D, чем Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="0f25c-367">Use of versions of Direct3D newer than Direct3D 9 is strongly encouraged.</span></span> <span data-ttu-id="0f25c-368">Ознакомьтесь с играми для демонстрации Windows S. 1.</span><span class="sxs-lookup"><span data-stu-id="0f25c-368">See the Games for Windows Showcase S.1.</span></span> <span data-ttu-id="0f25c-369">Требование Direct3D 10 или Direct3D 11 полностью соответствует требованию 1,7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-369">Requiring Direct3D 10 or Direct3D 11 is fully compliant with requirement 1.7.</span></span>

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="0f25c-370">1,8. Включение высокого разрешения</span><span class="sxs-lookup"><span data-stu-id="0f25c-370">1.8 Enable High-DPI-Aware</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-371"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-371"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-372">Игры и их установщики должны правильно работать без визуальных проблем, если включено масштабирование с точками на дюйм (с разрешением 144 DPI для 150% масштабирования при разрешении экрана 1600 1200) в Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-372">Games and their installers must run correctly without visual problems when dots-per-inch (DPI) scaling is enabled (tested with 144 DPI for 150% scaling at display resolution of 1600 1200) on Windows Vista and Windows 7.</span></span>

<span data-ttu-id="0f25c-373">Для этого, как правило, требуется, чтобы исполняемый файл был объявлен с учетом DPI.</span><span class="sxs-lookup"><span data-stu-id="0f25c-373">This typically requires the game executable to declare being DPI-aware.</span></span> <span data-ttu-id="0f25c-374">Это достигается путем встраивания элемента манифеста: <dpiAware> true <dpiAware> .</span><span class="sxs-lookup"><span data-stu-id="0f25c-374">This is accomplished by embedding a manifest element: <dpiAware>true<dpiAware> .</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-375"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-375"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-376">Высококачественные ЖК-мониторы являются представлением компьютеров, и их лучше всего использовать при их собственных разрешениях (обычно 1280 1024, 1600 1200 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="0f25c-376">High-quality LCD monitors are commonplace as computer displays, and they look best when driven at their native resolutions (typically 1280 1024, 1600 1200, and so on).</span></span> <span data-ttu-id="0f25c-377">Клиенты, которые испытывают трудности при чтении текста и просмотре изображений в этом разрешении, часто применяют к настольным компьютерам более низкую разрешающую способность, а визуальные артефакты —</span><span class="sxs-lookup"><span data-stu-id="0f25c-377">Customers who have difficulty reading text and seeing images at this resolution often set their computer desktops to a lower resolution and suffer visual artifacts from LCD scaling.</span></span> <span data-ttu-id="0f25c-378">Вместо этого клиенты могут оставить разрешение на собственный размер и изменить значение DPI на экране Windows, таким образом выполняя внешний вид элемента и текста без ущерба для качества изображения.</span><span class="sxs-lookup"><span data-stu-id="0f25c-378">Instead, customers can leave the resolution at the native size and change the DPI of the Windows display, thus making item and text appearance larger without sacrificing image quality.</span></span>

<span data-ttu-id="0f25c-379">Хотя эта функция была доступна в некоторых формах, начиная с Windows XP, она редко включается клиентами или поставщиками вычислительных систем.</span><span class="sxs-lookup"><span data-stu-id="0f25c-379">While this feature has been available in some form since Windows XP, it is seldom enabled by customers or by OEMs.</span></span> <span data-ttu-id="0f25c-380">Сегодня более половины всех мониторов компьютера имеют более низкое разрешение, чем собственное разрешение монитора на основе отзывов пользователей.</span><span class="sxs-lookup"><span data-stu-id="0f25c-380">More than half of all computer displays today are set to a lower resolution than the monitor's native resolution, based on customer feedback.</span></span> <span data-ttu-id="0f25c-381">Windows 7 делает эту функцию значительно более видимой для клиентов во время начальной настройки и при изменении параметров отображения рекомендуется использовать масштабирование DPI вместо изменения разрешения рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="0f25c-381">Windows 7 makes this feature much more visible to customers during initial setup and when changing display settings, encouraging them to use DPI scaling rather than change the desktop resolution.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-382"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-382"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-383">Вместо этого можно использовать функцию [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) , если она вызывается на раннем этапе кода запуска процесса.</span><span class="sxs-lookup"><span data-stu-id="0f25c-383">The [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function can be used instead, if called early in the process startup code.</span></span> <span data-ttu-id="0f25c-384">Рекомендуется добавить в манифест, чтобы убедиться в отсутствии конкуренции с программными элементами (такими как DLL), которые могут быть инициализированы перед вызовом основной точки входа.</span><span class="sxs-lookup"><span data-stu-id="0f25c-384">Adding to the manifest is preferred, to ensure there are no race conditions with software elements (such as DLLs) that might initialize before the main entry point is called.</span></span> <span data-ttu-id="0f25c-385">Обратите внимание, что **сетпроцессдпиаваре** имеется только в Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-385">Note that **SetProcessDPIAware** is only present on Windows Vista and Windows 7.</span></span>

<span data-ttu-id="0f25c-386">Добавить элемент manifest легко с Visual Studio 2005 и 2008; Создайте файл с именем дпиаваре. manifest, содержащий следующий текст:</span><span class="sxs-lookup"><span data-stu-id="0f25c-386">Adding the manifest element is easy to do with Visual Studio 2005 and 2008; create a file named dpiaware.manifest that contains the following text:</span></span>

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

<span data-ttu-id="0f25c-387">Затем в Visual Studio добавьте дпиваре. manifest в проект.</span><span class="sxs-lookup"><span data-stu-id="0f25c-387">Then, inside Visual Studio, add dpiware.manifest to the project.</span></span> <span data-ttu-id="0f25c-388">Убедитесь, что в свойствах проекта для параметра **внедрить манифест** задано значение **Да** .</span><span class="sxs-lookup"><span data-stu-id="0f25c-388">Ensure that **Embed Manifest** is set to **Yes** in the project's properties.</span></span> <span data-ttu-id="0f25c-389">Обратите внимание, что более старые версии средства манифеста (Mt.exe) будут создавать ложные предупреждения с элементами манифеста, поддерживающими DPI.</span><span class="sxs-lookup"><span data-stu-id="0f25c-389">Note that older versions of the Manifest Tool (Mt.exe) will generate a spurious warning with the DPI-aware manifest elements.</span></span> <span data-ttu-id="0f25c-390">Чтобы устранить эту проблему, обновите Mt.exe до последней версии из Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0f25c-390">To resolve this, update Mt.exe to the latest version from the Windows SDK.</span></span>

<span data-ttu-id="0f25c-391">Visual Studio 2010 включает параметр в свойствах проекта с именем **Enable dpi**, что устраняет необходимость в файле, например дпиаваре. manifest.</span><span class="sxs-lookup"><span data-stu-id="0f25c-391">Visual Studio 2010 includes a setting in the project properties, named **Enable DPI Awareness**, that eliminates the need for a file like dpiaware.manifest.</span></span> <span data-ttu-id="0f25c-392">Найдите **параметр Включить отслеживание dpi** путем расширения **свойств конфигурации** и **средства манифеста**, а затем выберите **входные & выходные данные**.</span><span class="sxs-lookup"><span data-stu-id="0f25c-392">Find **Enable DPI Awareness** by expanding **Configuration Properties** and **Manifest Tool**, and then selecting **Input & Output**.</span></span>

<span data-ttu-id="0f25c-393">В Windows в традиционном режиме экрана по умолчанию используется значение 96 DPI, которое было общим для ЭЛТ-мониторов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-393">On Windows, the traditional display mode defaults to 96 DPI, which was common for CRT monitors.</span></span>

<span data-ttu-id="0f25c-394">Хотя полноэкранные приложения изменяют разрешение экрана, они часто используют сообщения и метрики окна при настройке буферов и экранных прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="0f25c-394">While full-screen applications change the display resolution, they often use window messages and metrics when setting up buffers and display rectangles.</span></span> <span data-ttu-id="0f25c-395">Виртуализация DPI приводит к тому, что эти режимы отображения в полноэкранном режиме будут обрезаны, а объявление с учетом DPI не позволит устранить эти проблемы.</span><span class="sxs-lookup"><span data-stu-id="0f25c-395">DPI virtualization causes these full-screen display modes to appear cropped, and declaring DPI-aware will prevent these problems.</span></span> <span data-ttu-id="0f25c-396">Дополнительные сведения см. в разделе [написание DPI-Aware приложений Win32](../hidpi/high-dpi-desktop-application-development-on-windows.md).</span><span class="sxs-lookup"><span data-stu-id="0f25c-396">For more information, see [Writing DPI-Aware Win32 Applications](../hidpi/high-dpi-desktop-application-development-on-windows.md).</span></span>

</dd> </dl>

## <a name="security-and-compatibility"></a><span data-ttu-id="0f25c-397">Безопасность и совместимость</span><span class="sxs-lookup"><span data-stu-id="0f25c-397">Security and Compatibility</span></span>

<span data-ttu-id="0f25c-398">**Сводка требований к безопасности и совместимости**</span><span class="sxs-lookup"><span data-stu-id="0f25c-398">**Summary of Security and Compatibility Requirements**</span></span>

<span data-ttu-id="0f25c-399">**Преимущества для клиентов**</span><span class="sxs-lookup"><span data-stu-id="0f25c-399">**Customer Benefits**</span></span>

<span data-ttu-id="0f25c-400">Следующие требования повышают общую безопасность игр и гарантируют, что они работают с Windows в различных архитектурах, в различных конфигурациях и в разных режимах.</span><span class="sxs-lookup"><span data-stu-id="0f25c-400">The following requirements improve the overall security of games and help ensure that they work with Windows on different architectures, under different configurations, and in different modes.</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="0f25c-401">2,1 Следуйте рекомендациям по контролю учетных записей пользователей</span><span class="sxs-lookup"><span data-stu-id="0f25c-401">2.1 Follow User Account Control Guidelines</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-402"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-402"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-403">Каждый исполняемый файл (то есть каждый файл с расширением .exe) должен содержать внедренный манифест, определяющий его уровень выполнения, включая следующий тег:</span><span class="sxs-lookup"><span data-stu-id="0f25c-403">Every executable file (that is, every file that has a .exe extension) must contain an embedded manifest that defines its execution level by including the following tag:</span></span>

``` syntax
            <requestedExecutionLevel>
```

<span data-ttu-id="0f25c-404">Для каждого требования 1,2 основной исполняемый файл игры и запуска должен иметь уровень выполнения asInvoker для поддержки стандартных контекстов пользователя.</span><span class="sxs-lookup"><span data-stu-id="0f25c-404">Per requirement 1.2, the main game and Autorun executable must have the execution level of asInvoker to support Standard User contexts.</span></span>

<span data-ttu-id="0f25c-405">Файлы пользовательских данных с сопоставлениями файлов, зарегистрированными в проводнике, должны быть помещены во вложенную папку папки, указанной в **файле** CSid \_ ( **документы** или **Мои документы**).</span><span class="sxs-lookup"><span data-stu-id="0f25c-405">User data files that have file associations registered with **File Explorer** must be placed in a subfolder of the folder that is specified by CSIDL\_PERSONAL (also called **Documents** or **My Documents**).</span></span> <span data-ttu-id="0f25c-406">Все остальные файлы данных пользователя должны храниться во вложенной папке папок, заданных \_ локальными файлами \_ AppData или CSid общей папки AppData \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0f25c-406">All other user data files must be stored in a subfolder of the folders that are specified by CSIDL\_LOCAL\_APPDATA or CSIDL\_COMMON\_APPDATA.</span></span> <span data-ttu-id="0f25c-407">(Эти каталоги по умолчанию скрыты для отдельных пользователей и для всех пользователей.)</span><span class="sxs-lookup"><span data-stu-id="0f25c-407">(These directories are hidden by default for individual users and for all users.)</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-408"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-408"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-409">Пользовательский интерфейс Windows является более безопасным, если приложения выполняются только с необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="0f25c-409">A user's Windows experience is more secure if applications run only with the permissions needed.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-410"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-410"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-411">Если только несколько компонентов приложения требуют прав администратора (например, приложение, которому требуется настроить брандмауэр), основной процесс приложения по-прежнему должен выполняться с использованием стандартных привилегий пользователя.</span><span class="sxs-lookup"><span data-stu-id="0f25c-411">If only a few features in an application require administrative privileges (for example, an application that needs to configure a firewall), the main process of the application must still be run by using standard user privileges.</span></span> <span data-ttu-id="0f25c-412">Функции, требующие прав администратора, необходимо переместить в отдельный процесс, например в установщик или программу настройки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-412">Features that require administrative privileges must be moved into a separate process, such as an installer or configuration utility.</span></span>

<span data-ttu-id="0f25c-413">Если права администратора не требуются, внедренный XML-файл манифеста должен включать следующее:</span><span class="sxs-lookup"><span data-stu-id="0f25c-413">If administrative privileges are not required, the embedded manifest XML should include the following:</span></span>

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

<span data-ttu-id="0f25c-414">Если требуются права администратора, внедренный XML-файл манифеста должен включать следующее:</span><span class="sxs-lookup"><span data-stu-id="0f25c-414">If administrative privileges are required, the embedded manifest XML should include the following:</span></span>

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

<span data-ttu-id="0f25c-415">В Visual Studio 2005 это легко внедрить, просто добавив файл манифеста (manifest), содержащий один из предыдущих блоков к проекту, и установив для **манифеста внедрения** значение **Да** в свойствах проекта для средства манифеста.</span><span class="sxs-lookup"><span data-stu-id="0f25c-415">With Visual Studio 2005 this is easily embedded by just adding a manifest (.manifest) file that contains one of the preceding blocks to the project, and ensuring that **Embed Manifest** is set to **Yes** in the project properties for Manifest Tool.</span></span> <span data-ttu-id="0f25c-416">Для Visual Studio 2008 и 2010 свойства контроля учетных записей можно задать непосредственно в свойствах проекта компоновщика на странице **файла манифеста** .</span><span class="sxs-lookup"><span data-stu-id="0f25c-416">For Visual Studio 2008 and 2010, UAC properties can be set directly in the project properties for the linker on the **Manifest File** page.</span></span> <span data-ttu-id="0f25c-417">Обратите внимание, что старые версии средства манифеста (Mt.exe) создают ложное предупреждение с элементами манифеста контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="0f25c-417">Note that older versions of the Manifest Tool (Mt.exe) generate a spurious warning with the UAC manifest elements.</span></span> <span data-ttu-id="0f25c-418">Чтобы устранить эту проблему, обновите Mt.exe до последней версии из Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0f25c-418">To resolve this, update Mt.exe to the latest version from the Windows SDK.</span></span>

<span data-ttu-id="0f25c-419">Дополнительные сведения об отдельных случаях установки, исправления и удаления см. в статье требования 3,1.</span><span class="sxs-lookup"><span data-stu-id="0f25c-419">See requirement 3.1 for details on the special cases of installation, patching, and removal.</span></span>

<span data-ttu-id="0f25c-420">Библиотеки динамической компоновки (DLL) не нуждаются в таких манифестах.</span><span class="sxs-lookup"><span data-stu-id="0f25c-420">Dynamic Link Libraries (DLLs) do not require such manifests.</span></span>

<span data-ttu-id="0f25c-421">Дополнительные сведения об управлении учетными записями пользователей см. в разделе [Управление учетными записями пользователей для разработчиков игр](/windows/desktop/DxTechArts/user-account-control-for-game-developers).</span><span class="sxs-lookup"><span data-stu-id="0f25c-421">For more information about User Account Control, see [User Account Control for Game Developers](/windows/desktop/DxTechArts/user-account-control-for-game-developers).</span></span>

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a><span data-ttu-id="0f25c-422">2,2. Поддержка 64-разрядных версий Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-422">2.2 Support Windows x64 Versions</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-423"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-423"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-424">Для обеспечения совместимости с 64-разрядными выпусками Windows игры должны соответствовать следующим требованиям.</span><span class="sxs-lookup"><span data-stu-id="0f25c-424">To maintain compatibility with 64-bit editions of Windows, games should meet the following requirements.</span></span>

-   <span data-ttu-id="0f25c-425">Установщики titles и Title не должны содержать 16-разрядный код или использовать любой 16-разрядный компонент.</span><span class="sxs-lookup"><span data-stu-id="0f25c-425">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span>
-   <span data-ttu-id="0f25c-426">Если игра зависит от драйверов режима ядра для работы, должны быть доступны версии x64 этих драйверов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-426">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="0f25c-427">Программа установки игр должна обнаружить и установить правильные драйверы и компоненты для 64-разрядных выпусков Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-427">The game setup must detect and install the proper drivers and components for the 64-bit editions of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-428"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-428"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-429">Многие пользователи Windows Vista и Windows 7 будут запускать 64-разрядные выпуски операционной системы в течение жизненного цикла продукта, поэтому важно, чтобы приложения были совместимы с этой операционной системой.</span><span class="sxs-lookup"><span data-stu-id="0f25c-429">Many Windows Vista and Windows 7 users will run 64-bit editions of the operating system over the life of the product, so it is crucial for applications to be compatible with this operating system.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-430"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-430"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-431">Windows в Windows 64 (WOW64) позволяет выполнять 32-разрядный код в 64-разрядных выпусках Windows, поэтому нет необходимости в том, чтобы приложение было машинным кодом 64-bit в 64-разрядных выпусках Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-431">Windows on Windows 64 (WOW64) allows 32-bit code to run on 64-bit editions of Windows, so it is not necessary that the application be native 64-bit code on 64-bit editions of Windows.</span></span> <span data-ttu-id="0f25c-432">16-разрядный код не работает в 64-разрядных выпусках Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-432">Sixteen-bit code does not run on 64-bit editions of Windows.</span></span>

<span data-ttu-id="0f25c-433">Поддержка совместимости с Windows XP Professional x64 Edition не требуется, но настоятельно рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0f25c-433">Maintaining compatibility with Windows XP Professional x64 Edition is not required, but it is strongly encouraged.</span></span>

<span data-ttu-id="0f25c-434">Дополнительные сведения см. в разделе [64-разрядное программирование для разработчиков игр](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).</span><span class="sxs-lookup"><span data-stu-id="0f25c-434">For details, see [64-bit programming for Game Developers](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).</span></span>

</dd> </dl>

### <a name="23-sign-files"></a><span data-ttu-id="0f25c-435">2,3. входные файлы</span><span class="sxs-lookup"><span data-stu-id="0f25c-435">2.3 Sign Files</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-436"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-436"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-437">Все файлы исполняемого кода (как правило, файлы с расширением .exe или .dll) должны быть подписаны с помощью общедоступного сертификата Authenticode и должны иметь допустимый URL-адрес сервера отметок времени для рабочей подписи.</span><span class="sxs-lookup"><span data-stu-id="0f25c-437">All executable code files (typically, files with the extension .exe or .dll) must be signed with a publicly valid Authenticode certificate, and must have a valid timestamp server URL for production signing.</span></span>

<span data-ttu-id="0f25c-438">Если в игре используется установщик Windows, файлы пакета установщика (.msi файлы) должны быть подписаны.</span><span class="sxs-lookup"><span data-stu-id="0f25c-438">If your game uses Windows Installer, the installer package files (.msi files) must be signed.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-439"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-439"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-440">Подписывание файла помогает пользователям решить, следует ли доверять приложению и гарантировать, что файлы не были изменены.</span><span class="sxs-lookup"><span data-stu-id="0f25c-440">Signing a file helps users decide whether to trust an application, and assures users that files have not been tampered with.</span></span> <span data-ttu-id="0f25c-441">Это также позволяет приложениям правильно работать в заблокированных средах.</span><span class="sxs-lookup"><span data-stu-id="0f25c-441">It also allows applications to run properly in locked-down environments.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-442"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-442"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-443">Дополнительные сведения см. в статье [Подписывание Authenticode для разработчиков игр](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).</span><span class="sxs-lookup"><span data-stu-id="0f25c-443">For details, see [Authenticode Signing for Game Developers](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).</span></span>

<span data-ttu-id="0f25c-444">Если в игре используется установщик Windows, рекомендуется включить исправление UAC/LUA, включив таблицу Мсипатчцертификате.</span><span class="sxs-lookup"><span data-stu-id="0f25c-444">If your game uses Windows Installer, we recommend that you enable UAC/LUA patching, by including an MsiPatchCertificate table.</span></span> <span data-ttu-id="0f25c-445">Дополнительные сведения см. в статье об [установке контроля учетных записей пользователей (UAC)](/windows/desktop/Msi/user-account-control--uac--patching).</span><span class="sxs-lookup"><span data-stu-id="0f25c-445">For more information, see [User Account Control (UAC) Patching](/windows/desktop/Msi/user-account-control--uac--patching).</span></span>

<span data-ttu-id="0f25c-446">Не рекомендуется подписывать файлы CAB (.cab), если они не являются достаточно мелкими (менее 100 МБ).</span><span class="sxs-lookup"><span data-stu-id="0f25c-446">We do not recommend signing cabinet (.cab) files, unless they are relatively small (less than 100 MB).</span></span>

</dd> </dl>

### <a name="24-sign-drivers"></a><span data-ttu-id="0f25c-447">2,4. подписывать драйверы</span><span class="sxs-lookup"><span data-stu-id="0f25c-447">2.4 Sign Drivers</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-448"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-448"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-449">Любой драйвер режима ядра, установленный игрой, должен быть подписан открытым действительным сертификатом Authenticode.</span><span class="sxs-lookup"><span data-stu-id="0f25c-449">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span>

<span data-ttu-id="0f25c-450">Любой драйвер аппаратного устройства режима ядра, установленный игрой, должен иметь подпись Майкрософт, которая может быть получена из лаборатории WHQL или из программы подписи надежности драйвера (DRS).</span><span class="sxs-lookup"><span data-stu-id="0f25c-450">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature, which can be obtained from the Windows Hardware Quality Labs (WHQL) or from the Driver Reliability Signature (DRS) program.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-451"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-451"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-452">Плохо написанные или Антивредоносные драйверы могут серьезно повлиять на стабильность и безопасность системы.</span><span class="sxs-lookup"><span data-stu-id="0f25c-452">Poorly written or malware drivers can severely affect the stability and security of a system.</span></span> <span data-ttu-id="0f25c-453">В 64-разрядных выпусках Windows Vista и Windows 7 неподписанные драйверы не загружаются.</span><span class="sxs-lookup"><span data-stu-id="0f25c-453">On 64-bit editions of Windows Vista and Windows 7, unsigned drivers do not load.</span></span> <span data-ttu-id="0f25c-454">Эту политику также можно включить для 32-разрядных выпусков Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-454">This policy can also be enabled for 32-bit editions of Windows Vista and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-455"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-455"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-456">Для каждого требования 2,2 требуется как 32-разрядная, так и 64-разрядная версия для всех драйверов режима ядра.</span><span class="sxs-lookup"><span data-stu-id="0f25c-456">Both 32-bit and 64-bit native versions of all kernel-mode drivers are needed per requirement 2.2.</span></span>

<span data-ttu-id="0f25c-457">Дополнительные сведения о программах подписывания драйверов Майкрософт можно найти на [портале разработчика оборудования Windows](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx).</span><span class="sxs-lookup"><span data-stu-id="0f25c-457">More information about Microsoft driver signing programs can be found at the [Windows Hardware Developer portal](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx).</span></span>

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a><span data-ttu-id="0f25c-458">2,5. выполнение проверки правильности версий</span><span class="sxs-lookup"><span data-stu-id="0f25c-458">2.5 Perform Proper Version Checking</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-459"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-459"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-460">Игры не должны работать в будущих операционных системах, как указано в изменениях номера версии Windows, если лицензионное соглашение не запрещает использовать в будущих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="0f25c-460">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="0f25c-461">Если предполагается, что игра завершится ошибкой, она должна правильно сделать это, отображая соответствующее сообщение пользователю.</span><span class="sxs-lookup"><span data-stu-id="0f25c-461">If the game is supposed to fail, it must do so gracefully by displaying an appropriate message to the user.</span></span>

<span data-ttu-id="0f25c-462">Если выполняется проверка версии Windows, для проверки версии операционной системы необходимо использовать API-интерфейсы проверки версий ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) или [**верифиверсионинфо**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)).</span><span class="sxs-lookup"><span data-stu-id="0f25c-462">If Windows version checks are made, the version-checking APIs ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) or [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) must be used to check the operating system version.</span></span> <span data-ttu-id="0f25c-463">Для определения версии не следует считывать разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="0f25c-463">Registry keys must not be read to determine the version.</span></span>

<span data-ttu-id="0f25c-464">Явные проверки версий для среды выполнения DirectX не должны присутствовать в игре.</span><span class="sxs-lookup"><span data-stu-id="0f25c-464">Explicit version checks for the DirectX runtime must not be present in the game.</span></span> <span data-ttu-id="0f25c-465">Эти проверки версий не должны присутствовать в установке, запускающей программу установки среды выполнения DirectX (Директсетуп).</span><span class="sxs-lookup"><span data-stu-id="0f25c-465">These version checks must not be present in the installation that launches the DirectX runtime setup (DirectSetup).</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-466"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-466"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-467">Когда пользователи Windows обновляют свои операционные системы, они не должны блокировать воспроизведение текущих игр, просто потому, что номер версии Windows увеличился.</span><span class="sxs-lookup"><span data-stu-id="0f25c-467">When Windows users upgrade their operating systems, they should not be blocked from playing current games simply because the Windows version number has increased.</span></span> <span data-ttu-id="0f25c-468">Плохо написанные средства проверки версий продолжают создавать проблемы для программного обеспечения, которые, в противном случае, работают в более новых версиях Windows или просто с добавлением пакета обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-468">Poorly written version checkers continue to create problems for software that, otherwise, works fine on newer versions of Windows or simply with the addition of a Windows service pack.</span></span>

<span data-ttu-id="0f25c-469">Ненадежная логика сравнения проверки версий для среды выполнения DirectX создала многочисленные неудачные установки при запуске в различных версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-469">Fragile version check comparison logic for the DirectX runtime has created numerous failed installations when it is run on different versions of Windows.</span></span> <span data-ttu-id="0f25c-470">Номер версии DirectX применяется только к основным компонентам операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0f25c-470">The DirectX version number applies only to the core operating system components.</span></span> <span data-ttu-id="0f25c-471">Он не применяется к параллельным компонентам пакета SDK DirectX, используемым во многих играх.</span><span class="sxs-lookup"><span data-stu-id="0f25c-471">It does not apply to the side-by-side DirectX SDK components that are used by many games.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-472"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-472"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-473">Обычно установщики проверяют наличие минимальной версии ОС.</span><span class="sxs-lookup"><span data-stu-id="0f25c-473">It is quite common to see installers check for a minimum OS version.</span></span> <span data-ttu-id="0f25c-474">Однако эта проверка должна быть выполнена с осторожностью, чтобы убедиться в том, что она тестируется не так, а не на простой равенство, тем самым блокируя конкретную версию операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0f25c-474">This check, however, needs to be done with care to ensure that it tests for greater than or equal to, rather than simple equality, thereby locking to a specific version of the operating system.</span></span> <span data-ttu-id="0f25c-475">Использование теста **хигхверсионлие** для средство проверки приложений — это быстрый и простой способ определить, как установщик будет реагировать на значительные изменения в номере версии ОС.</span><span class="sxs-lookup"><span data-stu-id="0f25c-475">Using Application Verifier's **HighVersionLie** test is a quick and easy way to determine how your installer will react to a significant change in the OS version number.</span></span>

<span data-ttu-id="0f25c-476">Правильное использование пакета распространения среды выполнения DirectX (программа установки DirectX) включает в себя запуск во время установки, предпочтительно в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="0f25c-476">Proper use of the DirectX runtime redistribution package (DirectX Setup) involves always launching it during installation, preferably in silent mode.</span></span> <span data-ttu-id="0f25c-477">Это позволяет коду, предоставляемому корпорацией Майкрософт, выполнять все необходимые обновления версии.</span><span class="sxs-lookup"><span data-stu-id="0f25c-477">This allows the code that is provided by Microsoft to perform any required version updates.</span></span> <span data-ttu-id="0f25c-478">Он также позволяет устанавливать любые необязательные компоненты пакета SDK DirectX, такие как D3DX, транзакции, многомерные выражения или Ксинпут.</span><span class="sxs-lookup"><span data-stu-id="0f25c-478">It also allows installation of any optional side-by-side DirectX SDK components, such as D3DX, XACT, MDX, or XInput.</span></span>

<span data-ttu-id="0f25c-479">Рекомендации по развертыванию среды выполнения DirectX см. в статье [Установка DirectX для разработчиков игр](/windows/desktop/DxTechArts/directx-setup-for-game-developers).</span><span class="sxs-lookup"><span data-stu-id="0f25c-479">For best practices for deploying the DirectX runtime, see [DirectX Installation for Game Developers](/windows/desktop/DxTechArts/directx-setup-for-game-developers).</span></span>

<span data-ttu-id="0f25c-480">Рекомендуется, чтобы игры, поддерживающие Windows XP, проверяют наличие пакета обновления 2 или более поздней версии, так как пакет обновления 2 (SP2) и пакет обновления 3 (SP3) обеспечивают значительные улучшения в системе безопасности, упрощенное требование повторного распределения среды выполнения DirectX и очень широкое развертывание.</span><span class="sxs-lookup"><span data-stu-id="0f25c-480">It is recommended that games that support Windows XP check for a service pack level of 2 or higher, because Service Pack 2 (SP2) and Service Pack 3 (SP3) provide significant security improvements, a simplified DirectX Runtime Redistribution requirement, and extremely broad deployment.</span></span> <span data-ttu-id="0f25c-481">Для большинства современных технологий Майкрософт, поддерживающих Windows XP, требуется пакет обновления 2 (SP2) или SP3 (XAudio2, игры для Windows — LIVE и т. д.).</span><span class="sxs-lookup"><span data-stu-id="0f25c-481">Most modern Microsoft technologies that support Windows XP require SP2 or SP3 (XAudio2, Games for Windows - LIVE, and so on).</span></span>

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="0f25c-482">2,6 Поддержка параллельных сеансов пользователей</span><span class="sxs-lookup"><span data-stu-id="0f25c-482">2.6 Support Concurrent User Sessions</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-483"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-483"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-484">Игры, использующие трехмерную график, не должны работать через подключение к удаленному рабочему столу, но при сбое игры пользователь должен получать оповещения.</span><span class="sxs-lookup"><span data-stu-id="0f25c-484">Games that rely on 3D graphics are not required to work over a remote desktop connection, but the user must be alerted when the game fails.</span></span>

<span data-ttu-id="0f25c-485">Игры должны поддерживать стандартные многозадачные сценарии Windows путем соблюдения следующих правил:</span><span class="sxs-lookup"><span data-stu-id="0f25c-485">Games must support standard Windows multitasking scenarios by adhering to the following rules:</span></span>

-   <span data-ttu-id="0f25c-486">Игры не должны блокировать использование одновременных сеансов пользователей.</span><span class="sxs-lookup"><span data-stu-id="0f25c-486">Games must not block the use of concurrent user sessions.</span></span>
-   <span data-ttu-id="0f25c-487">Игра должна запускаться в новом сеансе пользователя, если он уже выполняется в другом сеансе.</span><span class="sxs-lookup"><span data-stu-id="0f25c-487">A game must run in a new user session when it is already running in another session.</span></span>
-   <span data-ttu-id="0f25c-488">Звук игры в одном сеансе пользователя не должен быть слышен, если другой пользователь активен в другом сеансе.</span><span class="sxs-lookup"><span data-stu-id="0f25c-488">Game sound in one user session must not be heard when another user is active in a different session.</span></span>
-   <span data-ttu-id="0f25c-489">Игры должны поддерживать быстрое переключение пользователей.</span><span class="sxs-lookup"><span data-stu-id="0f25c-489">Games must support Fast User Switching.</span></span>
-   <span data-ttu-id="0f25c-490">Игры не должны пытаться отключить стандартную смену задач.</span><span class="sxs-lookup"><span data-stu-id="0f25c-490">Games must not attempt to disable standard task switching.</span></span> <span data-ttu-id="0f25c-491">Игры не должны отключать сочетание клавиш ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="0f25c-491">Games must not disable the ALT+TAB keyboard shortcut.</span></span> <span data-ttu-id="0f25c-492">Играм разрешено отключать специальные сочетания клавиш, как описано в разделе [Отключение сочетаний клавиш в играх](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).</span><span class="sxs-lookup"><span data-stu-id="0f25c-492">Games are allowed to disable accessibility keyboard shortcuts, as described in [Disabling Shortcut Keys in Games](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-493"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-493"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-494">Пользователи Windows должны иметь возможность выполнять параллельные сеансы без конфликтов или прерываний.</span><span class="sxs-lookup"><span data-stu-id="0f25c-494">Windows users should be able to run concurrent sessions without conflict or disruption.</span></span> <span data-ttu-id="0f25c-495">Это распространенный сценарий для компьютера Windows, который совместно используется семейством, румматес или другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="0f25c-495">This is a common scenario for a Windows computer that is shared by a family, roommates, or others.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-496"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-496"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-497">Чтобы проверить, запущена ли игра в удаленном сеансе, вызовите [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM \_ ремотесессион).</span><span class="sxs-lookup"><span data-stu-id="0f25c-497">To test whether the game is launched in a remote session, call [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM\_REMOTESESSION).</span></span> <span data-ttu-id="0f25c-498">Ненулевое значение указывает, что сеанс является удаленным.</span><span class="sxs-lookup"><span data-stu-id="0f25c-498">A nonzero value indicates that the session is remote.</span></span>

<span data-ttu-id="0f25c-499">Дополнительные сведения см. в разделе [быстрое переключение пользователей](/windows-hardware/drivers/display/fast-user-switching).</span><span class="sxs-lookup"><span data-stu-id="0f25c-499">For more information, see [Fast User Switching](/windows-hardware/drivers/display/fast-user-switching).</span></span> <span data-ttu-id="0f25c-500">Обратите внимание, что быстрое переключение пользователей происходит, если во время работы пользователя включены ограничения по времени родительского контроля.</span><span class="sxs-lookup"><span data-stu-id="0f25c-500">Note that Fast User Switching occurs if Parental Controls time restrictions are enabled when the user's time is up.</span></span> <span data-ttu-id="0f25c-501">Дополнительные сведения см. в описании требования 1,2.</span><span class="sxs-lookup"><span data-stu-id="0f25c-501">See requirement 1.2 for more details.</span></span>

</dd> </dl>

### <a name="27-support-long-names"></a><span data-ttu-id="0f25c-502">2,7. Поддержка длинных имен</span><span class="sxs-lookup"><span data-stu-id="0f25c-502">2.7 Support Long Names</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-503"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-503"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-504">Если игра поддерживает сохранение файлов, она должна иметь возможность сохранять файлы с длинными именами и путями.</span><span class="sxs-lookup"><span data-stu-id="0f25c-504">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="0f25c-505">Игра должна правильно обрабатывала специальные символы файловой системы, такие как \\ /: \* ?</span><span class="sxs-lookup"><span data-stu-id="0f25c-505">The game must properly handle special file system characters, such as \\ / : \* ?</span></span> <span data-ttu-id="0f25c-506">" < >, в любых пользовательских полях ввода, которые используются для создания имен файлов или путей.</span><span class="sxs-lookup"><span data-stu-id="0f25c-506">" < >, in any user input fields that are used to create file names or paths.</span></span>

<span data-ttu-id="0f25c-507">Игры должны работать правильно, если пользователь имеет длинное имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="0f25c-507">Games must work properly when a user has a long user name.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-508"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-508"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-509">Игроки привыкли использовать длинные имена в путях с глубиной, которые поддерживаются базовой операционной системой.</span><span class="sxs-lookup"><span data-stu-id="0f25c-509">Players are accustomed to using long names on deep paths that are supported by the underlying operating system.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-510"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-510"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-511">Длинные имена определяются как те, которые содержат максимальные значения, определенные в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0f25c-511">Long names are defined as those that contain the maximum values that are defined in the Windows SDK.</span></span>

</dd> </dl>

## <a name="installation"></a><span data-ttu-id="0f25c-512">Установка</span><span class="sxs-lookup"><span data-stu-id="0f25c-512">Installation</span></span>

<span data-ttu-id="0f25c-513">**Сводка требований к безопасности и совместимости**</span><span class="sxs-lookup"><span data-stu-id="0f25c-513">**Summary of Security and Compatibility Requirements**</span></span>

<span data-ttu-id="0f25c-514">**Преимущества для клиентов**</span><span class="sxs-lookup"><span data-stu-id="0f25c-514">**Customer Benefits**</span></span>

<span data-ttu-id="0f25c-515">Клиенты могут быть уверены, что приложения будут устанавливаться в Windows без ухудшения операционной системы или других приложений, если приложения используют официальный способ распространения системных компонентов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-515">Customers can be confident that applications will install on Windows without degrading the operating system or other applications if applications use official system component distribution methods.</span></span> <span data-ttu-id="0f25c-516">Упрощенный процесс установки предоставляет более доступные и неисправности при работе в играх.</span><span class="sxs-lookup"><span data-stu-id="0f25c-516">A streamlined installation experience provides a more accessible and trouble-free out-of-box experience for games.</span></span>

### <a name="31-support-easy-installation"></a><span data-ttu-id="0f25c-517">3,1. поддержка быстрой установки</span><span class="sxs-lookup"><span data-stu-id="0f25c-517">3.1 Support Easy Installation</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-518"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-518"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-519">Игры должны предоставить упрощенный путь в пользовательском интерфейсе программы установки, реализовав следующие действия:</span><span class="sxs-lookup"><span data-stu-id="0f25c-519">Games must provide a simplified path in the setup user interface by implementing the following:</span></span>

-   <span data-ttu-id="0f25c-520">Отображать не более одного запроса EULA.</span><span class="sxs-lookup"><span data-stu-id="0f25c-520">Display a maximum of one EULA prompt.</span></span>
-   <span data-ttu-id="0f25c-521">Путь установки по умолчанию должен обходить все параметры установки (например, папку установки или параметры компонентов), использовать параметры по умолчанию, а затем запускать игру или средство запуска после успешной установки без дополнительных запросов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-521">The default installation path must bypass all selections for the installation (such as installation folder or component selections), assume the default selections, and then run the game or launcher upon successful installation, without additional prompts.</span></span> <span data-ttu-id="0f25c-522">При необходимости для расширенных параметров конфигурации можно указать пользовательский параметр установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-522">If desired, a custom installation option can be provided for advanced configuration options.</span></span>
-   <span data-ttu-id="0f25c-523">Установите необходимые компоненты операционной системы (например, среды выполнения DirectX и Visual C) с помощью правильных пакетов распространения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0f25c-523">Install any required operating system components (such as the DirectX and Visual C runtimes) using the correct Microsoft redistribution packages.</span></span> <span data-ttu-id="0f25c-524">Установка должна выполняться без вмешательства пользователя и без защиты от проверки версий компонентов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-524">The installation should be performed silently, without prompting and without being guarded by component version checks.</span></span>
-   <span data-ttu-id="0f25c-525">Удаление с помощью **программы и компонентов** на **панели управления** для игрового приложения и созданных рабочих файлов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-525">Provide removal through **Programs and Features** in **Control Panel** for both the game application and generated working files.</span></span> <span data-ttu-id="0f25c-526">Рекомендуется удалить все файлы данных, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="0f25c-526">An option for deleting any data files that are created by the user is recommended.</span></span> <span data-ttu-id="0f25c-527">Процесс удаления должен гарантировать, что все установленные файлы будут удалены, а все параметры (например, записи списка исключений брандмауэра и разделы реестра) будут сняты.</span><span class="sxs-lookup"><span data-stu-id="0f25c-527">The removal process must ensure that all installed files are removed and all settings (for example, firewall exception list entries and registry keys) are cleared.</span></span> <span data-ttu-id="0f25c-528">Перераспределенные компоненты операционной системы не должны удаляться.</span><span class="sxs-lookup"><span data-stu-id="0f25c-528">Redistributed operating system components must not be removed.</span></span>
-   <span data-ttu-id="0f25c-529">Если для игры требуется добавить исключения в брандмауэр Windows, процесс установки может сообщить пользователям о том, что это изменение необходимо.</span><span class="sxs-lookup"><span data-stu-id="0f25c-529">If the game requires exceptions to be added to the Windows Firewall, the setup process can prompt to inform users that this change is required.</span></span> <span data-ttu-id="0f25c-530">Это приглашение должно появиться перед началом установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-530">This prompt should appear before installation begins.</span></span>

<span data-ttu-id="0f25c-531">Для установки и удаления могут потребоваться права администратора.</span><span class="sxs-lookup"><span data-stu-id="0f25c-531">Installation and removal can require administrative rights.</span></span> <span data-ttu-id="0f25c-532">Для установки исправлений может потребоваться запрос учетных данных администратора в зависимости от частоты обновления.</span><span class="sxs-lookup"><span data-stu-id="0f25c-532">Patching can require prompting for administrative credentials, depending on frequency of update.</span></span> <span data-ttu-id="0f25c-533">При нормальном воспроизведении игры не требуются права администратора, каждое требование 2,1 следует рекомендациям по контролю учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="0f25c-533">Normal play of the game must not require administrative rights, per requirement 2.1 Follow User Account Control Guidelines.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-534"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-534"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-535">Простая установка — это философия разработки игр на основе Windows, предназначенная для упрощения и упрощения процесса установки игр на компьютерах под управлением операционных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-535">Easy installation is a Windows-centric game development philosophy that is designed to simplify and streamline the sometimes tedious and confusing process of installing games on computers that are running Windows operating systems.</span></span> <span data-ttu-id="0f25c-536">Простота установки включается с помощью набора технологий и рекомендаций, которые снижают ненужную сложность и наблюдаемый риск установки игр на компьютерах Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-536">Easy installation is enabled by utilizing a set of technologies and best practices that reduce the unnecessary complexity and perceived risk of installing games on Windows computers.</span></span>

<span data-ttu-id="0f25c-537">Основные цели:</span><span class="sxs-lookup"><span data-stu-id="0f25c-537">The key goals are to:</span></span>

-   <span data-ttu-id="0f25c-538">Сократите время начала игры и начните играть.</span><span class="sxs-lookup"><span data-stu-id="0f25c-538">Reduce the amount of time to get into the game and begin play.</span></span>
-   <span data-ttu-id="0f25c-539">Чтобы упростить процесс установки игр, сократите количество диалоговых окон и вариантов выбора до нескольких или нет.</span><span class="sxs-lookup"><span data-stu-id="0f25c-539">Reduce the number of dialog boxes and choices to very few, or none, in order to simplify the game installation experience.</span></span>

<span data-ttu-id="0f25c-540">В некоторых традиционных установках имеются запросы, которые разрешают нефункциональные установки, даже если приложение успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="0f25c-540">Some traditional installations have prompts that allow non-functional installations, even though the application appears to be successfully installed.</span></span> <span data-ttu-id="0f25c-541">Например, для игры может потребоваться, чтобы пользователь принял условия лицензионного соглашения.</span><span class="sxs-lookup"><span data-stu-id="0f25c-541">For example, a game can require a user to accept a EULA.</span></span> <span data-ttu-id="0f25c-542">После этого устанавливается игра, после чего появляется лицензионное соглашение DirectX.</span><span class="sxs-lookup"><span data-stu-id="0f25c-542">The game is then installed, and then the DirectX EULA appears.</span></span> <span data-ttu-id="0f25c-543">Это лицензионное соглашение позволяет пользователям отклонять и, таким образом, пропускать установку среды выполнения DirectX.</span><span class="sxs-lookup"><span data-stu-id="0f25c-543">This EULA allows users to decline, and thus skip installation of the DirectX runtime.</span></span> <span data-ttu-id="0f25c-544">В этом случае может возникнуть игра, которая не запускается из-за отсутствия компонентов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-544">This scenario can result in a game that fails to run because of missing components.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-545"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-545"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-546">Дополнительные сведения об установке игр, не традиционных методиках установки игр, решениях по установке исправлений, совместимых с UAC, и о частом исправлении см. в следующих статьях DirectX:</span><span class="sxs-lookup"><span data-stu-id="0f25c-546">For more information about game installation, non-traditional game installation techniques, UAC-compatible patching solutions, and handling frequent patching, see the following DirectX articles:</span></span>

-   [<span data-ttu-id="0f25c-547">Упрощение установки игр</span><span class="sxs-lookup"><span data-stu-id="0f25c-547">Simplifying Game Installation</span></span>](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [<span data-ttu-id="0f25c-548">Установка по запросу для игр</span><span class="sxs-lookup"><span data-stu-id="0f25c-548">Install-on-Demand for Games</span></span>](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [<span data-ttu-id="0f25c-549">Установка исправлений для игр в Windows XP, Windows Vista и Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f25c-549">Patching Game Software in Windows XP, Windows Vista, and Windows 7</span></span>](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [<span data-ttu-id="0f25c-550">Рекомендации по установке для массовых многопользовательских интернет-игр</span><span class="sxs-lookup"><span data-stu-id="0f25c-550">Installation Best Practices for Massively Multiplayer Online Games</span></span>](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> <span data-ttu-id="0f25c-551">Удаление созданных пользователем файлов данных должно выполняться только для текущего пользователя и для общих общих расположений пользователей.</span><span class="sxs-lookup"><span data-stu-id="0f25c-551">Removing user-specific generated data files should be performed only for the current user and for common shared user locations.</span></span> <span data-ttu-id="0f25c-552">Не существует надежного способа проверки системы на удаление пользовательских файлов для других пользователей, даже если для удаления требуются учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="0f25c-552">There is no robust way to scan the system to remove user-specific files for other users, even if the removal requires administrative credentials.</span></span>

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="0f25c-553">3,2. Поддержка контроля учетных записей пользователей для установки</span><span class="sxs-lookup"><span data-stu-id="0f25c-553">3.2 Support User Account Control for Installation</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-554"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-554"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-555">Установщик игры не должен считать, что он работает в том же контексте, что и пользователь.</span><span class="sxs-lookup"><span data-stu-id="0f25c-555">The game installer must not assume that it is running in the same context as the user.</span></span> <span data-ttu-id="0f25c-556">Пользовательские расположения будут отличаться от установщика и проигрывателя даже для однопользовательских систем из-за повышения прав администратора.</span><span class="sxs-lookup"><span data-stu-id="0f25c-556">User-specific locations will be different from the installer and the player even for single-user systems due to administrator credentials elevation.</span></span> <span data-ttu-id="0f25c-557">Таким образом, когда игра выполняется впервые, она должна выполнять определенные пользователем задачи отдельно от процесса установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-557">Therefore, when a game runs for the first time, it must perform user-specific tasks, separately from the installation process.</span></span>

<span data-ttu-id="0f25c-558">Диалоговое окно исключение брандмауэра Windows не должно появляться, когда пользователь размещает или присоединяется к многопользовательской игре.</span><span class="sxs-lookup"><span data-stu-id="0f25c-558">The Windows Firewall exception dialog box must not appear when a user hosts or joins a multiplayer game.</span></span> <span data-ttu-id="0f25c-559">Все необходимые настройки должны выполняться во время установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-559">Any required configuration must be done at installation time.</span></span> <span data-ttu-id="0f25c-560">Инструкции по установке должны информировать пользователя о том, что эта операция будет выполняться в процессе установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-560">The setup instructions should inform the user that this operation will occur as part of the setup.</span></span>

<span data-ttu-id="0f25c-561">Установщик игр должен предоставить внедренный манифест, обозначающий требуемый уровень выполнения, для каждого требования 2,1 следовать рекомендациям по контролю учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="0f25c-561">The game installer must provide an embedded manifest that designates the required execution level, per requirement 2.1 Follow User Account Control Guidelines.</span></span>

<span data-ttu-id="0f25c-562">Если после завершения установки игра запускается установщиком, ее необходимо запустить в контексте исходного пользователя.</span><span class="sxs-lookup"><span data-stu-id="0f25c-562">If the game is launched by the installer after installation is complete, it must be launched in the context of the original user.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-563"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-563"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-564">Одним из самых значительных изменений в операционной системе Windows в Windows Vista является добавление контроля учетных записей пользователей (UAC), которое по умолчанию запускает приложения с ограниченными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="0f25c-564">One of the largest changes to the Windows operating system in Windows Vista is the addition of User Account Control (UAC), which runs applications with reduced privileges by default.</span></span> <span data-ttu-id="0f25c-565">В результате установщики должны соответствующим образом управлять уровнями привилегий.</span><span class="sxs-lookup"><span data-stu-id="0f25c-565">As a result, installers need to manage privilege levels accordingly.</span></span> <span data-ttu-id="0f25c-566">Windows 7 также активно использует UAC.</span><span class="sxs-lookup"><span data-stu-id="0f25c-566">Windows 7 also makes extensive use of UAC.</span></span> <span data-ttu-id="0f25c-567">Хотя Windows 7 улучшает взаимодействие с пользователем UAC, установщики должны по-прежнему удовлетворять тем же требованиям, что и Windows Vista для правильной работы, не полагаясь на потенциально путаницу в работе виртуализации.</span><span class="sxs-lookup"><span data-stu-id="0f25c-567">While Windows 7 improves the user experience of UAC, installers must still meet the same requirements as on Windows Vista to function properly, without relying on potentially confusing virtualization behavior.</span></span>

<span data-ttu-id="0f25c-568">Контроль учетных записей активен по умолчанию в Windows Vista и Windows 7, и большинство клиентов (88% или более, на основе отзывов) оставляют эту функцию включенной.</span><span class="sxs-lookup"><span data-stu-id="0f25c-568">UAC is active by default on Windows Vista and Windows 7, and the vast majority of customers (88% or more, based on feedback) leave this feature enabled.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-569"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-569"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-570">Дополнительные сведения о настройке брандмауэра Windows см. в статье DirectX [Брандмауэр Windows для разработчиков игр](/windows/desktop/DxTechArts/games-and-firewalls) и пример фиреваллинсталлхелпер.</span><span class="sxs-lookup"><span data-stu-id="0f25c-570">For more details on configuring the Windows Firewall, see the DirectX article [Windows Firewall for Game Developers](/windows/desktop/DxTechArts/games-and-firewalls) and the FirewallInstallHelper sample.</span></span>

<span data-ttu-id="0f25c-571">Стандартный запуск игры в конце процесса установки не соответствует последнему аспекту этого требования, если установка запускается обычным пользователем, и если процессу установки требуются права администратора (то есть запрашиваются учетные данные администратора).</span><span class="sxs-lookup"><span data-stu-id="0f25c-571">Standard launch of the game at the end of the installation process fails to meet the last aspect of this requirement if the installation is launched by a standard user, and if the setup process requires administrative privileges (that is, prompts for a administrator credentials).</span></span> <span data-ttu-id="0f25c-572">Он также наследует административные привилегии, что является потенциальной угрозой безопасности.</span><span class="sxs-lookup"><span data-stu-id="0f25c-572">It also inherits administrative privileges, which is a potential security risk.</span></span> <span data-ttu-id="0f25c-573">Вместо этого загрузчик программы установки должен запустить игру после возврата после успешного вызова установщика.</span><span class="sxs-lookup"><span data-stu-id="0f25c-573">Instead, a setup bootstrap loader should launch the game after returning from a successful invocation of the installer.</span></span> <span data-ttu-id="0f25c-574">Дополнительные сведения см. в статье журнала MSDN Magazine [обучение приложений с помощью контроля учетных записей пользователей Windows Vista](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).</span><span class="sxs-lookup"><span data-stu-id="0f25c-574">For more information, see the MSDN Magazine article [Teach Your Apps to Play Nicely with Windows Vista User Account Control](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).</span></span>

</dd> </dl>

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="0f25c-575">3,3. Установка для исправления папок</span><span class="sxs-lookup"><span data-stu-id="0f25c-575">3.3 Install to Correct Folders</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-576"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-576"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-577">Игры, установленные для всех пользователей, должны быть установлены в папку Program Files по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f25c-577">Games that are installed for all users must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="0f25c-578">Пользовательские данные должны быть записаны во время первого запуска игры, а не во время установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-578">User data must be written when the game runs for the first time, not during the installation.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-579"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-579"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-580">Пользователи должны иметь гибкие возможности установки приложений, где они необходимы.</span><span class="sxs-lookup"><span data-stu-id="0f25c-580">Users should have the flexibility to install applications where they need them.</span></span> <span data-ttu-id="0f25c-581">Они также должны иметь единообразную и безопасную работу с расположением файлов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f25c-581">They should also have a consistent and secure experience with the default location of files.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-582"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-582"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-583">Игры могут использовать различные известные расположения папок (например, заданные \_ локальными \_ файлами AppData и CSid \_ \_ ) для хранения значительных объемов данных игр и поддержки исполняемых файлов для реализации расширенных сценариев установки по запросу и исправления.</span><span class="sxs-lookup"><span data-stu-id="0f25c-583">Games can make use of the various known folder locations (such as those specified by CSIDL\_LOCAL\_APPDATA and CSIDL\_COMMON\_APPDATA) to store significant amounts of game data and supporting executable files to implement advanced install-on-demand and patching scenarios.</span></span>

<span data-ttu-id="0f25c-584">Поскольку установка может потребовать повышения прав для другой учетной записи пользователя во время установки всех пользователей, нет правильного расположения пользователя, в котором будет храниться данные во время установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-584">Because installation can require elevation to a different user account during the all users installation process, there is no correct user location in which to store data at installation time.</span></span> <span data-ttu-id="0f25c-585">Кроме того, если включено шифрование файлов, зашифрованные файлы могут быть доступны только учетной записи пользователя, создавшей их.</span><span class="sxs-lookup"><span data-stu-id="0f25c-585">Also, if file encryption is enabled, encrypted files can be only accessed by the user account that created them.</span></span>

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="0f25c-586">3,4. Установка ресурсов Windows надлежащим образом</span><span class="sxs-lookup"><span data-stu-id="0f25c-586">3.4 Install Windows Resources Properly</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-587"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-587"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-588">Приложения не должны пытаться установить файлы или ключи реестра, защищенные защита ресурсов Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="0f25c-588">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span> <span data-ttu-id="0f25c-589">Если приложению требуются более новые версии компонентов системы, необходимо обновить эти компоненты с помощью пакета обновления Майкрософт или пакета установки, одобренного корпорацией Майкрософт, который содержит системный компонент.</span><span class="sxs-lookup"><span data-stu-id="0f25c-589">If the application requires newer versions of system components, it must update these components by using a Microsoft Service Pack or a Microsoft-approved installation package that contains the system component.</span></span> <span data-ttu-id="0f25c-590">Системные компоненты никогда не должны переноситься в пакеты.</span><span class="sxs-lookup"><span data-stu-id="0f25c-590">System components must never be repackaged.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-591"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-591"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-592">Защита ресурсов Windows (WRP) обеспечивает обновление защищенных системных ресурсов только с помощью утвержденных корпорацией Майкрософт механизмов установки или обновления.</span><span class="sxs-lookup"><span data-stu-id="0f25c-592">Windows Resource Protection (WRP) is designed to ensure that protected system resources are updated only by using Microsoft-approved installation or update mechanisms.</span></span> <span data-ttu-id="0f25c-593">WRP улучшает надежность системы, гарантируя предсказуемость результатов установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-593">WRP improves system reliability by ensuring that the results of an installation are predictable.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-594"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-594"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-595">WRP является преемником защиты файлов Windows, который защищает большинство компонентов системы, установленных в папке Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-595">WRP is the successor to Windows File Protection, which protects the majority of the system components that are installed in the Windows folder.</span></span> <span data-ttu-id="0f25c-596">WRP защищает большинство разделов реестра, в которых хранятся параметры для создания объектов COM.</span><span class="sxs-lookup"><span data-stu-id="0f25c-596">WRP protects most registry keys that store settings for COM object creation.</span></span> <span data-ttu-id="0f25c-597">Она также резервирует определенные папки для использования исключительно операционной системой.</span><span class="sxs-lookup"><span data-stu-id="0f25c-597">It also reserves certain folders for use exclusively by the operating system.</span></span> <span data-ttu-id="0f25c-598">Попытка доступа к защищенным ресурсам обычно приводит к ошибке отказа в доступе.</span><span class="sxs-lookup"><span data-stu-id="0f25c-598">Attempts to access protected resources typically result in an access denial error.</span></span>

<span data-ttu-id="0f25c-599">Сведения о рекомендациях по развертыванию среды выполнения DirectX с помощью игры см. в статье DirectX [Установка DirectX для разработчиков игр](/windows/desktop/DxTechArts/directx-setup-for-game-developers).</span><span class="sxs-lookup"><span data-stu-id="0f25c-599">For details of best practices when the DirectX runtime is deployed with a game, see the DirectX article [DirectX Installation for Game Developers](/windows/desktop/DxTechArts/directx-setup-for-game-developers).</span></span>

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="0f25c-600">3,5. Предотвращение перезагрузки во время установки</span><span class="sxs-lookup"><span data-stu-id="0f25c-600">3.5 Avoid Reboots During Installation</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-601"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-601"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-602">Установщик игр не предполагает, что установка компонентов Windows из пакетов распространения требует перезагрузки, если только перезагрузка не указана в результате возврата или документации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0f25c-602">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span>

<span data-ttu-id="0f25c-603">Если установщик игры всегда выполняет принудительную перезагрузку, он должен быть одобрен корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0f25c-603">If the game installer always forces a reboot, this must be approved by Microsoft.</span></span>

<span data-ttu-id="0f25c-604">В диалоговом окне "файлы в использовании", включенном в пакеты установщик Windows, должен быть параметр для автоматического закрытия приложений и попыток их перезапуска после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-604">Files-in-use dialog boxes that are included in Windows Installer packages must contain an option to automatically close applications and attempt to restart them after setup is complete.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-605"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-605"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-606">Перезагрузка системы после установки является неудобным нарушением работы пользователей и обычно не требуется.</span><span class="sxs-lookup"><span data-stu-id="0f25c-606">Rebooting the system after an installation is an inconvenient disruption for users and is usually unnecessary.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-607"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-607"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-608">Дополнительные сведения см. в разделе [использование установщик Windows с диспетчером перезапуска](/windows/desktop/Msi/using-windows-installer-with-restart-manager).</span><span class="sxs-lookup"><span data-stu-id="0f25c-608">For more information, see [Using Windows Installer with Restart Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager).</span></span>

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="0f25c-609">3,6. правильное использование управления версиями файлов</span><span class="sxs-lookup"><span data-stu-id="0f25c-609">3.6 Use File Versioning Correctly</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-610"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-610"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-611">Программа установки игр должна правильно проверить, чтобы убедиться, что установлены последние версии файлов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-611">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="0f25c-612">При установке игры никогда не следует регрессию файлов, которые не создаются или которые являются общими для приложений, которые не создаются.</span><span class="sxs-lookup"><span data-stu-id="0f25c-612">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-613"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-613"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-614">Общие компоненты и системные компоненты часто обновляются для исправления безопасности и расширенной функциональности.</span><span class="sxs-lookup"><span data-stu-id="0f25c-614">Shared components and system components are often updated for security fixes and expanded functionality.</span></span> <span data-ttu-id="0f25c-615">Установка, включающая более старую версию обновленных компонентов, не должна приводить к утрате обновлений и исправлений, которые уже были применены.</span><span class="sxs-lookup"><span data-stu-id="0f25c-615">An installation that includes an older version of updated components should not result in the loss of updates and fixes that already have been applied.</span></span>

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="0f25c-616">3,7 поддержка \[ условного требования автозапуска\]</span><span class="sxs-lookup"><span data-stu-id="0f25c-616">3.7 Support Autorun \[Conditional Requirement\]</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-617"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-617"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-618">Для игр, распространяемых на компакт-диске, DVD-диске или другом съемном носителе, поддерживающем автозапуск, при первой вставке диска приложение должно автоматически запуститься или предлагать пользователю установить игру, если только пользователь не отключил функцию автозапуска.</span><span class="sxs-lookup"><span data-stu-id="0f25c-618">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game, unless the user has disabled the Autorun feature.</span></span>

<span data-ttu-id="0f25c-619">После успешной установки приложения повторная вставка диска на диск не должна приводить к автоматическому запуску установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-619">After the application is successfully installed, re-inserting the disc in the drive must not cause installation to automatically begin again.</span></span> <span data-ttu-id="0f25c-620">Можно попросить пользователей обновить или изменить варианты установки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-620">It is acceptable to ask users if they want to update or change their installation choices.</span></span>

<span data-ttu-id="0f25c-621">Приложение автозапуска не должно запрашивать повышение прав (т. е. оно должно иметь значение asInvoker в манифесте в соответствии с требованием 2,1, хотя оно может запустить программу установки или другую программу, для которой требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="0f25c-621">The autorun application must not prompt for elevation (that is, it must have asInvoker in the manifest, per requirement 2.1, although it can launch the setup program or another utility that requires administrative rights.</span></span> <span data-ttu-id="0f25c-622">Повышение прав должно происходить только в том случае, если игра не установлена или если пользователь выбрал ее.</span><span class="sxs-lookup"><span data-stu-id="0f25c-622">Elevation should occur only if the game is not installed, or if the user specifically selects it.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-623"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-623"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-624">Автозапуск упрощает работу с распределенными мультимедиа приложениями, такими как игры, которые обычно занимают диск на диске, чтобы играть в игру.</span><span class="sxs-lookup"><span data-stu-id="0f25c-624">Autorun simplifies the experience of using media-distributed applications, such as games that typically require the disc to be present in the drive in order to play the game.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-625"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-625"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-626">Неприемлемо требовать от пользователя перейти в проводнике для запуска установки с компакт-диска или DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="0f25c-626">It is not acceptable to require the user to navigate in File Explorer to launch the installation from the CD or DVD.</span></span>

<span data-ttu-id="0f25c-627">Для игр, распространяемых на нескольких дисках, в идеале следует либо использовать функцию автозапуска, либо продолжить установку без запроса на нажатие клавиши или выполнения других действий.</span><span class="sxs-lookup"><span data-stu-id="0f25c-627">For games that are distributed on multiple discs, subsequent discs should ideally either use the Autorun feature or continue installation without prompting the user to press a key or take other action.</span></span>

<span data-ttu-id="0f25c-628">При создании программы автозапуска убедитесь, что все необходимые компоненты установлены в новых установках Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-628">When authoring an Autorun program, ensure all required components are present on fresh installs of Windows.</span></span> <span data-ttu-id="0f25c-629">Типичные приложения полагаются на технологии, установленные программой установки, но сам автоматический запуск выполняется до того, как произойдет такая установка.</span><span class="sxs-lookup"><span data-stu-id="0f25c-629">Typical applications rely on technologies installed by the setup, but Autorun itself executes before any such setup occurs.</span></span> <span data-ttu-id="0f25c-630">Одним из распространенных примеров является сбой программы автозапуска, так как библиотеки DLL среды выполнения Visual C не были включены в программу установки Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-630">One common example is the failure of Autorun programs because the Visual C Runtime DLLs were not included as part of the Windows setup.</span></span> <span data-ttu-id="0f25c-631">Поэтому программа автозапуска должна использовать локальное CRT-развертывание приложения или статически связать CRT.</span><span class="sxs-lookup"><span data-stu-id="0f25c-631">The Autorun program, therefore, must use application local CRT deployment or must statically link the CRT.</span></span>

<span data-ttu-id="0f25c-632">Программы автозапуска, написанные для использования в версиях Windows до Windows Vista, не должны использовать среду выполнения .NET, поскольку эта технология не включена в Windows XP или более ранние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-632">Autorun programs written for use on versions of Windows before Windows Vista should not use the .NET runtime because this technology is not included with Windows XP or older versions of Windows.</span></span> <span data-ttu-id="0f25c-633">Windows Server 2003 и Windows Vista — это первые версии Windows для включения среды выполнения .NET в составе операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0f25c-633">Windows Server 2003 and Windows Vista are the first versions of Windows to include .NET runtime as part of their operating system.</span></span>

<span data-ttu-id="0f25c-634">По тем же причинам, программам автозапуска не требуется наличие пакета SDK DirectX необязательных компонентов, таких как D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, активной транзакции, КСИНПУТ и MDX 1,1.</span><span class="sxs-lookup"><span data-stu-id="0f25c-634">For similar reasons, Autorun programs cannot require the presence of DirectX SDK optional side-by-side components such as D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, XACT, XINPUT, and MDX 1.1.</span></span>

<span data-ttu-id="0f25c-635">Пример использования автозапуска см. в разделе Образец запуска.</span><span class="sxs-lookup"><span data-stu-id="0f25c-635">For an example of using Autorun, see AutoRun Sample.</span></span>

</dd> </dl>

## <a name="reliability"></a><span data-ttu-id="0f25c-636">Надежность</span><span class="sxs-lookup"><span data-stu-id="0f25c-636">Reliability</span></span>

<span data-ttu-id="0f25c-637">**Сводка требований к безопасности и совместимости**</span><span class="sxs-lookup"><span data-stu-id="0f25c-637">**Summary of Security and Compatibility Requirements**</span></span>

<span data-ttu-id="0f25c-638">**Преимущества для клиентов**</span><span class="sxs-lookup"><span data-stu-id="0f25c-638">**Customer Benefits**</span></span>

<span data-ttu-id="0f25c-639">Эти требования делают приложение более надежным, уменьшая количество сбоев, зависаний и перезагрузок.</span><span class="sxs-lookup"><span data-stu-id="0f25c-639">These requirements make an application more reliable by minimizing the number of crashes, hangs, and reboots.</span></span> <span data-ttu-id="0f25c-640">Требования к надежности гарантируют, что программное обеспечение будет более предсказуемым, обслуживаемым, устойчивым и восстанавливаемым.</span><span class="sxs-lookup"><span data-stu-id="0f25c-640">The reliability requirements can help ensure that software is more predictable, maintainable, resilient, and recoverable.</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="0f25c-641">4,1. Устраните ненужные перезагрузки</span><span class="sxs-lookup"><span data-stu-id="0f25c-641">4.1 Eliminate Unnecessary Reboots</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-642"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-642"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-643">Все установщики приложений должны воспользоваться преимуществами API диспетчера перезапуска, чтобы избежать перезагрузки системы (см. требование 3,5).</span><span class="sxs-lookup"><span data-stu-id="0f25c-643">All application installers must take advantage of the restart manager APIs to avoid system reboots (see requirement 3.5).</span></span>

<span data-ttu-id="0f25c-644">Игры не должны блокировать завершение работы.</span><span class="sxs-lookup"><span data-stu-id="0f25c-644">Games must not block shutdown.</span></span>

<span data-ttu-id="0f25c-645">Все приложения должны отвечать на диспетчер перезапуска, прослушивая и реагируя на следующие сообщения о завершении работы:</span><span class="sxs-lookup"><span data-stu-id="0f25c-645">All applications must respond to the restart manager by listening and responding to the following shutdown messages:</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-646"><span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ куерендсессион с lParam = ENDSESSION \_ клосеапп (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f25c-646"><span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM\_QUERYENDSESSION with LPARAM = ENDSESSION\_CLOSEAPP (0x1)</span></span> 
</dt> <dd>

<span data-ttu-id="0f25c-647">Приложения GUI должны немедленно ответить (TRUE) при подготовке к перезапуску.</span><span class="sxs-lookup"><span data-stu-id="0f25c-647">GUI applications must respond (TRUE) immediately in preparation for a restart.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-648"><span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ ENDSESSION с lParam = ENDSESSION \_ клосеапп (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f25c-648"><span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM\_ENDSESSION with LPARAM = ENDSESSION\_CLOSEAPP (0x1)</span></span> 
</dt> <dd>

<span data-ttu-id="0f25c-649">Приложения должны возвращать значение 0 в течение 5 секунд, а затем закрывать.</span><span class="sxs-lookup"><span data-stu-id="0f25c-649">Applications must return a 0 value within 5 seconds, and then close.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-650"><span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL + C</span><span class="sxs-lookup"><span data-stu-id="0f25c-650"><span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL+C</span></span> 
</dt> <dd>

<span data-ttu-id="0f25c-651">Консольные приложения, получающие это сообщение, должны немедленно закрыться.</span><span class="sxs-lookup"><span data-stu-id="0f25c-651">Console applications that receive this message must close immediately.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0f25c-652"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-652"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-653">Перезагрузки системы являются значительным перерывом.</span><span class="sxs-lookup"><span data-stu-id="0f25c-653">System reboots are a major disruption.</span></span> <span data-ttu-id="0f25c-654">Они ведут к неправильному взаимоработе с пользователем и должны быть минимальными.</span><span class="sxs-lookup"><span data-stu-id="0f25c-654">They lead to a bad user experience, and should be minimized.</span></span> <span data-ttu-id="0f25c-655">Некоторые операции, например критические обновления системы, могут потребовать перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-655">Some operations, such as critical system updates can require reboots.</span></span> <span data-ttu-id="0f25c-656">Прослушивая сообщения о завершении работы, игра и другие приложения могут быстро реагировать на запросы от диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="0f25c-656">By listening to shutdown messages, the game and other applications can react promptly to requests from restart manager.</span></span> <span data-ttu-id="0f25c-657">Таким образом, они могут избежать неоправданных задержек в допустимых запросах на перезагрузку.</span><span class="sxs-lookup"><span data-stu-id="0f25c-657">In this way, they can avoid unnecessarily delays in valid reboot requests.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-658"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-658"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-659">Если установщик игр использует технологию установщик Windows (MSI) без каких-либо настраиваемых действий, эта функция предоставляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="0f25c-659">If a game installer uses the Windows Installer technology (MSI) without any custom actions, this functionality is provided automatically.</span></span> <span data-ttu-id="0f25c-660">Пакеты распространения Майкрософт также поддерживают диспетчер перезапуска.</span><span class="sxs-lookup"><span data-stu-id="0f25c-660">Microsoft redistribution packages also support the Restart Manager.</span></span>

<span data-ttu-id="0f25c-661">Дополнительные сведения о диспетчере перезапуска см. в статье MSDN [о диспетчере перезапуска](/windows/desktop/RstMgr/about-restart-manager).</span><span class="sxs-lookup"><span data-stu-id="0f25c-661">For more information about the Restart Manager, see the MSDN article [About Restart Manager](/windows/desktop/RstMgr/about-restart-manager).</span></span>

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="0f25c-662">4,2 Устранение сбоев средство проверки приложений</span><span class="sxs-lookup"><span data-stu-id="0f25c-662">4.2 Eliminate Application Verifier Failures</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-663"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-663"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-664">Игра не должна создавать ошибки, выполняемые в Microsoft средство проверки приложений (AppVerifier) версии 4,0 или более поздней, в следующих тестах:</span><span class="sxs-lookup"><span data-stu-id="0f25c-664">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span>

-   <span data-ttu-id="0f25c-665">Основные сведения: дескрипторы, кучи, блокировки, память, TLS</span><span class="sxs-lookup"><span data-stu-id="0f25c-665">Basics: Handles, Heaps, Locks, Memory, TLS</span></span>
-   <span data-ttu-id="0f25c-666">Прочее: Данжераусапис, Диртистаккс</span><span class="sxs-lookup"><span data-stu-id="0f25c-666">Miscellaneous: DangerousAPIs, DirtyStacks</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-667"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-667"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-668">AppVerifier тестирует множество известных проблем, вызывающих сбои и зависания в приложениях Windows, а также известные уязвимости системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="0f25c-668">AppVerifier tests for many known issues that cause crashes and hangs in Windows applications, as well as known security vulnerabilities.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-669"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-669"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-670">Дополнительные сведения о средство проверки приложений см. в статье [средство проверки приложений](/previous-versions/ms220948(v=vs.80)) и [использование средство проверки приложений в жизненном цикле разработки программного обеспечения](/previous-versions/aa480483(v=msdn.10)) на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="0f25c-670">For more information about Application Verifier, see [Application Verifier](/previous-versions/ms220948(v=vs.80)) and [Using Application Verifier Within Your Software Development Lifecycle](/previous-versions/aa480483(v=msdn.10)) on MSDN.</span></span> <span data-ttu-id="0f25c-671">Вы можете скачать средство проверки приложений из [сведений о скачивании: средство проверки приложений](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0f25c-671">You can download Application Verifier from [Download details: Application Verifier](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) on Microsoft Download Center.</span></span>

<span data-ttu-id="0f25c-672">Это требование не относится к чисто управляемым приложениям без собственного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="0f25c-672">This requirement does not apply to pure managed applications without native interop.</span></span>

<span data-ttu-id="0f25c-673">Эти тесты должны выполняться в сборке выпуска.</span><span class="sxs-lookup"><span data-stu-id="0f25c-673">These tests should be run on a release build.</span></span> <span data-ttu-id="0f25c-674">Отладочные сборки могут вызывать ложные сбои.</span><span class="sxs-lookup"><span data-stu-id="0f25c-674">Debugging builds can generate false failures.</span></span> <span data-ttu-id="0f25c-675">Некоторые технологии борьбы с пиратством и Памятка по могут мешать выполнению AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="0f25c-675">Some anti-piracy and anti-cheat technologies can interfere with the execution of AppVerifier.</span></span> <span data-ttu-id="0f25c-676">Поэтому эти тесты должны выполняться без защиты от пиратства и Памятка по технологий.</span><span class="sxs-lookup"><span data-stu-id="0f25c-676">Therefore, these tests should be performed without anti-piracy and anti-cheat technologies enabled.</span></span>

<span data-ttu-id="0f25c-677">Может потребоваться установить полное свойство базовых понятий: для куч — значение FALSE, поскольку полная Пажехеап значительно увеличивает нагрузку на память работающего приложения.</span><span class="sxs-lookup"><span data-stu-id="0f25c-677">It may be necessary to set the Full property of the Basics:Heaps test to FALSE, because the full PageHeap greatly increases the memory pressure of the running application.</span></span> <span data-ttu-id="0f25c-678">Ошибки по-прежнему будут обнаружены, но при использовании только частичного Пажехеап их может быть сложнее отключать.</span><span class="sxs-lookup"><span data-stu-id="0f25c-678">Failures will still be detected, but they might be more difficult to track down if you use only partial PageHeap.</span></span>

<span data-ttu-id="0f25c-679">При использовании тестов, связанных с UAC/LUA, в средство проверки приложений в соответствии с требованиями к контролю учетных записей 2,1 и 3,2, для просмотра результатов следует использовать [анализатор Standard User Analyzer](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) .</span><span class="sxs-lookup"><span data-stu-id="0f25c-679">If you use the UAC/LUA-related tests in Application Verifier to meet the User Account Control requirements 2.1 and 3.2, you should use the [Standard User Analyzer](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) to review the results.</span></span> <span data-ttu-id="0f25c-680">Существует также множество других полезных тестов, предоставляемых средство проверки приложений, которые настоятельно рекомендуется использовать в разработке и тестировании, чтобы обеспечить высокий уровень совместимости с текущими и будущими версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-680">There are also numerous other useful tests provided by Application Verifier which you are strongly encouraged to use in development and testing to ensure a high level of compatibility with current and future versions of Windows.</span></span> <span data-ttu-id="0f25c-681">Тест **хигхверсионлие** используется для проверки соответствия требованиям 2,5.</span><span class="sxs-lookup"><span data-stu-id="0f25c-681">The **HighVersionLie** test is used to verify compliance with requirement 2.5.</span></span>

<span data-ttu-id="0f25c-682">Visual Studio Team System включает подмножество функций AppVerifier, интегрированных в среду отладки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-682">Visual Studio Team System includes a subset of the AppVerifier functionality that is integrated into the debugging environment.</span></span> <span data-ttu-id="0f25c-683">Это может оказаться полезным для отслеживания и устранения проблем с основными понятиями: кучами, дескрипторами и тестами блокировок.</span><span class="sxs-lookup"><span data-stu-id="0f25c-683">This may prove useful for tracking down and resolving issues with Basics: Heaps, Handles, and Locks tests.</span></span>

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a><span data-ttu-id="0f25c-684">4,3 поддержка отчеты об ошибках Windows и сведения о версии файла</span><span class="sxs-lookup"><span data-stu-id="0f25c-684">4.3 Support Windows Error Reporting and File Version Information</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-685"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-685"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-686">Чтобы обеспечить поддержку отчеты об ошибках Windows, игры должны соответствовать следующим требованиям.</span><span class="sxs-lookup"><span data-stu-id="0f25c-686">To enable support of Windows Error Reporting, games must meet the following requirements:</span></span>

-   <span data-ttu-id="0f25c-687">Игры должны работать только с известными и ожидаемыми исключениями.</span><span class="sxs-lookup"><span data-stu-id="0f25c-687">Games must handle only exceptions that are known and expected.</span></span> <span data-ttu-id="0f25c-688">Отчеты об ошибках Windows не должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="0f25c-688">Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="0f25c-689">Если в игре возникает ошибка, например нарушение прав доступа, она должна разрешить отчеты об ошибках Windows сообщить о сбое.</span><span class="sxs-lookup"><span data-stu-id="0f25c-689">If a fault such as an Access Violation appears in a game, it must allow Windows Error Reporting to report the crash.</span></span>
-   <span data-ttu-id="0f25c-690">Все исполняемые файлы (например, .exe файлы или библиотеки DLL) должны содержать точное название продукта, название компании и версию файла.</span><span class="sxs-lookup"><span data-stu-id="0f25c-690">All executable files (for example, .exe files or DLLs) must contain an accurate product name, company name, and file version.</span></span>
-   <span data-ttu-id="0f25c-691">Нормальное завершение игры не должно приводить к ошибке неизвестного исключения.</span><span class="sxs-lookup"><span data-stu-id="0f25c-691">Normal exit of the game must not result in an unknown exception fault.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-692"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-692"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-693">Отчеты об ошибках Windows интерфейсы API предоставляют корпорации Майкрософт важные отзывы для выявления широкого сбоя и зависания в приложениях.</span><span class="sxs-lookup"><span data-stu-id="0f25c-693">The Windows Error Reporting APIs provide vital feedback to Microsoft for detecting widespread crashes and hangs in applications.</span></span> <span data-ttu-id="0f25c-694">Это позволяет корпорации Майкрософт и ее партнерам быстро обнаруживать и устранять проблемы с системой и драйверами, что приводит к быстрому выполнению сбоев приложений.</span><span class="sxs-lookup"><span data-stu-id="0f25c-694">This allows Microsoft and its partners to quickly detect and resolve system and driver issues that lead to application failures quickly.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-695"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-695"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-696">Игры могут включать пользовательские необработанные обработчики исключений для выполнения пользовательских функций поддержки и создания отчетов, но они должны передать любую ошибку в функции **репортфаулт** или **веррепортсубмит** .</span><span class="sxs-lookup"><span data-stu-id="0f25c-696">Games can include custom unhandled exception handlers to perform custom support and reporting functionality, but they must pass any error on to the **ReportFault** or **WerReportSubmit** functions.</span></span>

<span data-ttu-id="0f25c-697">Правильная информация о версии файла может быть проверена путем просмотра свойств файла в пользовательском интерфейсе Windows Desktop и проверки страницы свойств версия.</span><span class="sxs-lookup"><span data-stu-id="0f25c-697">Proper file version information can be verified by viewing the file properties in the Windows desktop UI and checking the Version property page.</span></span>

<span data-ttu-id="0f25c-698">Дополнительные сведения об API отчеты об ошибках Windows и о том, как анализировать аварийные дампы, формируемые при использовании этой службы, см. в статье DirectX: [анализ аварийного дампа](/windows/desktop/DxTechArts/crash-dump-analysis).</span><span class="sxs-lookup"><span data-stu-id="0f25c-698">For more information about the Windows Error Reporting APIs, and how to analyze the crash dumps that are generated when you use this service, see the DirectX article [Crash Dump Analysis](/windows/desktop/DxTechArts/crash-dump-analysis).</span></span>

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a><span data-ttu-id="0f25c-699">Стандартный контроллер Xbox 360 для терминологии Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-699">Xbox 360 Common Controller for Windows Terminology</span></span>



| <span data-ttu-id="0f25c-700">Имя</span><span class="sxs-lookup"><span data-stu-id="0f25c-700">Name</span></span>                                          | <span data-ttu-id="0f25c-701">Описание</span><span class="sxs-lookup"><span data-stu-id="0f25c-701">Description</span></span>                                                                                                 |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f25c-702">Объект</span><span class="sxs-lookup"><span data-stu-id="0f25c-702">A</span></span>                                        | <span data-ttu-id="0f25c-703">Кнопка.</span><span class="sxs-lookup"><span data-stu-id="0f25c-703">The A button.</span></span>                                                                                     |
| <span data-ttu-id="0f25c-704">B</span><span class="sxs-lookup"><span data-stu-id="0f25c-704">B</span></span>                                        | <span data-ttu-id="0f25c-705">Кнопка B.</span><span class="sxs-lookup"><span data-stu-id="0f25c-705">The B button.</span></span>                                                                                     |
| <span data-ttu-id="0f25c-706">НАЗАД</span><span class="sxs-lookup"><span data-stu-id="0f25c-706">BACK</span></span>                                     | <span data-ttu-id="0f25c-707">Кнопка Назад.</span><span class="sxs-lookup"><span data-stu-id="0f25c-707">The Back button.</span></span>                                                                                  |
| <span data-ttu-id="0f25c-708">(правый/левый) амортизатор</span><span class="sxs-lookup"><span data-stu-id="0f25c-708">(right/left) bumper</span></span>                      | <span data-ttu-id="0f25c-709">Кнопка в верхней правой и левой границах контроллера.</span><span class="sxs-lookup"><span data-stu-id="0f25c-709">The button at the top right and left edge of the controller.</span></span> <span data-ttu-id="0f25c-710">Эквивалентно кнопке наплеча.</span><span class="sxs-lookup"><span data-stu-id="0f25c-710">Equivalent to a shoulder button.</span></span>    |
| <span data-ttu-id="0f25c-711">направленная панель</span><span class="sxs-lookup"><span data-stu-id="0f25c-711">directional pad</span></span>                          | <span data-ttu-id="0f25c-712">Панель направления контроллера.</span><span class="sxs-lookup"><span data-stu-id="0f25c-712">The controller directional pad.</span></span>                                                                   |
| <span data-ttu-id="0f25c-713">Панель D</span><span class="sxs-lookup"><span data-stu-id="0f25c-713">D-pad</span></span>                                    | <span data-ttu-id="0f25c-714">Допустимое сокращение направленной панели.</span><span class="sxs-lookup"><span data-stu-id="0f25c-714">Accepted abbreviation of directional pad.</span></span>                                                         |
| <span data-ttu-id="0f25c-715">ТОЧЕК</span><span class="sxs-lookup"><span data-stu-id="0f25c-715">DP</span></span>                                       | <span data-ttu-id="0f25c-716">Аббревиатура направленной панели и метка контроллера.</span><span class="sxs-lookup"><span data-stu-id="0f25c-716">Directional pad abbreviation and controller label.</span></span>                                                |
| <span data-ttu-id="0f25c-717">RB, ФУНТОВ</span><span class="sxs-lookup"><span data-stu-id="0f25c-717">RB, LB</span></span>                                   | <span data-ttu-id="0f25c-718">Краткие и левые обозначения спуска и метки контроллера.</span><span class="sxs-lookup"><span data-stu-id="0f25c-718">Right and left bumper abbreviations and controller labels.</span></span>                                        |
| <span data-ttu-id="0f25c-719">RS, LS</span><span class="sxs-lookup"><span data-stu-id="0f25c-719">RS, LS</span></span>                                   | <span data-ttu-id="0f25c-720">Названия и метки для закрепления справа и слева.</span><span class="sxs-lookup"><span data-stu-id="0f25c-720">Right and left stick abbreviations and controller labels.</span></span>                                         |
| <span data-ttu-id="0f25c-721">RT, LT</span><span class="sxs-lookup"><span data-stu-id="0f25c-721">RT, LT</span></span>                                   | <span data-ttu-id="0f25c-722">Правая и левая аббревиатура триггера и метки контроллера.</span><span class="sxs-lookup"><span data-stu-id="0f25c-722">Right and left trigger abbreviations and controller labels.</span></span>                                       |
| <span data-ttu-id="0f25c-723">РСБ, ЛСБ</span><span class="sxs-lookup"><span data-stu-id="0f25c-723">RSB, LSB</span></span>                                 | <span data-ttu-id="0f25c-724">Названия и метки для закрепления справа и слева.</span><span class="sxs-lookup"><span data-stu-id="0f25c-724">Right and left stick abbreviations and controller labels.</span></span>                                         |
| <span data-ttu-id="0f25c-725">START</span><span class="sxs-lookup"><span data-stu-id="0f25c-725">START</span></span>                                    | <span data-ttu-id="0f25c-726">Кнопка запуска.</span><span class="sxs-lookup"><span data-stu-id="0f25c-726">The Start button.</span></span>                                                                                 |
| <span data-ttu-id="0f25c-727">(справа и слева)</span><span class="sxs-lookup"><span data-stu-id="0f25c-727">(right/left) stick</span></span>                       | <span data-ttu-id="0f25c-728">Контроллер.</span><span class="sxs-lookup"><span data-stu-id="0f25c-728">The controller stick.</span></span> <span data-ttu-id="0f25c-729">Ранее аналоговый стик.</span><span class="sxs-lookup"><span data-stu-id="0f25c-729">Formerly thumbstick.</span></span>                                                       |
| <span data-ttu-id="0f25c-730">(правая или левая) кнопка «закрепить»</span><span class="sxs-lookup"><span data-stu-id="0f25c-730">(right/left) stick button</span></span>                | <span data-ttu-id="0f25c-731">Кнопка "закрепить контроллер".</span><span class="sxs-lookup"><span data-stu-id="0f25c-731">The controller stick button.</span></span> <span data-ttu-id="0f25c-732">Прежнее нажатие кнопки аналоговый стика.</span><span class="sxs-lookup"><span data-stu-id="0f25c-732">Formerly thumbstick button.</span></span>                                         |
| <span data-ttu-id="0f25c-733">(правый/левый) триггер</span><span class="sxs-lookup"><span data-stu-id="0f25c-733">(right/left) trigger</span></span>                     | <span data-ttu-id="0f25c-734">Триггер контроллера.</span><span class="sxs-lookup"><span data-stu-id="0f25c-734">The controller trigger.</span></span>                                                                          |
| <span data-ttu-id="0f25c-735">Вибрация</span><span class="sxs-lookup"><span data-stu-id="0f25c-735">Vibration</span></span>                                | <span data-ttu-id="0f25c-736">Игрового процесса отзыв, созданный мотором контроллера.</span><span class="sxs-lookup"><span data-stu-id="0f25c-736">Gameplay feedback produced by the controller motor.</span></span> <span data-ttu-id="0f25c-737">Не используйте румбле.</span><span class="sxs-lookup"><span data-stu-id="0f25c-737">Do not use rumble.</span></span>                           |
| <span data-ttu-id="0f25c-738">X</span><span class="sxs-lookup"><span data-stu-id="0f25c-738">X</span></span>                                        | <span data-ttu-id="0f25c-739">Кнопка X.</span><span class="sxs-lookup"><span data-stu-id="0f25c-739">The X button.</span></span>                                                                                     |
| <span data-ttu-id="0f25c-740">Y</span><span class="sxs-lookup"><span data-stu-id="0f25c-740">Y</span></span>                                        | <span data-ttu-id="0f25c-741">Кнопка Y.</span><span class="sxs-lookup"><span data-stu-id="0f25c-741">The Y button.</span></span>                                                                                     |
| <span data-ttu-id="0f25c-742">Контроллер Xbox 360 для Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-742">Xbox 360 Controller for Windows</span></span>          | <span data-ttu-id="0f25c-743">Игровой планшет Xbox 360 продан как SKU оборудования для ПК, включая диск драйверов устройств Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-743">The Xbox 360 gamepad sold as a PC hardware SKU, including a Windows device driver disc.</span></span>          |
| <span data-ttu-id="0f25c-744">Контроллер беспроводной связи Xbox 360 для Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-744">Xbox 360 Wireless Controller for Windows</span></span> | <span data-ttu-id="0f25c-745">Игровой планшет Xbox 360 продан как SKU оборудования для ПК, включая диск с драйвером Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-745">The Xbox 360 wireless gamepad sold as a PC hardware SKU, including a Windows device driver disc.</span></span> |



 

## <a name="guidelines-for-game-middleware-products"></a><span data-ttu-id="0f25c-746">Рекомендации по промежуточному программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="0f25c-746">Guidelines for Game Middleware Products</span></span>

### <a name="introduction"></a><span data-ttu-id="0f25c-747">Введение</span><span class="sxs-lookup"><span data-stu-id="0f25c-747">Introduction</span></span>

<span data-ttu-id="0f25c-748">Чтобы игры соответствовали программе для игр Windows, они должны соответствовать списку технических требований.</span><span class="sxs-lookup"><span data-stu-id="0f25c-748">For games to qualify for the Games for Windows program, they must meet a list of technical requirements.</span></span> <span data-ttu-id="0f25c-749">Все сторонние компоненты, поставляемые с заголовком (исполняемые файлы, библиотеки DLL, драйверы и т. д.), также должны удовлетворять этим требованиям для того, чтобы подсчитаться в игре.</span><span class="sxs-lookup"><span data-stu-id="0f25c-749">Any third-party components that are shipped with a title (executable files, DLLs, drivers, and so forth) must also meet these requirements for the game to qualify.</span></span> <span data-ttu-id="0f25c-750">В этом документе описываются наиболее распространенные требования, которые также должны быть выполнены сторонними компонентами для игры, чтобы пройти проверку на соответствие.</span><span class="sxs-lookup"><span data-stu-id="0f25c-750">This document highlights the most common requirements that must also be met by the third-party components for the game to pass the compliance tests.</span></span> <span data-ttu-id="0f25c-751">Установщики и полные пакеты игр и рабочих пакетов должны ознакомиться с документацией по техническим требованиям к играм для Windows, так как эти средства затрагивают многие из этих требований.</span><span class="sxs-lookup"><span data-stu-id="0f25c-751">Installers and complete game engine/production packages should review the full Games for Windows technical requirements document, because many of these requirements are affected by these tools.</span></span>

### <a name="additional-recommendations"></a><span data-ttu-id="0f25c-752">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="0f25c-752">Additional Recommendations</span></span>

<span data-ttu-id="0f25c-753">Помимо гарантии того, что компонент поддерживает создание заголовков, соответствующих требованиям для игр для Windows, существует ряд других вопросов, которые следует учитывать при проектировании и развертывании библиотеки или служебной программы поддержки для игры Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-753">Beyond ensuring that your component supports the creation of titles that are compliant with the requirements for Games for Windows, there are a number of other considerations you should take into account when designing and deploying a library or support utility for a Windows game.</span></span>

-   <span data-ttu-id="0f25c-754">Для поддержки разработчиков, работающих с 64-разрядными версиями приложений x64, укажите как 32-разрядные, так и 64-разрядные версии библиотек.</span><span class="sxs-lookup"><span data-stu-id="0f25c-754">To support developers working on 64-bit native x64 applications, provide both 32-bit and 64-bit native versions of your libraries.</span></span> <span data-ttu-id="0f25c-755">32-разрядная версия должна быть совместима с 64-bit на 2,2.</span><span class="sxs-lookup"><span data-stu-id="0f25c-755">The 32-bit version must be 64-bit compatible per 2.2.</span></span> <span data-ttu-id="0f25c-756">Библиотеки для 32-разрядных приложений не должны рассчитывать на то, что старший бит любого 32-разрядного адреса не используется для поддержки использования в приложениях LARGEADDRESSAWARE x86.</span><span class="sxs-lookup"><span data-stu-id="0f25c-756">Libraries for 32-bit applications should not assume that the high bit of any 32-bit address is unused in order to support use within LARGEADDRESSAWARE x86 applications.</span></span>
-   <span data-ttu-id="0f25c-757">Если вы предоставляете заголовки машинного кода (C/C++), используйте синтаксис атрибута SAL для украшения подпрограмм общедоступного API.</span><span class="sxs-lookup"><span data-stu-id="0f25c-757">If you provide native code (C/C++) headers, use Standard Annotation Language (SAL) attribute syntax to decorate your public API routines.</span></span> <span data-ttu-id="0f25c-758">Это позволит пользователям вашей библиотеки получить максимальную пользу использования статического анализа кода (/Analyze), который входит в состав Visual Studio Team System 2005, Visual Studio Team System 2008, Visual Studio 2010 Premium и Visual Studio 2010 Ultimate, а также общедоступных Windows SDK средств компилятора.</span><span class="sxs-lookup"><span data-stu-id="0f25c-758">This will allow users of your library to get the maximum benefit of using Static Code Analysis (/analyze), which is part of Visual Studio Team System 2005, Visual Studio Team System 2008, Visual Studio 2010 Premium, and Visual Studio 2010 Ultimate, as well as the publicly available Windows SDK compiler tools.</span></span>
-   <span data-ttu-id="0f25c-759">Если ваш продукт создает потоки в процессе пользователя, обязательно присвойте каждому потоку имя, чтобы средства отладки могли правильно закомментировать выполняющиеся потоки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-759">If your product creates threads within the user's process, be sure to name each thread so that debugging tools can properly annotate running threads.</span></span>
-   <span data-ttu-id="0f25c-760">Если вы пишете подпрограммы, которые должны вызываться в главном цикле игры, используйте подпрограммы D3DX D3DPERF \_ бегиневент/ендевент и D3DPERF SetMarker, \_ чтобы закомментировать операции высокого уровня, чтобы упростить идентификацию узких мест с помощью PIX для Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-760">If you write routines that are intended to be called within a game's main loop, use the D3DX routines D3DPERF\_BeginEvent/EndEvent and D3DPERF\_SetMarker to annotate high-level operations for easier identification of bottlenecks using PIX for Windows.</span></span>
    > [!Note]  
    > <span data-ttu-id="0f25c-761">Для функций диагностики графики Visual Studio 2012 эти подпрограммы D3DX и PIX заменяются интерфейсом [**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) .</span><span class="sxs-lookup"><span data-stu-id="0f25c-761">For the Visual Studio 2012 graphics diagnostics functionality, these D3DX and PIX routines are replaced by the [**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) interface.</span></span>

     

-   <span data-ttu-id="0f25c-762">Для сетевых библиотек используйте независимые от IP реализации и Избегайте устаревших подпрограмм только IPv4 для поддержки технологий IPv6 и Teredo в Windows XP с пакетом обновления 2 (SP2), Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-762">For networking libraries, provide IP-neutral implementations and avoid deprecated IPv4 only routines to support the IPv6 and Teredo technologies in Windows XP with Service Pack 2, Windows Vista, and Windows 7.</span></span>
-   <span data-ttu-id="0f25c-763">Поставщики услуг игры должны зарегистрироваться в обозревателе игр с помощью версии 2 схемы ГДФ и использовать функцию RSS для предоставления новостей, относящихся к службам.</span><span class="sxs-lookup"><span data-stu-id="0f25c-763">Game service providers should register themselves with Games Explorer using version 2 of the GDF schema, and make use of the RSS feature to provide service-related news.</span></span>

### <a name="games-for-windows-showcases"></a><span data-ttu-id="0f25c-764">Игры для демонстрации Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-764">Games for Windows Showcases</span></span>

### <a name="introduction"></a><span data-ttu-id="0f25c-765">Введение</span><span class="sxs-lookup"><span data-stu-id="0f25c-765">Introduction</span></span>

<span data-ttu-id="0f25c-766">Игры для демонстрации Windows выходят за рамки игр, обеспечивающих твердую работу на компьютерах с Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-766">Games for Windows showcases go beyond providing a solid gaming experience on Windows PCs.</span></span> <span data-ttu-id="0f25c-767">Благодаря реализации этих функций игры могут повысить удобство работы пользователей на последних платформах Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-767">By implementing these features, games can add more excitement to the user experience on the latest Windows platforms.</span></span>

<span data-ttu-id="0f25c-768">Названия игр для Windows должны удовлетворять всем техническим требованиям, перечисленным в этой статье, но функции демонстрации не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="0f25c-768">Games for Windows titles must fulfill all technical requirements listed in this article, but showcase features are optional.</span></span> <span data-ttu-id="0f25c-769">Эти издания бесплатно реализуют некоторые из этих демонстраций.</span><span class="sxs-lookup"><span data-stu-id="0f25c-769">These titles are free to implement some, none, or all of these showcases.</span></span>

### <a name="s1-exploit-direct3d-11"></a><span data-ttu-id="0f25c-770">S. 1. эксплойты Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="0f25c-770">S.1 Exploit Direct3D 11</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-771"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-771"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-772">Direct3D 11 — это интерфейс API подготовки нового поколения для Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-772">Direct3D 11 is the next-generation rendering API for Windows Vista and Windows 7.</span></span> <span data-ttu-id="0f25c-773">Игры, использующие Direct3D 11, используют оптимизированное содержимое, расширенные приемы отрисовки и новые функции оборудования для создания привлекательного интерфейса на оборудовании, поддерживающем 10, 10,1 и 11.</span><span class="sxs-lookup"><span data-stu-id="0f25c-773">Games exploiting Direct3D 11 use optimized content, advanced rendering techniques, and new hardware features to create a compelling experience on hardware that supports 10, 10.1, and 11.</span></span>

<span data-ttu-id="0f25c-774">Если в игре также реализован Direct3D 9, то параллельное сравнение должно продемонстрировать заметное улучшение качества содержимого, визуальную точность, производительность, сложность сцены и другие области графики для Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="0f25c-774">If the game also implements Direct3D 9, a side-by-side comparison should demonstrate a perceptible improvement in content quality, visual fidelity, performance, scene complexity, and other areas of graphics fidelity for Direct3D 11.</span></span> <span data-ttu-id="0f25c-775">Эта поддержка накладываются на игры для технического требования Windows 1,7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-775">This support is subject to the Games for Windows Technical Requirement 1.7.</span></span>

<span data-ttu-id="0f25c-776">Технология Direct3D 10level9 можно использовать для поддержки аппаратного устройства построителя текстуры 2.0/3.0 Direct3D 9-Class в Windows Vista и Windows 7, вместо того чтобы использовать параллельную реализацию Direct3D 9 для широкой поддержки оборудования.</span><span class="sxs-lookup"><span data-stu-id="0f25c-776">Direct3D 10level9 technology can be used to support Shader Model 2.0/3.0 Direct3D 9-class video hardware on Windows Vista and Windows 7, rather than using a side-by-side Direct3D 9 implementation for broad hardware support.</span></span> <span data-ttu-id="0f25c-777">Однако это не является достаточным для демонстрации этой демонстрации.</span><span class="sxs-lookup"><span data-stu-id="0f25c-777">However, this is not sufficient to demonstrate this showcase.</span></span>

<span data-ttu-id="0f25c-778">На компьютерах под управлением Windows Vista или Windows 7 с установленным Direct3D 11 необходимо использовать по умолчанию Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="0f25c-778">On computers running Windows Vista or Windows 7 with Direct3D 11 installed, the game should default to using Direct3D 11.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-779"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-779"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-780">API-интерфейс Direct3D 11 основан на модели WDDM и инфраструктуре Direct3D 10,1 для поддержки новых возможностей: тесселяции оборудования, шейдеров вычислений, многопоточной отрисовки и создания ресурсов, новых форматов сжатия текстур и более гибкого языка шейдеров.</span><span class="sxs-lookup"><span data-stu-id="0f25c-780">The Direct3D 11 API builds on the Windows Display Driver Model (WDDM) and Direct3D 10.1 infrastructure to support new capabilities: hardware tessellation, compute shaders, multithreaded rendering and resource creation, new texture compression formats, and a more flexible shader language.</span></span> <span data-ttu-id="0f25c-781">Direct3D 11 предоставляет единую поддержку оборудования для современных видеоадаптеров, включая последние версии Direct3D 11 и 10,1, а также видеоадаптеры с поддержкой шейдеров 2.0/3.0 Direct3D 9, что является минимальным видеоадаптером, необходимым для рабочего стола Aero 3D Desktop.</span><span class="sxs-lookup"><span data-stu-id="0f25c-781">Direct3D 11 provides unified hardware support for modern video cards, including the latest generation Direct3D 11 parts, all Direct3D 10 and 10.1 video cards, and many Shader Model 2.0/3.0 Direct3D 9 video cards, which is the minimum video hardware required for the Aero 3D desktop.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-782"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-782"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-783">Миграция механизма визуализации Direct3D 9 на использование нового интерфейса Direct3D 11 является строго определенной задачей:</span><span class="sxs-lookup"><span data-stu-id="0f25c-783">Migrating a Direct3D 9 rendering engine to use the new Direct3D 11 interface is a well-defined task:</span></span>

-   <span data-ttu-id="0f25c-784">Исключите все операции с фиксированной функцией в пользу программируемых шейдеров.</span><span class="sxs-lookup"><span data-stu-id="0f25c-784">Eliminate all fixed-function operations in favor of programmable shaders.</span></span>
-   <span data-ttu-id="0f25c-785">Обновите все существующие шейдеры до нового синтаксиса модели шейдера 4. x/5.</span><span class="sxs-lookup"><span data-stu-id="0f25c-785">Update all existing shaders to the new syntax of Shader Model 4.x/5.</span></span>
-   <span data-ttu-id="0f25c-786">Обновление управления ресурсами для поддержки новой модели представления.</span><span class="sxs-lookup"><span data-stu-id="0f25c-786">Update resource management to support the new view model.</span></span>
-   <span data-ttu-id="0f25c-787">Преобразование всех ресурсов для использования нового списка доступных форматов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-787">Convert all assets to use a new list of available formats.</span></span>
-   <span data-ttu-id="0f25c-788">Обновление обработки состояния рендеринга для использования неизменяемых блоков состояния и переработки констант шейдера в константные буферы.</span><span class="sxs-lookup"><span data-stu-id="0f25c-788">Update render state handling to use immutable state blocks, and rework shader constants into constant buffers.</span></span>

<span data-ttu-id="0f25c-789">Это преобразование очень важно для демонстрации Direct3D 11, хотя результат не соответствует демонстрации потребности использования нового API.</span><span class="sxs-lookup"><span data-stu-id="0f25c-789">This conversion is essential to enable the Direct3D 11 showcase, although the result does not meet the showcase requirement of exploiting the new API.</span></span>

<span data-ttu-id="0f25c-790">Новый API и соответствующая модель программирования HLSL предлагают множество возможностей для расширенного содержимого:</span><span class="sxs-lookup"><span data-stu-id="0f25c-790">The new API and associated HLSL programming model offers many opportunities for enhanced content:</span></span>

-   <span data-ttu-id="0f25c-791">Использование существующих аппаратных компонентов Direct3D 10, таких как шейдер геометрии, потоковая передача, массивы текстур и форматы сжатых текстур BC4/BC5.</span><span class="sxs-lookup"><span data-stu-id="0f25c-791">Leveraging existing Direct3D 10 hardware features, such as Geometry Shader, Stream Out, texture arrays, and the BC4/BC5 compressed texture formats.</span></span>
-   <span data-ttu-id="0f25c-792">Использование существующих аппаратных функций Direct3D 10,1, например независимых режимов наложения для рендеринга, глубиной чтения, а также уровня MSAA для каждого примера, массивов схем кубов и подготовки к просмотру в виде блочных форматов (BC).</span><span class="sxs-lookup"><span data-stu-id="0f25c-792">Leveraging existing Direct3D 10.1 hardware features, such as independent per-render-target blend modes, MSAA depth read back, MSAA per-sample shader access, cube map arrays, and rendering to block-compressed (BC) formats.</span></span>
-   <span data-ttu-id="0f25c-793">Реализация дополнительных алгоритмов GPU с помощью COMPUTE. x на существующих видеоадаптерах Direct3D 10/10.1 (включенных обновленными видеодрайверами) или CS 5,0 на видеоадаптерах следующего поколения Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="0f25c-793">Implementing advanced GPU algorithms using Compute Shader with CS4.x on existing Direct3D 10/10.1 video cards (enabled by updated video drivers) or CS 5.0 on next-generation Direct3D 11 video cards.</span></span>
-   <span data-ttu-id="0f25c-794">Подготовка к просмотру нескольких потоков с помощью создания ресурсов в свободной потоковой среде и нескольких контекстов устройств для повышения производительности многоядерных систем (с обновленными видеодрайверами).</span><span class="sxs-lookup"><span data-stu-id="0f25c-794">Rendering on multiple threads using free-threaded resource creation and multiple device contexts for improved performance on multicore systems (with updated video drivers).</span></span> <span data-ttu-id="0f25c-795">Дополнительные сведения см. в разделе игры для Windows: демонстрация. 3.</span><span class="sxs-lookup"><span data-stu-id="0f25c-795">For more information, see the Games for Windows Showcase S.3.</span></span>
-   <span data-ttu-id="0f25c-796">Использование новых функций видеооборудования класса Direct3D 11, таких как тесселяция оборудования с помощью поверхности и шейдеров доменов, шейдер модели 5,0 HLSL, аппаратные функции шейдера BC6HBC7 сжатый формат текстуры и динамическая компоновка шейдера.</span><span class="sxs-lookup"><span data-stu-id="0f25c-796">Utilizing new features of Direct3D 11-class video hardware, such as hardware tessellation with hull and domain shaders, Shader Model 5.0 HLSL shader hardware features BC6HBC7 compressed texture formats, and Dynamic Shader Linkage.</span></span>

<span data-ttu-id="0f25c-797">Методы, которые могут быть реализованы с помощью Direct3D 9 (в основном с высокой стоимостью ЦП), могут быть отключены с помощью графического процессора эффективно, таким образом освобождая ресурсы ЦП для поддержки других требований игры.</span><span class="sxs-lookup"><span data-stu-id="0f25c-797">Techniques that can be implemented with Direct3D 9 (largely through high CPU cost) can be off loaded to the GPU in an efficient manner, thus freeing CPU resources to support other game demands.</span></span>

<span data-ttu-id="0f25c-798">API-интерфейсы Direct3D 11, вспомогательные средства и примеры доступны в пакете SDK для DirectX.</span><span class="sxs-lookup"><span data-stu-id="0f25c-798">Direct3D 11 APIs, supporting tools, and samples are available in the DirectX SDK.</span></span> <span data-ttu-id="0f25c-799">См. также графические API в Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-799">Also see Graphics APIs in Windows.</span></span>

</dd> </dl>

### <a name="s2-exploit-x64-native"></a><span data-ttu-id="0f25c-800">S. 2. эксплойт x64 Native</span><span class="sxs-lookup"><span data-stu-id="0f25c-800">S.2 Exploit x64 Native</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-801"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-801"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-802">Эта игра включает в себя 64-разрядный машинный исполняемый файл, который предоставляет новые возможности, предоставляемые выпусками x64 Windows, работающими на оборудовании с поддержкой x64.</span><span class="sxs-lookup"><span data-stu-id="0f25c-802">The game includes a 64-bit native executable that delivers a compelling new experience enabled by x64 editions of Windows running on x64-capable hardware.</span></span> <span data-ttu-id="0f25c-803">Параллельное сравнение с 32-разрядной версией игры должно показывать заметное улучшение сложности содержимого, сократить общее время загрузки и производительность.</span><span class="sxs-lookup"><span data-stu-id="0f25c-803">A side-by-side comparison with the 32-bit version of the game should show a perceptible improvement in content complexity, reduced overall load times, and performance.</span></span>

<span data-ttu-id="0f25c-804">В 64-разрядных выпусках Windows для установки по умолчанию в обозревателях игр и Windows XP Professional x64 Edition всегда должна быть настроена версия по 64-разрядной версии игры.</span><span class="sxs-lookup"><span data-stu-id="0f25c-804">On 64-bit editions of Windows, installation should always set up the 64-bit native version of the game as the default for shortcuts in Games Explorer and Windows XP Professional x64 Edition.</span></span> <span data-ttu-id="0f25c-805">Если требуется Двойная установка, можно указать дополнительную задачу воспроизведения для обозревателя игр в Windows Vista и Windows 7, которая указывает на 32-разрядную версию, но значение по умолчанию должно остаться в версии 64-bit Native.</span><span class="sxs-lookup"><span data-stu-id="0f25c-805">If dual installation is desired, then an additional play task can be specified for Games Explorer on Windows Vista and Windows 7 that points to the 32-bit version, but the default should remain the 64-bit native version.</span></span>

<span data-ttu-id="0f25c-806">Обратите внимание, что игра должна поддерживать 64-разрядные выпуски Windows Vista и Windows 7 для удовлетворения этой демонстрации.</span><span class="sxs-lookup"><span data-stu-id="0f25c-806">Note that the game should support the 64-bit editions of Windows Vista and Windows 7 to meet this showcase recommendation.</span></span> <span data-ttu-id="0f25c-807">Поддержка Windows XP Professional x64 Edition рекомендуется, но не является обязательной.</span><span class="sxs-lookup"><span data-stu-id="0f25c-807">Support for Windows XP Professional x64 Edition is encouraged, but not required.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-808"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-808"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-809">Технология x64 предоставляет возможности 64-разрядной адресации для рынков потребительского и серверного программного обеспечения с полной скоростью 32-бит обратно совместимости для существующих приложений.</span><span class="sxs-lookup"><span data-stu-id="0f25c-809">x64 technology provides 64-bit addressing capabilities for both the consumer and server markets that includes full-speed 32-bit backwards compatibly for existing applications.</span></span> <span data-ttu-id="0f25c-810">x64 является ключевой частью плана как для AMD (AMD64), так и для Intel (EMT64), и, за исключением Ultra-Mobile процессоров, поддерживает технологию для всех процессоров текущего и будущего поколения.</span><span class="sxs-lookup"><span data-stu-id="0f25c-810">x64 is a key part of the roadmap for both AMD (AMD64) and Intel (EMT64), and, with the exception of ultra-mobile CPUs, support the technology for all current and future generation processors.</span></span>

<span data-ttu-id="0f25c-811">Windows XP Professional x64 Edition была первой ориентированной на потребителя операционной системой Windows (ОС) для поддержки технологии x64, а Windows Vista и Windows 7 значительно расширяют доступность ОС для 64-разрядных вычислительных вычислений.</span><span class="sxs-lookup"><span data-stu-id="0f25c-811">Windows XP Professional x64 Edition was the first consumer-oriented Windows operating system (OS) to support x64 technology, and Windows Vista and Windows 7 greatly expand the availability of the OS-enablement for 64-bit consumer computing.</span></span> <span data-ttu-id="0f25c-812">Благодаря 2 ГБ ОЗУ в стандартном масштабе на многих новых компьютерах дальнейшие улучшения масштабирования памяти не повышают пользу 32-разрядных отдельных приложений, которые не могут использовать более 2 ГБ физической памяти.</span><span class="sxs-lookup"><span data-stu-id="0f25c-812">With 2 GB of RAM as standard on many new computers, further improvements in memory scaling will not benefit 32-bit individual applications that are unable to address more than 2 GB of physical RAM.</span></span> <span data-ttu-id="0f25c-813">Многие игры уже сегодня сталкиваются с проблемами, подключив все доступное содержимое к ограничениям в 2 ГБ виртуального адресного пространства, особенно если они объединены с большими воспоминаниями видео, доступными на высокопроизводительных графических процессорах, и переход на технологию x64 значительно увеличивает уровень детализации поддержки.</span><span class="sxs-lookup"><span data-stu-id="0f25c-813">Many games today are facing challenges fitting all of the available content into the constraints of 2 GB of virtual address space, especially when combined with the large video memories available on high-end GPUs, and moving to x64 technology greatly increases the supportable levels of detail.</span></span>

<span data-ttu-id="0f25c-814">совместимость с x64 для 32-разрядных игр — это игры для технического требования Windows (2,2), но для полного использования новых технологий требуется 64-разрядная собственная реализация.</span><span class="sxs-lookup"><span data-stu-id="0f25c-814">x64 compatibility for 32-bit games is a Games for Windows technical requirement (2.2), but taking full advantage of the new technologies requires a 64-bit native implementation.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-815"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-815"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-816">Основное преимущество 64-разрядной адресации — возможность прямого доступа к более чем 2 ГБ физической и виртуальной памяти.</span><span class="sxs-lookup"><span data-stu-id="0f25c-816">The primary benefit of 64-bit addressing is the ability to directly access more than 2 GB of physical and virtual memory.</span></span> <span data-ttu-id="0f25c-817">Пространство адресов большого объема виртуальной памяти позволяет широко использовать сопоставленные в памяти операции ввода-вывода без проблем с нехваткой адресного пространства виртуальной машины, которые были распространены в 32-разрядном программировании.</span><span class="sxs-lookup"><span data-stu-id="0f25c-817">The large virtual memory address space allows for extensive use of memory-mapped I/O without concern for VM address space exhaustion problems prevalent in 32-bit programming.</span></span> <span data-ttu-id="0f25c-818">Игры могут использовать новое пространство для значительного улучшения времени загрузки или, в некоторых случаях, для исключения пауз для загрузки содержимого.</span><span class="sxs-lookup"><span data-stu-id="0f25c-818">Games can take advantage of the new space to greatly improve load times or, in some instances, to eliminate pauses for loading content.</span></span>

<span data-ttu-id="0f25c-819">Существующие 32-разрядные приложения могут воспользоваться преимуществами 64-разрядных версий, используя возможность обработки адресов с полными 32 разрядами данных при построении с помощью параметра компоновщика "включить крупные адреса (**/LARGEADDRESSAWARE**)".</span><span class="sxs-lookup"><span data-stu-id="0f25c-819">Existing 32-bit applications can benefit from x64 editions by having the capability to process addresses with full 32-bit data when built with the Enable Large Addresses (**/LARGEADDRESSAWARE**) linker option.</span></span> <span data-ttu-id="0f25c-820">В 32-разрядных версиях Windows XP специальные режимы загрузки позволяли использовать такие приложения для адресации до 3 ГБ ОЗУ, а выпуски x64 предоставляют доступ к 4 ГБ ОЗУ для приложений с поддержкой больших адресов (LAA).</span><span class="sxs-lookup"><span data-stu-id="0f25c-820">On 32-bit versions of Windows XP, special boot modes allowed such applications to address up to 3 GB of RAM, and x64 editions provide access up to 4 GB of RAM for Large Address Aware (LAA) apps.</span></span> <span data-ttu-id="0f25c-821">Хотя использование LAA в 32-разрядном приложении не соответствует этим демонстрационным требованиям, эта технология моста является чрезвычайно полезным способом предоставления дополнительных преимуществ масштабирования в версиях Windows x64 для тех, которые не полностью реализуют это демонстрационное требование.</span><span class="sxs-lookup"><span data-stu-id="0f25c-821">While use of LAA in a 32-bit application does not meet this showcase requirement, this bridge technology is an extremely useful way of providing additional scaling benefits on x64 versions of Windows for those not fully implementing this showcase requirement.</span></span>

<span data-ttu-id="0f25c-822">Дополнительные сведения см. в статье [64-разрядное программирование для разработчиков игр](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) и [ОЗУ, видеопамяти и других объемов ОЗУ. в гамасутра есть 64-разрядные игры](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) .</span><span class="sxs-lookup"><span data-stu-id="0f25c-822">For more information, see [64-bit programming for Game Developers](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) and [RAM, VRAM, and More RAM: 64-bit Gaming Is Here](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) in Gamasutra.</span></span>

> [!Note]  
> <span data-ttu-id="0f25c-823">Ключевой задачей этой демонстрации является обеспечение того, что все сторонние библиотеки или компоненты, на которые полагается ваша игра, доступны для 64-разрядной разработки в машинном коде.</span><span class="sxs-lookup"><span data-stu-id="0f25c-823">A key challenge for this showcase is ensuring any third-party libraries or components your game relies on are available for 64-bit native development.</span></span> <span data-ttu-id="0f25c-824">Многие устаревшие API-интерфейсы Майкрософт также были исключены из 64-разрядной собственной среды, что может быть проблемой для баз кода ядра, содержащих старые реализации ключевых систем.</span><span class="sxs-lookup"><span data-stu-id="0f25c-824">Many legacy Microsoft APIs also have been eliminated from the 64-bit native environment, which can prove a challenge for engine code bases containing older implementations of key systems.</span></span>

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a><span data-ttu-id="0f25c-825">S. 3. эксплойты Many-Core процессоров</span><span class="sxs-lookup"><span data-stu-id="0f25c-825">S.3 Exploit Many-Core Processors</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-826"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-826"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-827">Игра реализует функции, которые используют преимущества многоядерных процессоров, масштабирование до 3, 4 или более ядер, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="0f25c-827">The game implements features that take advantage of multicore processors, scaling to 3, 4, or more cores, when available.</span></span>

<span data-ttu-id="0f25c-828">Если игра поддерживает однопроцессорные или двухъядерные системы, то параллельное сравнение с четырехъядерной системой должно продемонстрировать ощутимые новые функции, дополнительные привлекательные эффекты, улучшения качества содержимого и (или) повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="0f25c-828">If the game supports single-processor or dual-core systems, a side-by-side comparison with a quad-core system should demonstrate perceptible new features, additional compelling effects, improvement in content quality, and/or improved performance.</span></span>

<span data-ttu-id="0f25c-829">Поскольку технология масштабирования с двумя ядрами уже широко поддерживается играми, а также автоматически используется различными усовершенствованиями драйвера Direct3D, масштабирование с двумя ядрами недостаточно для демонстрации этой демонстрации.</span><span class="sxs-lookup"><span data-stu-id="0f25c-829">Because dual-core scaling is already widely supported by games, as well as automatically utilized by various Direct3D driver enhancements, dual-core scaling is not sufficient to demonstrate this showcase.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-830"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-830"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-831">Продолжение роста производительности для ЦП изменилось с улучшений частоты часов до добавления вычислительных ядер.</span><span class="sxs-lookup"><span data-stu-id="0f25c-831">The continuing growth in performance for CPUs has switched from clock rate improvements to the addition of computational cores.</span></span> <span data-ttu-id="0f25c-832">Планы AMD и Intel основаны на масштабируемых многоядерных проектах.</span><span class="sxs-lookup"><span data-stu-id="0f25c-832">Both AMD and Intel roadmaps are based on scalable, multicore designs.</span></span> <span data-ttu-id="0f25c-833">Все игровые платформы нового поколения имеют многоядерные ЦП из-за этой фундаментальной смены в развитии процессоров.</span><span class="sxs-lookup"><span data-stu-id="0f25c-833">All next-generation game platforms have multicore CPUs because of this fundamental shift in the evolution of processors.</span></span> <span data-ttu-id="0f25c-834">Приложения с одним потоком больше не будут видеть значительную прибыль от процессоров следующего поколения.</span><span class="sxs-lookup"><span data-stu-id="0f25c-834">Single-threaded applications no longer will see significant gains from next-generation CPUs.</span></span> <span data-ttu-id="0f25c-835">Простое многопоточность также не будет масштабироваться, так как количество ядер ЦП в общем использовании растет до трех или более.</span><span class="sxs-lookup"><span data-stu-id="0f25c-835">Simple multithreading also will fail to scale as the number of CPU cores in common use grows to three or more.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-836"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-836"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-837">Обратите внимание, что количество ядер не должно быть степенью двух, поэтому игры должны масштабироваться линейно и обрабатывать базовые показатели по 3, 4, 5, 6, 7, 8 и т. д.</span><span class="sxs-lookup"><span data-stu-id="0f25c-837">Note that core counts need not be a power of two, so games should scale linearly and handle core counts of 3, 4, 5, 6, 7, 8, and so on.</span></span>

<span data-ttu-id="0f25c-838">Масштабирование путем увеличения числа потоков в приложении обеспечивает возврат только в том случае, если стоимость связи и синхронизации потоков остаются в состоянии Check.</span><span class="sxs-lookup"><span data-stu-id="0f25c-838">Scaling by increasing the number of threads in an application only provides a return if the cost of communication and thread synchronization are kept in check.</span></span> <span data-ttu-id="0f25c-839">Масштабирование на основе компонентов может оказаться более простым решением в краткосрочной ситуации, что позволит играть нормально работать без дополнительных потоков на одноядерных системах и включать их при наличии дополнительной мощности ЦП.</span><span class="sxs-lookup"><span data-stu-id="0f25c-839">Feature-based scaling may prove an easier solution in the short-term, allowing the game to operate normally without the additional threads on single-core systems and enabling them when the additional CPU power is available.</span></span>

<span data-ttu-id="0f25c-840">Дополнительные сведения см. в разделах [Создание кода для нескольких ядер в xbox 360 и Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores) и [вопросы программирования для Xbox 360 и Microsoft Windows](/windows/desktop/DxTechArts/lockless-programming) в статьях DirectX, а также в разделе дксутлоккфрипипе Utility и коредетектион Sample.</span><span class="sxs-lookup"><span data-stu-id="0f25c-840">For more information, see [Coding For Multiple Cores on Xbox 360 and Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores) and [Lockless Programming Considerations for Xbox 360 and Microsoft Windows](/windows/desktop/DxTechArts/lockless-programming) in the DirectX articles, as well as the DXUTLockFreePipe utility and the CoreDetection sample.</span></span>

<span data-ttu-id="0f25c-841">Использование беспотокового создания ресурсов и контекстов устройств Direct3D 11 полезно при обеспечении масштабируемости для многих ядер при подготовке и загрузке графических ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-841">Making use of the Direct3D 11 free-threaded resource creation and device contexts is useful in achieving many-core scalability in rendering and loading graphics resources.</span></span> <span data-ttu-id="0f25c-842">Ознакомьтесь с играми для демонстрации Windows. 1.</span><span class="sxs-lookup"><span data-stu-id="0f25c-842">See Games for Windows Showcase S.1.</span></span>

<span data-ttu-id="0f25c-843">Обратите внимание, что использование инструкции ЦП, RDTSC напрямую, вместо использования API Windows для расчета времени на многоядерных системах может привести к проблемам с некоторыми конфигурациями оборудования и ОС. см. статью [время игры и многоядерные процессоры](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) в статьях DirectX.</span><span class="sxs-lookup"><span data-stu-id="0f25c-843">Note that using the CPU instruction rdtsc directly, instead of using Windows APIs to compute timing on multicore systems, can lead to problems on some hardware and OS configurations; see [Game Timing and Multicore Processors](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) in the DirectX articles.</span></span>

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a><span data-ttu-id="0f25c-844">S. 4. Поддержка игр для Windows — LIVE</span><span class="sxs-lookup"><span data-stu-id="0f25c-844">S.4 Support Games for Windows - LIVE</span></span>

<span data-ttu-id="0f25c-845">Игры для Windows (LIVE) больше не поддерживаются корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0f25c-845">Games for Windows - LIVE is no longer supported by Microsoft.</span></span>

### <a name="s5-support-windows-touch"></a><span data-ttu-id="0f25c-846">S. 5. Поддержка сенсорного ввода Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-846">S.5 Support Windows Touch</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-847"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-847"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-848">Игры с поддержкой сенсорного ввода Windows работают с помощью сенсорного ввода и (или) жестов на компьютерах под управлением Windows 7 с сенсорным экраном.</span><span class="sxs-lookup"><span data-stu-id="0f25c-848">Windows touch-capable games are playable using touch and/or gestures on computers running Windows 7 with a touch display.</span></span> <span data-ttu-id="0f25c-849">Также можно использовать ввод с клавиатуры, но основной интерфейс воспроизведения должен быть сенсорным.</span><span class="sxs-lookup"><span data-stu-id="0f25c-849">Keyboard input can be used as well, but the primary play interface must be touch-based.</span></span>

<span data-ttu-id="0f25c-850">Включение сенсорного ввода не должно препятствовать использованию мыши или общего контроллера в соответствии с техническим требованием 1,4.</span><span class="sxs-lookup"><span data-stu-id="0f25c-850">Enabling touch should not prevent the use of the mouse or common controller, subject to Technical Requirement 1.4.</span></span>

<span data-ttu-id="0f25c-851">Установщик игры не должен поддерживать функции сенсорного ввода Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-851">The game's installer is not expected to support Windows Touch functionality.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-852"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-852"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-853">Экраны с поддержкой нескольких сенсорных устройств доступны для ноутбуков и настольных компьютеров, и они представляют собой ключевую функцию, которая повышается с выпуском Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-853">Multi-touch-capable displays for computers are available for laptops and desktops, and they represent a key hardware feature being promoted with the release of Windows 7.</span></span> <span data-ttu-id="0f25c-854">Windows 7 поддерживает Windows Touch во всех интерфейсах рабочего стола и общих элементов управления.</span><span class="sxs-lookup"><span data-stu-id="0f25c-854">Windows 7 supports Windows Touch throughout the desktop and common controls interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-855"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-855"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-856">Приложения с машинным кодом могут получать доступ к нескольким касаниям через \_ сообщения WM Touch в сочетании с функцией [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) .</span><span class="sxs-lookup"><span data-stu-id="0f25c-856">Native code applications can access multi-touch through the WM\_TOUCH messages, in combination with the [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) function.</span></span> <span data-ttu-id="0f25c-857">См. также API манипуляций и инерции.</span><span class="sxs-lookup"><span data-stu-id="0f25c-857">See also the Manipulations and Inertia API.</span></span>

<span data-ttu-id="0f25c-858">Windows Presentation Foundation (WPF) 4,0 предоставляет управляемое решение для многосенсорных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-858">Windows Presentation Foundation (WPF) 4.0 provides a managed solution for multi-touch interfaces.</span></span>

<span data-ttu-id="0f25c-859">Дополнительные сведения см. в разделе Windows Touch SDK.</span><span class="sxs-lookup"><span data-stu-id="0f25c-859">For more information, see the Windows Touch SDK.</span></span>

</dd> </dl>

### <a name="s6-support-high-color"></a><span data-ttu-id="0f25c-860">С. 6 поддержка высокого цвета</span><span class="sxs-lookup"><span data-stu-id="0f25c-860">S.6 Support High Color</span></span>

<dl> <dt>

<span data-ttu-id="0f25c-861"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Требуются**</span><span class="sxs-lookup"><span data-stu-id="0f25c-861"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-862">Игры, поддерживающие высокий цвет, используют формат 10:10:10:2 \_ ( \_ R10G10B10A2 формата DXGI, D3DFMT \_ A2B10G10R10) или 16:16:16:16 (в \_ формате DXGI \_ R16G16B16A16, D3DFMT \_ A16B16G16R16) для фонового буфера отрисовки и режима полноэкранного отображения.</span><span class="sxs-lookup"><span data-stu-id="0f25c-862">Games that support High Color use a 10:10:10:2 (DXGI\_FORMAT\_R10G10B10A2, D3DFMT\_A2B10G10R10) or a 16:16:16:16 (DXGI\_FORMAT\_R16G16B16A16, D3DFMT\_A16B16G16R16) format for the rendering back-buffer and full-screen display mode.</span></span>

<span data-ttu-id="0f25c-863">При использовании целевого объекта рендеринга высокого цвета содержимое High-Dynamic диапазона (HDR) может быть визуализировано с расширенным или широким охватом при выполнении сопоставления тонового диапазона с 10-или 16-разрядным диапазоном.</span><span class="sxs-lookup"><span data-stu-id="0f25c-863">By using a  High Color  render target, High-Dynamic Range (HDR) content can be rendered with an extended or wide gamut when performing tone mapping to a 10-bit or 16-bit range.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-864"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="0f25c-864"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-865">Мониторы способны отображать более 256 уровней цвета на канал в течение многих лет, даже если дисплеи CRT распространены.</span><span class="sxs-lookup"><span data-stu-id="0f25c-865">Monitors have been capable of displaying more than 256 color levels per channel for many years, even when CRT displays were prevalent.</span></span> <span data-ttu-id="0f25c-866">Для проверки оборудования на видеоадаптерах установлен ограничивающий фактор.</span><span class="sxs-lookup"><span data-stu-id="0f25c-866">The scan out hardware on video cards has been the limiting factor.</span></span> <span data-ttu-id="0f25c-867">Современные GPU, в том числе большинство устройств Direct3D 9-Class и все 10-класс Direct3D и лучшее оборудование, имеют аппаратное обеспечение с поддержкой по крайней мере 10 бит на канал, а аппаратные возможности в будущем задаются в 16 бит на цветовой канал.</span><span class="sxs-lookup"><span data-stu-id="0f25c-867">Modern GPUs, including most Direct3D 9-class hardware and all Direct3D 10-class and better hardware, have scan-out hardware capable of at least 10-bits per channel, and hardware capability is set to grow to 16-bits per color channel in the future.</span></span> <span data-ttu-id="0f25c-868">Системы связи HD TV (HDMI, Дисплайпорт) были разработаны так, чтобы поддерживать более 8 бит на канал, а аналоговый VGA уже будет содержать такие сигналы.</span><span class="sxs-lookup"><span data-stu-id="0f25c-868">HD TV interconnect systems (HDMI, DisplayPort) have been designed to handle more than 8-bits per channel as well, and analog VGA will already carry such signals.</span></span>

</dd> <dt>

<span data-ttu-id="0f25c-869"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0f25c-869"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="0f25c-870">Обратите внимание, что высокий цвет, или Hi, исторически обозначает перемещение с 256 (8-разрядных) цвета на экран с 15-или 16-разрядным цветом.</span><span class="sxs-lookup"><span data-stu-id="0f25c-870">Note that High Color, or Hi Color, historically refers to moving from 256 (8-bit) color displays to 15- or 16-bit color displays.</span></span> <span data-ttu-id="0f25c-871">Большинство систем вывода имеют много времени, так как перемещено на True Color, который имеет 24-разрядный цвет или 8 бит на цветовой канал для красного, зеленого и синего цветов.</span><span class="sxs-lookup"><span data-stu-id="0f25c-871">Most display systems have long since moved on to True Color which is 24-bit color, or 8-bits per color channel for red, green, and blue.</span></span> <span data-ttu-id="0f25c-872">В соответствии с высоким уровнем цвета это означает, что новое поколение отображает системы, которые могут обрабатывать более 8 бит на отдельный цветовой канал.</span><span class="sxs-lookup"><span data-stu-id="0f25c-872">By High Color here we mean a new generation of displays systems that can operate with more than 8-bits per individual color channel.</span></span> <span data-ttu-id="0f25c-873">Также называется глубоким цветом.</span><span class="sxs-lookup"><span data-stu-id="0f25c-873">The is also referred to as Deep Color.</span></span>

</dd> </dl>

### <a name="recommended-best-practices"></a><span data-ttu-id="0f25c-874">Рекомендуемые рекомендации</span><span class="sxs-lookup"><span data-stu-id="0f25c-874">Recommended Best Practices</span></span>

### <a name="introduction"></a><span data-ttu-id="0f25c-875">Введение</span><span class="sxs-lookup"><span data-stu-id="0f25c-875">Introduction</span></span>

<span data-ttu-id="0f25c-876">Помимо удовлетворения технических требований и внедрения одного или нескольких демонстраций в заголовке, существует ряд рекомендаций, которые следует соблюдать для всех игр Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-876">In addition to meeting the Technical Requirements and adopting one or more Showcases in your title, there are a number of best practices that should be followed for all Windows games.</span></span> <span data-ttu-id="0f25c-877">Хотя эти рекомендации выходят за рамки основных технических требований, настоятельно рекомендуется использовать их для всех игр для заголовков Windows.</span><span class="sxs-lookup"><span data-stu-id="0f25c-877">While these recommendations fall outside the scope of the core Technical Requirements, you are strongly encouraged to employ them for all Games for Windows titles.</span></span>

### <a name="additional-recommendations"></a><span data-ttu-id="0f25c-878">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="0f25c-878">Additional Recommendations</span></span>

-   <span data-ttu-id="0f25c-879">Используйте последнюю версию компилятора и среды выполнения Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0f25c-879">Use the most recent Visual Studio compiler and runtime.</span></span> <span data-ttu-id="0f25c-880">Более новые версии компилятора реализуют значительные улучшения для качества создаваемого кода и для проблем безопасности, а также используют современные стратегии оптимизации процессоров.</span><span class="sxs-lookup"><span data-stu-id="0f25c-880">Newer versions of the compiler implement significant improvements for the quality of code generated and for security issues, and they employ modern processor optimization strategies.</span></span> <span data-ttu-id="0f25c-881">Обновление компилятора и использование последней версии среды выполнения C — это простой способ перехода на современные методики программирования.</span><span class="sxs-lookup"><span data-stu-id="0f25c-881">Updating the compiler and using the latest C Runtime is an easy way to migrate to modern coding practices.</span></span>
-   <span data-ttu-id="0f25c-882">Используйте версию библиотеки динамической компоновки (DLL) среды выполнения C, а не статическую компоновку, и используйте защищенную CRT.</span><span class="sxs-lookup"><span data-stu-id="0f25c-882">Use the dynamic-link library (DLL) version of the C Runtime, rather than static linking, and make use of Secure CRT.</span></span> <span data-ttu-id="0f25c-883">(Исключения могут быть сделаны в специальных сценариях предустановки, например для программы автозапуска или для самого установщика).</span><span class="sxs-lookup"><span data-stu-id="0f25c-883">(Exceptions can be made in special pre-installation cases, like for an Autorun program or for the installer itself).</span></span>
-   <span data-ttu-id="0f25c-884">Для игрового звука используйте XAudio2, X3DAudio и (или) запись транзакций вместо DirectSound.</span><span class="sxs-lookup"><span data-stu-id="0f25c-884">For game audio, use XAudio2, X3DAudio, and/or XACT, rather than DirectSound.</span></span> <span data-ttu-id="0f25c-885">Для обработчиков аудио, которые выполняют все смешивание и преобразование исходных данных и требуют только решения с низкой задержкой для вывода звука, используйте DirectSound в Windows XP (только) и ВАСАПИ в Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f25c-885">For audio engines that do all mixing and source-rate conversion and need only a low-latency solution for audio output, use DirectSound on Windows XP (only) and WASAPI on Windows Vista and Windows 7.</span></span>
-   <span data-ttu-id="0f25c-886">Старайтесь не использовать устаревшие и устаревшие интерфейсы API: DirectDraw, DirectSound, DirectPlay, уровень производительности DirectMusic, радиосвязь DirectPlay и режим "в режиме поддержки Direct3D".</span><span class="sxs-lookup"><span data-stu-id="0f25c-886">Avoid using legacy and deprecated APIs: DirectDraw, DirectSound, DirectPlay, DirectMusic's performance layer, DirectPlay Voice, and Direct3D Retained Mode.</span></span> <span data-ttu-id="0f25c-887">Обратите внимание, что в Windows Vista и Windows 7 недоступен режим "Радиочастота DirectPlay" и "сохраняемый Direct3D".</span><span class="sxs-lookup"><span data-stu-id="0f25c-887">Note that DirectPlay Voice and Direct3D Retained Mode are not available at all on Windows Vista or Windows 7.</span></span> <span data-ttu-id="0f25c-888">Уровень производительности DirectPlay и DirectMusic недоступен для приложений для машинного кода x64.</span><span class="sxs-lookup"><span data-stu-id="0f25c-888">DirectPlay and DirectMusic's performance layer are not available to x64-native applications.</span></span>
-   <span data-ttu-id="0f25c-889">Оптимизируйте использование наборов инструкций SSE/SSE2 SIMD.</span><span class="sxs-lookup"><span data-stu-id="0f25c-889">Optimize using SSE/SSE2 SIMD instruction sets.</span></span> <span data-ttu-id="0f25c-890">См. API [директксмас](/windows/desktop/dxmath/directxmath-portal) в Windows SDK в качестве межплатформенного решения для операций с оптимизированными для SIMD математическими операциями.</span><span class="sxs-lookup"><span data-stu-id="0f25c-890">See the [DirectXMath](/windows/desktop/dxmath/directxmath-portal) API in the Windows SDK as a cross-platform solution for SIMD-optimized math operations.</span></span>
-   <span data-ttu-id="0f25c-891">Используйте современные рекомендации для обеспечения безопасности Windows (включая параметры компилятора и компоновщика, такие как **/NXCOMPAT**, **/GS**, **/SAFESEH**, **/DynamicBase**, **/SDL** и т. д.).</span><span class="sxs-lookup"><span data-stu-id="0f25c-891">Use modern best practices for Windows security (including compiler and linker options like **/NXCOMPAT**, **/GS**, **/SAFESEH**, **/DYNAMICBASE**, **/SDL**, and so on).</span></span> <span data-ttu-id="0f25c-892">Дополнительные сведения см. [в разделе Лучшие методики обеспечения безопасности при разработке игр](/windows/desktop/DxTechArts/best-security-practices-in-game-development).</span><span class="sxs-lookup"><span data-stu-id="0f25c-892">For more information, see [Best Security Practices in Game Development](/windows/desktop/DxTechArts/best-security-practices-in-game-development).</span></span>
-   <span data-ttu-id="0f25c-893">Используйте новейшие компоненты и библиотеки Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0f25c-893">Use the latest Windows SDK components and libraries.</span></span> <span data-ttu-id="0f25c-894">Удалите зависимости от устаревших Директсетуп, развернутых нестандартных компонентов, таких как D3DX9, D3DX10 и D3DX11.</span><span class="sxs-lookup"><span data-stu-id="0f25c-894">Remove dependencies on the legacy DirectSetup deployed out-of-band components such as D3DX9, D3DX10, and D3DX11.</span></span> <span data-ttu-id="0f25c-895">Рассмотрите возможность использования [директкстекс](https://github.com/Microsoft/DirectXTex) или [директкстк](https://github.com/Microsoft/DirectXTK) или и того, и другого.</span><span class="sxs-lookup"><span data-stu-id="0f25c-895">Consider using [DirectXTex](https://github.com/Microsoft/DirectXTex) or [DirectXTK](https://github.com/Microsoft/DirectXTK) or both.</span></span>
-   <span data-ttu-id="0f25c-896">Избегайте использования более старого компилятора HLSL, а вместо этого используйте современный компилятор HLSL.</span><span class="sxs-lookup"><span data-stu-id="0f25c-896">Avoid using the older HLSL compiler, and instead, use the modern HLSL compiler.</span></span> <span data-ttu-id="0f25c-897">Если для приложения требуется поддержка Pixel Shader 1. x, используйте сборку шейдера вместо HLSL или ограничьте использование более старого компилятора только этими сценариями.</span><span class="sxs-lookup"><span data-stu-id="0f25c-897">If support for Pixel Shader 1.x is required by your application, use shader assembly rather than HLSL, or limit the use of the older compiler to just those scenarios.</span></span>

## <a name="resources"></a><span data-ttu-id="0f25c-898">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="0f25c-898">Resources</span></span>



| <span data-ttu-id="0f25c-899">Термин</span><span class="sxs-lookup"><span data-stu-id="0f25c-899">Term</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="0f25c-900">Описание</span><span class="sxs-lookup"><span data-stu-id="0f25c-900">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f25c-901"><span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Игры для Windows: тестовые случаи</span><span class="sxs-lookup"><span data-stu-id="0f25c-901"><span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Games for Windows: Test Cases</span></span> <br/>                              | <span data-ttu-id="0f25c-902">Рекомендации по работе с играми в Windows XP, Windows Vista и Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f25c-902">Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="0f25c-903"><span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0f25c-903"><span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows SDK</span></span> <br/>                                                                                                      | [<span data-ttu-id="0f25c-904">Пакеты SDK для Windows</span><span class="sxs-lookup"><span data-stu-id="0f25c-904">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span data-ttu-id="0f25c-905"><span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>Рекомендации по контролю учетных записей пользователей</span><span class="sxs-lookup"><span data-stu-id="0f25c-905"><span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>User Account Control Guidelines</span></span> <br/>                      | <span data-ttu-id="0f25c-906">[Требования к разработке приложений Windows Vista для обеспечения совместимости управления учетными записями пользователей](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="0f25c-906">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span><br/> |
| <span data-ttu-id="0f25c-907"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Портал разработчика Винкуал</span><span class="sxs-lookup"><span data-stu-id="0f25c-907"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> <br/>                                                  | [<span data-ttu-id="0f25c-908">Веб-службы Windows Quality Services (Винкуал)</span><span class="sxs-lookup"><span data-stu-id="0f25c-908">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span data-ttu-id="0f25c-909"><span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>Портал разработчика DirectX</span><span class="sxs-lookup"><span data-stu-id="0f25c-909"><span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>DirectX Developer Portal</span></span> <br/>                                                  | <span data-ttu-id="0f25c-910">[Центр разработчиков DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="0f25c-910">[Directx Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span><br/>                                                                               |
| <span data-ttu-id="0f25c-911"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Блог о играх для Windows и DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="0f25c-911"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span><br/> | [<span data-ttu-id="0f25c-912">Записи блога, посвященные играм для Windows и DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="0f25c-912">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)<br/>                                                                           |
| <span data-ttu-id="0f25c-913"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Дополнительные статьи по DirectX</span><span class="sxs-lookup"><span data-stu-id="0f25c-913"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span><br/>                                             | [<span data-ttu-id="0f25c-914">Технические статьи по DirectX</span><span class="sxs-lookup"><span data-stu-id="0f25c-914">DirectX Technical Articles</span></span>](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

