---
description: Сообщение о завершении будет отправлено сразу после сообщения Spec (изменение спецификации шифра), чтобы проверить успешность обмена ключами и процессов проверки подлинности.
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: Завершение сообщений в протоколе TLS 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a0f0f3e85916e66d434cb3e69b083348e40143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684098"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a>Завершение сообщений в протоколе TLS 1,0

Сообщение о завершении будет отправлено сразу после сообщения Spec (изменение спецификации шифра), чтобы проверить успешность обмена ключами и процессов проверки подлинности. Сообщения о завершении в протоколе TLS 1,0 вычисляются с помощью [*функции псевдо-Random*](../secgloss/p-gly.md) (PRF) с [*главным ключом*](../secgloss/m-gly.md), меткой и начальным значением в качестве входных данных. PRF создает выходные данные произвольной длины. Следующий метод используется для создания выходных данных PRF, используемых в сообщениях завершения TLS 1,0.

Для создания PRF [*-*](../secgloss/h-gly.md) обработчика используется [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) со значением **\_ идентификатора ALG** , установленным в калг \_ TLS1PRF, и маркером к главному ключу, переданному в параметре *hKey* . Значения меток и начальных значений задаются для хэш-маркера с использованием значений HP \_ TLS1PRF \_ Label и HP \_ TLS1PRF \_ SEED соответственно в параметре *двпарам* с функцией [**криптсесашпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) . Наконец, обработчик протокола вызывает функцию [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) со значением HP \_ хашвал в параметре *ДВПАРАМ* , чтобы извлечь PRF данные, включаемые в сообщение о завершении. При вызове **CryptGetHashParam** механизм протокола должен указать, сколько байт данных PRF будет создавать. Это делается в параметре *пдвдатален* , и результирующие данные помещаются в буфер, на который указывает параметр *pbData* .

Ниже приведен типичный исходный код для этой подсистемы протокола.


```C++
CRYPT_DATA_BLOB Data;
HCRYPTHASH hFinishHash;
BYTE rgbFinishPRF[12];
BYTE rgbCliHashOfHandshakes[36];

//------------------------------------------------------------
// get client finish message

CryptCreateHash(
         hProv, 
         CALG_TLS1PRF, 
         hMasterKey, 
         0, 
         &hFinishHash);

Data.pbData = (BYTE*)"client finished";
Data.cbData = 15;
CryptSetHashParam(
         hFinishHash, 
         HP_TLS1PRF_LABEL, 
         (BYTE*)&Data, 
         0);

Data.pbData = rgbCliHashOfHandshakes;
Data.cbData = sizeof(rgbCliHashOfHandshakes);
CryptSetHashParam(
          hFinishHash, 
          HP_TLS1PRF_SEED, 
          (BYTE*)&Data, 
          0);

cbFinishPRF = sizeof(rgbFinishPRF);
CryptGetHashParam(
          hFinishHash, 
          HP_HASHVAL, 
          rgbFinishPRF, 
          &cbFinishPRF, 
          0);

CryptDestroyHash(hFinishHash);
```



 

 
