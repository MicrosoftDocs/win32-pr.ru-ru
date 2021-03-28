---
title: dcl_tgsm_raw (SM5-ASM)
description: Объявите ссылку на область общей памяти, доступную для группы потоков COMPUTE Shader s.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785001"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a>дкл \_ тгсм \_ RAW (SM5-ASM)

Объявите ссылку на область общей памяти, доступную для группы потоков COMPUTE Shader s.



| дкл \_ тгсм \_ RAW g \# , byteCount |
|-------------------------------|



 



| Элемент                                                                                                       | Описание                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*модуле\#*<br/>                                                 | \[в \] ссылке на блок типа *byteCount* для нетипизированной общей памяти. <br/> |
| <span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*<br/> | \[в \] должно быть кратно 4. <br/>                                             |



 

## <a name="remarks"></a>Примечания

Общий объем хранилища для всех g \# должен быть <= объем общей памяти, доступной для каждой группы потоков, которая является 32 КБ.

В экстремальном случае можно объявить 8192 \# с общим числом g s, каждый с параметром *byteCount* 4.

В противоположной крайней части можно объявить один g \# с *byteCount* 32768.

> [!Note]  
> CS \_ 4 \_ 0 и CS \_ 4 \_ 1 поддерживают [дкл \_ тгсм \_ Structured](dcl-tgsm-structured--sm5---asm-.md), но не **дкл \_ тгсм \_ RAW**.

 

Эта инструкция применяется к следующим этапам шейдера:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта инструкция поддерживается в следующих моделях шейдеров:



| Модель шейдера                                              | Поддерживается |
|-----------------------------------------------------------|-----------|
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | Нет        |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Нет        |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сборка Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





