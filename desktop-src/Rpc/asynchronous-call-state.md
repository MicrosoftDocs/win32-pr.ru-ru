---
title: Асинхронное состояние вызова
description: На этой странице описывается асинхронное состояние вызова для вызовов RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889207"
---
# <a name="asynchronous-call-state"></a>Асинхронное состояние вызова

На этой странице описывается асинхронное состояние вызова для вызовов RPC.

## <a name="client-behavior"></a>Поведение клиента



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Состояние</th>
<th>Имя состояния</th>
<th>Действие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Сделать вызов</td>
<td>Создание RPC
<ul>
<li>При успешном завершении переходит в состояние Вкомп</li>
<li>При возникновении исключения перейдите в конец</li>
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
<td>Ожидается получение уведомления Нотификатионкалл-Complete<br/> К Comp<br/></td>
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



 

## <a name="server-behavior"></a>Поведение сервера



| Состояние | Имя состояния     | Действие                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | Вызов отправляется RPC Рунтимепроцесс<br/> К Comp<br/> Неустранимая ошибка (при выполнении в потоке RPC): вызов исключения; к концу<br/> Для корректного сбоя: перейдите на<br/> |
| Объект     | Прервать вызов | Вызов [**рпкасинкаборткалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)к концу<br/>                                                                                                                                             |
| Соответствовал  | Completion     | Выдача [**рпкасинккомплетекалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)к концу<br/>                                                                                                                                      |
| Конец   |                |                                                                                                                                                                                                                     |



 

 

 





