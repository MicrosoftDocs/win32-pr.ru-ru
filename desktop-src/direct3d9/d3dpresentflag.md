---
description: Константы, используемые \_ параметрами D3DPRESENT.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebf3a8ad3a22f5104e4d4a78d3a01a29d07d757
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624560"
---
# <a name="d3dpresentflag"></a>D3DPRESENTFLAG

Константы, [**используемые \_ параметрами D3DPRESENT**](d3dpresent-parameters.md).



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#определенно</td>
<td>Значение</td>
<td>Описание:</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_DEVICECLIP</td>
<td>0x00000004</td>
<td>Обрезает оконный <a href="/windows/desktop/api"><strong>Блит в</strong></a> клиентскую область окна в области экрана монитора видеоадаптера, создавшего устройство Direct3D. D3DPRESENTFLAG_DEVICECLIP не является допустимым для D3DSWAPEFFECT_FLIPEX.</td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</td>
<td>0x00000002</td>
<td>Установите этот флаг при создании цепочки устройств или буферов, чтобы включить удаление z-буфера. Если этот флаг установлен, содержимое буфера шаблона глубины будет недействительным после <a href="/windows/desktop/api"><strong>вызова либо</strong></a> <a href="/windows/desktop/api"><strong>сетдепсстенЦилсурфаце</strong></a> с другой поверхностью глубины. Отмена данных z-буфера может повысить производительность и зависит от драйвера. Среда выполнения отладки будет принудительно применять отмену, очистив z-буфер до какого-либо постоянного значения после <a href="/windows/desktop/api"><strong>вызова либо</strong></a> <a href="/windows/desktop/api"><strong>сетдепсстенЦилсурфаце</strong></a> с другой поверхностью глубины.<br/> Удаление данных z-буфера недопустимо для всех блокируемых форматов, D3DFMT_D16_LOCKABLE и D3DFMT_D32F_LOCKABLE. Любое использование <a href="/windows/desktop/api"><strong>креатедевице</strong></a> с указанием блокируемого формата и отклонения z-буфера завершится ошибкой. Дополнительные сведения о форматах см. в разделе <a href="d3dformat.md">D3DFORMAT</a>.<br/></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</td>
<td>0x00000001</td>
<td>Установите этот флаг, если приложению требуется возможность непосредственной блокировки заднего буфера. Обратите внимание, что задние буферы не являются блокируемыми, если только в приложении не указано D3DPRESENTFLAG_LOCKABLE_BACKBUFFER при вызове <a href="/windows/desktop/api"><strong>креатедевице</strong></a> или <a href="/windows/desktop/api"><strong>сбросе</strong></a>. Блокируемые задние буферы приводят к снижению производительности в некоторых конфигурациях графического оборудования. Выполнение операции блокировки (или использования <a href="/windows/desktop/api"><strong>упдатесурфаце</strong></a> для записи) в блокируемом обратном буфере снижает производительность на многих картах. В этом случае рассмотрите возможность использования текстурированных треугольников для перемещения данных в задний буфер.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 9Ex:<br/> В Direct3D9Ex этот флаг не может быть установлен, если D3DSWAPEFFECT имеет D3DSWAPEFFECT_FLIPEX, так как модель перелистывания позволяет диспетчер окон рабочего стола доступ к обратному буферу приложения. Невозможно заблокировать общую поверхность между процессами.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_NOAUTOROTATE</td>
<td>0x00000020</td>
<td>Повернутые мониторы обрабатываются автоматически при помощи вращающейся копии во время презентации, что не очень эффективно. Этот флаг означает, что приложение будет выполнять собственный поворот экрана. 
<table>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 9Ex:<br/> Этот флаг доступен только в Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p>Приложения могут достичь собственного вращения, возможно, с помощью матрицы повернутого представления. Для поиска текущего параметра вращения должны использоваться методы <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>жетдисплаймодикс</strong></a> и <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>жетадаптердисплаймодикс</strong></a> . Параметры ширины и высоты буфера в <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>креатедевицеекс</strong></a> и <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ресетекс</strong></a> должны иметь альбомную ориентацию, тогда как структура полноэкранного режима должна быть такой же, как и та, что возвращается из <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>енумадаптермодесекс</strong></a> (т. е. ширина и высота меняются при повороте 90 и 270 градусов).</p>
<p>При использовании блокировки повернутых целевых объектов отрисовки, в левом верхнем углу предполагается, что они не будут иметь значение true, целевой объект прорисовки SURFACE_DESC останется альбомным (как подразумевается в параметрах создания), а окно GDI, координаты мыши и, таким образом, должны быть правильно переведены при использовании с целевым объектом отрисовки Direct3D и сценой.</p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_UNPRUNEDMODE</td>
<td>0x00000040</td>
<td>Используйте этот флаг, чтобы указать любой режим вывода RAW, перечисленный видеоадаптером, даже если в Direct3D был указан недопустимый режим. Приложение должно реализовать это надежным образом в случае, если требуемый режим действительно является недопустимым. 
<table>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 9Ex:<br/> Этот флаг доступен только в Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_VIDEO</td>
<td>0x00000010</td>
<td>Это указание драйверу, что задние буферы будут содержать данные видео.</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</td>
<td>0x00000080</td>
<td>Указывает, является ли наложение полным диапазоном RGB или ограниченным диапазоном RGB. Установка этого флага означает ограниченный диапазон RGB. В ограниченном диапазоне RGB диапазон RGB сжимается таким, что 16:16:16 является черным, а 235:235:235 — белым.
<table>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 9Ex:<br/> Этот флаг доступен только в Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</td>
<td>0x00000100</td>
<td>Указывает, является ли наложение BT. 601 или BT. 709. Установка этого флага означает BT. 709 для телевидения высокой четкости (ТВВЧ).
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
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</td>
<td>0x00000200</td>
<td>Указывает, является ли наложение традиционным Икбкр или расширенным Икбкр (Ксвикк). Установка этого флага означает расширенный Икбкр (Ксвикк).
<table>
<tbody>
<tr class="odd">
<td>Различия между Direct3D 9 и Direct3D 9Ex:<br/> Этот флаг доступен только в Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_RESTRICTED_CONTENT</td>
<td>0x00000400</td>
<td>установка этого флага означает, что имеющуюся цепочку буферов содержит защищенное содержимое и автоматически заставляет среду выполнения ограничить доступ к имеющуюся цепочку буферов, чтобы только рабочий стол Windows Manager (DWM) мог использовать имеющуюся цепочку буферов.
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
<td>D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</td>
<td>0x00000800</td>
<td>Установка этого флага означает, что драйвер должен ограничивать доступ ко всем общим ресурсам, созданным для взаимодействия с DWM. Вызывающий объект должен создать канал с проверкой подлинности с помощью драйвера. После этого драйвер должен разрешить доступ к процессам, пытающимся открыть эти общие ресурсы.
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



 

Эти константы используются [**\_ параметрами D3DPRESENT**](d3dpresent-parameters.md).

## <a name="constant-information"></a>Сведения о константе



| Требование                         | Значение            |
|--------------------------|-------------|
| Заголовок                   | d3d9types. h |
| Минимальная операционная система | Windows 98  |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Константы Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




