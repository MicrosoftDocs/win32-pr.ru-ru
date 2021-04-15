---
description: Ряд фактоидс описывают входные данные, которые являются общими для всех распознавателей языков и не должны иметь различных форматов для разных языков. В следующей таблице перечислены фактоидс, общие для всех языков.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Фактоидс, общие для разных языков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701611"
---
# <a name="factoids-common-across-languages"></a>Фактоидс, общие для разных языков

Ряд фактоидс описывают входные данные, которые являются общими для всех распознавателей языков и не должны иметь различных форматов для разных языков. В следующей таблице перечислены фактоидс, общие для всех языков.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>фактоид</th>
<th>Определение</th>
<th>Примеры</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Число</strong></td>
<td>Задает сдвиг для одной цифры. Распознаватель перемещается в сторону возврата только отдельных цифр, если задано значение фактоид.<br/></td>
<td>0-9<br/></td>
</tr>
<tr class="even">
<td><strong>Электронная почта</strong></td>
<td>Задает смещение адреса электронной почты.<br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><strong>Web</strong></td>
<td>Задает смещение для различных форматов URL-адресов.<br/>
<blockquote>
[!Note]<br />
Параметры по умолчанию для распознавателя включают в себя <strong>веб-</strong> фактоид. По этой причине вы не можете заметить значительную разницу между <strong>веб-</strong> фактоид и параметром по умолчанию. Однако <strong>веб-</strong> фактоид помогает избежать пробелов между словами в URL-адресе.
</blockquote>
<br/></td>
<td>http: \\ Microsoft.NET<br/> https://microsoft.us/<br/> HTTPS: \\ www.Microsoft.au \<br/> https://microsoft.com<br/> www.microsoft_world. com<br/> www.microsoft.us \<br/> http: \\www.microsoft.com\myfile.htm<br/> http: \\www.microsoft.com\myfile.html<br/> http: \\ www. Microsoft. ком\мифиле.АСП<br/> http: \\ www.Microsoft.UK<br/> http: \\ www.Microsoft.info<br/> www.microsoft.biz<br/></td>
</tr>
<tr class="even">
<td><strong>По умолчанию</strong></td>
<td>Возвращает распознаватель в параметры по умолчанию.<br/></td>
<td>Значение по умолчанию для фактоидс для западных языков включает системный словарь, Пользовательский словарь, различные знаки препинания, а также <strong>веб-</strong> Фактоидс и <strong>Number</strong> .<br/> Значение по умолчанию для фактоидс для восточно-азиатских языков включает все символы, поддерживаемые распознавателем.<br/></td>
</tr>
<tr class="odd">
<td><strong>Нет</strong></td>
<td>Отключает все фактоидс, словари и языковую модель.<br/></td>
<td>Этот фактоид следует использовать, только если вы не хотите, чтобы распознаватель использовал грамматические правила или словари, включая системный словарь. Этот фактоид полезен для ввода случайных строк, таких как коды продуктов. Не используйте флаг приведение к этому фактоид.<br/></td>
</tr>
</tbody>
</table>



 

 

 




