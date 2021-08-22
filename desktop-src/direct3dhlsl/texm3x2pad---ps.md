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
ms.openlocfilehash: 55943d2a62f49e6bdb45d893385f0824898d665ee4a4065c4f8c8ed75c2f8249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485444"
---
# <a name="texm3x2pad---ps"></a>texm3x2pad-PS

Выполняет умножение первой строки на матрицу с двумя строками. Эту инструкцию необходимо сочетать с [texm3x2tex-PS](texm3x2tex---ps.md) или [texm3x2depth-PS](texm3x2depth---ps.md). Дополнительные сведения об использовании тексмпад см. в любой из этих инструкций.

## <a name="syntax"></a>Синтаксис



| tex3x2pad DST, src |
|--------------------|



 

where

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2pad            | x    | x    | x    |      |      |      |       |      |       |



 

Эта инструкция не может использоваться сама по себе.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




