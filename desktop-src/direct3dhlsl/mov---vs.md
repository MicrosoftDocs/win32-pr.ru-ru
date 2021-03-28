---
title: MOV – VS
description: Перемещение данных с плавающей запятой между регистрами.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784989"
---
# <a name="mov---vs"></a>MOV – VS

Перемещение данных с плавающей запятой между регистрами.

## <a name="syntax"></a>Синтаксис



| MOV DST, src |
|--------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| функцию                    | x    | x    | x    | x     | x    | x     |



 

Может использоваться для данных с плавающей запятой. Для версии VS \_ 1 \_ можно также использовать для записи регистра адресов. При использовании для обновления регистров адресов значения преобразуются из плавающей запятой с помощью функции округления к ближайшему.

В следующем фрагменте кода показаны выполняемые операции.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




