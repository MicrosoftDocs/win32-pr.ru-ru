---
title: Модель шейдера 2
description: Модель шейдеров 2 добавила дополнительные возможности в модель шейдера 1.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed402b34bdb8ba8caed8dc7cd5b66126d242c9ad
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988027"
---
# <a name="shader-model-2"></a>Модель шейдера 2

Модель шейдеров 2 добавила дополнительные возможности в [модель шейдера 1](dx-graphics-hlsl-sm1.md).





|--------|-------| | Компонент | Возможности | | Набор инструкций | <ul><li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Функции HLSL</strong></a></li><li>Инструкции по сборке (см. <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">инструкции по VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">инструкции vs_2_x</a>, инструкции <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0</a>, инструкции <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x</a>)</li></ul> | | Зарегистрировать набор | <ul><li>Регистры шейдеров пикселей (см. <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">Ps_2_0 регистры</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">регистры ps_2_x</a>)</li><li>Регистры шейдеров вершин (см. раздел <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">registers-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">registers-vs_2_x</a>)</li></ul> | | Максимальный размер шейдера пикселей | <ul><li>ps_2_0-32 текстура + 64, арифметические действия</li><li>ps_2_x-96 минимум и до количества слотов в D3DCAPS9. D3DPSHADERCAPS2_0. Нуминструктионслотс. См. D3DPSHADERCAPS2_0</li></ul> | | Максимум вершинного шейдера | 256 инструкции | | Профили шейдеров | ps_2_0, ps_2_x, vs_2_0, vs_2_x | 




 

Дополнительные сведения о модели шейдеров 2 см. в следующих статьях:

-   [Шейдер пикселей 2,0](dx9-graphics-reference-asm-ps-2-0.md), [построитель текстуры 2. x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Шейдер вершин 2,0](dx9-graphics-reference-asm-vs-2-0.md), [Вершинный шейдер 2. x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Модели шейдеров и профили шейдеров](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




