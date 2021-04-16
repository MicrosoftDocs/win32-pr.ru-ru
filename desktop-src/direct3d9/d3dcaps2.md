---
description: Флаги возможностей драйвера.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953e73c0ea6b079a6b8f0658790c749b4f30a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719258"
---
# <a name="d3dcaps2"></a>D3DCAPS2

Флаги возможностей драйвера.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#определенно</td>
<td>Значение</td>
<td>Описание</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANAUTOGENMIPMAP</td>
<td>0x40000000L</td>
<td>Драйвер способен автоматически создавать MIP-карты. Дополнительные сведения см. в разделе <a href="automatic-generation-of-mipmaps.md">Автоматическое создание MIP-карты (Direct3D 9)</a>.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANCALIBRATEGAMMA</td>
<td>0x00100000L</td>
<td>В системе установлен калибратора, который может автоматически корректировать гамму-шкалу, чтобы результат совпадал во всех системах с калибратора. Чтобы вызвать калибратора при установке новых уровней гаммы, используйте флаг D3DSGR_CALIBRATE при вызове <a href="/windows/desktop/api"><strong>сетгаммарамп</strong></a>. Калибровка гаммы увеличивает нагрузку на обработку и не должна часто использоваться.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANSHARERESOURCE</td>
<td>0x80000000L</td>
<td>Устройство может создавать совместно создаваемые ресурсы. Методы, создающие ресурсы, могут задавать значения, отличные от NULL, для их параметров <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>пшаредхандле</strong></a> . 
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
<td>D3DCAPS2_CANMANAGERESOURCE</td>
<td>0x10000000L</td>
<td>Драйвер способен управлять ресурсами. Для таких драйверов D3DPOOL_MANAGED ресурсы будут управляться драйвером. Чтобы Direct3D переопределял драйвер, чтобы Direct3D управлял ресурсы, используйте флаг D3DCREATE_DISABLE_DRIVER_MANAGEMENT при вызове <a href="/windows/desktop/api"><strong>креатедевице</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_DYNAMICTEXTURES</td>
<td>0x20000000L</td>
<td>Драйвер поддерживает динамические текстуры.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_FULLSCREENGAMMA</td>
<td>0x00020000L</td>
<td>Драйвер поддерживает настройку динамической гаммы пандус в полноэкранном режиме.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_RESERVED</td>
<td>0x02000000L</td>
<td>Процессу не используется.</td>
</tr>
</tbody>
</table>



 

Эти константы используются членом D3CAPS2 объекта [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Сведения о константе



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Минимальная операционная система | Windows 98 |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Константы Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
