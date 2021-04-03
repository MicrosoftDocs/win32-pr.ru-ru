---
description: Тестирование является инициатором запроса VSS, который проверяет расширенные операции резервного копирования и восстановления.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Средство тестирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7559c304532b337214108435b740595897694f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913387"
---
# <a name="betest-tool"></a><span data-ttu-id="526a9-103">Средство тестирования</span><span class="sxs-lookup"><span data-stu-id="526a9-103">BETest Tool</span></span>

<span data-ttu-id="526a9-104">Тестирование является инициатором запроса VSS, который проверяет расширенные операции резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="526a9-104">BETest is a VSS requester that tests advanced backup and restore operations.</span></span> <span data-ttu-id="526a9-105">Это средство можно использовать для проверки использования приложением сложных функций VSS, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="526a9-105">This tool can be used to test an application's use of complex VSS features such as the following:</span></span>

-   <span data-ttu-id="526a9-106">Добавочная и разностная резервные копии</span><span class="sxs-lookup"><span data-stu-id="526a9-106">Incremental and differential backup</span></span>
-   <span data-ttu-id="526a9-107">Сложные параметры восстановления, такие как полномочное восстановление</span><span class="sxs-lookup"><span data-stu-id="526a9-107">Complex restore options, such as authoritative restore</span></span>
-   <span data-ttu-id="526a9-108">Параметры Накату</span><span class="sxs-lookup"><span data-stu-id="526a9-108">Rollforward options</span></span>

> [!Note]  
> <span data-ttu-id="526a9-109">Тестирование включено в пакет средств разработки программного обеспечения Microsoft Windows (SDK) для Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="526a9-109">BETest is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="526a9-110">Пакет SDK для VSS 7,2 включает версию теста "тестирование", которая выполняется только в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="526a9-110">The VSS 7.2 SDK includes a version of BETest that runs only on Windows Server 2003.</span></span> <span data-ttu-id="526a9-111">В этом разделе описывается Windows SDKная версия теста, а не версия Windows Server 2003, входящая в состав пакета SDK для VSS 7,2.</span><span class="sxs-lookup"><span data-stu-id="526a9-111">This topic describes the Windows SDK version of BETest, not the Windows Server 2003 version included in the VSS 7.2 SDK.</span></span> <span data-ttu-id="526a9-112">Сведения о скачивании Windows SDK и пакета SDK для VSS 7,2 см. в разделе [Служба теневого копирования томов](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="526a9-112">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="526a9-113">В Windows SDK установки средство тестирования можно найти в `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (для 64-разрядной версии Windows) и `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (для 32-разрядной версии Windows).</span><span class="sxs-lookup"><span data-stu-id="526a9-113">In the Windows SDK installation, the BETest tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="running-the-betest-tool"></a><span data-ttu-id="526a9-114">Запуск средства тестирования</span><span class="sxs-lookup"><span data-stu-id="526a9-114">Running the BETest Tool</span></span>

<span data-ttu-id="526a9-115">Чтобы запустить средство тестирования из командной строки, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="526a9-115">To run the BETest tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="526a9-116"> *Параметры командной строки* для тестирования</span><span class="sxs-lookup"><span data-stu-id="526a9-116">**BETest** *command-line-options*</span></span>

<span data-ttu-id="526a9-117">В следующем примере показано, как использовать средство "тестирование" вместе с [средством записи теста VSS](vss-test-writer-tool.md), которое является модулем записи VSS.</span><span class="sxs-lookup"><span data-stu-id="526a9-117">The following usage example shows how to use the BETest tool together with the [VSS Test Writer tool](vss-test-writer-tool.md), which is a VSS writer.</span></span>

<span data-ttu-id="526a9-118">**Пример использования средства тестирования**</span><span class="sxs-lookup"><span data-stu-id="526a9-118">**BETest Tool Usage Example**</span></span>

1.  <span data-ttu-id="526a9-119">Создайте тестовый каталог с именем C: \\ Test.</span><span class="sxs-lookup"><span data-stu-id="526a9-119">Create a test directory named C:\\BETest.</span></span> <span data-ttu-id="526a9-120">Скопируйте следующие файлы в этот каталог:</span><span class="sxs-lookup"><span data-stu-id="526a9-120">Copy the following files into this directory:</span></span>
    -   <span data-ttu-id="526a9-121">betest.exe</span><span class="sxs-lookup"><span data-stu-id="526a9-121">betest.exe</span></span>
    -   <span data-ttu-id="526a9-122">vswriter.exe</span><span class="sxs-lookup"><span data-stu-id="526a9-122">vswriter.exe</span></span>
    -   [<span data-ttu-id="526a9-123">BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="526a9-123">BetestSample.xml</span></span>](#sample-xml-configuration-file-betestsamplexml)
    -   [<span data-ttu-id="526a9-124">VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="526a9-124">VswriterSample.xml</span></span>](#sample-xml-configuration-file-vswritersamplexml)
2.  <span data-ttu-id="526a9-125">Создайте каталог с именем C: \\ тестпас.</span><span class="sxs-lookup"><span data-stu-id="526a9-125">Create a directory named C:\\TestPath.</span></span> <span data-ttu-id="526a9-126">Помещайте в этот каталог некоторые файлы тестовых данных.</span><span class="sxs-lookup"><span data-stu-id="526a9-126">Put some test data files in this directory.</span></span>
3.  <span data-ttu-id="526a9-127">Создайте каталог с именем C: \\ баккупдестинатион.</span><span class="sxs-lookup"><span data-stu-id="526a9-127">Create a directory named C:\\BackupDestination.</span></span> <span data-ttu-id="526a9-128">Оставьте этот каталог пустым.</span><span class="sxs-lookup"><span data-stu-id="526a9-128">Leave this directory empty.</span></span>
4.  <span data-ttu-id="526a9-129">Откройте два окна команд с повышенными привилегиями и настройте рабочий каталог в каждом из на C: \\ Test.</span><span class="sxs-lookup"><span data-stu-id="526a9-129">Open two elevated command windows and set the working directory in each to C:\\BETest.</span></span>
5.  <span data-ttu-id="526a9-130">В первом окне командной строки запустите [средство записи теста VSS](vss-test-writer-tool.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="526a9-130">In the first command window, start the [VSS Test Writer tool](vss-test-writer-tool.md) as follows:</span></span>

    <span data-ttu-id="526a9-131">**vswriter.exe VswriterSample.xml**</span><span class="sxs-lookup"><span data-stu-id="526a9-131">**vswriter.exe VswriterSample.xml**</span></span>

    <span data-ttu-id="526a9-132">Файл vswriterSample.xml настраивает средство записи тестов VSS (всвритер) для сообщения о содержимом каталога c: \\ тестпас в процессе подготовки к операции резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="526a9-132">The vswriterSample.xml file configures the VSS Test Writer tool (vswriter) to report the contents of the c:\\TestPath directory in preparation for a backup operation.</span></span> <span data-ttu-id="526a9-133">Обратите внимание, что средство записи тестов VSS не будет создавать выходные данные до тех пор, пока не обнаружит действия от запрашивающей стороны, например, для выполнения проверки.</span><span class="sxs-lookup"><span data-stu-id="526a9-133">Note that the VSS Test Writer tool will not produce output until it detects activity from a requester such as BETest.</span></span> <span data-ttu-id="526a9-134">Чтобы закрыть средство записи тестов VSS, нажмите клавиши CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="526a9-134">To stop the VSS Test Writer tool, press CTRL+C.</span></span>

6.  <span data-ttu-id="526a9-135">Во втором окне команды используйте средство тестирования для выполнения операции резервного копирования следующим образом.</span><span class="sxs-lookup"><span data-stu-id="526a9-135">In the second command window, use the BETest tool to perform a backup operation as follows:</span></span>

    <span data-ttu-id="526a9-136">**betest.exe/B/S backup.xml/D C: \\ баккупдестинатион/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="526a9-136">**betest.exe /B /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

    <span data-ttu-id="526a9-137">В ходе тестирования выполняется резервное копирование файлов из каталога C: \\ тестпас в каталог c: \\ баккупдестинатион.</span><span class="sxs-lookup"><span data-stu-id="526a9-137">BETest will back up the files from the C:\\TestPath directory to the C:\\BackupDestination directory.</span></span> <span data-ttu-id="526a9-138">Документ компонента резервного копирования будет сохранен на языке C: \\ test \\backup.xml.</span><span class="sxs-lookup"><span data-stu-id="526a9-138">It will save the backup component document to C:\\BETest\\backup.xml.</span></span>

7.  <span data-ttu-id="526a9-139">Если операция резервного копирования прошла успешно, удалите содержимое каталога C: \\ тестпас и используйте средство тестирования для выполнения операции восстановления следующим образом.</span><span class="sxs-lookup"><span data-stu-id="526a9-139">If the backup operation is successful, delete the contents of the C:\\TestPath directory, and use the BETest tool to perform a restore operation as follows:</span></span>

    <span data-ttu-id="526a9-140">**betest.exe/R/S backup.xml/D C: \\ баккупдестинатион/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="526a9-140">**betest.exe /R /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

## <a name="betest-tool-command-line-options"></a><span data-ttu-id="526a9-141">Параметры Command-Line средства тестирования</span><span class="sxs-lookup"><span data-stu-id="526a9-141">BETest Tool Command-Line Options</span></span>

<span data-ttu-id="526a9-142">Средство тестирования использует следующие параметры командной строки для задания выполняемой работы.</span><span class="sxs-lookup"><span data-stu-id="526a9-142">The BETest tool uses the following command-line options to identify the work to perform.</span></span>

<dl> <dt>

<span data-ttu-id="526a9-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/аус**</span><span class="sxs-lookup"><span data-stu-id="526a9-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span></span>
</dt> <dd>

<span data-ttu-id="526a9-144">Выполняет принудительную операцию восстановления для Active Directory или Active Directory режиме приложения.</span><span class="sxs-lookup"><span data-stu-id="526a9-144">Performs an authoritative restore operation for Active Directory or Active Directory Application Mode.</span></span>

<span data-ttu-id="526a9-145">**Windows Server 2003:** Этот параметр командной строки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="526a9-145">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-146"><span id="_B"></span><span id="_b"></span>**B**</span><span class="sxs-lookup"><span data-stu-id="526a9-146"><span id="_B"></span><span id="_b"></span>**/B**</span></span>
</dt> <dd>

<span data-ttu-id="526a9-147">Выполняет операцию резервного копирования, но не выполняет восстановление.</span><span class="sxs-lookup"><span data-stu-id="526a9-147">Performs a backup operation but does not perform a restore.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-148"><span id="_BC"></span><span id="_bc"></span>**/бк**</span><span class="sxs-lookup"><span data-stu-id="526a9-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span></span>
</dt> <dd>

<span data-ttu-id="526a9-149">Выполняет только операцию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="526a9-149">Performs only the backup complete operation.</span></span>

<span data-ttu-id="526a9-150">**Windows Server 2003:** Этот параметр командной строки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="526a9-150">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *имя файла*</span><span class="sxs-lookup"><span data-stu-id="526a9-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *Filename*</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="526a9-152">Этот параметр командной строки предоставляется только для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="526a9-152">This command-line option is provided only for backward compatibility.</span></span> <span data-ttu-id="526a9-153">Вместо него следует использовать параметр командной строки **/x** .</span><span class="sxs-lookup"><span data-stu-id="526a9-153">The **/X** command-line option should be used instead.</span></span>

 

<span data-ttu-id="526a9-154">Выбирает компоненты для резервного копирования или восстановления в зависимости от содержимого файла конфигурации, заданного параметром *filename*.</span><span class="sxs-lookup"><span data-stu-id="526a9-154">Selects the components to be backed up or restored based on the contents of the configuration file specified by *Filename*.</span></span> <span data-ttu-id="526a9-155">Этот файл должен содержать только символы ANSI в диапазоне от 0 до 127 и не должен превышать 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="526a9-155">This file must contain only ANSI characters in the range from 0 through 127, and it must be no larger than 1 MB.</span></span> <span data-ttu-id="526a9-156">Каждая строка в файле должна иметь следующий формат:</span><span class="sxs-lookup"><span data-stu-id="526a9-156">Each line in the file must use the following format:</span></span>

<span data-ttu-id="526a9-157">*Вритерид* : *ComponentName*;</span><span class="sxs-lookup"><span data-stu-id="526a9-157">*WriterId* : *ComponentName*;</span></span>

<span data-ttu-id="526a9-158">Где *вритерид* — это идентификатор модуля записи, а *ComponentName* — имя одного из компонентов модуля записи.</span><span class="sxs-lookup"><span data-stu-id="526a9-158">Where *WriterId* is the writer ID, and *ComponentName* is the name of one of the writer's components.</span></span> <span data-ttu-id="526a9-159">Имена идентификатора модуля записи и компонента должны быть заключены в кавычки и должны быть пробелами до и после двоеточия (:).</span><span class="sxs-lookup"><span data-stu-id="526a9-159">The writer ID and component names must be in quotation marks, and there must be spaces before and after the colon (:).</span></span> <span data-ttu-id="526a9-160">Если указано два или более компонентов, их необходимо разделять запятыми.</span><span class="sxs-lookup"><span data-stu-id="526a9-160">If two or more components are specified, they must be separated by commas.</span></span> <span data-ttu-id="526a9-161">Пример:</span><span class="sxs-lookup"><span data-stu-id="526a9-161">For example:</span></span>

<span data-ttu-id="526a9-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span><span class="sxs-lookup"><span data-stu-id="526a9-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span></span>

</dd> <dt>

<span data-ttu-id="526a9-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *путь*</span><span class="sxs-lookup"><span data-stu-id="526a9-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *Path*</span></span>
</dt> <dd>

<span data-ttu-id="526a9-164">Сохраните резервные копии файлов или восстановите их из каталога резервного копирования, указанного в параметре *path*.</span><span class="sxs-lookup"><span data-stu-id="526a9-164">Save the backed-up files to or restore them from the backup directory specified by *Path*.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-165"><span id="_NBC"></span><span id="_nbc"></span>**/нбк**</span><span class="sxs-lookup"><span data-stu-id="526a9-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span></span>
</dt> <dd>

<span data-ttu-id="526a9-166">Пропускает операцию резервного копирования завершено.</span><span class="sxs-lookup"><span data-stu-id="526a9-166">Omits the backup complete operation.</span></span>

<span data-ttu-id="526a9-167">**Windows Server 2003:** Этот параметр командной строки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="526a9-167">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-168"><span id="_O"></span><span id="_o"></span>**/O**</span><span class="sxs-lookup"><span data-stu-id="526a9-168"><span id="_O"></span><span id="_o"></span>**/O**</span></span>
</dt> <dd>

<span data-ttu-id="526a9-169">Указывает, что резервная копия включает загрузочное состояние системы.</span><span class="sxs-lookup"><span data-stu-id="526a9-169">Specifies that the backup includes a bootable system state.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-170"><span id="_P"></span><span id="_p"></span>**/P**</span><span class="sxs-lookup"><span data-stu-id="526a9-170"><span id="_P"></span><span id="_p"></span>**/P**</span></span>
</dt> <dd>

<span data-ttu-id="526a9-171">Создает постоянную теневую копию.</span><span class="sxs-lookup"><span data-stu-id="526a9-171">Creates a persistent shadow copy.</span></span>

<span data-ttu-id="526a9-172">**Windows Server 2003:** Этот параметр командной строки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="526a9-172">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span> *Имя файла* /пре</span><span class="sxs-lookup"><span data-stu-id="526a9-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="526a9-174">Если тип резервной копии, указанный в параметре командной строки **/t** , является добавочным или разностным, задайте для документа резервного копирования файл, указанный в поле *имя файла* для предыдущей полной или добавочной архивации.</span><span class="sxs-lookup"><span data-stu-id="526a9-174">If the backup type specified in the **/T** command-line option is INCREMENTAL or DIFFERENTIAL, set the backup document to the file specified by *Filename* for previous full or incremental backup.</span></span>

<span data-ttu-id="526a9-175">**Windows Server 2003 и Windows XP:** Этот параметр командной строки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="526a9-175">**Windows Server 2003 and Windows XP:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-176"><span id="_R"></span><span id="_r"></span>**/R**</span><span class="sxs-lookup"><span data-stu-id="526a9-176"><span id="_R"></span><span id="_r"></span>**/R**</span></span>
</dt> <dd>

<span data-ttu-id="526a9-177">Выполняет восстановление, но не выполняет резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="526a9-177">Performs restore but does not perform backup.</span></span> <span data-ttu-id="526a9-178">Аргумент должен использоваться вместе с параметром командной строки **/s** .</span><span class="sxs-lookup"><span data-stu-id="526a9-178">Must be used together with the **/S** command-line option.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/роллбакк**</span><span class="sxs-lookup"><span data-stu-id="526a9-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span></span>
</dt> <dd>

<span data-ttu-id="526a9-180">Создает теневую копию, которую можно использовать для отката приложения.</span><span class="sxs-lookup"><span data-stu-id="526a9-180">Creates a shadow copy that can be used for application rollback.</span></span>

<span data-ttu-id="526a9-181">**Windows Server 2003:** Этот параметр командной строки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="526a9-181">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *имя файла*</span><span class="sxs-lookup"><span data-stu-id="526a9-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="526a9-183">В случае резервного копирования сохраняет документ резервной копии в файл, указанный параметром *filename*.</span><span class="sxs-lookup"><span data-stu-id="526a9-183">In case of backup, saves the backup document to the file specified by *Filename*.</span></span> <span data-ttu-id="526a9-184">В случае только восстановления загружает документ резервной копии из этого файла.</span><span class="sxs-lookup"><span data-stu-id="526a9-184">In case of restore only, loads the backup document from this file.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/снапшот**</span><span class="sxs-lookup"><span data-stu-id="526a9-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="526a9-186">Создает теневую копию тома, но не выполняет резервное копирование и восстановление.</span><span class="sxs-lookup"><span data-stu-id="526a9-186">Creates a volume shadow copy but does not perform backup or restore.</span></span>

<span data-ttu-id="526a9-187">**Windows Server 2003:** Этот параметр командной строки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="526a9-187">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/стоперрор**</span><span class="sxs-lookup"><span data-stu-id="526a9-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span></span>
</dt> <dd>

<span data-ttu-id="526a9-189">Останавливает выполнение теста при обнаружении ошибки первого модуля записи.</span><span class="sxs-lookup"><span data-stu-id="526a9-189">Stops BETest when the first writer error is encountered.</span></span>

<span data-ttu-id="526a9-190">**Windows Server 2003:** Этот параметр командной строки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="526a9-190">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*</span><span class="sxs-lookup"><span data-stu-id="526a9-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*</span></span>
</dt> <dd>

<span data-ttu-id="526a9-192">Указывает тип резервной копии.</span><span class="sxs-lookup"><span data-stu-id="526a9-192">Specifies the backup type.</span></span> <span data-ttu-id="526a9-193">*BackupType* может быть полным, записывать, копировать, добавочным или разностным.</span><span class="sxs-lookup"><span data-stu-id="526a9-193">*BackupType* can be FULL, LOG, COPY, INCREMENTAL, or DIFFERENTIAL.</span></span> <span data-ttu-id="526a9-194">Дополнительные сведения о типах резервных копий см. в статье [**\_ \_ тип резервного копирования VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span><span class="sxs-lookup"><span data-stu-id="526a9-194">For more information about backup types, see [**VSS\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span></span>

</dd> <dt>

<span data-ttu-id="526a9-195"><span id="_V"></span><span id="_v"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="526a9-195"><span id="_V"></span><span id="_v"></span>**/V**</span></span>
</dt> <dd>

<span data-ttu-id="526a9-196">Создает подробный вывод, который можно использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="526a9-196">Generates verbose output that can be used for troubleshooting.</span></span>

<span data-ttu-id="526a9-197">**Windows Server 2003:** Этот параметр командной строки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="526a9-197">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="526a9-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *имя_файла*</span><span class="sxs-lookup"><span data-stu-id="526a9-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="526a9-199">Выбирает компоненты для резервного копирования или восстановления в зависимости от содержимого XML-файла конфигурации, заданного параметром *filename*.</span><span class="sxs-lookup"><span data-stu-id="526a9-199">Selects the components to be backed up or restored based on the contents of the XML configuration file specified by *Filename*.</span></span> <span data-ttu-id="526a9-200">Этот файл должен содержать только символы ANSI в диапазоне от 0 до 127.</span><span class="sxs-lookup"><span data-stu-id="526a9-200">This file must contain only ANSI characters in the range from 0 through 127.</span></span> <span data-ttu-id="526a9-201">Формат XML-файла определяется схемой в файле BETest.xml.</span><span class="sxs-lookup"><span data-stu-id="526a9-201">The format of the XML file is defined by the schema in the BETest.xml file.</span></span> <span data-ttu-id="526a9-202">Пример файла конфигурации см. в разделе BetestSample.xml.</span><span class="sxs-lookup"><span data-stu-id="526a9-202">For a sample configuration file, see BetestSample.xml.</span></span> <span data-ttu-id="526a9-203">Оба эти файла находятся в каталоге всстулс.</span><span class="sxs-lookup"><span data-stu-id="526a9-203">Both of these files are in the vsstools directory.</span></span>

> [!Note]  
> <span data-ttu-id="526a9-204">Файл BETest.xml можно просмотреть в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="526a9-204">You can view the BETest.xml file in Internet Explorer.</span></span> <span data-ttu-id="526a9-205">Перед открытием этого файла убедитесь, что файл ксдр-счема. XSL находится в том же каталоге, что и BETest.xml.</span><span class="sxs-lookup"><span data-stu-id="526a9-205">Before you open this file, make sure that the xdr-schema.xsl file is in the same directory as BETest.xml.</span></span> <span data-ttu-id="526a9-206">Файл ксдр-счема. xsl содержит инструкции по подготовке к просмотру, которые делают файл BETest.xml более читаемым.</span><span class="sxs-lookup"><span data-stu-id="526a9-206">The xdr-schema.xsl file contains rendering instructions that make the BETest.xml file more readable.</span></span>

 

<span data-ttu-id="526a9-207">**Windows Server 2003:** Этот параметр командной строки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="526a9-207">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a><span data-ttu-id="526a9-208">Пример XML-файла конфигурации: BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="526a9-208">Sample XML Configuration File: BetestSample.xml</span></span>

<span data-ttu-id="526a9-209">Следующий пример файла конфигурации, BetestSample.xml, можно найти в каталоге Всстулс.</span><span class="sxs-lookup"><span data-stu-id="526a9-209">The following sample configuration file, BetestSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

<span data-ttu-id="526a9-210">В этом примере простого файла конфигурации выбирается один компонент для резервного копирования или восстановления.</span><span class="sxs-lookup"><span data-stu-id="526a9-210">This example of a simple configuration file selects one component to be backed up or restored.</span></span>

## <a name="sample-xml-configuration-file-vswritersamplexml"></a><span data-ttu-id="526a9-211">Пример XML-файла конфигурации: VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="526a9-211">Sample XML Configuration File: VswriterSample.xml</span></span>

<span data-ttu-id="526a9-212">Следующий пример файла конфигурации, VswriterSample.xml, можно найти в каталоге Всстулс.</span><span class="sxs-lookup"><span data-stu-id="526a9-212">The following sample configuration file, VswriterSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

<span data-ttu-id="526a9-213">Корневой элемент в этом файле конфигурации называется Тествритер.</span><span class="sxs-lookup"><span data-stu-id="526a9-213">The root element in this configuration file is named TestWriter.</span></span> <span data-ttu-id="526a9-214">Все остальные элементы упорядочиваются по элементу Тествритер.</span><span class="sxs-lookup"><span data-stu-id="526a9-214">All other elements are arranged under the TestWriter element.</span></span>

<span data-ttu-id="526a9-215">Первый атрибут, связанный с Тествритер, — это атрибут Usage.</span><span class="sxs-lookup"><span data-stu-id="526a9-215">The first attribute associated with TestWriter is the usage attribute.</span></span> <span data-ttu-id="526a9-216">Этот атрибут указывает тип использования, сообщаемый с помощью метода [**ивссексаминевритерметадата::-Identity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) .</span><span class="sxs-lookup"><span data-stu-id="526a9-216">This attribute specifies the usage type reported through the [**IVssExamineWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) method.</span></span> <span data-ttu-id="526a9-217">Одним из возможных значений этого атрибута являются \_ данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="526a9-217">One of the possible values for this attribute is USER\_DATA.</span></span>

<span data-ttu-id="526a9-218">Вторым атрибутом является атрибут Делетефилес.</span><span class="sxs-lookup"><span data-stu-id="526a9-218">The second attribute is the deleteFiles attribute.</span></span> <span data-ttu-id="526a9-219">Этот атрибут описан в разделе [Настройка атрибутов модуля записи](vss-test-writer-tool.md).</span><span class="sxs-lookup"><span data-stu-id="526a9-219">This attribute is described in [Configuring Writer Attributes](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="526a9-220">Первым дочерним элементом корневого элемента является элемент Ресторемесод.</span><span class="sxs-lookup"><span data-stu-id="526a9-220">The first child element of the root element is a RestoreMethod element.</span></span> <span data-ttu-id="526a9-221">Этот элемент задает следующее:</span><span class="sxs-lookup"><span data-stu-id="526a9-221">This element specifies the following:</span></span>

-   <span data-ttu-id="526a9-222">Метод Restore (в данном случае Restore \_ , \_ Если \_ можно \_ заменить)</span><span class="sxs-lookup"><span data-stu-id="526a9-222">The restore method (in this case, RESTORE\_IF\_CAN\_BE\_REPLACED)</span></span>
-   <span data-ttu-id="526a9-223">Требует ли модуль записи события восстановления (в данном случае всегда)</span><span class="sxs-lookup"><span data-stu-id="526a9-223">Whether the writer requires restore events (in this case, always)</span></span>
-   <span data-ttu-id="526a9-224">Требуется ли перезагрузка после восстановления модуля записи (в данном случае нет)</span><span class="sxs-lookup"><span data-stu-id="526a9-224">Whether a reboot is required after the writer is restored (in this case, no)</span></span>

<span data-ttu-id="526a9-225">Этот элемент может дополнительно указывать сопоставление альтернативного расположения.</span><span class="sxs-lookup"><span data-stu-id="526a9-225">This element can optionally specify an alternate-location mapping.</span></span> <span data-ttu-id="526a9-226">(В этом случае альтернативное расположение не указано.) Дополнительные сведения см. в разделе [Указание сопоставлений альтернативного расположения](vss-test-writer-tool.md).</span><span class="sxs-lookup"><span data-stu-id="526a9-226">(In this case, no alternate location is specified.) For more information, see [Specifying Alternate Location Mappings](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="526a9-227">Второй дочерний элемент является элементом компонента.</span><span class="sxs-lookup"><span data-stu-id="526a9-227">The second child element is a Component element.</span></span> <span data-ttu-id="526a9-228">Этот элемент заставляет модуль записи добавить компонент в свои метаданные.</span><span class="sxs-lookup"><span data-stu-id="526a9-228">This element causes the writer to add a component to its metadata.</span></span> <span data-ttu-id="526a9-229">Элемент component содержит атрибуты, описывающие компонент и дочерние элементы для описания содержимого компонента, например следующие:</span><span class="sxs-lookup"><span data-stu-id="526a9-229">A Component element contains attributes to describe the component and child elements to describe the content of the component, such as the following:</span></span>

-   <span data-ttu-id="526a9-230">Параметра ComponentType, указывающее, является ли это файловой группой или базой данных (в данном случае, файловой группой)</span><span class="sxs-lookup"><span data-stu-id="526a9-230">componentType to indicate whether this is a filegroup or a database (in this case, a filegroup)</span></span>
-   <span data-ttu-id="526a9-231">Логикалпас для логического пути к компоненту (в данном случае — None)</span><span class="sxs-lookup"><span data-stu-id="526a9-231">logicalPath for the component logical path (in this case, none is specified)</span></span>
-   <span data-ttu-id="526a9-232">componentName для имени компонента (в данном случае "Тестфилес")</span><span class="sxs-lookup"><span data-stu-id="526a9-232">componentName for the name of the component (in this case, "TestFiles")</span></span>
-   <span data-ttu-id="526a9-233">Выберите параметр, чтобы указать состояние для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="526a9-233">selectable to indicate selectable-for-backup status</span></span>

<span data-ttu-id="526a9-234">Элемент Component также имеет дочерний элемент с именем Компонентфиле, который добавляет спецификацию файла в этот компонент.</span><span class="sxs-lookup"><span data-stu-id="526a9-234">The Component element also has a child element named ComponentFile to add a file specification to this component.</span></span> <span data-ttu-id="526a9-235">(Элемент компонента может иметь произвольное число элементов Компонентфиле, которые можно указать для каждого компонента.) Этот элемент Компонентфиле имеет следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="526a9-235">(A Component element can have an arbitrary number of ComponentFile elements that can be specified for each component.) This ComponentFile element has the following attributes:</span></span>

-   <span data-ttu-id="526a9-236">path = "c: \\ тестпас"</span><span class="sxs-lookup"><span data-stu-id="526a9-236">path="c:\\TestPath"</span></span>
-   <span data-ttu-id="526a9-237">filespec = " \* "</span><span class="sxs-lookup"><span data-stu-id="526a9-237">filespec="\*"</span></span>
-   <span data-ttu-id="526a9-238">recursive = "нет"</span><span class="sxs-lookup"><span data-stu-id="526a9-238">recursive="no"</span></span>

 

 



