---
title: Новые возможности Windows Server 2008
description: В Windows Server 2008 появились следующие новые программные элементы для служб терминалов.
ms.assetid: a2299b03-5e06-4984-a33f-b44c7cded513
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab74f22c41fa88147a1ef30a8f55f158e34990c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104413937"
---
# <a name="whats-new-in-windows-server-2008"></a>Новые возможности Windows Server 2008

В Windows Server 2008 появились следующие новые программные элементы для служб терминалов.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Программный элемент</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Справочник по динамическим виртуальным каналам<br/></td>
<td>Динамические API виртуальных каналов (DVC) расширяют существующие API виртуальных каналов для служб терминалов, известных как статические API виртуальных каналов (SVC).<br/>
<ul>
<li><a href="dynamic-virtual-channels.md">Динамические виртуальные каналы</a></li>
<li><a href="dynamic-virtual-channels-reference.md">Справочник по динамическим виртуальным каналам</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Справочник по веб-подключение к удаленному рабочему столу<br/></td>
<td>Следующие интерфейсы (и связанные с ними методы и свойства) были добавлены в <a href="remote-desktop-web-connection-reference.md">ссылку на веб-подключение к удаленному рабочему столу</a>:<br/>
<ul>
<li><a href="imsrdpclient5.md"><strong>Интерфейс IMsRdpClient5</strong></a></li>
<li><a href="imsrdpclient6.md"><strong>Интерфейс IMsRdpClient6</strong></a></li>
<li><a href="imsrdpclientadvancedsettings5.md"><strong>Интерфейс IMsRdpClientAdvancedSettings5</strong></a></li>
<li><a href="imsrdpclientadvancedsettings6.md"><strong>Интерфейс IMsRdpClientAdvancedSettings6</strong></a></li>
<li><a href="imsrdpclientnonscriptable3.md"><strong>Интерфейс IMsRdpClientNonScriptable3</strong></a></li>
<li><a href="imsrdpclientshell.md"><strong>Интерфейс Имсрдпклиентшелл</strong></a></li>
<li><a href="imsrdpclienttransportsettings.md"><strong>Интерфейс Имсрдпклиенттранспортсеттингс</strong></a></li>
<li><a href="imsrdpclienttransportsettings2.md"><strong>Интерфейс IMsRdpClientTransportSettings2</strong></a></li>
<li><a href="imsrdpdevice.md"><strong>Интерфейс Имсрдпдевице</strong></a></li>
<li><a href="imsrdpdevicecollection.md"><strong>Интерфейс Имсрдпдевицеколлектион</strong></a></li>
<li><a href="imsrdpdrive.md"><strong>Интерфейс Имсрдпдриве</strong></a></li>
<li><a href="imsrdpdrivecollection.md"><strong>Интерфейс Имсрдпдривеколлектион</strong></a></li>
<li><a href="itsremoteprogram.md"><strong>Интерфейс Итсремотепрограм</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Справочник по API служб терминалов<br/></td>
<td>В <a href="terminal-services-api-reference.md">справочнике по API служб терминалов</a>были добавлены следующие функции:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona"><strong>Функция Втсконнектсессион</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex"><strong>Функция Втсрегистерсессионнотификатионекс</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona"><strong>Функция Втсстартремотеконтролсессион</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession"><strong>Функция Втсстопремотеконтролсессион</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex"><strong>Функция Втсунрегистерсессионнотификатионекс</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex"><strong>Функция Втсвиртуалчаннелопенекс</strong></a></li>
</ul>
Были добавлены следующие структуры:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta"><strong>Структура ВТСКЛИЕНТ</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa"><strong>Структура ВТСИНФО</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Поставщик WMI служб терминалов<br/></td>
<td>В <a href="terminal-services-wmi-provider.md">поставщик WMI служб терминалов</a>были добавлены следующие классы и методы.<br/>
<ul>
<li><a href="terminal-services-gateway-classes.md">Классы шлюза служб терминалов (и связанные методы)</a></li>
<li><a href="terminal-services-license-server-classes.md">Классы сервера лицензирования служб терминалов (и связанные методы)</a></li>
<li><a href="terminal-services-remoteapp-classes.md">Классы RemoteApp (и связанные методы)</a></li>
<li><a href="win32-tsdiscoveredlicenseserver.md"><strong>Класс Win32_TSDiscoveredLicenseServer</strong></a></li>
<li><a href="create-win32-terminal.md"><strong>Метод Create класса Win32_Terminal</strong></a></li>
<li><a href="delete-win32-terminal.md"><strong>Метод Delete класса Win32_Terminal</strong></a></li>
<li><a href="canaccesslicenseserver-win32-terminalservicesetting.md"><strong>Метод Канакцесслиценсесервер класса Win32_TerminalServiceSetting</strong></a></li>
<li><a href="findlicenseservers-win32-terminalservicesetting.md"><strong>Метод Финдлиценсесерверс класса Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getdomain-win32-terminalservicesetting.md"><strong>Метод @ Domain класса Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getgraceperioddays-win32-terminalservicesetting.md"><strong>Метод Жетграцепериоддайс класса Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getwinstationdrivernames-win32-terminalservicesetting.md"><strong>Метод Жетвинстатиондривернамес класса Win32_TerminalServiceSetting</strong></a></li>
<li><a href="pinglicenseserver-win32-terminalservicesetting.md"><strong>Метод Пинглиценсесервер класса Win32_TerminalServiceSetting</strong></a></li>
<li><a href="updatedirectconnectlicenseserver-win32-terminalservicesetting.md"><strong>Метод Упдатедиректконнектлиценсесервер класса Win32_TerminalServiceSetting</strong></a></li>
<li><a href="setuserauthenticationrequired-win32-tsgeneralsetting.md"><strong>Метод Сетусераусентикатионрекуиред класса Win32_TSGeneralSetting</strong></a></li>
<li><a href="getcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Метод Жеткуррентредиректаблеаддрессес класса Win32_TSSessionDirectory</strong></a></li>
<li><a href="setcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Метод Сеткуррентредиректаблеаддрессес класса Win32_TSSessionDirectory</strong></a></li>
<li><a href="getredirectableaddresses-win32-tssessiondirectory.md"><strong>Метод Жетредиректаблеаддрессес класса Win32_TSSessionDirectory</strong></a></li>
<li><a href="pingsessiondirectory-win32-tssessiondirectory.md"><strong>Метод Пингсессиондиректори класса Win32_TSSessionDirectory</strong></a></li>
<li><a href="setloadbalancingstate-win32-tssessiondirectory.md"><strong>Метод СетлоадбаланЦингстате класса Win32_TSSessionDirectory</strong></a></li>
<li><a href="setserverweight-win32-tssessiondirectory.md"><strong>Метод Сетсервервеигхт класса Win32_TSSessionDirectory</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Справочник по подключаемому модулю посредника сеансов служб терминалов<br/></td>
<td>Подключаемый модуль посредника сеансов служб терминалов используется для расширения возможностей посредника сеансов TS.<br/>
<ul>
<li><a href="/windows/desktop/TermServ/terminal-services-virtualization-api-reference">Справочник по подключаемому модулю посредника сеансов служб терминалов</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

