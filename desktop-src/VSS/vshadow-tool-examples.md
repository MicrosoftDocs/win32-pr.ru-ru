---
description: 'Дополнительные сведения: примеры инструментов Вшадов'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Примеры инструментов Вшадов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65fd2bfa1c390b1bd5310cd80f02e029dbf935f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809827"
---
# <a name="vshadow-tool-examples"></a><span data-ttu-id="bfb47-103">Примеры инструментов Вшадов</span><span class="sxs-lookup"><span data-stu-id="bfb47-103">VShadow Tool Examples</span></span>

<span data-ttu-id="bfb47-104">В следующих примерах показано, как использовать средство Вшадов для выполнения наиболее распространенных задач.</span><span class="sxs-lookup"><span data-stu-id="bfb47-104">The following examples show how to use the VShadow tool to perform the most common tasks:</span></span>

-   [<span data-ttu-id="bfb47-105">Доступ к свойствам теневого копирования из скрипта CMD</span><span class="sxs-lookup"><span data-stu-id="bfb47-105">Accessing Shadow Copy Properties from a CMD Script</span></span>](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [<span data-ttu-id="bfb47-106">Доступ к непостоянным теневым копиям</span><span class="sxs-lookup"><span data-stu-id="bfb47-106">Accessing Nonpersistent Shadow Copies</span></span>](#accessing-nonpersistent-shadow-copies)
-   [<span data-ttu-id="bfb47-107">Копирование файла из теневой копии</span><span class="sxs-lookup"><span data-stu-id="bfb47-107">Copying a File from a Shadow Copy</span></span>](#copying-a-file-from-a-shadow-copy)
-   [<span data-ttu-id="bfb47-108">Перечисление всех файлов на устройстве теневого копирования</span><span class="sxs-lookup"><span data-stu-id="bfb47-108">Enumerating All Files on a Shadow Copy Device</span></span>](#enumerating-all-files-on-a-shadow-copy-device)
-   [<span data-ttu-id="bfb47-109">Импорт переносимой теневой копии</span><span class="sxs-lookup"><span data-stu-id="bfb47-109">Importing a Transportable Shadow Copy</span></span>](#importing-a-transportable-shadow-copy)
-   [<span data-ttu-id="bfb47-110">Включение модулей записи или компонентов</span><span class="sxs-lookup"><span data-stu-id="bfb47-110">Including Writers or Components</span></span>](#including-writers-or-components)
-   [<span data-ttu-id="bfb47-111">Исключение модулей записи или компонентов</span><span class="sxs-lookup"><span data-stu-id="bfb47-111">Excluding Writers or Components</span></span>](#excluding-writers-or-components)
-   [<span data-ttu-id="bfb47-112">Разбиение наборов теневых копий с помощью метода Бреакснапшотсетекс</span><span class="sxs-lookup"><span data-stu-id="bfb47-112">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

<span data-ttu-id="bfb47-113">Полный список параметров командной строки и их использовании см. в разделе [Вшадов Tool и Sample](vshadow-tool-and-sample.md).</span><span class="sxs-lookup"><span data-stu-id="bfb47-113">For a complete list of command-line options and their use, see [VShadow Tool and Sample](vshadow-tool-and-sample.md).</span></span>

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a><span data-ttu-id="bfb47-114">Доступ к свойствам теневого копирования из скрипта CMD</span><span class="sxs-lookup"><span data-stu-id="bfb47-114">Accessing Shadow Copy Properties from a CMD Script</span></span>

<span data-ttu-id="bfb47-115">При использовании необязательного флага **-script** при создании теневых копий вшадов создает файл сценария cmd, содержащий переменные среды, связанные с созданными теневыми копиями, например следующие:</span><span class="sxs-lookup"><span data-stu-id="bfb47-115">If you use the **-script** optional flag when you create shadow copies, VShadow creates a CMD script file containing environment variables related to the newly created shadow copies, such as the following:</span></span>

-   <span data-ttu-id="bfb47-116">Идентификатор набора теневых копий, который хранится в переменной среды% ВШАДОВ \_ Set \_ ID%</span><span class="sxs-lookup"><span data-stu-id="bfb47-116">The shadow copy set ID, which is stored in the %VSHADOW\_SET\_ID% environment variable</span></span>
-   <span data-ttu-id="bfb47-117">Идентификаторы теневых копий, которые хранятся в переменных вида% ВШАДОВ \_ ID \_ *nnn*%, где *nnn* представляет индекс исходного тома в командной строке вшадов</span><span class="sxs-lookup"><span data-stu-id="bfb47-117">The shadow copy IDs, which are stored in variables of the form %VSHADOW\_ID\_*NNN*%, where *NNN* represents the index of the source volume in the VShadow command line</span></span>
-   <span data-ttu-id="bfb47-118">Имена устройств теневого копирования, которые хранятся в переменных вида% ВШАДОВ \_ устройство \_ *nnn*%, где *nnn* — индекс исходного тома в командной строке вшадов</span><span class="sxs-lookup"><span data-stu-id="bfb47-118">The shadow copy device names, which are stored in variables of the form %VSHADOW\_DEVICE\_*NNN*%, where *NNN* is the index of the source volume in the VShadow command line</span></span>

<span data-ttu-id="bfb47-119">Созданный КОМАНДный файл можно использовать для выполнения ограниченных операций управления теневыми копиями.</span><span class="sxs-lookup"><span data-stu-id="bfb47-119">You can use the generated CMD file to perform limited management operations on the shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="bfb47-120">Событие [**баккупкомплете**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) Writer отправляется после выполнения скрипта **-exec** .</span><span class="sxs-lookup"><span data-stu-id="bfb47-120">The [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) writer event is sent after the **-exec** script is executed.</span></span> <span data-ttu-id="bfb47-121">VSS вызывает метод **ивссбаккупкомпонентс:: баккупкомплете** , чтобы сообщить средствам записи о завершении резервного копирования, а также модули записи, которые могут усечь журналы на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="bfb47-121">VSS calls the **IVssBackupComponents::BackupComplete** method to signal to the writers that the backup is completed, and the writers can potentially truncate logs at this point.</span></span> <span data-ttu-id="bfb47-122">Поэтому важно убедиться, что на самом деле завершена теневая или резервная копия.</span><span class="sxs-lookup"><span data-stu-id="bfb47-122">Therefore, it is important to verify that the shadow/backup actually completed.</span></span> <span data-ttu-id="bfb47-123">Если резервное копирование завершилось сбоем, можно отменить процесс создания, возвращая ненулевой код выхода в выполненном сценарии или команде.</span><span class="sxs-lookup"><span data-stu-id="bfb47-123">If the backup failed, you can cancel the creation process by returning a nonzero exit code in the executed script/command.</span></span> <span data-ttu-id="bfb47-124">(См. документацию по команде Exit в [справочнике по командной строке Windows](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) Если пользовательская команда возвращается с ненулевым кодом выхода, создание теневой копии отменяется и **ивссбаккупкомпонентс:: баккупкомплете** не будет вызываться.</span><span class="sxs-lookup"><span data-stu-id="bfb47-124">(See the documentation for the exit command in the [Windows Command Line Reference](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) If the custom command returns with a nonzero exit code, then the shadow copy creation is canceled and **IVssBackupComponents::BackupComplete** will not be called.</span></span>

 

<span data-ttu-id="bfb47-125">В следующем примере показано, как создать постоянную теневую копию из командной строки и использовать для ее предоставления командный скрипт.</span><span class="sxs-lookup"><span data-stu-id="bfb47-125">The following example shows how to create a persistent shadow copy from the command line and use the CMD script to expose it.</span></span>

1.  <span data-ttu-id="bfb47-126">**вшадов-p-NW-Script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="bfb47-126">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
2.  <span data-ttu-id="bfb47-127">**вызов SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="bfb47-127">**call SETVAR1.cmd**</span></span>
3.  <span data-ttu-id="bfb47-128">**C: \\>вшадов-El =% вшадов \_ ID \_ 1%, c: \\ Directory1**</span><span class="sxs-lookup"><span data-stu-id="bfb47-128">**C:\\>vshadow -el=%VSHADOW\_ID\_1%,c:\\directory1**</span></span>

## <a name="accessing-nonpersistent-shadow-copies"></a><span data-ttu-id="bfb47-129">Доступ к непостоянным теневым копиям</span><span class="sxs-lookup"><span data-stu-id="bfb47-129">Accessing Nonpersistent Shadow Copies</span></span>

<span data-ttu-id="bfb47-130">Непостоянные теневые копии автоматически удаляются при выходе из программы, которая их создает (в данном случае Вшадов).</span><span class="sxs-lookup"><span data-stu-id="bfb47-130">Nonpersistent shadow copies are automatically deleted when the program that creates them (in this case, VShadow) exits.</span></span> <span data-ttu-id="bfb47-131">Для доступа к содержимому этих теневых копий Вшадов позволяет выполнить сценарий после создания теневых копий, но до выхода из программы Вшадов.</span><span class="sxs-lookup"><span data-stu-id="bfb47-131">To access the contents of these shadow copies, VShadow allows you to execute a script after the shadow copies are created but before the VShadow program exits.</span></span>

<span data-ttu-id="bfb47-132">В следующем примере показано, как использовать параметр командной строки-exec для выполнения скрипта с именем "Enum. cmd":</span><span class="sxs-lookup"><span data-stu-id="bfb47-132">The following example shows how to use the -exec command-line option to run a script called "enum.cmd":</span></span>

<span data-ttu-id="bfb47-133">**вшадов-NW-Exec = Enum. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="bfb47-133">**vshadow -nw -exec=enum.cmd c:**</span></span>

<span data-ttu-id="bfb47-134">В выполненном сценарии можно также запустить созданный скрипт SETVAR в этой пользовательской команде.</span><span class="sxs-lookup"><span data-stu-id="bfb47-134">In the executed script, you can also run the generated SETVAR script in this custom command.</span></span> <span data-ttu-id="bfb47-135">Это позволяет сценарию получить доступ к содержимому теневых копий напрямую.</span><span class="sxs-lookup"><span data-stu-id="bfb47-135">This allows the script to access the contents of the shadow copies directly.</span></span> <span data-ttu-id="bfb47-136">Помните, что теневое устройство можно получить из \_ \_ переменной среды вшадов устройства nnn.</span><span class="sxs-lookup"><span data-stu-id="bfb47-136">Remember that the shadow device can be retrieved from the VSHADOW\_DEVICE\_NNN environment variable.</span></span>

<span data-ttu-id="bfb47-137">Ниже приведен пример сценария Enum. cmd:</span><span class="sxs-lookup"><span data-stu-id="bfb47-137">Here is an example enum.cmd script:</span></span>

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

<span data-ttu-id="bfb47-138">Ниже приведена Командная строка для выполнения скрипта Enum. cmd:</span><span class="sxs-lookup"><span data-stu-id="bfb47-138">Here is the command line to execute the enum.cmd script:</span></span>

<span data-ttu-id="bfb47-139">**вшадов-NW-Exec = c: \\ Enum. cmd-Script = setvar1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="bfb47-139">**vshadow -nw -exec=c:\\enum.cmd -script=setvar1.cmd c:**</span></span>

## <a name="copying-a-file-from-a-shadow-copy"></a><span data-ttu-id="bfb47-140">Копирование файла из теневой копии</span><span class="sxs-lookup"><span data-stu-id="bfb47-140">Copying a File from a Shadow Copy</span></span>

<span data-ttu-id="bfb47-141">В следующем примере показано, как скопировать файл из теневой копии.</span><span class="sxs-lookup"><span data-stu-id="bfb47-141">The following example shows how to copy a file from a shadow copy.</span></span>

1.  <span data-ttu-id="bfb47-142">**dir > c: \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="bfb47-142">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="bfb47-143">**вшадов-p-NW-Script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="bfb47-143">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="bfb47-144">**вызов SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="bfb47-144">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="bfb47-145">**копирование% ВШАДОВ \_ устройства \_ 1% \\somefile.txt c: \\ somefile \_bak.txt**</span><span class="sxs-lookup"><span data-stu-id="bfb47-145">**copy %VSHADOW\_DEVICE\_1%\\somefile.txt c:\\somefile\_bak.txt**</span></span>

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a><span data-ttu-id="bfb47-146">Перечисление всех файлов на устройстве теневого копирования</span><span class="sxs-lookup"><span data-stu-id="bfb47-146">Enumerating All Files on a Shadow Copy Device</span></span>

<span data-ttu-id="bfb47-147">В следующем примере показано, как перечислить все файлы на устройстве теневого копирования из пакетного файла.</span><span class="sxs-lookup"><span data-stu-id="bfb47-147">The following example shows how to enumerate all files on a shadow copy device from a batch file.</span></span>

1.  <span data-ttu-id="bfb47-148">**dir > c: \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="bfb47-148">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="bfb47-149">**вшадов-p-NW-Script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="bfb47-149">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="bfb47-150">**вызов SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="bfb47-150">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="bfb47-151">**для/R% ВШАДОВ \_ устройства \_ 1%%% \\ i в ( \* ) выполнить @echo %% i**</span><span class="sxs-lookup"><span data-stu-id="bfb47-151">**for /R %VSHADOW\_DEVICE\_1%\\ %%i in (\*) do @echo %%i**</span></span>

## <a name="importing-a-transportable-shadow-copy"></a><span data-ttu-id="bfb47-152">Импорт переносимой теневой копии</span><span class="sxs-lookup"><span data-stu-id="bfb47-152">Importing a Transportable Shadow Copy</span></span>

<span data-ttu-id="bfb47-153">Чтобы создать транспортную теневую копию на одном компьютере и импортировать ее на другой компьютер, необходимо иметь два компьютера, подключенные (через конфигурацию SAN), к массиву хранения данных, поддерживающему теневые копии оборудования VSS.</span><span class="sxs-lookup"><span data-stu-id="bfb47-153">To create a transportable shadow copy on one machine and import it to another machine, you must have two computers that are connected (through a SAN configuration) to a storage array that supports VSS hardware shadow copies.</span></span> <span data-ttu-id="bfb47-154">На каждом компьютере должен быть установлен поставщик оборудования VSS.</span><span class="sxs-lookup"><span data-stu-id="bfb47-154">A VSS hardware provider must be installed on each computer.</span></span>

<span data-ttu-id="bfb47-155">В следующем примере показано, как создать и импортировать теневую копию.</span><span class="sxs-lookup"><span data-stu-id="bfb47-155">The following example shows how to create and import the shadow copy.</span></span>

1.  <span data-ttu-id="bfb47-156">Создайте набор теневых копий на компьютере а (рабочем сервере), введя следующую команду после командной строки:</span><span class="sxs-lookup"><span data-stu-id="bfb47-156">Create the shadow copy set on computer A (the production server) by typing the following command after the command prompt:</span></span>

    <span data-ttu-id="bfb47-157">**вшадов-p-t =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="bfb47-157">**vshadow -p -t=bc1.xml**</span></span>

    <span data-ttu-id="bfb47-158">При этом не будут предоставляться устройства теневого копирования на компьютере A.</span><span class="sxs-lookup"><span data-stu-id="bfb47-158">This will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="bfb47-159">Скопируйте документ с компонентами резервного копирования (bc1.xml) с компьютера A на компьютер B.</span><span class="sxs-lookup"><span data-stu-id="bfb47-159">Copy the backup components document (bc1.xml) from computer A to computer B.</span></span>
3.  <span data-ttu-id="bfb47-160">Импортируйте теневой набор на компьютере B, введя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bfb47-160">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="bfb47-161">**вшадов-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="bfb47-161">**vshadow -i=bc1.xml**</span></span>

<span data-ttu-id="bfb47-162">При необходимости эти теневые копии можно предоставить как буквы диска или подключенные папки.</span><span class="sxs-lookup"><span data-stu-id="bfb47-162">Optionally, you could expose these shadow copies as drive letters or mounted folders.</span></span> <span data-ttu-id="bfb47-163">Кроме того, можно нарушить работу теневого набора, чтобы сделать новые тома теневой копии доступны для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="bfb47-163">Also, you could potentially break the shadow set to make the new shadow copy volumes read-write.</span></span>

<span data-ttu-id="bfb47-164">Чтобы автоматизировать процесс управления теневыми наборами, можно использовать параметр командной строки **-script** для создания СКРИПТа cmd, содержащего идентификаторы теневых копий.</span><span class="sxs-lookup"><span data-stu-id="bfb47-164">To automate the shadow set management process you might use the **-script** command-line option to generate the CMD script containing the shadow copy IDs.</span></span> <span data-ttu-id="bfb47-165">Затем можно скопировать созданный скрипт вместе с компонентами резервного копирования на другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="bfb47-165">Then you can copy the generated script along with the backup components to the other computer.</span></span>

<span data-ttu-id="bfb47-166">В следующем примере показано, как создавать, предоставлять и разрывать переносимые теневые копии с помощью сценариев CMD.</span><span class="sxs-lookup"><span data-stu-id="bfb47-166">The following example shows how to create, expose, and break transportable shadow copies using CMD scripts.</span></span>

1.  <span data-ttu-id="bfb47-167">Создайте набор теневых копий на компьютере а (рабочем сервере) из командной строки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bfb47-167">Create the shadow copy set on computer A (the production server) from the command line as follows:</span></span>

    <span data-ttu-id="bfb47-168">**вшадов-p-t =bc1.xml-Script = SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="bfb47-168">**vshadow -p -t=bc1.xml -script=sc1.cmd**</span></span>

    <span data-ttu-id="bfb47-169">Укажите параметр **-script** , чтобы создать скрипт, содержащий правильные определения переменных среды.</span><span class="sxs-lookup"><span data-stu-id="bfb47-169">Specify the **-script** option to generate the script containing the proper environment variable definitions.</span></span> <span data-ttu-id="bfb47-170">Обратите внимание, что при этом не будут предоставляться устройства теневого копирования на компьютере A.</span><span class="sxs-lookup"><span data-stu-id="bfb47-170">Note that this will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="bfb47-171">Скопируйте документ компонентов резервного копирования (bc1.xml) и созданный скрипт (SC1. cmd) с компьютера A на компьютер B.</span><span class="sxs-lookup"><span data-stu-id="bfb47-171">Copy the backup components document (bc1.xml) and the generated script (sc1.cmd) from computer A to computer B.</span></span>
3.  <span data-ttu-id="bfb47-172">Импортируйте теневой набор на компьютере B, введя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bfb47-172">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="bfb47-173">**вшадов-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="bfb47-173">**vshadow -i=bc1.xml**</span></span>

    <span data-ttu-id="bfb47-174">Созданные устройства будут отображаться на компьютере B.</span><span class="sxs-lookup"><span data-stu-id="bfb47-174">This will surface the created devices on computer B.</span></span>

4.  <span data-ttu-id="bfb47-175">Запустите созданный скрипт, чтобы задать переменные среды для набора теневых копий, введя имя файла в командной строке, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="bfb47-175">Run the generated script to set the environment variables for the shadow copy set by typing the file name at the command prompt as in the following example:</span></span>

    <span data-ttu-id="bfb47-176">**SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="bfb47-176">**sc1.cmd**</span></span>

    <span data-ttu-id="bfb47-177">Будут заданы соответствующие переменные среды, как описано в статье свойства теневого копирования Access из скрипта CMD.</span><span class="sxs-lookup"><span data-stu-id="bfb47-177">This will set the relevant environment variables as described in Access Shadow Copy Properties from a CMD Script.</span></span>

5.  <span data-ttu-id="bfb47-178">Предоставьте теневые копии на компьютере B, введя следующие команды:</span><span class="sxs-lookup"><span data-stu-id="bfb47-178">Expose the shadow copies on computer B by typing the following commands:</span></span>
    1.  <span data-ttu-id="bfb47-179">**rmdir/s c: \\ \_ точка подключения**</span><span class="sxs-lookup"><span data-stu-id="bfb47-179">**rmdir /s c:\\mount\_point**</span></span>
    2.  <span data-ttu-id="bfb47-180">**mkdir c: \\ \_ точка подключения**</span><span class="sxs-lookup"><span data-stu-id="bfb47-180">**mkdir c:\\mount\_point**</span></span>
    3.  <span data-ttu-id="bfb47-181">**вшадов — El =% ВШАДОВ \_ ID \_ 1%, c: \\ \_ точка подключения**</span><span class="sxs-lookup"><span data-stu-id="bfb47-181">**vshadow –el=%VSHADOW\_ID\_1%,c:\\mount\_point**</span></span>

    <span data-ttu-id="bfb47-182">На компьютере B будут созданы устройства теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="bfb47-182">This will surface the created shadow copy devices on computer B.</span></span>
6.  <span data-ttu-id="bfb47-183">Разбейте набор теневых копий, чтобы сделать тома доступными для записи, введя следующую команду:**C: \\>вшадов – BW =% вшадов \_ Set \_ ID%**</span><span class="sxs-lookup"><span data-stu-id="bfb47-183">Break the shadow copy set to make the volumes writable by typing the following command:**C:\\>vshadow –bw=%VSHADOW\_SET\_ID%**</span></span>

<span data-ttu-id="bfb47-184">Обратите внимание, что непостоянные транспортные теневые копии также можно импортировать, но они автоматически удаляются при завершении процесса **вшадов** **-i** .</span><span class="sxs-lookup"><span data-stu-id="bfb47-184">Note that nonpersistent transportable shadow copies can also be imported, but they are automatically deleted when the **vshadow** **-i** process exits.</span></span> <span data-ttu-id="bfb47-185">Чтобы импортировать теневые копии перед удалением, необходимо использовать параметр командной строки **-exec** , как описано в статье доступ к непостоянным теневым копиям.</span><span class="sxs-lookup"><span data-stu-id="bfb47-185">To import the shadow copies before they are deleted, you must use the **-exec** command-line option as described in Access Nonpersistent Shadow Copies.</span></span>

## <a name="including-writers-or-components"></a><span data-ttu-id="bfb47-186">Включение модулей записи или компонентов</span><span class="sxs-lookup"><span data-stu-id="bfb47-186">Including Writers or Components</span></span>

<span data-ttu-id="bfb47-187">По умолчанию все модули записи участвуют в создании теневой копии.</span><span class="sxs-lookup"><span data-stu-id="bfb47-187">By default, all writers participate in shadow copy creation.</span></span> <span data-ttu-id="bfb47-188">Чтобы определить, какие модули записи и компоненты будут включаться в набор теневых копий, используйте параметр командной строки **-WM** или **-wm2** , как описано в разделе [Вывод сведений о состоянии и метаданных модуля записи](vshadow-tool-and-sample.md).</span><span class="sxs-lookup"><span data-stu-id="bfb47-188">To determine which writers and components will be included in a shadow copy set, use the **-wm** or **-wm2** command-line option as described in [Listing Writer Status and Metadata](vshadow-tool-and-sample.md).</span></span>

<span data-ttu-id="bfb47-189">Чтобы убедиться, что все компоненты модуля записи включены, используйте необязательный флаг **-Wi** в любом из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="bfb47-189">To verify that all of a writer's components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="bfb47-190">**вшадов** **— Wi-** *вритернаме*</span><span class="sxs-lookup"><span data-stu-id="bfb47-190">**vshadow** **-wi** *WriterName*</span></span>
-   <span data-ttu-id="bfb47-191">**вшадов** **-Wi** **"**_строка имени модуля записи_*_"_*</span><span class="sxs-lookup"><span data-stu-id="bfb47-191">**vshadow** **-wi** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="bfb47-192">**вшадов** **-Wi** **{**_вритерид_*_}_*</span><span class="sxs-lookup"><span data-stu-id="bfb47-192">**vshadow** **-wi** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="bfb47-193">**вшадов** **-Wi** **{**_InstanceId_*_}_*</span><span class="sxs-lookup"><span data-stu-id="bfb47-193">**vshadow** **-wi** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="bfb47-194">Чтобы убедиться в том, что некоторые компоненты включены, используйте необязательный флаг **-Wi** в любом из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="bfb47-194">To verify that specific components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="bfb47-195">**вшадов** **-Wi** \*вритернаме \***: \\**_логикалпас_\* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="bfb47-195">**vshadow** **-wi** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="bfb47-196">**вшадов** **-Wi** **"**_строка имени модуля записи_*_" \\ :_*_логикалпас_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="bfb47-196">**vshadow** **-wi** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="bfb47-197">**вшадов** **-Wi** **{**_вритерид_*_}: \\_*_логикалпас_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="bfb47-197">**vshadow** **-wi** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="bfb47-198">**вшадов** **-Wi** **{**_InstanceId_*_}: \\_*_логикалпас_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="bfb47-198">**vshadow** **-wi** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="bfb47-199">В следующих примерах показано, как использовать необязательный флаг **-Wi** .</span><span class="sxs-lookup"><span data-stu-id="bfb47-199">The following examples show how to use the **-wi** optional flag.</span></span>

-   <span data-ttu-id="bfb47-200">Указание *вритернаме*: \\ *логикалпас* \\ *ComponentName*:</span><span class="sxs-lookup"><span data-stu-id="bfb47-200">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="bfb47-201">**вшадов-Wi = "модуль записи в реестр: \\ Реестр"**</span><span class="sxs-lookup"><span data-stu-id="bfb47-201">**vshadow -wi="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="bfb47-202">Указание {*вритерид*}:</span><span class="sxs-lookup"><span data-stu-id="bfb47-202">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="bfb47-203">**вшадов-Wi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="bfb47-203">**vshadow -wi={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="bfb47-204">Указание более одного модуля записи или компонента:</span><span class="sxs-lookup"><span data-stu-id="bfb47-204">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="bfb47-205">**вшадов-Wi = "модуль записи в реестр: \\ Реестр"-Wi = "com+ Регдб Writer"**</span><span class="sxs-lookup"><span data-stu-id="bfb47-205">**vshadow -wi="Registry Writer:\\Registry" -wi="COM+ REGDB Writer"**</span></span>

## <a name="excluding-writers-or-components"></a><span data-ttu-id="bfb47-206">Исключение модулей записи или компонентов</span><span class="sxs-lookup"><span data-stu-id="bfb47-206">Excluding Writers or Components</span></span>

<span data-ttu-id="bfb47-207">Чтобы исключить все модули записи, используйте флаг **-NW** Optional при создании теневой копии.</span><span class="sxs-lookup"><span data-stu-id="bfb47-207">To exclude all writers, use the **-nw** optional flag when creating the shadow copy.</span></span>

<span data-ttu-id="bfb47-208">Чтобы исключить все компоненты модуля записи, используйте необязательный флаг **-WX** в любом из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="bfb47-208">To exclude all of a writer's components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="bfb47-209">**вшадов** **-WX** *вритернаме*</span><span class="sxs-lookup"><span data-stu-id="bfb47-209">**vshadow** **-wx** *WriterName*</span></span>
-   <span data-ttu-id="bfb47-210">**вшадов** **-WX** **"**_строка имени модуля записи_*_"_*</span><span class="sxs-lookup"><span data-stu-id="bfb47-210">**vshadow** **-wx** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="bfb47-211">**вшадов** **-WX** **{**_вритерид_*_}_*</span><span class="sxs-lookup"><span data-stu-id="bfb47-211">**vshadow** **-wx** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="bfb47-212">**вшадов** **-WX** **{**_InstanceId_*_}_*</span><span class="sxs-lookup"><span data-stu-id="bfb47-212">**vshadow** **-wx** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="bfb47-213">Чтобы исключить определенные компоненты, используйте необязательный флаг **-WX** в любом из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="bfb47-213">To exclude specific components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="bfb47-214">**вшадов** **-WX** \*вритернаме \***: \\**_логикалпас_\* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="bfb47-214">**vshadow** **-wx** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="bfb47-215">**вшадов** **-WX** **"**_строка имени модуля записи_*_" \\ :_*_логикалпас_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="bfb47-215">**vshadow** **-wx** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="bfb47-216">**вшадов** **-WX** **{**_вритерид_*_}: \\_*_логикалпас_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="bfb47-216">**vshadow** **-wx** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="bfb47-217">**вшадов** **-WX** **{**_InstanceId_*_}: \\_*_логикалпас_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="bfb47-217">**vshadow** **-wx** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="bfb47-218">В следующих примерах показано, как использовать необязательный флаг **-WX** .</span><span class="sxs-lookup"><span data-stu-id="bfb47-218">The following examples show how to use the **-wx** optional flag.</span></span>

-   <span data-ttu-id="bfb47-219">Указание *вритернаме*: \\ *логикалпас* \\ *ComponentName*:</span><span class="sxs-lookup"><span data-stu-id="bfb47-219">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="bfb47-220">**вшадов-WX = "модуль записи реестра: \\ Реестр"**</span><span class="sxs-lookup"><span data-stu-id="bfb47-220">**vshadow -wx="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="bfb47-221">Указание {*вритерид*}:</span><span class="sxs-lookup"><span data-stu-id="bfb47-221">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="bfb47-222">**вшадов-WX = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="bfb47-222">**vshadow -wx={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="bfb47-223">Указание более одного модуля записи или компонента:</span><span class="sxs-lookup"><span data-stu-id="bfb47-223">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="bfb47-224">**вшадов-WX = "модуль записи реестра: \\ Реестр"-WX = "com+ Регдб Writer"**</span><span class="sxs-lookup"><span data-stu-id="bfb47-224">**vshadow -wx="Registry Writer:\\Registry" -wx="COM+ REGDB Writer"**</span></span>

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="bfb47-225">Разбиение наборов теневых копий с помощью метода Бреакснапшотсетекс</span><span class="sxs-lookup"><span data-stu-id="bfb47-225">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="bfb47-226">В следующих примерах показано, как использовать параметр командной строки **-BEX** .</span><span class="sxs-lookup"><span data-stu-id="bfb47-226">The following examples show how to use the **-bex** command-line option.</span></span>

-   <span data-ttu-id="bfb47-227">Указание того, что LUN теневой копии будет маскироваться от узла:</span><span class="sxs-lookup"><span data-stu-id="bfb47-227">Specifying that the shadow copy LUN will be masked from the host:</span></span>

    <span data-ttu-id="bfb47-228">**вшадов** **-BEX** **-Mask**</span><span class="sxs-lookup"><span data-stu-id="bfb47-228">**vshadow** **-bex** **-mask**</span></span>

-   <span data-ttu-id="bfb47-229">Указание того, что LUN теневой копии будет предоставляться узлу в качестве тома для чтения и записи:</span><span class="sxs-lookup"><span data-stu-id="bfb47-229">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume:</span></span>

    <span data-ttu-id="bfb47-230">**вшадов** **-BEX** **-RW**</span><span class="sxs-lookup"><span data-stu-id="bfb47-230">**vshadow** **-bex** **-rw**</span></span>

-   <span data-ttu-id="bfb47-231">Указание того, что LUN теневой копии будет предоставляться узлу в качестве тома для чтения и записи и что ни одна из подписей дисков в LUN теневой копии не будет возвращена к исходным LUN:</span><span class="sxs-lookup"><span data-stu-id="bfb47-231">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume, and that none of the disk signatures on the shadow copy LUNs will be reverted to that of the original LUNs:</span></span>

    <span data-ttu-id="bfb47-232">**вшадов** **-BEX** **-revert**</span><span class="sxs-lookup"><span data-stu-id="bfb47-232">**vshadow** **-bex** **-norevert**</span></span>

 

 
