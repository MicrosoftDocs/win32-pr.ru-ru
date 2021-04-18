---
description: Используется в качестве маркера для поставщика служб шифрования CryptoAPI (CSP) или CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664116"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a>\_ \_ \_ маркер ключа хкриптпров или \_ NCRYPT

Тип **данных \_ \_ \_ \_ обработчика ключа хкриптпров или NCRYPT** используется в качестве маркера для поставщика служб [*шифрования*](../secgloss/c-gly.md) CryptoAPI (CSP) или CNG. Этот обработчик должен быть обработчиком [**хкриптпров**](hcryptprov.md) , созданным с помощью функции [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) или обработчика **\_ ключей \_ NCRYPT** , созданного с помощью функции [**нкриптопенкэй**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) . Новые приложения всегда должны передавать маркер **\_ \_ маркера ключа NCRYPT** в CSP CNG.


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Винкрипт. h</dt> </dl> |



 

 
