---
title: Инверсия исходного регистра
description: Выполняет вычисление (1 значение) для каждого канала указанного регистра.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983744"
---
# <a name="source-register-invert"></a>Инверсия исходного регистра

Выполняет вычисление (1 значение) для каждого канала указанного регистра.

## <a name="syntax"></a>Синтаксис


```
1 - register
```



## <a name="registers"></a>Регистры

Исходный регистр. Дополнительные сведения о типах регистров см. в описании [ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ регистров PS 1 1 PS 1 2](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.

## <a name="remarks"></a>Примечания

Содержимое регистра не изменяется. Модификатор применяется только к данным, считанным из регистра. Операция инвертирования применяется ко всем четырем цветовым каналам (RGBA).

Этот модификатор можно использовать только с арифметическими инструкциями. Кроме того, этот модификатор нельзя сочетать с другой [маской записи регистра назначения](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="example"></a>Например, .

В этом примере используется инверсия для создания дополнения для Register R1.


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Модификаторы исходных регистров исходного шейдера пикселей](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




