---
Описание: исполняемая программа, которая интерпретирует пакеты и устанавливает продукты, является Msiexec.exe. Примечание. Программа Msiexec также устанавливает уровень ошибок, соответствующий кодам системных ошибок. В следующей таблице приведены стандартные параметры командной строки для этой программы. Параметры командной строки не чувствительны к регистру. Установщик Windows 2,0: параметры командной строки, указанные в этом разделе, доступны начиная с установщик Windows 3,0. Параметры Command-Line установщик Windows доступны в установщик Windows&\# 160; 3.0 и более ранних версиях.
MS. AssetID: b1707c88-1cca-45ab-bb23-6002bfd5204e Title: Стандартный установщик Command-Line параметры MS. Topic: статья MS. Date: 05/31/2018
---

# <a name="standard-installer-command-line-options"></a>Параметры Command-Line стандартного установщика

Исполняемая программа, которая интерпретирует пакеты и устанавливает продукты, Msiexec.exe.

> [!Note]  
> Кроме того, msiexec устанавливает уровень ошибок, соответствующий [кодам системных ошибок](../debug/system-error-codes.md).

 

В следующей таблице приведены стандартные параметры командной строки для этой программы. Параметры командной строки не чувствительны к регистру.

**Установщик Windows 2,0:** Параметры командной строки, указанные в этом разделе, доступны начиная с установщик Windows 3,0. [Параметры командной строки](command-line-options.md) установщик Windows доступны в установщик Windows 3,0 и более ранних версиях.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Параметр</th>
<th>Параметры</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/help</strong></td>
<td> </td>
<td>Справка и быстрый справочник. Отображает правильное использование команды установки, включая список всех параметров и поведений. Описание использования может отображаться в пользовательском интерфейсе. Неправильное использование любого параметра вызывает этот параметр справки.<br/> Пример: <strong>msiexec/Help</strong><br/>
<blockquote>
[!Note]<br />
Эквивалентный установщик Windows <a href="command-line-options.md">параметр командной строки</a> — <strong>/?</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/quiet</strong></td>
<td> </td>
<td>Тихий режим вывода. Установщик запускает установку без отображения пользовательского интерфейса. Пользователю не выводятся запросы, сообщения или диалоговые окна. Пользователь не может отменить установку. Используйте стандартные параметры командной строки <strong>/norestart</strong> или <strong>/форцерестарт</strong> для управления перезагрузками. Если параметры перезагрузки не указаны, установщик перезапускает компьютер при необходимости, не отображая пользователю никаких запросов или предупреждений.<br/> Примеры: <br/> <strong>msiexec/Package Application.msi/quiet</strong><br/> <strong>Msiexec/uninstall Application.msi/quiet</strong><br/> <strong>Msiexec/Update мсипатч. MSP/quiet</strong><br/> <strong>Msiexec/uninstall мсипатч. MSP/Package Application.msi/quiet</strong><br/>
<blockquote>
[!Note]<br />
Эквивалентный <a href="command-line-options.md">параметр командной строки</a> установщик Windows — <strong>/qn</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/passive</strong></td>
<td> </td>
<td>Параметр пассивного экрана. Установщик отображает индикатор выполнения для пользователя, который указывает, что установка выполняется, но для пользователя не отображаются запросы и сообщения об ошибках. Пользователь не может отменить установку. Используйте стандартные параметры командной строки <strong>/norestart</strong> или <strong>/форцерестарт</strong> для управления перезагрузками. Если параметр reboot не указан, установщик перезапускает компьютер при необходимости, не отображая пользователю никаких запросов или предупреждений. <br/> Пример: <strong>msiexec/package Application.msi/passive</strong> <br/>
<blockquote>
[!Note]<br />
Эквивалентный установщик Windows <a href="command-line-options.md">параметр командной строки</a> — <strong>/QB!-</strong> With <a href="rebootprompt.md"><strong>ребутпромпт</strong></a>= S Set в командной строке.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/norestart</strong></td>
<td> </td>
<td>Параметр "никогда не перезапускать". Установщик никогда не перезагружает компьютер после установки.<br/> Пример: msiexec/Package Application.msi <strong>/norestart</strong><br/>
<blockquote>
[!Note]<br />
Эквивалентная Командная строка установщик Windows в командной строке — <a href="reboot.md"><strong>Перезагрузка</strong></a>= реаллисуппресс.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/форцерестарт</strong></td>
<td> </td>
<td>Параметр всегда перезапуска. Установщик всегда перезапускает компьютер после каждой установки.<br/> Пример: msiexec/Package Application.msi <strong>/форцерестарт</strong><br/>
<blockquote>
[!Note]<br />
Эквивалентная Командная строка, соответствующая установщик Windows командной строке, имеет значение <a href="reboot.md"><strong>reboot</strong></a>= принудительно задано в командной строке.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/promptrestart</strong></td>
<td> </td>
<td>Запрос перед перезапуском параметра. Выводит сообщение о том, что для завершения установки требуется перезагрузка, и пользователю предлагается ли перезапустить систему сейчас. Этот параметр нельзя использовать вместе с параметром <strong>/quiet</strong> .<br/>
<blockquote>
[!Note]<br />
Эквивалентная Командная строка установщик Windows <a href="rebootprompt.md"><strong>ребутпромпт</strong></a>  =  &quot; &quot; задана в командной строке.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/uninstall</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Параметр удаления продукта. Удаляет продукт.<br/>
<blockquote>
[!Note]<br />
Эквивалентный установщик Windows <a href="command-line-options.md">параметр командной строки</a> — <strong>/x</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/uninstall</strong></td>
<td><em>/Package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1> [; Update2. MSP | PatchGUID2]</em></td>
<td>Удаление параметра обновления. Удаляет обновление.<br/>
<blockquote>
[!Note]<br />
Эквивалентный <a href="command-line-options.md">параметр командной строки</a> установщик Windows — <strong>/i</strong> с <a href="msipatchremove.md"><strong>мсипатчремове</strong></a>= update1. MSP | PatchGUID1[; Update2. MSP | PatchGUID2] задается в командной строке.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/log</strong></td>
<td><em><logfile></em></td>
<td>Параметр log. Записывает данные журнала в файл журнала по указанному существующему пути. Путь к расположению файла журнала должен уже существовать. Установщик не создает структуру каталогов для файла журнала.<br/> В журнал вносятся следующие сведения:<br/>
<ul>
<li>Сообщения о состоянии</li>
<li>Некритические предупреждения</li>
<li>Все сообщения об ошибках</li>
<li>Запуск действий</li>
<li>Записи, относящиеся к действию</li>
<li>Запросы пользователей</li>
<li>Начальные параметры пользовательского интерфейса</li>
<li>Сведения о нехватке памяти или аварийном завершении</li>
<li>Сообщения о нехватке места на диске</li>
<li>Свойства терминала</li>
</ul>
<blockquote>
[!Note]<br />
Эквивалентный установщик Windows <a href="command-line-options.md">параметр командной строки</a> — <strong>/l *</strong>.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Дополнительные сведения о всех методах, доступных для настройки режима ведения журнала, см. в разделе " <a href="normal-logging.md">нормальное ведение журнала</a> " раздела <a href="windows-installer-logging.md">установщик Windows Logging</a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/Package</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Установите параметр продукта. Устанавливает или настраивает продукт.<br/>
<blockquote>
[!Note]<br />
Эквивалентный <a href="command-line-options.md">параметр командной строки</a> установщик Windows — <strong>/i</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/Update</strong></td>
<td><em><Update1.msp>[; Update2. MSP]</em></td>
<td>Параметр установки исправлений. Устанавливает один или несколько исправлений. <br/>
<blockquote>
[!Note]<br />
Эквивалентная установщик Windows командной строки <a href="patch.md"><strong>Patch</strong></a> = [мсипатч. msp] <; PatchGuid2> задается в командной строке.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
