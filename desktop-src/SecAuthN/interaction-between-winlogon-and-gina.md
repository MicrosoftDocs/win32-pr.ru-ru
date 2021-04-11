---
description: Winlogon и GINA должны передавать сведения об инициализации, управлять мониторингом последовательности защиты (SAS) и уведомлениями, а также выполнять действия по выходу и завершению работы.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Взаимодействие между Winlogon и GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759d9171bca02e0a00fd35b77a4514d7438d43f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081395"
---
# <a name="interaction-between-winlogon-and-gina"></a>Взаимодействие между Winlogon и GINA 

[*Winlogon*](../secgloss/w-gly.md) и [*GINA*](../secgloss/g-gly.md) должны передавать сведения об инициализации, управлять мониторингом [*последовательности защиты*](../secgloss/s-gly.md) (SAS) и уведомлениями, а также выполнять действия по выходу и завершению работы. Состояние Winlogon определяет, какая функция GINA вызывается для обработки любого заданного события SAS. Связь происходит в порядке, показанном здесь.

> [!Note]  
> Библиотеки DLL GINA не учитываются в Windows Vista.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Событие</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Загрузка рабочей станции</td>
<td><ol>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>ВЛКСНЕГОТИАТЕ</strong></a> GINA, чтобы уведомить GINA о используемой версии Winlogon.</li>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>ВЛКСИНИТИАЛИЗЕ</strong></a> GINA, чтобы передать модели GINA адреса функций поддержки, обработчику Winlogon и получить сведения о <a href="/windows/desktop/SecGloss/c-gly"><em>контексте</em></a> для модели GINA (для использования во всех будущих вызовах модели GINA).<br/> Winlogon находится в состоянии "выход".<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>Никто не вошел в систему</td>
<td>(GINA отслеживает устройства для событий SAS).
<ol>
<li>GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>Влкссаснотифи</strong></a> Winlogon при получении события SAS.</li>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>ВЛКСЛОГЖЕДАУТСАС</strong></a> GINA, позволяя GINA обрабатывать данные идентификации пользователя и проверки подлинности.<br/> После успешного входа в систему Winlogon находится в состоянии "в системе".<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>Пользователь вошел в систему</td>
<td>(GINA отслеживает устройства для событий SAS).
<ol>
<li>GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>Влкссаснотифи</strong></a> Winlogon при получении события SAS.</li>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>ВЛКСЛОГЖЕДОНСАС</strong></a> GINA, позволяя модели GINA предоставлять параметры пользователю, который в данный момент вошел в систему.</li>
</ol></td>
</tr>
<tr class="even">
<td>Пользователь вошел в систему и хочет заблокировать компьютер</td>
<td>(GINA отслеживает устройства для событий SAS).
<ol>
<li>GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>влкссаснотифи</strong></a> .</li>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>ВЛКСЛОГЖЕДОНСАС</strong></a> GINA.</li>
<li>GINA возвращает WLX_SAS_ACTION_LOCK_WKSTA.<br/> Winlogon находится в состоянии блокировки рабочей станции.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>Пользователь вошел в систему, Рабочая станция заблокирована, и пользователь хочет разблокировать компьютер</td>
<td>(GINA отслеживает устройства для событий SAS).
<ol>
<li>GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>влкссаснотифи</strong></a> .</li>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>ВЛКСВКСТАЛОККЕДСАС</strong></a> GINA.</li>
<li>GINA возвращает WLX_SAS_ACTION_UNLOCK_WKSTA.</li>
</ol></td>
</tr>
<tr class="even">
<td>Пользователь вошел в систему, и программа вызывает функцию <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></td>
<td>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>ВЛКСЛОГОФФ</strong></a> GINA.</td>
</tr>
<tr class="odd">
<td>Пользователь вошел в систему и хочет выйти из системы с помощью SAS.</td>
<td>(GINA отслеживает устройства для событий SAS).
<ol>
<li>GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>влкссаснотифи</strong></a> .</li>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>ВЛКСЛОГЖЕДОНСАС</strong></a> GINA.</li>
<li>GINA возвращает WLX_SAS_ACTION_LOGOFF.</li>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>ВЛКСЛОГОФФ</strong></a> GINA.</li>
</ol></td>
</tr>
<tr class="even">
<td>Пользователь вошел в систему и хочет выйти из системы и завершить работу с помощью функции <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong> .</a></td>
<td><ol>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>ВЛКСЛОГОФФ</strong></a> GINA.</li>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>ВЛКСШУТДОВН</strong></a> GINA.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Пользователь вошел в систему и хочет выйти из системы и завершить работу с помощью SAS.</td>
<td>(GINA отслеживает устройства для событий SAS).
<ol>
<li>GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>влкссаснотифи</strong></a> .</li>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>ВЛКСЛОГЖЕДОНСАС</strong></a> GINA.</li>
<li>GINA возвращает WLX_SAS_ACTION_SHUTDOWN.</li>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>ВЛКСЛОГОФФ</strong></a> GINA.</li>
<li>Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>ВЛКСШУТДОВН</strong></a> GINA.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
