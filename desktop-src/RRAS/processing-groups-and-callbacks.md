---
title: Обработка групп и обратных вызовов
description: В следующей таблице приведена последовательность действий в рабочем взаимодействии между протоколом маршрутизации и диспетчером групп многоадресной рассылки.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2878ec15cfb663353f3dd0bc1dc5aeadbd2e1e7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339476"
---
# <a name="processing-groups-and-callbacks"></a>Обработка групп и обратных вызовов

В следующей таблице приведена последовательность действий в рабочем взаимодействии между протоколом маршрутизации и диспетчером групп многоадресной рассылки. В первом столбце описываются действия, выполняемые протоколом маршрутизации, а также ответы протокола маршрутизации к диспетчеру групп многоадресной рассылки. Во втором столбце описаны ответы диспетчера групп многоадресной рассылки по протоколу маршрутизации и действия, выполняемые диспетчером групп многоадресной рассылки, такие как обратные вызовы. В третьем столбце представлены дополнительные сведения.

Каждая строка таблицы представляет один шаг.

Задачи, перечисленные в этой таблице, не выполняются в определенном порядке. Вместо этого они происходят в зависимости от состояния членства в группах многоадресной рассылки. В таблице ниже показан пример порядка.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Действие протокола маршрутизации</th>
<th>Действие диспетчера групп многоадресной рассылки</th>
<th>Примечания</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Управление членством в группах на основе сведений о протоколе, полученных в интерфейсах, которыми владеет протокол. Управление выполняется с помощью следующих функций:
<ul>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>мгмаддграупмембершипентри</strong></a></li>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>мгмделетеграупмембершипентри</strong></a></li>
</ul></td>
<td>Добавьте и удалите из списка исходящих интерфейсов для указанных записей (s, g), (*, g) и (*, *). Этот список представляет набор интерфейсов, на которые перенаправляются данные для этой группы. Данные для этой группы находятся в указанном источнике.</td>

</tr>
<tr class="even">

<td>Отправка предупреждений в протоколы маршрутизации в форме обратных вызовов. Следующие события активируют Диспетчер групп многоадресной рассылки для вызова обратного вызова:
<ul>
<li>Объединение или выход из групп ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</li>
<li>Членство в группе изменено IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</li>
<li>Данные получены на неправильном интерфейсе ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</li>
<li>Данные, полученные из новых источников или в новую группу ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> и <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</li>
</ul></td>
<td>Используя эти обратные вызовы, Диспетчер групп многоадресной рассылки может координировать пересылку пакетов, если на маршрутизаторе есть несколько протоколов многоадресной маршрутизации.</td>
</tr>
<tr class="odd">
<td>Перечислите записи многоадресной пересылки (мфес) с помощью функций <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>мгмжетфирстмфе</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>мгмжетнекстмфе</strong></a>и <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>мгмжетмфе</strong></a> . Принимать решения о многоадресных данных на основе результатов перечисления.</td>
<td>Возврат запрошенной мфес. Возвращать ERROR_NO_MORE элементов, если больше нет возвращаемых мфес.<br/></td>
<td>Используйте функции <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>мгмжетфирстмфестатс</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>мгмжетнекстмфестатс</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>мгмжетмфестатс</strong></a> для перечисления статистики мфе. Полный пример использования этих функций см. в разделе <a href="administrative-application-scenario.md">сценарий административного приложения</a> .<br/></td>
</tr>
<tr class="even">
<td>Измените вышестоящего соседа в МФЕ с помощью функции <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>мгмсетмфе</strong></a> .</td>

<td>Клиенты используют эту функцию для изменения сведений о входящем интерфейсе.</td>
</tr>
</tbody>
</table>



 

 

