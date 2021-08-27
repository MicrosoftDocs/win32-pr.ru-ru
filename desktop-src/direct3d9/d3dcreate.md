---
description: См. сочетание одного или нескольких флагов, управляющих поведением при создании устройства в константе D3DCREATE.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09cfd220e3fae2af079ba4eceba8f820a9267b4d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630232"
---
# <a name="d3dcreate"></a>D3DCREATE

Сочетание одного или нескольких флагов, управляющих поведением при создании устройства.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#определенно</td>
<td>Описание:</td>
</tr>
<tr class="even">
<td>D3DCREATE_ADAPTERGROUP_DEVICE</td>
<td>Приложение запрашивает у устройства все головки, которыми владеет этот главный адаптер. Недопустимый флаг для неосновных адаптеров. Если этот флаг установлен, параметры представления, передаваемые в <a href="/windows/desktop/api"><strong>креатедевице</strong></a> , должны указывать на массив <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>. Число элементов в <strong>D3DPRESENT_PARAMETERS</strong> должно равняться количеству адаптеров, определенных элементом Нумберофадаптерсинграуп структуры <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> . Среда выполнения DirectX присвоит каждому элементу каждый заголовок в числовом порядке, указанном элементом Адаптерординалинграуп <strong>D3DCAPS9</strong>.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT</td>
<td>Direct3D будет управлять ресурсами вместо драйвера. Вызовы Direct3D не завершатся ошибкой ресурсов, например нехваткой видеопамяти.</td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</td>
<td>Как и D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D будет управлять ресурсами, а не драйвером. В отличие от D3DCREATE_DISABLE_DRIVER_MANAGEMENT D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX будет возвращать ошибки для таких условий, как нехватка видеопамяти.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_PRINTSCREEN</td>
<td>Приводит к тому, что среда выполнения не регистрирует горячие клавиши для принтскрин, Ctrl-Printscreen и Alt-Printscreen для захвата содержимого рабочего стола или окна. 
<table>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 9Ex:<br/> Этот флаг доступен только в Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_PSGP_THREADING</td>
<td>Ограничьте вычисления до основного потока приложения. Если флаг не установлен, среда выполнения может выполнять обработку вершин программного обеспечения и другие вычисления в рабочем потоке для повышения производительности многопроцессорных систем. 
<table>
<tbody>
<tr class="odd">
<td>различия между Windows XP и Windows Vista:<br/> этот флаг доступен в Windows Vista, Windows Server 2008 и Windows 7.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DCREATE_ENABLE_PRESENTSTATS</td>
<td>Включает сбор данных о текущей статистике на устройстве. Вызовы <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>жетпресентстатистикс</strong></a> будут возвращать допустимые данные. 
<table>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 9Ex:<br/> Этот флаг доступен только в Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_FPU_PRESERVE</td>
<td>Задайте точность вычислений Direct3D с плавающей запятой до точности, используемой вызывающим потоком. Если этот флаг не указан, Direct3D по умолчанию принимает значение Single-to-ближайшего режима, по двум причинам:
<ul>
<li>Режим двойной точности снизит производительность Direct3D.</li>
<li>Части Direct3D предполагают, что исключения модуля с плавающей запятой имеют маску. снятие маски этих исключений может привести к неопределенному поведению.</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCREATE_HARDWARE_VERTEXPROCESSING</td>
<td>Указывает аппаратную обработку вершин.</td>
</tr>
<tr class="even">
<td>D3DCREATE_MIXED_VERTEXPROCESSING</td>
<td>Задает смешанную обработку вершин (как программного, так и аппаратного обеспечения). для Windows 10 версии 1607 и более поздней использовать этот параметр не рекомендуется. См. D3DCREATE_SOFTWARE_VERTEXPROCESSING.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SOFTWARE_VERTEXPROCESSING</td>
<td>Указывает процесс обработки вершин программного обеспечения. для Windows 10 версии 1607 и более поздней использовать этот параметр не рекомендуется. Используйте D3DCREATE_HARDWARE_VERTEXPROCESSING.
<div class="alert">
<blockquote>
[!Note]<br />
если аппаратная обработка вершин недоступна, использование обработки вершин программного обеспечения не рекомендуется в Windows 10, версии 1607 (и более поздних версиях), так как эффективность обработки вершин программного обеспечения была значительно снижена при повышении безопасности реализации.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_MULTITHREADED</td>
<td>Указывает, что приложение запрашивает безпотоковую безопасность Direct3D. Таким образом, поток Direct3D становится более часто становиться владельцем своей глобальной <a href="/windows/desktop/Sync/critical-section-objects">критической секции</a> , что может привести к снижению производительности. Если приложение обрабатывает сообщения окна в одном потоке, одновременно делая вызовы API Direct3D в другой, приложение должно использовать этот флаг при создании устройства. Это окно также необходимо уничтожить перед выгрузкой d3d9.dll.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_NOWINDOWCHANGES</td>
<td>Указывает, что Direct3D не должен изменять фокус окна каким бы ни было образом.
<div class="alert">
<blockquote>
[!Note]<br />
Если этот флаг установлен, приложение должно полностью поддерживать все события управления фокусом, такие как события ALT + TAB и щелчок мыши.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_PUREDEVICE</td>
<td>Указывает, что Direct3D не поддерживает вызовы Get * для любых данных, которые могут храниться в блоках состояния. Он также указывает Direct3D не предоставлять какие бы то ни было службы эмуляции для обработки вершин. Это означает, что если устройство не поддерживает обработку вершин, то приложение может использовать только после преобразования вершин.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SCREENSAVER</td>
<td>Разрешает экранные заставки во время полноэкранного приложения. Без этого флага Direct3D отключает заставки в течение всего времени, пока вызывающее приложение находится в полноэкранном режиме. Если вызывающее приложение уже является экранной заставкой, этот флаг не действует. 
<table>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 9Ex:<br/> Этот флаг доступен только в Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

D3DCREATE \_ оборудование \_ ВЕРТЕКСПРОЦЕССИНГ, D3DCREATE \_ Mixed \_ вертекспроцессинг и D3DCREATE \_ Software вертекспроцессинг являются взаимоисключающими \_ флагами. При вызове [**креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)необходимо указать хотя бы один из этих флагов обработки вершин.

## <a name="constant-information"></a>Сведения о константе



| Требование                         |  Значение          |
|--------------------------|------------|
| Заголовок                   | D3D9. h     |
| Минимальная операционная система | Windows 98 |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Константы Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
