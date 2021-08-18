---
description: Константы фильтрации текстур.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86645ca1d0f8c1904307b80c27c2b8ce8d635229d3bb15b0f8178d6a9d70dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804672"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

Константы фильтрации текстур.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#определенно</td>
<td>Описание</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_CONVOLUTIONMONO</td>
<td>Устройство поддерживает фильтрацию свертки по монохромному свертыванию. Этот фильтр представлен элементом D3DTEXF_CONVOLUTIONMONO перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> . 
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
<td>D3DPTFILTERCAPS_MAGFPOINT</td>
<td>Устройство поддерживает многоэтапную фильтрацию на основе точек для увеличения текстур. Фильтр увеличения точки-образца представлен элементом D3DTEXF_POINT перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFLINEAR</td>
<td>Устройство поддерживает фильтрацию билинейной интерполяции на уровне для увеличения MIP-карты. Фильтр функции текстурирования интерполяции билинейной представлен элементом D3DTEXF_LINEAR перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFANISOTROPIC</td>
<td>Устройство поддерживает анизотропную фильтрацию по этапам для увеличения текстур. Фильтр анизотропной лупы представлен элементом D3DTEXF_ANISOTROPIC перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</td>
<td>Устройство поддерживает многоэтапную фильтрацию образцов для увеличения текстур. Фильтр попирамидальной лупы представляется элементом D3DTEXF_PYRAMIDALQUAD перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</td>
<td>Устройство поддерживает грубую фильтрацию по Гауссу для увеличенных текстур.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFPOINT</td>
<td>Устройство поддерживает многоэтапную фильтрацию на основе точек для текстур Минификация. Фильтр минификации в виде образца представляется элементом D3DTEXF_POINT перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>Устройство поддерживает линейную фильтрацию по этапам для текстур Минификация. Фильтр линейного минификации представляется элементом D3DTEXF_LINEAR перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>Устройство поддерживает анизотропную фильтрацию по этапам для текстур Минификация. Фильтр анизотропной минификации представляется элементом D3DTEXF_ANISOTROPIC перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</td>
<td>Устройство поддерживает фильтрацию образцов с поэтапным примером для текстур Минификация.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFGAUSSIANQUAD</td>
<td>Устройство поддерживает грубую фильтрацию по Гауссу для текстур Минификация.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MIPFPOINT</td>
<td>Устройство поддерживает фильтрацию точек на уровне этапа для MIP-карты. Фильтр функции текстурирования в виде образца представляется элементом D3DTEXF_POINT перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MIPFLINEAR</td>
<td>Устройство поддерживает фильтрацию билинейной интерполяции на уровне MIP-карты. Фильтр функции текстурирования интерполяции билинейной представлен элементом D3DTEXF_LINEAR перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
</tbody>
</table>



 

Эти константы используются членами Текстурефилтеркапс, Кубетекстурефилтеркапс, Волуметекстурефилтеркапс и Вертекстекстурефилтеркапс в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Сведения о константе



|  Требование                        | Значение           |
|--------------------------|------------|
| Заголовок                   | d3d9caps. h |
| Минимальная операционная система | Windows 98 |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Константы Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
