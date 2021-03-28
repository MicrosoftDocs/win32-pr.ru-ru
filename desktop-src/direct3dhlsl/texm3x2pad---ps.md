---
title: texm3x2pad-PS
description: Выполняет умножение первой строки на матрицу с двумя строками. Эту инструкцию необходимо сочетать с texm3x2tex-PS или texm3x2depth-PS. Дополнительные сведения об использовании тексмпад см. в любой из этих инструкций.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91d161d0b3cc7a90bbbfcee17774b1a587e4c04f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890020"
---
# <a name="texm3x2pad---ps"></a>texm3x2pad-PS

Выполняет умножение первой строки на матрицу с двумя строками. Эту инструкцию необходимо сочетать с [texm3x2tex-PS](texm3x2tex---ps.md) или [texm3x2depth-PS](texm3x2depth---ps.md). Дополнительные сведения об использовании тексмпад см. в любой из этих инструкций.

## <a name="syntax"></a>Синтаксис



| tex3x2pad DST, src |
|--------------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2pad            | x    | x    | x    |      |      |      |       |      |       |



 

Эта инструкция не может использоваться сама по себе.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




