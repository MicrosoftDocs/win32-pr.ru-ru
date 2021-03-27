---
title: Сравнение break_comp
description: Безусловное нарушение текущего цикла в ближайшем ендлуп-VS или ендреп-vs.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890012"
---
# <a name="break_comp---vs"></a>прерывание \_ comp-VS

Безусловное нарушение текущего цикла в ближайшем [ендлуп-VS](endloop---vs.md) или [ендреп-VS](endrep---vs.md).

## <a name="syntax"></a>Синтаксис



| Разбейте \_ comp src0, src1 |
|------------------------|



 

Где:

-   \_Comp — это сравнение двух исходных регистров. Может принимать одно из следующих значений: 

    | Синтаксис | Сравнение            |
    |--------|-----------------------|
    | \_gt   | Больше чем          |
    | \_светл   | Меньше чем             |
    | \_GE   | Больше или равно |
    | \_Le   | Меньше или равно    |
    | \_EQ   | Равно              |
    | \_видимому   | Не равно          |

    

     

-   src0 является исходным регистром. Для выбора одного компонента требуется репликация свиззле.
-   src1 является исходным регистром. Для выбора одного компонента требуется репликация свиззле.

## <a name="remarks"></a>Примечания

Эта инструкция поддерживается в следующих версиях.



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| разбить \_ comp            |      |      | x    | x     | x    | x     |



 

Если сравнение истинно, оно выходит из текущего цикла, как показано.


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




