---
title: Параметры WER
description: Параметры, чтобы настроить отчеты о проблемах. Все эти параметры можно задать с помощью групповая политика. некоторые из них также можно изменить в центре поддержки для Windows 7 и Windows 8. для Windows 10 используйте функцию поиска в Параметры, чтобы найти дополнительные параметры системы.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Windows отчеты об ошибках Windows отчетов об ошибках, параметры
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 4586c4f282cbc5c4e2f683c0764eac048f6c05d22a1972cb0ceb84f9699c7925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442233"
---
# <a name="wer-settings"></a>Параметры WER

отчеты об ошибках Windows (WER) предоставляет множество параметров для настройки отчетов о проблемах. Все эти параметры можно задать с помощью групповая политика. некоторые из них также можно изменить в **центре поддержки** для Windows 7 и Windows 8. для Windows 10 используйте функцию поиска в Параметры, чтобы найти **дополнительные параметры системы**. Параметры WER находятся в одном из следующих подразделов реестра:

-   **HKey \_ текущее \_ пользовательское** \\ **программное обеспечение** \\ **Microsoft** \\ **Windows** \\ **отчеты об ошибках Windows**
-   **HKey \_ \_** \\ **программное обеспечение** \\ **Microsoft** \\ **Windows** \\  на локальном компьютере отчеты об ошибках Windows

## <a name="windows-error-reporting-subkey"></a>подраздел отчеты об ошибках Windows

<dl> <dt>

<span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**бипассдатасроттлинг**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>

0 — отключить регулирование для обхода данных. Если обход отключен или не настроен в качестве параметра политики, WER по умолчанию регулирует данные. WER не отправляет более одного CAB-файла для отчета, содержащего данные о тех же типах событий.

</dd> <dd>

1 — включить регулирование для обхода данных. WER не регулирует данные. WER отправляет дополнительные CAB-файлы, которые могут содержать данные о тех же типах событий, что и ранее отправленный отчет.

</dd> </dl>

Следует ли включить обход регулирования данных клиента WER

</dd> <dt>

<span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**конфигуреарчиве**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>1 — только параметры (по умолчанию в Windows 7)</dd> <dd>2 — все данные (по умолчанию в Windows Vista)</dd> </dl>

Следует ли архивировать только параметры или все данные

</dd> <dt>

<span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**\\Дефаултконсент согласия**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>1 — всегда спрашивать (по умолчанию)</dd> <dd>2 — только параметры</dd> <dd>3 — параметры и данные безопасности</dd> <dd>4 — все данные</dd> </dl>

Вариант согласия по умолчанию

</dd> <dt>

<span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**\\Дефаултоверридебехавиор согласия**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>0 — разрешение по вертикали будет переопределять согласие по умолчанию (по умолчанию)</dd> <dd>1 — согласие по умолчанию будет переопределять согласие конкретного приложения.</dd> </dl>

Указывает, переопределяет ли согласие по умолчанию разрешение по вертикали

</dd> <dt>

<span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**\\ \[ Вертикалнаме согласия\]**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>1 — всегда спрашивать (по умолчанию)</dd> <dd>2 — только параметры</dd> <dd>3 — параметры и данные безопасности</dd> <dd>4 — все данные</dd> </dl>

Вариант согласия для подключаемого модуля WER

</dd> <dt>

<span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**корпоратевердиректори**
</dt> <dd>

**REG \_ SZ**

Путь к каталогу

Целевой каталог на сервере

</dd> <dt>

<span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**корпоратеверпортнумбер**
</dt> <dd>

**REG \_ DWORD**

Номер порта

Номер порта, используемый с корпоративным сервером

</dd> <dt>

<span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**корпоратеверсервер**
</dt> <dd>

**REG \_ SZ**

имя сервера;

Имя корпоративного сервера

</dd> <dt>

<span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**корпоратеверусеаусентикатион**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>0 — нет (по умолчанию)</dd> <dd>1 — да;</dd> </dl>

использовать ли встроенную проверку подлинности Windows

</dd> <dt>

<span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**корпоратеверусессл**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>0 — нет (по умолчанию)</dd> <dd>1 — да;</dd> </dl>

Использовать ли SSL

</dd> <dt>

<span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**Дебугаппликатионс \\ \[ ексенаме \] (замените " \[ ексенаме \] " фактическим именем файла .exe, например "notepad.exe").**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:

<dl> <dd>0 — процессам с именем исполняемого образа **\[ ексенаме \]** не требуется, чтобы пользователь выбрал параметр **Отладка** или **продолжить** (по умолчанию)</dd> <dd>1 — процессам с именем исполняемого образа **\[ ексенаме \]** требуется, чтобы пользователь выбрал параметр **Отладка** или **продолжить** .</dd> </dl> </dd> <dt>

<span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**Дебугаппликатионс \\ \* (" \* " — это имя литерального значения)**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:

<dl> <dd>0 — все процессы, кроме тех, которые явно указаны в параметре **дебугаппликатионс \\ \[ \] ексенаме** , не нуждаются в выборе варианта " **Отладка** **" или "продолжить"** (по умолчанию)</dd> <dd>1 — все процессы, кроме тех, которые явно указаны в параметре **дебугаппликатионс \\ \[ ексенаме \]** , потребовали от пользователя выбрать **отладку** или **продолжить** .</dd> </dl> </dd> <dt>

<span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**дисаблеарчиве**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>0 - Включено</dd> <dd>1 - Выключено</dd> </dl>

Включение или отключение архива

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Доступ**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>0 — включено (по умолчанию)</dd> <dd>1 - Выключено</dd> </dl>

Включение и отключение WER

</dd> <dt>

<span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**дисаблекуеуе**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>0 - Включено</dd> <dd>1 - Выключено</dd> </dl>

Включение или отключение очереди отчетов

</dd> <dt>

<span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>0 — пользовательский интерфейс (по умолчанию)</dd> <dd>1 — нет пользовательского интерфейса</dd> </dl>

Включение или отключение пользовательского интерфейса WER

</dd> <dt>

<span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**донтсендаддитионалдата**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>0 — отправить (по умолчанию)</dd> <dd>1 — не отправляйте</dd> </dl>

Следует ли запретить отправку данных второго уровня

</dd> <dt>

<span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**\\ \[ Имя приложения ексклудедаппликатионс\]**
</dt> <dd>

**REG \_ SZ**

Использование [ **вераддексклудедаппликатион**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)

Список исключенных приложений

</dd> <dt>

<span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**форцекуеуе**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>0 — нет (по умолчанию)</dd> <dd>1 — да;</dd> </dl>

Следует ли отсылать все отчеты в очередь пользователя

</dd> <dt>

<span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**Локалдумпс \\ Думпфолдер** или **локалдумпс \\ \[ имя приложения \] \\ думпфолдер**
</dt> <dd>

**\_распаковать \_ SZ**

Путь к каталогу. Значение по умолчанию —% LOCALAPPDATA% \\ CrashDumps. Если значение по умолчанию не используется, приложение должно обеспечить наличие достаточного ACL для папки.

**Windows Vista:** Значения реестра в ключе **локалдумпс** не поддерживаются. обратите внимание, что это поведение изменилось с Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).

Путь, по которому должны храниться файлы дампа.

Обратите внимание, что параметры для каждого процесса будут переопределять все существующие глобальные параметры для получения дополнительных сведений, см. раздел [сбор User-Mode дампов](collecting-user-mode-dumps.md).

Этот параметр не поддерживается в кусте реестра **hKey " \_ текущий \_ пользователь** ".

</dd> <dt>

<span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**Локалдумпс \\ Думпкаунт** или **локалдумпс \\ \[ имя приложения \] \\ думпкаунт**
</dt> <dd>

**REG \_ DWORD**

Максимальное число. Значение по умолчанию равно 10. Если превышено максимальное значение, самый старый файл дампа в папке будет заменен новым файлом дампа.

**Windows Vista:** Значения реестра в ключе **локалдумпс** не поддерживаются. обратите внимание, что это поведение изменилось с Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).

Максимальное число файлов дампа в папке.

Этот параметр не поддерживается в кусте реестра **hKey " \_ текущий \_ пользователь** ".

</dd> <dt>

<span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**Локалдумпс \\ Думптипе** или **локалдумпс \\ \[ имя приложения \] \\ думптипе**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>0 — пользовательский дамп</dd> <dd>1 — Малый дамп (по умолчанию)</dd> <dd>2. полный дамп</dd> </dl>

**Windows Vista:** Значения реестра в ключе **локалдумпс** не поддерживаются. обратите внимание, что это поведение изменилось с Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).

Тип дампа.

Этот параметр не поддерживается в кусте реестра **hKey " \_ текущий \_ пользователь** ".

</dd> <dt>

<span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**Локалдумпс \\ Кустомдумпфлагс** или **локалдумпс \\ \[ имя приложения \] \\ кустомдумпфлагс**
</dt> <dd>

**REG \_ DWORD**

Одно или несколько значений из перечисления [**\_ типов минидампа**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) . Значение по умолчанию — {**минидумпвисдатасегс** \| **минидумпвисунлоадедмодулес** \| **минидумпвиспроцесссреаддата**}.

**Windows Vista:** Значения реестра в ключе **локалдумпс** не поддерживаются. обратите внимание, что это поведение изменилось с Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).

Используемые параметры пользовательского дампа. Это значение используется, только если **думптипе** имеет значение 0.

Этот параметр не поддерживается в кусте реестра **hKey " \_ текущий \_ пользователь** ".

</dd> <dt>

<span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**логгингдисаблед**
</dt> <dd>

**REG \_ DWORD**

Возможные значения:<dl> <dd>0 — включено (по умолчанию)</dd> <dd>1 — отключено</dd> </dl>

Включение или отключение ведения журнала

</dd> <dt>

<span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**максарчивекаунт**
</dt> <dd>

**REG \_ DWORD**

Диапазон возможных значений: 1 – 5000. Значение по умолчанию — 1000.

Максимальный размер архива, в файлах

</dd> <dt>

<span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**макскуеуекаунт**
</dt> <dd>

**REG \_ DWORD**

Диапазон возможных значений: 1 – 500. Число по умолчанию — 50.

Максимальный размер очереди

</dd> <dt>

<span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**куеуепестеринтервал**
</dt> <dd>

**REG \_ DWORD**

Количество дней

Интервал между напоминаниями, которые пользователь проверяет на наличие решений, в днях

</dd> <dt>

<span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**Рунтимиксцептионхелпермодулес! \[ имя Пвсзаутофпроцесскаллбаккдлл, включая путь\]**
</dt> <dd>

**REG \_ DWORD**

Содержимое значения игнорируется.

Имя значения используется для выборки значения Пвсзаутофпроцесскаллбаккдлл.

**Windows server 2008, Windows Vista, Windows Server 2003 и Windows XP:** Это значение реестра не поддерживается.

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a>отчеты об активных ядрах WER Параметры

Параметры отчетов о ядре в режиме реального времени, описанные далее, находятся в следующем подразделе реестра:

-   **HKey \_ \_** \\  \\  \\  \\ **Крашконтрол** управления CurrentControlSet системы локального компьютера

## <a name="fulllivekernelreports-subkey"></a>Подраздел Фуллливекернелрепортс

<dl> <dt>

<span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**компонентсроттлесрешолд**
</dt> <dd>

**REG \_ DWORD**

Пороговое значение (в часах) того, как часто любой отдельный компонент может создать полный динамический дамп. Это значение должно быть больше или равно **системсроттлесрешолд**. Если задать оба значения равными нулю (0), это приведет к отключению регулирования на основе времени. Значение по умолчанию — 168 (7 дней).

</dd> <dt>

<span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**фуллливерепортсмакс**
</dt> <dd>

**REG \_ DWORD**

Максимальное количество полных оперативных дампов, которые могут быть на диске в любой момент времени. Значение по умолчанию — 1. Если установить это значение равным нулю (0), функция динамического дампа будет отключена.

</dd> <dt>

<span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**ластфуллливерепорт**
</dt> <dd>

**REG \_ QWORD**

[SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , показывающий время последнего полного отчетного времени для системы или конкретного reportType. Используется для определения того, удовлетворен ли порог политики.

</dd> <dt>

<span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**системсроттлесрешолд**
</dt> <dd>

**REG \_ DWORD**

Пороговое значение (в часах) того, как часто любой компонент в системе может создать полный динамический дамп. Значение по умолчанию — 120 (5 дней).

</dd> </dl>

## <a name="livekernelreports-subkey"></a>Подраздел Ливекернелрепортс

<dl> <dt>

<span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**ливекернелрепортспас**
</dt> <dd>

**REG \_ SZ**


Перенаправленное место хранения отчетов ядра в режиме реального времени. Расположение по умолчанию —%Системрут%\ливекернелрепортс. Это значение должно быть допустимым путем. Путь должен быть указан в формате пути NT. Например, \? ? \c: \ливедумпсфолдер.  дополнительные сведения о форматах путей см. [в разделе форматы путей к файлам в Windows systems](/dotnet/standard/io/file-path-formats).

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по WER](wer-reference.md)
</dt> </dl>

 

 
