---
description: Для получения данных из инструментария WMI (на локальном или удаленном компьютере) необходимо подключиться к службе WMI, подключившись к определенному пространству имен.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: Задачи WMI. подключение к службе WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da816b45709f6140efb7e6e0460e27d9f9ed00f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627720"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a>Задачи WMI. подключение к службе WMI

Для получения данных из инструментария WMI (на локальном или удаленном компьютере) необходимо подключиться к службе WMI, подключившись к определенному [*пространству имен*](gloss-n.md). В большинстве случаев используйте сокращенное подключение [моникера](creating-a-wmi-script.md) или подключение [**локатора**](swbemlocator-connectserver.md) . Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

для удаленных подключений требуются соответствующие параметры брандмауэра Windows и DCOM. дополнительные сведения см. в статьях [подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md) и [подключение через брандмауэр Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista). начиная с Windows Vista управление учетными записями пользователей (UAC) может повлиять на доступ к WMI. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](user-account-control-and-wmi.md).

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
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Часто выполняемые действия в новом интерфейсе</th>
<th>Классы или методы WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... подключиться к удаленному компьютеру с помощью инструментария WMI?</td>
<td>Укажите один из следующих элементов в строке подключения <a href="constructing-a-moniker-string.md">моникера</a> :<br/>
<ul>
<li>Имя компьютера NetBIOS, например &quot; ATL-DC-01&quot;</li>
<li>Полное доменное имя, например &quot; ATL-DC-01.fabrikam.com&quot;</li>
<li>IPv4-адрес, например &quot; 192.168.1.1&quot;</li>
<li>начиная с Windows Vista, можно указать ipv6-адрес, если целевой компьютер и компьютер, с которого устанавливается подключение, используют ipv6.<br/></li>
</ul>
Дополнительные сведения см. в разделе <a href="connecting-to-wmi-on-a-remote-computer.md">Подключение к WMI на удаленном компьютере</a> и <a href="ipv6-and-ipv4-support-in-wmi.md">Поддержка IPv6 и IPv4 в WMI</a>.<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... запустить сценарий WMI в разделе "альтернативные учетные данные"?</td>
<td><p>Используйте метод <a href="swbemlocator-connectserver.md"><strong>SWbemLocator. коннектсервер</strong></a> или <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>Ивбемлокатор:: коннектсервер</strong></a> в C++ и укажите соответствующие имя пользователя и пароль. При подключении к локальному компьютеру изменить учетные данные нельзя. Дополнительные сведения см. в статьях <a href="creating-a-wmi-script.md">Создание сценария WMI</a> и <a href="connecting-to-wmi-on-a-remote-computer.md">Подключение к WMI на удаленном компьютере</a>.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
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

 

 



`
