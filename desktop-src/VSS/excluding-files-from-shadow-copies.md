---
description: В Windows Vista и Windows Server 2008 и более поздних версиях разработчик модуля записи VSS или приложения может исключить определенные файлы из теневых копий.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Исключение файлов из теневых копий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52546c8ddc6da62433dc610f2bf4fc2c46c5e53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272585"
---
# <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="7698d-103">Исключение файлов из теневых копий</span><span class="sxs-lookup"><span data-stu-id="7698d-103">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="7698d-104">В Windows Vista и Windows Server 2008 и более поздних версиях разработчик модуля записи VSS или приложения может исключить определенные файлы из теневых копий.</span><span class="sxs-lookup"><span data-stu-id="7698d-104">In Windows Vista and Windows Server 2008 and later, the developer of a VSS writer or application may choose to exclude certain files from shadow copies.</span></span>

<span data-ttu-id="7698d-105">Влияние на производительность и область хранения теневых копий (также называемое «областью копирования») файла в теневой копии напрямую связаны с объемом изменений в содержимом файла после создания теневой копии.</span><span class="sxs-lookup"><span data-stu-id="7698d-105">The performance impact and shadow copy storage area (also called "diff area") usage of a file in a shadow copy are directly related to the amount of change in the file's contents after the shadow copy is created.</span></span> <span data-ttu-id="7698d-106">Кроме того, исключение файлов из теневых копий может замедлить создание теневых копий.</span><span class="sxs-lookup"><span data-stu-id="7698d-106">In addition, excluding files from shadow copies may slow down shadow copy creation.</span></span>

<span data-ttu-id="7698d-107">По этим причинам файл должен быть исключен из теневых копий только в том случае, если он большой, не требует значительных изменений между одной теневой копией и следующей и не нуждается в резервном копировании.</span><span class="sxs-lookup"><span data-stu-id="7698d-107">For these reasons, a file should be excluded from shadow copies only if it is large, undergoes significant change between one shadow copy and the next, and does not need to be backed up.</span></span>

<span data-ttu-id="7698d-108">Следует исключать только файлы, принадлежащие приложению.</span><span class="sxs-lookup"><span data-stu-id="7698d-108">You should only exclude files that belong to your application.</span></span>

<span data-ttu-id="7698d-109">Если \_ в контексте теневого копирования не установлен флаг "VOLSNAP" для VSS, то \_ \_ \_ это означает, что автоматическое восстановление отключено и никакие файлы не могут быть исключены из теневой копии.</span><span class="sxs-lookup"><span data-stu-id="7698d-109">If the VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY flag is set in the shadow copy context, this means that auto-recovery is disabled, and no files can be excluded from the shadow copy.</span></span> <span data-ttu-id="7698d-110">Дополнительные сведения см. в разделе Перечисление [**\_ \_ \_ \_ атрибутов моментальных снимков тома VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) .</span><span class="sxs-lookup"><span data-stu-id="7698d-110">For more information, see the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration.</span></span>

## <a name="using-the-addexcludefilesfromsnapshot-method"></a><span data-ttu-id="7698d-111">Использование метода Аддексклудефилесфромснапшот</span><span class="sxs-lookup"><span data-stu-id="7698d-111">Using the AddExcludeFilesFromSnapshot Method</span></span>

<span data-ttu-id="7698d-112">Модуль записи VSS может исключить файлы из теневой копии следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7698d-112">A VSS writer can exclude files from a shadow copy as follows:</span></span>

1.  <span data-ttu-id="7698d-113">Вызовите метод [**ивсскреатевритерметадатаекс:: аддексклудефилесфромснапшот**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) , чтобы сообщить исключаемые файлы.</span><span class="sxs-lookup"><span data-stu-id="7698d-113">Call the [**IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) method to report the files to be excluded.</span></span>
2.  <span data-ttu-id="7698d-114">В методе [**квссвритер:: онпостснапшот**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) модуля записи удалите файлы из теневой копии.</span><span class="sxs-lookup"><span data-stu-id="7698d-114">In the writer's [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) method, delete the files from the shadow copy.</span></span>

## <a name="using-the-filesnottosnapshot-registry-key"></a><span data-ttu-id="7698d-115">Использование раздела реестра Филесноттоснапшот</span><span class="sxs-lookup"><span data-stu-id="7698d-115">Using the FilesNotToSnapshot Registry Key</span></span>

> [!Note]  
> <span data-ttu-id="7698d-116">Раздел реестра **FilesNotToSnapshot** предназначен для использования только приложениями.</span><span class="sxs-lookup"><span data-stu-id="7698d-116">The **FilesNotToSnapshot** registry key is intended to be used only by applications.</span></span> <span data-ttu-id="7698d-117">Пользователи, пытающиеся использовать этот раздел, сталкиваются с приведенными ниже ограничениями.</span><span class="sxs-lookup"><span data-stu-id="7698d-117">Users who attempt to use it will encounter limitations such as the following:</span></span>
>
> -   <span data-ttu-id="7698d-118">Он не может удалять файлы из теневой копии, созданной на Windows Server, с помощью функции "Предыдущие версии".</span><span class="sxs-lookup"><span data-stu-id="7698d-118">It cannot delete files from a shadow copy that was created on a Windows Server by using the Previous Versions feature.</span></span>
> -   <span data-ttu-id="7698d-119">Он не может удалить файлы из теневых копий общих папок.</span><span class="sxs-lookup"><span data-stu-id="7698d-119">It cannot delete files from shadow copies for shared folders.</span></span>
> -   <span data-ttu-id="7698d-120">Он может удалять файлы из теневой копии, созданной с помощью служебной программы [Diskshadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) , но не может удалять файлы из теневой копии, созданной с помощью программы [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="7698d-120">It can delete files from a shadow copy that was created by using the [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) utility, but it cannot delete files from a shadow copy that was created by using the [Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) utility.</span></span>
> -   <span data-ttu-id="7698d-121">Файлы удаляются из теневой копии при наличии соответствующих ресурсов и возможностей.</span><span class="sxs-lookup"><span data-stu-id="7698d-121">Files are deleted from a shadow copy on a best-effort basis.</span></span> <span data-ttu-id="7698d-122">Это означает, что их удаление не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="7698d-122">This means that they are not guaranteed to be deleted.</span></span>

 

<span data-ttu-id="7698d-123">Приложение VSS может удалять файлы из теневой копии во время создания теневой копии с помощью следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="7698d-123">A VSS application can delete files from a shadow copy during shadow copy creation by using the following registry key:</span></span>

<span data-ttu-id="7698d-124">**HKEY \_ локальный \_ компьютер \\ система \\ CurrentControlSet \\ элемент управления \\ баккупресторе \\ филесноттоснапшот**</span><span class="sxs-lookup"><span data-stu-id="7698d-124">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\BackupRestore\\FilesNotToSnapshot**</span></span>

<span data-ttu-id="7698d-125">Этот раздел реестра содержит \_ несколько \_ SZ значений для каждого приложения, файлы которого можно исключить.</span><span class="sxs-lookup"><span data-stu-id="7698d-125">This registry key has REG\_MULTI\_SZ values for each application whose files can be excluded.</span></span> <span data-ttu-id="7698d-126">Файлы указываются с помощью полных путей, которые могут содержать \* подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="7698d-126">The files are specified by fully qualified paths, which can contain the \* wildcard.</span></span>

<span data-ttu-id="7698d-127">Во всех случаях запись не учитывается, если нет файлов, соответствующих строке пути.</span><span class="sxs-lookup"><span data-stu-id="7698d-127">In all cases, the entry is ignored if there are no files that match the path string.</span></span>

<span data-ttu-id="7698d-128">После добавления файла к соответствующему разделу реестра он удаляется из теневой копии во время создания с помощью модуля записи оптимизации теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="7698d-128">After a file is added to the appropriate registry key value, it is deleted from the shadow copy during creation by the shadow copy optimization writer on a best-effort basis.</span></span>

<span data-ttu-id="7698d-129">Если невозможно указать полный путь, то путь может быть также неявно указан с помощью $UserProfile $ или $AllVolumes $ Variable.</span><span class="sxs-lookup"><span data-stu-id="7698d-129">If a fully qualified path cannot be specified, then a path can also be implied by using the $UserProfile$ or $AllVolumes$ variable.</span></span> <span data-ttu-id="7698d-130">Пример:</span><span class="sxs-lookup"><span data-stu-id="7698d-130">For example:</span></span>

-   <span data-ttu-id="7698d-131">$UserProfile $ \\ каталог \\ имя файла подкаталога \\ .\*</span><span class="sxs-lookup"><span data-stu-id="7698d-131">$UserProfile$\\Directory\\Subdirectory\\FileName.\*</span></span>
-   <span data-ttu-id="7698d-132">$AllVolumes $ \\ темпорарифилес \\ \* .\*</span><span class="sxs-lookup"><span data-stu-id="7698d-132">$AllVolumes$\\TemporaryFiles\\\*.\*</span></span>

<span data-ttu-id="7698d-133">Чтобы сделать путь рекурсивным, добавьте "/s" в конец.</span><span class="sxs-lookup"><span data-stu-id="7698d-133">To make the path recursive, append " /s" to the end.</span></span> <span data-ttu-id="7698d-134">Пример:</span><span class="sxs-lookup"><span data-stu-id="7698d-134">For example:</span></span>

-   <span data-ttu-id="7698d-135">$UserProfile $ \\ каталог \\ подкаталог \\ имя_файла. \* /s</span><span class="sxs-lookup"><span data-stu-id="7698d-135">$UserProfile$\\Directory\\Subdirectory\\FileName.\* /s</span></span>
-   <span data-ttu-id="7698d-136">$AllVolumes $ \\ темпорарифилес \\ \* . \* /s</span><span class="sxs-lookup"><span data-stu-id="7698d-136">$AllVolumes$\\TemporaryFiles\\\*.\* /s</span></span>

<span data-ttu-id="7698d-137">Переменная $UserProfile $ вызывает применение строки пути ко всем профилям пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="7698d-137">The $UserProfile$ variable causes the path string to be applied to all user profiles on the computer.</span></span> <span data-ttu-id="7698d-138">Профили пользователей перечисляются путем проверки следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="7698d-138">The user profiles are enumerated by examining the following registry key:</span></span>

<span data-ttu-id="7698d-139">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows NT \\ CurrentVersion \\ профилелист**</span><span class="sxs-lookup"><span data-stu-id="7698d-139">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\ProfileList**</span></span>

<span data-ttu-id="7698d-140">Переменная $AllVolumes $ вызывает применение строки пути ко всем теневым копиям на компьютере.</span><span class="sxs-lookup"><span data-stu-id="7698d-140">The $AllVolumes$ variable causes the path string to be applied to all shadow copies on the computer.</span></span> <span data-ttu-id="7698d-141">Например, предположим, что путь имеет значение «$AllVolumes $ \\ темпорарифилес \\ \* . \* /s ", и компьютер имеет три тома: C:, D: и Е:.</span><span class="sxs-lookup"><span data-stu-id="7698d-141">For example, suppose the path is "$AllVolumes$\\TemporaryFiles\\\*.\* /s", and the computer has three volumes: C:, D:, and E:.</span></span> <span data-ttu-id="7698d-142">Если C: и E: содержат путь " \\ темпорарифилес \\ ", а том d: содержит только путь d: \\ Data \\ , дерево каталогов C: \\ темпорарифилес \\ удаляется из теневых копий C:, а дерево каталогов E: \\ темпорарифилес \\ удаляется из теневых копий е:.</span><span class="sxs-lookup"><span data-stu-id="7698d-142">If C: and E: contain the path "\\TemporaryFiles\\", and volume D: contains only the path D:\\Data\\, the directory tree C:\\TemporaryFiles\\ is deleted from shadow copies of C:, and the directory tree E:\\TemporaryFiles\\ is deleted from shadow copies of E:.</span></span>

<span data-ttu-id="7698d-143">Администраторы могут отключить расширение переменной $UserProfile $, используя следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="7698d-143">Administrators can disable expansion of the $UserProfile$ variable by using the following registry key:</span></span>

<span data-ttu-id="7698d-144">**\_ \_ \\ \\ \\ \\ Параметры VSS CURRENTCONTROLSET Services System \\ для локального компьютера hKey**</span><span class="sxs-lookup"><span data-stu-id="7698d-144">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Vss\\Settings**</span></span>

<span data-ttu-id="7698d-145">В разделе этого раздела реестра укажите Дисаблеусерпрофиликспансион в качестве имени значения, REG \_ DWORD для типа значения и ненулевое значение для данных значения.</span><span class="sxs-lookup"><span data-stu-id="7698d-145">Under this registry key, specify DisableUserProfileExpansion for the value name, REG\_DWORD for the value type, and a nonzero value for the value data.</span></span>

## <a name="about-the-filesnottobackup-registry-key"></a><span data-ttu-id="7698d-146">Сведения о разделе реестра Филесноттобаккуп</span><span class="sxs-lookup"><span data-stu-id="7698d-146">About the FilesNotToBackup Registry Key</span></span>

<span data-ttu-id="7698d-147">Раздел реестра **филесноттобаккуп** можно использовать для указания имен файлов и каталогов, которые приложения резервного копирования не должны выполнять резервное копирование или восстановление.</span><span class="sxs-lookup"><span data-stu-id="7698d-147">The **FilesNotToBackup** registry key can be used to specify the names of the files and directories that backup applications should not backup or restore.</span></span> <span data-ttu-id="7698d-148">Однако они не исключают эти файлы из теневых копий.</span><span class="sxs-lookup"><span data-stu-id="7698d-148">However, it does not exclude those files from shadow copies.</span></span> <span data-ttu-id="7698d-149">Дополнительные сведения об этом разделе реестра см. в разделе [разделы реестра и значения для резервного копирования и восстановления](../backup/registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="7698d-149">For more information about this registry key, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

 

 
