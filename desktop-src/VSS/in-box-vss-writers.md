---
description: Операционная система Windows включает набор модулей записи VSS, которые отвечают за перечисление данных, необходимых для различных функций Windows. Они называются &\# 0034; встроенными&\# 0034; модулями записи.
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: Встроенные модули записи VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc256cfe72f3653d4af282148c87c2b45bcac51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692913"
---
# <a name="in-box-vss-writers"></a><span data-ttu-id="8f942-104">Встроенные модули записи VSS</span><span class="sxs-lookup"><span data-stu-id="8f942-104">In-Box VSS Writers</span></span>

<span data-ttu-id="8f942-105">Операционная система Windows включает набор модулей записи VSS, которые отвечают за перечисление данных, необходимых для различных функций Windows.</span><span class="sxs-lookup"><span data-stu-id="8f942-105">The Windows operating system includes a set of VSS writers that are responsible for enumerating the data that is required by various Windows features.</span></span> <span data-ttu-id="8f942-106">Они называются встроенными модулями записи.</span><span class="sxs-lookup"><span data-stu-id="8f942-106">These are referred to as "in-box" writers.</span></span>

> [!Note]  
> <span data-ttu-id="8f942-107">Модуль записи MSDE в Box недоступен в Windows Vista, Windows Server 2008 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8f942-107">The MSDE in-box writer is not available in Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="8f942-108">Вместо этого для резервного копирования SQL Server баз данных следует использовать модуль записи SQL.</span><span class="sxs-lookup"><span data-stu-id="8f942-108">Instead, the SQL Writer should be used to back up SQL Server databases.</span></span> <span data-ttu-id="8f942-109">В Windows Vista, Windows Server 2008 и более поздних версиях поддерживаются только SQL Server 2005 с пакетом обновления 2 (SP2) и выше.</span><span class="sxs-lookup"><span data-stu-id="8f942-109">Only SQL Server 2005 SP2 and later are supported on Windows Vista, Windows Server 2008, and later.</span></span>

 

-   [<span data-ttu-id="8f942-110">Модуль записи VSS служб домен Active Directory Services (NTDS)</span><span class="sxs-lookup"><span data-stu-id="8f942-110">Active Directory Domain Services (NTDS) VSS Writer</span></span>](#active-directory-domain-services-ntds-vss-writer)
-   [<span data-ttu-id="8f942-111">Модуль записи службы федерации Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="8f942-111">Active Directory Federation Services Writer</span></span>](#active-directory-federation-services-writer)
-   [<span data-ttu-id="8f942-112">Модуль записи VSS службы Active Directory облегченного доступа к каталогам (LDS)</span><span class="sxs-lookup"><span data-stu-id="8f942-112">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [<span data-ttu-id="8f942-113">Модуль записи службы Active Directory Rights Management (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="8f942-113">Active Directory Rights Management Services (AD RMS) Writer</span></span>](#active-directory-rights-management-services-ad-rms-writer)
-   [<span data-ttu-id="8f942-114">Средство записи автоматического восстановления системы (ASR)</span><span class="sxs-lookup"><span data-stu-id="8f942-114">Automated System Recovery (ASR) Writer</span></span>](#automated-system-recovery-asr-writer)
-   [<span data-ttu-id="8f942-115">Модуль записи фоновая интеллектуальная служба передачи (BITS)</span><span class="sxs-lookup"><span data-stu-id="8f942-115">Background Intelligent Transfer Service (BITS) Writer</span></span>](#background-intelligent-transfer-service-bits-writer)
-   [<span data-ttu-id="8f942-116">Модуль записи центра сертификации</span><span class="sxs-lookup"><span data-stu-id="8f942-116">Certificate Authority Writer</span></span>](#certificate-authority-writer)
-   [<span data-ttu-id="8f942-117">Модуль записи службы кластеров</span><span class="sxs-lookup"><span data-stu-id="8f942-117">Cluster Service Writer</span></span>](#cluster-service-writer)
-   [<span data-ttu-id="8f942-118">Модуль записи VSS общий том кластера (CSV)</span><span class="sxs-lookup"><span data-stu-id="8f942-118">Cluster Shared Volume (CSV) VSS Writer</span></span>](#cluster-shared-volume-csv-vss-writer)
-   [<span data-ttu-id="8f942-119">Модуль записи базы данных регистрации классов COM+</span><span class="sxs-lookup"><span data-stu-id="8f942-119">COM+ Class Registration Database Writer</span></span>](#com-class-registration-database-writer)
-   [<span data-ttu-id="8f942-120">Модуль записи дедупликации данных</span><span class="sxs-lookup"><span data-stu-id="8f942-120">Data Deduplication Writer</span></span>](#data-deduplication-writer)
-   [<span data-ttu-id="8f942-121">Служба репликации распределенной файловой системы (DSFR).</span><span class="sxs-lookup"><span data-stu-id="8f942-121">Distributed File System Replication (DFSR)</span></span>](#distributed-file-system-replication-dfsr)
-   [<span data-ttu-id="8f942-122">Модуль записи протокола DHCP</span><span class="sxs-lookup"><span data-stu-id="8f942-122">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>](#dynamic-host-configuration-protocol-dhcp-writer)
-   [<span data-ttu-id="8f942-123">Служба репликации файлов (FRS)</span><span class="sxs-lookup"><span data-stu-id="8f942-123">File Replication Service (FRS)</span></span>](#file-replication-service-frs)
-   [<span data-ttu-id="8f942-124">Модуль записи диспетчер ресурсов файлового сервера (FSRM)</span><span class="sxs-lookup"><span data-stu-id="8f942-124">File Server Resource Manager (FSRM) Writer</span></span>](#file-server-resource-manager-fsrm-writer)
-   [<span data-ttu-id="8f942-125">Модуль записи Hyper-V</span><span class="sxs-lookup"><span data-stu-id="8f942-125">Hyper-V Writer</span></span>](#hyper-v-writer)
-   [<span data-ttu-id="8f942-126">Модуль записи конфигурации IIS</span><span class="sxs-lookup"><span data-stu-id="8f942-126">IIS Configuration Writer</span></span>](#iis-configuration-writer)
-   [<span data-ttu-id="8f942-127">Модуль записи метабазы IIS</span><span class="sxs-lookup"><span data-stu-id="8f942-127">IIS Metabase Writer</span></span>](#iis-metabase-writer)
-   [<span data-ttu-id="8f942-128">Модуль записи очереди сообщений Майкрософт (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="8f942-128">Microsoft Message Queuing (MSMQ) Writer</span></span>](#microsoft-message-queuing-msmq-writer)
-   [<span data-ttu-id="8f942-129">Модуль записи службы MSSearch</span><span class="sxs-lookup"><span data-stu-id="8f942-129">MSSearch Service Writer</span></span>](#mssearch-service-writer)
-   [<span data-ttu-id="8f942-130">Модуль записи VSS NPS</span><span class="sxs-lookup"><span data-stu-id="8f942-130">NPS VSS Writer</span></span>](#nps-vss-writer)
-   [<span data-ttu-id="8f942-131">Модуль записи счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="8f942-131">Performance Counters Writer</span></span>](#performance-counters-writer)
-   [<span data-ttu-id="8f942-132">Модуль записи реестра</span><span class="sxs-lookup"><span data-stu-id="8f942-132">Registry Writer</span></span>](#registry-writer)
-   [<span data-ttu-id="8f942-133">Модуль записи VSS шлюза службы удаленных рабочих столов (службы терминалов)</span><span class="sxs-lookup"><span data-stu-id="8f942-133">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [<span data-ttu-id="8f942-134">Модуль записи VSS лицензирования службы удаленных рабочих столов (службы терминалов)</span><span class="sxs-lookup"><span data-stu-id="8f942-134">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [<span data-ttu-id="8f942-135">Модуль записи оптимизации теневого копирования</span><span class="sxs-lookup"><span data-stu-id="8f942-135">Shadow Copy Optimization Writer</span></span>](#shadow-copy-optimization-writer)
-   [<span data-ttu-id="8f942-136">Средство записи общего доступа к службе синхронизации</span><span class="sxs-lookup"><span data-stu-id="8f942-136">Sync Share Service Writer</span></span>](#sync-share-service-writer)
-   [<span data-ttu-id="8f942-137">Модуль записи системы</span><span class="sxs-lookup"><span data-stu-id="8f942-137">System Writer</span></span>](#system-writer)
-   [<span data-ttu-id="8f942-138">Модуль записи планировщик задач</span><span class="sxs-lookup"><span data-stu-id="8f942-138">Task Scheduler Writer</span></span>](#task-scheduler-writer)
-   [<span data-ttu-id="8f942-139">Модуль записи хранилища метаданных VSS</span><span class="sxs-lookup"><span data-stu-id="8f942-139">VSS Metadata Store Writer</span></span>](#vss-metadata-store-writer)
-   [<span data-ttu-id="8f942-140">Модуль записи служб развертывания Windows (WDS)</span><span class="sxs-lookup"><span data-stu-id="8f942-140">Windows Deployment Services (WDS) Writer</span></span>](#windows-deployment-services-wds-writer)
-   [<span data-ttu-id="8f942-141">Модуль записи внутренней базы данных Windows (WID)</span><span class="sxs-lookup"><span data-stu-id="8f942-141">Windows Internal Database (WID) Writer</span></span>](#windows-internal-database-wid-writer)
-   [<span data-ttu-id="8f942-142">Модуль записи службы Windows Internet Name Service (WINS)</span><span class="sxs-lookup"><span data-stu-id="8f942-142">Windows Internet Name Service (WINS) Writer</span></span>](#windows-internet-name-service-wins-writer)
-   [<span data-ttu-id="8f942-143">Модуль записи WMI</span><span class="sxs-lookup"><span data-stu-id="8f942-143">WMI Writer</span></span>](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a><span data-ttu-id="8f942-144">Модуль записи VSS служб домен Active Directory Services (NTDS)</span><span class="sxs-lookup"><span data-stu-id="8f942-144">Active Directory Domain Services (NTDS) VSS Writer</span></span>

<span data-ttu-id="8f942-145">Этот модуль записи сообщает файл базы данных NTDS (Ntds. dit) и связанные файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="8f942-145">This writer reports the NTDS database file (ntds.dit) and the associated log files.</span></span> <span data-ttu-id="8f942-146">Эти файлы необходимы для правильного восстановления Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f942-146">These files are required to restore the Active Directory correctly.</span></span>

<span data-ttu-id="8f942-147">В каждом контроллере домена имеется только один файл Ntds. dit, который указывается в метаданных модуля записи, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="8f942-147">There is only one ntds.dit file per domain controller, and it is reported in the writer metadata as in the following example:</span></span>

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

<span data-ttu-id="8f942-148">Ниже приведен пример, в котором показано, как вывести список компонентов в метаданных модуля записи:</span><span class="sxs-lookup"><span data-stu-id="8f942-148">Here is an example that shows how to list components in the writer's metadata:</span></span>

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Windows_NTDS" 
                     componentName="ntds" 
                     caption="" restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/> 
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

<span data-ttu-id="8f942-149">Во время резервного копирования модуль записи задает срок действия резервной копии в метаданных резервной копии модуля записи.</span><span class="sxs-lookup"><span data-stu-id="8f942-149">At backup time, the writer sets the backup expiration time in the writer's backup metadata.</span></span> <span data-ttu-id="8f942-150">Запрашивающие стороны должны получить эти метаданные с помощью [**ивсскомпонент:: жетбаккупметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) , чтобы определить, истек ли срок действия базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f942-150">Requesters should retrieve this metadata by using [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) to determine whether the database has expired.</span></span> <span data-ttu-id="8f942-151">Невозможно восстановить базы данных с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="8f942-151">Expired databases cannot be restored.</span></span>

<span data-ttu-id="8f942-152">Если компьютер, содержащий базу данных NTDS, является контроллером домена, то приложение резервного копирования всегда должно выполнять резервное копирование состояния системы на всех томах, содержащих критически важные сведения о состоянии системы.</span><span class="sxs-lookup"><span data-stu-id="8f942-152">If the computer that contains the NTDS database is a domain controller, the backup application should always perform a system state backup across all volumes containing critical system state information.</span></span> <span data-ttu-id="8f942-153">Во время восстановления приложение должно сначала перезагрузить компьютер в режиме восстановления служб каталогов, а затем выполнить восстановление состояния системы.</span><span class="sxs-lookup"><span data-stu-id="8f942-153">At restore time, the application should first restart the computer in Directory Services Restore Mode and then perform a system state restore.</span></span>

<span data-ttu-id="8f942-154">Строка имени модуля записи для этого модуля записи — "NTDS".</span><span class="sxs-lookup"><span data-stu-id="8f942-154">The writer name string for this writer is "NTDS".</span></span>

<span data-ttu-id="8f942-155">Идентификатор модуля записи для этого модуля записи — B2014C9E-8711-4C5C-A5A9-3CF384484757.</span><span class="sxs-lookup"><span data-stu-id="8f942-155">The writer ID for this writer is B2014C9E-8711-4C5C-A5A9-3CF384484757.</span></span>

## <a name="active-directory-federation-services-writer"></a><span data-ttu-id="8f942-156">Модуль записи службы федерации Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="8f942-156">Active Directory Federation Services Writer</span></span>

<span data-ttu-id="8f942-157">Этот модуль записи сообщает о файлах данных службы федерации Active Directory (AD FS) (ADFS).</span><span class="sxs-lookup"><span data-stu-id="8f942-157">This writer reports the Active Directory Federation Services (ADFS) data files.</span></span>

<span data-ttu-id="8f942-158">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-158">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-159">Строка имени модуля записи для этого модуля записи — "модуль записи VSS ADFS".</span><span class="sxs-lookup"><span data-stu-id="8f942-159">The writer name string for this writer is "ADFS VSS Writer".</span></span>

<span data-ttu-id="8f942-160">Идентификатор модуля записи для этого модуля записи — 772C45F8-AE01-4F94-940C-94961864ACAD.</span><span class="sxs-lookup"><span data-stu-id="8f942-160">The writer ID for this writer is 772C45F8-AE01-4F94-940C-94961864ACAD.</span></span>

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a><span data-ttu-id="8f942-161">Модуль записи VSS службы Active Directory облегченного доступа к каталогам (LDS)</span><span class="sxs-lookup"><span data-stu-id="8f942-161">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>

<span data-ttu-id="8f942-162">Этот модуль записи сообщает файл базы данных ADAM (адамнтдс. dit) и связанные файлы журнала для каждого экземпляра в% Program Files% \\ Microsoft ADAM \\ instance *n* \\ Data, где *N* — номер экземпляра ADAM.</span><span class="sxs-lookup"><span data-stu-id="8f942-162">This writer reports the ADAM database file (adamntds.dit) and the associated log files for each instance in %program files%\\Microsoft ADAM\\instance *N*\\data, where *N* is the ADAM instance number.</span></span> <span data-ttu-id="8f942-163">Эти файлы журналов базы данных необходимы для восстановления экземпляров ADAM.</span><span class="sxs-lookup"><span data-stu-id="8f942-163">These database log files are required to restore ADAM instances.</span></span>

<span data-ttu-id="8f942-164">**Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-164">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-165">Ниже приведен пример, в котором показано, как вывести список компонентов в метаданных модуля записи:</span><span class="sxs-lookup"><span data-stu-id="8f942-165">Here is an example that shows how to list components in the writer's metadata:</span></span>

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Program Files_Microsoft ADAM_instance1_data" 
                     componentName="adamntds" 
                     caption="" 
                     restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="adamntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

<span data-ttu-id="8f942-166">Во время резервного копирования модуль записи задает срок действия резервной копии в метаданных резервной копии.</span><span class="sxs-lookup"><span data-stu-id="8f942-166">At backup time, the writer sets the backup expiration time in the backup metadata.</span></span> <span data-ttu-id="8f942-167">Приложения резервного копирования должны извлекать эти метаданные с помощью метода [**ивсскомпонент:: жетбаккупметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) , чтобы определить, истек ли срок действия базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f942-167">Backup applications should retrieve this metadata by using the [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) method to determine whether the database has expired.</span></span> <span data-ttu-id="8f942-168">Невозможно восстановить базы данных с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="8f942-168">Expired databases cannot be restored.</span></span>

<span data-ttu-id="8f942-169">Строка имени модуля записи для этого модуля записи — «Адам (экземпляр *N*) Writer», где *N* — это номер экземпляра ADAM, например «Адам (instance1) WRITER», «ADAM (Instance2) Writer» и т. д.</span><span class="sxs-lookup"><span data-stu-id="8f942-169">The writer name string for this writer is "ADAM (instance *N*) Writer", where *N* is the ADAM instance number, for example, "ADAM (instance1) Writer", "ADAM (instance2) Writer", and so on.</span></span>

<span data-ttu-id="8f942-170">Идентификатор модуля записи для этого модуля записи — DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span><span class="sxs-lookup"><span data-stu-id="8f942-170">The writer ID for this writer is DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span></span> <span data-ttu-id="8f942-171">Этот идентификатор записи одинаков для всех экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8f942-171">This writer ID is the same for all instances.</span></span>

## <a name="active-directory-rights-management-services-ad-rms-writer"></a><span data-ttu-id="8f942-172">Модуль записи службы Active Directory Rights Management (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="8f942-172">Active Directory Rights Management Services (AD RMS) Writer</span></span>

<span data-ttu-id="8f942-173">Этот модуль записи сообщает о файлах данных Active Directory Rights Management Service (AD RMS).</span><span class="sxs-lookup"><span data-stu-id="8f942-173">This writer reports the Active Directory Rights Management Service (AD RMS) data files.</span></span>

<span data-ttu-id="8f942-174">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-174">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-175">Строка имени модуля записи для этого модуля записи — "AD RMS Writer".</span><span class="sxs-lookup"><span data-stu-id="8f942-175">The writer name string for this writer is "AD RMS Writer".</span></span>

<span data-ttu-id="8f942-176">Идентификатор модуля записи для этого модуля записи — 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span><span class="sxs-lookup"><span data-stu-id="8f942-176">The writer ID for this writer is 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span></span>

## <a name="automated-system-recovery-asr-writer"></a><span data-ttu-id="8f942-177">Средство записи автоматического восстановления системы (ASR)</span><span class="sxs-lookup"><span data-stu-id="8f942-177">Automated System Recovery (ASR) Writer</span></span>

<span data-ttu-id="8f942-178">Модуль записи ASR сохраняет конфигурацию дисков в системе.</span><span class="sxs-lookup"><span data-stu-id="8f942-178">The ASR writer stores the configuration of disks on the system.</span></span> <span data-ttu-id="8f942-179">Этот модуль записи сообщает о базе данных конфигурации загрузки (BCD) и также отвечает за отключение куста реестра, представляющего BCD во время создания теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="8f942-179">This writer reports the Boot Configuration Database (BCD) and is also responsible for dismounting the registry hive that represents the BCD during shadow copy creation.</span></span> <span data-ttu-id="8f942-180">Модуль записи ASR должен включаться в любые резервные копии, необходимые для восстановления исходного состояния системы.</span><span class="sxs-lookup"><span data-stu-id="8f942-180">The ASR writer must be included in any backups required for bare-metal recovery.</span></span> <span data-ttu-id="8f942-181">Дополнительные сведения о ASR см. в разделе [Использование автоматического восстановления системы VSS для аварийного восстановления](using-vss-automated-system-recovery-for-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="8f942-181">For more information about ASR, see [Using VSS Automated System Recovery for Disaster Recovery](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span>

<span data-ttu-id="8f942-182">**Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-182">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-183">Строка имени модуля записи для этого модуля записи: "модуль записи ASR".</span><span class="sxs-lookup"><span data-stu-id="8f942-183">The writer name string for this writer is "ASR Writer".</span></span>

<span data-ttu-id="8f942-184">Идентификатор модуля записи для модуля записи ASR — BE000CBE-11FE-4426-9C58-531AA6355FC4.</span><span class="sxs-lookup"><span data-stu-id="8f942-184">The writer ID for the ASR writer is BE000CBE-11FE-4426-9C58-531AA6355FC4.</span></span>

## <a name="background-intelligent-transfer-service-bits-writer"></a><span data-ttu-id="8f942-185">Модуль записи фоновая интеллектуальная служба передачи (BITS)</span><span class="sxs-lookup"><span data-stu-id="8f942-185">Background Intelligent Transfer Service (BITS) Writer</span></span>

<span data-ttu-id="8f942-186">Модуль записи BITS использует раздел реестра **филесноттобаккуп** для исключения файлов из папки кэша BITS.</span><span class="sxs-lookup"><span data-stu-id="8f942-186">The BITS writer uses the **FilesNotToBackup** registry key to exclude files from the BITS cache folder.</span></span> <span data-ttu-id="8f942-187">Расположение кэша по умолчанию:% AllUsersProfile \\ % \\ \\ Кэш загрузчика сети Microsoft \\ .</span><span class="sxs-lookup"><span data-stu-id="8f942-187">The default cache location is %AllUsersProfile%\\Microsoft\\Network\\Downloader\\Cache.</span></span>

<span data-ttu-id="8f942-188">**Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-188">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-189">Кроме того, модуль записи BITS исключает из резервного копирования следующие файлы: файлы состояния BITS (qmgr0. dat и qmgr1. dat), файл журнала отладки BITS и файлы, частично Скачанные в БИТАХ.</span><span class="sxs-lookup"><span data-stu-id="8f942-189">In addition, the BITS writer excludes the following files from backup: the BITS state files (qmgr0.dat and qmgr1.dat), the BITS debug log file, and BITS partially downloaded files.</span></span>

<span data-ttu-id="8f942-190">Если файл назначения загрузки BITS является SMB-файлом, учетная запись клиента должна иметь доверительные отношения с сервером, иначе резервное копирование может завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8f942-190">If the BITS download destination file is an SMB file, the client account must have a trust relationship to the server, or else backups may fail.</span></span>

<span data-ttu-id="8f942-191">Строка имени модуля записи для этого модуля записи: "модуль записи BITS".</span><span class="sxs-lookup"><span data-stu-id="8f942-191">The writer name string for this writer is "BITS Writer".</span></span>

<span data-ttu-id="8f942-192">Идентификатор модуля записи для модуля записи BITS — 4969D978-BE47-48B0-B100-F328F07AC1E0.</span><span class="sxs-lookup"><span data-stu-id="8f942-192">The writer ID for the BITS writer is 4969D978-BE47-48B0-B100-F328F07AC1E0.</span></span>

## <a name="certificate-authority-writer"></a><span data-ttu-id="8f942-193">Модуль записи центра сертификации</span><span class="sxs-lookup"><span data-stu-id="8f942-193">Certificate Authority Writer</span></span>

<span data-ttu-id="8f942-194">Этот модуль записи отвечает за перечисление файлов данных для сервера сертификатов.</span><span class="sxs-lookup"><span data-stu-id="8f942-194">This writer is responsible for enumerating the data files for the Certificate Server.</span></span>

<span data-ttu-id="8f942-195">Строка имени модуля записи для этого модуля записи — "центр сертификации".</span><span class="sxs-lookup"><span data-stu-id="8f942-195">The writer name string for this writer is "Certificate Authority".</span></span>

<span data-ttu-id="8f942-196">**Windows XP:** Строка имени модуля записи для этого модуля записи — "модуль записи сервера сертификатов".</span><span class="sxs-lookup"><span data-stu-id="8f942-196">**Windows XP:** The writer name string for this writer is "Certificate Server Writer".</span></span>

<span data-ttu-id="8f942-197">Идентификатор модуля записи — 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span><span class="sxs-lookup"><span data-stu-id="8f942-197">The writer ID for the writer is 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span></span>

## <a name="cluster-service-writer"></a><span data-ttu-id="8f942-198">Модуль записи службы кластеров</span><span class="sxs-lookup"><span data-stu-id="8f942-198">Cluster Service Writer</span></span>

<span data-ttu-id="8f942-199">Модуль записи VSS службы кластеров описан в документации по API [службы кластеров](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) .</span><span class="sxs-lookup"><span data-stu-id="8f942-199">The Cluster Service VSS writer is documented in the [Cluster Service](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) API documentation.</span></span>

<span data-ttu-id="8f942-200">Windows **Vista, Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается до Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f942-200">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with Service Pack 1 (SP1) and Windows Server 2008.</span></span>

## <a name="cluster-shared-volume-csv-vss-writer"></a><span data-ttu-id="8f942-201">Модуль записи VSS общий том кластера (CSV)</span><span class="sxs-lookup"><span data-stu-id="8f942-201">Cluster Shared Volume (CSV) VSS Writer</span></span>

<span data-ttu-id="8f942-202">Этот модуль записи сообщает о файлах данных общий том кластера (CSV).</span><span class="sxs-lookup"><span data-stu-id="8f942-202">This writer reports the Cluster Shared Volume (CSV) data files.</span></span> <span data-ttu-id="8f942-203">Этот модуль записи является встроенным средством записи для версий операционной системы Windows Server; Он не поставляется в клиенте Windows.</span><span class="sxs-lookup"><span data-stu-id="8f942-203">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8f942-204">**Windows server 2008 R2, Windows server 2008 и Windows server 2003:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-204">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-205">Строка имени модуля записи для этого модуля записи: "общий том кластера модуля записи VSS".</span><span class="sxs-lookup"><span data-stu-id="8f942-205">The writer name string for this writer is "Cluster Shared Volume VSS Writer".</span></span>

<span data-ttu-id="8f942-206">Идентификатор модуля записи — 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span><span class="sxs-lookup"><span data-stu-id="8f942-206">The writer ID for the writer is 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span></span>

## <a name="com-class-registration-database-writer"></a><span data-ttu-id="8f942-207">Модуль записи базы данных регистрации классов COM+</span><span class="sxs-lookup"><span data-stu-id="8f942-207">COM+ Class Registration Database Writer</span></span>

<span data-ttu-id="8f942-208">Этот модуль записи отвечает за содержимое каталога регистрации% SystemRoot% \\ .</span><span class="sxs-lookup"><span data-stu-id="8f942-208">This writer is responsible for the contents of the %SystemRoot%\\Registration directory.</span></span> <span data-ttu-id="8f942-209">Каталог COM+ — это файл в регистрации% SystemRoot% \\ с именем, которое соответствует шаблону R *XXXXXXXXXXXX*. распределения, где *XXXXXXXXXXXX* — 12-разрядное шестнадцатеричное число.</span><span class="sxs-lookup"><span data-stu-id="8f942-209">The COM+ catalog is a file in %SystemRoot%\\Registration with a name that follows the pattern R *xxxxxxxxxxxx*.clb, where *xxxxxxxxxxxx* is a 12-digit hexadecimal number.</span></span> <span data-ttu-id="8f942-210">Возможно наличие нескольких таких файлов, если на компьютере настроены приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="8f942-210">There can potentially be multiple such files if COM+ applications have been configured on the computer.</span></span> <span data-ttu-id="8f942-211">Файл, содержащий текущий каталог COM+, является файлом с самым большим значением *XXXXXXXXXXXX*.</span><span class="sxs-lookup"><span data-stu-id="8f942-211">The file that contains the current COM+ catalog is the file with the largest value of *xxxxxxxxxxxx*.</span></span>

<span data-ttu-id="8f942-212">**Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-212">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-213">База данных регистрации классов COM+ зависит от копируемого раздела реестра и поэтому нуждается в резервном копировании и восстановлении вместе с реестром.</span><span class="sxs-lookup"><span data-stu-id="8f942-213">The COM+ class registration database depends on a registry key being backed up and hence needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="8f942-214">Чтобы восстановить базу данных регистрации COM+, приложение резервного копирования (инициатор запроса) должно вызвать метод [**икомадминкаталог:: ресторерегдб**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .</span><span class="sxs-lookup"><span data-stu-id="8f942-214">To restore the COM+ Registration Database, a backup application (requester) must call the [**ICOMAdminCatalog::RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="8f942-215">Строка имени модуля записи для этого модуля записи — "COM+ РЕГДБ Writer".</span><span class="sxs-lookup"><span data-stu-id="8f942-215">The writer name string for this writer is "COM+ REGDB Writer".</span></span>

<span data-ttu-id="8f942-216">Идентификатор модуля записи для модуля записи базы данных регистрации классов COM+ — 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span><span class="sxs-lookup"><span data-stu-id="8f942-216">The writer ID for the COM+ class registration database writer is 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span></span>

## <a name="data-deduplication-writer"></a><span data-ttu-id="8f942-217">Модуль записи дедупликации данных</span><span class="sxs-lookup"><span data-stu-id="8f942-217">Data Deduplication Writer</span></span>

<span data-ttu-id="8f942-218">Модуль записи VSS для дедупликации данных описан в документации по API [дедупликации данных](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) .</span><span class="sxs-lookup"><span data-stu-id="8f942-218">The Data Deduplication VSS writer is documented in the [Data Deduplication](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) API documentation.</span></span> <span data-ttu-id="8f942-219">Этот модуль записи является встроенным средством записи для версий операционной системы Windows Server; Он не поставляется в клиенте Windows.</span><span class="sxs-lookup"><span data-stu-id="8f942-219">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8f942-220">**Windows server 2008 R2, Windows server 2008 и Windows server 2003:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-220">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

## <a name="distributed-file-system-replication-dfsr"></a><span data-ttu-id="8f942-221">Служба репликации распределенной файловой системы (DSFR).</span><span class="sxs-lookup"><span data-stu-id="8f942-221">Distributed File System Replication (DFSR)</span></span>

<span data-ttu-id="8f942-222">Следующий компонент включает модуль записи VSS: [Распределенная файловая система Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span><span class="sxs-lookup"><span data-stu-id="8f942-222">The following component includes a VSS writer: [Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span></span>

<span data-ttu-id="8f942-223">Windows **Vista, Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается до Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f942-223">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a><span data-ttu-id="8f942-224">Модуль записи протокола DHCP</span><span class="sxs-lookup"><span data-stu-id="8f942-224">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>

<span data-ttu-id="8f942-225">Этот модуль записи отвечает за перечисление файлов, необходимых для роли DHCP-сервера.</span><span class="sxs-lookup"><span data-stu-id="8f942-225">This writer is responsible for enumerating files required for the DHCP server role.</span></span> <span data-ttu-id="8f942-226">Этот модуль записи является встроенным средством записи для версий операционной системы Windows Server; Он не поставляется в клиенте Windows.</span><span class="sxs-lookup"><span data-stu-id="8f942-226">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8f942-227">Строка имени модуля записи для этого модуля записи — "модуль записи Jet в DHCP".</span><span class="sxs-lookup"><span data-stu-id="8f942-227">The writer name string for this writer is "Dhcp Jet Writer".</span></span>

<span data-ttu-id="8f942-228">Идентификатор модуля записи для этого модуля записи — BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span><span class="sxs-lookup"><span data-stu-id="8f942-228">The writer ID for this writer is BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span></span>

## <a name="file-replication-service-frs"></a><span data-ttu-id="8f942-229">Служба репликации файлов (FRS)</span><span class="sxs-lookup"><span data-stu-id="8f942-229">File Replication Service (FRS)</span></span>

<span data-ttu-id="8f942-230">Модуль записи службы репликации файлов описан в статье [резервное копирование и восстановление папки FRS-Replicated SYSVOL](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span><span class="sxs-lookup"><span data-stu-id="8f942-230">The File Replication Service writer is documented in [Backing Up and Restoring an FRS-Replicated SYSVOL Folder](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span></span>

<span data-ttu-id="8f942-231">Windows **Vista, Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается до Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f942-231">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="file-server-resource-manager-fsrm-writer"></a><span data-ttu-id="8f942-232">Модуль записи диспетчер ресурсов файлового сервера (FSRM)</span><span class="sxs-lookup"><span data-stu-id="8f942-232">File Server Resource Manager (FSRM) Writer</span></span>

<span data-ttu-id="8f942-233">Этот модуль записи перечисляет файлы конфигурации FSRM, которые используются для резервного копирования состояния системы.</span><span class="sxs-lookup"><span data-stu-id="8f942-233">This writer enumerates the FSRM configuration files that are used for system state backup.</span></span> <span data-ttu-id="8f942-234">Во время операций восстановления предотвращается изменение конфигурации FSRM и временно прекращается применение квот и экранов файлов.</span><span class="sxs-lookup"><span data-stu-id="8f942-234">During restore operations it prevents changes in FSRM configuration and temporarily halts enforcement of quotas and file screens.</span></span> <span data-ttu-id="8f942-235">После завершения восстановления модуль записи обновляет файл FSRM с восстановленной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="8f942-235">After the restore is complete, the writer refreshes FSRM with the configuration that was restored.</span></span> <span data-ttu-id="8f942-236">Этот модуль записи доступен только в том случае, если компонент FSRM (часть роли файловых служб) установлен и работает.</span><span class="sxs-lookup"><span data-stu-id="8f942-236">This writer is only present when FSRM (part of File Services role) is both installed and running.</span></span> <span data-ttu-id="8f942-237">Этот модуль записи является встроенным средством записи для версий операционной системы Windows Server; Он не поставляется в клиенте Windows.</span><span class="sxs-lookup"><span data-stu-id="8f942-237">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8f942-238">**Windows Server 2003:** Этот модуль записи не поддерживается до Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="8f942-238">**Windows Server 2003:** This writer is not supported until Windows Server 2003 R2.</span></span>

<span data-ttu-id="8f942-239">Строка имени записи для этого модуля записи — "модуль записи FSRM".</span><span class="sxs-lookup"><span data-stu-id="8f942-239">The writer name string for this writer is "FSRM Writer".</span></span>

<span data-ttu-id="8f942-240">Идентификатор модуля записи для этого модуля записи — 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span><span class="sxs-lookup"><span data-stu-id="8f942-240">The writer ID for this writer is 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span></span>

## <a name="hyper-v-writer"></a><span data-ttu-id="8f942-241">Модуль записи Hyper-V</span><span class="sxs-lookup"><span data-stu-id="8f942-241">Hyper-V Writer</span></span>

<span data-ttu-id="8f942-242">Модуль записи VSS для Hyper-V описан в документации по API [Hyper-v](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) .</span><span class="sxs-lookup"><span data-stu-id="8f942-242">The Hyper-V VSS writer is documented in the [Hyper-V](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) API documentation.</span></span> <span data-ttu-id="8f942-243">Этот модуль записи является встроенным средством записи для версий операционной системы Windows Server; Он не поставляется в клиенте Windows.</span><span class="sxs-lookup"><span data-stu-id="8f942-243">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8f942-244">**Windows Server 2003:** Этот модуль записи не поддерживается до Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f942-244">**Windows Server 2003:** This writer is not supported until Windows Server 2008.</span></span>

## <a name="iis-configuration-writer"></a><span data-ttu-id="8f942-245">Модуль записи конфигурации IIS</span><span class="sxs-lookup"><span data-stu-id="8f942-245">IIS Configuration Writer</span></span>

<span data-ttu-id="8f942-246">Модуль записи конфигурации IIS отвечает за перечисление файлов конфигурации IIS.</span><span class="sxs-lookup"><span data-stu-id="8f942-246">The IIS configuration writer is responsible for enumerating the IIS configuration files.</span></span>

<span data-ttu-id="8f942-247">Windows **Vista, Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается до Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f942-247">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="8f942-248">Запрашивающие стороны необходимы для резервного копирования файлов конфигурации IIS, включая файл machine.config .NET FX или корневой web.config файла ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="8f942-248">Requesters are required to back up the IIS configuration files, including the .NET FX machine.config file or the ASP.NET root web.config file.</span></span>

<span data-ttu-id="8f942-249">Этот модуль записи не выполняет резервное копирование файла machine.config .NET FX или корневого web.config файла ASP.NET, так как эти файлы перечисляются модулем записи системы.</span><span class="sxs-lookup"><span data-stu-id="8f942-249">This writer does not back up the .NET FX machine.config file or the ASP.NET root web.config file because these files are enumerated by the System Writer.</span></span>

<span data-ttu-id="8f942-250">Этот модуль записи создает резервные копии всех файлов, которые находятся в каталоге% WINDIR% \\ system32 \\ Inetsrv \\ config \\ и каталогах% WINDIR% \\ system32 \\ Inetsrv \\ config, за исключением файлов, перечисленных модулем записи системы.</span><span class="sxs-lookup"><span data-stu-id="8f942-250">This writer backs up all files that are in the %windir%\\system32\\inetsrv\\config\\schema and %windir%\\system32\\inetsrv\\config directories, except for files that are enumerated by the System Writer.</span></span>

<span data-ttu-id="8f942-251">Идентификатор модуля записи для модуля записи конфигурации IIS — 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span><span class="sxs-lookup"><span data-stu-id="8f942-251">The writer ID for the IIS configuration writer is 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span></span>

## <a name="iis-metabase-writer"></a><span data-ttu-id="8f942-252">Модуль записи метабазы IIS</span><span class="sxs-lookup"><span data-stu-id="8f942-252">IIS Metabase Writer</span></span>

<span data-ttu-id="8f942-253">Модуль записи в метабазу IIS отвечает за перечисление файла метабазы IIS.</span><span class="sxs-lookup"><span data-stu-id="8f942-253">The Internet Information Server (IIS) metabase writer is responsible for enumerating the IIS metabase file.</span></span>

<span data-ttu-id="8f942-254">Windows **Vista, Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается до Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f942-254">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="8f942-255">Для создания резервной копии файла метабазы IIS требуются инициаторы запроса.</span><span class="sxs-lookup"><span data-stu-id="8f942-255">Requesters are required to back up the IIS metabase file.</span></span>

<span data-ttu-id="8f942-256">Идентификатор модуля записи метабазы IIS — 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span><span class="sxs-lookup"><span data-stu-id="8f942-256">The writer ID for the IIS metabase writer is 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span></span>

## <a name="microsoft-message-queuing-msmq-writer"></a><span data-ttu-id="8f942-257">Модуль записи очереди сообщений Майкрософт (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="8f942-257">Microsoft Message Queuing (MSMQ) Writer</span></span>

<span data-ttu-id="8f942-258">Этот модуль записи сообщает о файлах данных очереди сообщений Майкрософт (MSMQ).</span><span class="sxs-lookup"><span data-stu-id="8f942-258">This writer reports the Microsoft Message Queuing (MSMQ) data files.</span></span>

<span data-ttu-id="8f942-259">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-259">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-260">Строка имени модуля записи для этого модуля записи — «модуль записи MSMQ (*SvcName*)», где *SvcName* — имя службы MSMQ, с которой связан модуль записи.</span><span class="sxs-lookup"><span data-stu-id="8f942-260">The writer name string for this writer is "MSMQ Writer (*SvcName*)", where *SvcName* is the name of the MSMQ service the writer is associated with.</span></span> <span data-ttu-id="8f942-261">Для установки по умолчанию используется имя службы MSMQ.</span><span class="sxs-lookup"><span data-stu-id="8f942-261">For default installation, the service name is "MSMQ".</span></span> <span data-ttu-id="8f942-262">Для кластеризованных экземпляров именем службы является MSMQ $*resourceName*, где *resourceName* — это кластеризованное имя ресурса MSMQ.</span><span class="sxs-lookup"><span data-stu-id="8f942-262">For clustered instances, the service name is MSMQ$*ResourceName*, where *ResourceName* is the clustered MSMQ resource name.</span></span>

<span data-ttu-id="8f942-263">Идентификатор модуля записи для этого модуля записи — 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span><span class="sxs-lookup"><span data-stu-id="8f942-263">The writer ID for this writer is 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span></span>

## <a name="mssearch-service-writer"></a><span data-ttu-id="8f942-264">Модуль записи службы MSSearch</span><span class="sxs-lookup"><span data-stu-id="8f942-264">MSSearch Service Writer</span></span>

<span data-ttu-id="8f942-265">Этот модуль записи существует для удаления файлов индекса поиска из теневых копий после создания.</span><span class="sxs-lookup"><span data-stu-id="8f942-265">This writer exists to delete search index files from shadow copies after creation.</span></span> <span data-ttu-id="8f942-266">Это делается для того, чтобы уменьшить влияние операций копирования на запись и ввода-вывода во время обычных операций ввода-вывода для этих файлов на теневой копии тома.</span><span class="sxs-lookup"><span data-stu-id="8f942-266">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span>

<span data-ttu-id="8f942-267">**Windows Server 2003:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-267">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-268">Чтобы установить этот модуль записи на сервере, необходимо установить роль файловых служб и включить Служба поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="8f942-268">To install this writer on the server, you must install the File Services role and enable the Windows Search Service.</span></span>

<span data-ttu-id="8f942-269">Строка имени модуля записи для этого модуля записи — "модуль записи службы MSSearch".</span><span class="sxs-lookup"><span data-stu-id="8f942-269">The writer name string for this writer is "MSSearch Service Writer".</span></span>

<span data-ttu-id="8f942-270">Идентификатор модуля записи для модуля записи службы MSSearch — CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span><span class="sxs-lookup"><span data-stu-id="8f942-270">The writer ID for the MSSearch service writer is CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span></span>

## <a name="nps-vss-writer"></a><span data-ttu-id="8f942-271">Модуль записи VSS NPS</span><span class="sxs-lookup"><span data-stu-id="8f942-271">NPS VSS Writer</span></span>

<span data-ttu-id="8f942-272">Модуль записи NPS отвечает за перечисление файлов конфигурации сервера политики сети (NPS) для серверов, на которых установлена роль служб политики сети и доступа.</span><span class="sxs-lookup"><span data-stu-id="8f942-272">The NPS writer is responsible for enumerating the Network Policy Server (NPS) configuration files for servers that have the Network Policy and Access Services role installed.</span></span>

<span data-ttu-id="8f942-273">Windows **Vista, Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается до Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f942-273">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

<span data-ttu-id="8f942-274">Строка имени модуля записи для этого модуля записи: "модуль записи VSS NPS".</span><span class="sxs-lookup"><span data-stu-id="8f942-274">The writer name string for this writer is "NPS VSS Writer".</span></span>

<span data-ttu-id="8f942-275">Идентификатор записи для модуля записи VSS в NPS — 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span><span class="sxs-lookup"><span data-stu-id="8f942-275">The writer ID for the NPS VSS writer is 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span></span>

## <a name="performance-counters-writer"></a><span data-ttu-id="8f942-276">Модуль записи счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="8f942-276">Performance Counters Writer</span></span>

<span data-ttu-id="8f942-277">Этот модуль записи сообщает о файлах конфигурации счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="8f942-277">This writer reports the performance counter configuration files.</span></span> <span data-ttu-id="8f942-278">Эти файлы изменяются только во время установки приложения и должны быть архивированы и восстановлены во время резервного копирования и восстановления состояния системы.</span><span class="sxs-lookup"><span data-stu-id="8f942-278">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

<span data-ttu-id="8f942-279">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-279">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="8f942-280">Для создания резервных копий этих файлов вручную требуются инициаторы запроса.</span><span class="sxs-lookup"><span data-stu-id="8f942-280">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="8f942-281">(См. раздел [резервное копирование и восстановление состояния системы](locating-additional-system-files.md).)</span><span class="sxs-lookup"><span data-stu-id="8f942-281">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="8f942-282">Строка имени модуля записи для этого модуля записи — "модуль записи счетчиков производительности".</span><span class="sxs-lookup"><span data-stu-id="8f942-282">The writer name string for this writer is "Performance Counters Writer".</span></span>

<span data-ttu-id="8f942-283">Идентификатор модуля записи для модуля записи счетчиков производительности — 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span><span class="sxs-lookup"><span data-stu-id="8f942-283">The writer ID for the Performance Counters Writer is 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span></span>

## <a name="registry-writer"></a><span data-ttu-id="8f942-284">Модуль записи реестра</span><span class="sxs-lookup"><span data-stu-id="8f942-284">Registry Writer</span></span>

<span data-ttu-id="8f942-285">Модуль записи в реестр сообщает о файлах реестра Windows, чтобы обеспечить возможность резервного копирования на месте и восстановления реестра.</span><span class="sxs-lookup"><span data-stu-id="8f942-285">The registry writer is reports the Windows registry files to enable in-place backups and restores of the registry.</span></span> <span data-ttu-id="8f942-286">Он не сообщает о пользовательских кустах.</span><span class="sxs-lookup"><span data-stu-id="8f942-286">It does not report user hives.</span></span>

<span data-ttu-id="8f942-287">**Windows Server 2003:** В Windows Server 2003 этот модуль записи использует промежуточный файл репозитория (который иногда называется "выдам File") для хранения данных реестра.</span><span class="sxs-lookup"><span data-stu-id="8f942-287">**Windows Server 2003:** In Windows Server 2003, this writer uses an intermediate repository file (sometimes called a "spit file") to store registry data.</span></span> <span data-ttu-id="8f942-288">(См. [раздел Резервное копирование реестра и операции восстановления в VSS](registry-backup-and-restore-operations-under-vss.md).)</span><span class="sxs-lookup"><span data-stu-id="8f942-288">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="8f942-289">**Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-289">**Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="8f942-290">(См. [раздел Резервное копирование реестра и операции восстановления в VSS](registry-backup-and-restore-operations-under-vss.md).)</span><span class="sxs-lookup"><span data-stu-id="8f942-290">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="8f942-291">Строка имени модуля записи для этого модуля записи — "модуль записи в реестр".</span><span class="sxs-lookup"><span data-stu-id="8f942-291">The writer name string for this writer is "Registry Writer".</span></span>

<span data-ttu-id="8f942-292">Идентификатор модуля записи реестра — AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span><span class="sxs-lookup"><span data-stu-id="8f942-292">The writer ID for the registry writer is AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span></span>

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a><span data-ttu-id="8f942-293">Модуль записи VSS шлюза службы удаленных рабочих столов (службы терминалов)</span><span class="sxs-lookup"><span data-stu-id="8f942-293">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>

<span data-ttu-id="8f942-294">Этот модуль записи отвечает за перечисление файлов шлюза службы удаленных рабочих столов (служб терминалов) для серверов, на которых установлен шлюз удаленный рабочий стол, подроль службы удаленных рабочих столов роли.</span><span class="sxs-lookup"><span data-stu-id="8f942-294">This writer is responsible for enumerating the Remote Desktop Services (Terminal Services) Gateway files for servers that have Remote Desktop Gateway, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="8f942-295">**Windows Server 2003:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-295">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-296">Этот модуль записи является встроенным средством записи для версий операционной системы Windows Server; Он не поставляется в клиенте Windows.</span><span class="sxs-lookup"><span data-stu-id="8f942-296">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8f942-297">Шлюз службы удаленных рабочих столов зависит от нескольких архивируемых разделов реестра и поэтому нуждается в резервном копировании и восстановлении вместе с реестром.</span><span class="sxs-lookup"><span data-stu-id="8f942-297">The Remote Desktop Services Gateway depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="8f942-298">Строка имени модуля записи для этого модуля записи — "модуль записи шлюза TS".</span><span class="sxs-lookup"><span data-stu-id="8f942-298">The writer name string for this writer is "TS Gateway Writer".</span></span>

<span data-ttu-id="8f942-299">Идентификатор модуля записи для этого модуля записи — 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span><span class="sxs-lookup"><span data-stu-id="8f942-299">The writer ID for this writer is 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span></span>

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a><span data-ttu-id="8f942-300">Модуль записи VSS лицензирования службы удаленных рабочих столов (службы терминалов)</span><span class="sxs-lookup"><span data-stu-id="8f942-300">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="8f942-301">Этот модуль записи отвечает за перечисление файлов лицензирования службы удаленных рабочих столов (лицензирование удаленных рабочих столов) или лицензирования служб терминалов для серверов, которые имеют удаленный рабочий стол лицензирования, подроль службы удаленных рабочих столов роли.</span><span class="sxs-lookup"><span data-stu-id="8f942-301">This writer is responsible for enumerating the Remote Desktop Services Licensing (RD Licensing) or Terminal Services Licensing (TS Licensing) files for servers that have Remote Desktop Licensing, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="8f942-302">**Windows Server 2003:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-302">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-303">Этот модуль записи является встроенным средством записи для версий операционной системы Windows Server; Он не поставляется в клиенте Windows.</span><span class="sxs-lookup"><span data-stu-id="8f942-303">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8f942-304">Лицензирование службы удаленных рабочих столов зависит от нескольких архивируемых разделов реестра и поэтому нуждается в резервном копировании и восстановлении вместе с реестром.</span><span class="sxs-lookup"><span data-stu-id="8f942-304">Remote Desktop Services Licensing depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="8f942-305">Строка имени модуля записи для этого модуля записи — "TermServLicensing".</span><span class="sxs-lookup"><span data-stu-id="8f942-305">The writer name string for this writer is "TermServLicensing".</span></span>

<span data-ttu-id="8f942-306">Идентификатор модуля записи для этого модуля записи — 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span><span class="sxs-lookup"><span data-stu-id="8f942-306">The writer ID for this writer is 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span></span>

## <a name="shadow-copy-optimization-writer"></a><span data-ttu-id="8f942-307">Модуль записи оптимизации теневого копирования</span><span class="sxs-lookup"><span data-stu-id="8f942-307">Shadow Copy Optimization Writer</span></span>

<span data-ttu-id="8f942-308">Этот модуль записи удаляет определенные файлы из теневых копий томов.</span><span class="sxs-lookup"><span data-stu-id="8f942-308">This writer deletes certain files from volume shadow copies.</span></span> <span data-ttu-id="8f942-309">Это делается для того, чтобы уменьшить влияние операций копирования на запись и ввода-вывода во время обычных операций ввода-вывода для этих файлов на теневой копии тома.</span><span class="sxs-lookup"><span data-stu-id="8f942-309">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span> <span data-ttu-id="8f942-310">Удаляемые файлы обычно являются временными файлами или файлами, которые не содержат состояния пользователя или системы.</span><span class="sxs-lookup"><span data-stu-id="8f942-310">The files that are deleted are typically temporary files or files that do not contain user or system state.</span></span>

<span data-ttu-id="8f942-311">**Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-311">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-312">Строка имени модуля записи для этого модуля записи — "модуль записи оптимизации теневого копирования".</span><span class="sxs-lookup"><span data-stu-id="8f942-312">The writer name string for this writer is "Shadow Copy Optimization Writer".</span></span>

<span data-ttu-id="8f942-313">Идентификатор модуля записи для модуля записи оптимизации теневого копирования — 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span><span class="sxs-lookup"><span data-stu-id="8f942-313">The writer ID for the shadow copy optimization writer is 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span></span>

## <a name="sync-share-service-writer"></a><span data-ttu-id="8f942-314">Средство записи общего доступа к службе синхронизации</span><span class="sxs-lookup"><span data-stu-id="8f942-314">Sync Share Service Writer</span></span>

<span data-ttu-id="8f942-315">**Windows Server 2012 R2:** Этот модуль записи входит в состав Windows Server 2012 R2 и более поздних версий сервера.</span><span class="sxs-lookup"><span data-stu-id="8f942-315">**Windows Server 2012 R2:** This writer is included with Windows Server 2012 R2 and newer server versions.</span></span> <span data-ttu-id="8f942-316">Он несовместим с версиями для настольных систем.</span><span class="sxs-lookup"><span data-stu-id="8f942-316">It is not compatible with desktop versions.</span></span>

<span data-ttu-id="8f942-317">Этот модуль записи отвечает за перечисление общих папок синхронизации на серверах, на которых установлена служба общего ресурса синхронизации, и для обеспечения согласованности их метаданных и данных во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="8f942-317">This writer is responsible for enumerating the sync shares on servers that have the Sync Share Service installed, and for ensuring that their metadata and data remain consistent during backup and restore.</span></span>

<span data-ttu-id="8f942-318">Этот модуль записи имеется только в том случае, если установлена и запущена служба общего ресурса синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8f942-318">This writer is only present when Sync Share Service is both installed and running.</span></span>

<span data-ttu-id="8f942-319">Для каждого общего ресурса синхронизации будет использоваться один компонент модуля записи VSS.</span><span class="sxs-lookup"><span data-stu-id="8f942-319">There will be one VSS writer component for each sync share.</span></span> <span data-ttu-id="8f942-320">Сюда входят метаданные и пути к данным.</span><span class="sxs-lookup"><span data-stu-id="8f942-320">This includes the metadata and data paths.</span></span> <span data-ttu-id="8f942-321">Для обеспечения согласованности их необходимо архивировать вместе.</span><span class="sxs-lookup"><span data-stu-id="8f942-321">These must be backed up together for consistency.</span></span>

<span data-ttu-id="8f942-322">Строка имени модуля записи — "модуль записи VSS для службы общих ресурсов синхронизации".</span><span class="sxs-lookup"><span data-stu-id="8f942-322">The writer name string is "Sync Share Service VSS writer".</span></span>

<span data-ttu-id="8f942-323">Идентификатор модуля записи — D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span><span class="sxs-lookup"><span data-stu-id="8f942-323">The writer ID is D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span></span>

## <a name="system-writer"></a><span data-ttu-id="8f942-324">Модуль записи системы</span><span class="sxs-lookup"><span data-stu-id="8f942-324">System Writer</span></span>

<span data-ttu-id="8f942-325">Модуль записи системы перечисляет все двоичные файлы операционной системы и драйверов и требуется для резервного копирования состояния системы.</span><span class="sxs-lookup"><span data-stu-id="8f942-325">The system writer enumerates all operating system and driver binaries and it is required for a system state backup.</span></span>

<span data-ttu-id="8f942-326">**Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-326">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-327">Этот модуль записи выполняется как часть службы криптографии (Криптсвк).</span><span class="sxs-lookup"><span data-stu-id="8f942-327">This writer runs as part of the Cryptographic Services (CryptSvc) service.</span></span> <span data-ttu-id="8f942-328">Модуль записи системы создает список файлов, содержащий следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="8f942-328">The system writer generates a file list that contains the following files:</span></span>

-   <span data-ttu-id="8f942-329">Все установленные статические файлы.</span><span class="sxs-lookup"><span data-stu-id="8f942-329">All static files that have been installed.</span></span> <span data-ttu-id="8f942-330">Статический файл — это файл, указанный в манифесте компонента с атрибутом файла **вритеаблетипе** , имеющим значение "static" или "".</span><span class="sxs-lookup"><span data-stu-id="8f942-330">A static file is a file that is listed in the component manifest with the **writeableType** file attribute set to "static" or "".</span></span> <span data-ttu-id="8f942-331">Статические файлы включают все файлы, защищенные защита ресурсов Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="8f942-331">Static files include all files that are protected by Windows Resource Protection (WRP).</span></span> <span data-ttu-id="8f942-332">Однако не все статические файлы являются файлами, защищенными WRP.</span><span class="sxs-lookup"><span data-stu-id="8f942-332">However, not all static files are WRP-protected files.</span></span> <span data-ttu-id="8f942-333">Например, файлы игр являются статическими, но не защищены WRP, поэтому администраторы могут изменять параметры родительского контроля.</span><span class="sxs-lookup"><span data-stu-id="8f942-333">For example, game files are static but not WRP-protected so that administrators can change parental control settings.</span></span>
-   <span data-ttu-id="8f942-334">Содержимое каталога Windows параллельно (WinSxS), включая все манифесты, дополнительные компоненты и сторонние файлы Win32.</span><span class="sxs-lookup"><span data-stu-id="8f942-334">The contents of the Windows Side-by-Side (WinSxS) directory, including all manifests, optional components, and third-party Win32 files.</span></span>
    > [!Note]  
    > <span data-ttu-id="8f942-335">Многие файлы в каталоге% WINDIR% \\ system32 являются жесткими ссылками на файлы в каталоге WinSxS.</span><span class="sxs-lookup"><span data-stu-id="8f942-335">Many of the files in the %windir%\\system32 directory are hard links to files in the WinSxS directory.</span></span>

     

-   <span data-ttu-id="8f942-336">Все файлы PnP для установленных драйверов (принадлежащие PnP).</span><span class="sxs-lookup"><span data-stu-id="8f942-336">All PnP files for installed drivers (owned by PnP).</span></span>
-   <span data-ttu-id="8f942-337">Все службы пользовательского режима и драйверы без PnP.</span><span class="sxs-lookup"><span data-stu-id="8f942-337">All user-mode services and non-PnP drivers.</span></span>
-   <span data-ttu-id="8f942-338">Все каталоги, принадлежащие Криптсвк.</span><span class="sxs-lookup"><span data-stu-id="8f942-338">All catalogs owned by CryptSvc.</span></span>

<span data-ttu-id="8f942-339">Приложение восстановления отвечает за размещение файлов и реестра и настройку списков управления доступом в соответствии с теневой копией системы.</span><span class="sxs-lookup"><span data-stu-id="8f942-339">The restore application is responsible for laying down the files and registry and setting ACLs to match the system shadow copy.</span></span> <span data-ttu-id="8f942-340">Для завершения восстановления состояния системы также необходимо создать соответствующие жесткие связи.</span><span class="sxs-lookup"><span data-stu-id="8f942-340">The appropriate hard links must also be created for a system state restore to succeed.</span></span>

<span data-ttu-id="8f942-341">Строка имени модуля записи для этого модуля записи — "модуль записи системы".</span><span class="sxs-lookup"><span data-stu-id="8f942-341">The writer name string for this writer is "System Writer".</span></span>

<span data-ttu-id="8f942-342">Идентификатор модуля записи для модуля записи системы — E8132975-6F93-4464-A53E-1050253AE220.</span><span class="sxs-lookup"><span data-stu-id="8f942-342">The writer ID for the system writer is E8132975-6F93-4464-A53E-1050253AE220.</span></span>

## <a name="task-scheduler-writer"></a><span data-ttu-id="8f942-343">Модуль записи планировщик задач</span><span class="sxs-lookup"><span data-stu-id="8f942-343">Task Scheduler Writer</span></span>

<span data-ttu-id="8f942-344">Этот модуль записи сообщает о файлах задач планировщика заданий.</span><span class="sxs-lookup"><span data-stu-id="8f942-344">This writer reports the task scheduler's task files.</span></span>

<span data-ttu-id="8f942-345">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-345">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="8f942-346">Для создания резервных копий этих файлов вручную требуются инициаторы запроса.</span><span class="sxs-lookup"><span data-stu-id="8f942-346">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="8f942-347">(См. раздел [резервное копирование и восстановление состояния системы](locating-additional-system-files.md).)</span><span class="sxs-lookup"><span data-stu-id="8f942-347">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="8f942-348">Строка имени модуля записи для этого модуля записи — "планировщик задач Writer".</span><span class="sxs-lookup"><span data-stu-id="8f942-348">The writer name string for this writer is "Task Scheduler Writer".</span></span>

<span data-ttu-id="8f942-349">Идентификатор модуля записи — D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span><span class="sxs-lookup"><span data-stu-id="8f942-349">The writer ID for the writer is D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span></span>

## <a name="vss-metadata-store-writer"></a><span data-ttu-id="8f942-350">Модуль записи хранилища метаданных VSS</span><span class="sxs-lookup"><span data-stu-id="8f942-350">VSS Metadata Store Writer</span></span>

<span data-ttu-id="8f942-351">Этот модуль записи сообщает файлы метаданных модуля записи для всех модулей записи VSS Express.</span><span class="sxs-lookup"><span data-stu-id="8f942-351">This writer reports the writer metadata files for all VSS express writers.</span></span>

<span data-ttu-id="8f942-352">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-352">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-353">Строка имени модуля записи для этого модуля записи — "модуль записи хранилища метаданных модуля Экспресс-записи VSS".</span><span class="sxs-lookup"><span data-stu-id="8f942-353">The writer name string for this writer is "VSS Express Writer Metadata Store Writer".</span></span>

<span data-ttu-id="8f942-354">Идентификатор модуля записи — 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span><span class="sxs-lookup"><span data-stu-id="8f942-354">The writer ID for the writer is 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span></span>

## <a name="windows-deployment-services-wds-writer"></a><span data-ttu-id="8f942-355">Модуль записи служб развертывания Windows (WDS)</span><span class="sxs-lookup"><span data-stu-id="8f942-355">Windows Deployment Services (WDS) Writer</span></span>

<span data-ttu-id="8f942-356">Этот модуль записи сообщает о файлах данных служб развертывания Windows (WDS).</span><span class="sxs-lookup"><span data-stu-id="8f942-356">This writer reports the Windows Deployment Services (WDS) data files.</span></span>

<span data-ttu-id="8f942-357">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-357">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-358">Строка имени модуля записи для этого модуля записи — "модуль записи VSS WDS".</span><span class="sxs-lookup"><span data-stu-id="8f942-358">The writer name string for this writer is "WDS VSS Writer".</span></span>

<span data-ttu-id="8f942-359">Идентификатор модуля записи для этого модуля записи — 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span><span class="sxs-lookup"><span data-stu-id="8f942-359">The writer ID for this writer is 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span></span>

## <a name="windows-internal-database-wid-writer"></a><span data-ttu-id="8f942-360">Модуль записи внутренней базы данных Windows (WID)</span><span class="sxs-lookup"><span data-stu-id="8f942-360">Windows Internal Database (WID) Writer</span></span>

<span data-ttu-id="8f942-361">Этот модуль записи сообщает о файлах данных внутренней базы данных Windows (WID).</span><span class="sxs-lookup"><span data-stu-id="8f942-361">This writer reports the Windows Internal Database (WID) data files.</span></span>

<span data-ttu-id="8f942-362">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-362">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-363">Строка имени модуля записи для этого модуля записи — "Видвритер".</span><span class="sxs-lookup"><span data-stu-id="8f942-363">The writer name string for this writer is "WIDWriter".</span></span>

<span data-ttu-id="8f942-364">Идентификатор модуля записи для этого модуля записи — 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span><span class="sxs-lookup"><span data-stu-id="8f942-364">The writer ID for this writer is 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span></span>

## <a name="windows-internet-name-service-wins-writer"></a><span data-ttu-id="8f942-365">Модуль записи службы Windows Internet Name Service (WINS)</span><span class="sxs-lookup"><span data-stu-id="8f942-365">Windows Internet Name Service (WINS) Writer</span></span>

<span data-ttu-id="8f942-366">Этот модуль записи отвечает за перечисление файлов, необходимых для WINS.</span><span class="sxs-lookup"><span data-stu-id="8f942-366">This writer is responsible for enumerating files required for WINS.</span></span>

<span data-ttu-id="8f942-367">**Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-367">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-368">Строка имени модуля записи для этого модуля записи — "модуль записи Jet в службу".</span><span class="sxs-lookup"><span data-stu-id="8f942-368">The writer name string for this writer is "WINS Jet Writer".</span></span>

<span data-ttu-id="8f942-369">Идентификатор модуля записи для этого модуля записи — F08C1483-8407-4A26-8C26-6C267A629741.</span><span class="sxs-lookup"><span data-stu-id="8f942-369">The writer ID for this writer is F08C1483-8407-4A26-8C26-6C267A629741.</span></span>

## <a name="wmi-writer"></a><span data-ttu-id="8f942-370">Модуль записи WMI</span><span class="sxs-lookup"><span data-stu-id="8f942-370">WMI Writer</span></span>

<span data-ttu-id="8f942-371">Этот модуль записи используется для идентификации состояния и данных инструментария WMI во время операций резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="8f942-371">This writer is used for identifying WMI-specific state and data during backup operations.</span></span> <span data-ttu-id="8f942-372">Данные включают файлы из репозитория WBEM.</span><span class="sxs-lookup"><span data-stu-id="8f942-372">The data includes files from the WBEM repository.</span></span>

<span data-ttu-id="8f942-373">**Windows Server 2003 и Windows XP:** Этот модуль записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f942-373">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8f942-374">Строка имени модуля записи для этого модуля записи — "модуль записи WMI".</span><span class="sxs-lookup"><span data-stu-id="8f942-374">The writer name string for this writer is "WMI Writer".</span></span>

<span data-ttu-id="8f942-375">Идентификатор модуля записи для этого модуля записи — A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span><span class="sxs-lookup"><span data-stu-id="8f942-375">The writer ID for this writer is A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span></span>

 

 
