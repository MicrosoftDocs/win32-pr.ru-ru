---
description: Объекты потоковой передачи мультимедиа
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Объекты потоковой передачи мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05762e4a3d7aa486b8a22b73905fc5d9c1610078
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351685"
---
# <a name="multimedia-streaming-objects"></a>Объекты потоковой передачи мультимедиа

> [!Note]  
> Это нерекомендуемый API. Новые приложения не должны использовать его.

 

В следующей таблице описаны объекты потоковой передачи мультимедиа.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>CLSID</th>
<th>Описание</th>
<th>Поддерживаемые интерфейсы</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CLSID_AMMediaTypeStream</td>
<td>Может создавать примеры носителей для любого типа данных, поддерживаемого DirectShow</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>иаммедиастреам</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>имедиастреам</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>CLSID_AMAudioData</td>
<td>Реализация объекта <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>иаудиодата</strong></a> Audio Container.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>иаудиодата</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>CLSID_AMDirectDrawStream</td>
<td>Поток мультимедиа DirectDraw, который можно добавить в поток мультимедиа DirectShow.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>иаммедиастреам</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>имедиастреам</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>идиректдравмедиастреам</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>CLSID_AMMultiMediaStream</td>
<td>Реализация DirectShow потока мультимедиа.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>иаммултимедиастреам</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>имултимедиастреам</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>CLSID_MediaStreamFilter</td>
<td>Предоставляет функции потоковой передачи мультимедиа для объекта CLSID_AMMultiMediaStream через интерфейс <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>иаммултимедиастреам</strong></a> .</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Н/Д</td>
<td>Примеры, созданные объектом CLSID_AMMediaTypeStream.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>истреамсампле</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>имедиасампле</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Н/Д</td>
<td>Примеры, созданные потоком DirectDraw.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>истреамсампле</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>идиректдравстреамсампле</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>имедиасампле</strong></a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



