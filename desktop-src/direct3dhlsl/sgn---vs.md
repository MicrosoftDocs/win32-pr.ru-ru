---
title: СГН — VS
description: Вычисление знака входных данных.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1a4994c807ff1df99016aad734edf71e5e1ce6efe59fd53a4fb9bb3ee91a4b25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671684"
---
# <a name="sgn---vs"></a>СГН — VS

Вычисление знака входных данных.

## <a name="syntax"></a>Синтаксис



| СГН DST, src0, src1, src2 |
|---------------------------|



 

where

-   DST — это регистр назначения.
-   src0 является исходным регистром.
-   src1 — это временный регистр, содержащий промежуточные результаты. После выполнения, содержимое не определено.
-   src2 — это временный регистр, содержащий промежуточные результаты. После выполнения, содержимое не определено.

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| сгн                    |      | x    | x    | x     | x    | x     |



 

Эта инструкция работает, как показано ниже.


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



src1 и src2 должны быть разными [временными регистрами](dx9-graphics-reference-asm-vs-registers-temporary.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




