---
description: Запланированные задачи WMI создают и получают сведения о запланированных задачах. Другие примеры см. в разделе TechNet Скриптцентер по адресу https://www.microsoft.com/technet .
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: 'Задачи WMI: запланированные задачи'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee4fcf193296d5c474987a3a99877b3bfb43868f79527200893303df351920cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738843"
---
# <a name="wmi-tasks-scheduled-tasks"></a>Задачи WMI: запланированные задачи

Запланированные задачи WMI создают и получают сведения о запланированных задачах. Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера. Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).


В следующей процедуре описывается выполнение скрипта.

**Запуск сценария**

1.  Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*. Убедитесь, что текстовый редактор не добавляет к файлу расширение .txt.
2.  Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.
3.  Введите **cscript filename.vbs** в командной строке.
4.  Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями. Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).

> [!Note]  
> По умолчанию Cscript отображает выходные данные скрипта в окне командной строки. Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл. Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.

 

В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Часто выполняемые действия в новом интерфейсе</th>
<th>Классы или методы WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... создавать запланированные задачи с помощью сценариев?</td>
<td>Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>CREATE</strong></a> . если у вас возникли трудности при выполнении этой задачи в Windows 7 или более поздней версии, см. раздел <strong>Win32_ScheduledJob</strong> примечаний. вероятно, ваши параметры препятствуют использованию класса.<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
JobID = &quot;Test&quot;
Set objNewJob = objWMIService.Get(&quot;Win32_ScheduledJob&quot;)
errJobCreate = objNewJob.Create _
    (&quot;Notepad.exe&quot;, &quot;********143000.000000-420&quot;, True , 1 OR 4 OR 16, ,True, JobId) 
If errJobCreate = 0 Then
    WScript.Echo &quot;Job created successfully: &quot; & VBNewLine _
        & &quot;Notepad.exe scheduled to run repeately at 14.30 (2:30 P.M.) PST&quot; & VBNewLine _
        & &quot;on Mon, Wed, and Fri.&quot;
Else
    WScript.Echo &quot;Job not created. Error code = &quot; & errJobCreate
End If</code></pre></td>
</tr>
</tbody>
</table>

<p>В строке &quot; * * * * * * * * 143000.000000-420 &quot; (используется в значении параметра <em>StartTime</em> метода <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>CREATE</strong></a> ), * * * * * * * * &quot; 143000,000000 &quot; указывает, что задача начинается с 14,30 (2:30 P.M.) и &quot; -420 &quot; указывает часовой пояс. Номер часового пояса — это текущий сдвиг местного перевода времени. Смещение — это разница между временем в формате UTC и местным временем. Чтобы вычислить смещение для часового пояса, умножьте число часов, в течение которых часовой пояс составляет вперед или выше среднего времени по Гринвичу (GMT) на 60 (Используйте положительное число в часах, если часовой пояс находится впереди GMT и отрицательное число, если часовой пояс находится за GMT). Добавьте дополнительные 60 к вычислению, если часовой пояс использует летнее время. Например, тихоокеанское стандартное часовое пояса составляет восемь часов после GMT, поэтому он равен-420 (-8 * 60 + 60) при использовании летнего времени и-480 (-8 * 60), если летнее время не используется. Можно также определить значение смещения, запросив свойство смещения класса <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> .</p></td>
</tr>
<tr class="even">
<td>... возвратить список всех запланированных задач на компьютере?</td>
<td><p>Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> . Обратите внимание, что этот класс может возвращать только задания, созданные с помощью скрипта или AT.exe. Он не может возвращать сведения о заданиях, которые либо созданы или изменены мастером планирования заданий.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colScheduledJobs = objWMIService.ExecQuery (&quot;Select * from Win32_ScheduledJob&quot;)
For Each objJob in colScheduledJobs
    Wscript.Echo &quot;Command: &quot; & objJob.Command & VBNewLine _
    & &quot;Days Of Month: &quot; & objJob.DaysOfMonth & VBNewLine _
    & &quot;Days Of Week: &quot; & objJob.DaysOfWeek & VBNewLine _
    & &quot;Description: &quot; & objJob.Description & VBNewLine _
    & &quot;Elapsed Time: &quot; & objJob.ElapsedTime & VBNewLine _
    & &quot;Install Date: &quot; & objJob.InstallDate & VBNewLine _
    & &quot;Interact with Desktop: &quot; & objJob.InteractWithDesktop & VBNewLine _
    & &quot;Job ID: &quot; & objJob.JobId & VBNewLine _
    & &quot;Job Status: &quot; & objJob.JobStatus & VBNewLine _
    & &quot;Name: &quot; & objJob.Name & VBNewLine _
    & &quot;Notify: &quot; & objJob.Notify & VBNewLine _
    & &quot;Owner: &quot; & objJob.Owner & VBNewLine _
    & &quot;Priority: &quot; & objJob.Priority & VBNewLine _
    & &quot;Run Repeatedly: &quot; & objJob.RunRepeatedly & VBNewLine _
    & &quot;Start Time: &quot; & objJob.StartTime & VBNewLine _
    & &quot;Status: &quot; & objJob.Status & VBNewLine _
    & &quot;Time Submitted: &quot; & objJob.TimeSubmitted & VBNewLine _
    & &quot;Until Time: &quot; & objJob.UntilTime
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Задачи WMI для скриптов и приложений](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Примеры приложений WMI на C++](wmi-c---application-examples.md)
</dt> <dt>

[Скриптцентер TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

