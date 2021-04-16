---
description: Функции для установки и получения дескриптора безопасности объектов.
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: 'Функции дескрипторов безопасности низкого уровня '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72406dc2481e4671d8d535327f416a2d003c3a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664658"
---
# <a name="low-level-security-descriptor-functions"></a>Функции дескрипторов безопасности низкого уровня 

Существует несколько пар низкоуровневых функций для установки и извлечения [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly)объекта. Каждая из этих пар работает только с ограниченным набором объектов Windows. Например, одна пара работает с объектами File, а другая работает с разделами реестра. В следующей таблице показаны низкоуровневые функции для использования с различными типами защищаемых объектов.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип объекта</th>
<th>Низкоуровневые функции</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Файлы</a></li>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Каталоги</a></li>
<li>маилслотс</li>
<li><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Именованные каналы</a></li>
</ul></td>
<td>Используйте функции <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>жетфилесекурити</strong></a> и <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>сетфилесекурити</strong></a> . Эти функции используют символьные строки для обнаружения защищаемого объекта вместо использования дескрипторов.</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Процессы</a></li>
<li><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Потоки</a></li>
<li><a href="access-rights-for-access-token-objects.md">Маркеры доступа в Azure Active Directory</a></li>
<li><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Объекты сопоставления файлов</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Семафоры</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">События</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Мьютексы</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Ожидающие таймеры</a></li>
</ul></td>
<td>Используйте функции <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>жеткернелобжектсекурити</strong></a> и <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>сеткернелобжектсекурити</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Оконные станции</a></li>
<li><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Настольные системы</a></li>
</ul></td>
<td>Используйте функции <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>жетусеробжектсекурити</strong></a> и <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>сетусеробжектсекурити</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Разделы реестра</a></li>
</ul></td>
<td>Используйте функции <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>регжеткэйсекурити</strong></a> и <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>регсеткэйсекурити</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/Services/service-security-and-access-rights">Объекты службы Windows</a></li>
</ul></td>
<td>Используйте функции <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>куерисервицеобжектсекурити</strong></a> и <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>сетсервицеобжектсекурити</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li>Объекты принтера</li>
</ul></td>
<td>Используйте структуру <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> с функциями <a href="/windows/desktop/printdocs/getprinter"><strong>PrintOut</strong></a> и <a href="/windows/desktop/printdocs/setprinter"><strong>сетпринтер</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Общие сетевые папки</a></li>
</ul></td>
<td>Используйте уровень 502 с функциями <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>нетшарежетинфо</strong></a> и <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>нетшаресетинфо</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="acl-based-access-control.md">Закрытые объекты (объекты являются частными для создания приложения)</a></li>
</ul></td>
<td>Используйте функции <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>креатеприватеобжектсекурити</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>дестройприватеобжектсекурити</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>жетприватеобжектсекурити</strong></a> и <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> .</td>
</tr>
</tbody>
</table>



 

 

 
