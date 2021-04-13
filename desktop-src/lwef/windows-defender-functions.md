---
title: Функции защитника Windows
description: Функции, вызываемые приложениями для запроса проверок, обновлений сигнатур или сведений из защитника Windows.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412433"
---
# <a name="windows-defender-functions"></a>Функции защитника Windows

Функции, вызываемые приложениями для запроса проверок, обновлений сигнатур или сведений из защитника Windows.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mperrormessageformat.md"><strong>мперрормессажеформат</strong></a></td>
<td>Возвращает отформатированное сообщение об ошибке на основе кода ошибки.<br/></td>
</tr>
<tr class="even">
<td><a href="mpfreememory.md"><strong>мпфримемори</strong></a></td>
<td>Освобождает память для диспетчера защиты от вредоносных программ.<br/></td>
</tr>
<tr class="odd">
<td><a href="mphandleclose.md"><strong>мфандлеклосе</strong></a></td>
<td>Закрывает маркер, возвращенный <a href="mpmanageropen.md"><strong>мпманажеропен</strong></a>, <a href="mpscanstart.md"><strong>мпсканстарт</strong></a>, <a href="mpthreatopen.md"><strong>мпсреатопен</strong></a>или <a href="mpupdatestart.md"><strong>мпупдатестарт</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanageropen.md"><strong>мпманажеропен</strong></a></td>
<td>Устанавливает подключение к диспетчеру защиты от вредоносных программ на локальном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerstatusquery.md"><strong>мпманажерстатускуери</strong></a></td>
<td><strong>Не поддерживается.</strong> Возвращает сведения о состоянии различных компонентов диспетчера защиты от вредоносных программ.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanagerstatusqueryex.md"><strong>мпманажерстатускуерекс</strong></a></td>
<td>Возвращает сведения о состоянии различных компонентов диспетчера защиты от вредоносных программ.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerversionquery.md"><strong>мпманажерверсионкуери</strong></a></td>
<td>Возвращает сведения о версии различных компонентов диспетчера защиты от вредоносных программ.<br/></td>
</tr>
<tr class="even">
<td><a href="mpscancontrol.md"><strong>мпсканконтрол</strong></a></td>
<td>Разрешает Управление сканированием, которое было асинхронно инициировано через <a href="mpscanstart.md"><strong>мпсканстарт</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpscanstart.md"><strong>мпсканстарт</strong></a></td>
<td>Запускает операцию сканирования.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatenumerate.md"><strong>мпсреатенумерате</strong></a></td>
<td>Возвращает сведения о следующей угрозе в списке перечисления. Эту функцию можно вызывать повторно до тех пор, пока не завершится перечисление всех угроз.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpthreatopen.md"><strong>мпсреатопен</strong></a></td>
<td>Возвращает маркер перечисления, предназначенный для получения угроз. Эта функция может использоваться для открытия угроз, обнаруженных конкретным сканированием, всех активных угроз в системе, истории заражения угроз или всех угроз, имеющихся в базе данных сигнатур.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatquery.md"><strong>мпсреаткуери</strong></a></td>
<td>Используется для запроса статических (таких как серьезность и категория) или локализованных сведений о конкретной угрозе (например, описание категории и рекомендации).<br/></td>
</tr>
<tr class="odd">
<td><a href="mpupdatecontrol.md"><strong>мпупдатеконтрол</strong></a></td>
<td>Позволяет управлять операцией обновления сигнатур, которая была асинхронно инициирована через <a href="mpupdatestart.md"><strong>мпупдатестарт</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mpupdatestart.md"><strong>мпупдатестарт</strong></a></td>
<td>Запускает операцию обновления сигнатур.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>вденабле</strong></a></td>
<td>Изменяет состояние защитника Windows на вкл. или выключено.<br/>
<blockquote>
[!Note]<br />
Начиная с Windows 10, версии 1607 и Windows Server 2016 функция <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>вденабле</strong></a> всегда возвращает <strong>E_NOTIMPL</strong>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>вдстатус</strong></a></td>
<td>Возвращает текущее состояние защитника Windows.<br/></td>
</tr>
</tbody>
</table>



 

 

 





