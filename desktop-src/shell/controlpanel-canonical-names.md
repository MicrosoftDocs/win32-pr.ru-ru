---
description: Начиная с Windows Vista, элементы панели управления, входящие в состав Windows, получают каноническое имя, которое можно использовать в вызове API или инструкции командной строки для запуска этого элемента программным способом.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Канонические имена элементов панели управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fc360b0d3db0f85a057977d1898c59d09d5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990960"
---
# <a name="canonical-names-of-control-panel-items"></a><span data-ttu-id="2280b-103">Канонические имена элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="2280b-103">Canonical Names of Control Panel Items</span></span>

<span data-ttu-id="2280b-104">Начиная с Windows Vista, элементы панели управления, входящие в состав Windows, получают каноническое имя, которое можно использовать в [вызове API или инструкции командной строки](executing-control-panel-items.md) для запуска этого элемента программным способом.</span><span class="sxs-lookup"><span data-stu-id="2280b-104">As of Windows Vista, Control Panel items included with Windows are given a canonical name that can be used in an [API call or a command-line instruction](executing-control-panel-items.md) to programmatically launch that item.</span></span> <span data-ttu-id="2280b-105">Начиная с Windows 7 и Windows Server 2008 R2 канонические имена можно использовать в групповой политике для скрытия отдельных элементов панели управления.</span><span class="sxs-lookup"><span data-stu-id="2280b-105">As of Windows 7 and Windows Server 2008 R2, canonical names can be used in a group policy to hide specific Control Panel items.</span></span> <span data-ttu-id="2280b-106">В этом разделе приводятся сведения для каждого элемента панели управления: каноническое имя, GUID, имя модуля и версии операционной системы, которые распознают каноническое имя.</span><span class="sxs-lookup"><span data-stu-id="2280b-106">This topic provides details for each Control Panel item: canonical name, GUID, module name, and the operating system versions that recognize the canonical name.</span></span>

> [!Note]  
> <span data-ttu-id="2280b-107">Канонические имена для элементов панели управления не поддерживаются до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2280b-107">Canonical names for Control Panel items are not supported prior to Windows Vista.</span></span>

 

-   [<span data-ttu-id="2280b-108">Канонические имена панели управления</span><span class="sxs-lookup"><span data-stu-id="2280b-108">Control Panel Canonical Names</span></span>](#control-panel-canonical-names)
-   [<span data-ttu-id="2280b-109">Устаревшие канонические имена панели управления</span><span class="sxs-lookup"><span data-stu-id="2280b-109">Deprecated Control Panel Canonical Names</span></span>](#deprecated-control-panel-canonical-names)
-   [<span data-ttu-id="2280b-110">Использование канонических имен в групповая политика</span><span class="sxs-lookup"><span data-stu-id="2280b-110">Using Canonical Names in Group Policy</span></span>](#using-canonical-names-in-local-group-policy)
-   [<span data-ttu-id="2280b-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="2280b-111">Remarks</span></span>](#remarks)

## <a name="control-panel-canonical-names"></a><span data-ttu-id="2280b-112">Канонические имена панели управления</span><span class="sxs-lookup"><span data-stu-id="2280b-112">Control Panel Canonical Names</span></span>

<span data-ttu-id="2280b-113">Указывает, что следует помнить при работе со следующими значениями:</span><span class="sxs-lookup"><span data-stu-id="2280b-113">Points to remember when working with these values:</span></span>

-   <span data-ttu-id="2280b-114">По определению канонические имена не меняются в зависимости от языка системы; они всегда находятся на английском языке, даже если язык системы отсутствует.</span><span class="sxs-lookup"><span data-stu-id="2280b-114">By definition, canonical names do not change based on the system language; they're always in English, even if the system's language is not.</span></span>
-   <span data-ttu-id="2280b-115">Не все элементы панели управления представлены во всех окнах.</span><span class="sxs-lookup"><span data-stu-id="2280b-115">Not all Control Panel items are present in all varieties of Windows.</span></span>
-   <span data-ttu-id="2280b-116">Некоторые элементы панели управления отображаются только в том случае, если в системе обнаружено правильное оборудование.</span><span class="sxs-lookup"><span data-stu-id="2280b-116">Some Control Panel items only appear if the right hardware is detected on the system.</span></span>
-   <span data-ttu-id="2280b-117">Сторонние лица также могут добавлять элементы панели управления.</span><span class="sxs-lookup"><span data-stu-id="2280b-117">Third parties can also add Control Panel items.</span></span> <span data-ttu-id="2280b-118">Указанные здесь канонические имена предназначены только для элементов панели управления, включенных в Windows.</span><span class="sxs-lookup"><span data-stu-id="2280b-118">The canonical names listed here are only for Control Panel items that are included with Windows.</span></span>

<span data-ttu-id="2280b-119">Ниже перечислены элементы панели управления, доступные в Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="2280b-119">The following are the Control Panel items available in Windows 8.1:</span></span>

-   [<span data-ttu-id="2280b-120">Центр уведомлений</span><span class="sxs-lookup"><span data-stu-id="2280b-120">Action Center</span></span>](#action-center)
-   [<span data-ttu-id="2280b-121">Средства администрирования</span><span class="sxs-lookup"><span data-stu-id="2280b-121">Administrative Tools</span></span>](#administrative-tools)
-   [<span data-ttu-id="2280b-122">Автозапуска</span><span class="sxs-lookup"><span data-stu-id="2280b-122">AutoPlay</span></span>](#autoplay)
-   [<span data-ttu-id="2280b-123">Биометрические устройства</span><span class="sxs-lookup"><span data-stu-id="2280b-123">Biometric Devices</span></span>](#biometric-devices)
-   [<span data-ttu-id="2280b-124">Шифрование диска BitLocker</span><span class="sxs-lookup"><span data-stu-id="2280b-124">BitLocker Drive Encryption</span></span>](#bitlocker-drive-encryption)
-   [<span data-ttu-id="2280b-125">Управление цветом</span><span class="sxs-lookup"><span data-stu-id="2280b-125">Color Management</span></span>](#color-management)
-   [<span data-ttu-id="2280b-126">Диспетчер учетных данных</span><span class="sxs-lookup"><span data-stu-id="2280b-126">Credential Manager</span></span>](#credential-manager)
-   [<span data-ttu-id="2280b-127">Дата и время</span><span class="sxs-lookup"><span data-stu-id="2280b-127">Date and Time</span></span>](#date-and-time)
-   [<span data-ttu-id="2280b-128">Программы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2280b-128">Default Programs</span></span>](#default-programs)
-   [<span data-ttu-id="2280b-129">диспетчер устройств</span><span class="sxs-lookup"><span data-stu-id="2280b-129">Device Manager</span></span>](#device-manager)
-   [<span data-ttu-id="2280b-130">"Устройства и принтеры"</span><span class="sxs-lookup"><span data-stu-id="2280b-130">Devices and Printers</span></span>](#devices-and-printers)
-   [<span data-ttu-id="2280b-131">Дисплей</span><span class="sxs-lookup"><span data-stu-id="2280b-131">Display</span></span>](#display)
-   [<span data-ttu-id="2280b-132">Центр специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="2280b-132">Ease of Access Center</span></span>](#ease-of-access-center)
-   [<span data-ttu-id="2280b-133">Семейная безопасность</span><span class="sxs-lookup"><span data-stu-id="2280b-133">Family Safety</span></span>](#family-safety)
-   [<span data-ttu-id="2280b-134">История файлов</span><span class="sxs-lookup"><span data-stu-id="2280b-134">File History</span></span>](#file-history)
-   [<span data-ttu-id="2280b-135">Свойства папки</span><span class="sxs-lookup"><span data-stu-id="2280b-135">Folder Options</span></span>](#folder-options)
-   [<span data-ttu-id="2280b-136">Шрифты</span><span class="sxs-lookup"><span data-stu-id="2280b-136">Fonts</span></span>](#fonts)
-   [<span data-ttu-id="2280b-137">Домашняя группа</span><span class="sxs-lookup"><span data-stu-id="2280b-137">HomeGroup</span></span>](#homegroup)
-   [<span data-ttu-id="2280b-138">Параметры индексирования</span><span class="sxs-lookup"><span data-stu-id="2280b-138">Indexing Options</span></span>](#indexing-options)
-   [<span data-ttu-id="2280b-139">Инфракрасная связь</span><span class="sxs-lookup"><span data-stu-id="2280b-139">Infrared</span></span>](#infrared)
-   [<span data-ttu-id="2280b-140">Свойства браузера</span><span class="sxs-lookup"><span data-stu-id="2280b-140">Internet Options</span></span>](#internet-options)
-   [<span data-ttu-id="2280b-141">Инициатор iSCSI</span><span class="sxs-lookup"><span data-stu-id="2280b-141">iSCSI Initiator</span></span>](#iscsi-initiator)
-   [<span data-ttu-id="2280b-142">iSNS-сервер</span><span class="sxs-lookup"><span data-stu-id="2280b-142">iSNS Server</span></span>](#isns-server)
-   [<span data-ttu-id="2280b-143">Клавиатура</span><span class="sxs-lookup"><span data-stu-id="2280b-143">Keyboard</span></span>](#keyboard)
-   [<span data-ttu-id="2280b-144">Параметры расположения</span><span class="sxs-lookup"><span data-stu-id="2280b-144">Location Settings</span></span>](#location-settings)
-   [<span data-ttu-id="2280b-145">Мышь</span><span class="sxs-lookup"><span data-stu-id="2280b-145">Mouse</span></span>](#mouse)
-   [<span data-ttu-id="2280b-146">мпиоконфигуратион</span><span class="sxs-lookup"><span data-stu-id="2280b-146">MPIOConfiguration</span></span>](#mpioconfiguration)
-   [<span data-ttu-id="2280b-147">Центр управления сетями и общим доступом</span><span class="sxs-lookup"><span data-stu-id="2280b-147">Network and Sharing Center</span></span>](#network-and-sharing-center)
-   [<span data-ttu-id="2280b-148">Значки области уведомлений</span><span class="sxs-lookup"><span data-stu-id="2280b-148">Notification Area Icons</span></span>](#notification-area-icons)
-   [<span data-ttu-id="2280b-149">Перо и сенсорный ввод</span><span class="sxs-lookup"><span data-stu-id="2280b-149">Pen and Touch</span></span>](#pen-and-touch)
-   [<span data-ttu-id="2280b-150">Персонализация</span><span class="sxs-lookup"><span data-stu-id="2280b-150">Personalization</span></span>](#personalization)
-   [<span data-ttu-id="2280b-151">Телефон и модем</span><span class="sxs-lookup"><span data-stu-id="2280b-151">Phone and Modem</span></span>](#phone-and-modem)
-   [<span data-ttu-id="2280b-152">Параметры электропитания</span><span class="sxs-lookup"><span data-stu-id="2280b-152">Power Options</span></span>](#power-options)
-   [<span data-ttu-id="2280b-153">"Программы и компоненты",</span><span class="sxs-lookup"><span data-stu-id="2280b-153">Programs and Features</span></span>](#programs-and-features)
-   [<span data-ttu-id="2280b-154">Восстановление</span><span class="sxs-lookup"><span data-stu-id="2280b-154">Recovery</span></span>](#recovery)
-   [<span data-ttu-id="2280b-155">Регион</span><span class="sxs-lookup"><span data-stu-id="2280b-155">Region</span></span>](#region)
-   [<span data-ttu-id="2280b-156">Подключения к рабочим столам и RemoteApp</span><span class="sxs-lookup"><span data-stu-id="2280b-156">RemoteApp and Desktop Connections</span></span>](#remoteapp-and-desktop-connections)
-   [<span data-ttu-id="2280b-157">Звук</span><span class="sxs-lookup"><span data-stu-id="2280b-157">Sound</span></span>](#sound)
-   [<span data-ttu-id="2280b-158">Распознавание речи</span><span class="sxs-lookup"><span data-stu-id="2280b-158">Speech Recognition</span></span>](#speech-recognition)
-   [<span data-ttu-id="2280b-159">Дисковые пространства</span><span class="sxs-lookup"><span data-stu-id="2280b-159">Storage Spaces</span></span>](#storage-spaces)
-   [<span data-ttu-id="2280b-160">Центр синхронизации</span><span class="sxs-lookup"><span data-stu-id="2280b-160">Sync Center</span></span>](#sync-center)
-   [<span data-ttu-id="2280b-161">Система</span><span class="sxs-lookup"><span data-stu-id="2280b-161">System</span></span>](#system)
-   [<span data-ttu-id="2280b-162">Параметры планшетного ПК</span><span class="sxs-lookup"><span data-stu-id="2280b-162">Tablet PC Settings</span></span>](#tablet-pc-settings)
-   [<span data-ttu-id="2280b-163">Панель задач и Навигация</span><span class="sxs-lookup"><span data-stu-id="2280b-163">Taskbar and Navigation</span></span>](#taskbar-and-navigation)
-   [<span data-ttu-id="2280b-164">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="2280b-164">Troubleshooting</span></span>](#troubleshooting)
-   [<span data-ttu-id="2280b-165">тсаппинсталл</span><span class="sxs-lookup"><span data-stu-id="2280b-165">TSAppInstall</span></span>](#tsappinstall)
-   [<span data-ttu-id="2280b-166">Учетные записи пользователей</span><span class="sxs-lookup"><span data-stu-id="2280b-166">User Accounts</span></span>](#user-accounts)
-   [<span data-ttu-id="2280b-167">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="2280b-167">Windows Anytime Upgrade</span></span>](#windows-anytime-upgrade)
-   [<span data-ttu-id="2280b-168">Защитник Windows</span><span class="sxs-lookup"><span data-stu-id="2280b-168">Windows Defender</span></span>](#windows-defender)
-   [<span data-ttu-id="2280b-169">Брандмауэр Windows</span><span class="sxs-lookup"><span data-stu-id="2280b-169">Windows Firewall</span></span>](#windows-firewall)
-   [<span data-ttu-id="2280b-170">Центр мобильности Windows</span><span class="sxs-lookup"><span data-stu-id="2280b-170">Windows Mobility Center</span></span>](#windows-mobility-center)
-   [<span data-ttu-id="2280b-171">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="2280b-171">Windows To Go</span></span>](#windows-to-go)
-   [<span data-ttu-id="2280b-172">Клиентский компонент Центра обновления Windows</span><span class="sxs-lookup"><span data-stu-id="2280b-172">Windows Update</span></span>](#windows-update)
-   [<span data-ttu-id="2280b-173">Рабочие папки</span><span class="sxs-lookup"><span data-stu-id="2280b-173">Work Folders</span></span>](#work-folders)

### <a name="action-center"></a><span data-ttu-id="2280b-174">Центр уведомлений</span><span class="sxs-lookup"><span data-stu-id="2280b-174">Action Center</span></span>

-   <span data-ttu-id="2280b-175">**Каноническое имя**: Microsoft. актионцентер</span><span class="sxs-lookup"><span data-stu-id="2280b-175">**Canonical name**: Microsoft.ActionCenter</span></span>
-   <span data-ttu-id="2280b-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span><span class="sxs-lookup"><span data-stu-id="2280b-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span></span>
-   <span data-ttu-id="2280b-177">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-177">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-178">**Имя модуля**: @% systemroot% \\ system32 \\ActionCenterCPL.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-178">**Module name**: @%SystemRoot%\\System32\\ActionCenterCPL.dll,-1</span></span>
-   <span data-ttu-id="2280b-179">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-179">**Pages**</span></span>

    | <span data-ttu-id="2280b-180">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-180">Page Name</span></span>           | <span data-ttu-id="2280b-181">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-181">Opens</span></span>                      |
    |---------------------|----------------------------|
    | <span data-ttu-id="2280b-182">маинтенанцесеттингс</span><span class="sxs-lookup"><span data-stu-id="2280b-182">MaintenanceSettings</span></span> | <span data-ttu-id="2280b-183">Автоматическое обслуживание</span><span class="sxs-lookup"><span data-stu-id="2280b-183">Automatic Maintenance</span></span>      |
    | <span data-ttu-id="2280b-184">пажепроблемс</span><span class="sxs-lookup"><span data-stu-id="2280b-184">pageProblems</span></span>        | <span data-ttu-id="2280b-185">Отчеты о проблемах</span><span class="sxs-lookup"><span data-stu-id="2280b-185">Problem Reports</span></span>            |
    | <span data-ttu-id="2280b-186">пажерелиабилитивиев</span><span class="sxs-lookup"><span data-stu-id="2280b-186">pageReliabilityView</span></span> | <span data-ttu-id="2280b-187">Монитор надежности</span><span class="sxs-lookup"><span data-stu-id="2280b-187">Reliability Monitor</span></span>        |
    | <span data-ttu-id="2280b-188">пажереспонсеарчиве</span><span class="sxs-lookup"><span data-stu-id="2280b-188">pageResponseArchive</span></span> | <span data-ttu-id="2280b-189">Архивные сообщения</span><span class="sxs-lookup"><span data-stu-id="2280b-189">Archived Messages</span></span>          |
    | <span data-ttu-id="2280b-190">pageSettings</span><span class="sxs-lookup"><span data-stu-id="2280b-190">pageSettings</span></span>        | <span data-ttu-id="2280b-191">Параметры отчетов о проблемах</span><span class="sxs-lookup"><span data-stu-id="2280b-191">Problem Reporting Settings</span></span> |

    

     

### <a name="administrative-tools"></a><span data-ttu-id="2280b-192">«Администрирование»</span><span class="sxs-lookup"><span data-stu-id="2280b-192">Administrative Tools</span></span>

-   <span data-ttu-id="2280b-193">**Каноническое имя**: Microsoft. административетулс</span><span class="sxs-lookup"><span data-stu-id="2280b-193">**Canonical name**: Microsoft.AdministrativeTools</span></span>
-   <span data-ttu-id="2280b-194">**GUID**: {D20EA4E1-3957-11d2-A40B-0C5020524153}</span><span class="sxs-lookup"><span data-stu-id="2280b-194">**GUID**: {D20EA4E1-3957-11d2-A40B-0C5020524153}</span></span>
-   <span data-ttu-id="2280b-195">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-195">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-196">**Имя модуля**: @% systemroot% \\ system32 \\shell32.dll,-22982</span><span class="sxs-lookup"><span data-stu-id="2280b-196">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22982</span></span>

### <a name="autoplay"></a><span data-ttu-id="2280b-197">Автозапуск</span><span class="sxs-lookup"><span data-stu-id="2280b-197">AutoPlay</span></span>

-   <span data-ttu-id="2280b-198">**Каноническое имя**: Microsoft. Автозапуск</span><span class="sxs-lookup"><span data-stu-id="2280b-198">**Canonical name**: Microsoft.AutoPlay</span></span>
-   <span data-ttu-id="2280b-199">**GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}</span><span class="sxs-lookup"><span data-stu-id="2280b-199">**GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}</span></span>
-   <span data-ttu-id="2280b-200">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-200">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-201">**Имя модуля**: @% systemroot% \\ system32 \\autoplay.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-201">**Module name**: @%SystemRoot%\\System32\\autoplay.dll,-1</span></span>

### <a name="biometric-devices"></a><span data-ttu-id="2280b-202">Биометрические устройства</span><span class="sxs-lookup"><span data-stu-id="2280b-202">Biometric Devices</span></span>

-   <span data-ttu-id="2280b-203">**Каноническое имя**: Microsoft. биометрикдевицес</span><span class="sxs-lookup"><span data-stu-id="2280b-203">**Canonical name**: Microsoft.BiometricDevices</span></span>
-   <span data-ttu-id="2280b-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span><span class="sxs-lookup"><span data-stu-id="2280b-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span></span>
-   <span data-ttu-id="2280b-205">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-205">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-206">**Имя модуля**: @% systemroot% \\ system32 \\biocpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-206">**Module name**: @%SystemRoot%\\System32\\biocpl.dll,-1</span></span>

### <a name="bitlocker-drive-encryption"></a><span data-ttu-id="2280b-207">Шифрование диска BitLocker</span><span class="sxs-lookup"><span data-stu-id="2280b-207">BitLocker Drive Encryption</span></span>

-   <span data-ttu-id="2280b-208">**Каноническое имя**: Microsoft. битлоккердривинкриптион</span><span class="sxs-lookup"><span data-stu-id="2280b-208">**Canonical name**: Microsoft.BitLockerDriveEncryption</span></span>
-   <span data-ttu-id="2280b-209">**GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}</span><span class="sxs-lookup"><span data-stu-id="2280b-209">**GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}</span></span>
-   <span data-ttu-id="2280b-210">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-210">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-211">**Имя модуля**: @% systemroot% \\ system32 \\fvecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-211">**Module name**: @%SystemRoot%\\System32\\fvecpl.dll,-1</span></span>

### <a name="color-management"></a><span data-ttu-id="2280b-212">Управление цветом</span><span class="sxs-lookup"><span data-stu-id="2280b-212">Color Management</span></span>

-   <span data-ttu-id="2280b-213">**Каноническое имя**: Microsoft. колорманажемент</span><span class="sxs-lookup"><span data-stu-id="2280b-213">**Canonical name**: Microsoft.ColorManagement</span></span>
-   <span data-ttu-id="2280b-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span><span class="sxs-lookup"><span data-stu-id="2280b-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span></span>
-   <span data-ttu-id="2280b-215">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-215">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-216">**Имя модуля**: @% systemroot% \\ system32 \\colorcpl.exe,-6</span><span class="sxs-lookup"><span data-stu-id="2280b-216">**Module name**: @%systemroot%\\system32\\colorcpl.exe,-6</span></span>

### <a name="credential-manager"></a><span data-ttu-id="2280b-217">Диспетчер учетных данных</span><span class="sxs-lookup"><span data-stu-id="2280b-217">Credential Manager</span></span>

-   <span data-ttu-id="2280b-218">**Каноническое имя**: Microsoft. кредентиалманажер</span><span class="sxs-lookup"><span data-stu-id="2280b-218">**Canonical name**: Microsoft.CredentialManager</span></span>
-   <span data-ttu-id="2280b-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span><span class="sxs-lookup"><span data-stu-id="2280b-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span></span>
-   <span data-ttu-id="2280b-220">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-220">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-221">**Имя модуля**: @% systemroot% \\ system32 \\Vault.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-221">**Module name**: @%SystemRoot%\\system32\\Vault.dll,-1</span></span>
-   <span data-ttu-id="2280b-222">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-222">**Pages**</span></span>

    | <span data-ttu-id="2280b-223">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-223">Page Name</span></span>                   | <span data-ttu-id="2280b-224">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-224">Opens</span></span>               |
    |-----------------------------|---------------------|
    | <span data-ttu-id="2280b-225">? Селектедваулт = Кредманваулт</span><span class="sxs-lookup"><span data-stu-id="2280b-225">?SelectedVault=CredmanVault</span></span> | <span data-ttu-id="2280b-226">учетными данными Windows</span><span class="sxs-lookup"><span data-stu-id="2280b-226">Windows Credentials</span></span> |

    

     

### <a name="date-and-time"></a><span data-ttu-id="2280b-227">Дата и время</span><span class="sxs-lookup"><span data-stu-id="2280b-227">Date and Time</span></span>

-   <span data-ttu-id="2280b-228">**Каноническое имя**: Microsoft. датеандтиме</span><span class="sxs-lookup"><span data-stu-id="2280b-228">**Canonical name**: Microsoft.DateAndTime</span></span>
-   <span data-ttu-id="2280b-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span><span class="sxs-lookup"><span data-stu-id="2280b-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span></span>
-   <span data-ttu-id="2280b-230">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-230">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-231">**Имя модуля**: @% systemroot% \\ system32 \\timedate.cpl,-51</span><span class="sxs-lookup"><span data-stu-id="2280b-231">**Module name**: @%SystemRoot%\\System32\\timedate.cpl,-51</span></span>
-   <span data-ttu-id="2280b-232">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-232">**Pages**</span></span>

    | <span data-ttu-id="2280b-233">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-233">Page Name</span></span> | <span data-ttu-id="2280b-234">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-234">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="2280b-235">1</span><span class="sxs-lookup"><span data-stu-id="2280b-235">1</span></span>         | <span data-ttu-id="2280b-236">Дополнительные часы</span><span class="sxs-lookup"><span data-stu-id="2280b-236">Additional Clocks</span></span> |

    

     

### <a name="default-programs"></a><span data-ttu-id="2280b-237">Программы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2280b-237">Default Programs</span></span>

-   <span data-ttu-id="2280b-238">**Каноническое имя**: Microsoft. дефаултпрограмс</span><span class="sxs-lookup"><span data-stu-id="2280b-238">**Canonical name**: Microsoft.DefaultPrograms</span></span>
-   <span data-ttu-id="2280b-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span><span class="sxs-lookup"><span data-stu-id="2280b-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span></span>
-   <span data-ttu-id="2280b-240">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-240">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-241">**Имя модуля**: @% systemroot% \\ system32 \\sud.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-241">**Module name**: @%SystemRoot%\\System32\\sud.dll,-1</span></span>
-   <span data-ttu-id="2280b-242">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-242">**Pages**</span></span>

    | <span data-ttu-id="2280b-243">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-243">Page Name</span></span>          | <span data-ttu-id="2280b-244">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-244">Opens</span></span>                |
    |--------------------|----------------------|
    | <span data-ttu-id="2280b-245">пажедефаултпрограм</span><span class="sxs-lookup"><span data-stu-id="2280b-245">pageDefaultProgram</span></span> | <span data-ttu-id="2280b-246">Установка программ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2280b-246">Set Default Programs</span></span> |
    | <span data-ttu-id="2280b-247">пажефилеассок</span><span class="sxs-lookup"><span data-stu-id="2280b-247">pageFileAssoc</span></span>      | <span data-ttu-id="2280b-248">Задать связи</span><span class="sxs-lookup"><span data-stu-id="2280b-248">Set Associations</span></span>     |

    

     

### <a name="device-manager"></a><span data-ttu-id="2280b-249">Диспетчер устройств</span><span class="sxs-lookup"><span data-stu-id="2280b-249">Device Manager</span></span>

-   <span data-ttu-id="2280b-250">**Каноническое имя**: Microsoft. девицеманажер</span><span class="sxs-lookup"><span data-stu-id="2280b-250">**Canonical name**: Microsoft.DeviceManager</span></span>
-   <span data-ttu-id="2280b-251">**GUID**: {74246bfc-4c96-11D0-abef-0020af6b0b7a}</span><span class="sxs-lookup"><span data-stu-id="2280b-251">**GUID**: {74246bfc-4c96-11d0-abef-0020af6b0b7a}</span></span>
-   <span data-ttu-id="2280b-252">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-252">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-253">**Имя модуля**: @% systemroot% \\ system32 \\devmgr.dll,-4</span><span class="sxs-lookup"><span data-stu-id="2280b-253">**Module name**: @%SystemRoot%\\System32\\devmgr.dll,-4</span></span>

### <a name="devices-and-printers"></a><span data-ttu-id="2280b-254">"Устройства и принтеры"</span><span class="sxs-lookup"><span data-stu-id="2280b-254">Devices and Printers</span></span>

-   <span data-ttu-id="2280b-255">**Каноническое имя**: Microsoft. девицесандпринтерс</span><span class="sxs-lookup"><span data-stu-id="2280b-255">**Canonical name**: Microsoft.DevicesAndPrinters</span></span>
-   <span data-ttu-id="2280b-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span><span class="sxs-lookup"><span data-stu-id="2280b-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span></span>
-   <span data-ttu-id="2280b-257">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-257">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-258">**Имя модуля**: @% systemroot% \\ system32 \\DeviceCenter.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="2280b-258">**Module name**: @%systemroot%\\system32\\DeviceCenter.dll,-1000</span></span>

### <a name="display"></a><span data-ttu-id="2280b-259">Отображение</span><span class="sxs-lookup"><span data-stu-id="2280b-259">Display</span></span>

-   <span data-ttu-id="2280b-260">**Каноническое имя**: Microsoft. дисплей</span><span class="sxs-lookup"><span data-stu-id="2280b-260">**Canonical name**: Microsoft.Display</span></span>
-   <span data-ttu-id="2280b-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span><span class="sxs-lookup"><span data-stu-id="2280b-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span></span>
-   <span data-ttu-id="2280b-262">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-262">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-263">**Имя модуля**: @% systemroot% \\ system32 \\Display.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-263">**Module name**: @%SystemRoot%\\System32\\Display.dll,-1</span></span>
-   <span data-ttu-id="2280b-264">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-264">**Pages**</span></span>

    | <span data-ttu-id="2280b-265">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-265">Page Name</span></span> | <span data-ttu-id="2280b-266">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-266">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="2280b-267">Параметры</span><span class="sxs-lookup"><span data-stu-id="2280b-267">Settings</span></span>  | <span data-ttu-id="2280b-268">Разрешение экрана</span><span class="sxs-lookup"><span data-stu-id="2280b-268">Screen Resolution</span></span> |

    

     

### <a name="ease-of-access-center"></a><span data-ttu-id="2280b-269">Центр специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="2280b-269">Ease of Access Center</span></span>

-   <span data-ttu-id="2280b-270">**Каноническое имя**: Microsoft. еасеофакцессцентер</span><span class="sxs-lookup"><span data-stu-id="2280b-270">**Canonical name**: Microsoft.EaseOfAccessCenter</span></span>
-   <span data-ttu-id="2280b-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span><span class="sxs-lookup"><span data-stu-id="2280b-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span></span>
-   <span data-ttu-id="2280b-272">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-272">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-273">**Имя модуля**: @% systemroot% \\ system32 \\accessibilitycpl.dll,-10</span><span class="sxs-lookup"><span data-stu-id="2280b-273">**Module name**: @%SystemRoot%\\System32\\accessibilitycpl.dll,-10</span></span>
-   <span data-ttu-id="2280b-274">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-274">**Pages**</span></span>

    | <span data-ttu-id="2280b-275">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-275">Page Name</span></span>               | <span data-ttu-id="2280b-276">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-276">Opens</span></span>                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | <span data-ttu-id="2280b-277">пажееасиертокликк</span><span class="sxs-lookup"><span data-stu-id="2280b-277">pageEasierToClick</span></span>       | <span data-ttu-id="2280b-278">Настройка системы для удобной работы с мышью</span><span class="sxs-lookup"><span data-stu-id="2280b-278">Make the mouse easier to use</span></span>                                        |
    | <span data-ttu-id="2280b-279">пажееасиертоси</span><span class="sxs-lookup"><span data-stu-id="2280b-279">pageEasierToSee</span></span>         | <span data-ttu-id="2280b-280">Упрощение просмотра компьютера</span><span class="sxs-lookup"><span data-stu-id="2280b-280">Make the computer easier to see</span></span>                                     |
    | <span data-ttu-id="2280b-281">пажееасиервиссаундс</span><span class="sxs-lookup"><span data-stu-id="2280b-281">pageEasierWithSounds</span></span>    | <span data-ttu-id="2280b-282">Использование текстовых или визуальных вариантов для звуков</span><span class="sxs-lookup"><span data-stu-id="2280b-282">Use text or visual alternatives for sounds</span></span>                          |
    | <span data-ttu-id="2280b-283">пажефилтеркэйссеттингс</span><span class="sxs-lookup"><span data-stu-id="2280b-283">pageFilterKeysSettings</span></span>  | <span data-ttu-id="2280b-284">Настройка ключей фильтров</span><span class="sxs-lookup"><span data-stu-id="2280b-284">Set up Filter Keys</span></span>                                                  |
    | <span data-ttu-id="2280b-285">пажекэйбоардеасиертаусе</span><span class="sxs-lookup"><span data-stu-id="2280b-285">pageKeyboardEasierToUse</span></span> | <span data-ttu-id="2280b-286">Настройка системы для удобной работы с клавиатурой</span><span class="sxs-lookup"><span data-stu-id="2280b-286">Make the keyboard easier to use</span></span>                                     |
    | <span data-ttu-id="2280b-287">паженомаусеоркэйбоард</span><span class="sxs-lookup"><span data-stu-id="2280b-287">pageNoMouseOrKeyboard</span></span>   | <span data-ttu-id="2280b-288">Использование компьютера без мыши или клавиатуры</span><span class="sxs-lookup"><span data-stu-id="2280b-288">Use the computer without a mouse or keyboard</span></span>                        |
    | <span data-ttu-id="2280b-289">паженовисуал</span><span class="sxs-lookup"><span data-stu-id="2280b-289">pageNoVisual</span></span>            | <span data-ttu-id="2280b-290">Использование компьютера без экрана</span><span class="sxs-lookup"><span data-stu-id="2280b-290">Use the computer without a display</span></span>                                  |
    | <span data-ttu-id="2280b-291">пажекуестионскогнитиве</span><span class="sxs-lookup"><span data-stu-id="2280b-291">pageQuestionsCognitive</span></span>  | <span data-ttu-id="2280b-292">Получение рекомендаций по упрощению работы с компьютером</span><span class="sxs-lookup"><span data-stu-id="2280b-292">Get recommendations to make your computer easier to use (cognitive)</span></span> |
    | <span data-ttu-id="2280b-293">пажекуестионсэйесигхт</span><span class="sxs-lookup"><span data-stu-id="2280b-293">pageQuestionsEyesight</span></span>   | <span data-ttu-id="2280b-294">Получение рекомендаций по упрощению использования компьютера (эйесигхт)</span><span class="sxs-lookup"><span data-stu-id="2280b-294">Get recommendations to make your computer easier to use (eyesight)</span></span>  |

    

     

### <a name="family-safety"></a><span data-ttu-id="2280b-295">Семейная безопасность</span><span class="sxs-lookup"><span data-stu-id="2280b-295">Family Safety</span></span>

-   <span data-ttu-id="2280b-296">**Каноническое имя**: Microsoft. паренталконтролс</span><span class="sxs-lookup"><span data-stu-id="2280b-296">**Canonical name**: Microsoft.ParentalControls</span></span>
-   <span data-ttu-id="2280b-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span><span class="sxs-lookup"><span data-stu-id="2280b-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span></span>
-   <span data-ttu-id="2280b-298">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-298">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-299">**Имя модуля**: @% systemroot% \\ system32 \\wpccpl.dll,-100</span><span class="sxs-lookup"><span data-stu-id="2280b-299">**Module name**: @%SystemRoot%\\System32\\wpccpl.dll,-100</span></span>
-   <span data-ttu-id="2280b-300">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-300">**Pages**</span></span>

    | <span data-ttu-id="2280b-301">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-301">Page Name</span></span>   | <span data-ttu-id="2280b-302">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-302">Opens</span></span>                                  |
    |-------------|----------------------------------------|
    | <span data-ttu-id="2280b-303">пажеусерхуб</span><span class="sxs-lookup"><span data-stu-id="2280b-303">pageUserHub</span></span> | <span data-ttu-id="2280b-304">Выбор пользователя и настройка семейной безопасности</span><span class="sxs-lookup"><span data-stu-id="2280b-304">Choose a user and set up Family Safety</span></span> |

    

     

### <a name="file-history"></a><span data-ttu-id="2280b-305">История файлов</span><span class="sxs-lookup"><span data-stu-id="2280b-305">File History</span></span>

-   <span data-ttu-id="2280b-306">**Каноническое имя**: Microsoft. филехистори</span><span class="sxs-lookup"><span data-stu-id="2280b-306">**Canonical name**: Microsoft.FileHistory</span></span>
-   <span data-ttu-id="2280b-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span><span class="sxs-lookup"><span data-stu-id="2280b-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span></span>
-   <span data-ttu-id="2280b-308">**Поддерживаемая ОС**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-308">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-309">**Имя модуля**: @% systemroot% \\ system32 \\fhcpl.dll,-52</span><span class="sxs-lookup"><span data-stu-id="2280b-309">**Module name**: @%SystemRoot%\\System32\\fhcpl.dll,-52</span></span>
-   <span data-ttu-id="2280b-310">В журнал файлов входит более новая версия элемента резервного копирования и восстановления, но каноническое имя этого элемента не переносится в журнал файлов.</span><span class="sxs-lookup"><span data-stu-id="2280b-310">File History includes a newer version of the Backup and Restore item, but that older item's canonical name does not remap to File History.</span></span>

### <a name="folder-options"></a><span data-ttu-id="2280b-311">Свойства папки</span><span class="sxs-lookup"><span data-stu-id="2280b-311">Folder Options</span></span>

-   <span data-ttu-id="2280b-312">**Каноническое имя**: Microsoft. фолдероптионс</span><span class="sxs-lookup"><span data-stu-id="2280b-312">**Canonical name**: Microsoft.FolderOptions</span></span>
-   <span data-ttu-id="2280b-313">**GUID**: {6DFD7C5C-2451-11D3-A299-00C04F8EF6AF}</span><span class="sxs-lookup"><span data-stu-id="2280b-313">**GUID**: {6DFD7C5C-2451-11d3-A299-00C04F8EF6AF}</span></span>
-   <span data-ttu-id="2280b-314">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-314">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-315">**Имя модуля**: @% systemroot% \\ system32 \\shell32.dll,-22985</span><span class="sxs-lookup"><span data-stu-id="2280b-315">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22985</span></span>

### <a name="fonts"></a><span data-ttu-id="2280b-316">Шрифты</span><span class="sxs-lookup"><span data-stu-id="2280b-316">Fonts</span></span>

-   <span data-ttu-id="2280b-317">**Каноническое имя**: Microsoft. Fonts</span><span class="sxs-lookup"><span data-stu-id="2280b-317">**Canonical name**: Microsoft.Fonts</span></span>
-   <span data-ttu-id="2280b-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span><span class="sxs-lookup"><span data-stu-id="2280b-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span></span>
-   <span data-ttu-id="2280b-319">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-319">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-320">**Имя модуля**: @% systemroot% \\ system32 \\FontExt.dll,-8007</span><span class="sxs-lookup"><span data-stu-id="2280b-320">**Module name**: @%SystemRoot%\\System32\\FontExt.dll,-8007</span></span>

### <a name="homegroup"></a><span data-ttu-id="2280b-321">Домашняя группа</span><span class="sxs-lookup"><span data-stu-id="2280b-321">HomeGroup</span></span>

-   <span data-ttu-id="2280b-322">**Каноническое имя**: Microsoft. Домашняя группа</span><span class="sxs-lookup"><span data-stu-id="2280b-322">**Canonical name**: Microsoft.HomeGroup</span></span>
-   <span data-ttu-id="2280b-323">**GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span><span class="sxs-lookup"><span data-stu-id="2280b-323">**GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span></span>
-   <span data-ttu-id="2280b-324">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-324">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-325">**Имя модуля**: @% systemroot% \\ system32 \\hgcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-325">**Module name**: @%SystemRoot%\\System32\\hgcpl.dll,-1</span></span>

### <a name="indexing-options"></a><span data-ttu-id="2280b-326">Параметры индексирования</span><span class="sxs-lookup"><span data-stu-id="2280b-326">Indexing Options</span></span>

-   <span data-ttu-id="2280b-327">**Каноническое имя**: Microsoft. индексингоптионс</span><span class="sxs-lookup"><span data-stu-id="2280b-327">**Canonical name**: Microsoft.IndexingOptions</span></span>
-   <span data-ttu-id="2280b-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span><span class="sxs-lookup"><span data-stu-id="2280b-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span></span>
-   <span data-ttu-id="2280b-329">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-329">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-330">**Имя модуля**: @% systemroot% \\ system32 \\srchadmin.dll,-601</span><span class="sxs-lookup"><span data-stu-id="2280b-330">**Module name**: @%SystemRoot%\\System32\\srchadmin.dll,-601</span></span>

### <a name="infrared"></a><span data-ttu-id="2280b-331">Инфракрасная связь</span><span class="sxs-lookup"><span data-stu-id="2280b-331">Infrared</span></span>

-   <span data-ttu-id="2280b-332">**Каноническое имя**: Microsoft. Infrared</span><span class="sxs-lookup"><span data-stu-id="2280b-332">**Canonical name**: Microsoft.Infrared</span></span>
-   <span data-ttu-id="2280b-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="2280b-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span>
-   <span data-ttu-id="2280b-334">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-334">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-335">**Имя модуля**: @% systemroot% \\ system32 \\irprops.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-335">**Module name**: @%SystemRoot%\\System32\\irprops.cpl,-1</span></span>

### <a name="internet-options"></a><span data-ttu-id="2280b-336">Свойства браузера</span><span class="sxs-lookup"><span data-stu-id="2280b-336">Internet Options</span></span>

-   <span data-ttu-id="2280b-337">**Каноническое имя**: Microsoft. интернетоптионс</span><span class="sxs-lookup"><span data-stu-id="2280b-337">**Canonical name**: Microsoft.InternetOptions</span></span>
-   <span data-ttu-id="2280b-338">**GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}</span><span class="sxs-lookup"><span data-stu-id="2280b-338">**GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}</span></span>
-   <span data-ttu-id="2280b-339">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-339">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-340">**Имя модуля**: @C: \\ \\inetcpl.cpl Windows System32 \\ ,-4312</span><span class="sxs-lookup"><span data-stu-id="2280b-340">**Module name**: @C:\\Windows\\System32\\inetcpl.cpl,-4312</span></span>
-   <span data-ttu-id="2280b-341">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-341">**Pages**</span></span>

    | <span data-ttu-id="2280b-342">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-342">Page Name</span></span> | <span data-ttu-id="2280b-343">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-343">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="2280b-344">1</span><span class="sxs-lookup"><span data-stu-id="2280b-344">1</span></span>         | <span data-ttu-id="2280b-345">Безопасность</span><span class="sxs-lookup"><span data-stu-id="2280b-345">Security</span></span>    |
    | <span data-ttu-id="2280b-346">2</span><span class="sxs-lookup"><span data-stu-id="2280b-346">2</span></span>         | <span data-ttu-id="2280b-347">Конфиденциальность</span><span class="sxs-lookup"><span data-stu-id="2280b-347">Privacy</span></span>     |
    | <span data-ttu-id="2280b-348">3</span><span class="sxs-lookup"><span data-stu-id="2280b-348">3</span></span>         | <span data-ttu-id="2280b-349">Содержимое</span><span class="sxs-lookup"><span data-stu-id="2280b-349">Content</span></span>     |
    | <span data-ttu-id="2280b-350">4</span><span class="sxs-lookup"><span data-stu-id="2280b-350">4</span></span>         | <span data-ttu-id="2280b-351">Соединения</span><span class="sxs-lookup"><span data-stu-id="2280b-351">Connections</span></span> |
    | <span data-ttu-id="2280b-352">5</span><span class="sxs-lookup"><span data-stu-id="2280b-352">5</span></span>         | <span data-ttu-id="2280b-353">Programs</span><span class="sxs-lookup"><span data-stu-id="2280b-353">Programs</span></span>    |
    | <span data-ttu-id="2280b-354">6</span><span class="sxs-lookup"><span data-stu-id="2280b-354">6</span></span>         | <span data-ttu-id="2280b-355">Дополнительно</span><span class="sxs-lookup"><span data-stu-id="2280b-355">Advanced</span></span>    |

    

     

### <a name="iscsi-initiator"></a><span data-ttu-id="2280b-356">Инициатор iSCSI</span><span class="sxs-lookup"><span data-stu-id="2280b-356">iSCSI Initiator</span></span>

-   <span data-ttu-id="2280b-357">**Каноническое имя**: Microsoft. исксиинитиатор</span><span class="sxs-lookup"><span data-stu-id="2280b-357">**Canonical name**: Microsoft.iSCSIInitiator</span></span>
-   <span data-ttu-id="2280b-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span><span class="sxs-lookup"><span data-stu-id="2280b-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span></span>
-   <span data-ttu-id="2280b-359">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-359">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-360">**Имя модуля**: @% systemroot% \\ system32 \\iscsicpl.dll,-5001</span><span class="sxs-lookup"><span data-stu-id="2280b-360">**Module name**: @%SystemRoot%\\System32\\iscsicpl.dll,-5001</span></span>

### <a name="isns-server"></a><span data-ttu-id="2280b-361">iSNS-сервер</span><span class="sxs-lookup"><span data-stu-id="2280b-361">iSNS Server</span></span>

-   <span data-ttu-id="2280b-362">**Каноническое имя**: Microsoft. иснссервер</span><span class="sxs-lookup"><span data-stu-id="2280b-362">**Canonical name**: Microsoft.iSNSServer</span></span>
-   <span data-ttu-id="2280b-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span><span class="sxs-lookup"><span data-stu-id="2280b-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span></span>
-   <span data-ttu-id="2280b-364">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-364">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-365">**Имя модуля**: @% systemroot% \\ system32 \\isnssrv.dll,-5005</span><span class="sxs-lookup"><span data-stu-id="2280b-365">**Module name**: @%SystemRoot%\\System32\\isnssrv.dll,-5005</span></span>
-   <span data-ttu-id="2280b-366">Этот элемент панели управления будет отображаться только в серверных версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="2280b-366">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="keyboard"></a><span data-ttu-id="2280b-367">Клавиатура</span><span class="sxs-lookup"><span data-stu-id="2280b-367">Keyboard</span></span>

-   <span data-ttu-id="2280b-368">**Каноническое имя**: Microsoft. Keyboard</span><span class="sxs-lookup"><span data-stu-id="2280b-368">**Canonical name**: Microsoft.Keyboard</span></span>
-   <span data-ttu-id="2280b-369">**GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span><span class="sxs-lookup"><span data-stu-id="2280b-369">**GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span></span>
-   <span data-ttu-id="2280b-370">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-370">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-371">**Имя модуля**: @% systemroot% \\ system32 \\main.cpl,-102</span><span class="sxs-lookup"><span data-stu-id="2280b-371">**Module name**: @%SystemRoot%\\System32\\main.cpl,-102</span></span>

### <a name="location-settings"></a><span data-ttu-id="2280b-372">Параметры расположения</span><span class="sxs-lookup"><span data-stu-id="2280b-372">Location Settings</span></span>

-   <span data-ttu-id="2280b-373">**Каноническое имя**: Microsoft. локатионсеттингс</span><span class="sxs-lookup"><span data-stu-id="2280b-373">**Canonical name**: Microsoft.LocationSettings</span></span>
-   <span data-ttu-id="2280b-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="2280b-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span></span>
-   <span data-ttu-id="2280b-375">**Поддерживаемая ОС**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-375">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-376">**Имя модуля**: @% systemroot% \\ system32 \\SensorsCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-376">**Module name**: @%SystemRoot%\\System32\\SensorsCpl.dll,-1</span></span>

### <a name="mouse"></a><span data-ttu-id="2280b-377">Мышь</span><span class="sxs-lookup"><span data-stu-id="2280b-377">Mouse</span></span>

-   <span data-ttu-id="2280b-378">**Каноническое имя**: Microsoft. Mouse</span><span class="sxs-lookup"><span data-stu-id="2280b-378">**Canonical name**: Microsoft.Mouse</span></span>
-   <span data-ttu-id="2280b-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span><span class="sxs-lookup"><span data-stu-id="2280b-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span></span>
-   <span data-ttu-id="2280b-380">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-380">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-381">**Имя модуля**: @% systemroot% \\ system32 \\main.cpl,-100</span><span class="sxs-lookup"><span data-stu-id="2280b-381">**Module name**: @%SystemRoot%\\System32\\main.cpl,-100</span></span>
-   <span data-ttu-id="2280b-382">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-382">**Pages**</span></span>

    | <span data-ttu-id="2280b-383">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-383">Page Name</span></span> | <span data-ttu-id="2280b-384">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-384">Opens</span></span>           |
    |-----------|-----------------|
    | <span data-ttu-id="2280b-385">1</span><span class="sxs-lookup"><span data-stu-id="2280b-385">1</span></span>         | <span data-ttu-id="2280b-386">Указатели</span><span class="sxs-lookup"><span data-stu-id="2280b-386">Pointers</span></span>        |
    | <span data-ttu-id="2280b-387">2</span><span class="sxs-lookup"><span data-stu-id="2280b-387">2</span></span>         | <span data-ttu-id="2280b-388">Параметры указателя</span><span class="sxs-lookup"><span data-stu-id="2280b-388">Pointer Options</span></span> |
    | <span data-ttu-id="2280b-389">3</span><span class="sxs-lookup"><span data-stu-id="2280b-389">3</span></span>         | <span data-ttu-id="2280b-390">Wheel</span><span class="sxs-lookup"><span data-stu-id="2280b-390">Wheel</span></span>           |
    | <span data-ttu-id="2280b-391">4</span><span class="sxs-lookup"><span data-stu-id="2280b-391">4</span></span>         | <span data-ttu-id="2280b-392">Оборудование</span><span class="sxs-lookup"><span data-stu-id="2280b-392">Hardware</span></span>        |

    

     

### <a name="mpioconfiguration"></a><span data-ttu-id="2280b-393">мпиоконфигуратион</span><span class="sxs-lookup"><span data-stu-id="2280b-393">MPIOConfiguration</span></span>

-   <span data-ttu-id="2280b-394">**Каноническое имя**: Microsoft. мпиоконфигуратион</span><span class="sxs-lookup"><span data-stu-id="2280b-394">**Canonical name**: Microsoft.MPIOConfiguration</span></span>
-   <span data-ttu-id="2280b-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span><span class="sxs-lookup"><span data-stu-id="2280b-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span></span>
-   <span data-ttu-id="2280b-396">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-396">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-397">**Имя модуля**: @% systemroot% \\ system32 \\mpiocpl.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="2280b-397">**Module name**: @%SystemRoot%\\System32\\mpiocpl.dll,-1000</span></span>
-   <span data-ttu-id="2280b-398">Этот элемент панели управления будет отображаться только в серверных версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="2280b-398">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="network-and-sharing-center"></a><span data-ttu-id="2280b-399">Центр управления сетями и общим доступом</span><span class="sxs-lookup"><span data-stu-id="2280b-399">Network and Sharing Center</span></span>

-   <span data-ttu-id="2280b-400">**Каноническое имя**: Microsoft. нетворкандшарингцентер</span><span class="sxs-lookup"><span data-stu-id="2280b-400">**Canonical name**: Microsoft.NetworkAndSharingCenter</span></span>
-   <span data-ttu-id="2280b-401">**GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}</span><span class="sxs-lookup"><span data-stu-id="2280b-401">**GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}</span></span>
-   <span data-ttu-id="2280b-402">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-402">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-403">**Имя модуля**: @% systemroot% \\ system32 \\netcenter.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-403">**Module name**: @%SystemRoot%\\System32\\netcenter.dll,-1</span></span>
-   <span data-ttu-id="2280b-404">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-404">**Pages**</span></span>

    | <span data-ttu-id="2280b-405">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-405">Page Name</span></span>  | <span data-ttu-id="2280b-406">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-406">Opens</span></span>                     |
    |------------|---------------------------|
    | <span data-ttu-id="2280b-407">Дополнительно</span><span class="sxs-lookup"><span data-stu-id="2280b-407">Advanced</span></span>   | <span data-ttu-id="2280b-408">Дополнительные параметры общего доступа</span><span class="sxs-lookup"><span data-stu-id="2280b-408">Advanced sharing settings</span></span> |
    | <span data-ttu-id="2280b-409">шаремедиа</span><span class="sxs-lookup"><span data-stu-id="2280b-409">ShareMedia</span></span> | <span data-ttu-id="2280b-410">Параметры потоковой передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2280b-410">Media streaming options</span></span>   |

    

     

### <a name="notification-area-icons"></a><span data-ttu-id="2280b-411">Значки области уведомлений</span><span class="sxs-lookup"><span data-stu-id="2280b-411">Notification Area Icons</span></span>

-   <span data-ttu-id="2280b-412">**Каноническое имя**: Microsoft. нотификатионареаиконс</span><span class="sxs-lookup"><span data-stu-id="2280b-412">**Canonical name**: Microsoft.NotificationAreaIcons</span></span>
-   <span data-ttu-id="2280b-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span><span class="sxs-lookup"><span data-stu-id="2280b-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span></span>
-   <span data-ttu-id="2280b-414">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-414">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-415">**Имя модуля**: @% systemroot% \\ system32 \\taskbarcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-415">**Module name**: @%SystemRoot%\\System32\\taskbarcpl.dll,-1</span></span>

### <a name="pen-and-touch"></a><span data-ttu-id="2280b-416">Перо и сенсорный ввод</span><span class="sxs-lookup"><span data-stu-id="2280b-416">Pen and Touch</span></span>

-   <span data-ttu-id="2280b-417">**Каноническое имя**: Microsoft. пенандтауч</span><span class="sxs-lookup"><span data-stu-id="2280b-417">**Canonical name**: Microsoft.PenAndTouch</span></span>
-   <span data-ttu-id="2280b-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="2280b-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span>
-   <span data-ttu-id="2280b-419">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-419">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-420">**Имя модуля**: @% systemroot% \\ system32 \\tabletpc.cpl,-10103</span><span class="sxs-lookup"><span data-stu-id="2280b-420">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10103</span></span>
-   <span data-ttu-id="2280b-421">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-421">**Pages**</span></span>

    | <span data-ttu-id="2280b-422">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-422">Page Name</span></span> | <span data-ttu-id="2280b-423">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-423">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="2280b-424">1</span><span class="sxs-lookup"><span data-stu-id="2280b-424">1</span></span>         | <span data-ttu-id="2280b-425">Жесты</span><span class="sxs-lookup"><span data-stu-id="2280b-425">Flicks</span></span>      |
    | <span data-ttu-id="2280b-426">2</span><span class="sxs-lookup"><span data-stu-id="2280b-426">2</span></span>         | <span data-ttu-id="2280b-427">Handwriting</span><span class="sxs-lookup"><span data-stu-id="2280b-427">Handwriting</span></span> |

    

     

### <a name="personalization"></a><span data-ttu-id="2280b-428">Personalization</span><span class="sxs-lookup"><span data-stu-id="2280b-428">Personalization</span></span>

-   <span data-ttu-id="2280b-429">**Каноническое имя**: Microsoft. Персонализация</span><span class="sxs-lookup"><span data-stu-id="2280b-429">**Canonical name**: Microsoft.Personalization</span></span>
-   <span data-ttu-id="2280b-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span><span class="sxs-lookup"><span data-stu-id="2280b-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span></span>
-   <span data-ttu-id="2280b-431">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-431">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-432">**Имя модуля**: @% systemroot% \\ system32 \\themecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-432">**Module name**: @%SystemRoot%\\System32\\themecpl.dll,-1</span></span>
-   <span data-ttu-id="2280b-433">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-433">**Pages**</span></span>

    | <span data-ttu-id="2280b-434">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-434">Page Name</span></span>        | <span data-ttu-id="2280b-435">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-435">Opens</span></span>                |
    |------------------|----------------------|
    | <span data-ttu-id="2280b-436">пажеколоризатион</span><span class="sxs-lookup"><span data-stu-id="2280b-436">pageColorization</span></span> | <span data-ttu-id="2280b-437">Цвет и внешний вид</span><span class="sxs-lookup"><span data-stu-id="2280b-437">Color and Appearance</span></span> |
    | <span data-ttu-id="2280b-438">пажеваллпапер</span><span class="sxs-lookup"><span data-stu-id="2280b-438">pageWallpaper</span></span>    | <span data-ttu-id="2280b-439">Фон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="2280b-439">Desktop Background</span></span>   |

    

     

### <a name="phone-and-modem"></a><span data-ttu-id="2280b-440">Телефон и модем</span><span class="sxs-lookup"><span data-stu-id="2280b-440">Phone and Modem</span></span>

-   <span data-ttu-id="2280b-441">**Каноническое имя**: Microsoft. фонеандмодем</span><span class="sxs-lookup"><span data-stu-id="2280b-441">**Canonical name**: Microsoft.PhoneAndModem</span></span>
-   <span data-ttu-id="2280b-442">**GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="2280b-442">**GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}</span></span>
-   <span data-ttu-id="2280b-443">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-443">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-444">**Имя модуля**: @% systemroot% \\ system32 \\telephon.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-444">**Module name**: @%SystemRoot%\\System32\\telephon.cpl,-1</span></span>
-   <span data-ttu-id="2280b-445">Окно, в котором запускается это значение, называется "сведения о расположении" в версиях Windows, предшествовавших Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2280b-445">The window that this value launches is titled "Location Information" in versions of Windows prior to Windows 8.</span></span> <span data-ttu-id="2280b-446">Пользовательский интерфейс элемента значительно изменен в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2280b-446">The item's UI is considerably changed as of Windows 8.</span></span>

### <a name="power-options"></a><span data-ttu-id="2280b-447">Параметры электропитания</span><span class="sxs-lookup"><span data-stu-id="2280b-447">Power Options</span></span>

-   <span data-ttu-id="2280b-448">**Каноническое имя**: Microsoft. повероптионс</span><span class="sxs-lookup"><span data-stu-id="2280b-448">**Canonical name**: Microsoft.PowerOptions</span></span>
-   <span data-ttu-id="2280b-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span><span class="sxs-lookup"><span data-stu-id="2280b-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span></span>
-   <span data-ttu-id="2280b-450">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-450">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-451">**Имя модуля**: @% systemroot% \\ system32 \\powercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-451">**Module name**: @%SystemRoot%\\System32\\powercpl.dll,-1</span></span>
-   <span data-ttu-id="2280b-452">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-452">**Pages**</span></span>

    | <span data-ttu-id="2280b-453">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-453">Page Name</span></span>          | <span data-ttu-id="2280b-454">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-454">Opens</span></span>              |
    |--------------------|--------------------|
    | <span data-ttu-id="2280b-455">пажеглобалсеттингс</span><span class="sxs-lookup"><span data-stu-id="2280b-455">pageGlobalSettings</span></span> | <span data-ttu-id="2280b-456">Системные настройки</span><span class="sxs-lookup"><span data-stu-id="2280b-456">System Settings</span></span>    |
    | <span data-ttu-id="2280b-457">пажеплансеттингс</span><span class="sxs-lookup"><span data-stu-id="2280b-457">pagePlanSettings</span></span>   | <span data-ttu-id="2280b-458">Изменение параметров плана</span><span class="sxs-lookup"><span data-stu-id="2280b-458">Edit Plan Settings</span></span> |

    

     

### <a name="programs-and-features"></a><span data-ttu-id="2280b-459">"Программы и компоненты",</span><span class="sxs-lookup"><span data-stu-id="2280b-459">Programs and Features</span></span>

-   <span data-ttu-id="2280b-460">**Каноническое имя**: Microsoft. програмсандфеатурес</span><span class="sxs-lookup"><span data-stu-id="2280b-460">**Canonical name**: Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="2280b-461">**GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span><span class="sxs-lookup"><span data-stu-id="2280b-461">**GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span></span>
-   <span data-ttu-id="2280b-462">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-462">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-463">**Имя модуля**: @% systemroot% \\ system32 \\appwiz.cpl,-159</span><span class="sxs-lookup"><span data-stu-id="2280b-463">**Module name**: @%systemroot%\\system32\\appwiz.cpl,-159</span></span>
-   <span data-ttu-id="2280b-464">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-464">**Pages**</span></span>

    | <span data-ttu-id="2280b-465">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-465">Page Name</span></span>                                | <span data-ttu-id="2280b-466">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-466">Opens</span></span>             |
    |------------------------------------------|-------------------|
    | <span data-ttu-id="2280b-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span><span class="sxs-lookup"><span data-stu-id="2280b-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span></span> | <span data-ttu-id="2280b-468">Установленные обновления</span><span class="sxs-lookup"><span data-stu-id="2280b-468">Installed Updates</span></span> |

    

     

### <a name="recovery"></a><span data-ttu-id="2280b-469">Восстановление</span><span class="sxs-lookup"><span data-stu-id="2280b-469">Recovery</span></span>

-   <span data-ttu-id="2280b-470">**Каноническое имя**: Microsoft. Recovery</span><span class="sxs-lookup"><span data-stu-id="2280b-470">**Canonical name**: Microsoft.Recovery</span></span>
-   <span data-ttu-id="2280b-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span><span class="sxs-lookup"><span data-stu-id="2280b-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span></span>
-   <span data-ttu-id="2280b-472">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-472">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-473">**Имя модуля**: @% systemroot% \\ system32 \\recovery.dll,-101</span><span class="sxs-lookup"><span data-stu-id="2280b-473">**Module name**: @%SystemRoot%\\System32\\recovery.dll,-101</span></span>

### <a name="region"></a><span data-ttu-id="2280b-474">Region</span><span class="sxs-lookup"><span data-stu-id="2280b-474">Region</span></span>

-   <span data-ttu-id="2280b-475">**Каноническое имя**: Microsoft. регионандлангуаже</span><span class="sxs-lookup"><span data-stu-id="2280b-475">**Canonical name**: Microsoft.RegionAndLanguage</span></span>
-   <span data-ttu-id="2280b-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="2280b-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span>
-   <span data-ttu-id="2280b-477">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-477">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-478">**Имя модуля**: @% systemroot% \\ system32 \\intl.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-478">**Module name**: @%SystemRoot%\\System32\\intl.cpl,-1</span></span>
-   <span data-ttu-id="2280b-479">Язык и региональные элементы, найденные в Windows 7, были разделены на Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2280b-479">The Region and Language item found in Windows 7 was split as of Windows 8.</span></span> <span data-ttu-id="2280b-480">Теперь Microsoft. Регионандлангуаже запускает элемент Region.</span><span class="sxs-lookup"><span data-stu-id="2280b-480">Microsoft.RegionAndLanguage now launches the Region item.</span></span> <span data-ttu-id="2280b-481">Чтобы запустить языковой элемент, используйте [Microsoft. Language](#location-settings).</span><span class="sxs-lookup"><span data-stu-id="2280b-481">To launch the Language item, use [Microsoft.Language](#location-settings).</span></span>
-   <span data-ttu-id="2280b-482">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-482">**Pages**</span></span>

    | <span data-ttu-id="2280b-483">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-483">Page Name</span></span> | <span data-ttu-id="2280b-484">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-484">Opens</span></span>          |
    |-----------|----------------|
    | <span data-ttu-id="2280b-485">1</span><span class="sxs-lookup"><span data-stu-id="2280b-485">1</span></span>         | <span data-ttu-id="2280b-486">Расположение</span><span class="sxs-lookup"><span data-stu-id="2280b-486">Location</span></span>       |
    | <span data-ttu-id="2280b-487">2</span><span class="sxs-lookup"><span data-stu-id="2280b-487">2</span></span>         | <span data-ttu-id="2280b-488">Административный</span><span class="sxs-lookup"><span data-stu-id="2280b-488">Administrative</span></span> |

    

     

### <a name="remoteapp-and-desktop-connections"></a><span data-ttu-id="2280b-489">Подключения к рабочим столам и RemoteApp</span><span class="sxs-lookup"><span data-stu-id="2280b-489">RemoteApp and Desktop Connections</span></span>

-   <span data-ttu-id="2280b-490">**Каноническое имя**: Microsoft. ремотеаппанддесктопконнектионс</span><span class="sxs-lookup"><span data-stu-id="2280b-490">**Canonical name**: Microsoft.RemoteAppAndDesktopConnections</span></span>
-   <span data-ttu-id="2280b-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span><span class="sxs-lookup"><span data-stu-id="2280b-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span></span>
-   <span data-ttu-id="2280b-492">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-492">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-493">**Имя модуля**: @% systemroot% \\ system32 \\tsworkspace.dll,-15300</span><span class="sxs-lookup"><span data-stu-id="2280b-493">**Module name**: @%SystemRoot%\\System32\\tsworkspace.dll,-15300</span></span>

### <a name="sound"></a><span data-ttu-id="2280b-494">Звук</span><span class="sxs-lookup"><span data-stu-id="2280b-494">Sound</span></span>

-   <span data-ttu-id="2280b-495">**Каноническое имя**: Microsoft. Sound</span><span class="sxs-lookup"><span data-stu-id="2280b-495">**Canonical name**: Microsoft.Sound</span></span>
-   <span data-ttu-id="2280b-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="2280b-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span>
-   <span data-ttu-id="2280b-497">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-497">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-498">**Имя модуля**: @% systemroot% \\ system32 \\mmsys.cpl,-300</span><span class="sxs-lookup"><span data-stu-id="2280b-498">**Module name**: @%SystemRoot%\\System32\\mmsys.cpl,-300</span></span>

### <a name="speech-recognition"></a><span data-ttu-id="2280b-499">Распознавание речи</span><span class="sxs-lookup"><span data-stu-id="2280b-499">Speech Recognition</span></span>

-   <span data-ttu-id="2280b-500">**Каноническое имя**: Microsoft. спичрекогнитион</span><span class="sxs-lookup"><span data-stu-id="2280b-500">**Canonical name**: Microsoft.SpeechRecognition</span></span>
-   <span data-ttu-id="2280b-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="2280b-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span></span>
-   <span data-ttu-id="2280b-502">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-502">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-503">**Имя модуля**: @% systemroot% \\ System32 \\ Speech \\ спичукс \\speechuxcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-503">**Module name**: @%SystemRoot%\\System32\\Speech\\SpeechUX\\speechuxcpl.dll,-1</span></span>

### <a name="storage-spaces"></a><span data-ttu-id="2280b-504">Дисковые пространства</span><span class="sxs-lookup"><span data-stu-id="2280b-504">Storage Spaces</span></span>

-   <span data-ttu-id="2280b-505">**Каноническое имя**: Microsoft. сторажеспацес</span><span class="sxs-lookup"><span data-stu-id="2280b-505">**Canonical name**: Microsoft.StorageSpaces</span></span>
-   <span data-ttu-id="2280b-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span><span class="sxs-lookup"><span data-stu-id="2280b-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span></span>
-   <span data-ttu-id="2280b-507">**Поддерживаемая ОС**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-507">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-508">**Имя модуля**: @C: \\ \\SpaceControl.dll Windows System32 \\ ,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-508">**Module name**: @C:\\Windows\\System32\\SpaceControl.dll,-1</span></span>

### <a name="sync-center"></a><span data-ttu-id="2280b-509">Центр синхронизации</span><span class="sxs-lookup"><span data-stu-id="2280b-509">Sync Center</span></span>

-   <span data-ttu-id="2280b-510">**Каноническое имя**: Microsoft. синкцентер</span><span class="sxs-lookup"><span data-stu-id="2280b-510">**Canonical name**: Microsoft.SyncCenter</span></span>
-   <span data-ttu-id="2280b-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span><span class="sxs-lookup"><span data-stu-id="2280b-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span></span>
-   <span data-ttu-id="2280b-512">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-512">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-513">**Имя модуля**: @% systemroot% \\ system32 \\SyncCenter.dll,-3000</span><span class="sxs-lookup"><span data-stu-id="2280b-513">**Module name**: @%SystemRoot%\\System32\\SyncCenter.dll,-3000</span></span>

### <a name="system"></a><span data-ttu-id="2280b-514">Система</span><span class="sxs-lookup"><span data-stu-id="2280b-514">System</span></span>

-   <span data-ttu-id="2280b-515">**Каноническое имя**: Microsoft.SysTEM</span><span class="sxs-lookup"><span data-stu-id="2280b-515">**Canonical name**: Microsoft.System</span></span>
-   <span data-ttu-id="2280b-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span><span class="sxs-lookup"><span data-stu-id="2280b-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span></span>
-   <span data-ttu-id="2280b-517">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-517">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-518">**Имя модуля**: @% systemroot% \\ system32 \\systemcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-518">**Module name**: @%SystemRoot%\\System32\\systemcpl.dll,-1</span></span>

### <a name="tablet-pc-settings"></a><span data-ttu-id="2280b-519">Параметры планшетного ПК</span><span class="sxs-lookup"><span data-stu-id="2280b-519">Tablet PC Settings</span></span>

-   <span data-ttu-id="2280b-520">**Каноническое имя**: Microsoft. таблетпксеттингс</span><span class="sxs-lookup"><span data-stu-id="2280b-520">**Canonical name**: Microsoft.TabletPCSettings</span></span>
-   <span data-ttu-id="2280b-521">**GUID**: {80F3F1D5-FECA-45F3-BC32-752C152E456E}</span><span class="sxs-lookup"><span data-stu-id="2280b-521">**GUID**: {80F3F1D5-FECA-45F3-BC32-752C152E456E}</span></span>
-   <span data-ttu-id="2280b-522">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-522">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-523">**Имя модуля**: @% systemroot% \\ system32 \\tabletpc.cpl,-10100</span><span class="sxs-lookup"><span data-stu-id="2280b-523">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10100</span></span>

### <a name="taskbar-and-navigation"></a><span data-ttu-id="2280b-524">Панель задач и Навигация</span><span class="sxs-lookup"><span data-stu-id="2280b-524">Taskbar and Navigation</span></span>

-   <span data-ttu-id="2280b-525">**Каноническое имя**: Microsoft. панель задач</span><span class="sxs-lookup"><span data-stu-id="2280b-525">**Canonical name**: Microsoft.Taskbar</span></span>
-   <span data-ttu-id="2280b-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="2280b-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span>
-   <span data-ttu-id="2280b-527">**Поддерживаемая ОС**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-527">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-528">**Имя модуля**: @% systemroot% \\ system32 \\shell32.dll,-32517</span><span class="sxs-lookup"><span data-stu-id="2280b-528">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-32517</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="2280b-529">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="2280b-529">Troubleshooting</span></span>

-   <span data-ttu-id="2280b-530">**Каноническое имя**: Microsoft. Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="2280b-530">**Canonical name**: Microsoft.Troubleshooting</span></span>
-   <span data-ttu-id="2280b-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span><span class="sxs-lookup"><span data-stu-id="2280b-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span></span>
-   <span data-ttu-id="2280b-532">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-532">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-533">**Имя модуля**: @% systemroot% \\ system32 \\DiagCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-533">**Module name**: @%SystemRoot%\\System32\\DiagCpl.dll,-1</span></span>
-   <span data-ttu-id="2280b-534">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-534">**Pages**</span></span>

    | <span data-ttu-id="2280b-535">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-535">Page Name</span></span>   | <span data-ttu-id="2280b-536">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-536">Opens</span></span>   |
    |-------------|---------|
    | <span data-ttu-id="2280b-537">хисторипаже</span><span class="sxs-lookup"><span data-stu-id="2280b-537">HistoryPage</span></span> | <span data-ttu-id="2280b-538">Журнал</span><span class="sxs-lookup"><span data-stu-id="2280b-538">History</span></span> |

    

     

### <a name="tsappinstall"></a><span data-ttu-id="2280b-539">тсаппинсталл</span><span class="sxs-lookup"><span data-stu-id="2280b-539">TSAppInstall</span></span>

-   <span data-ttu-id="2280b-540">**Каноническое имя**: Microsoft. тсаппинсталл</span><span class="sxs-lookup"><span data-stu-id="2280b-540">**Canonical name**: Microsoft.TSAppInstall</span></span>
-   <span data-ttu-id="2280b-541">**GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span><span class="sxs-lookup"><span data-stu-id="2280b-541">**GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span></span>
-   <span data-ttu-id="2280b-542">**Поддерживаемая ОС**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-542">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-543">**Имя модуля**: @% systemroot% \\ system32 \\tsappinstall.exe,-2001</span><span class="sxs-lookup"><span data-stu-id="2280b-543">**Module name**: @%systemroot%\\system32\\tsappinstall.exe,-2001</span></span>

### <a name="user-accounts"></a><span data-ttu-id="2280b-544">Учетные записи пользователей</span><span class="sxs-lookup"><span data-stu-id="2280b-544">User Accounts</span></span>

-   <span data-ttu-id="2280b-545">**Каноническое имя**: Microsoft. UserAccounts</span><span class="sxs-lookup"><span data-stu-id="2280b-545">**Canonical name**: Microsoft.UserAccounts</span></span>
-   <span data-ttu-id="2280b-546">**GUID**: {60632754-c523-4b62-b45c-4172da012619}</span><span class="sxs-lookup"><span data-stu-id="2280b-546">**GUID**: {60632754-c523-4b62-b45c-4172da012619}</span></span>
-   <span data-ttu-id="2280b-547">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-547">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-548">**Имя модуля**: @% systemroot% \\ system32 \\usercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-548">**Module name**: @%SystemRoot%\\System32\\usercpl.dll,-1</span></span>

### <a name="windows-anytime-upgrade"></a><span data-ttu-id="2280b-549">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="2280b-549">Windows Anytime Upgrade</span></span>

-   <span data-ttu-id="2280b-550">**Каноническое имя**: Microsoft. виндовсанитимеупграде</span><span class="sxs-lookup"><span data-stu-id="2280b-550">**Canonical name**: Microsoft.WindowsAnytimeUpgrade</span></span>
-   <span data-ttu-id="2280b-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span><span class="sxs-lookup"><span data-stu-id="2280b-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span></span>
-   <span data-ttu-id="2280b-552">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-552">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-553">**Имя модуля**: @ $ (ресаурцестринг. \_ \_Путь sys Mod \_ ),-1</span><span class="sxs-lookup"><span data-stu-id="2280b-553">**Module name**: @$(resourceString.\_SYS\_MOD\_PATH),-1</span></span>

### <a name="windows-defender"></a><span data-ttu-id="2280b-554">Защитник Windows</span><span class="sxs-lookup"><span data-stu-id="2280b-554">Windows Defender</span></span>

-   <span data-ttu-id="2280b-555">**Каноническое имя**: Microsoft. виндовсдефендер</span><span class="sxs-lookup"><span data-stu-id="2280b-555">**Canonical name**: Microsoft.WindowsDefender</span></span>
-   <span data-ttu-id="2280b-556">**GUID**: {D8559EB9-20C0-410E-Beda-7ED416AECC2A}</span><span class="sxs-lookup"><span data-stu-id="2280b-556">**GUID**: {D8559EB9-20C0-410E-BEDA-7ED416AECC2A}</span></span>
-   <span data-ttu-id="2280b-557">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-557">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-558">**Имя модуля**: @% ProgramFiles% \\MsMpRes.dll защитника Windows \\ ,-104</span><span class="sxs-lookup"><span data-stu-id="2280b-558">**Module name**: @%ProgramFiles%\\Windows Defender\\MsMpRes.dll,-104</span></span>

### <a name="windows-firewall"></a><span data-ttu-id="2280b-559">Брандмауэр Windows</span><span class="sxs-lookup"><span data-stu-id="2280b-559">Windows Firewall</span></span>

-   <span data-ttu-id="2280b-560">**Каноническое имя**: Microsoft. брандмауэра Windows</span><span class="sxs-lookup"><span data-stu-id="2280b-560">**Canonical name**: Microsoft.WindowsFirewall</span></span>
-   <span data-ttu-id="2280b-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span><span class="sxs-lookup"><span data-stu-id="2280b-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span></span>
-   <span data-ttu-id="2280b-562">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-562">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-563">**Имя модуля**: @C: \\ \\FirewallControlPanel.dll Windows System32 \\ ,-12122</span><span class="sxs-lookup"><span data-stu-id="2280b-563">**Module name**: @C:\\Windows\\system32\\FirewallControlPanel.dll,-12122</span></span>
-   <span data-ttu-id="2280b-564">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-564">**Pages**</span></span>

    | <span data-ttu-id="2280b-565">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-565">Page Name</span></span>         | <span data-ttu-id="2280b-566">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-566">Opens</span></span>        |
    |-------------------|--------------|
    | <span data-ttu-id="2280b-567">пажеконфигуреаппс</span><span class="sxs-lookup"><span data-stu-id="2280b-567">pageConfigureApps</span></span> | <span data-ttu-id="2280b-568">Разрешенные приложения</span><span class="sxs-lookup"><span data-stu-id="2280b-568">Allowed apps</span></span> |

    

     

### <a name="windows-mobility-center"></a><span data-ttu-id="2280b-569">Центр мобильности Windows</span><span class="sxs-lookup"><span data-stu-id="2280b-569">Windows Mobility Center</span></span>

-   <span data-ttu-id="2280b-570">**Каноническое имя**: Microsoft. мобилитицентер</span><span class="sxs-lookup"><span data-stu-id="2280b-570">**Canonical name**: Microsoft.MobilityCenter</span></span>
-   <span data-ttu-id="2280b-571">**GUID**: {5ea4f148-308c-46d7-98a9-49041b1dd468}</span><span class="sxs-lookup"><span data-stu-id="2280b-571">**GUID**: {5ea4f148-308c-46d7-98a9-49041b1dd468}</span></span>
-   <span data-ttu-id="2280b-572">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-572">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-573">**Имя модуля**: @% systemroot% \\ system32 \\mblctr.exe,-1002</span><span class="sxs-lookup"><span data-stu-id="2280b-573">**Module name**: @%SystemRoot%\\system32\\mblctr.exe,-1002</span></span>

### <a name="windows-to-go"></a><span data-ttu-id="2280b-574">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="2280b-574">Windows To Go</span></span>

-   <span data-ttu-id="2280b-575">**Каноническое имя**: Microsoft. портаблеворкспацекреатор</span><span class="sxs-lookup"><span data-stu-id="2280b-575">**Canonical name**: Microsoft.PortableWorkspaceCreator</span></span>
-   <span data-ttu-id="2280b-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span><span class="sxs-lookup"><span data-stu-id="2280b-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span></span>
-   <span data-ttu-id="2280b-577">**Поддерживаемая ОС**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-577">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-578">**Имя модуля**: @% systemroot% \\ system32 \\pwcreator.exe,-151</span><span class="sxs-lookup"><span data-stu-id="2280b-578">**Module name**: @%SystemRoot%\\System32\\pwcreator.exe,-151</span></span>

### <a name="windows-update"></a><span data-ttu-id="2280b-579">Центра обновления Windows;</span><span class="sxs-lookup"><span data-stu-id="2280b-579">Windows Update</span></span>

-   <span data-ttu-id="2280b-580">**Каноническое имя**: Microsoft. windowsupdate</span><span class="sxs-lookup"><span data-stu-id="2280b-580">**Canonical name**: Microsoft.WindowsUpdate</span></span>
-   <span data-ttu-id="2280b-581">**GUID**: {36eef7db-88ad-4e81-AD49-0e313f0c35f8}</span><span class="sxs-lookup"><span data-stu-id="2280b-581">**GUID**: {36eef7db-88ad-4e81-ad49-0e313f0c35f8}</span></span>
-   <span data-ttu-id="2280b-582">**Поддерживаемая ОС**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-582">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="2280b-583">**Имя модуля**: @% systemroot% \\ system32 \\wucltux.dll,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-583">**Module name**: @%SystemRoot%\\system32\\wucltux.dll,-1</span></span>
-   <span data-ttu-id="2280b-584">**Страницы**</span><span class="sxs-lookup"><span data-stu-id="2280b-584">**Pages**</span></span>

    | <span data-ttu-id="2280b-585">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="2280b-585">Page Name</span></span>         | <span data-ttu-id="2280b-586">Открытия</span><span class="sxs-lookup"><span data-stu-id="2280b-586">Opens</span></span>               |
    |-------------------|---------------------|
    | <span data-ttu-id="2280b-587">pageSettings</span><span class="sxs-lookup"><span data-stu-id="2280b-587">pageSettings</span></span>      | <span data-ttu-id="2280b-588">Изменить параметры</span><span class="sxs-lookup"><span data-stu-id="2280b-588">Change settings</span></span>     |
    | <span data-ttu-id="2280b-589">пажеупдатехистори</span><span class="sxs-lookup"><span data-stu-id="2280b-589">pageUpdateHistory</span></span> | <span data-ttu-id="2280b-590">Просмотр журнала обновлений</span><span class="sxs-lookup"><span data-stu-id="2280b-590">View update history</span></span> |

    

     

### <a name="work-folders"></a><span data-ttu-id="2280b-591">рабочие папки</span><span class="sxs-lookup"><span data-stu-id="2280b-591">Work Folders</span></span>

-   <span data-ttu-id="2280b-592">**Каноническое имя**: Microsoft. воркфолдерс</span><span class="sxs-lookup"><span data-stu-id="2280b-592">**Canonical name**: Microsoft.WorkFolders</span></span>
-   <span data-ttu-id="2280b-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span><span class="sxs-lookup"><span data-stu-id="2280b-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span></span>
-   <span data-ttu-id="2280b-594">**Поддерживаемая ОС**: Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2280b-594">**Supported OS**: Windows 8.1</span></span>
-   <span data-ttu-id="2280b-595">**Имя модуля**: @C: \\ \\WorkfoldersControl.dll Windows System32 \\ ,-1</span><span class="sxs-lookup"><span data-stu-id="2280b-595">**Module name**: @C:\\Windows\\System32\\WorkfoldersControl.dll,-1</span></span>

## <a name="deprecated-control-panel-canonical-names"></a><span data-ttu-id="2280b-596">Устаревшие канонические имена панели управления</span><span class="sxs-lookup"><span data-stu-id="2280b-596">Deprecated Control Panel Canonical Names</span></span>

<span data-ttu-id="2280b-597">Ниже приведены канонические имена, которые больше не используются в Windows 8.1 или более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="2280b-597">The following are canonical names that are no longer in use as of Windows 8.1 or later.</span></span> <span data-ttu-id="2280b-598">Некоторые из них были удалены полностью.</span><span class="sxs-lookup"><span data-stu-id="2280b-598">Some have been removed altogether.</span></span> <span data-ttu-id="2280b-599">Другие были повторно сопоставлены в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="2280b-599">Others have been remapped in these situations:</span></span>

-   <span data-ttu-id="2280b-600">Элемент панели управления переименовывается.</span><span class="sxs-lookup"><span data-stu-id="2280b-600">A Control Panel item is renamed.</span></span> <span data-ttu-id="2280b-601">Переименованному элементу присваивается новое каноническое имя, но сохраняется тот же идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="2280b-601">The renamed item is given a new canonical name but keeps the same GUID.</span></span> <span data-ttu-id="2280b-602">В этом случае старое каноническое имя запускает переименованный элемент панели управления.</span><span class="sxs-lookup"><span data-stu-id="2280b-602">In this case, the old canonical name launches the renamed Control Panel item.</span></span> <span data-ttu-id="2280b-603">Имейте в виду, что запускаемый элемент может не использовать тот же пользовательский интерфейс, что и старая версия этого элемента.</span><span class="sxs-lookup"><span data-stu-id="2280b-603">Be aware that the item that's launched might not use the same UI as that item's older version.</span></span>
-   <span data-ttu-id="2280b-604">Функции одного или нескольких элементов панели управления перемещаются или объединяются в новый элемент.</span><span class="sxs-lookup"><span data-stu-id="2280b-604">The functionality of one or more Control Panel items is moved or consolidated into a new item.</span></span> <span data-ttu-id="2280b-605">В этом случае старое каноническое имя сопоставляется с наиболее подходящим новым элементом панели управления.</span><span class="sxs-lookup"><span data-stu-id="2280b-605">In this case, the old canonical name maps to the most appropriate new Control Panel item.</span></span>

> [!Note]  
> <span data-ttu-id="2280b-606">Повторное сопоставление существует для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="2280b-606">Remappings exist for backward compatibility.</span></span> <span data-ttu-id="2280b-607">Не следует использовать устаревшие значения в новом коде.</span><span class="sxs-lookup"><span data-stu-id="2280b-607">You should not use deprecated values in new code.</span></span>

 



| <span data-ttu-id="2280b-608">Устаревшее каноническое имя</span><span class="sxs-lookup"><span data-stu-id="2280b-608">Deprecated canonical name</span></span>                                   | <span data-ttu-id="2280b-609">Элемент панели управления</span><span class="sxs-lookup"><span data-stu-id="2280b-609">Control Panel Item</span></span>                | <span data-ttu-id="2280b-610">Код GUID</span><span class="sxs-lookup"><span data-stu-id="2280b-610">GUID</span></span>                                   | <span data-ttu-id="2280b-611">Примечания</span><span class="sxs-lookup"><span data-stu-id="2280b-611">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2280b-612">Microsoft. Аддхардваре</span><span class="sxs-lookup"><span data-stu-id="2280b-612">Microsoft.AddHardware</span></span>                                       | <span data-ttu-id="2280b-613">Установка оборудования</span><span class="sxs-lookup"><span data-stu-id="2280b-613">Add Hardware</span></span>                      | <span data-ttu-id="2280b-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span><span class="sxs-lookup"><span data-stu-id="2280b-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span></span> | <span data-ttu-id="2280b-615">Сопоставляется с [Microsoft. девицесандпринтерс](#devices-and-printers) в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-615">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2280b-616">Microsoft. Аудиодевицесандсаундсемес</span><span class="sxs-lookup"><span data-stu-id="2280b-616">Microsoft.AudioDevicesAndSoundThemes</span></span>                        | <span data-ttu-id="2280b-617">Звук</span><span class="sxs-lookup"><span data-stu-id="2280b-617">Sound</span></span>                             | <span data-ttu-id="2280b-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="2280b-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span> | <span data-ttu-id="2280b-619">Сопоставляется с [Microsoft. Sound](#sound) в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-619">Maps to [Microsoft.Sound](#sound) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2280b-620">Microsoft. Баккупандресторецентер/Microsoft. Баккупандресторе</span><span class="sxs-lookup"><span data-stu-id="2280b-620">Microsoft.BackupAndRestoreCenter/Microsoft.BackupAndRestore</span></span> | <span data-ttu-id="2280b-621">Центр архивации и восстановления</span><span class="sxs-lookup"><span data-stu-id="2280b-621">Backup and Restore Center</span></span>         | <span data-ttu-id="2280b-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span><span class="sxs-lookup"><span data-stu-id="2280b-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span></span> | <span data-ttu-id="2280b-623">Microsoft. Баккупандресторецентер сопоставляется с Microsoft. Баккупандресторе в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-623">Microsoft.BackupAndRestoreCenter maps to Microsoft.BackupAndRestore in Windows 7.</span></span> <span data-ttu-id="2280b-624">Оба варианта удаляются из Windows 8; Вместо этого используйте [Microsoft. филехистори](#file-history) .</span><span class="sxs-lookup"><span data-stu-id="2280b-624">Both are removed as of Windows 8; use [Microsoft.FileHistory](#file-history) instead.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="2280b-625">Microsoft. CardSpace</span><span class="sxs-lookup"><span data-stu-id="2280b-625">Microsoft.CardSpace</span></span>                                         | <span data-ttu-id="2280b-626">Windows CardSpace</span><span class="sxs-lookup"><span data-stu-id="2280b-626">Windows CardSpace</span></span>                 | <span data-ttu-id="2280b-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span><span class="sxs-lookup"><span data-stu-id="2280b-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span></span> | <span data-ttu-id="2280b-628">Удалено в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2280b-628">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2280b-629">Microsoft. Десктопгаджетс</span><span class="sxs-lookup"><span data-stu-id="2280b-629">Microsoft.DesktopGadgets</span></span>                                    | <span data-ttu-id="2280b-630">Мини-приложения рабочего стола</span><span class="sxs-lookup"><span data-stu-id="2280b-630">Desktop Gadgets</span></span>                   | <span data-ttu-id="2280b-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="2280b-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="2280b-632">Удалено в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2280b-632">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2280b-633">Microsoft. Жетпрограмсонлине</span><span class="sxs-lookup"><span data-stu-id="2280b-633">Microsoft.GetProgramsOnline</span></span>                                 | <span data-ttu-id="2280b-634">Windows Marketplace</span><span class="sxs-lookup"><span data-stu-id="2280b-634">Windows Marketplace</span></span>               | <span data-ttu-id="2280b-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span><span class="sxs-lookup"><span data-stu-id="2280b-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span></span> | <span data-ttu-id="2280b-636">Удалено в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-636">Removed as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2280b-637">Microsoft. Инфраредоптионс</span><span class="sxs-lookup"><span data-stu-id="2280b-637">Microsoft.InfraredOptions</span></span>                                   | <span data-ttu-id="2280b-638">Инфракрасная связь</span><span class="sxs-lookup"><span data-stu-id="2280b-638">Infrared</span></span>                          | <span data-ttu-id="2280b-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="2280b-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span> | <span data-ttu-id="2280b-640">Сопоставляется [Microsoft. Инфракрасная связь](#infrared) на Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-640">Maps to [Microsoft.Infrared](#infrared) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2280b-641">Microsoft. Language</span><span class="sxs-lookup"><span data-stu-id="2280b-641">Microsoft.Language</span></span>                                          | <span data-ttu-id="2280b-642">Язык</span><span class="sxs-lookup"><span data-stu-id="2280b-642">Language</span></span>                          | <span data-ttu-id="2280b-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span><span class="sxs-lookup"><span data-stu-id="2280b-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span></span> | <span data-ttu-id="2280b-644">Удалено с Windows 10, версия 1803</span><span class="sxs-lookup"><span data-stu-id="2280b-644">Removed as of Windows 10, version 1803</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="2280b-645">Microsoft. Локатионандосерсенсорс</span><span class="sxs-lookup"><span data-stu-id="2280b-645">Microsoft.LocationAndOtherSensors</span></span>                           | <span data-ttu-id="2280b-646">Расположение и другие датчики</span><span class="sxs-lookup"><span data-stu-id="2280b-646">Location and Other Sensors</span></span>        | <span data-ttu-id="2280b-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="2280b-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span></span> | <span data-ttu-id="2280b-648">Сопоставляется с [Microsoft. локатионсеттингс](#infrared) в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2280b-648">Maps to [Microsoft.LocationSettings](#infrared) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2280b-649">Microsoft. Пенандинпутдевицес</span><span class="sxs-lookup"><span data-stu-id="2280b-649">Microsoft.PenAndInputDevices</span></span>                                | <span data-ttu-id="2280b-650">Перо и устройства ввода</span><span class="sxs-lookup"><span data-stu-id="2280b-650">Pen and Input Devices</span></span>             | <span data-ttu-id="2280b-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="2280b-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span> | <span data-ttu-id="2280b-652">Сопоставляется с [Microsoft. пенандтауч](#pen-and-touch) в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-652">Maps to [Microsoft.PenAndTouch](#pen-and-touch) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2280b-653">Microsoft. Пеопленеарме</span><span class="sxs-lookup"><span data-stu-id="2280b-653">Microsoft.PeopleNearMe</span></span>                                      | <span data-ttu-id="2280b-654">Соседние пользователи</span><span class="sxs-lookup"><span data-stu-id="2280b-654">People Near Me</span></span>                    | <span data-ttu-id="2280b-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span><span class="sxs-lookup"><span data-stu-id="2280b-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span></span> | <span data-ttu-id="2280b-656">Удалено в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2280b-656">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2280b-657">Microsoft. Перформанцеинформатионандтулс</span><span class="sxs-lookup"><span data-stu-id="2280b-657">Microsoft.PerformanceInformationAndTools</span></span>                    | <span data-ttu-id="2280b-658">Сведения о производительности и средства</span><span class="sxs-lookup"><span data-stu-id="2280b-658">Performance Information and Tools</span></span> | <span data-ttu-id="2280b-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span><span class="sxs-lookup"><span data-stu-id="2280b-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span></span> | <span data-ttu-id="2280b-660">Удалено из Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="2280b-660">Removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="2280b-661">Microsoft. Фонеандмодемоптионс</span><span class="sxs-lookup"><span data-stu-id="2280b-661">Microsoft.PhoneAndModemOptions</span></span>                              | <span data-ttu-id="2280b-662">Телефон и модем</span><span class="sxs-lookup"><span data-stu-id="2280b-662">Phone and Modem</span></span>                   | <span data-ttu-id="2280b-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="2280b-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span></span> | <span data-ttu-id="2280b-664">Сопоставляется с [Microsoft. фонеандмодем](#phone-and-modem) в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-664">Maps to [Microsoft.PhoneAndModem](#phone-and-modem) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2280b-665">Microsoft. Printers</span><span class="sxs-lookup"><span data-stu-id="2280b-665">Microsoft.Printers</span></span>                                          | <span data-ttu-id="2280b-666">принтеры;</span><span class="sxs-lookup"><span data-stu-id="2280b-666">Printers</span></span>                          | <span data-ttu-id="2280b-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="2280b-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span></span> | <span data-ttu-id="2280b-668">Сопоставляется с [Microsoft. девицесандпринтерс](#devices-and-printers) в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-668">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2280b-669">Microsoft. Проблемрепортсандсолутионс</span><span class="sxs-lookup"><span data-stu-id="2280b-669">Microsoft.ProblemReportsAndSolutions</span></span>                        | <span data-ttu-id="2280b-670">Отчеты о проблемах и решения</span><span class="sxs-lookup"><span data-stu-id="2280b-670">Problem Reports and Solutions</span></span>     | <span data-ttu-id="2280b-671">{ФКФИКАЕ-EE1B-4849-AE50-685DCF7717EC}</span><span class="sxs-lookup"><span data-stu-id="2280b-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span></span> | <span data-ttu-id="2280b-672">Сопоставляется с [Microsoft. актионцентер](#action-center) в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-672">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2280b-673">Microsoft. Регионаландлангуажеоптионс</span><span class="sxs-lookup"><span data-stu-id="2280b-673">Microsoft.RegionalAndLanguageOptions</span></span>                        | <span data-ttu-id="2280b-674">Региональные и языковые параметры</span><span class="sxs-lookup"><span data-stu-id="2280b-674">Regional and Language Options</span></span>     | <span data-ttu-id="2280b-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="2280b-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span> | <span data-ttu-id="2280b-676">Сопоставляется с [Microsoft. регионандлангуаже](#region) в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-676">Maps to [Microsoft.RegionAndLanguage](#region) as of Windows 7.</span></span> <span data-ttu-id="2280b-677">Обратите внимание, что в Windows 8 для каждого региона и языка задан собственный элемент панели управления.</span><span class="sxs-lookup"><span data-stu-id="2280b-677">Note that as of Windows 8, Region and Language were each given their own Control Panel item.</span></span> <span data-ttu-id="2280b-678">В настоящее время Microsoft. Регионаландлангуажеоптионс и Microsoft. Регионандлангуаже открывают элемент региона.</span><span class="sxs-lookup"><span data-stu-id="2280b-678">Both Microsoft.RegionalAndLanguageOptions and Microsoft.RegionAndLanguage currently open the Region item.</span></span> <span data-ttu-id="2280b-679">Для доступа к элементу языка необходимо использовать [Microsoft. Language](#location-settings) .</span><span class="sxs-lookup"><span data-stu-id="2280b-679">You must use [Microsoft.Language](#location-settings) to access the Language item.</span></span> |
| <span data-ttu-id="2280b-680">Microsoft. Секуритицентер</span><span class="sxs-lookup"><span data-stu-id="2280b-680">Microsoft.SecurityCenter</span></span>                                    | <span data-ttu-id="2280b-681">Центр обеспечения безопасности Windows</span><span class="sxs-lookup"><span data-stu-id="2280b-681">Windows Security Center</span></span>           | <span data-ttu-id="2280b-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span><span class="sxs-lookup"><span data-stu-id="2280b-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span></span> | <span data-ttu-id="2280b-683">Сопоставляется с [Microsoft. актионцентер](#action-center) в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-683">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2280b-684">Microsoft. Спичрекогнитионоптионс</span><span class="sxs-lookup"><span data-stu-id="2280b-684">Microsoft.SpeechRecognitionOptions</span></span>                          | <span data-ttu-id="2280b-685">Параметры распознавания речи</span><span class="sxs-lookup"><span data-stu-id="2280b-685">Speech Recognition Options</span></span>        | <span data-ttu-id="2280b-686">{58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="2280b-686">{58E3C745-D971-4081-9034-86E34B30836A}</span></span> | <span data-ttu-id="2280b-687">Сопоставляется с [Microsoft. спичрекогнитион](#speech-recognition) в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-687">Maps to [Microsoft.SpeechRecognition](#speech-recognition) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="2280b-688">Microsoft. Таскбарандстартмену</span><span class="sxs-lookup"><span data-stu-id="2280b-688">Microsoft.TaskbarAndStartMenu</span></span>                               | <span data-ttu-id="2280b-689">Панель задач и меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="2280b-689">Taskbar and Start Menu</span></span>            | <span data-ttu-id="2280b-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="2280b-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span> | <span data-ttu-id="2280b-691">Сопоставляется с [Microsoft. панель задач](#speech-recognition) в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2280b-691">Maps to [Microsoft.Taskbar](#speech-recognition) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2280b-692">Microsoft. Велкомецентер</span><span class="sxs-lookup"><span data-stu-id="2280b-692">Microsoft.WelcomeCenter</span></span>                                     | <span data-ttu-id="2280b-693">Центр начальной настройки</span><span class="sxs-lookup"><span data-stu-id="2280b-693">Welcome Center</span></span>                    | <span data-ttu-id="2280b-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span><span class="sxs-lookup"><span data-stu-id="2280b-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span></span> | <span data-ttu-id="2280b-695">Сопоставляется с Microsoft. GettingStarted в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-695">Maps to Microsoft.GettingStarted in Windows 7.</span></span> <span data-ttu-id="2280b-696">Открывает домашнюю страницу панели управления в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2280b-696">Launches the Control Panel home page as of Windows 8.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2280b-697">Microsoft. Виндовссидебарпропертиес</span><span class="sxs-lookup"><span data-stu-id="2280b-697">Microsoft.WindowsSidebarProperties</span></span>                          | <span data-ttu-id="2280b-698">Свойства боковой панели Windows</span><span class="sxs-lookup"><span data-stu-id="2280b-698">Windows Sidebar Properties</span></span>        | <span data-ttu-id="2280b-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="2280b-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="2280b-700">Сопоставляется с Microsoft. Десктопгаджетс в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2280b-700">Maps to Microsoft.DesktopGadgets in Windows 7.</span></span> <span data-ttu-id="2280b-701">Удалено в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2280b-701">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="2280b-702">Microsoft. Виндовссидешов</span><span class="sxs-lookup"><span data-stu-id="2280b-702">Microsoft.WindowsSideShow</span></span>                                   | <span data-ttu-id="2280b-703">Windows SideShow</span><span class="sxs-lookup"><span data-stu-id="2280b-703">Windows SideShow</span></span>                  | <span data-ttu-id="2280b-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span><span class="sxs-lookup"><span data-stu-id="2280b-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span></span> | <span data-ttu-id="2280b-705">Функция устарела в Windows 8, удалена из Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="2280b-705">Feature deprecated in Windows 8, removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a><span data-ttu-id="2280b-706">Использование канонических имен в локальных групповая политика</span><span class="sxs-lookup"><span data-stu-id="2280b-706">Using Canonical Names in Local Group Policy</span></span>

<span data-ttu-id="2280b-707">Начиная с Windows 7, для ограничения доступа к отдельным элементам панели управления с помощью групповой политики можно использовать канонические имена.</span><span class="sxs-lookup"><span data-stu-id="2280b-707">As of Windows 7, you can use canonical names to restrict access to individual Control Panel items through group policy.</span></span> <span data-ttu-id="2280b-708">Эта же процедура может использоваться в Windows Vista, но вместо канонического имени необходимо использовать имя модуля.</span><span class="sxs-lookup"><span data-stu-id="2280b-708">This same procedure can be used in Windows Vista, but you have to use the module name instead of the canonical name.</span></span>

### <a name="hiding-individual-control-panel-items"></a><span data-ttu-id="2280b-709">Скрытие отдельных элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="2280b-709">Hiding individual Control Panel items</span></span>

<span data-ttu-id="2280b-710">Используйте этот метод, если требуется отобразить больше элементов панели управления, чем требуется скрыть.</span><span class="sxs-lookup"><span data-stu-id="2280b-710">Use this method if you want to show more Control Panel items than you want to hide.</span></span>

1.  <span data-ttu-id="2280b-711">Запустите файл gpedit. msc, чтобы запустить редактор локальных групповых политик.</span><span class="sxs-lookup"><span data-stu-id="2280b-711">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="2280b-712">Можно также ввести "Групповая политика" на начальном экране Windows 8.1 и выбрать пункт **изменить групповую политику** в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="2280b-712">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="2280b-713">Выберите **Конфигурация пользователя**  >  **Административные шаблоны**  >  **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="2280b-713">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="2280b-714">Выберите **Скрыть указанные элементы панели управления**.</span><span class="sxs-lookup"><span data-stu-id="2280b-714">Select **Hide specified Control Panel items**.</span></span>
4.  <span data-ttu-id="2280b-715">В открывшемся окне **Скрыть указанные элементы панели управления** щелкните **включено**.</span><span class="sxs-lookup"><span data-stu-id="2280b-715">In the **Hide Specified Control Panel Items** window that opens, click **Enabled**.</span></span>
5.  <span data-ttu-id="2280b-716">Нажмите кнопку « **Показывать** » на панели «параметры», чтобы отобразить список запрещенных элементов панели управления.</span><span class="sxs-lookup"><span data-stu-id="2280b-716">Click the **Show** button in the Options panel to show the list of disallowed Control Panel items.</span></span>
6.  <span data-ttu-id="2280b-717">В открывшемся окне **Отображение содержимого** введите каноническое имя в столбец **значение** .</span><span class="sxs-lookup"><span data-stu-id="2280b-717">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="2280b-718">При необходимости повторите операцию.</span><span class="sxs-lookup"><span data-stu-id="2280b-718">Repeat as necessary.</span></span>
7.  <span data-ttu-id="2280b-719">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2280b-719">Click **OK**.</span></span>

### <a name="showing-individual-control-panel-items"></a><span data-ttu-id="2280b-720">Отображение отдельных элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="2280b-720">Showing individual Control Panel items</span></span>

<span data-ttu-id="2280b-721">Используйте этот метод, если требуется скрыть больше элементов панели управления, чем требуется отобразить.</span><span class="sxs-lookup"><span data-stu-id="2280b-721">Use this method if you want to hide more Control Panel items than you want to show.</span></span>

1.  <span data-ttu-id="2280b-722">Запустите файл gpedit. msc, чтобы запустить редактор локальных групповых политик.</span><span class="sxs-lookup"><span data-stu-id="2280b-722">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="2280b-723">Можно также ввести "Групповая политика" на начальном экране Windows 8.1 и выбрать пункт **изменить групповую политику** в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="2280b-723">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="2280b-724">Выберите **Конфигурация пользователя**  >  **Административные шаблоны**  >  **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="2280b-724">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="2280b-725">Выберите **Показывать только указанные элементы панели управления**.</span><span class="sxs-lookup"><span data-stu-id="2280b-725">Select **Show only specified Control Panel items**.</span></span>
4.  <span data-ttu-id="2280b-726">В открывшемся окне **Показывать только указанные элементы панели управления** щелкните **включено**.</span><span class="sxs-lookup"><span data-stu-id="2280b-726">In the **Show Only Specified Control Panel Items** window that opens, click **Enabled**.</span></span> <span data-ttu-id="2280b-727">Это скрывает все элементы на панели управления.</span><span class="sxs-lookup"><span data-stu-id="2280b-727">This hides everything in the Control Panel.</span></span>
5.  <span data-ttu-id="2280b-728">Нажмите кнопку « **Показывать** » на панели «параметры», чтобы отобразить список разрешенных элементов панели управления.</span><span class="sxs-lookup"><span data-stu-id="2280b-728">Click the **Show** button in the Options panel to show the list of allowed Control Panel items.</span></span>
6.  <span data-ttu-id="2280b-729">В открывшемся окне **Отображение содержимого** введите каноническое имя в столбец **значение** .</span><span class="sxs-lookup"><span data-stu-id="2280b-729">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="2280b-730">При необходимости повторите операцию.</span><span class="sxs-lookup"><span data-stu-id="2280b-730">Repeat as necessary.</span></span>
7.  <span data-ttu-id="2280b-731">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2280b-731">Click **OK**.</span></span>

<span data-ttu-id="2280b-732">Если вы хотите удалить все записи, добавленные в список Показать или скрыть элементы панели управления, вернитесь на экран в шаге 4 и выберите **не настроено** для очистки списка.</span><span class="sxs-lookup"><span data-stu-id="2280b-732">If you want to remove all of the entries that you've added to a Show or Hide Control Panel items list, return to the screen in step 4 and select **Not Configured** to clear the list.</span></span> <span data-ttu-id="2280b-733">Если вы хотите хранить записи, но приостановите ограничения, выберите **отключено**.</span><span class="sxs-lookup"><span data-stu-id="2280b-733">If you want to retain your entries but suspend the restrictions, select **Disabled**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2280b-734">Примечания</span><span class="sxs-lookup"><span data-stu-id="2280b-734">Remarks</span></span>

<span data-ttu-id="2280b-735">На панели управления могут отображаться элементы, которые не перечислены здесь.</span><span class="sxs-lookup"><span data-stu-id="2280b-735">You might see items in your Control Panel that are not listed here.</span></span> <span data-ttu-id="2280b-736">Эти элементы не являются частью Windows, а добавляются во время установки различных программных и аппаратных средств, например Microsoft Office или видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="2280b-736">Those items are not part of Windows, but instead are added during the installation of various software and hardware, such as Microsoft Office or a video card.</span></span> <span data-ttu-id="2280b-737">Элементы панели управления, отличной от Windows, могут иметь или не иметь канонического имени.</span><span class="sxs-lookup"><span data-stu-id="2280b-737">Non-Windows Control Panel items may or may not have a canonical name.</span></span> <span data-ttu-id="2280b-738">Чтобы найти каноническое имя элемента панели управления, не указанного здесь, найдите в реестре следующие пути:</span><span class="sxs-lookup"><span data-stu-id="2280b-738">To find the canonical name of a Control Panel item not listed here, look in the registry under these paths:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

<span data-ttu-id="2280b-739">Дополнительные сведения, которые могут помочь в обнаружении необходимых идентификаторов CLSID, см. в статьях [Регистрация исполняемых элементов панели управления](how-to-register-an-executable-control-panel-item-registration-.md) и [Регистрация элементов панели управления DLL](how-to-register-dll-control-panel-item-registration-.md).</span><span class="sxs-lookup"><span data-stu-id="2280b-739">For more information that can help you discover the necessary CLSIDs, see [How to Register Executable Control Panel Items](how-to-register-an-executable-control-panel-item-registration-.md) and [How to Register DLL Control Panel Items](how-to-register-dll-control-panel-item-registration-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2280b-740">См. также</span><span class="sxs-lookup"><span data-stu-id="2280b-740">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2280b-741">Исполнение элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="2280b-741">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="2280b-742">**иопенконтролпанел**</span><span class="sxs-lookup"><span data-stu-id="2280b-742">**IOpenControlPanel**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



