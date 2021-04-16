---
description: Групповое шифрование и ключи MAC являются производными от главного ключа, но могут включать другие источники в зависимости от используемого протокола и набора шифров.
ms.assetid: f78acb54-c32a-46a8-b465-855251069a57
title: Создание производного шифрования и ключей MAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cbf216fd850c7b98c638d4fdc10a84087d91ac
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105664845"
---
# <a name="deriving-bulk-encryption-and-mac-keys"></a>Создание производного шифрования и ключей MAC

[*Групповое шифрование*](../secgloss/b-gly.md) и [*ключи Mac*](../secgloss/m-gly.md) являются производными от [*главного ключа*](../secgloss/m-gly.md) , но могут включать другие источники в зависимости от используемого протокола и набора шифров.

Процесс создания производного шифрования и ключей MAC одинаков для клиента и сервера:

1.  Ядро протокола вызывает [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) в главном ключе один или несколько раз, чтобы предоставить CSP сведения, необходимые для создания ключей.
2.  Поскольку ключи [*CryptoAPI*](../secgloss/c-gly.md) не могут быть получены непосредственно из других ключей, хэш-объект создается из главного ключа с помощью [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Этот [*хэш*](../secgloss/h-gly.md) используется для создания новых ключей.
3.  Два ключа шифрования и два ключа для MAC создаются из объекта "основной хэш" с помощью четырех вызовов [**криптдеривекэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).

> [!Note]
> При выполнении повторного подключения SSL механизм протокола может выполнить описанную выше процедуру несколько раз с помощью одного и того же главного ключа. Это позволяет клиенту и серверу иметь несколько, часто одновременные подключения, каждый из которых использует различные операции [*шифрования*](../secgloss/b-gly.md) и ключи Mac без дополнительных операций RSA или Diffie-Hellman.
> 
> Все CSP должны использовать хорошие потокобезопасные методики. Число потоков, равное нескольким десяткам, не является необычным.

 

Ниже приведен типичный исходный код для механизма протокола.


```C++
//--------------------------------------------------------------------
//   Define and initialize local variables.

BOOL fClient = <TRUE if this is code for the client?>;
CRYPT_DATA_BLOB Data;
HCRYPTHASH hMasterHash;

//--------------------------------------------------------------------
// Finish creating the master_secret.

switch(<protocol being used>)
{
    case <PCT 1.0>:

//------------------------------------------------------------
// Specify clear key value.

        Data.pbData = pClearKey;
        Data.cbData = cbClearKey;
        CryptSetKeyParam(
                   hMasterKey, 
                   KP_CLEAR_KEY, 
                   (PBYTE)&Data, 
                   0);

//------------------------------------------------------------
// Specify the CH_CHALLENGE_DATA.

        Data.pbData = pChallenge;
        Data.cbData = cbChallenge;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_CLIENT_RANDOM, 
                    (PBYTE)&Data, 
                    0);

//------------------------------------------------------------
// Specify the SH_CONNECTION_ID_DATA.

        Data.pbData = pConnectionID;
        Data.cbData = cbConnectionID;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_SERVER_RANDOM, 
                    (PBYTE)&Data, 
                    0);

//------------------------------------------------------------
// Specify the SH_CERTIFICATE_DATA.
        Data.pbData = pbServerCertificate;
        Data.cbData = cbServerCertificate;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_CERTIFICATE, 
                    (PBYTE)&Data, 
                    0);
        break;

    case <SSL 2.0>:

//------------------------------------------------------------
// Specify clear key value.

        Data.pbData = pClearKey;
        Data.cbData = cbClearKey;
        CryptSetKeyParam(
                 hMasterKey, 
                 KP_CLEAR_KEY, 
                 (PBYTE)&Data, 
                 0);

//------------------------------------------------------------
// Specify the CH_CHALLENGE_DATA.

        Data.pbData = pChallenge;
        Data.cbData = cbChallenge;
        CryptSetKeyParam(
                 hMasterKey, 
                 KP_CLIENT_RANDOM,
                 (BYTE*)&Data, 
                 0);

//------------------------------------------------------------
// Specify the SH_CONNECTION_ID_DATA.

        Data.pbData = pConnectionID;
        Data.cbData = cbConnectionID;
        CryptSetKeyParam(
                   hMasterKey, 
                   KP_SERVER_RANDOM,
                   (BYTE*)&Data, 
                   0);
        break;

case <SSL 3.0>:
case <TLS 1.0>:


//------------------------------------------------------------
// Specify client_random.

        Data.pbData = pClientRandom;
        Data.cbData = cbClientRandom;
        CryptSetKeyParam(
                hMasterKey, 
                KP_CLIENT_RANDOM, 
                (PBYTE)&Data, 
                 0);

//------------------------------------------------------------
// Specify server_random.

        Data.pbData = pServerRandom;
        Data.cbData = cbServerRandom;
        CryptSetKeyParam(
                  hMasterKey, 
                  KP_SERVER_RANDOM, 
                  (PBYTE)&Data, 
                  0);
}

//------------------------------------------------------------
// Create the master hash object from the master key.

CryptCreateHash(
            hProv, 
            CALG_SCHANNEL_MASTER_HASH,
            hMasterKey, 
            0, 
            &hMasterHash);

//------------------------------------------------------------
// Derive read key from the master hash object.

CryptDeriveKey(hProv, 
               CALG_SCHANNEL_ENC_KEY, 
               hMasterHash,
               fClient ? CRYPT_SERVER : 0,
               &hReadKey);

//------------------------------------------------------------
// Derive write key from the master hash object.

CryptDeriveKey(
           hProv,
           CALG_SCHANNEL_ENC_KEY,
           hMasterHash,
           fClient ? 0 : CRYPT_SERVER,
           &hWriteKey);

if(<protocol being used> != <SSL 2.0>)   // for SSL 2.0, the master 
                                         // key is also the MAC.
{
//------------------------------------------------------------
// Derive read MAC from the master hash object.

    CryptDeriveKey(
              hProv,
              CALG_SCHANNEL_MAC_KEY,
              hMasterHash,
              fClient ? CRYPT_SERVER : 0,
              &hReadMAC);

//------------------------------------------------------------
// Derive write MAC from the master hash object.

    CryptDeriveKey(
             hProv,
             CALG_SCHANNEL_MAC_KEY,
             hMasterHash,
             fClient ? 0 : CRYPT_SERVER,
             &hWriteMAC);
}

CryptDestroyHash(hMasterHash);
```



 

 
