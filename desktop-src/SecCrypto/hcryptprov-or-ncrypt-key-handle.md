---
description: Используется в качестве маркера для поставщика служб шифрования CryptoAPI (CSP) или CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982ab2a37c1a2d6035f76cac5c55dcdae44c4cf38f86138c52590c73724b53e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006342"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a>\_ \_ \_ маркер ключа хкриптпров или \_ NCRYPT

Тип **данных \_ \_ \_ \_ обработчика ключа хкриптпров или NCRYPT** используется в качестве маркера для поставщика служб [*шифрования*](../secgloss/c-gly.md) CryptoAPI (CSP) или CNG. Этот обработчик должен быть обработчиком [**хкриптпров**](hcryptprov.md) , созданным с помощью функции [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) или обработчика **\_ ключей \_ NCRYPT** , созданного с помощью функции [**нкриптопенкэй**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) . Новые приложения всегда должны передавать маркер **\_ \_ маркера ключа NCRYPT** в CSP CNG.


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Винкрипт. h</dt> </dl> |



 

 
