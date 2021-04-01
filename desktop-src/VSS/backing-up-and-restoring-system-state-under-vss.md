---
description: Примечание. Этот раздел относится только к Windows Server 2003 R2 и Windows Server 2003 с пакетом обновления 1 (SP1).
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: Резервное копирование и восстановление состояния системы в Windows Server 2003 R2 и Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2fdb50e3f719a5208c2894f5659f927bcc922d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999497"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a><span data-ttu-id="93e4d-103">Резервное копирование и восстановление состояния системы в Windows Server 2003 R2 и Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="93e4d-103">Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1</span></span>

> [!Note]  
> <span data-ttu-id="93e4d-104">Этот раздел относится только к Windows Server 2003 R2 и Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="93e4d-104">This topic only applies to Windows Server 2003 R2 and Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="93e4d-105">Сведения о других версиях операционных систем см. в разделе [резервное копирование и восстановление состояния системы](locating-additional-system-files.md).</span><span class="sxs-lookup"><span data-stu-id="93e4d-105">For information about other operating system versions, see [Backing Up and Restoring System State](locating-additional-system-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="93e4d-106">Корпорация Майкрософт не предоставляет техническую поддержку для разработчиков и ИТ-специалистов по внедрению оперативного восстановления состояния системы в Windows (все выпуски).</span><span class="sxs-lookup"><span data-stu-id="93e4d-106">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span> <span data-ttu-id="93e4d-107">Сведения об использовании интерфейсов API и процедур, предоставляемых корпорацией Майкрософт для внедрения оперативного восстановления состояния системы, см. в разделе Ресурсы сообщества, доступные в [центре сообщества MSDN](https://msdn.microsoft.com/community/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="93e4d-107">For information about using Microsoft-provided APIs and procedures to implement online system state restores, see the community resources available at the [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).</span></span>

 

<span data-ttu-id="93e4d-108">При выполнении резервного копирования или восстановления VSS состояние системы Windows определяется как коллекция из нескольких ключевых элементов операционной системы и их файлов.</span><span class="sxs-lookup"><span data-stu-id="93e4d-108">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="93e4d-109">Эти элементы всегда должны обрабатываться операциями резервного копирования и восстановления как единое целое.</span><span class="sxs-lookup"><span data-stu-id="93e4d-109">These elements should always be treated by backup and restore operations as a unit.</span></span>

<span data-ttu-id="93e4d-110">В Windows Server 2003 R2 и Windows Server 2003 с пакетом обновления 1 (SP1) нет API Windows, предназначенного для обработки этих объектов, поэтому рекомендуется, чтобы у запрашивающих сторон был собственный объект состояния системы, чтобы они могли обрабатывать эти компоненты согласованным образом.</span><span class="sxs-lookup"><span data-stu-id="93e4d-110">In Windows Server 2003 R2 and Windows Server 2003 with SP1, there is no Windows API designed to treat these objects as one, so it is recommended that requesters have their own system state object so that they can process these components in a consistent manner.</span></span>

<span data-ttu-id="93e4d-111">Поскольку служба VSS работает на версиях Windows, где [*Защита системных файлов*](vssgloss-s.md) (WFP) защищает файлы состояния системы от повреждения, для резервного копирования и восстановления состояния системы требуются специальные действия.</span><span class="sxs-lookup"><span data-stu-id="93e4d-111">Because VSS runs on versions of Windows where [*System File Protection*](vssgloss-s.md) (WFP) protects system state files from corruption, special steps are needed to back up and restore system state.</span></span>

<span data-ttu-id="93e4d-112">Состояние системы состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="93e4d-112">System state consists of the following:</span></span>

-   <span data-ttu-id="93e4d-113">Все файлы, защищенные WFP, загрузочные файлы, включая конфигурации NTLDR, нтдетект и счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="93e4d-113">All files protected by WFP, boot files including ntldr, ntdetect, and performance counter configurations</span></span>
-   <span data-ttu-id="93e4d-114">Active Directory (ADSI) (в системах, являющихся контроллерами домена);</span><span class="sxs-lookup"><span data-stu-id="93e4d-114">The Active Directory (ADSI) (on systems that are domain controllers)</span></span>
-   <span data-ttu-id="93e4d-115">Папка системного тома (SYSVOL), которая реплицируется службой репликации файлов (FRS) (в системах, являющихся контроллерами домена).</span><span class="sxs-lookup"><span data-stu-id="93e4d-115">The System Volume Folder (SYSVOL) that is replicated by the File Replication Service (FRS) (on systems that are domain controllers)</span></span>
-   <span data-ttu-id="93e4d-116">Сервер сертификатов (на компьютерах, которые предоставляют центр сертификации)</span><span class="sxs-lookup"><span data-stu-id="93e4d-116">Certificate server (on systems that provide Certification Authority)</span></span>
-   <span data-ttu-id="93e4d-117">База данных кластера (на системах, которые являются узлами кластера Windows)</span><span class="sxs-lookup"><span data-stu-id="93e4d-117">Cluster database (on systems that are a node of a Windows cluster)</span></span>
-   <span data-ttu-id="93e4d-118">Служба реестра</span><span class="sxs-lookup"><span data-stu-id="93e4d-118">Registry service</span></span>
-   <span data-ttu-id="93e4d-119">База данных регистрации классов COM+</span><span class="sxs-lookup"><span data-stu-id="93e4d-119">COM+ class registration database</span></span>

<span data-ttu-id="93e4d-120">Состояние системы можно архивировать в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="93e4d-120">The system state can be backed up in any order.</span></span>

<span data-ttu-id="93e4d-121">Однако при восстановлении состояния системы сначала следует заменить загрузочные файлы и зафиксировать системный раздел (Hive) реестра в качестве завершающего шага процесса и выполнить его в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="93e4d-121">However, the restoration of the system state should replace boot files first and commit the system section (hive) of the registry as a final step in the process, and might occur in the following order:</span></span>

1.  <span data-ttu-id="93e4d-122">Восстановите файлы загрузки.</span><span class="sxs-lookup"><span data-stu-id="93e4d-122">Restore the boot files.</span></span>
2.  <span data-ttu-id="93e4d-123">База данных регистрации классов COM+</span><span class="sxs-lookup"><span data-stu-id="93e4d-123">COM+ class registration database</span></span>
3.  <span data-ttu-id="93e4d-124">Восстановление SYSVOL, сервера сертификатов и баз данных кластера (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="93e4d-124">Restore SYSVOL, Certificate Server, and Cluster databases (if needed).</span></span>
4.  <span data-ttu-id="93e4d-125">Active Directory восстановления (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="93e4d-125">Restore Active Directory (if needed).</span></span>
5.  <span data-ttu-id="93e4d-126">Восстановите реестр.</span><span class="sxs-lookup"><span data-stu-id="93e4d-126">Restore the registry.</span></span>

<span data-ttu-id="93e4d-127">Некоторые системные службы, такие как центр сертификации, имеют традиционные модули записи VSS и следуют алгоритмам резервного копирования и восстановления VSS.</span><span class="sxs-lookup"><span data-stu-id="93e4d-127">Some system services, such as the Certification Authority, have conventional VSS writers and follow the VSS backup and restore algorithms.</span></span> <span data-ttu-id="93e4d-128">Другие, например реестр, нуждаются в пользовательских операциях резервного копирования или восстановления. Дополнительные сведения см. в разделе [пользовательские резервные копии и восстановление](custom-backups-and-restores.md).</span><span class="sxs-lookup"><span data-stu-id="93e4d-128">Others, such as the registry, require custom backup or restore operations; for more information, see [Custom Backups and Restores](custom-backups-and-restores.md).</span></span>

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a><span data-ttu-id="93e4d-129">Резервное копирование и восстановление VSS для загрузочных и системных файлов</span><span class="sxs-lookup"><span data-stu-id="93e4d-129">VSS Backup and Restores of Boot and System Files</span></span>

<span data-ttu-id="93e4d-130">Загрузочный и системный файлы должны быть резервными копиями и восстановлены только как единая сущность.</span><span class="sxs-lookup"><span data-stu-id="93e4d-130">The boot and system files should be backed up and restored only as a single entity.</span></span>

<span data-ttu-id="93e4d-131">Инициатор запроса может безопасно использовать теневые копии этих файлов, а также убедиться, что системный том и загрузочное устройство имеют [*теневое копирование*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="93e4d-131">A requester can safely use shadow-copied versions of these files, and should be sure that the system volume and boot device are [*shadow copied*](vssgloss-s.md).</span></span>

<span data-ttu-id="93e4d-132">Системные и загрузочные файлы включают в себя:</span><span class="sxs-lookup"><span data-stu-id="93e4d-132">The system and boot files include:</span></span>

-   <span data-ttu-id="93e4d-133">Основные загрузочные файлы:</span><span class="sxs-lookup"><span data-stu-id="93e4d-133">The core boot files:</span></span> <dl> <span data-ttu-id="93e4d-134">NtLdr.exe</span><span class="sxs-lookup"><span data-stu-id="93e4d-134">NtLdr.exe</span></span>  
    <span data-ttu-id="93e4d-135">Boot.ini</span><span class="sxs-lookup"><span data-stu-id="93e4d-135">Boot.ini</span></span>  
    <span data-ttu-id="93e4d-136">NtDetect.com</span><span class="sxs-lookup"><span data-stu-id="93e4d-136">NtDetect.com</span></span>  
    <span data-ttu-id="93e4d-137">NtBootDD.sys (при наличии)</span><span class="sxs-lookup"><span data-stu-id="93e4d-137">NtBootDD.sys (if present)</span></span>  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> <span data-ttu-id="93e4d-138">% SystemRoot% \\ system32 \\ катрут \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE}</span><span class="sxs-lookup"><span data-stu-id="93e4d-138">%SystemRoot%\\System32\\CatRoot\\{F750E6C3-38EE-11D1-85E5-00C04FC295EE}</span></span> </dl><span data-ttu-id="93e4d-139">
-   Файлы конфигурации счетчиков производительности для всех файлов, защищенных с помощью [\*защиты системных файлов*](vssgloss-s.md) и перечисленных [\*\*сфкжетнекстпротектедфиле**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (см. раздел операции восстановления из защищенных файлов WFP в VSS) -   :</span><span class="sxs-lookup"><span data-stu-id="93e4d-139">
-   All files protected by [\*System File Protection*](vssgloss-s.md) and enumerated by [\*\*SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (see VSS Restore Operations of WFP Protected Files) -   The Performance Counter Configuration files:</span></span> <dl> <span data-ttu-id="93e4d-140">% SystemRoot% \\ system32 \\ Perf? 00?. включая</span><span class="sxs-lookup"><span data-stu-id="93e4d-140">%SystemRoot%\\System32\\Perf?00?.dat</span></span>  
    <span data-ttu-id="93e4d-141">% SystemRoot% \\ system32 \\ Perf? 00?. BAK</span><span class="sxs-lookup"><span data-stu-id="93e4d-141">%SystemRoot%\\System32\\Perf?00?.bak</span></span> </dl><span data-ttu-id="93e4d-142">
-   Если этот параметр присутствует, файл метабазы IIS должен быть включен в операции резервного копирования и восстановления, так как он содержит состояние, используемое Microsoft Exchange и другими сетевыми приложениями.</span><span class="sxs-lookup"><span data-stu-id="93e4d-142">
-   If present, the Internet Information Server (IIS) metabase file should be included in backup and restore operations because it contains state that is used by Microsoft Exchange and other network applications.</span></span> <span data-ttu-id="93e4d-143">Этот файл находится в папке</span><span class="sxs-lookup"><span data-stu-id="93e4d-143">This file can be found at:</span></span> <dl> <span data-ttu-id="93e4d-144">% SystemRoot% \\ system32 \\ InetSrv \\ MetaBase. bin</span><span class="sxs-lookup"><span data-stu-id="93e4d-144">%SystemRoot%\\System32\\InetSrv\\Metabase.bin</span></span> </dl><span data-ttu-id="93e4d-145">
-   Если создается резервная копия файла метабазы IIS, то ключи, позволяющие приложениям считывать определенные зашифрованные записи, должны восстанавливаться как часть состояния системы.</span><span class="sxs-lookup"><span data-stu-id="93e4d-145">
-   If the IIS metabase file is backed up, keys to enable applications to read certain encrypted entries should be restored as part of the system state.</span></span> <span data-ttu-id="93e4d-146">Файлы можно найти в разделе:</span><span class="sxs-lookup"><span data-stu-id="93e4d-146">The files can be found under:</span></span> <dl> <span data-ttu-id="93e4d-147">% SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*</span><span class="sxs-lookup"><span data-stu-id="93e4d-147">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
    <span data-ttu-id="93e4d-148">% AllUsersProfile% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="93e4d-148">%AllUsersProfile%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span> </dl><span data-ttu-id="93e4d-149">
-При резервном копировании загрузочных и системных файлов может потребоваться определить загрузочное устройство DOS, выполнив следующие действия. 1. найдите системный раздел в разделе "Установка системпартитион \*\*\_ локального \_ компьютера\*\*" раздела hKey \\  \\  \\ .</span><span class="sxs-lookup"><span data-stu-id="93e4d-149">
-   When backing up boot and system files, it may become necessary to determine the DOS boot device by doing the following: 1.  Find the system partition under \*\*HKEY\_LOCAL\_MACHINE\*\*\\*\*System\*\*\\*\*Setup\*\*\\*\*SystemPartition\**.</span></span>
    <span data-ttu-id="93e4d-150">2.  Передать переменную корневой среды системы (% SystemRoot%) в Диспетчер подключений, чтобы получить имя устройства NT.</span><span class="sxs-lookup"><span data-stu-id="93e4d-150">2.  Pass the System Root environment variable (%SystemRoot%) to the mount manager to obtain the NT device name.</span></span>

## <a name="vss-restore-operations-of-wfp-protected-files"></a><span data-ttu-id="93e4d-151">Операции восстановления VSS для защищенных файлов WFP</span><span class="sxs-lookup"><span data-stu-id="93e4d-151">VSS Restore Operations of WFP Protected Files</span></span>

<span data-ttu-id="93e4d-152">Служба WFP предназначена для предотвращения случайной или поэтапной замены системных файлов.</span><span class="sxs-lookup"><span data-stu-id="93e4d-152">The WFP service is designed to prevent accidental or piecemeal replacement of system files.</span></span> <span data-ttu-id="93e4d-153">Поэтому необходимо выполнить специальные действия по восстановлению данных WFP.</span><span class="sxs-lookup"><span data-stu-id="93e4d-153">Therefore, special steps need to be undertaken to restore WFP data.</span></span>

<span data-ttu-id="93e4d-154">Означает, что модуль записи WFP должен указать метод VSS рме RESTORE при **\_ \_ \_ \_ перезагрузке** при определении его документа метаданных модуля записи.</span><span class="sxs-lookup"><span data-stu-id="93e4d-154">The means the WFP writer should specify the **VSS\_RME\_RESTORE\_AT\_REBOOT** restore method when defining its Writer Metadata Document.</span></span> <span data-ttu-id="93e4d-155">Если инициатор запроса определяет, что модуль записи WFP не смог указать этот метод Restore, он указывает на ошибку модуля записи.</span><span class="sxs-lookup"><span data-stu-id="93e4d-155">If a requester determines that the WFP writer has failed to specify this restore method, it indicates a writer error.</span></span>

<span data-ttu-id="93e4d-156">Чтобы заменить системные файлы, запрашивающий объект должен реализовать метод Restore **\_ рме \_ RESTORE в службе VSS \_ при \_ перезагрузке** с помощью функции Win32 [**мовефиликс**](/windows/win32/api/winbase/nf-winbase-movefileexa) с параметром **MOVEFILE \_ delay \_ до \_ reboot** .</span><span class="sxs-lookup"><span data-stu-id="93e4d-156">A requester should implement a restore method of **VSS\_RME\_RESTORE\_AT\_REBOOT** using the Win32 function [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) with the **MOVEFILE\_DELAY\_UNTIL\_REBOOT** parameter to replace system files.</span></span> <span data-ttu-id="93e4d-157">Восстановленные файлы не копируются в реальные каталоги системных файлов до перезагрузки системы.</span><span class="sxs-lookup"><span data-stu-id="93e4d-157">The restored files are not copied into the actual system file directories until after system reboot.</span></span> <span data-ttu-id="93e4d-158">Перезапись защищенных системных файлов выполняется только в том случае, если значение следующей записи реестра **reg \_ Word** равно 1:</span><span class="sxs-lookup"><span data-stu-id="93e4d-158">The overwriting of protected system files will occur only if the value of the following **REG\_WORD** registry entry is set to 1:</span></span>

<span data-ttu-id="93e4d-159">**HKey \_ Система локального \_ компьютера** \\  \\ **CurrentControlSet** \\  \\ **диспетчер сеансов** управления \\ **алловпротектедренамес** = 1</span><span class="sxs-lookup"><span data-stu-id="93e4d-159">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Session Manager**\\**AllowProtectedRenames** = 1</span></span>

<span data-ttu-id="93e4d-160">Это значение должно быть задано до любой загрузки, в которой защищенные файлы должны быть заменены через [**мовефиликс**](/windows/win32/api/winbase/nf-winbase-movefileexa) и удалены после перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="93e4d-160">This value must be set before any boot where protected files are to be replaced via [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) and is deleted after reboot.</span></span>

<span data-ttu-id="93e4d-161">Кроме того, необходимо создать резервную копию и восстановить каталог системы Dllcache с помощью резервного копирования и восстановления загрузочного тома и найти его, изучив запись реестра **\_ \_ SZ Expand** :</span><span class="sxs-lookup"><span data-stu-id="93e4d-161">The system dllcache directory should also be backed up or restored, with boot volume backup and restore, and is located by examining the **REG\_EXPAND\_SZ** registry entry:</span></span>

<span data-ttu-id="93e4d-162">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **сфкдллкаче**</span><span class="sxs-lookup"><span data-stu-id="93e4d-162">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**SfcDllCache**</span></span><dl> <dt>

                  Data type
</dt> <dd>                  <span data-ttu-id="93e4d-163">\_распаковать \_ SZ</span><span class="sxs-lookup"><span data-stu-id="93e4d-163">REG\_EXPAND\_SZ</span></span></dd> </dl>

<span data-ttu-id="93e4d-164">Содержимое каталога системы Dllcache перестраивается с помощью средства проверки системных файлов (SFC) из командной строки.</span><span class="sxs-lookup"><span data-stu-id="93e4d-164">The contents of the system dllcache directory are rebuilt by using the System File Checker (SFC) from the command prompt:</span></span>

-   <span data-ttu-id="93e4d-165">Параметр **/сканонце** сканирует все защищенные файлы при следующей загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="93e4d-165">The **/SCANONCE** option scans all protected files at the next system boot.</span></span>
-   <span data-ttu-id="93e4d-166">Параметр **/scannow** сканирует все защищенные файлы немедленно.</span><span class="sxs-lookup"><span data-stu-id="93e4d-166">The **/SCANNOW** option scans all protected files immediately.</span></span>

<span data-ttu-id="93e4d-167">Все защищенные файлы будут просканированы, а все недопустимые версии будут заменены как в каталоге, так и в расположении Dllcache.</span><span class="sxs-lookup"><span data-stu-id="93e4d-167">All protected files will be scanned, and any versions that are not valid will be replaced in both the directory and dllcache location.</span></span>

<span data-ttu-id="93e4d-168">Существует четыре файла, которые являются частью платформы WFP и не могут быть восстановлены с помощью файлов WFP:</span><span class="sxs-lookup"><span data-stu-id="93e4d-168">There are four files that are part of the WFP that cannot be restored with the WFP files:</span></span>

<dl> <span data-ttu-id="93e4d-169">Ctl3dv2.dll</span><span class="sxs-lookup"><span data-stu-id="93e4d-169">Ctl3dv2.dll</span></span>  
<span data-ttu-id="93e4d-170">DtcSetup.exe</span><span class="sxs-lookup"><span data-stu-id="93e4d-170">DtcSetup.exe</span></span>  
<span data-ttu-id="93e4d-171">NtDll.dll</span><span class="sxs-lookup"><span data-stu-id="93e4d-171">NtDll.dll</span></span>  
<span data-ttu-id="93e4d-172">Smss.exe</span><span class="sxs-lookup"><span data-stu-id="93e4d-172">Smss.exe</span></span>  
</dl>

<span data-ttu-id="93e4d-173">Эти файлы помогают в процессе восстановления файлов WFP, поэтому существует циклическая зависимость.</span><span class="sxs-lookup"><span data-stu-id="93e4d-173">These files help in the process of restoring the WFP files and as such there is a circular dependency.</span></span> <span data-ttu-id="93e4d-174">Сейчас нет способа восстановить эти файлы, кроме переустановки Windows.</span><span class="sxs-lookup"><span data-stu-id="93e4d-174">Currently, there is no way to restore these files except to reinstall Windows.</span></span>

 

 
