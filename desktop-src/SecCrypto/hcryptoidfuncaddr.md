---
description: Представляет обработчик для устанавливаемой функции идентификатора объекта (OID).
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: ХКРИПТОИДФУНКАДДР (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4f083d87234e598e8464491f2968868fa2b3c8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664117"
---
# <a name="hcryptoidfuncaddr"></a>хкриптоидфункаддр

Тип данных **хкриптоидфункаддр** представляет собой описатель для устанавливаемой функции [*идентификатора объекта*](../secgloss/o-gly.md) (OID). Функции [**криптжетдефаултоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**криптжетоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)и [**криптфриоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) , а также [**\_ \_ \_ информационная структура хранилища сертификатов Prov**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) используют этот тип данных.


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Винкрипт. h</dt> </dl> |



 

 
