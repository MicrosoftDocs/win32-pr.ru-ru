---
title: МОВА — VS
description: Перемещение данных из регистра с плавающей запятой в регистр адресов a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dec849009ee47b4aaef1bc3766e2b141a8a6ccf5e17b16a370c6ea8284eaf957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986334"
---
# <a name="mova---vs"></a>МОВА — VS

Перемещение данных из регистра с плавающей запятой в [регистр адресов](dx9-graphics-reference-asm-vs-registers-address.md)a0.

## <a name="syntax"></a>Синтаксис



| МОВА DST, src |
|---------------|



 

where

-   DST должен быть [регистром адресов](dx9-graphics-reference-asm-vs-registers-address.md), a0.
-   src является исходным регистром.

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| мова                   |      | x    | x    | x     | x    | x     |



 

Перемещает данные с плавающей запятой в целочисленный регистр. Значения преобразуются из плавающей запятой с помощью функции округления к ближайшему.

Регистр адреса — это единственный допустимый регистр назначения.

В следующем фрагменте кода показаны выполняемые операции.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



Для версий 2 \_ x и выше регистр адресов является вектором компонентов. Поэтому разрешена любая маска записи.


```
mova a0.xz, r0
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




