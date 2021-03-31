---
title: Состояние асинхронного канала
description: На этой странице описывается асинхронное состояние канала для вызовов RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069577"
---
# <a name="asynchronous-pipe-state"></a>Состояние асинхронного канала

На этой странице описывается асинхронное состояние канала для вызовов RPC.

## <a name="in-pipe"></a>В канале

Поведение клиента

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Состояние</th>
<th>State Name</th>
<th>Действие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Сделать вызов</td>
<td>Создание RPC
<ul>
<li>При успешном завершении переходит в состояние WS</li>
<li>При возникновении исключения перейдите в конец</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="even">
<td>С</td>
<td>push</td>
<td>Выполнить принудительную отправку
<ul>
<li>При сбое переходит в конец</li>
<li>При успешном переходе в WS</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Ожидание отправки</td>
<td>Ожидание уведомления
<ul>
<li>При сбое получения уведомления может</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и требуется отправить дополнительные данные, перейдите на страницу P</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и больше не нужно отправлять данные, перейдите на страницу NP</li>
<li>Если сообщение о сбое <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпккаллкомплете</strong></a> получено Go</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push-уведомления null</td>
<td>Отправить 0 байт (Push-уведомления null)
<ul>
<li>При сбое переходит в конец</li>
<li>При успешном завершении переходит в Вкомп</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="odd">
<td>Можно</td>
<td>Отменить вызов</td>
<td>Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>рпкасинкканцелкалл</strong></a>Go to вкомп<br/></td>
</tr>
<tr class="even">
<td>вкомп</td>
<td>Ожидание завершения</td>
<td>Должно быть получено уведомление о Нотификатионкалл-завершении.<br/> К Comp<br/></td>
</tr>
<tr class="odd">
<td>Соответствовал</td>
<td>Completion</td>
<td>Выдача <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>к концу<br/></td>
</tr>
<tr class="even">
<td>Конец</td>


</tr>
</tbody>
</table>



 

Поведение сервера

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Состояние</th>
<th>State Name</th>
<th>Действие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>Вызов отправляется средой выполнения RPC к P<br/> Неустранимая ошибка (при выполнении в потоке RPC): вызов исключения; к концу<br/> Для корректного сбоя: перейдите на<br/></td>
</tr>
<tr class="even">
<td>С</td>
<td>По запросу</td>
<td>Сделать запрос на вытягивание
<ul>
<li>При сбое переходит в конец</li>
<li>При успешном выполнении и синхронном завершении с чтением ненулевых байтов перейдите к P</li>
<li>При успешном выполнении и синхронном завершении с нулевым количеством считанных байтов (по запросу null) переход к Comp</li>
<li>При успешном выполнении и асинхронном завершении (возвращается ERROR_IO_PENDING) перейдите к WP.</li>
</ul>
Сбой: перейдите на<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Ожидание запроса на вытягивание</td>
<td>Ожидание уведомления
<ul>
<li>При сбое для получения завершения перейдите к</li>
<li>Если <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> сбоя получен, перейдите к</li>
<li>Если получено <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> об успешном выполнении с чтением ненулевых байтов, перейдите к P</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> с нулевым количеством считанных байтов (по запросу null), перейдите в раздел "Comp"</li>
<li>При получении ошибки перейдите к</li>
</ul>
Сбой: перейдите на<br/></td>
</tr>
<tr class="even">
<td>Объект</td>
<td>Прервать вызов</td>
<td>Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>рпкасинкаборткалл</strong></a>к концу<br/></td>
</tr>
<tr class="odd">
<td>Соответствовал</td>
<td>Completion</td>
<td>Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>к концу<br/></td>
</tr>
<tr class="even">
<td>Конец</td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a>ВЫХОДНОЙ канал

Поведение клиента

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Состояние</th>
<th>State Name</th>
<th>Действие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Сделать вызов</td>
<td>Создание RPC
<ul>
<li>При успешном переходе на P</li>
<li>При сбое перейдите в раздел Comp</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="even">
<td>С</td>
<td>По запросу</td>
<td>Сделать запрос на вытягивание
<ul>
<li>При сбое переходит в конец</li>
<li>При успешном выполнении и синхронном завершении с чтением ненулевых байтов перейдите к P</li>
<li>При успешном выполнении и синхронном завершении с нулевым количеством считанных байтов (по запросу null) перейдите в Вкомп.</li>
<li>При успешном выполнении и асинхронном завершении (возвращается ERROR_IO_PENDING) перейдите к WP.</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Ожидание запроса на вытягивание</td>
<td>Ожидание уведомления
<ul>
<li>При неудачном завершении переходит к CAN</li>
<li>Если <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> сбоя получен, переходит к CAN</li>
<li>Если получено <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> об успешном выполнении с чтением ненулевых байтов, перейдите к P</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> с нулевым количеством считанных байтов (по запросу null), перейдите в раздел "Comp"</li>
<li>Если ошибка получена, можно</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="even">
<td>Можно</td>
<td>Отменить вызов</td>
<td>Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>рпкасинкканцелкалл</strong></a>Go to вкомп<br/></td>
</tr>
<tr class="odd">
<td>вкомп</td>
<td>Ожидание завершения</td>
<td>Ожидание уведомления. Должно быть получено уведомление о завершении вызова.<br/> К Comp<br/></td>
</tr>
<tr class="even">
<td>Соответствовал</td>
<td>Completion</td>
<td>Выдача <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>к концу<br/></td>
</tr>
<tr class="odd">
<td>Конец</td>


</tr>
</tbody>
</table>



 

Поведение сервера

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Состояние</th>
<th>State Name</th>
<th>Действие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>Вызов отправляется средой выполнения RPC к P<br/> Неустранимая ошибка (при выполнении в потоке RPC): вызов исключения; к концу<br/> Для корректного сбоя: перейдите на<br/></td>
</tr>
<tr class="even">
<td>С</td>
<td>push</td>
<td>Выполнить принудительную отправку
<ul>
<li>При успешном переходе в WP</li>
<li>При сбое переходит в конец</li>
</ul>
Сбой: перейдите на<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Ожидание принудительной отправки</td>
<td>Ожидание уведомления
<ul>
<li>При сбое для получения завершения перейдите к</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и требуется отправить дополнительные данные, перейдите на страницу P</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и больше не нужно отправлять данные, перейдите на страницу NP</li>
<li>Если ошибка получена, переходите к следующему.</li>
</ul>
Сбой: перейдите на<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push-уведомления null</td>
<td>Отправить 0 байт
<ul>
<li>При успешном переходе на WNP</li>
<li>при сбое перейдите в раздел Comp</li>
</ul>
Сбой: перейдите на<br/></td>
</tr>
<tr class="odd">
<td>WNP</td>
<td>Ожидание принудительной отправки null</td>
<td>Ожидание уведомления
<ul>
<li>При сбое для получения завершения перейдите к</li>
<li>Если ошибка получена, переходите к следующему.</li>
<li>Если получено сообщение об успешном выполнении Go</li>
</ul></td>
</tr>
<tr class="even">
<td>Объект</td>
<td>Прервать вызов</td>
<td>Вызовите <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>рпкасинкаборткалл</strong></a>; к концу</td>
</tr>
<tr class="odd">
<td>Соответствовал</td>
<td>Completion</td>
<td>Ошибка <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>; к концу</td>
</tr>
<tr class="even">
<td>Конец</td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a>Исходящий канал

Поведение клиента

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Состояние</th>
<th>State Name</th>
<th>Действие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Сделать вызов</td>
<td>Создание RPC
<ul>
<li>При успешном переходе в WS</li>
<li>При возникновении исключения перейдите в конец</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>push</td>
<td>Выполнить принудительную отправку
<ul>
<li>При сбое переходит в конец</li>
<li>При успешном переходе в WS</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Ожидание отправки</td>
<td>Ожидание уведомления
<ul>
<li>При сбое получения уведомления может</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и требуется отправить дополнительные данные, перейдите в PS</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и больше не нужно отправлять данные, перейдите на страницу NP</li>
<li>Если сообщение о сбое <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпккаллкомплете</strong></a> получено Go</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push-уведомления null</td>
<td>Отправить 0 байт (Push-уведомления null)
<ul>
<li>При сбое переходит в конец</li>
<li>При успешном переходе на PL</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="odd">
<td>PL</td>
<td>По запросу</td>
<td>Сделать запрос на вытягивание
<ul>
<li>При сбое переходит в конец</li>
<li>При успешном выполнении и синхронном завершении с ненулевыми байтами чтение переходит к PL</li>
<li>При успешном выполнении и синхронном завершении с нулевым количеством считанных байтов (по запросу null) перейдите в Вкомп.</li>
<li>При успешном выполнении и асинхронном завершении (возвращается ERROR_IO_PENDING) перейдите к WPL.</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="even">
<td>WPL</td>
<td>Ожидание запроса на вытягивание</td>
<td>Ожидание уведомления
<ul>
<li>При неудачном завершении переходит к CAN</li>
<li>Если <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> сбоя получен, переходит к CAN</li>
<li>Если получено <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> об успешном выполнении с чтением ненулевых байтов, перейдите к PL</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> с нулевым количеством байтов, перейдите к Comp</li>
<li>Если ошибка получена, можно</li>
</ul>
Сбой: перейдите на страницу Can<br/></td>
</tr>
<tr class="odd">
<td>Можно</td>
<td>Отменить вызов</td>
<td>Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>рпкасинкканцелкалл</strong></a>Go to вкомп<br/></td>
</tr>
<tr class="even">
<td>вкомп</td>
<td>Ожидание завершения</td>
<td>Ожидание уведомления. Должно быть получено уведомление Каллкомплете.<br/> К Comp<br/></td>
</tr>
<tr class="odd">
<td>Соответствовал</td>
<td>Completion</td>
<td>Выдача <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>к концу<br/></td>
</tr>
<tr class="even">
<td>Конец</td>


</tr>
</tbody>
</table>



 

Поведение сервера

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Состояние</th>
<th>State Name</th>
<th>Действие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>Вызов отправляется с помощью RPC Рунтимего в PL.<br/> Неустранимая ошибка (при выполнении в потоке RPC): вызов исключения; к концу<br/> Для корректного сбоя: перейдите на<br/></td>
</tr>
<tr class="even">
<td>PL</td>
<td>По запросу</td>
<td>Сделать запрос на вытягивание
<ul>
<li>При сбое переходит в конец</li>
<li>При успешном выполнении и синхронном завершении с ненулевыми байтами чтение переходит к PL</li>
<li>При успешном выполнении и синхронном завершении с нулевым количеством прочитанных байтов (по запросу null) переход к PS</li>
<li>При успешном выполнении и асинхронном завершении (возвращается ERROR_IO_PENDING) перейдите к WPL.</li>
</ul>
Сбой: перейдите на<br/></td>
</tr>
<tr class="odd">
<td>WPL</td>
<td>Ожидание запроса на вытягивание</td>
<td>Ожидание уведомления
<ul>
<li>При сбое для получения завершения перейдите к</li>
<li>Если <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> сбоя получен, перейдите к</li>
<li>Если получено <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> об успешном выполнении с чтением ненулевых байтов, перейдите к PL</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпкрецеивекомплете</strong></a> с нулевым числом байтов Read, перейдите к PS</li>
<li>Если ошибка получена, перейдите к</li>
</ul>
Сбой: перейдите на<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>push</td>
<td>Выполнить принудительную отправку
<ul>
<li>При успешном переходе в WPS</li>
<li>При сбое переходит в конец</li>
</ul>
Сбой: перейдите на<br/></td>
</tr>
<tr class="odd">
<td>Информационный</td>
<td>Ожидание принудительной отправки</td>
<td>Ожидание уведомления
<ul>
<li>При сбое для получения завершения перейдите к</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и требуется отправить дополнительные данные, перейдите в PS</li>
<li>Если получено сообщение об успешном <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>рпксендкомплетее</strong></a> и больше не нужно отправлять данные, перейдите на страницу NP</li>
<li>Если ошибка получена, переходите к следующему.</li>
</ul>
Сбой: перейдите на<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push-уведомления null</td>
<td>Отправить 0 байт
<ul>
<li>При успешном переходе на WNP</li>
<li>при сбое перейдите в раздел Comp</li>
</ul>
Сбой: перейдите на<br/></td>
</tr>
<tr class="odd">
<td>WNP</td>
<td>Ожидание принудительной отправки null</td>
<td>Ожидание уведомления
<ul>
<li>При сбое для получения завершения перейдите к</li>
<li>Если ошибка получена, переходите к следующему.</li>
<li>Если получено сообщение об успешном выполнении Go</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Объект</td>
<td>Прервать вызов</td>
<td>Вызовите <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>рпкасинкаборткалл</strong></a>; к концу</td>
</tr>
<tr class="odd">
<td>Соответствовал</td>
<td>Completion</td>
<td>Ошибка <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>; к концу</td>
</tr>
<tr class="even">
<td>Конец</td>


</tr>
</tbody>
</table>



 

 

 





