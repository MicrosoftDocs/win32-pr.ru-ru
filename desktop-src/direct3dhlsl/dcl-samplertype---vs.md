---
title: dcl_samplerType (SM3-VS ASM)
description: Объявите образец шейдера вершин.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 048246f8a48430dca26a763e9266f00edd61215e769f4ff5385036054aebc34b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726574"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>дкл \_ самплертипе (SM3-VS ASM)

Объявите образец шейдера вершин.

## <a name="syntax"></a>Синтаксис

дкл \_ самплертипе s\#



 

где:

-   \_Самплертипе определяет тип данных образца. Определяет, сколько координат требуется для каждой координаты текстуры при выборки. Определены следующие измерения координат текстуры.
    -   \_двухмерном
    -   \_Куба
    -   \_тома
-   s \# определяет образец, где s — это аббревиатура для образца, а \# — номер образца. [Образцы (Direct3D 9 ASM-VS)](dx9-graphics-reference-asm-vs-registers-sampler.md)s являются псевдо, так как вы не можете напрямую читать их или записывать.

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| дкл \_ самплертипе       |      |      |      |       | x    | x     |



 

Все \_ инструкции самплертипе дкл должны располагаться перед первой исполняемой инструкцией.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




