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
ms.openlocfilehash: 611ec04a5c3a53bbb8c6c35380bd0d9f824dc697a7d27a3656b262d885fb4eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457514"
---
# <a name="if-bool---ps"></a>If bool-PS

Начало блока if.

## <a name="syntax"></a>Синтаксис



| Если bool |
|---------|



 

Где:

-   bool представляет собой логический (логический) номер регистра. См. раздел [Постоянный логический регистр](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Если bool               |      |      |      |      |      | x    | x     | x    | x     |



 

Если исходный логический регистр в операторе If имеет значение true, выполняется код, заключенный в операторе if и соответствующий параметру [endif-PS](endif---ps.md) или [else-PS](else---ps.md) . В противном случае код, заключенный в else-PS... выполняется инструкция endif-PS. Эта инструкция использует один слот инструкций.

Блок If может быть вложенным.

Блок if не может помешать блоку цикла.

За блоком if может следовать блок инструкции, или инструкция [else-PS](else---ps.md) , а также инструкция [endif-PS](endif---ps.md) .

## <a name="example"></a>Пример

Эта инструкция предоставляет условное статическое управление потоком.


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[else-PS](else---ps.md)
</dt> <dt>

[endif-PS](endif---ps.md)
</dt> </dl>

 

 




