---
description: Прежде чем приступить к разработке приложения служб Microsoft Windows HTTP (WinHTTP), необходимо сначала решить, следует ли использовать API C/C++ или COM-интерфейс.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Выбор интерфейса WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712127"
---
# <a name="choosing-a-winhttp-interface"></a>Выбор интерфейса WinHTTP

Прежде чем приступить к разработке приложения служб Microsoft Windows HTTP (WinHTTP), необходимо сначала решить, следует ли использовать API C/C++ или COM-интерфейс. В следующей таблице перечислены преимущества и недостатки, связанные с каждым из этих подходов.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>API C/C++</th>
<th>Интерфейс COM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Преимущества</td>
<td><ul>
<li>Ответы могут обрабатываться в виде фрагментов, что является более эффективным.</li>
<li>Операции POST также можно обрабатывать в виде фрагментов, ускоряя время обработки.</li>
<li>Поддержка автопрокси.</li>
<li>Доступ к полному набору функций WinHTTP.</li>
<li>Двоичные данные можно легко обрабатывать.</li>
</ul></td>
<td><ul>
<li>Создание приложения несложно и требует меньше строк кода, чем API C/C++.</li>
<li>Интерфейс может использоваться в языках сценариев.</li>
</ul></td>
</tr>
<tr class="even">
<td>Недостатки</td>
<td><ul>
<li>Обработка более сложная.</li>
<li>API C/C++ требует больше шагов, чем COM-интерфейс для выполнения тех же действий.</li>
<li>Настройка запроса занимает больше кода.</li>
</ul></td>
<td><ul>
<li>COM-интерфейс не предоставляет доступ к полному набору функций WinHTTP.</li>
<li>Трудно управлять двоичными типами данных на некоторых языках сценариев, таких как VBScript и JScript.</li>
<li>Интерфейс COM не поддерживает автопрокси.</li>
<li>Приложения должны использовать модель COM APARTMENT_THREADED.</li>
<li>Перед обработкой ответа необходимо сначала получить и буферизовать весь ответ.</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



