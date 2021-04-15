---
title: Сообщения DWM
description: В этом разделе содержатся сведения о диспетчер окон рабочего стола (DWM) сообщений.
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Диспетчер окон рабочего стола (DWM), справочные материалы
- DWM (диспетчер окон рабочего стола), Справочник
- Диспетчер окон рабочего стола (DWM), сообщения
- DWM (диспетчер окон рабочего стола), сообщения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "105710229"
---
# <a name="dwm-messages"></a>Сообщения DWM

В этом разделе содержатся сведения о диспетчер окон рабочего стола (DWM) сообщений.

## <a name="in-this-section"></a>В этом разделе



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a><br/></td>
<td>Информирует все окна верхнего уровня о том, что цвет цветов изменился.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a><br/></td>
<td>Информирует все окна верхнего уровня, что композиция DWM включена или отключена. <br/>
<blockquote>
[!Note]<br />
Начиная с Windows 8, композиция DWM всегда включена, поэтому это сообщение не отправляется независимо от изменения видеорежима.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a><br/></td>
<td>Посылается, когда изменилась политика отрисовки области, не являющейся клиентской.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a><br/></td>
<td>Указывает окну указать статический точечный рисунок для использования в качестве <em>динамического предварительного просмотра</em> (также известного как <em>Предварительный просмотр</em>) этого окна.<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a><br/></td>
<td>Указывает окну указать статический точечный рисунок для использования в качестве эскиза этого окна.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a><br/></td>
<td>Посылается, когда оконное окно DWM разворачивается.<br/></td>
</tr>
</tbody>
</table>



 

 

 





