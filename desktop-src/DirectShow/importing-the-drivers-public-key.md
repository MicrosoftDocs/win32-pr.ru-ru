---
description: Импорт открытого ключа драйверов
ms.assetid: 9bab0e43-6e9f-4cdb-bfd0-cdafcc12d526
title: Импорт открытого ключа драйверов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222b9c62bd9babe0a01a0e6a9b3a50747ab3b039
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894850"
---
# <a name="importing-the-drivers-public-key"></a>Импорт открытого ключа драйверов

Открытый ключ RSA драйвера содержится в тегах модуля и экспоненту конечного узла сертификата. Оба значения кодируются в кодировке Base64 и должны быть декодированы. Если вы используете CryptoAPI Майкрософт, необходимо импортировать ключ в поставщик служб шифрования (CSP), который является модулем, реализующим алгоритмы шифрования.

Чтобы преобразовать модуль и показатель степени из кодировки Base64 в двоичные массивы, используйте функцию **криптстрингтобинари** , как показано в следующем коде. Вызовите функцию один раз, чтобы получить размер массива байтов. Затем выделите буфер и снова вызовите функцию.


```C++
DWORD cbLen = 0, dwSkip = 0, dwFlags = 0;
::CryptStringToBinary(
   pszModulus,  // String that contains the Base64-encoded modulus.
   cchModulus,  // Length of the string, not including the trailing NULL.
   CRYPT_STRING_BASE64,  // Base64 encoding.
   NULL,     // Do not convert yet. Just calculate the length.
   &cbLen,   // Receives the length of the buffer that is required.
   &dwSkip,  // Receives the number of skipped characters.
   &dwFlags  // Receives flags.
);

// Allocate a new buffer.
BYTE *pbBuffer = new BYTE [cbLen];
::CryptStringToBinary(pszModulus, cchModulus, CRYPT_STRING_BASE64, 
    pbBuffer, &cbLen, &dwSkip, &dwFlags);

// (Repeat these steps for the exponent.)
```



Массив в кодировке Base64 находится в порядке с обратным порядком байтов, в то время как интерфейс CryptoAPI ждет число в порядке с прямым порядком байтов, поэтому необходимо поменять порядок байтов массива, возвращаемого из **криптстрингтобинари**. Остаток от деления составляет 256 байт, но декодированный массив байтов может быть меньше 256 байт. В этом случае необходимо выделить новый массив длиной 256 байт, скопировать данные в новый массив и заполнить его передним числом нулями. Экспонента — это значение типа DWORD (4 байта).

После получения значений модуля и экспоненты можно импортировать ключ в стандартный поставщик служб шифрования (CSP), как показано в следующем коде:


```C++
// Assume the following values exist:
BYTE *pModulus;     // Byte array that contains the modulus.
DWORD cbModulus;    // Size of the modulus in bytes.
DWORD dwExponent;   // Exponent.

// Create a new key container to hold the key. 
::CryptAcquireContext(
    &hCSP,         // Receives a handle to the CSP.
    NULL,          // Use the default key container.
    NULL,          // Use the default CSP.
    PROV_RSA_AES,  // Use the AES provider (public-key algorithm).
    CRYPT_SILENT | CRYPT_NEWKEYSET 
);

// Move the key into the key container. 
// The data format is: PUBLICKEYSTRUC + RSAPUBKEY + key
DWORD cbKeyBlob = cbModulus + sizeof(PUBLICKEYSTRUC) + sizeof(RSAPUBKEY)
BYTE *pBlob = new BYTE[cbKeyBlob];

// Fill in the data.
PUBLICKEYSTRUC *pPublicKey = (PUBLICKEYSTRUC*)pBlob;
pPublicKey->bType = PUBLICKEYBLOB; 
pPublicKey->bVersion = CUR_BLOB_VERSION;  // Always use this value.
pPublicKey->reserved = 0;                 // Must be zero.
pPublicKey->aiKeyAlg = CALG_RSA_KEYX;     // RSA public-key key exchange. 

// The next block of data is the RSAPUBKEY structure.
RSAPUBKEY *pRsaPubKey = (RSAPUBKEY*)(pBlob + sizeof(PUBLICKEYSTRUC));
pRsaPubKey->magic = RSA1;            // Public key.
pRsaPubKey->bitlen = cbModulus * 8;  // Number of bits in the modulus.
pRsaPubKey->pubexp = dwExponent;     // Exponent.

// Copy the modulus into the blob. Put the modulus directly after the
// RSAPUBKEY structure in the blob.
BYTE *pKey = (BYTE*)(pRsaPubkey + sizeof(RSAPUBKEY));
CopyMemory(pKey, pModulus, cbModulus);

// Now import the key.
HCRYPTKEY hRSAKey;  // Receives a handle to the key.
CryptImportKey(hCSP, pBlob, cbKeyBlob, 0, 0, &hRSAKey) 
```



Теперь можно использовать интерфейс CryptoAPI для шифрования команд и запросов состояния с помощью открытого ключа драйвера.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование протокола сертифицированной выходной защиты (Копп)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



