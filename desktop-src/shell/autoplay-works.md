---
description: Создание приложения с поддержкой автозапуска — это простая процедура. В этом разделе используется компакт-диск в качестве примера (он был первым носителем для реализации этой технологии), но на сегодняшний день существует множество различных типов носителей, которые могут использовать его.
title: Создание приложения AutoRun-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 24a944b011c926d1638e5d0bcb0d35fc348e5783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143978"
---
# <a name="creating-an-autorun-enabled-application"></a><span data-ttu-id="324c3-104">Создание приложения AutoRun-Enabled</span><span class="sxs-lookup"><span data-stu-id="324c3-104">Creating an AutoRun-Enabled Application</span></span>

<span data-ttu-id="324c3-105">Создание приложения с поддержкой автозапуска — это простая процедура.</span><span class="sxs-lookup"><span data-stu-id="324c3-105">Creating an AutoRun-enabled application is a straightforward procedure.</span></span> <span data-ttu-id="324c3-106">В этом разделе используется компакт-диск в качестве примера (он был первым носителем для реализации этой технологии), но на сегодняшний день существует множество различных типов носителей, которые могут использовать его.</span><span class="sxs-lookup"><span data-stu-id="324c3-106">This topic uses CD-ROM as an example (it was the first medium to implement this technology) but today there are many different media types that can use it.</span></span>

<span data-ttu-id="324c3-107">Чтобы включить функцию автозапуска в приложении, просто включите два необходимых файла:</span><span class="sxs-lookup"><span data-stu-id="324c3-107">To enable AutoRun in your application, you simply include two essential files:</span></span>

-   <span data-ttu-id="324c3-108">Файл autorun. INF</span><span class="sxs-lookup"><span data-stu-id="324c3-108">An Autorun.inf file</span></span>
-   <span data-ttu-id="324c3-109">Запускаемое приложение</span><span class="sxs-lookup"><span data-stu-id="324c3-109">A startup application</span></span>

<span data-ttu-id="324c3-110">Когда пользователь вставляет диск в дисковод компакт-дисков на компьютере, совместимом с автозагрузками, система немедленно проверяет наличие у диска файловой системы с персональным компьютером.</span><span class="sxs-lookup"><span data-stu-id="324c3-110">When a user inserts a disc into a CD-ROM drive on a AutoRun-compatible computer, the system immediately checks to see if the disc has a personal computer file system.</span></span> <span data-ttu-id="324c3-111">Если это так, система выполняет поиск файла с именем [Autorun. INF](#creating-an-autoruninf-file).</span><span class="sxs-lookup"><span data-stu-id="324c3-111">If it does, the system searches for a file named [Autorun.inf](#creating-an-autoruninf-file).</span></span> <span data-ttu-id="324c3-112">В этом файле указывается приложение установки, которое будет запущено вместе с множеством необязательных параметров.</span><span class="sxs-lookup"><span data-stu-id="324c3-112">This file specifies a setup application that will be run, along with a variety of optional settings.</span></span> <span data-ttu-id="324c3-113">Обычно запускаемое приложение устанавливает, удаляет, настраивает и, возможно, запускает приложение.</span><span class="sxs-lookup"><span data-stu-id="324c3-113">The startup application typically installs, uninstalls, configures, and perhaps runs the application.</span></span>

-   [<span data-ttu-id="324c3-114">Создание файла autorun. INF</span><span class="sxs-lookup"><span data-stu-id="324c3-114">Creating an Autorun.inf File</span></span>](#creating-an-autoruninf-file)
-   <span data-ttu-id="324c3-115">[\[Раздел девицеинсталл \]](#the-deviceinstall-section)</span><span class="sxs-lookup"><span data-stu-id="324c3-115">[The \[DeviceInstall\] Section](#the-deviceinstall-section)</span></span>
-   [<span data-ttu-id="324c3-116">См. также</span><span class="sxs-lookup"><span data-stu-id="324c3-116">Related topics</span></span>](#related-topics)

## <a name="creating-an-autoruninf-file"></a><span data-ttu-id="324c3-117">Создание файла autorun. INF</span><span class="sxs-lookup"><span data-stu-id="324c3-117">Creating an Autorun.inf File</span></span>

<span data-ttu-id="324c3-118">Autorun. INF — это текстовый файл, расположенный в корневом каталоге компакт-диска, который содержит приложение.</span><span class="sxs-lookup"><span data-stu-id="324c3-118">Autorun.inf is a text file located in the root directory of the CD-ROM that contains your application.</span></span> <span data-ttu-id="324c3-119">Его основная функция заключается в том, чтобы предоставить системе имя и расположение программы запуска приложения, которая будет запускаться при вставке диска.</span><span class="sxs-lookup"><span data-stu-id="324c3-119">Its primary function is to provide the system with the name and location of the application's startup program that will be run when the disc is inserted.</span></span>

> [!Note]  
> <span data-ttu-id="324c3-120">Файлы Autorun. inf не поддерживаются в Windows XP для дисков, которые возвращают диск, \_ съемный из [**жетдриветипе**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span><span class="sxs-lookup"><span data-stu-id="324c3-120">Autorun.inf files are not supported under Windows XP for drives that return DRIVE\_REMOVABLE from [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span></span>

 

<span data-ttu-id="324c3-121">Файл autorun. INF также может содержать дополнительные сведения, включая:</span><span class="sxs-lookup"><span data-stu-id="324c3-121">The Autorun.inf file can also contain optional information including:</span></span>

-   <span data-ttu-id="324c3-122">Имя файла, содержащего значок, который будет представлять устройство чтения компакт-дисков приложения.</span><span class="sxs-lookup"><span data-stu-id="324c3-122">The name of a file that contains an icon that will represent your application's CD-ROM drive.</span></span> <span data-ttu-id="324c3-123">Этот значок будет отображаться проводником Windows вместо стандартного значка диска.</span><span class="sxs-lookup"><span data-stu-id="324c3-123">This icon will be displayed by Windows Explorer in place of the standard drive icon.</span></span>
-   <span data-ttu-id="324c3-124">Дополнительные команды для контекстного меню, которые отображаются, когда пользователь щелкает правой кнопкой мыши значок компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="324c3-124">Additional commands for the shortcut menu that is displayed when the user right-clicks the CD-ROM icon.</span></span> <span data-ttu-id="324c3-125">Можно также указать команду по умолчанию, которая выполняется при двойном щелчке значка пользователем.</span><span class="sxs-lookup"><span data-stu-id="324c3-125">You can also specify the default command that is run when the user double-clicks the icon.</span></span>

<span data-ttu-id="324c3-126">Файлы Autorun. INF похожи на ini-файлы.</span><span class="sxs-lookup"><span data-stu-id="324c3-126">Autorun.inf files are similar to .ini files.</span></span> <span data-ttu-id="324c3-127">Они состоят из одного или нескольких разделов, каждый из которых направляется по имени, заключенному в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="324c3-127">They consist of one or more sections, each headed by a name enclosed in square brackets.</span></span> <span data-ttu-id="324c3-128">Каждый раздел содержит ряд команд, которые будут запускаться оболочкой при вставке диска.</span><span class="sxs-lookup"><span data-stu-id="324c3-128">Each section contains a series of commands that will be run by the Shell when the disc is inserted.</span></span> <span data-ttu-id="324c3-129">Существуют два раздела, которые в настоящее время определены для файлов autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="324c3-129">There are two sections that are currently defined for Autorun.inf files.</span></span>

-   <span data-ttu-id="324c3-130">Раздел **\[ автозапуска \]** содержит команды автозапуска по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="324c3-130">The **\[autorun\]** section contains the default AutoRun commands.</span></span> <span data-ttu-id="324c3-131">Все файлы Autorun. inf должны содержать раздел **\[ Autorun \]** .</span><span class="sxs-lookup"><span data-stu-id="324c3-131">All Autorun.inf files must have an **\[autorun\]** section.</span></span>
-   <span data-ttu-id="324c3-132">Необязательный раздел **\[ Autorun \] . Alpha** можно включить для систем, работающих на компьютерах с RISC-процессорами.</span><span class="sxs-lookup"><span data-stu-id="324c3-132">An optional **\[autorun.alpha\]** section can be included for systems running on RISC-based computers.</span></span> <span data-ttu-id="324c3-133">При вставке диска в дисковод компакт-дисков в системе с RISC-процессором оболочка будет выполнять команды в этом разделе, а не в разделе **\[ автозапуска \]** .</span><span class="sxs-lookup"><span data-stu-id="324c3-133">When a disc is inserted in a CD-ROM drive on a RISC-based system, the Shell will run the commands in this section instead of those in the **\[autorun\]** section.</span></span>

> [!Note]  
> <span data-ttu-id="324c3-134">Сначала оболочка проверяет раздел для конкретной архитектуры.</span><span class="sxs-lookup"><span data-stu-id="324c3-134">The Shell checks for an architecture-specific section first.</span></span> <span data-ttu-id="324c3-135">Если он не найден, то он использует информацию из раздела **\[ Autorun \]** .</span><span class="sxs-lookup"><span data-stu-id="324c3-135">If it does not find one, it uses the information in the **\[autorun\]** section.</span></span> <span data-ttu-id="324c3-136">После того как оболочка обнаружит раздел, он пропускает все остальные, поэтому каждый раздел должен быть самодостаточным.</span><span class="sxs-lookup"><span data-stu-id="324c3-136">After the Shell finds a section, it ignores all others, so each section must be self-contained.</span></span>

 

<span data-ttu-id="324c3-137">Каждый раздел содержит ряд команд, которые определяют, как выполняется операция автозапуска.</span><span class="sxs-lookup"><span data-stu-id="324c3-137">Each section contains a series of commands that determine how the Autorun operation takes place.</span></span> <span data-ttu-id="324c3-138">Доступно пять команд.</span><span class="sxs-lookup"><span data-stu-id="324c3-138">There are five commands available.</span></span>



| <span data-ttu-id="324c3-139">Команда</span><span class="sxs-lookup"><span data-stu-id="324c3-139">Command</span></span>                         | <span data-ttu-id="324c3-140">Описание</span><span class="sxs-lookup"><span data-stu-id="324c3-140">Description</span></span>                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="324c3-141">дефаултикон</span><span class="sxs-lookup"><span data-stu-id="324c3-141">defaulticon</span></span>](autorun-cmds.md) | <span data-ttu-id="324c3-142">Задает значок по умолчанию для приложения.</span><span class="sxs-lookup"><span data-stu-id="324c3-142">Specifies the default icon for the application.</span></span>                                        |
| [<span data-ttu-id="324c3-143">значок</span><span class="sxs-lookup"><span data-stu-id="324c3-143">icon</span></span>](autorun-cmds.md)        | <span data-ttu-id="324c3-144">Указывает путь и имя файла для конкретного значка устройства чтения компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="324c3-144">Specifies the path and file name of an application-specific icon for the CD-ROM drive.</span></span> |
| [<span data-ttu-id="324c3-145">open</span><span class="sxs-lookup"><span data-stu-id="324c3-145">open</span></span>](autorun-cmds.md)        | <span data-ttu-id="324c3-146">Указывает путь и имя файла запускаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="324c3-146">Specifies the path and file name of the startup application.</span></span>                           |
| [<span data-ttu-id="324c3-147">усеауторун</span><span class="sxs-lookup"><span data-stu-id="324c3-147">useautorun</span></span>](autorun-cmds.md)  | <span data-ttu-id="324c3-148">Указывает, что при поддержке следует использовать функции автозапуска v2.</span><span class="sxs-lookup"><span data-stu-id="324c3-148">Specifies that Autoplay V2 features should be used if supported.</span></span>                       |
| [<span data-ttu-id="324c3-149">консоль</span><span class="sxs-lookup"><span data-stu-id="324c3-149">shell</span></span>](autorun-cmds.md)       | <span data-ttu-id="324c3-150">Определяет команду по умолчанию в контекстном меню компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="324c3-150">Defines the default command in the CD-ROM's shortcut menu.</span></span>                             |
| [<span data-ttu-id="324c3-151">\_команда оболочки</span><span class="sxs-lookup"><span data-stu-id="324c3-151">shell\_verb</span></span>](autorun-cmds.md) | <span data-ttu-id="324c3-152">Добавляет команды в контекстное меню компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="324c3-152">Adds commands to the CD-ROM's shortcut menu.</span></span>                                           |



 

<span data-ttu-id="324c3-153">Ниже приведен пример простого файла autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="324c3-153">The following is an example of a simple Autorun.inf file.</span></span> <span data-ttu-id="324c3-154">Он указывает Filename.exe в качестве запускаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="324c3-154">It specifies Filename.exe as the startup application.</span></span> <span data-ttu-id="324c3-155">Второй значок в Filename.exe будет представлять дисковод компакт-дисков вместо стандартного значка диска.</span><span class="sxs-lookup"><span data-stu-id="324c3-155">The second icon in Filename.exe will represent the CD-ROM drive instead of the standard drive icon.</span></span>


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



<span data-ttu-id="324c3-156">В этом примере файла autorun. INF выполняются различные запускаемые приложения в зависимости от типа компьютера.</span><span class="sxs-lookup"><span data-stu-id="324c3-156">This Autorun.inf sample runs different startup applications depending on the type of computer.</span></span>


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a><span data-ttu-id="324c3-157">\[Раздел девицеинсталл \]</span><span class="sxs-lookup"><span data-stu-id="324c3-157">The \[DeviceInstall\] Section</span></span>

<span data-ttu-id="324c3-158">Вы можете использовать раздел **\[ девицеинсталл \]** на любом съемном носителе.</span><span class="sxs-lookup"><span data-stu-id="324c3-158">You can use the **\[DeviceInstall\]** section on any removable media.</span></span> <span data-ttu-id="324c3-159">Он поддерживается только в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="324c3-159">It is supported only under Windows XP.</span></span> <span data-ttu-id="324c3-160">**DriverPath** используется для указания пути к каталогу, в котором Windows XP ищет файлы драйверов, что позволяет не допустить продолжительного поиска по всему содержимому.</span><span class="sxs-lookup"><span data-stu-id="324c3-160">You use **DriverPath** to specify a directory path where Windows XP searches for driver files, which prevents a lengthy search through the entire contents.</span></span>

<span data-ttu-id="324c3-161">Используйте раздел **\[ девицеинсталл \]** с установкой драйвера, чтобы указать каталоги, в которых Windows XP должна выполнять поиск файлов драйверов на носителе.</span><span class="sxs-lookup"><span data-stu-id="324c3-161">You use the **\[DeviceInstall\]** section with a driver installation to specify directories where Windows XP should search the media for driver files.</span></span> <span data-ttu-id="324c3-162">В Windows XP по умолчанию не выполняется поиск по всему носителю, поэтому требуется **\[ девицеинсталл \]** для указания расположения поиска.</span><span class="sxs-lookup"><span data-stu-id="324c3-162">Under Windows XP, entire media are no longer searched by default, therefore requiring **\[DeviceInstall\]** to specify search locations.</span></span> <span data-ttu-id="324c3-163">Ниже приведен единственный съемный носитель, который полностью ищется в Windows XP без раздела **\[ девицеинсталл \]** в файле autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="324c3-163">The following are the only removable media that Windows XP fully searches without a **\[DeviceInstall\]** section in an Autorun.inf file.</span></span>

-   <span data-ttu-id="324c3-164">Обнаружены гибкие диски на дисках A или B.</span><span class="sxs-lookup"><span data-stu-id="324c3-164">Floppy disks found in drives A or B.</span></span>
-   <span data-ttu-id="324c3-165">КОМПАКТ-диск или DVD-диск меньше размера 1 гигабайта (ГБ).</span><span class="sxs-lookup"><span data-stu-id="324c3-165">CD/DVD media less that 1 gigabyte (GB) in size.</span></span>

<span data-ttu-id="324c3-166">Все остальные носители должны содержать раздел **\[ Девицеинсталл \]** для Windows XP, чтобы обнаружить драйверы, хранящиеся на этом носителе.</span><span class="sxs-lookup"><span data-stu-id="324c3-166">All other media must include a **\[DeviceInstall\]** section for Windows XP to detect any drivers stored on that media.</span></span>

> [!Note]  
> <span data-ttu-id="324c3-167">Как и в разделе **\[ Autorun \]** , раздел **\[ девицеинсталл \]** может быть зависящим от архитектуры.</span><span class="sxs-lookup"><span data-stu-id="324c3-167">As with the **\[AutoRun\]** section, the **\[DeviceInstall\]** section can be architecture-specific.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="324c3-168">См. также</span><span class="sxs-lookup"><span data-stu-id="324c3-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="324c3-169">Как реализовать запускаемые приложения автозапуска</span><span class="sxs-lookup"><span data-stu-id="324c3-169">How to Implement Autorun Startup Applications</span></span>](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[<span data-ttu-id="324c3-170">Создание приложения для установки устройства</span><span class="sxs-lookup"><span data-stu-id="324c3-170">Writing a Device Installation Application</span></span>](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
