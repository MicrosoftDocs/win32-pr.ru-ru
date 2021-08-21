---
title: Модель шейдера 3
description: Модель шейдеров 3 добавила дополнительные возможности в модель шейдера 2.
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed2d64ccfb06fc0fe50e5bd0075732c1fd9cbb70ca1e05bda5afd24cd5c5f98f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789544"
---
# <a name="shader-model-3-hlsl-reference"></a>Модель шейдера 3 (Справочник по HLSL)

Модель шейдеров 3 добавила дополнительные возможности в [модель шейдера 2](dx-graphics-hlsl-sm2.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Компонент</td>
<td>Возможностями.</td>
</tr>
<tr class="even">
<td>Набор инструкций</td>
<td><ul>
<li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Функции HLSL</strong></a></li>
<li>Инструкции по сборке (см. <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">Ps_3_0 инструкции</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">инструкции — vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Набор регистров</td>
<td><ul>
<li>Регистры шейдеров пикселей (см. раздел <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">регистры ps_3_0</a>)</li>
<li>Регистры шейдеров вершин (см. раздел <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">registers-vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Максимальный размер шейдера пикселей</td>
<td>512 минимум и до количества слотов в D3DCAPS9. MaxPixelShader30InstructionSlots (см. <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</td>
</tr>
<tr class="odd">
<td>Максимум вершинного шейдера</td>
<td>512 минимум и до количества слотов в D3DCAPS9. MaxVertexShader30InstructionSlots (см. <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</td>
</tr>
<tr class="even">
<td>Профили шейдеров</td>
<td>ps_3_0, vs_3_0</td>
</tr>
</tbody>
</table>



 

Дополнительные сведения о шейдерах модели 3 см. в следующих статьях:

-   [Построитель текстуры 3,0](dx9-graphics-reference-asm-ps-3-0.md)
-   [Шейдер вершин 3,0](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Модели шейдеров и профили шейдеров](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 