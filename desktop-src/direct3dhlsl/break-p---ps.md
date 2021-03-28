---
title: бреакп-PS
description: Условное нарушение текущего цикла в ближайшем ендлуп-PS или ендреп-PS. Используйте один из компонентов в качестве условия, чтобы определить, следует ли выполнять инструкцию.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412192"
---
# <a name="breakp---ps"></a>бреакп-PS

Условное нарушение текущего цикла в ближайшем [ендлуп-PS](endloop---ps.md) или [ендреп-PS](endrep---ps.md). Используйте один из компонентов в качестве условия, чтобы определить, следует ли выполнять инструкцию.

## <a name="syntax"></a>Синтаксис



| бреакп \[ ! \] P0. x|&|гармошкой|Белая |
|-----------------------------|



 

Где:

-   \[!\] является необязательным модификатором отрицания.
-   P0 — это [регистр предикатов](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} — это обязательная репликация свиззле в P0.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| бреакп                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




