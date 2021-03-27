---
title: ФРК-PS
description: Возвращает дробную часть каждого входного компонента. | ФРК-PS
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353415"
---
# <a name="frc---ps"></a>ФРК-PS

Возвращает дробную часть каждого входного компонента.

## <a name="syntax"></a>Синтаксис



| ФРК DST, src |
|--------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| фрк                   |      |      |      |      | x    | x    | x     | x    | x     |



 

В следующем фрагменте кода показано, как работает инструкция.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



Функция Floor Преобразует аргумент, переданный в, в наибольшее целое число, которое меньше (или равно) аргументу. Это преобразование преобразуется в тип float, а затем вычитается ФОМ исходное значение. Результирующие дробные значения в диапазоне от 0,0 до 1,0.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




