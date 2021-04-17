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
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412184"
---
# <a name="sgn---vs"></a>СГН — VS

Вычисление знака входных данных.

## <a name="syntax"></a>Синтаксис



| СГН DST, src0, src1, src2 |
|---------------------------|



 

где

-   DST — это регистр назначения.
-   src0 является исходным регистром.
-   src1 — это временный регистр, содержащий промежуточные результаты. После выполнения, содержимое не определено.
-   src2 — это временный регистр, содержащий промежуточные результаты. После выполнения, содержимое не определено.

## <a name="remarks"></a>Примечания



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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




