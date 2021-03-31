---
description: При выполнении резервного копирования или восстановления VSS состояние системы Windows определяется как коллекция из нескольких ключевых элементов операционной системы и их файлов. Эти элементы всегда должны рассматриваться как единое целое при операциях резервного копирования и восстановления.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Резервное копирование и восстановление состояния системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812808"
---
# <a name="backing-up-and-restoring-system-state"></a><span data-ttu-id="2d133-104">Резервное копирование и восстановление состояния системы</span><span class="sxs-lookup"><span data-stu-id="2d133-104">Backing Up and Restoring System State</span></span>

> [!Note]  
> <span data-ttu-id="2d133-105">Этот раздел относится к Windows Vista, Windows Server 2008 и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="2d133-105">This topic applies to Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="2d133-106">Сведения о Windows Server 2003 см. [в статье резервное копирование и восстановление состояния системы в Windows server 2003 R2 и Windows server 2003 с пакетом обновления 1 (SP1)](backing-up-and-restoring-system-state-under-vss.md)</span><span class="sxs-lookup"><span data-stu-id="2d133-106">For information about Windows Server 2003, see [Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)</span></span>

 

<span data-ttu-id="2d133-107">При выполнении резервного копирования или восстановления VSS состояние системы Windows определяется как коллекция из нескольких ключевых элементов операционной системы и их файлов.</span><span class="sxs-lookup"><span data-stu-id="2d133-107">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="2d133-108">Эти элементы всегда должны рассматриваться как единое целое при операциях резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="2d133-108">These elements should always be treated as a unit by backup and restore operations.</span></span>

> [!Note]  
> <span data-ttu-id="2d133-109">Корпорация Майкрософт не предоставляет техническую поддержку для разработчиков и ИТ-специалистов по внедрению оперативного восстановления состояния системы в Windows (все выпуски).</span><span class="sxs-lookup"><span data-stu-id="2d133-109">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

 

<span data-ttu-id="2d133-110">При резервном копировании и восстановлении состояния системы рекомендуемой стратегией является резервное копирование и восстановление системных и загрузочных томов в дополнение к файлам, перечисленным модулями записи состояния системы.</span><span class="sxs-lookup"><span data-stu-id="2d133-110">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span> <span data-ttu-id="2d133-111">Модули записи состояния системы — это модули записи, для которых в качестве атрибута [**\_ \_ типа использования VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) задано значение VSS \_ UT \_ бутаблесистемстате или VSS \_ UT \_ системсервице.</span><span class="sxs-lookup"><span data-stu-id="2d133-111">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d133-112">Если модуль записи VSS определяется [**\_ \_ типом использования VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) как модуль записи состояния системы, он должен быть включен в резервную копию состояния системы, даже если он доступен для выбора.</span><span class="sxs-lookup"><span data-stu-id="2d133-112">If a VSS Writer is identified by its [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) as a system state writer it must be included in a system state backup even if it is selectable.</span></span>

 

<span data-ttu-id="2d133-113">В дополнение к перечислимым двоичным файлам операционной системы и драйверов, перечисленным модулями записи состояния системы, существуют некоторые другие файлы, которые необходимо архивировать как часть состояния системы.</span><span class="sxs-lookup"><span data-stu-id="2d133-113">In addition to the enumerated operating system and driver binary files that are enumerated by the system state writers, there are certain other files that must be backed up as part of system state.</span></span>

<span data-ttu-id="2d133-114">Все компоненты, сообщаемые модулем записи состояния системы VSS, являются частью состояния системы, за исключением тех, для которых \_ \_ установлен флаг VSS CF не \_ \_ состояния системы.</span><span class="sxs-lookup"><span data-stu-id="2d133-114">All the components reported by a VSS system state writer are part of system state except those for which the VSS\_CF\_NOT\_SYSTEM\_STATE flag is set.</span></span>

<span data-ttu-id="2d133-115">Программы резервного копирования должны также установить раздел реестра **ластрестореид** .</span><span class="sxs-lookup"><span data-stu-id="2d133-115">Backup programs should also set the **LastRestoreId** registry key.</span></span> <span data-ttu-id="2d133-116">Дополнительные сведения см. в разделах [разделы реестра и значения для резервного копирования и восстановления](../backup/registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="2d133-116">For more information, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

> [!Note]  
> <span data-ttu-id="2d133-117">В Windows Vista, Windows Server 2008 и более поздних версиях имена и расположения некоторых системных файлов были изменены следующим образом.</span><span class="sxs-lookup"><span data-stu-id="2d133-117">In Windows Vista, Windows Server 2008, and later, the names and locations of some system files have been changed as follows.</span></span>

 

## <a name="system-state"></a><span data-ttu-id="2d133-118">Состояние системы</span><span class="sxs-lookup"><span data-stu-id="2d133-118">System State</span></span>

<span data-ttu-id="2d133-119">Для Windows Server 2012 и более поздних версий в дополнение к файлам, сообщаемым различными модулями записи состояния системы VSS, необходимо явно включать только следующие файлы лицензирования, а следующие файлы DRM необходимо исключить явным образом.</span><span class="sxs-lookup"><span data-stu-id="2d133-119">For Windows Server 2012 and later, in addition to the files reported by the various VSS system-state writers, only the following licensing files need to be included explicitly, and the following DRM files need to be excluded explicitly.</span></span>

## <a name="windows-media-digital-rights-management-files"></a><span data-ttu-id="2d133-120">Файлы цифровых Rights Management Windows Media</span><span class="sxs-lookup"><span data-stu-id="2d133-120">Windows Media Digital Rights Management Files</span></span>

<span data-ttu-id="2d133-121">В Windows Server 2008 и более поздних версиях следующие файлы, включая все подкаталоги по следующему пути, исключаются из состояния системы и их не следует архивировать.</span><span class="sxs-lookup"><span data-stu-id="2d133-121">In Windows Server 2008 and later, the following files, including all subdirectories under the following path, are excluded from system state and must not be backed up:</span></span>

-   <span data-ttu-id="2d133-122">% Папка ProgramData% \\ \\ Windows \\ DRM</span><span class="sxs-lookup"><span data-stu-id="2d133-122">%ProgramData%\\Microsoft\\Windows\\DRM</span></span>\\

<span data-ttu-id="2d133-123">Это приводит к замене информации в разделе Windows Media Digital Rights Management [работы с файловой системой и функциями безопасности](working-with-file-system-and-security-features.md).</span><span class="sxs-lookup"><span data-stu-id="2d133-123">This supersedes the information in the Windows Media Digital Rights Management section of [Working with File System and Security Features](working-with-file-system-and-security-features.md).</span></span>

## <a name="performance-counter-configuration-files"></a><span data-ttu-id="2d133-124">Файлы конфигурации счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="2d133-124">Performance Counter Configuration Files</span></span>

<span data-ttu-id="2d133-125">Файлы конфигурации счетчиков производительности находятся в каталоге% SystemRoot% \\ system32 \\ и имеют следующие имена:</span><span class="sxs-lookup"><span data-stu-id="2d133-125">The performance counter configuration files are located in the %SystemRoot%\\System32\\ directory and have the following names:</span></span>

<dl> <span data-ttu-id="2d133-126">Производительности? 00?. включая</span><span class="sxs-lookup"><span data-stu-id="2d133-126">Perf?00?.dat</span></span>  
<span data-ttu-id="2d133-127">Perfc0??. включая</span><span class="sxs-lookup"><span data-stu-id="2d133-127">Perfc0??.dat</span></span>  
<span data-ttu-id="2d133-128">Perfd0??. включая</span><span class="sxs-lookup"><span data-stu-id="2d133-128">Perfd0??.dat</span></span>  
<span data-ttu-id="2d133-129">Perfh0??. включая</span><span class="sxs-lookup"><span data-stu-id="2d133-129">Perfh0??.dat</span></span>  
<span data-ttu-id="2d133-130">Perfi0??. включая</span><span class="sxs-lookup"><span data-stu-id="2d133-130">Perfi0??.dat</span></span>  
<span data-ttu-id="2d133-131">Prfc0???. включая</span><span class="sxs-lookup"><span data-stu-id="2d133-131">Prfc0???.dat</span></span>  
<span data-ttu-id="2d133-132">Prfd0???. включая</span><span class="sxs-lookup"><span data-stu-id="2d133-132">Prfd0???.dat</span></span>  
<span data-ttu-id="2d133-133">Prfh0???. включая</span><span class="sxs-lookup"><span data-stu-id="2d133-133">Prfh0???.dat</span></span>  
<span data-ttu-id="2d133-134">Prfi0???. включая</span><span class="sxs-lookup"><span data-stu-id="2d133-134">Prfi0???.dat</span></span>  
</dl>

<span data-ttu-id="2d133-135">Эти файлы изменяются только во время установки приложения и должны быть архивированы и восстановлены во время резервного копирования и восстановления состояния системы.</span><span class="sxs-lookup"><span data-stu-id="2d133-135">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

## <a name="iis-configuration-files"></a><span data-ttu-id="2d133-136">Файлы конфигурации IIS</span><span class="sxs-lookup"><span data-stu-id="2d133-136">IIS Configuration Files</span></span>

> [!Note]  
> <span data-ttu-id="2d133-137">В Windows Vista с пакетом обновления 1 (SP1) и более поздних версий не следует создавать резервные копии этих файлов.</span><span class="sxs-lookup"><span data-stu-id="2d133-137">In Windows Vista with Service Pack 1 (SP1) and later, you should not back up these files.</span></span> <span data-ttu-id="2d133-138">Вместо этого используйте модуль записи конфигурации IIS в Box.</span><span class="sxs-lookup"><span data-stu-id="2d133-138">Instead, use the in-box IIS configuration writer.</span></span> <span data-ttu-id="2d133-139">Дополнительные сведения об этом модуле записи см. [в разделе модули записи VSS в Box](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="2d133-139">For more information about this writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

<span data-ttu-id="2d133-140">Ниже перечислены соответствующие файлы конфигурации IIS и их расположения.</span><span class="sxs-lookup"><span data-stu-id="2d133-140">The relevant IIS configuration files and their locations are listed below:</span></span>

-   <span data-ttu-id="2d133-141">Файл machine.config .NET FX находится в каталоге версий платформы.</span><span class="sxs-lookup"><span data-stu-id="2d133-141">The .NET FX machine.config file is located in the framework version directory.</span></span>
-   <span data-ttu-id="2d133-142">Корневой web.config файл ASP.NET находится в каталоге версий платформы.</span><span class="sxs-lookup"><span data-stu-id="2d133-142">The ASP.NET root web.config file is located in the framework version directory.</span></span>
    > [!Note]  
    > <span data-ttu-id="2d133-143">Файлы конфигурации для .NET FX и ASP.NET находятся в каталоге версий платформы.</span><span class="sxs-lookup"><span data-stu-id="2d133-143">The configuration files for both .NET FX and ASP.NET are in the framework version directory.</span></span> <span data-ttu-id="2d133-144">Если на компьютере установлено несколько версий платформы, этот каталог будет содержать один файл конфигурации для каждой установленной версии.</span><span class="sxs-lookup"><span data-stu-id="2d133-144">If multiple versions of the framework are installed on the computer, this directory will contain one configuration file for each installed version.</span></span>

     

-   <span data-ttu-id="2d133-145">Файл конфигурации центра IIS applicationHost.config находится в каталоге% WINDIR% \\ system32 \\ Inetsrv \\ config.</span><span class="sxs-lookup"><span data-stu-id="2d133-145">The IIS applicationHost.config central configuration file is located in the %windir%\\system32\\inetsrv\\config directory.</span></span> <span data-ttu-id="2d133-146">Чтобы сервер понял этот файл конфигурации, существуют файлы схемы, определяющие его грамматику и структуру.</span><span class="sxs-lookup"><span data-stu-id="2d133-146">For the server to understand this configuration file, there are schema files that determine its grammar and structure.</span></span> <span data-ttu-id="2d133-147">Эти файлы находятся в \\ \\ \\ каталоге схемы конфигурации% WINDIR% system32 Inetsrv \\ .</span><span class="sxs-lookup"><span data-stu-id="2d133-147">These files are located in the %windir%\\system32\\inetsrv\\config\\schema directory.</span></span>

<span data-ttu-id="2d133-148">Путь к каталогу версии платформы хранится в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="2d133-148">The framework version directory path is stored in the following registry key:</span></span>

<span data-ttu-id="2d133-149">**HKEY \_ по для локального \_ компьютера \\ \\ Майкрософт \\ . NETFramework \\ InstallRoot**</span><span class="sxs-lookup"><span data-stu-id="2d133-149">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\.NETFramework\\InstallRoot**</span></span>

<span data-ttu-id="2d133-150">Кроме того, необходимо создать резервную копию следующих ключей шифрования:</span><span class="sxs-lookup"><span data-stu-id="2d133-150">In addition, the following cryptography keys must be backed up:</span></span><dl> <span data-ttu-id="2d133-151">% Папка ProgramData% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="2d133-151">%ProgramData%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span>  
<span data-ttu-id="2d133-152">% SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*</span><span class="sxs-lookup"><span data-stu-id="2d133-152">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
</dl>

## <a name="framework-files"></a><span data-ttu-id="2d133-153">Файлы платформы</span><span class="sxs-lookup"><span data-stu-id="2d133-153">Framework Files</span></span>

<span data-ttu-id="2d133-154">Необходимо создать резервную копию всех версий платформы .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="2d133-154">All versions of the .NET framework must be backed up.</span></span> <span data-ttu-id="2d133-155">Файлы находятся в одном или обоих следующих каталогах:</span><span class="sxs-lookup"><span data-stu-id="2d133-155">The files are located in one or both of the following directories:</span></span>

<dl> <span data-ttu-id="2d133-156">% WINDIR% \\ Microsoft.NET \\ Framework</span><span class="sxs-lookup"><span data-stu-id="2d133-156">%windir%\\Microsoft.Net\\Framework</span></span>  
<span data-ttu-id="2d133-157">% WINDIR% \\ Microsoft.NET \\ Framework64</span><span class="sxs-lookup"><span data-stu-id="2d133-157">%windir%\\Microsoft.Net\\Framework64</span></span>  
</dl>

<span data-ttu-id="2d133-158">Кроме того, необходимо создать резервную копию файлов сборки.</span><span class="sxs-lookup"><span data-stu-id="2d133-158">In addition, the assembly files must be backed up.</span></span> <span data-ttu-id="2d133-159">Эти файлы расположены в следующем каталоге:</span><span class="sxs-lookup"><span data-stu-id="2d133-159">These files are located in the following directory:</span></span><dl> <span data-ttu-id="2d133-160">Сборка% WINDIR% \\</span><span class="sxs-lookup"><span data-stu-id="2d133-160">%windir%\\assembly</span></span>  
</dl>

## <a name="task-scheduler-task-files"></a><span data-ttu-id="2d133-161">Файлы задач планировщик задач</span><span class="sxs-lookup"><span data-stu-id="2d133-161">Task Scheduler Task Files</span></span>

<span data-ttu-id="2d133-162">Необходимо создать резервную копию файлов задач планировщика заданий.</span><span class="sxs-lookup"><span data-stu-id="2d133-162">The task scheduler's task files must be backed up.</span></span> <span data-ttu-id="2d133-163">Файлы находятся в одном или обоих следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="2d133-163">The files are located in one or both of the following locations:</span></span>

<dl> <span data-ttu-id="2d133-164">задачи% WINDIR% \\ system32 \\ и все подкаталоги (рекурсивно)</span><span class="sxs-lookup"><span data-stu-id="2d133-164">%windir%\\system32\\tasks and any subdirectories (recursively)</span></span>  
<span data-ttu-id="2d133-165">задач% WINDIR% \\ (нет подкаталогов)</span><span class="sxs-lookup"><span data-stu-id="2d133-165">%windir%\\tasks (no subdirectories)</span></span>  
</dl>

 

 
