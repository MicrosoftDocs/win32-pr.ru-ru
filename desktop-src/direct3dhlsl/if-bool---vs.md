---
title: Если bool — VS
description: Запускает if... else... endif — блок vs.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b113c806342d786d258713128bc2cadcbb000235c2639f49e5b57ce3fa3bd2e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986534"
---
# <a name="if-bool---vs"></a>Если bool — VS

Запускает if... [else](else---vs.md)... [endif — блок VS](endif---vs.md) .

## <a name="syntax"></a>Синтаксис



| Если bool |
|---------|



 

где bool — номер регистра bool. См. раздел [Постоянный логический регистр](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Если bool                |      | x    | x    | x     | x    | x     |



 

Если исходный логический регистр в операторе If имеет значение true, выполняется код, заключенный в операторе if и соответствующий else. В противном случае код, заключенный в [else](else---vs.md)... выполняется инструкция [endif-VS](endif---vs.md) . Эта инструкция использует один слот инструкций.

Если блоки могут быть вложенными.

Блок if не может помешать блоку цикла.

## <a name="example"></a>Пример

Эта инструкция предоставляет условное статическое управление потоком.


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[else — VS](else---vs.md)
</dt> <dt>

[endif — VS](endif---vs.md)
</dt> </dl>

 

 




