---
description: Представляет маркер для набора устанавливаемых функций идентификатора объекта (OID).
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: ХКРИПТОИДФУНКСЕТ (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437511de32de97d4fb226d299f224427267381ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664118"
---
# <a name="hcryptoidfuncset"></a>хкриптоидфунксет

Тип данных **хкриптоидфунксет** представляет собой маркер набора устанавливаемых функций [*идентификатора объекта*](../secgloss/o-gly.md) (OID). Функции [**криптжетдефаултоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**криптжетоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**криптфриоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)и [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) используют этот тип данных.


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Винкрипт. h</dt> </dl> |



 

 
