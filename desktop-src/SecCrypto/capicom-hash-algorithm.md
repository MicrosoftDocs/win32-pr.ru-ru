---
description: '\_Перечисление хэш- \_ алгоритма CAPICOM определяет хэш-алгоритм.'
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: Перечисление CAPICOM_HASH_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: df312c7e1ed578150069ff335527a20a2185c721b67a9e0e02cc1d57938b1cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879144"
---
# <a name="capicom_hash_algorithm-enumeration"></a>\_Перечисление хэш- \_ АЛГОРИТМа CAPICOM

Перечисление **\_ хэш- \_ алгоритма CAPICOM** определяет хэш-алгоритм.

## <a name="members"></a>Элементы



| Член                                 | Описание                                                                                                                                                                 | Значение |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_Алгоритм ХЭША \_ CAPICOM \_ SHA1**     | [*Алгоритм*](../secgloss/s-gly.md) SHA, создающий дайджест сообщения 160-bit.<br/> | 0     |
| **\_ \_ MD2 алгоритма CAPICOM hash \_**      | Алгоритм хэширования MD2.<br/>                                                                                                                                           | 1     |
| **\_Хэш- \_ алгоритмы CAPICOM \_ MD4**      | Алгоритм хэширования MD4.<br/>                                                                                                                                           | 2     |
| **\_MD5- \_ алгоритм хеширования \_**      | Алгоритм хэширования MD5.<br/>                                                                                                                                           | 3     |
| **\_Хэш-алгоритм "CAPICOM hash \_ \_ SHA \_ 256"** | Алгоритм хеширования SHA-256.<br/> **CAPICOM 2.0.0.3 и более ранние версии:** Это значение не поддерживается.<br/>                                                                 | 4     |
| **\_Хэш-алгоритм "CAPICOM hash \_ \_ SHA \_ 384"** | Алгоритм хеширования SHA-384.<br/> **CAPICOM 2.0.0.3 и более ранние версии:** Это значение не поддерживается.<br/>                                                                 | 5     |
| **\_Хэш-алгоритм "CAPICOM hash \_ \_ SHA \_ 512"** | Алгоритм хеширования SHA-512.<br/> **CAPICOM 2.0.0.3 и более ранние версии:** Это значение не поддерживается.<br/>                                                                 | 6     |



## <a name="remarks"></a>Remarks

Перечисление **\_ хэш- \_ алгоритма CAPICOM** используется свойством [**хашеддата. Algorithm**](hasheddata-algorithm.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|--------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                |
| Заголовок<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
