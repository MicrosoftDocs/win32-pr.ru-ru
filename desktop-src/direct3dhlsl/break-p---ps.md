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
ms.openlocfilehash: 2da0d2bceea7a3e44f02e6b732337cb3447d6ef1c9798f95b664bf4da96ec2dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983324"
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

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| бреакп                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




