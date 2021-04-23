---
title: Параметры WER
description: Параметры для настройки отчетов о проблемах. Все эти параметры можно задать с помощью групповая политика. Некоторые из них также можно изменить в центре поддержки для Windows 7 и Windows 8. Для Windows 10 используйте функцию поиска в параметрах, чтобы найти дополнительные параметры системы.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Отчеты об ошибках Windows отчетов об ошибках Windows, параметры
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 28b6abbda7d851daddb75ec534b8128d1a831b3f
ms.sourcegitcommit: 434d5437d4c31c47358598ea5275177c2698f557
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "105651539"
---
# <a name="wer-settings"></a><span data-ttu-id="07cfb-107">Параметры WER</span><span class="sxs-lookup"><span data-stu-id="07cfb-107">WER Settings</span></span>

<span data-ttu-id="07cfb-108">Отчеты об ошибках Windows (WER) предоставляет множество параметров для настройки отчетов о проблемах.</span><span class="sxs-lookup"><span data-stu-id="07cfb-108">Windows Error Reporting (WER) provides many settings to customize the problem reporting experience.</span></span> <span data-ttu-id="07cfb-109">Все эти параметры можно задать с помощью групповая политика.</span><span class="sxs-lookup"><span data-stu-id="07cfb-109">All of these settings can be set using Group Policy.</span></span> <span data-ttu-id="07cfb-110">Некоторые из них также можно изменить в **центре поддержки** для Windows 7 и Windows 8.</span><span class="sxs-lookup"><span data-stu-id="07cfb-110">Some can also be changed in **Action Center** for Windows 7 and Windows 8.</span></span> <span data-ttu-id="07cfb-111">Для Windows 10 используйте функцию поиска в параметрах, чтобы найти **Дополнительные параметры системы**.</span><span class="sxs-lookup"><span data-stu-id="07cfb-111">For Windows 10, use the search function in Settings to locate **View advanced system settings**.</span></span> <span data-ttu-id="07cfb-112">Параметры WER находятся в одном из следующих подразделов реестра:</span><span class="sxs-lookup"><span data-stu-id="07cfb-112">WER settings are located in one of the following registry subkeys:</span></span>

-   <span data-ttu-id="07cfb-113">**HKey \_ Текущее \_ пользовательское** \\ **программное обеспечение** \\ **Microsoft** \\ **Windows** \\ **отчеты об ошибках Windows**</span><span class="sxs-lookup"><span data-stu-id="07cfb-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>
-   <span data-ttu-id="07cfb-114">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **Windows** \\ **отчеты об ошибках Windows**</span><span class="sxs-lookup"><span data-stu-id="07cfb-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>

## <a name="windows-error-reporting-subkey"></a><span data-ttu-id="07cfb-115">Подраздел отчеты об ошибках Windows</span><span class="sxs-lookup"><span data-stu-id="07cfb-115">Windows Error Reporting subkey</span></span>

<dl> <dt>

<span data-ttu-id="07cfb-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**бипассдатасроттлинг**</span><span class="sxs-lookup"><span data-stu-id="07cfb-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-117">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-117">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-118">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-118">Possible values:</span></span><dl> <dd>

<span data-ttu-id="07cfb-119">0 — отключить регулирование для обхода данных.</span><span class="sxs-lookup"><span data-stu-id="07cfb-119">0 - Disable data bypass throttling.</span></span> <span data-ttu-id="07cfb-120">Если обход отключен или не настроен в качестве параметра политики, WER по умолчанию регулирует данные.</span><span class="sxs-lookup"><span data-stu-id="07cfb-120">If the bypass is disabled or not configured as a policy setting, WER throttles data by default.</span></span> <span data-ttu-id="07cfb-121">WER не отправляет более одного CAB-файла для отчета, содержащего данные о тех же типах событий.</span><span class="sxs-lookup"><span data-stu-id="07cfb-121">WER does not upload more than one CAB file for a report that contains data about the same event types.</span></span>

</dd> <dd>

<span data-ttu-id="07cfb-122">1 — включить регулирование для обхода данных.</span><span class="sxs-lookup"><span data-stu-id="07cfb-122">1 - Enable data bypass throttling.</span></span> <span data-ttu-id="07cfb-123">WER не регулирует данные.</span><span class="sxs-lookup"><span data-stu-id="07cfb-123">WER does not throttle data.</span></span> <span data-ttu-id="07cfb-124">WER отправляет дополнительные CAB-файлы, которые могут содержать данные о тех же типах событий, что и ранее отправленный отчет.</span><span class="sxs-lookup"><span data-stu-id="07cfb-124">WER uploads additional CAB files that can contain data about the same event types as an earlier uploaded report.</span></span>

</dd> </dl>

<span data-ttu-id="07cfb-125">Следует ли включить обход регулирования данных клиента WER</span><span class="sxs-lookup"><span data-stu-id="07cfb-125">Whether to enable the bypass of WER client data throttling</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**конфигуреарчиве**</span><span class="sxs-lookup"><span data-stu-id="07cfb-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-127">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-127">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-128">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-128">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-129">1 — только параметры (по умолчанию в Windows 7)</span><span class="sxs-lookup"><span data-stu-id="07cfb-129">1 - Parameters only (default on Windows 7)</span></span></dd> <dd><span data-ttu-id="07cfb-130">2 — все данные (по умолчанию в Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="07cfb-130">2 - All data (default on Windows Vista)</span></span></dd> </dl>

<span data-ttu-id="07cfb-131">Следует ли архивировать только параметры или все данные</span><span class="sxs-lookup"><span data-stu-id="07cfb-131">Whether to archive parameters only or all data</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**\\Дефаултконсент согласия**</span><span class="sxs-lookup"><span data-stu-id="07cfb-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consent\\DefaultConsent**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-133">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-133">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-134">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-134">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-135">1 — всегда спрашивать (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-135">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="07cfb-136">2 — только параметры</span><span class="sxs-lookup"><span data-stu-id="07cfb-136">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="07cfb-137">3 — параметры и данные безопасности</span><span class="sxs-lookup"><span data-stu-id="07cfb-137">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="07cfb-138">4 — все данные</span><span class="sxs-lookup"><span data-stu-id="07cfb-138">4 - All data</span></span></dd> </dl>

<span data-ttu-id="07cfb-139">Вариант согласия по умолчанию</span><span class="sxs-lookup"><span data-stu-id="07cfb-139">Default consent choice</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**\\Дефаултоверридебехавиор согласия**</span><span class="sxs-lookup"><span data-stu-id="07cfb-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consent\\DefaultOverrideBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-141">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-141">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-142">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-142">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-143">0 — разрешение по вертикали будет переопределять согласие по умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-143">0 - Vertical consent will override the default consent (default)</span></span></dd> <dd><span data-ttu-id="07cfb-144">1 — согласие по умолчанию будет переопределять согласие конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="07cfb-144">1 - Default consent will override the application-specific consent</span></span></dd> </dl>

<span data-ttu-id="07cfb-145">Указывает, переопределяет ли согласие по умолчанию разрешение по вертикали</span><span class="sxs-lookup"><span data-stu-id="07cfb-145">Whether default consent overrides vertical consent</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**\\ \[ Вертикалнаме согласия\]**</span><span class="sxs-lookup"><span data-stu-id="07cfb-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consent\\\[VerticalName\]**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-147">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-147">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-148">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-148">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-149">1 — всегда спрашивать (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-149">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="07cfb-150">2 — только параметры</span><span class="sxs-lookup"><span data-stu-id="07cfb-150">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="07cfb-151">3 — параметры и данные безопасности</span><span class="sxs-lookup"><span data-stu-id="07cfb-151">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="07cfb-152">4 — все данные</span><span class="sxs-lookup"><span data-stu-id="07cfb-152">4 - All data</span></span></dd> </dl>

<span data-ttu-id="07cfb-153">Вариант согласия для подключаемого модуля WER</span><span class="sxs-lookup"><span data-stu-id="07cfb-153">Consent choice for the WER plug-in</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**корпоратевердиректори**</span><span class="sxs-lookup"><span data-stu-id="07cfb-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-155">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="07cfb-155">**REG\_SZ**</span></span>

<span data-ttu-id="07cfb-156">Путь к каталогу</span><span class="sxs-lookup"><span data-stu-id="07cfb-156">The directory path</span></span>

<span data-ttu-id="07cfb-157">Целевой каталог на сервере</span><span class="sxs-lookup"><span data-stu-id="07cfb-157">Target directory on the server</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**корпоратеверпортнумбер**</span><span class="sxs-lookup"><span data-stu-id="07cfb-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-159">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-159">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-160">Номер порта</span><span class="sxs-lookup"><span data-stu-id="07cfb-160">The port number</span></span>

<span data-ttu-id="07cfb-161">Номер порта, используемый с корпоративным сервером</span><span class="sxs-lookup"><span data-stu-id="07cfb-161">Port number to be used with the corporate server</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**корпоратеверсервер**</span><span class="sxs-lookup"><span data-stu-id="07cfb-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-163">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="07cfb-163">**REG\_SZ**</span></span>

<span data-ttu-id="07cfb-164">имя сервера;</span><span class="sxs-lookup"><span data-stu-id="07cfb-164">The name of the server</span></span>

<span data-ttu-id="07cfb-165">Имя корпоративного сервера</span><span class="sxs-lookup"><span data-stu-id="07cfb-165">Corporate server name</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**корпоратеверусеаусентикатион**</span><span class="sxs-lookup"><span data-stu-id="07cfb-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-167">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-167">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-168">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-168">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-169">0 — нет (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-169">0 - No (default)</span></span></dd> <dd><span data-ttu-id="07cfb-170">1 — да;</span><span class="sxs-lookup"><span data-stu-id="07cfb-170">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="07cfb-171">Использовать ли встроенную проверку подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="07cfb-171">Whether to use Windows Integrated Authentication</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**корпоратеверусессл**</span><span class="sxs-lookup"><span data-stu-id="07cfb-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-173">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-173">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-174">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-174">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-175">0 — нет (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-175">0 - No (default)</span></span></dd> <dd><span data-ttu-id="07cfb-176">1 — да;</span><span class="sxs-lookup"><span data-stu-id="07cfb-176">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="07cfb-177">Использовать ли SSL</span><span class="sxs-lookup"><span data-stu-id="07cfb-177">Whether to use SSL</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**Дебугаппликатионс \\ \[ ексенаме \] (замените " \[ ексенаме \] " фактическим именем exe-файла, например "notepad.exe").**</span><span class="sxs-lookup"><span data-stu-id="07cfb-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications\\\[ExeName\] (replace "\[ExeName\]" with an actual name of an .exe file, for example, "notepad.exe")**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-179">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-179">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-180">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-180">Possible values:</span></span>

<dl> <dd><span data-ttu-id="07cfb-181">0 — процессам с именем исполняемого образа **\[ ексенаме \]** не требуется, чтобы пользователь выбрал параметр **Отладка** или **продолжить** (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-181">0 - Processes with an executable image name of **\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="07cfb-182">1 — процессам с именем исполняемого образа **\[ ексенаме \]** требуется, чтобы пользователь выбрал параметр **Отладка** или **продолжить** .</span><span class="sxs-lookup"><span data-stu-id="07cfb-182">1 - Processes with an executable image name of **\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="07cfb-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**Дебугаппликатионс \\ \* (" \* " — это имя литерального значения)**</span><span class="sxs-lookup"><span data-stu-id="07cfb-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications\\\* ("\*" is the literal value name)**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-184">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-184">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-185">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-185">Possible values:</span></span>

<dl> <dd><span data-ttu-id="07cfb-186">0 — все процессы, кроме тех, которые явно указаны в параметре **дебугаппликатионс \\ \[ \] ексенаме** , не нуждаются в выборе варианта " **Отладка** **" или "продолжить"** (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-186">0 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="07cfb-187">1 — все процессы, кроме тех, которые явно указаны в параметре **дебугаппликатионс \\ \[ ексенаме \]** , потребовали от пользователя выбрать **отладку** или **продолжить** .</span><span class="sxs-lookup"><span data-stu-id="07cfb-187">1 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="07cfb-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**дисаблеарчиве**</span><span class="sxs-lookup"><span data-stu-id="07cfb-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-189">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-189">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-190">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-190">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-191">0 - Включено</span><span class="sxs-lookup"><span data-stu-id="07cfb-191">0 - Enabled</span></span></dd> <dd><span data-ttu-id="07cfb-192">1 - Выключено</span><span class="sxs-lookup"><span data-stu-id="07cfb-192">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="07cfb-193">Включение или отключение архива</span><span class="sxs-lookup"><span data-stu-id="07cfb-193">Enable or disable the archive</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Доступ**</span><span class="sxs-lookup"><span data-stu-id="07cfb-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-195">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-195">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-196">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-196">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-197">0 — включено (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-197">0 - Enabled (default)</span></span></dd> <dd><span data-ttu-id="07cfb-198">1 - Выключено</span><span class="sxs-lookup"><span data-stu-id="07cfb-198">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="07cfb-199">Включение и отключение WER</span><span class="sxs-lookup"><span data-stu-id="07cfb-199">Enable or disable WER</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**дисаблекуеуе**</span><span class="sxs-lookup"><span data-stu-id="07cfb-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-201">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-201">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-202">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-202">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-203">0 - Включено</span><span class="sxs-lookup"><span data-stu-id="07cfb-203">0 - Enabled</span></span></dd> <dd><span data-ttu-id="07cfb-204">1 - Выключено</span><span class="sxs-lookup"><span data-stu-id="07cfb-204">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="07cfb-205">Включение или отключение очереди отчетов</span><span class="sxs-lookup"><span data-stu-id="07cfb-205">Enable or disable report queuing</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span><span class="sxs-lookup"><span data-stu-id="07cfb-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-207">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-207">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-208">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-208">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-209">0 — пользовательский интерфейс (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-209">0 - UI (default)</span></span></dd> <dd><span data-ttu-id="07cfb-210">1 — нет пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="07cfb-210">1 - No UI</span></span></dd> </dl>

<span data-ttu-id="07cfb-211">Включение или отключение пользовательского интерфейса WER</span><span class="sxs-lookup"><span data-stu-id="07cfb-211">Enable or disable the WER UI</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**донтсендаддитионалдата**</span><span class="sxs-lookup"><span data-stu-id="07cfb-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-213">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-213">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-214">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-214">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-215">0 — отправить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-215">0 - Send (default)</span></span></dd> <dd><span data-ttu-id="07cfb-216">1 — не отправляйте</span><span class="sxs-lookup"><span data-stu-id="07cfb-216">1 - Do not send</span></span></dd> </dl>

<span data-ttu-id="07cfb-217">Следует ли запретить отправку данных второго уровня</span><span class="sxs-lookup"><span data-stu-id="07cfb-217">Whether to prevent sending second-level data</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**\\ \[ Имя приложения ексклудедаппликатионс\]**</span><span class="sxs-lookup"><span data-stu-id="07cfb-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**ExcludedApplications\\\[Application Name\]**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-219">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="07cfb-219">**REG\_SZ**</span></span>

<span data-ttu-id="07cfb-220">Использование [ **вераддексклудедаппликатион**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span><span class="sxs-lookup"><span data-stu-id="07cfb-220">Use [**WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span></span>

<span data-ttu-id="07cfb-221">Список исключенных приложений</span><span class="sxs-lookup"><span data-stu-id="07cfb-221">List of excluded applications</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**форцекуеуе**</span><span class="sxs-lookup"><span data-stu-id="07cfb-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-223">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-223">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-224">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-224">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-225">0 — нет (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-225">0 - No (default)</span></span></dd> <dd><span data-ttu-id="07cfb-226">1 — да;</span><span class="sxs-lookup"><span data-stu-id="07cfb-226">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="07cfb-227">Следует ли отсылать все отчеты в очередь пользователя</span><span class="sxs-lookup"><span data-stu-id="07cfb-227">Whether to send all reports to the user's queue</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**Локалдумпс \\ Думпфолдер** или **локалдумпс \\ \[ имя приложения \] \\ думпфолдер**</span><span class="sxs-lookup"><span data-stu-id="07cfb-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps\\DumpFolder** or **LocalDumps\\\[Application Name\]\\DumpFolder**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-229">**\_распаковать \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="07cfb-229">**REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="07cfb-230">Путь к каталогу.</span><span class="sxs-lookup"><span data-stu-id="07cfb-230">The directory path.</span></span> <span data-ttu-id="07cfb-231">Значение по умолчанию —% LOCALAPPDATA% \\ CrashDumps.</span><span class="sxs-lookup"><span data-stu-id="07cfb-231">The default value is %LOCALAPPDATA%\\CrashDumps.</span></span> <span data-ttu-id="07cfb-232">Если значение по умолчанию не используется, приложение должно обеспечить наличие достаточного ACL для папки.</span><span class="sxs-lookup"><span data-stu-id="07cfb-232">If the default is not used, the application must ensure that the folder has a sufficient ACL.</span></span>

<span data-ttu-id="07cfb-233">**Windows Vista:** Значения реестра в ключе **локалдумпс** не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="07cfb-233">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="07cfb-234">Обратите внимание, что это поведение изменилось в Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="07cfb-234">Note that this behavior changed with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="07cfb-235">Путь, по которому должны храниться файлы дампа.</span><span class="sxs-lookup"><span data-stu-id="07cfb-235">The path where the dump files are to be stored.</span></span>

<span data-ttu-id="07cfb-236">Обратите внимание, что параметры для каждого процесса будут переопределять все существующие глобальные параметры для получения дополнительных сведений, см. раздел [сбор User-Mode дампов](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="07cfb-236">Note that per-process settings will override any global settings that exist For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

<span data-ttu-id="07cfb-237">Этот параметр не поддерживается в кусте реестра **hKey " \_ текущий \_ пользователь** ".</span><span class="sxs-lookup"><span data-stu-id="07cfb-237">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**Локалдумпс \\ Думпкаунт** или **локалдумпс \\ \[ имя приложения \] \\ думпкаунт**</span><span class="sxs-lookup"><span data-stu-id="07cfb-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps\\DumpCount** or **LocalDumps\\\[Application Name\]\\DumpCount**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-239">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-239">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-240">Максимальное число.</span><span class="sxs-lookup"><span data-stu-id="07cfb-240">The maximum number.</span></span> <span data-ttu-id="07cfb-241">Значение по умолчанию равно 10.</span><span class="sxs-lookup"><span data-stu-id="07cfb-241">The default is 10.</span></span> <span data-ttu-id="07cfb-242">Если превышено максимальное значение, самый старый файл дампа в папке будет заменен новым файлом дампа.</span><span class="sxs-lookup"><span data-stu-id="07cfb-242">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span>

<span data-ttu-id="07cfb-243">**Windows Vista:** Значения реестра в ключе **локалдумпс** не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="07cfb-243">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="07cfb-244">Обратите внимание, что это поведение изменилось в Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="07cfb-244">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="07cfb-245">Максимальное число файлов дампа в папке.</span><span class="sxs-lookup"><span data-stu-id="07cfb-245">The maximum number of dump files in the folder.</span></span>

<span data-ttu-id="07cfb-246">Этот параметр не поддерживается в кусте реестра **hKey " \_ текущий \_ пользователь** ".</span><span class="sxs-lookup"><span data-stu-id="07cfb-246">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**Локалдумпс \\ Думптипе** или **локалдумпс \\ \[ имя приложения \] \\ думптипе**</span><span class="sxs-lookup"><span data-stu-id="07cfb-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps\\DumpType** or **LocalDumps\\\[Application Name\]\\DumpType**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-248">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-248">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-249">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-249">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-250">0 — пользовательский дамп</span><span class="sxs-lookup"><span data-stu-id="07cfb-250">0 - Custom dump</span></span></dd> <dd><span data-ttu-id="07cfb-251">1 — Малый дамп (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-251">1 - Minidump (default)</span></span></dd> <dd><span data-ttu-id="07cfb-252">2. полный дамп</span><span class="sxs-lookup"><span data-stu-id="07cfb-252">2 - Full dump</span></span></dd> </dl>

<span data-ttu-id="07cfb-253">**Windows Vista:** Значения реестра в ключе **локалдумпс** не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="07cfb-253">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="07cfb-254">Обратите внимание, что это поведение изменилось в Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="07cfb-254">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="07cfb-255">Тип дампа.</span><span class="sxs-lookup"><span data-stu-id="07cfb-255">The dump type.</span></span>

<span data-ttu-id="07cfb-256">Этот параметр не поддерживается в кусте реестра **hKey " \_ текущий \_ пользователь** ".</span><span class="sxs-lookup"><span data-stu-id="07cfb-256">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**Локалдумпс \\ Кустомдумпфлагс** или **локалдумпс \\ \[ имя приложения \] \\ кустомдумпфлагс**</span><span class="sxs-lookup"><span data-stu-id="07cfb-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps\\CustomDumpFlags** or **LocalDumps\\\[Application Name\]\\CustomDumpFlags**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-258">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-258">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-259">Одно или несколько значений из перечисления [**\_ типов минидампа**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) .</span><span class="sxs-lookup"><span data-stu-id="07cfb-259">One or more values from the [**MINIDUMP\_TYPE**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) enumeration.</span></span> <span data-ttu-id="07cfb-260">Значение по умолчанию — {**минидумпвисдатасегс** \| **минидумпвисунлоадедмодулес** \| **минидумпвиспроцесссреаддата**}.</span><span class="sxs-lookup"><span data-stu-id="07cfb-260">The default is {**MiniDumpWithDataSegs**\|**MiniDumpWithUnloadedModules**\|**MiniDumpWithProcessThreadData**}.</span></span>

<span data-ttu-id="07cfb-261">**Windows Vista:** Значения реестра в ключе **локалдумпс** не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="07cfb-261">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="07cfb-262">Обратите внимание, что это поведение изменилось в Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="07cfb-262">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="07cfb-263">Используемые параметры пользовательского дампа.</span><span class="sxs-lookup"><span data-stu-id="07cfb-263">The custom dump options to be used.</span></span> <span data-ttu-id="07cfb-264">Это значение используется, только если **думптипе** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="07cfb-264">This value is used only when **DumpType** is set to 0.</span></span>

<span data-ttu-id="07cfb-265">Этот параметр не поддерживается в кусте реестра **hKey " \_ текущий \_ пользователь** ".</span><span class="sxs-lookup"><span data-stu-id="07cfb-265">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**логгингдисаблед**</span><span class="sxs-lookup"><span data-stu-id="07cfb-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-267">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-267">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-268">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="07cfb-268">Possible values:</span></span><dl> <dd><span data-ttu-id="07cfb-269">0 — включено (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07cfb-269">0–Enabled (default)</span></span></dd> <dd><span data-ttu-id="07cfb-270">1 — отключено</span><span class="sxs-lookup"><span data-stu-id="07cfb-270">1–Disabled</span></span></dd> </dl>

<span data-ttu-id="07cfb-271">Включение или отключение ведения журнала</span><span class="sxs-lookup"><span data-stu-id="07cfb-271">Enable or disable logging</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**максарчивекаунт**</span><span class="sxs-lookup"><span data-stu-id="07cfb-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-273">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-273">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-274">Диапазон возможных значений: 1 – 5000.</span><span class="sxs-lookup"><span data-stu-id="07cfb-274">Range of possible values: 1–5000.</span></span> <span data-ttu-id="07cfb-275">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="07cfb-275">The default is 1000.</span></span>

<span data-ttu-id="07cfb-276">Максимальный размер архива, в файлах</span><span class="sxs-lookup"><span data-stu-id="07cfb-276">Maximum size of the archive, in files</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**макскуеуекаунт**</span><span class="sxs-lookup"><span data-stu-id="07cfb-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-278">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-278">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-279">Диапазон возможных значений: 1 – 500.</span><span class="sxs-lookup"><span data-stu-id="07cfb-279">Range of possible values: 1–500.</span></span> <span data-ttu-id="07cfb-280">Число по умолчанию — 50.</span><span class="sxs-lookup"><span data-stu-id="07cfb-280">The default is 50.</span></span>

<span data-ttu-id="07cfb-281">Максимальный размер очереди</span><span class="sxs-lookup"><span data-stu-id="07cfb-281">Maximum size of the queue</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**куеуепестеринтервал**</span><span class="sxs-lookup"><span data-stu-id="07cfb-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-283">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-283">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-284">Число дней</span><span class="sxs-lookup"><span data-stu-id="07cfb-284">Number of days</span></span>

<span data-ttu-id="07cfb-285">Интервал между напоминаниями, которые пользователь проверяет на наличие решений, в днях</span><span class="sxs-lookup"><span data-stu-id="07cfb-285">Interval between reminders to the user to check for solutions, in days</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**Рунтимиксцептионхелпермодулес! \[ имя Пвсзаутофпроцесскаллбаккдлл, включая путь\]**</span><span class="sxs-lookup"><span data-stu-id="07cfb-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules!\[ pwszOutOfProcessCallbackDll name including path\]**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-287">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-287">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-288">Содержимое значения игнорируется.</span><span class="sxs-lookup"><span data-stu-id="07cfb-288">The contents of the value are ignored.</span></span>

<span data-ttu-id="07cfb-289">Имя значения используется для выборки значения Пвсзаутофпроцесскаллбаккдлл.</span><span class="sxs-lookup"><span data-stu-id="07cfb-289">The name of the value is used to fetch the pwszOutOfProcessCallbackDll value.</span></span>

<span data-ttu-id="07cfb-290">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Это значение реестра не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="07cfb-290">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This registry value is not supported.</span></span>

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a><span data-ttu-id="07cfb-291">Параметры активных отчетов о ядре WER</span><span class="sxs-lookup"><span data-stu-id="07cfb-291">WER Live Kernel Reports Settings</span></span>

<span data-ttu-id="07cfb-292">Параметры отчетов о ядре в режиме реального времени, описанные далее, находятся в следующем подразделе реестра:</span><span class="sxs-lookup"><span data-stu-id="07cfb-292">WER's Live Kernel Reports settings, which are described next, are both located under the following registry subkey:</span></span>

-   <span data-ttu-id="07cfb-293">**HKey \_ \_** \\  \\  \\  \\ **Крашконтрол** управления CurrentControlSet системы локального компьютера</span><span class="sxs-lookup"><span data-stu-id="07cfb-293">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

## <a name="fulllivekernelreports-subkey"></a><span data-ttu-id="07cfb-294">Подраздел Фуллливекернелрепортс</span><span class="sxs-lookup"><span data-stu-id="07cfb-294">FullLiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="07cfb-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**компонентсроттлесрешолд**</span><span class="sxs-lookup"><span data-stu-id="07cfb-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-296">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-296">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-297">Пороговое значение (в часах) того, как часто любой отдельный компонент может создать полный динамический дамп.</span><span class="sxs-lookup"><span data-stu-id="07cfb-297">The threshold (in hours) of how often any single component can create a full live dump.</span></span> <span data-ttu-id="07cfb-298">Это значение должно быть больше или равно **системсроттлесрешолд**.</span><span class="sxs-lookup"><span data-stu-id="07cfb-298">This value must be greater than or equal to **SystemThrottleThreshold**.</span></span> <span data-ttu-id="07cfb-299">Если задать оба значения равными нулю (0), это приведет к отключению регулирования на основе времени.</span><span class="sxs-lookup"><span data-stu-id="07cfb-299">Setting both to zero (0) will disable all time-based throttling.</span></span> <span data-ttu-id="07cfb-300">Значение по умолчанию — 168 (7 дней).</span><span class="sxs-lookup"><span data-stu-id="07cfb-300">The default is 168 (7 days).</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**фуллливерепортсмакс**</span><span class="sxs-lookup"><span data-stu-id="07cfb-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-302">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-302">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-303">Максимальное количество полных оперативных дампов, которые могут быть на диске в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="07cfb-303">The maximum number of full live dumps that may be on disk at any given time.</span></span> <span data-ttu-id="07cfb-304">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="07cfb-304">The default is 1.</span></span> <span data-ttu-id="07cfb-305">Если установить это значение равным нулю (0), функция динамического дампа будет отключена.</span><span class="sxs-lookup"><span data-stu-id="07cfb-305">Setting this value to zero (0) will disable the live dump feature.</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**ластфуллливерепорт**</span><span class="sxs-lookup"><span data-stu-id="07cfb-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-307">**REG \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-307">**REG\_QWORD**</span></span>

<span data-ttu-id="07cfb-308">[SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , показывающий время последнего полного отчетного времени для системы или конкретного reportType.</span><span class="sxs-lookup"><span data-stu-id="07cfb-308">A [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) indicating the last full live report time, for the system or a specific ReportType.</span></span> <span data-ttu-id="07cfb-309">Используется для определения того, удовлетворен ли порог политики.</span><span class="sxs-lookup"><span data-stu-id="07cfb-309">This is used to calculate whether a policy threshold has been satisfied.</span></span>

</dd> <dt>

<span data-ttu-id="07cfb-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**системсроттлесрешолд**</span><span class="sxs-lookup"><span data-stu-id="07cfb-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-311">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cfb-311">**REG\_DWORD**</span></span>

<span data-ttu-id="07cfb-312">Пороговое значение (в часах) того, как часто любой компонент в системе может создать полный динамический дамп.</span><span class="sxs-lookup"><span data-stu-id="07cfb-312">The threshold (in hours) of how often any component on the system can create a full live dump.</span></span> <span data-ttu-id="07cfb-313">Значение по умолчанию — 120 (5 дней).</span><span class="sxs-lookup"><span data-stu-id="07cfb-313">The default is 120 (5 days).</span></span>

</dd> </dl>

## <a name="livekernelreports-subkey"></a><span data-ttu-id="07cfb-314">Подраздел Ливекернелрепортс</span><span class="sxs-lookup"><span data-stu-id="07cfb-314">LiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="07cfb-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**ливекернелрепортспас**</span><span class="sxs-lookup"><span data-stu-id="07cfb-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span></span>
</dt> <dd>

<span data-ttu-id="07cfb-316">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="07cfb-316">**REG\_SZ**</span></span>


<span data-ttu-id="07cfb-317">Перенаправленное место хранения отчетов ядра в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="07cfb-317">The redirected storage location of live kernel reports.</span></span> <span data-ttu-id="07cfb-318">Расположение по умолчанию —%Системрут%\ливекернелрепортс.</span><span class="sxs-lookup"><span data-stu-id="07cfb-318">The default location is %systemroot%\LiveKernelReports.</span></span> <span data-ttu-id="07cfb-319">Это значение должно быть допустимым путем.</span><span class="sxs-lookup"><span data-stu-id="07cfb-319">This value must be a valid path.</span></span> <span data-ttu-id="07cfb-320">Путь должен быть указан в формате пути NT.</span><span class="sxs-lookup"><span data-stu-id="07cfb-320">The path must be in NT path format.</span></span> <span data-ttu-id="07cfb-321">Например, \? ? \c: \ливедумпсфолдер.</span><span class="sxs-lookup"><span data-stu-id="07cfb-321">For example, \??\C:\LiveDumpsFolder.</span></span>  <span data-ttu-id="07cfb-322">Дополнительные сведения о форматах путей см.  [в разделе форматы путей к файлам в системах Windows](/dotnet/standard/io/file-path-formats).</span><span class="sxs-lookup"><span data-stu-id="07cfb-322">For more information on path formats, see  [File path formats on Windows systems](/dotnet/standard/io/file-path-formats).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="07cfb-323">См. также</span><span class="sxs-lookup"><span data-stu-id="07cfb-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07cfb-324">Справочник по WER</span><span class="sxs-lookup"><span data-stu-id="07cfb-324">WER Reference</span></span>](wer-reference.md)
</dt> </dl>

 

 
