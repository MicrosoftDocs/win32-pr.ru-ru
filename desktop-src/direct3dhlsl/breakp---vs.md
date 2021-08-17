---
title: бреакп — VS
description: Безусловное нарушение текущего цикла в ближайшем ендлуп-VS или ендреп-vs. Используйте один из компонентов, зарегистрированных в предикате, чтобы определить, следует ли выполнять инструкцию.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a768acaecaa77a42990b34c50cd8eccb24d61353550751f3ed830e7844d7624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794318"
---
# <a name="breakp---vs"></a>бреакп — VS

Безусловное нарушение текущего цикла в ближайшем [ендлуп-VS](endloop---vs.md) или [ендреп-VS](endrep---vs.md). Используйте один из компонентов в качестве условия, чтобы определить, следует ли выполнять инструкцию.

## <a name="syntax"></a>Синтаксис



| бреакп \[ ! \] P0. x|&|гармошкой|Белая |
|-----------------------------|



 

Где:

-   \[!\] Необязательное логическое значение NOT.
-   P0 — это регистр предикатов. См. раздел [Регистрация предиката](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} — это обязательная репликация свиззле в P0.

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| бреакп                 |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




