---
description: Поддерживаемые протоколы и комплекты шифров могут быть перечислены вызовами Криптжетпровпарам с PP \_ енумалгс или PP \_ енумалгс \_ ex.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Перечисление поддерживаемых протоколов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662856"
---
# <a name="enumerating-supported-protocols"></a>Перечисление поддерживаемых протоколов

Поддерживаемые протоколы и комплекты шифров могут быть перечислены вызовами [**криптжетпровпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) с PP \_ енумалгс или PP \_ енумалгс \_ ex. Значение PP \_ енумалгс \_ ex работает так же, как PP \_ енумалгс, но возвращает структуру [**Prov \_ енумалгс \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) , содержащую более обширную информацию о алгоритмах, поддерживаемых поставщиком.

Дополнительные сведения об определенных флагах протокола и их значениях см. в разделе [флаги протокола](protocol-flags.md).

Учитывая, что элемент **хкриптпров** является [*маркером*](../secgloss/h-gly.md) открытого криптографического [*контекста*](../secgloss/c-gly.md) , полученного с помощью [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) с параметром *двпровтипе* , имеющим значение Prov \_ RSA \_ SChannel, в следующем примере перечисляются имена всех алгоритмов, доступных в CSP.


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



В следующей таблице перечислены некоторые алгоритмы, возвращаемые обычным внутренним \_ CSP Prov RSA \_ SChannel. Обратите внимание, что в этом примере CSP не поддерживает шифрование SHA Макинтош и SSL2 DES.



| Идентификатор алгоритма                                                                        | Минимальная длина ключа | Максимальная длина ключа | Протоколы | Имя алгоритма |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [*КАЛГ \_ RSA \_ KEYX*](../secgloss/c-gly.md) | 512                | 2048               | 0x0007    | "RSA \_ KEYX"    |
| [*\_MD5 калг*](../secgloss/c-gly.md)                 | 128                | 128                | 0x0007    | MD5          |
| [*\_SHA калг*](../secgloss/c-gly.md)                 | 160                | 160                | 0x0005    | ХЭШ          |
| [*КАЛГ \_ RC4*](../secgloss/c-gly.md)                 | 40                 | 128                | 0x0007    | RC4          |
| КАЛГ \_ des                                                                                   | 56                 | 56                 | 0x0005    | 3DES          |



 

Чтобы подготовиться к отправке сообщений Клиенселло или Серверхелло, механизм протокола [*SChannel*](../secgloss/s-gly.md) перечисляет алгоритмы и размеры ключей, поддерживаемые CSP, и создает список, который является внутренним набором поддерживаемых комплектов шифров.

 

 
