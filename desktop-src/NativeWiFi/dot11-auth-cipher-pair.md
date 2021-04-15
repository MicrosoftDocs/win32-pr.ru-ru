---
description: Определяет пару из 802,11 алгоритмов проверки подлинности и шифров, которые могут быть включены одновременно на станции 802,11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: Структура DOT11_AUTH_CIPHER_PAIR (Влантипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683669"
---
# <a name="dot11_auth_cipher_pair-structure"></a>\_ \_ Структура пары шифров для проверки подлинности DOT11 \_

Структура **\_ \_ \_ пары шифров** для проверки подлинности DOT11 определяет пару из 802,11 алгоритмов шифрования и шифров, которые могут быть включены одновременно на станции 802,11.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a>Члены

<dl> <dt>

**аусалгоид**
</dt> <dd>

Алгоритм проверки подлинности, использующий перечислимый тип [**\_ \_ алгоритма проверки**](dot11-auth-algorithm.md) подлинности DOT11.

</dd> <dt>

**Цифералгоид**
</dt> <dd>

Алгоритм шифрования, использующий перечислимый тип [**\_ \_ алгоритма шифрования DOT11**](dot11-cipher-algorithm.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

\_ \_ Пара шифров шифрования DOT11 \_ определяет алгоритм проверки подлинности и шифрования, который можно включить совместно для сетевых подключений "базовый набор служб (BSS)".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                        |
| Распространяемые компоненты<br/>          | Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                                                         |
| Header<br/>                   | <dl> <dt>Влантипес. h (включение Windot11. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Алгоритм проверки подлинности DOT11 \_**](dot11-auth-algorithm.md)
</dt> <dt>

[**\_Алгоритм шифрования \_ DOT11**](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




