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
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983897"
---
# <a name="mova---vs"></a>МОВА — VS

Перемещение данных из регистра с плавающей запятой в [регистр адресов](dx9-graphics-reference-asm-vs-registers-address.md)a0.

## <a name="syntax"></a>Синтаксис



| МОВА DST, src |
|---------------|



 

где

-   DST должен быть [регистром адресов](dx9-graphics-reference-asm-vs-registers-address.md), a0.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




