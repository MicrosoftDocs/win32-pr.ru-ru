---
title: texm3x3pad-PS
description: Выполняет первую или вторую строку умножение матрицы из трех строк. Эта инструкция должна использоваться в сочетании с texm3x3-PS, texm3x3spec-PS, texm3x3vspec-PS или texm3x3tex-PS.
ms.assetid: 375526ee-cd58-4179-9b21-c63f17282f6b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0013c4d2baf9a404406982b5a8e984698a964f33
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412172"
---
# <a name="texm3x3pad---ps"></a>texm3x3pad-PS

Выполняет первую или вторую строку умножение матрицы из трех строк. Эта инструкция должна использоваться в сочетании с [texm3x3-PS](texm3x3---ps.md), [texm3x3spec-PS](texm3x3spec---ps.md), [texm3x3vspec-PS](texm3x3vspec---ps.md)или [texm3x3tex-PS](texm3x3tex---ps.md).

## <a name="syntax"></a>Синтаксис



| texm3x3pad DST, src |
|---------------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3pad            | x    | x    | x    |      |      |      |       |      |       |



 

Эта инструкция не может использоваться сама по себе.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




