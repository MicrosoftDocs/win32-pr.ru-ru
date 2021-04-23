---
description: Вшадов — это программа командной строки, которую можно использовать для создания и управления теневыми копиями томов.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Средство Вшадов и пример
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497523"
---
# <a name="vshadow-tool-and-sample"></a><span data-ttu-id="3c439-103">Средство Вшадов и пример</span><span class="sxs-lookup"><span data-stu-id="3c439-103">VShadow Tool and Sample</span></span>

<span data-ttu-id="3c439-104">Вшадов — это программа командной строки, которую можно использовать для создания и управления теневыми копиями томов.</span><span class="sxs-lookup"><span data-stu-id="3c439-104">VShadow is a command-line tool that you can use to create and manage volume shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="3c439-105">Вшадов входит в состав пакета средств разработки программного обеспечения Microsoft Windows (SDK) для Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3c439-105">VShadow is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="3c439-106">Пакет SDK для VSS 7,2 включает версию Вшадов, которая работает только в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3c439-106">The VSS 7.2 SDK includes a version of VShadow that runs only on Windows Server 2003.</span></span> <span data-ttu-id="3c439-107">Сведения о скачивании Windows SDK и пакета SDK для VSS 7,2 см. в разделе [Служба теневого копирования томов](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="3c439-107">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="3c439-108">Средство Вшадов использует параметры командной строки и необязательные флаги для задания выполняемой работы.</span><span class="sxs-lookup"><span data-stu-id="3c439-108">The VShadow tool uses command-line options and optional flags to identify the work to perform.</span></span> <span data-ttu-id="3c439-109">При использовании без параметров командной строки команда Вшадов создает новый набор теневых копий.</span><span class="sxs-lookup"><span data-stu-id="3c439-109">When used without any command-line options, the VShadow command creates a new shadow copy set.</span></span>

<span data-ttu-id="3c439-110">Команды Вшадов выполняют следующие операции:</span><span class="sxs-lookup"><span data-stu-id="3c439-110">VShadow commands perform the following operations:</span></span>

-   [<span data-ttu-id="3c439-111">Создание набора теневых копий</span><span class="sxs-lookup"><span data-stu-id="3c439-111">Creating a Shadow Copy Set</span></span>](#creating-a-shadow-copy-set)
-   [<span data-ttu-id="3c439-112">Импорт набора теневых копий</span><span class="sxs-lookup"><span data-stu-id="3c439-112">Importing a Shadow Copy Set</span></span>](#importing-a-shadow-copy-set)
-   [<span data-ttu-id="3c439-113">Запрос свойств теневого копирования</span><span class="sxs-lookup"><span data-stu-id="3c439-113">Querying Shadow Copy Properties</span></span>](#querying-shadow-copy-properties)
-   [<span data-ttu-id="3c439-114">Удаление теневых копий</span><span class="sxs-lookup"><span data-stu-id="3c439-114">Deleting Shadow Copies</span></span>](#deleting-shadow-copies)
-   [<span data-ttu-id="3c439-115">Разбиение набора теневых копий</span><span class="sxs-lookup"><span data-stu-id="3c439-115">Breaking a Shadow Copy Set</span></span>](#breaking-a-shadow-copy-set)
-   [<span data-ttu-id="3c439-116">Разбиение набора теневых копий с помощью метода Бреакснапшотсетекс</span><span class="sxs-lookup"><span data-stu-id="3c439-116">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [<span data-ttu-id="3c439-117">Локальное предоставление теневой копии</span><span class="sxs-lookup"><span data-stu-id="3c439-117">Exposing a Shadow Copy Locally</span></span>](#exposing-a-shadow-copy-locally)
-   [<span data-ttu-id="3c439-118">Удаленное предоставление теневой копии</span><span class="sxs-lookup"><span data-stu-id="3c439-118">Exposing a Shadow Copy Remotely</span></span>](#exposing-a-shadow-copy-remotely)
-   [<span data-ttu-id="3c439-119">Вывод сведений о состоянии и метаданных модуля записи</span><span class="sxs-lookup"><span data-stu-id="3c439-119">Listing Writer Status and Metadata</span></span>](#listing-writer-status-and-metadata)
-   [<span data-ttu-id="3c439-120">Выполнение операций восстановления</span><span class="sxs-lookup"><span data-stu-id="3c439-120">Performing Restore Operations</span></span>](#performing-restore-operations)
-   [<span data-ttu-id="3c439-121">Возврат к предыдущей теневой копии</span><span class="sxs-lookup"><span data-stu-id="3c439-121">Reverting to a Previous Shadow Copy</span></span>](#reverting-to-a-previous-shadow-copy)
-   [<span data-ttu-id="3c439-122">Повторная синхронизация LUN</span><span class="sxs-lookup"><span data-stu-id="3c439-122">Resynchronizing LUNs</span></span>](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a><span data-ttu-id="3c439-123">Создание набора теневых копий</span><span class="sxs-lookup"><span data-stu-id="3c439-123">Creating a Shadow Copy Set</span></span>

<span data-ttu-id="3c439-124">**вшадов** \[ Оптионалфлагс \] *волумелист*</span><span class="sxs-lookup"><span data-stu-id="3c439-124">**vshadow** \[OptionalFlags\] *VolumeList*</span></span>

<span data-ttu-id="3c439-125">Эта команда создает новый набор теневых копий.</span><span class="sxs-lookup"><span data-stu-id="3c439-125">This command creates a new shadow copy set.</span></span>

<span data-ttu-id="3c439-126">*Волумелист* — это список имен томов.</span><span class="sxs-lookup"><span data-stu-id="3c439-126">*VolumeList* is a list of volume names.</span></span> <span data-ttu-id="3c439-127">Вшадов создает одну теневую копию для каждого тома в списке.</span><span class="sxs-lookup"><span data-stu-id="3c439-127">VShadow creates one shadow copy for each volume in the list.</span></span> <span data-ttu-id="3c439-128">При необходимости имя тома можно завершить с помощью обратной косой черты ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="3c439-128">A volume name can optionally be terminated with a backslash (\\).</span></span> <span data-ttu-id="3c439-129">Например, C: и C: \\ являются допустимыми именами томов.</span><span class="sxs-lookup"><span data-stu-id="3c439-129">For example, both C: and C:\\ are valid volume names.</span></span> <span data-ttu-id="3c439-130">Можно также указать имена подключенных папок (например, C: \\ директоринаме) или идентификатор GUID тома (например, \\ \\ ? \\ Том {edbed95e-7e8d-11d8-9d01-505054503030}).</span><span class="sxs-lookup"><span data-stu-id="3c439-130">You can also specify mounted folders (for example, C:\\DirectoryName) or volume GUID names (for example, \\\\?\\Volume{edbed95e-7e8d-11d8-9d01-505054503030}).</span></span>

<span data-ttu-id="3c439-131">*Оптионалфлагс* — это битовая маска необязательных значений флагов из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="3c439-131">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c439-132">Необязательное значение флага</span><span class="sxs-lookup"><span data-stu-id="3c439-132">Optional Flag Value</span></span></th>
<th><span data-ttu-id="3c439-133">Описание</span><span class="sxs-lookup"><span data-stu-id="3c439-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c439-134"><span id="-ad"></span><span id="-AD"></span><strong>-AD</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-134"><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-135">Этот необязательный флаг указывает разностное аппаратное теневое копирование.</span><span class="sxs-lookup"><span data-stu-id="3c439-135">This optional flag specifies differential hardware shadow copies.</span></span> <span data-ttu-id="3c439-136">Этот флаг и флаг <strong>-AP</strong> являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="3c439-136">This flag and the <strong>-ap</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-137">Этот флаг поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-137">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c439-138"><span id="-ap"></span><span id="-AP"></span><strong>-AP</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-138"><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-139">Этот необязательный флаг указывает на плекс аппаратных теневых копий.</span><span class="sxs-lookup"><span data-stu-id="3c439-139">This optional flag specifies plex hardware shadow copies.</span></span> <span data-ttu-id="3c439-140">Этот флаг и флаг <strong>-AD</strong> являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="3c439-140">This flag and the <strong>-ad</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-141">Этот флаг поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-141">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c439-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-BC =</strong><em>файл</em><strong>. XML</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span> <strong></strong> <strong>-bc=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-143">Этот необязательный флаг задает непереносимые теневые копии и сохраняет документ компонентов резервного копирования в указанном файле.</span><span class="sxs-lookup"><span data-stu-id="3c439-143">This optional flag specifies non-transportable shadow copies and stores the Backup Components Document into the specified file.</span></span> <span data-ttu-id="3c439-144">Этот файл можно использовать в последующей операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="3c439-144">This file can be used in a subsequent restore operation.</span></span> <span data-ttu-id="3c439-145">Этот флаг и флаг <strong>-t</strong> являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="3c439-145">This flag and the <strong>-t</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-146">Этот флаг поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-146">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c439-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec =</strong>-<em>команда</em></span><span class="sxs-lookup"><span data-stu-id="3c439-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec=</strong><em>Command</em></span></span><br/></td>
<td><span data-ttu-id="3c439-148">Этот необязательный флаг выполняет команду или сценарий после создания теневых копий, но перед завершением работы средства Вшадов.</span><span class="sxs-lookup"><span data-stu-id="3c439-148">This optional flag executes a command or script after the shadow copies are created but before the VShadow tool exits.</span></span> <span data-ttu-id="3c439-149"><em>Команда</em> может указать исполняемую команду оболочки или CMD-файл.</span><span class="sxs-lookup"><span data-stu-id="3c439-149"><em>Command</em> can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="3c439-150">Если он указывает команду оболочки, параметры команды указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="3c439-150">If it specifies a shell command, no command parameters can be specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-151">По соображениям безопасности и для простоты реализации необязательный флаг <strong>-exec</strong> не принимает параметры, передаваемые команде или сценарию.</span><span class="sxs-lookup"><span data-stu-id="3c439-151">For security reasons and to keep the implementation simple, the <strong>-exec</strong> optional flag will not accept parameters to be passed to the command or script.</span></span> <span data-ttu-id="3c439-152">Вся строка, передаваемая в необязательный флаг <strong>-exec</strong> , рассматривается как отдельный файл CMD или exe.</span><span class="sxs-lookup"><span data-stu-id="3c439-152">The entire string passed to the <strong>-exec</strong> optional flag is treated as a single CMD or EXE file.</span></span> <span data-ttu-id="3c439-153">Дополнительные сведения об этом ограничении см. в разделе исходный код Вшадов.</span><span class="sxs-lookup"><span data-stu-id="3c439-153">For more information about this limitation, see the VShadow source code.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c439-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-форцереверт</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-155">Этот необязательный флаг указывает, что операция теневого копирования должна быть выполнена только в том случае, если все подписи диска можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="3c439-155">This optional flag specifies that the shadow copy operation should be completed only if all disk signatures can be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-156">Этот флаг поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-156">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3c439-157"><strong>Windows Server 2003:</strong> Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3c439-157"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c439-158"><span id="-mask"></span><span id="-MASK"></span><strong>-Mask</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-158"><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-159">Этот необязательный флаг указывает, что при разрыве набора теневых копий LUN теневой копии должен быть замаскирован с компьютера.</span><span class="sxs-lookup"><span data-stu-id="3c439-159">This optional flag specifies that the shadow copy LUNs should be masked from the computer when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-160">Этот флаг поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-160">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3c439-161"><strong>Windows Server 2003:</strong> Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3c439-161"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c439-162"><span id="-nar"></span><span id="-NAR"></span><strong>-нар</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-162"><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-163">Этот необязательный флаг указывает теневые копии без автоматического восстановления.</span><span class="sxs-lookup"><span data-stu-id="3c439-163">This optional flag specifies shadow copies without auto-recovery.</span></span> <span data-ttu-id="3c439-164">Дополнительные сведения об этом параметре см. в документации по флагу VSS_VOLSNAP_ATTR_NO_AUTORECOVERY перечисления <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3c439-164">For more information about this option, see the documentation for the VSS_VOLSNAP_ATTR_NO_AUTORECOVERY flag of the <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> enumeration.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c439-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-невозвратно</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-166">Этот необязательный флаг указывает, что не следует выполнять откат для подписей дисков.</span><span class="sxs-lookup"><span data-stu-id="3c439-166">This optional flag specifies that disk signatures should not be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-167">Этот флаг поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-167">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3c439-168"><strong>Windows Server 2003:</strong> Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3c439-168"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c439-169"><span id="-nw"></span><span id="-NW"></span><strong>-NW</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-169"><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-170">Этот необязательный флаг указывает теневые копии без участия в модулях записи.</span><span class="sxs-lookup"><span data-stu-id="3c439-170">This optional flag specifies shadow copies without involving writers.</span></span> <span data-ttu-id="3c439-171">Дополнительные сведения о теневых копиях без участия в записи см. в разделе <a href="shadow-copy-creation-details.md">сведения о создании теневого копирования</a>.</span><span class="sxs-lookup"><span data-stu-id="3c439-171">For more information about shadow copies without writer participation, see <a href="shadow-copy-creation-details.md">Shadow Copy Creation Details</a>.</span></span> <span data-ttu-id="3c439-172">Этот флаг и флаги <strong>-Wi</strong> и <strong>-WX</strong> являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="3c439-172">This flag and the <strong>-wi</strong> and <strong>-wx</strong> flags are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c439-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-174">Этот необязательный флаг указывает <a href="vssgloss-p.md"><em>постоянные теневые копии</em></a>.</span><span class="sxs-lookup"><span data-stu-id="3c439-174">This optional flag specifies <a href="vssgloss-p.md"><em>persistent shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-175">Этот флаг поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-175">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c439-176"><span id="-rw"></span><span id="-RW"></span><strong>-RW</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-176"><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-177">Этот необязательный флаг указывает, что LUN теневой копии должен быть доступен для чтения и записи, если набор теневых копий поврежден.</span><span class="sxs-lookup"><span data-stu-id="3c439-177">This optional flag specifies that the shadow copy LUNs should be made read/write when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-178">Этот флаг поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-178">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3c439-179"><strong>Windows Server 2003:</strong> Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3c439-179"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c439-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-сксф</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-181">Этот необязательный флаг указывает <a href="vssgloss-c.md"><em>теневые копии, доступные для клиента</em></a>.</span><span class="sxs-lookup"><span data-stu-id="3c439-181">This optional flag specifies <a href="vssgloss-c.md"><em>client-accessible shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-182">Этот флаг поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-182">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c439-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script =</strong><em>File</em><strong>. cmd</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script=</strong><em>File</em><strong>.cmd</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-184">Этот необязательный флаг создает CMD-файл, содержащий переменные среды, связанные с созданными теневыми копиями, такие как идентификаторы теневых копий и идентификаторы наборов теневых копий.</span><span class="sxs-lookup"><span data-stu-id="3c439-184">This optional flag generates a CMD file containing environment variables related to the created shadow copies, such as shadow copy IDs and shadow copy set IDs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c439-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>файл File</em><strong>. XML</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-186">Этот необязательный флаг определяет переносимые теневые копии и сохраняет документ компонентов резервного копирования в файл, указанный параметром <em>File.xml</em> .</span><span class="sxs-lookup"><span data-stu-id="3c439-186">This optional flag specifies transportable shadow copies and stores the Backup Components Document into the file specified by the <em>File.xml</em> parameter.</span></span> <span data-ttu-id="3c439-187">Этот файл можно использовать в последующих операциях импорта и (или) восстановления.</span><span class="sxs-lookup"><span data-stu-id="3c439-187">This file can be used in a subsequent import and/or restore operation.</span></span> <span data-ttu-id="3c439-188">Этот флаг и флаг <strong>-BC</strong> являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="3c439-188">This flag and the <strong>-bc</strong> flag are mutually exclusive.</span></span><br/> <span data-ttu-id="3c439-189"><strong>Windows server 2003, Standard Edition и Windows Server 2003, Web Edition:</strong> Перепереносимые теневые копии не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="3c439-189"><strong>Windows Server 2003, Standard Edition and Windows Server 2003, Web Edition:</strong> Transportable shadow copies are not supported.</span></span> <span data-ttu-id="3c439-190">Все выпуски Windows Server 2003 с пакетом обновления 1 (SP1) поддерживают переносимые теневые копии.</span><span class="sxs-lookup"><span data-stu-id="3c439-190">All editions of Windows Server 2003 with Service Pack 1 (SP1) support transportable shadow copies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c439-191"><span id="-tr"></span><span id="-TR"></span><strong>-TR</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-191"><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-192">Этот необязательный флаг указывает, что во время создания теневой копии необходимо принудительно выполнить восстановление TxF.</span><span class="sxs-lookup"><span data-stu-id="3c439-192">This optional flag specifies that TxF recovery should be enforced during shadow copy creation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-193">Этот флаг поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-193">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c439-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-Трассировка</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-tracing</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-195">Этот необязательный флаг создает подробный вывод, который можно использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="3c439-195">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c439-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-Wait</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-197">Этот необязательный флаг заставляет средство Вшадов ждать подтверждения пользователя перед выходом.</span><span class="sxs-lookup"><span data-stu-id="3c439-197">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c439-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-Wi =</strong><em>модуль записи</em></span><span class="sxs-lookup"><span data-stu-id="3c439-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="3c439-199">Этот необязательный флаг проверяет, включен ли указанный модуль записи или компонент в теневую копию.</span><span class="sxs-lookup"><span data-stu-id="3c439-199">This optional flag verifies that the specified writer or component is included in the shadow copy.</span></span> <span data-ttu-id="3c439-200"><em>Модуль записи</em> может указывать путь к компоненту, имя модуля записи, идентификатор модуля записи или идентификатор экземпляра модуля записи.</span><span class="sxs-lookup"><span data-stu-id="3c439-200"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="3c439-201">Этот флаг и флаг <strong>-NW</strong> являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="3c439-201">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c439-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-WX =</strong><em>модуль записи</em></span><span class="sxs-lookup"><span data-stu-id="3c439-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="3c439-203">Этот необязательный флаг проверяет, исключен ли указанный модуль записи или компонент из теневой копии.</span><span class="sxs-lookup"><span data-stu-id="3c439-203">This optional flag verifies that the specified writer or component is excluded from the shadow copy.</span></span> <span data-ttu-id="3c439-204"><em>Модуль записи</em> может указывать путь к компоненту, имя модуля записи, идентификатор модуля записи или идентификатор экземпляра модуля записи.</span><span class="sxs-lookup"><span data-stu-id="3c439-204"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="3c439-205">Этот флаг и флаг <strong>-NW</strong> являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="3c439-205">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a><span data-ttu-id="3c439-206">Импорт набора теневых копий</span><span class="sxs-lookup"><span data-stu-id="3c439-206">Importing a Shadow Copy Set</span></span>

<span data-ttu-id="3c439-207">**вшадов** \[ Оптионалфлагс \] **-i =**_файл File_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="3c439-207">**vshadow** \[OptionalFlags\] **-i=**_File_*_.xml_*</span></span>

<span data-ttu-id="3c439-208">Параметр командной строки **-i** импортирует транспортный набор теневых копий.</span><span class="sxs-lookup"><span data-stu-id="3c439-208">The **-i** command-line option imports a transportable shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="3c439-209">Этот параметр командной строки поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-209">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="3c439-210">Файл *File.xml* должен быть файлом документа компонентов резервного копирования для переносимого набора теневых копий, который был создан с помощью необязательного флага **-t** или **-BC** .</span><span class="sxs-lookup"><span data-stu-id="3c439-210">The *File.xml* file must be a Backup Components Document file for a transportable shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="3c439-211">Набор теневых копий является [*постоянной теневой копией*](vssgloss-p.md) , если он был создан с помощью необязательного флага **-p** .</span><span class="sxs-lookup"><span data-stu-id="3c439-211">A shadow copy set is a [*persistent shadow copy*](vssgloss-p.md) if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="3c439-212">Если транспортный набор теневых копий является непостоянным, он появляется в течение короткого промежутка времени во время выполнения команды создания теневого копирования и автоматически удаляется при возврате команды.</span><span class="sxs-lookup"><span data-stu-id="3c439-212">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="3c439-213">Вы можете импортировать непостоянные теневые копии только во время создания теневого копирования, создав набор теневых копий с помощью флага **-exec** , чтобы выполнить cmd-файл, вызывающий вшадов **– i**.</span><span class="sxs-lookup"><span data-stu-id="3c439-213">You can import nonpersistent shadow copies only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls VShadow **-i**.</span></span>

<span data-ttu-id="3c439-214">Параметр командной строки **-i** не может использоваться вместе с другими параметрами командной строки.</span><span class="sxs-lookup"><span data-stu-id="3c439-214">The **-i** command-line option cannot be combined with other command-line options.</span></span>

<span data-ttu-id="3c439-215">*Оптионалфлагс* — это битовая маска необязательных значений флагов из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="3c439-215">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="3c439-216">Необязательное значение флага</span><span class="sxs-lookup"><span data-stu-id="3c439-216">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="3c439-217">Описание</span><span class="sxs-lookup"><span data-stu-id="3c439-217">Description</span></span>                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c439-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**-_команда_</span><span class="sxs-lookup"><span data-stu-id="3c439-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="3c439-219">Этот необязательный флаг выполняет команду или сценарий после импорта теневых копий, но до завершения работы средства Вшадов.</span><span class="sxs-lookup"><span data-stu-id="3c439-219">This optional flag executes a command or script after the shadow copies are imported but before the VShadow tool exits.</span></span> <span data-ttu-id="3c439-220">*Команда* может указать исполняемую команду оболочки или CMD-файл.</span><span class="sxs-lookup"><span data-stu-id="3c439-220">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="3c439-221">Если он указывает команду оболочки, параметры команды указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="3c439-221">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="3c439-222"><span id="-tracing"></span><span id="-TRACING"></span>**-Трассировка**</span><span class="sxs-lookup"><span data-stu-id="3c439-222"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="3c439-223">Этот необязательный флаг создает подробный вывод, который можно использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="3c439-223">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="3c439-224"><span id="-wait"></span><span id="-WAIT"></span>**-Wait**</span><span class="sxs-lookup"><span data-stu-id="3c439-224"><span id="-wait"></span><span id="-WAIT"></span>**-wait**</span></span><br/>                                                           | <span data-ttu-id="3c439-225">Этот необязательный флаг заставляет средство Вшадов ждать подтверждения пользователя перед выходом.</span><span class="sxs-lookup"><span data-stu-id="3c439-225">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a><span data-ttu-id="3c439-226">Запрос свойств теневого копирования</span><span class="sxs-lookup"><span data-stu-id="3c439-226">Querying Shadow Copy Properties</span></span>

<span data-ttu-id="3c439-227">**вшадов** **-q**</span><span class="sxs-lookup"><span data-stu-id="3c439-227">**vshadow** **-q**</span></span>

<span data-ttu-id="3c439-228">**вшадов** **-ККС =**_шадовкописетид_</span><span class="sxs-lookup"><span data-stu-id="3c439-228">**vshadow** **-qx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="3c439-229">**вшадов** **-s =**_шадовкопид_</span><span class="sxs-lookup"><span data-stu-id="3c439-229">**vshadow** **-s=**_ShadowCopyId_</span></span>

<span data-ttu-id="3c439-230">Параметр командной строки **-q** содержит свойства всех теневых копий на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3c439-230">The **-q** command-line option lists the properties of all shadow copies on the computer.</span></span>

<span data-ttu-id="3c439-231">Параметр командной строки **-ККС** перечисляет свойства всех теневых копий в наборе теневых копий, идентификатор которых указан в параметре *шадовкописетид*.</span><span class="sxs-lookup"><span data-stu-id="3c439-231">The **-qx** command-line option lists the properties of all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="3c439-232">Параметр командной строки **-s** перечисляет свойства теневой копии, идентификатор которой указан в *шадовкопид*.</span><span class="sxs-lookup"><span data-stu-id="3c439-232">The **-s** command-line option lists the properties of the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="3c439-233">Эти параметры командной строки используют сочетание [**ивссбаккупкомпонентс:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) и [**Ивссбаккупкомпонентс:: жетснапшотпропертиес**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) для получения свойств заданного набора теневых копий.</span><span class="sxs-lookup"><span data-stu-id="3c439-233">These command-line options use a combination of [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) and [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) to get the properties of the given set of shadow copies.</span></span>

<span data-ttu-id="3c439-234">Параметры командной строки **-q**, **-ККС** и **-s** являются взаимоисключающими и не могут быть объединены с другими параметрами командной строки.</span><span class="sxs-lookup"><span data-stu-id="3c439-234">The **-q**, **-qx**, and **-s** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="deleting-shadow-copies"></a><span data-ttu-id="3c439-235">Удаление теневых копий</span><span class="sxs-lookup"><span data-stu-id="3c439-235">Deleting Shadow Copies</span></span>

<span data-ttu-id="3c439-236">**вшадов** **-Da**</span><span class="sxs-lookup"><span data-stu-id="3c439-236">**vshadow** **-da**</span></span>

<span data-ttu-id="3c439-237">**вшадов** **-Do**</span><span class="sxs-lookup"><span data-stu-id="3c439-237">**vshadow** **-do**</span></span>

<span data-ttu-id="3c439-238">**вшадов** **-DX =**_шадовкописетид_</span><span class="sxs-lookup"><span data-stu-id="3c439-238">**vshadow** **-dx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="3c439-239">**вшадов** **-DS =**_шадовкопид_</span><span class="sxs-lookup"><span data-stu-id="3c439-239">**vshadow** **-ds=**_ShadowCopyId_</span></span>

<span data-ttu-id="3c439-240">Команда **-Da** удаляет все теневые копии на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3c439-240">The **-da** command deletes all shadow copies on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="3c439-241">Параметр командной строки **-Da** требует подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c439-241">The **-da** command-line option requires user confirmation.</span></span>

 

<span data-ttu-id="3c439-242">Параметр командной строки **-Do** удаляет старую теневую копию на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3c439-242">The **-do** command-line option deletes the oldest shadow copy on the computer.</span></span>

<span data-ttu-id="3c439-243">Параметр командной строки **-DX** удаляет все теневые копии в наборе теневых копий, идентификатор которых указан в параметре *шадовкописетид*.</span><span class="sxs-lookup"><span data-stu-id="3c439-243">The **-dx** command-line option deletes all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="3c439-244">Параметр командной строки **-DS** удаляет теневую копию, идентификатор которой указан в *шадовкопид*.</span><span class="sxs-lookup"><span data-stu-id="3c439-244">The **-ds** command-line option deletes the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="3c439-245">Эти параметры командной строки предназначены для использования только с [*постоянными теневыми копиями*](vssgloss-p.md) .</span><span class="sxs-lookup"><span data-stu-id="3c439-245">These command-line options are for use with [*persistent shadow copies*](vssgloss-p.md) only.</span></span> <span data-ttu-id="3c439-246">Непостоянные теневые копии не нужно удалять явным образом, так как они автоматически удаляются при выходе из команды Вшадов-создания.</span><span class="sxs-lookup"><span data-stu-id="3c439-246">Nonpersistent shadow copies do not need to be explicitly deleted, because they are automatically deleted when the VShadow creation command exits.</span></span>

<span data-ttu-id="3c439-247">Параметры командной строки **-Da**, **-Do**, **-DX** и **-DS** являются взаимоисключающими и не могут быть объединены с другими параметрами командной строки.</span><span class="sxs-lookup"><span data-stu-id="3c439-247">The **-da**, **-do**, **-dx**, and **-ds** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set"></a><span data-ttu-id="3c439-248">Разбиение набора теневых копий</span><span class="sxs-lookup"><span data-stu-id="3c439-248">Breaking a Shadow Copy Set</span></span>

<span data-ttu-id="3c439-249">**вшадов** **-b =**_шадовкописетид_</span><span class="sxs-lookup"><span data-stu-id="3c439-249">**vshadow** **-b=**_ShadowCopySetId_</span></span>

<span data-ttu-id="3c439-250">**вшадов** **-BW =**_шадовкописетид_</span><span class="sxs-lookup"><span data-stu-id="3c439-250">**vshadow** **-bw=**_ShadowCopySetId_</span></span>

<span data-ttu-id="3c439-251">Параметр командной строки **-b =**_шадовкописетид_ преобразует каждую теневую копию в наборе теневых копий в изолированный том только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3c439-251">The **-b=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone read-only volume.</span></span>

<span data-ttu-id="3c439-252">Параметр командной строки **-BW =**_шадовкописетид_ преобразует каждую теневую копию в наборе теневых копий в изолированный доступный для записи том.</span><span class="sxs-lookup"><span data-stu-id="3c439-252">The **-bw=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone writable volume.</span></span>

> [!Note]  
> <span data-ttu-id="3c439-253">Параметры командной строки **-b** и **-BW** поддерживаются только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-253">The **-b** and **-bw** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="3c439-254">Сведения о разбиении набора теневых копий см. в разделе [критическое копирование теневых копий](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="3c439-254">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

<span data-ttu-id="3c439-255">После разрыва набора теневых копий набор теневых копий и отдельные теневые копии больше не существуют и не могут управляться с помощью команд VSS.</span><span class="sxs-lookup"><span data-stu-id="3c439-255">After the shadow copy set is broken, the shadow copy set and the individual shadow copies no longer exist and cannot be managed using VSS commands.</span></span>

<span data-ttu-id="3c439-256">Набор теневых копий является постоянным, если он был создан с помощью необязательного флага **-p** .</span><span class="sxs-lookup"><span data-stu-id="3c439-256">A shadow copy set is persistent if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="3c439-257">Если транспортный набор теневых копий является непостоянным, он появляется в течение короткого промежутка времени во время выполнения команды создания теневого копирования и автоматически удаляется при возврате команды.</span><span class="sxs-lookup"><span data-stu-id="3c439-257">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="3c439-258">Неустойчивые наборы теневых копий можно прерывать только во время создания теневого копирования, создав набор теневых копий с помощью флага **-exec** , чтобы выполнить cmd-файл, вызывающий **вшадов** **– b** или **вшадов** **-BW**.</span><span class="sxs-lookup"><span data-stu-id="3c439-258">You can break nonpersistent shadow copy sets only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls **vshadow** **-b** or **vshadow** **-bw**.</span></span>

<span data-ttu-id="3c439-259">Параметры командной строки **-b** и **-BW** являются взаимоисключающими и не могут быть объединены с другими параметрами командной строки.</span><span class="sxs-lookup"><span data-stu-id="3c439-259">The **-b** and **-bw** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="3c439-260">Разбиение набора теневых копий с помощью метода Бреакснапшотсетекс</span><span class="sxs-lookup"><span data-stu-id="3c439-260">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="3c439-261">**вшадов** **— BEX**</span><span class="sxs-lookup"><span data-stu-id="3c439-261">**vshadow** **-bex**</span></span>

<span data-ttu-id="3c439-262">Параметр командной строки **-BEX** прерывает набор теневых копий в соответствии с параметрами, заданными флагами необязательных параметров **-Mask**, **-RW**, **-форцереверт** и **-не revert** .</span><span class="sxs-lookup"><span data-stu-id="3c439-262">The **-bex** command-line option breaks a shadow copy set according to the options specified by the optional **-mask**, **-rw**, **-forcerevert**, and **-norevert** flags.</span></span> <span data-ttu-id="3c439-263">Этот параметр командной строки похож на параметры командной строки **-b** и **-BW** .</span><span class="sxs-lookup"><span data-stu-id="3c439-263">This command-line option is similar to the **-b** and **-bw** command-line options.</span></span> <span data-ttu-id="3c439-264">Параметр командной строки **-BEX** использует метод [**IVssBackupComponentsEx2:: бреакснапшотсетекс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) , тогда как параметры командной строки **-b** и **-BW** используют метод [**ивссбаккупкомпонентс:: бреакснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .</span><span class="sxs-lookup"><span data-stu-id="3c439-264">The **-bex** command-line option uses the [**IVssBackupComponentsEx2::BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) method, whereas the **-b** and **-bw** command-line options use the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>

<span data-ttu-id="3c439-265">Сведения о разбиении набора теневых копий см. в разделе [критическое копирование теневых копий](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="3c439-265">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

> [!Note]  
> <span data-ttu-id="3c439-266">Параметр командной строки **-BEX** поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-266">The **-bex** command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="3c439-267">**вшадов** **-BEX** **-Mask**</span><span class="sxs-lookup"><span data-stu-id="3c439-267">**vshadow** **-bex** **-mask**</span></span>

<span data-ttu-id="3c439-268">Флаг **-Mask** указывает, что LUN теневой копии будет маскироваться от узла.</span><span class="sxs-lookup"><span data-stu-id="3c439-268">The **-mask** flag specifies that the shadow copy LUN will be masked from the host.</span></span> <span data-ttu-id="3c439-269">Если указан флаг **-Mask** , то флаги **-RW**, **-форцереверт** и **-** не могут быть указаны.</span><span class="sxs-lookup"><span data-stu-id="3c439-269">If the **-mask** flag is specified, the **-rw**, **-forcerevert**, and **-norevert** flags cannot be specified.</span></span>

<span data-ttu-id="3c439-270">**вшадов** **-BEX** **-RW**</span><span class="sxs-lookup"><span data-stu-id="3c439-270">**vshadow** **-bex** **-rw**</span></span>

<span data-ttu-id="3c439-271">Флаг **-RW** указывает, что LUN теневой копии будет предоставляться узлу в качестве тома для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3c439-271">The **-rw** flag specifies that the shadow copy LUN will be exposed to the host as a read/write volume.</span></span>

<span data-ttu-id="3c439-272">**вшадов** **-BEX** **-форцереверт**</span><span class="sxs-lookup"><span data-stu-id="3c439-272">**vshadow** **-bex** **-forcerevert**</span></span>

<span data-ttu-id="3c439-273">Флаг **-форцереверт** указывает, что идентификаторы дисков всех LUN теневой копии будут возвращены к исходным LUN.</span><span class="sxs-lookup"><span data-stu-id="3c439-273">The **-forcerevert** flag specifies that the disk identifiers of all of the shadow copy LUNs will be reverted to that of the original LUNs.</span></span> <span data-ttu-id="3c439-274">Однако если в системе имеются какие либо исходные LUN, операция завершится ошибкой и ни один из идентификаторов не будет отменен.</span><span class="sxs-lookup"><span data-stu-id="3c439-274">However, if any of the original LUNs are present on the system, the operation will fail and none of the identifiers will be reverted.</span></span> <span data-ttu-id="3c439-275">Этот флаг и флаг **-без изменений** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="3c439-275">This flag and the **-norevert** flag are mutually exclusive.</span></span>

<span data-ttu-id="3c439-276">**вшадов** **-BEX** **-revert**</span><span class="sxs-lookup"><span data-stu-id="3c439-276">**vshadow** **-bex** **-norevert**</span></span>

<span data-ttu-id="3c439-277">Флаг **-with revert** указывает, что ни один из идентификаторов диска LUN теневой копии не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="3c439-277">The **-norevert** flag specifies that none of the shadow copy LUN disk identifiers will be reverted.</span></span> <span data-ttu-id="3c439-278">Этот флаг и флаг **-форцереверт** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="3c439-278">This flag and the **-forcerevert** flag are mutually exclusive.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="3c439-279">Локальное предоставление теневой копии</span><span class="sxs-lookup"><span data-stu-id="3c439-279">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="3c439-280">**вшадов** **-El =**_шадовкопид_*_,_*_локалемптидиректори_</span><span class="sxs-lookup"><span data-stu-id="3c439-280">**vshadow** **-el=**_ShadowCopyId_*_,_*_LocalEmptyDirectory_</span></span>

 <span data-ttu-id="3c439-281">**вшадов** **-El =**_шадовкопид_*_,_*_унуседдривелеттер_</span><span class="sxs-lookup"><span data-stu-id="3c439-281">**vshadow** **-el=**_ShadowCopyId_*_,_*_UnusedDriveLetter_</span></span>

<span data-ttu-id="3c439-282">Параметр командной строки **-El** назначает подключенной папке или букве диска постоянную теневую копию.</span><span class="sxs-lookup"><span data-stu-id="3c439-282">The **-el** command-line option assigns a mounted folder or a drive letter to a persistent shadow copy.</span></span> <span data-ttu-id="3c439-283">Обратите внимание, что содержимое тома будет доступно только для чтения, пока вы не назовите **вшадов** **-BW** , чтобы нарушить набор теневых копий.</span><span class="sxs-lookup"><span data-stu-id="3c439-283">Note that the volume contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="3c439-284">Непостоянные теневые копии и [*теневые копии, доступные для клиента*](vssgloss-c.md) , нельзя предоставлять локально.</span><span class="sxs-lookup"><span data-stu-id="3c439-284">Nonpersistent shadow copies and [*client-accessible shadow copies*](vssgloss-c.md) cannot be exposed locally.</span></span>

 

<span data-ttu-id="3c439-285">Например, если {edbed95e-7e8d-11d8-9d01-505054503030} является идентификатором GUID существующей сохраняемой теневой копии, а X: является неиспользуемой буквой диска, следующая команда предоставляет теневую копию в разделе X:</span><span class="sxs-lookup"><span data-stu-id="3c439-285">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and X: is an unused drive letter, the following command exposes the shadow copy under X:</span></span>

<span data-ttu-id="3c439-286">**вшадов** **-El = {edbed95e-7e8d-11d8-9d01-505054503030}, x:**</span><span class="sxs-lookup"><span data-stu-id="3c439-286">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},x:**</span></span>

<span data-ttu-id="3c439-287">В следующем примере показано, как предоставить ту же теневую копию в подключенной папке C: \\ шадовкопиес \\ June23:</span><span class="sxs-lookup"><span data-stu-id="3c439-287">The following example shows how to expose the same shadow copy under the mounted folder C:\\ShadowCopies\\June23:</span></span>

<span data-ttu-id="3c439-288">**mkdir c: \\ шадовкопиес \\ June23**</span><span class="sxs-lookup"><span data-stu-id="3c439-288">**mkdir c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="3c439-289">**вшадов** **-El = {edbed95e-7e8d-11d8-9d01-505054503030}, c: \\ шадовкопиес \\ June23**</span><span class="sxs-lookup"><span data-stu-id="3c439-289">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="3c439-290">Параметр командной строки **-El** не может использоваться вместе с другими параметрами командной строки.</span><span class="sxs-lookup"><span data-stu-id="3c439-290">The **-el** command-line option cannot be combined with other command-line options.</span></span>

## <a name="exposing-a-shadow-copy-remotely"></a><span data-ttu-id="3c439-291">Удаленное предоставление теневой копии</span><span class="sxs-lookup"><span data-stu-id="3c439-291">Exposing a Shadow Copy Remotely</span></span>

<span data-ttu-id="3c439-292">**вшадов** **-ER =**_шадовкопид_*_,_*_унуседшаренаме_</span><span class="sxs-lookup"><span data-stu-id="3c439-292">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_</span></span>

 <span data-ttu-id="3c439-293">**вшадов** **-ER =**_шадовкопид_*_,_*_унуседшаренаме_*_,_*_пасфромрутоншадов_</span><span class="sxs-lookup"><span data-stu-id="3c439-293">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_</span></span>

<span data-ttu-id="3c439-294">Параметр командной строки **-ER** назначает имя общего ресурса только для чтения корневому каталогу (или подкаталогу) из теневой копии.</span><span class="sxs-lookup"><span data-stu-id="3c439-294">The **-er** command-line option assigns a read-only share name to the root directory (or a subdirectory) from the shadow copy.</span></span> <span data-ttu-id="3c439-295">Обратите внимание, что содержимое общей папки будет доступно только для чтения, пока вы не назовите **вшадов** **-BW** , чтобы нарушить набор теневых копий.</span><span class="sxs-lookup"><span data-stu-id="3c439-295">Note that the share contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="3c439-296">[*Доступ к теневым копиям, доступным для клиента*](vssgloss-c.md) , нельзя предоставить удаленно.</span><span class="sxs-lookup"><span data-stu-id="3c439-296">[*Client-accessible shadow copies*](vssgloss-c.md) cannot be exposed remotely.</span></span>

 

<span data-ttu-id="3c439-297">Например, если {edbed95e-7e8d-11d8-9d01-505054503030} является идентификатором GUID существующей сохраняемой теневой копии, а общий ресурс \_ 123 является неиспользуемым именем общей папки, то следующая команда предоставляет теневую копию в разделе share \_ 123:</span><span class="sxs-lookup"><span data-stu-id="3c439-297">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and share\_123 is an unused share name, the following command exposes the shadow copy under share\_123:</span></span>

<span data-ttu-id="3c439-298">**вшадов** **-ER = {edbed95e-7e8d-11d8-9d01-505054503030}, общий ресурс \_ 123**</span><span class="sxs-lookup"><span data-stu-id="3c439-298">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123**</span></span>

<span data-ttu-id="3c439-299">В следующем примере показано, как предоставить только поддерево (с именем "папка1 \\ folder2") той же теневой копии в той же общей папке:</span><span class="sxs-lookup"><span data-stu-id="3c439-299">The following example shows how to expose only a subtree (named "Folder1\\Folder2") of the same shadow copy under the same share:</span></span>

<span data-ttu-id="3c439-300">**вшадов** **-ER = {edbed95e-7e8d-11d8-9d01-505054503030}, Share \_ 123, папка1 \\ folder2**</span><span class="sxs-lookup"><span data-stu-id="3c439-300">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123,Folder1\\Folder2**</span></span>

<span data-ttu-id="3c439-301">Параметр командной строки **-ER** не может использоваться вместе с другими параметрами командной строки.</span><span class="sxs-lookup"><span data-stu-id="3c439-301">The **-er** command-line option cannot be combined with other command-line options.</span></span>

## <a name="listing-writer-status-and-metadata"></a><span data-ttu-id="3c439-302">Вывод сведений о состоянии и метаданных модуля записи</span><span class="sxs-lookup"><span data-stu-id="3c439-302">Listing Writer Status and Metadata</span></span>

<span data-ttu-id="3c439-303">**вшадов** **-WS**</span><span class="sxs-lookup"><span data-stu-id="3c439-303">**vshadow** **-ws**</span></span>

<span data-ttu-id="3c439-304">**вшадов** **-WM**</span><span class="sxs-lookup"><span data-stu-id="3c439-304">**vshadow** **-wm**</span></span>

<span data-ttu-id="3c439-305">**вшадов** **— wm2**</span><span class="sxs-lookup"><span data-stu-id="3c439-305">**vshadow** **-wm2**</span></span>

<span data-ttu-id="3c439-306">**вшадов** **— WM3**</span><span class="sxs-lookup"><span data-stu-id="3c439-306">**vshadow** **-wm3**</span></span>

<span data-ttu-id="3c439-307">Параметр командной строки **-WS** перечисляет модули записи VSS, которые в данный момент выполняются на компьютере, и описывает их состояние.</span><span class="sxs-lookup"><span data-stu-id="3c439-307">The **-ws** command-line option enumerates the VSS writers that are currently running on the computer and describes their state.</span></span> <span data-ttu-id="3c439-308">Эта команда эквивалентна команде [vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="3c439-308">This command is the equivalent of the [Vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) command.</span></span> <span data-ttu-id="3c439-309">Существует шесть возможных значений состояния: стабильный, сбойный, неизвестный, ожидание фиксации, замораживания и ожидание завершения.</span><span class="sxs-lookup"><span data-stu-id="3c439-309">There are six possible state values: Stable, Failed, Unknown, Waiting for freeze, Frozen, and Waiting for completion.</span></span>

<span data-ttu-id="3c439-310">Параметр командной строки **-WM** содержит сводку метаданных модуля записи, включая затронутые тома.</span><span class="sxs-lookup"><span data-stu-id="3c439-310">The **-wm** command-line option lists a summary of the writer metadata, including the affected volumes.</span></span>

<span data-ttu-id="3c439-311">Параметр командной строки **-wm2** перечисляет все метаданные модуля записи.</span><span class="sxs-lookup"><span data-stu-id="3c439-311">The **-wm2** command-line option lists all writer metadata.</span></span>

<span data-ttu-id="3c439-312">Параметр командной строки **-WM3** перечисляет все метаданные модуля записи в формате RAW XML.</span><span class="sxs-lookup"><span data-stu-id="3c439-312">The **-wm3** command-line option lists all writer metadata in raw XML format.</span></span>

<span data-ttu-id="3c439-313">**Windows Vista и Windows Server 2003:** Параметр командной строки **-WM3** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3c439-313">**Windows Vista and Windows Server 2003:** The **-wm3** command-line option is not supported.</span></span>

<span data-ttu-id="3c439-314">Эти сведения можно использовать, чтобы определить, какие тома следует включить в набор теневых копий томов.</span><span class="sxs-lookup"><span data-stu-id="3c439-314">You can use this information to determine which volumes to include in the volume shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="3c439-315">Если состояние модуля записи является стабильным или ожидает завершения, модуль записи может считаться в стабильном состоянии, готовым к следующей резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3c439-315">If the writer state is Stable or Waiting for completion, the writer can be considered to be in a stable state, ready for the next backup.</span></span>

 

<span data-ttu-id="3c439-316">Параметры командной строки **-WS**, **-WM**, **-wm2** и **-WM3** являются взаимоисключающими и не могут использоваться вместе с другими параметрами командной строки.</span><span class="sxs-lookup"><span data-stu-id="3c439-316">The **-ws**, **-wm**, **-wm2**, and **-wm3** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="performing-restore-operations"></a><span data-ttu-id="3c439-317">Выполнение операций восстановления</span><span class="sxs-lookup"><span data-stu-id="3c439-317">Performing Restore Operations</span></span>

<span data-ttu-id="3c439-318">**вшадов** \[ Оптионалфлагс \] **-r =**_файл_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="3c439-318">**vshadow** \[OptionalFlags\] **-r=**_File_*_.xml_*</span></span>

<span data-ttu-id="3c439-319">**вшадов** \[ Оптионалфлагс \] **-RS =**_файл_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="3c439-319">**vshadow** \[OptionalFlags\] **-rs=**_File_*_.xml_*</span></span>

<span data-ttu-id="3c439-320">Параметр командной строки **-r** выполняет операцию восстановления.</span><span class="sxs-lookup"><span data-stu-id="3c439-320">The **-r** command-line option performs a restore operation.</span></span>

<span data-ttu-id="3c439-321">Параметр командной строки **-RS** выполняет имитацию операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="3c439-321">The **-rs** command-line option performs a simulated restore operation.</span></span>

<span data-ttu-id="3c439-322">Файл *File.xml* должен быть файлом документа компонентов резервного копирования для набора теневых копий, который был создан с помощью необязательного флага **-t** или **-BC** .</span><span class="sxs-lookup"><span data-stu-id="3c439-322">The *File.xml* file must be a Backup Components Document file for a shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="3c439-323">Параметры командной строки **-r** и **-RS** являются взаимоисключающими и не могут использоваться совместно с другими параметрами командной строки.</span><span class="sxs-lookup"><span data-stu-id="3c439-323">The **-r** and **-rs** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

<span data-ttu-id="3c439-324">*Оптионалфлагс* — это битовая маска необязательных значений флагов из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="3c439-324">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="3c439-325">Необязательное значение флага</span><span class="sxs-lookup"><span data-stu-id="3c439-325">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="3c439-326">Описание</span><span class="sxs-lookup"><span data-stu-id="3c439-326">Description</span></span>                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c439-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-Wi =**_модуль записи_</span><span class="sxs-lookup"><span data-stu-id="3c439-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi=**_Writer_</span></span><br/>             | <span data-ttu-id="3c439-328">Этот необязательный флаг проверяет, включен ли указанный модуль записи или компонент в восстановление.</span><span class="sxs-lookup"><span data-stu-id="3c439-328">This optional flag verifies that the specified writer or component is included in the restore.</span></span> <span data-ttu-id="3c439-329">*Модуль записи* может указывать путь к компоненту, имя модуля записи, идентификатор модуля записи или идентификатор экземпляра модуля записи.</span><span class="sxs-lookup"><span data-stu-id="3c439-329">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                    |
| <span data-ttu-id="3c439-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-WX =**_модуль записи_</span><span class="sxs-lookup"><span data-stu-id="3c439-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx=**_Writer_</span></span><br/>             | <span data-ttu-id="3c439-331">Этот необязательный флаг проверяет, исключен ли указанный модуль записи или компонент из восстановления.</span><span class="sxs-lookup"><span data-stu-id="3c439-331">This optional flag verifies that the specified writer or component is excluded from the restore.</span></span> <span data-ttu-id="3c439-332">*Модуль записи* может указывать путь к компоненту, имя модуля записи, идентификатор модуля записи или идентификатор экземпляра модуля записи.</span><span class="sxs-lookup"><span data-stu-id="3c439-332">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="3c439-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**-_команда_</span><span class="sxs-lookup"><span data-stu-id="3c439-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="3c439-334">Этот необязательный флаг выполняет команду или скрипт между событиями перед восстановлением и после восстановления, которые отправляются модулям записи.</span><span class="sxs-lookup"><span data-stu-id="3c439-334">This optional flag executes a command or script between the pre-restore and post-restore events that are sent to the writers.</span></span> <span data-ttu-id="3c439-335">*Команда* может указать исполняемую команду оболочки или CMD-файл.</span><span class="sxs-lookup"><span data-stu-id="3c439-335">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="3c439-336">Если он указывает команду оболочки, параметры команды указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="3c439-336">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="3c439-337"><span id="-tracing"></span><span id="-TRACING"></span>**-Трассировка**</span><span class="sxs-lookup"><span data-stu-id="3c439-337"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="3c439-338">Этот необязательный флаг создает подробный вывод, который можно использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="3c439-338">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a><span data-ttu-id="3c439-339">Возврат к предыдущей теневой копии</span><span class="sxs-lookup"><span data-stu-id="3c439-339">Reverting to a Previous Shadow Copy</span></span>

<span data-ttu-id="3c439-340">**вшадов** **-revert =**_шадовкопид_</span><span class="sxs-lookup"><span data-stu-id="3c439-340">**vshadow** **-revert=**_ShadowCopyId_</span></span>

> [!Note]  
> <span data-ttu-id="3c439-341">Этот параметр командной строки поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-341">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="3c439-342">**Windows server 2008 и Windows server 2003:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3c439-342">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="3c439-343">Параметр командной строки **-revert** восстанавливает из тома предыдущую теневую копию, идентификатор которой указан в *шадовкопид*.</span><span class="sxs-lookup"><span data-stu-id="3c439-343">The **-revert** command-line option reverts a volume to the previous shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="3c439-344">Параметр командной строки **-revert** не может использоваться вместе с другими параметрами командной строки.</span><span class="sxs-lookup"><span data-stu-id="3c439-344">The **-revert** command-line option cannot be combined with other command-line options.</span></span>

## <a name="resynchronizing-luns"></a><span data-ttu-id="3c439-345">Повторная синхронизация LUN</span><span class="sxs-lookup"><span data-stu-id="3c439-345">Resynchronizing LUNs</span></span>

<span data-ttu-id="3c439-346">**вшадов** **-аддресинк =**_шадовкопид_ **— Повторная синхронизация =**_бкдфиленаме_ \[ оптионалресинкфлагс\]</span><span class="sxs-lookup"><span data-stu-id="3c439-346">**vshadow** **-addresync=**_ShadowCopyId_ **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="3c439-347">**вшадов** **-аддресинк =**_шадовкопид_*_,_* *таржетволумедривелеттер* **-Resync =**_бкдфиленаме_ \[ оптионалресинкфлагс\]</span><span class="sxs-lookup"><span data-stu-id="3c439-347">**vshadow** **-addresync=**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="3c439-348">Параметр командной строки **-аддресинк** указывает тома, которые будут включаться в операцию повторной синхронизации LUN.</span><span class="sxs-lookup"><span data-stu-id="3c439-348">The **-addresync** command-line option specifies the volumes to be included in a LUN resynchronization operation.</span></span> <span data-ttu-id="3c439-349">Параметр *шадовкопид* задает идентификатор теневой копии.</span><span class="sxs-lookup"><span data-stu-id="3c439-349">The *ShadowCopyId* parameter specifies the identifier of the shadow copy.</span></span> <span data-ttu-id="3c439-350">Необязательный параметр *таржетволумедривелеттер* указывает том назначения, куда будут копироваться содержимое тома теневой копии.</span><span class="sxs-lookup"><span data-stu-id="3c439-350">The optional *TargetVolumeDriveLetter* parameter specifies the destination volume where the contents of the shadow copy volume are to be copied.</span></span>

<span data-ttu-id="3c439-351">Параметр командной строки **-Resync** инициирует операцию повторной синхронизации LUN.</span><span class="sxs-lookup"><span data-stu-id="3c439-351">The **-resync** command-line option initiates a LUN resynchronization operation.</span></span> <span data-ttu-id="3c439-352">После завершения операции сигнатура каждого целевого LUN будет совпадать с подписью LUN целевого тома.</span><span class="sxs-lookup"><span data-stu-id="3c439-352">After the operation is complete, the signature of each target LUN should be identical to that of the target volume LUN.</span></span> <span data-ttu-id="3c439-353">Параметр *бкдфиленаме* указывает имя XML-файла, содержащего документ компонента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="3c439-353">The *BCDFileName* parameter specifies the name of the XML file that contains the Backup Component Document.</span></span>

> [!Note]  
> <span data-ttu-id="3c439-354">Параметры командной строки **-аддресинк** и **-Resync** поддерживаются только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-354">The **-addresync** and **-resync** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="3c439-355">**Windows server 2008 и Windows server 2003:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3c439-355">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="3c439-356">*Оптионалресинкфлагс* — это битовая маска необязательных значений флагов из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="3c439-356">*OptionalResyncFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c439-357">Необязательное значение флага</span><span class="sxs-lookup"><span data-stu-id="3c439-357">Optional flag value</span></span></th>
<th><span data-ttu-id="3c439-358">Описание</span><span class="sxs-lookup"><span data-stu-id="3c439-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c439-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-ревертсиг</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-360">Этот необязательный флаг указывает, что после завершения операции подпись каждого целевого LUN должна быть идентична исходной LUN, использованной для создания теневой копии, а не LUN целевого тома.</span><span class="sxs-lookup"><span data-stu-id="3c439-360">This optional flag specifies that after the operation is complete, the signature of each target LUN should be identical to that of the original LUN that was used to create the shadow copy, not the target volume LUN.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-361">Флаг <strong>-ревертсиг</strong> поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-361">The <strong>-revertsig</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3c439-362"><strong>Windows server 2008 и Windows server 2003:</strong> Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3c439-362"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c439-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-новолчекк</strong></span><span class="sxs-lookup"><span data-stu-id="3c439-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span></span><br/></td>
<td><span data-ttu-id="3c439-364">Этот необязательный флаг указывает, что службе VSS не следует проверять наличие невыбранных томов, которые будут перезаписаны операцией повторной синхронизации LUN.</span><span class="sxs-lookup"><span data-stu-id="3c439-364">This optional flag specifies that the VSS service should not check for unselected volumes that would be overwritten by the LUN resynchronization operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3c439-365">Флаг <strong>-новолчекк</strong> поддерживается только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c439-365">The <strong>-novolcheck</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3c439-366"><strong>Windows server 2008 и Windows server 2003:</strong> Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3c439-366"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 
