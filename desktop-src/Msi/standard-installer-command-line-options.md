---
<span data-ttu-id="39669-101">Описание: исполняемая программа, которая интерпретирует пакеты и устанавливает продукты, является Msiexec.exe. Примечание. Программа Msiexec также устанавливает уровень ошибок, соответствующий кодам системных ошибок.</span><span class="sxs-lookup"><span data-stu-id="39669-101">description: The executable program that interprets packages and installs products is Msiexec.exe.Note  Msiexec also sets an error level on return that corresponds to System Error Codes.</span></span> <span data-ttu-id="39669-102">В следующей таблице приведены стандартные параметры командной строки для этой программы.</span><span class="sxs-lookup"><span data-stu-id="39669-102">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="39669-103">Параметры командной строки не чувствительны к регистру. Установщик Windows 2,0: параметры командной строки, указанные в этом разделе, доступны начиная с установщик Windows 3,0.</span><span class="sxs-lookup"><span data-stu-id="39669-103">Command-line options are case insensitive.Windows Installer 2.0:  The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="39669-104">Параметры Command-Line установщик Windows доступны в установщик Windows&\# 160; 3.0 и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="39669-104">The Windows Installer Command-Line Options are available with Windows Installer&\#160;3.0 and earlier versions.</span></span>
<span data-ttu-id="39669-105">MS. AssetID: b1707c88-1cca-45ab-bb23-6002bfd5204e Title: Стандартный установщик Command-Line параметры MS. Topic: статья MS. Date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="39669-105">ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e title: Standard Installer Command-Line Options ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="standard-installer-command-line-options"></a><span data-ttu-id="39669-106">Параметры Command-Line стандартного установщика</span><span class="sxs-lookup"><span data-stu-id="39669-106">Standard Installer Command-Line Options</span></span>

<span data-ttu-id="39669-107">Исполняемая программа, которая интерпретирует пакеты и устанавливает продукты, Msiexec.exe.</span><span class="sxs-lookup"><span data-stu-id="39669-107">The executable program that interprets packages and installs products is Msiexec.exe.</span></span>

> [!Note]  
> <span data-ttu-id="39669-108">Кроме того, msiexec устанавливает уровень ошибок, соответствующий [кодам системных ошибок](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="39669-108">Msiexec also sets an error level on return that corresponds to [System Error Codes](../debug/system-error-codes.md).</span></span>

 

<span data-ttu-id="39669-109">В следующей таблице приведены стандартные параметры командной строки для этой программы.</span><span class="sxs-lookup"><span data-stu-id="39669-109">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="39669-110">Параметры командной строки не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="39669-110">Command-line options are case insensitive.</span></span>

<span data-ttu-id="39669-111">**Установщик Windows 2,0:** Параметры командной строки, указанные в этом разделе, доступны начиная с установщик Windows 3,0.</span><span class="sxs-lookup"><span data-stu-id="39669-111">**Windows Installer 2.0:** The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="39669-112">[Параметры командной строки](command-line-options.md) установщик Windows доступны в установщик Windows 3,0 и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="39669-112">The Windows Installer [Command-Line Options](command-line-options.md) are available with Windows Installer 3.0 and earlier versions.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39669-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="39669-113">Option</span></span></th>
<th><span data-ttu-id="39669-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="39669-114">Parameters</span></span></th>
<th><span data-ttu-id="39669-115">Значение</span><span class="sxs-lookup"><span data-stu-id="39669-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39669-116"><strong>/help</strong></span><span class="sxs-lookup"><span data-stu-id="39669-116"><strong>/help</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="39669-117">Справка и быстрый справочник.</span><span class="sxs-lookup"><span data-stu-id="39669-117">Help and quick reference option.</span></span> <span data-ttu-id="39669-118">Отображает правильное использование команды установки, включая список всех параметров и поведений.</span><span class="sxs-lookup"><span data-stu-id="39669-118">Displays the correct usage of the setup command including a list of all switches and behavior.</span></span> <span data-ttu-id="39669-119">Описание использования может отображаться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="39669-119">The description of usage can be displayed in the user interface.</span></span> <span data-ttu-id="39669-120">Неправильное использование любого параметра вызывает этот параметр справки.</span><span class="sxs-lookup"><span data-stu-id="39669-120">Incorrect use of any option invokes this help option.</span></span><br/> <span data-ttu-id="39669-121">Пример: <strong>msiexec/Help</strong></span><span class="sxs-lookup"><span data-stu-id="39669-121">Example: <strong>msiexec /help</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-122">Эквивалентный установщик Windows <a href="command-line-options.md">параметр командной строки</a> — <strong>/?</strong>.</span><span class="sxs-lookup"><span data-stu-id="39669-122">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/?</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39669-123"><strong>/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="39669-123"><strong>/quiet</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="39669-124">Тихий режим вывода.</span><span class="sxs-lookup"><span data-stu-id="39669-124">Quiet display option.</span></span> <span data-ttu-id="39669-125">Установщик запускает установку без отображения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="39669-125">The installer runs an installation without displaying a user interface.</span></span> <span data-ttu-id="39669-126">Пользователю не выводятся запросы, сообщения или диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="39669-126">No prompts, messages, or dialog boxes are displayed to the user.</span></span> <span data-ttu-id="39669-127">Пользователь не может отменить установку.</span><span class="sxs-lookup"><span data-stu-id="39669-127">The user cannot cancel the installation.</span></span> <span data-ttu-id="39669-128">Используйте стандартные параметры командной строки <strong>/norestart</strong> или <strong>/форцерестарт</strong> для управления перезагрузками.</span><span class="sxs-lookup"><span data-stu-id="39669-128">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="39669-129">Если параметры перезагрузки не указаны, установщик перезапускает компьютер при необходимости, не отображая пользователю никаких запросов или предупреждений.</span><span class="sxs-lookup"><span data-stu-id="39669-129">If no reboot options are specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span><br/> <span data-ttu-id="39669-130">Примеры:</span><span class="sxs-lookup"><span data-stu-id="39669-130">Examples:</span></span> <br/> <span data-ttu-id="39669-131"><strong>msiexec/Package Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="39669-131"><strong>msiexec /package Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="39669-132"><strong>Msiexec/uninstall Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="39669-132"><strong>Msiexec /uninstall Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="39669-133"><strong>Msiexec/Update мсипатч. MSP/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="39669-133"><strong>Msiexec /update msipatch.msp /quiet</strong></span></span><br/> <span data-ttu-id="39669-134"><strong>Msiexec/uninstall мсипатч. MSP/Package Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="39669-134"><strong>Msiexec /uninstall msipatch.msp /package Application.msi / quiet</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-135">Эквивалентный <a href="command-line-options.md">параметр командной строки</a> установщик Windows — <strong>/qn</strong>.</span><span class="sxs-lookup"><span data-stu-id="39669-135">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qn</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39669-136"><strong>/passive</strong></span><span class="sxs-lookup"><span data-stu-id="39669-136"><strong>/passive</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="39669-137">Параметр пассивного экрана.</span><span class="sxs-lookup"><span data-stu-id="39669-137">Passive display option.</span></span> <span data-ttu-id="39669-138">Установщик отображает индикатор выполнения для пользователя, который указывает, что установка выполняется, но для пользователя не отображаются запросы и сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="39669-138">The installer displays a progress bar to the user that indicates that an installation is in progress but no prompts or error messages are displayed to the user.</span></span> <span data-ttu-id="39669-139">Пользователь не может отменить установку.</span><span class="sxs-lookup"><span data-stu-id="39669-139">The user cannot cancel the installation.</span></span> <span data-ttu-id="39669-140">Используйте стандартные параметры командной строки <strong>/norestart</strong> или <strong>/форцерестарт</strong> для управления перезагрузками.</span><span class="sxs-lookup"><span data-stu-id="39669-140">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="39669-141">Если параметр reboot не указан, установщик перезапускает компьютер при необходимости, не отображая пользователю никаких запросов или предупреждений.</span><span class="sxs-lookup"><span data-stu-id="39669-141">If no reboot option is specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span> <br/> <span data-ttu-id="39669-142">Пример: <strong>msiexec/package Application.msi/passive</strong> </span><span class="sxs-lookup"><span data-stu-id="39669-142">Example: <strong>msiexec /package Application.msi /passive</strong> </span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-143">Эквивалентный установщик Windows <a href="command-line-options.md">параметр командной строки</a> — <strong>/QB!-</strong> With <a href="rebootprompt.md"><strong>ребутпромпт</strong></a>= S Set в командной строке.</span><span class="sxs-lookup"><span data-stu-id="39669-143">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qb!-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>=S set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39669-144"><strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="39669-144"><strong>/norestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="39669-145">Параметр "никогда не перезапускать".</span><span class="sxs-lookup"><span data-stu-id="39669-145">Never restart option.</span></span> <span data-ttu-id="39669-146">Установщик никогда не перезагружает компьютер после установки.</span><span class="sxs-lookup"><span data-stu-id="39669-146">The installer never restarts the computer after the installation.</span></span><br/> <span data-ttu-id="39669-147">Пример: msiexec/Package Application.msi <strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="39669-147">Example: msiexec /package Application.msi <strong>/norestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-148">Эквивалентная Командная строка установщик Windows в командной строке — <a href="reboot.md"><strong>Перезагрузка</strong></a>= реаллисуппресс.</span><span class="sxs-lookup"><span data-stu-id="39669-148">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39669-149"><strong>/форцерестарт</strong></span><span class="sxs-lookup"><span data-stu-id="39669-149"><strong>/forcerestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="39669-150">Параметр всегда перезапуска.</span><span class="sxs-lookup"><span data-stu-id="39669-150">Always restart option.</span></span> <span data-ttu-id="39669-151">Установщик всегда перезапускает компьютер после каждой установки.</span><span class="sxs-lookup"><span data-stu-id="39669-151">The installer always restarts the computer after every installation.</span></span><br/> <span data-ttu-id="39669-152">Пример: msiexec/Package Application.msi <strong>/форцерестарт</strong></span><span class="sxs-lookup"><span data-stu-id="39669-152">Example: msiexec /package Application.msi <strong>/forcerestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-153">Эквивалентная Командная строка, соответствующая установщик Windows командной строке, имеет значение <a href="reboot.md"><strong>reboot</strong></a>= принудительно задано в командной строке.</span><span class="sxs-lookup"><span data-stu-id="39669-153">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=Force set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39669-154"><strong>/promptrestart</strong></span><span class="sxs-lookup"><span data-stu-id="39669-154"><strong>/promptrestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="39669-155">Запрос перед перезапуском параметра.</span><span class="sxs-lookup"><span data-stu-id="39669-155">Prompt before restarting option.</span></span> <span data-ttu-id="39669-156">Выводит сообщение о том, что для завершения установки требуется перезагрузка, и пользователю предлагается ли перезапустить систему сейчас.</span><span class="sxs-lookup"><span data-stu-id="39669-156">Displays a message that a restart is required to complete the installation and asks the user whether to restart the system now.</span></span> <span data-ttu-id="39669-157">Этот параметр нельзя использовать вместе с параметром <strong>/quiet</strong> .</span><span class="sxs-lookup"><span data-stu-id="39669-157">This option cannot be used together with the <strong>/quiet</strong> option.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-158">Эквивалентная Командная строка установщик Windows <a href="rebootprompt.md"><strong>ребутпромпт</strong></a>  =  &quot; &quot; задана в командной строке.</span><span class="sxs-lookup"><span data-stu-id="39669-158">The equivalent Windows Installer command line has <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a> = &quot;&quot; set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39669-159"><strong>/uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="39669-159"><strong>/uninstall</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="39669-160">Параметр удаления продукта.</span><span class="sxs-lookup"><span data-stu-id="39669-160">Uninstall product option.</span></span> <span data-ttu-id="39669-161">Удаляет продукт.</span><span class="sxs-lookup"><span data-stu-id="39669-161">Uninstalls a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-162">Эквивалентный установщик Windows <a href="command-line-options.md">параметр командной строки</a> — <strong>/x</strong>.</span><span class="sxs-lookup"><span data-stu-id="39669-162">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/x</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39669-163"><strong>/uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="39669-163"><strong>/uninstall</strong></span></span></td>
<td><span data-ttu-id="39669-164"><em>/Package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1> [; Update2. MSP | PatchGUID2]</em></span><span class="sxs-lookup"><span data-stu-id="39669-164"><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1>[;Update2.msp | PatchGUID2]</em></span></span></td>
<td><span data-ttu-id="39669-165">Удаление параметра обновления.</span><span class="sxs-lookup"><span data-stu-id="39669-165">Uninstall update option.</span></span> <span data-ttu-id="39669-166">Удаляет обновление.</span><span class="sxs-lookup"><span data-stu-id="39669-166">Uninstalls an update patch.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-167">Эквивалентный <a href="command-line-options.md">параметр командной строки</a> установщик Windows — <strong>/i</strong> с <a href="msipatchremove.md"><strong>мсипатчремове</strong></a>= update1. MSP | PatchGUID1[; Update2. MSP | PatchGUID2] задается в командной строке.</span><span class="sxs-lookup"><span data-stu-id="39669-167">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong> with <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>=Update1.msp | PatchGUID1[;Update2.msp | PatchGUID2] set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39669-168"><strong>/log</strong></span><span class="sxs-lookup"><span data-stu-id="39669-168"><strong>/log</strong></span></span></td>
<td><em><logfile></em></td>
<td><span data-ttu-id="39669-169">Параметр log.</span><span class="sxs-lookup"><span data-stu-id="39669-169">Log option.</span></span> <span data-ttu-id="39669-170">Записывает данные журнала в файл журнала по указанному существующему пути.</span><span class="sxs-lookup"><span data-stu-id="39669-170">Writes logging information into a log file at the specified existing path.</span></span> <span data-ttu-id="39669-171">Путь к расположению файла журнала должен уже существовать.</span><span class="sxs-lookup"><span data-stu-id="39669-171">The path to the log file location must already exist.</span></span> <span data-ttu-id="39669-172">Установщик не создает структуру каталогов для файла журнала.</span><span class="sxs-lookup"><span data-stu-id="39669-172">The installer does not create the directory structure for the logfile.</span></span><br/> <span data-ttu-id="39669-173">В журнал вносятся следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="39669-173">The following information is entered into the log:</span></span><br/>
<ul>
<li><span data-ttu-id="39669-174">Сообщения о состоянии</span><span class="sxs-lookup"><span data-stu-id="39669-174">Status messages</span></span></li>
<li><span data-ttu-id="39669-175">Некритические предупреждения</span><span class="sxs-lookup"><span data-stu-id="39669-175">Nonfatal warnings</span></span></li>
<li><span data-ttu-id="39669-176">Все сообщения об ошибках</span><span class="sxs-lookup"><span data-stu-id="39669-176">All error messages</span></span></li>
<li><span data-ttu-id="39669-177">Запуск действий</span><span class="sxs-lookup"><span data-stu-id="39669-177">Start up of actions</span></span></li>
<li><span data-ttu-id="39669-178">Записи, относящиеся к действию</span><span class="sxs-lookup"><span data-stu-id="39669-178">Action-specific records</span></span></li>
<li><span data-ttu-id="39669-179">Запросы пользователей</span><span class="sxs-lookup"><span data-stu-id="39669-179">User requests</span></span></li>
<li><span data-ttu-id="39669-180">Начальные параметры пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="39669-180">Initial UI parameters</span></span></li>
<li><span data-ttu-id="39669-181">Сведения о нехватке памяти или аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="39669-181">Out-of-memory or fatal exit information</span></span></li>
<li><span data-ttu-id="39669-182">Сообщения о нехватке места на диске</span><span class="sxs-lookup"><span data-stu-id="39669-182">Out-of-disk-space messages</span></span></li>
<li><span data-ttu-id="39669-183">Свойства терминала</span><span class="sxs-lookup"><span data-stu-id="39669-183">Terminal properties</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-184">Эквивалентный установщик Windows <a href="command-line-options.md">параметр командной строки</a> — <strong>/l \*</strong>.</span><span class="sxs-lookup"><span data-stu-id="39669-184">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/L\*</strong>.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-185">Дополнительные сведения о всех методах, доступных для настройки режима ведения журнала, см. в разделе " <a href="normal-logging.md">нормальное ведение журнала</a> " раздела <a href="windows-installer-logging.md">установщик Windows Logging</a> .</span><span class="sxs-lookup"><span data-stu-id="39669-185">For more information about all the methods that are available for setting the logging mode, see <a href="normal-logging.md">Normal Logging</a> in the <a href="windows-installer-logging.md">Windows Installer Logging</a> section.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39669-186"><strong>/Package</strong></span><span class="sxs-lookup"><span data-stu-id="39669-186"><strong>/package</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="39669-187">Установите параметр продукта.</span><span class="sxs-lookup"><span data-stu-id="39669-187">Install product option.</span></span> <span data-ttu-id="39669-188">Устанавливает или настраивает продукт.</span><span class="sxs-lookup"><span data-stu-id="39669-188">Installs or configures a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-189">Эквивалентный <a href="command-line-options.md">параметр командной строки</a> установщик Windows — <strong>/i</strong>.</span><span class="sxs-lookup"><span data-stu-id="39669-189">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39669-190"><strong>/Update</strong></span><span class="sxs-lookup"><span data-stu-id="39669-190"><strong>/update</strong></span></span></td>
<td><span data-ttu-id="39669-191"><em><Update1.msp>[; Update2. MSP]</em></span><span class="sxs-lookup"><span data-stu-id="39669-191"><em><Update1.msp>[;Update2.msp]</em></span></span></td>
<td><span data-ttu-id="39669-192">Параметр установки исправлений.</span><span class="sxs-lookup"><span data-stu-id="39669-192">Install patches option.</span></span> <span data-ttu-id="39669-193">Устанавливает один или несколько исправлений.</span><span class="sxs-lookup"><span data-stu-id="39669-193">Installs one or multiple patches.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="39669-194">Эквивалентная установщик Windows командной строки <a href="patch.md"><strong>Patch</strong></a> = [мсипатч. msp] <; PatchGuid2> задается в командной строке.</span><span class="sxs-lookup"><span data-stu-id="39669-194">The equivalent Windows Installer command line has <a href="patch.md"><strong>PATCH</strong></a> = [msipatch.msp]<;PatchGuid2> set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
