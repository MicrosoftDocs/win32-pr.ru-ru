---
title: If bool-PS
description: Начало блока if.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784890"
---
# <a name="if-bool---ps"></a>If bool-PS

Начало блока if.

## <a name="syntax"></a>Синтаксис



| Если bool |
|---------|



 

Где:

-   bool представляет собой логический (логический) номер регистра. См. раздел [Постоянный логический регистр](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Если bool               |      |      |      |      |      | x    | x     | x    | x     |



 

Если исходный логический регистр в операторе If имеет значение true, выполняется код, заключенный в операторе if и соответствующий параметру [endif-PS](endif---ps.md) или [else-PS](else---ps.md) . В противном случае код, заключенный в else-PS... выполняется инструкция endif-PS. Эта инструкция использует один слот инструкций.

Блок If может быть вложенным.

Блок if не может помешать блоку цикла.

За блоком if может следовать блок инструкции, или инструкция [else-PS](else---ps.md) , а также инструкция [endif-PS](endif---ps.md) .

## <a name="example"></a>Например, .

Эта инструкция предоставляет условное статическое управление потоком.


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[else-PS](else---ps.md)
</dt> <dt>

[endif-PS](endif---ps.md)
</dt> </dl>

 

 




