---
title: Call-PS
description: Выполняет вызов функции в инструкцию, помеченную указанной меткой. | Call-PS
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ae1b8a19178b0a6633a98472814e225e9ac2f7de9e3e2f016720f2f5b1a9b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794088"
---
# <a name="call---ps"></a>Call-PS

Выполняет вызов функции в инструкцию, помеченную указанной меткой.

## <a name="syntax"></a>Синтаксис



| вызов l\# |
|----------|



 

Где:

-   l \# — [Метка-PS](label---ps.md) , помечающая начало подпрограммы для вызова.

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| вызывает                  |      |      |      |      |      | x    | x     | x    | x     |



 

Эта инструкция выполняет следующие действия:

1.  Адрес принудительной отправки следующей инструкции в стек адресов возврата.
2.  Продолжить выполнение из инструкции, помеченной меткой.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




