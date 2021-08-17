---
title: Модель шейдера 4
description: Shader Model 4 является надмножеством возможностей в модели шейдера 3, за исключением того, что модель шейдеров 4 не поддерживает функции в модели шейдера 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d90444aff674ce876f19f02f21104dd7e42143de5926ba068bbe2c49f427fdde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725891"
---
# <a name="shader-model-4"></a>Модель шейдера 4

Shader Model 4 является надмножеством возможностей в [модели шейдера 3](dx-graphics-hlsl-sm3.md), за исключением того, что модель шейдеров 4 не поддерживает функции в модели шейдера 1. Она была разработана с помощью стандартного шейдера, предоставляющего общий набор функций для всех программируемых шейдеров, которые можно программировать только с помощью HLSL.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Компонент</th>
<th>Возможностями.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Набор инструкций</td>
<td><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Функции HLSL</strong></a></td>
</tr>
<tr class="even">
<td>Набор регистров</td>
<td>Набор регистров доступен через члены в постоянных и текстурных буферах с использованием семантики HLSL для таких операций, как упаковка компонентов.
<ul>
<li>Регистры шейдеров пикселей (см. раздел <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">регистры-ps_4_0</a> и <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">регистры-ps_4_1</a>)</li>
<li>Регистры шейдеров вершин (см. раздел <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">регистры-vs_4_0</a> и <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">регистры-vs_4_1</a>)</li>
<li>Регистры шейдеров Geometry (см. раздел <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">регистры-gs_4_0</a> и <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">регистры-gs_4_1</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Максимум вершинного шейдера</td>
<td>Без ограничений</td>
</tr>
<tr class="even">
<td>Максимальный размер шейдера пикселей</td>
<td>Без ограничений</td>
</tr>
<tr class="odd">
<td>Добавлены новые профили шейдеров</td>
<td>gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 *</td>
</tr>
<tr class="even">
<td>Добавлен новый профиль Effect-Framework</td>
<td>fx_4_0, fx_4_1 *</td>
</tr>
</tbody>
</table>



 

\* -GS \_ 4 \_ 1, PS \_ 4 1 \_ , VS \_ 4 \_ 1 и FX \_ 4 1 \_ поддерживаются в Direct3D 10,1 или более поздней версии.

Модель шейдеров 4 поддерживает новый этап конвейера — этап шейдера Geometry, который можно использовать для создания или изменения существующей геометрии. Он также включает два новых типа объектов: объект потокового вывода, предназначенный для потоковой передачи данных из этапа геометрии, и объект текстуры шаблона, реализующий функции выборки текстур.

-   [Основные компоненты шейдера](dx-graphics-hlsl-common-core.md)
-   [Константы](dx-graphics-hlsl-constants.md)
-   [Объект Geometry-Shader](dx-graphics-hlsl-geometry-shader.md)
-   [Потоковый выходной объект](dx-graphics-hlsl-so-type.md)
-   [Объект текстуры](dx-graphics-hlsl-to-type.md)

Модель шейдеров 4 поддерживает правила упаковки, определяющие, насколько тесно данные могут быть упорядочены при хранении. Эти правила описаны в разделе [правила упаковки для константных переменных](dx-graphics-hlsl-packing-rules.md) .

В разделе [Assembly Shader Model 4](dx-graphics-hlsl-sm4-asm.md) описаны инструкции ассемблера, поддерживаемые шейдером Model 4 и shader Model 4,1.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Модели шейдеров и профили шейдеров](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




