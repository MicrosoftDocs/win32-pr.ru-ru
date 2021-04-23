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
# <a name="deriving-bulk-encryption-and-mac-keys"></a><span data-ttu-id="7d724-103">Создание производного шифрования и ключей MAC</span><span class="sxs-lookup"><span data-stu-id="7d724-103">Deriving Bulk Encryption and MAC Keys</span></span>

<span data-ttu-id="7d724-104">[*Групповое шифрование*](../secgloss/b-gly.md) и [*ключи Mac*](../secgloss/m-gly.md) являются производными от [*главного ключа*](../secgloss/m-gly.md) , но могут включать другие источники в зависимости от используемого протокола и набора шифров.</span><span class="sxs-lookup"><span data-stu-id="7d724-104">[*Bulk encryption*](../secgloss/b-gly.md) and [*MAC keys*](../secgloss/m-gly.md) are derived from a [*master key*](../secgloss/m-gly.md) but can include other sources depending on the protocol and cipher suite used.</span></span>

<span data-ttu-id="7d724-105">Процесс создания производного шифрования и ключей MAC одинаков для клиента и сервера:</span><span class="sxs-lookup"><span data-stu-id="7d724-105">The process of deriving bulk encryption and MAC keys is the same for both client and server:</span></span>

1.  <span data-ttu-id="7d724-106">Ядро протокола вызывает [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) в главном ключе один или несколько раз, чтобы предоставить CSP сведения, необходимые для создания ключей.</span><span class="sxs-lookup"><span data-stu-id="7d724-106">The protocol engine calls [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) on the master key one or more times to provide the CSP with the information needed to build the keys.</span></span>
2.  <span data-ttu-id="7d724-107">Поскольку ключи [*CryptoAPI*](../secgloss/c-gly.md) не могут быть получены непосредственно из других ключей, хэш-объект создается из главного ключа с помощью [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="7d724-107">Because [*CryptoAPI*](../secgloss/c-gly.md) keys cannot be derived directly from other keys, a hash object is created from the master key using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="7d724-108">Этот [*хэш*](../secgloss/h-gly.md) используется для создания новых ключей.</span><span class="sxs-lookup"><span data-stu-id="7d724-108">This [*hash*](../secgloss/h-gly.md) is used to create the new keys.</span></span>
3.  <span data-ttu-id="7d724-109">Два ключа шифрования и два ключа для MAC создаются из объекта "основной хэш" с помощью четырех вызовов [**криптдеривекэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).</span><span class="sxs-lookup"><span data-stu-id="7d724-109">The two bulk encryption keys and the two MAC keys are created from the "master hash" object using four calls to [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).</span></span>

> [!Note]
> <span data-ttu-id="7d724-110">При выполнении повторного подключения SSL механизм протокола может выполнить описанную выше процедуру несколько раз с помощью одного и того же главного ключа.</span><span class="sxs-lookup"><span data-stu-id="7d724-110">When performing SSL reconnects, a protocol engine can perform the above procedure several times using the same master key.</span></span> <span data-ttu-id="7d724-111">Это позволяет клиенту и серверу иметь несколько, часто одновременные подключения, каждый из которых использует различные операции [*шифрования*](../secgloss/b-gly.md) и ключи Mac без дополнительных операций RSA или Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="7d724-111">This enables the client and server to have multiple, often simultaneous connections, each using different [*Bulk encryption*](../secgloss/b-gly.md) and MAC keys without additional RSA or Diffie-Hellman operations.</span></span>
> 
> <span data-ttu-id="7d724-112">Все CSP должны использовать хорошие потокобезопасные методики.</span><span class="sxs-lookup"><span data-stu-id="7d724-112">All CSPs must use good thread-safe practices.</span></span> <span data-ttu-id="7d724-113">Число потоков, равное нескольким десяткам, не является необычным.</span><span class="sxs-lookup"><span data-stu-id="7d724-113">Thread counts of several dozen are not unusual.</span></span>

 

<span data-ttu-id="7d724-114">Ниже приведен типичный исходный код для механизма протокола.</span><span class="sxs-lookup"><span data-stu-id="7d724-114">The following is typical source code for the protocol engine:</span></span>


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



 

 
