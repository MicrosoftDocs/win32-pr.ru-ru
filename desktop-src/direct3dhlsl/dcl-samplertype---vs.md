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
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996970"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>дкл \_ самплертипе (SM3-VS ASM)

Объявите образец шейдера вершин.

## <a name="syntax"></a>Синтаксис



|                      |
|----------------------|
| дкл \_ самплертипе s\# |



 

где:

-   \_Самплертипе определяет тип данных образца. Определяет, сколько координат требуется для каждой координаты текстуры при выборки. Определены следующие измерения координат текстуры.
    -   \_двухмерном
    -   \_Куба
    -   \_тома
-   s \# определяет образец, где s — это аббревиатура для образца, а \# — номер образца. [Образцы (Direct3D 9 ASM-VS)](dx9-graphics-reference-asm-vs-registers-sampler.md)s являются псевдо, так как вы не можете напрямую читать их или записывать.

## <a name="remarks"></a>Примечания



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| дкл \_ самплертипе       |      |      |      |       | x    | x     |



 

Все \_ инструкции самплертипе дкл должны располагаться перед первой исполняемой инструкцией.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




