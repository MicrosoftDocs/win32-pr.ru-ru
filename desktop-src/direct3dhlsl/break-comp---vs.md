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
ms.openlocfilehash: a02bf34844918255086b318d9a13feeabbd6e75bdecca03684adaba70b420626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626564"
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

## <a name="remarks"></a>Remarks

Эта инструкция поддерживается в следующих версиях.



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| разбить \_ comp            |      |      | x    | x     | x    | x     |



 

Если сравнение истинно, оно выходит из текущего цикла, как показано.


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




