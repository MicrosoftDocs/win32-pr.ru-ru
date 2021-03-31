---
description: Сетевой DDE предоставляет функции, позволяющие удалять общую папку, получать или задавать сведения о ресурсах или перечислять общие папки.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Управление общими ресурсами DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350952"
---
# <a name="managing-dde-shares"></a>Управление общими ресурсами DDE

\[Сетевой DDE больше не поддерживается. Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]

Сетевой DDE предоставляет функции, позволяющие удалять общую папку, получать или задавать сведения о ресурсах или перечислять общие папки.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Задача</th>
<th>Процедура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Удаление общего ресурса DDE</td>
<td>Используйте функцию <a href="nddesharedel.md"><strong>нддешаредел</strong></a> .</td>
</tr>
<tr class="even">
<td>Получение сведений об общем ресурсе DDE</td>
<td>Используйте функцию <a href="nddesharegetinfo.md"><strong>нддешарежетинфо</strong></a> .</td>
</tr>
<tr class="odd">
<td>Задать сведения об общем ресурсе DDE</td>
<td>Используйте функцию <a href="nddesharesetinfo.md"><strong>нддешаресетинфо</strong></a> .</td>
</tr>
<tr class="even">
<td>Перечисление общих ресурсов DDE</td>
<td>Используйте функцию <a href="nddeshareenum.md"><strong>нддешаринум</strong></a> . Вы также можете перечислить доверенные общие ресурсы DDE с помощью функции <a href="nddetrustedshareenum.md"><strong>нддетрустедшаринум</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td>Перечисление подключенных пользователей</td>
<td>Используйте функцию <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>нетсессионенум</strong></a> .</td>
</tr>
<tr class="even">
<td>Изменение имени общего ресурса DDE</td>
<td>Удалите старую общую папку и создайте новую.
<ol>
<li>Получите сведения об общем ресурсе с помощью <a href="nddesharegetinfo.md"><strong>нддешарежетинфо</strong></a>.</li>
<li>Удалите общую папку с помощью <a href="nddesharedel.md"><strong>нддешаредел</strong></a>.</li>
<li>Измените элемент <strong>лпсзшаренаме</strong> структуры <a href="nddeshareinfo-str.md"><strong>нддешареинфо</strong></a> , возвращенной <a href="nddesharegetinfo.md"><strong>нддешарежетинфо</strong></a>.</li>
<li>Передайте измененную структуру <a href="nddeshareinfo-str.md"><strong>нддешареинфо</strong></a> в <a href="nddeshareadd.md"><strong>нддешареадд</strong></a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

