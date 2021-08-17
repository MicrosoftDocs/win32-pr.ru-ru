---
title: ФРК — VS
description: Возвращает дробную часть каждого входного компонента. | ФРК — VS
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2ecc6a1c903f78fb7c03442809f792e3ddb984d04975d3f5ecb0b5c918f7ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907647"
---
# <a name="frc---vs"></a>ФРК — VS

Возвращает дробную часть каждого входного компонента.

## <a name="syntax"></a>Синтаксис



| ФРК DST, src |
|--------------|



 

where

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| фрк                    | x    | x    | x    | x     | x    | x     |



 

В следующем фрагменте кода показано, как работает инструкция.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



Функция Floor Преобразует аргумент, переданный в, в наибольшее целое число, которое меньше (или равно) аргументу. Это преобразование преобразуется в тип float, а затем вычитается ФОМ исходное значение. Результирующие дробные значения в диапазоне от 0,0 до 1,0.

Для версии 1 \_ 1 допустимые маски записи:. y и. XY (. x не разрешены).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




