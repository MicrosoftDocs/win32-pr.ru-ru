---
title: Метка — VS
description: Пометьте следующую инструкцию как индекс метки. | Метка — VS
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81c36c3db93acdc82d725c9cf7893c52d7177bbe70e16378c3b86f39ec4d6a2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854184"
---
# <a name="label---vs"></a>Метка — VS

Пометьте следующую инструкцию как индекс метки.

## <a name="syntax"></a>Синтаксис



| Метка l\# |
|-----------|



 

где \# определяет номер метки.

Для VS \_ 2 \_ 0 и VS \_ 2 \_ x номер метки должен находиться в диапазоне от 0 до 15.

Для VS \_ 2 \_ SW, VS \_ 3 \_ 0 и VS \_ 3 \_ SW номер метки должен находиться в диапазоне от 0 до 2047.

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| метка                  |      | x    | x    | x     | x    | x     |



 

Эта инструкция определяет метку, расположенную в следующей инструкции шейдера. Инструкция Label может присутствовать непосредственно после инструкции [RET](ret---vs.md) (которая определяет конец предыдущей подпрограммы или основной программы).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




