---
description: Сведения о создании, обмене, импорте и экспорте ключей Diffie-Hellman.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Ключи Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00eaddd580ac74e18e26498175f87b5d81b8e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350145"
---
# <a name="diffie-hellman-keys"></a>Ключи Diffie-Hellman

-   [Создание ключей Diffie-Hellman](#generating-diffie-hellman-keys)
-   [Обмен ключами Diffie-Hellman](#exchanging-diffie-hellman-keys)
-   [Экспорт Diffie-Hellman закрытого ключа](#exporting-a-diffie-hellman-private-key)
-   [Пример кода](#example-code)

## <a name="generating-diffie-hellman-keys"></a>Создание ключей Diffie-Hellman

Чтобы создать ключ Diffie-Hellman, выполните следующие действия.

1.  Вызовите функцию [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft Diffie-Hellman.
2.  Создайте новый ключ. Это можно сделать двумя способами: выполнив генерацию CryptoAPI всех новых значений для G, P и X или используя существующие значения для G и P и создав новое значение для X.

    **Создание ключа путем создания всех новых значений**

    1.  Вызовите функцию [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , передав **калг \_ DH \_ SF** (Store and Forward) или **калг \_ DH \_ ефем** (эфемерный) в параметре *алгид* . Ключ будет создан с использованием новых случайных значений для G и P, только что вычисленное значение для X, а его маркер будет возвращен в параметре *фкэй* .
    2.  Теперь новый ключ готов к использованию. Значения G и P должны отправляться получателю вместе с ключом (или отсылаться другим методом) при [*обмене ключами*](../secgloss/e-gly.md).

    **Создание ключа с помощью стандартных значений для G и P**

    1.  Вызовите [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , **передав \_ калг \_ DH SF** (хранение и переадресация) или **калг \_ DH \_ ефем** (эфемерный) в параметре *алгид* , а также метод **шифрования \_ прежен** для параметра *dwFlags* . В параметре *фкэй* будет создан и возвращен маркер ключа.
    2.  Инициализируйте [**зашифрованную структуру \_ \_ BLOB-объектов данных**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) , в которой для элемента **pbData** задано значение P. [*BLOB-объект*](../secgloss/b-gly.md) не содержит сведений о заголовках, а элемент **pbData** имеет формат с [*прямым порядком байтов*](../secgloss/l-gly.md) .
    3.  Значение P задается путем вызова функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , передачи маркера ключа, полученного на шаге a, в параметре *hKey* , флага **\_ P ключевого индикатора** в параметре *Двпарам* и указателя на структуру, содержащую значение P в параметре *pbData* .
    4.  Инициализируйте [**зашифрованную структуру \_ \_ BLOB-объектов данных**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) , в которой для элемента **pbData** задано значение G. BLOB-объект не содержит сведений о заголовках, а элемент **pbData** имеет формат с прямым порядком байтов.
    5.  Значение G задается вызовом функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , передачей маркера ключа, полученного на шаге a, в параметре *hKey* , флаг **\_ G** в параметре *Двпарам* и указатель на структуру, содержащую значение G в параметре *pbData* .
    6.  Значение X создается путем вызова функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , передачей маркера ключа, полученного на шаге a, в параметре *hKey* , флаг **\_ X** в параметре *двпарам* и **значение NULL** в параметре *pbData* .
    7.  Если все вызовы функции были выполнены, Diffie-Hellman открытый ключ готов к использованию.

3.  Если ключ больше не нужен, удалите его, передав маркер ключа в функцию [**криптдестройкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .

Если в предыдущих процедурах был указан **калг \_ DH \_ SF** , значения ключей сохраняются в хранилище при каждом вызове функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam). Затем можно получить значения G и P с помощью функции [**криптжеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) . Некоторые поставщики служб шифрования могут иметь жестко запрограммированные значения G и P. В этом случае возникнет ошибка **\_ фикседпараметер** , если метод **криптсеткэйпарам** вызывается с помощью **ключевого индикатора \_ G** или **ключевого индикатора \_ P** , указанного в параметре *двпарам* . Если вызывается **криптдестройкэй** , маркер ключа уничтожается, но значения ключа сохраняются в CSP. Однако если **калг \_ DH \_ ефем** был указан, то маркер ключа уничтожается, и все значения удаляются из CSP.

## <a name="exchanging-diffie-hellman-keys"></a>Обмен ключами Diffie-Hellman

Целью алгоритма Diffie-Hellman является возможность создания и совместного использования идентичного секретного ключа сеанса двумя или более сторонами путем предоставления общего доступа к информации по незащищенной сети. Общие сведения о сети находятся в виде пары значений констант и Diffie-Hellman открытого ключа. Ниже приведены процессы, используемые двумя сторонами обмена ключами.

-   Обе стороны согласны с Diffie-Hellmanными параметрами, которые являются простыми числами (P) и номером генератора (G).
-   Сторона 1 отправляет свой Diffie-Hellman открытый ключ в сторону 2.
-   Сторона 2 рассчитывает секретный ключ сеанса, используя сведения, содержащиеся в его закрытом ключе и открытом ключе.
-   Сторона 2 отправляет свой Diffie-Hellman открытый ключ в сторону 1.
-   Сторона 1 рассчитывает секретный ключ сеанса, используя сведения, содержащиеся в его закрытом ключе и открытом ключе.
-   Обе стороны теперь имеют одинаковый сеансовый ключ, который можно использовать для шифрования и расшифровки данных. Шаги, необходимые для этого, показаны в следующей процедуре.

**Подготовка Diffie-Hellman открытого ключа к передаче**

1.  Вызовите функцию [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft Diffie-Hellman.
2.  Создайте ключ Diffie-Hellman, вызвав функцию [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) для создания нового ключа или вызвав функцию [**криптжетусеркэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) для получения существующего ключа.
3.  Получите размер, необходимый для хранения большого двоичного объекта Diffie-Hellman Key, вызвав [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), передав **значение NULL** для параметра *pbData* . Требуемый размер будет возвращен в *пдвдатален*.
4.  Выделение памяти для большого двоичного объекта ключа.
5.  Создайте Diffie-Hellman [*большой двоичный объект открытого ключа*](../secgloss/p-gly.md) , вызвав функцию [**Криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , передав **публиккэйблоб** в параметре *двблобтипе* и в качестве ключа в Diffie-Hellman ключ в параметре *hKey* . Этот вызов функции вызывает вычисление значения открытого ключа (G ^ X) mod P.
6.  Если все предыдущие вызовы функций были успешными, Diffie-Hellman большой двоичный объект открытого ключа теперь готов для кодирования и передачи.

**Импорт Diffie-Hellman открытого ключа и вычисление секретного ключа сеанса**

1.  Вызовите функцию [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft Diffie-Hellman.
2.  Создайте ключ Diffie-Hellman, вызвав функцию [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) для создания нового ключа или вызвав функцию [**криптжетусеркэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) для получения существующего ключа.
3.  Чтобы импортировать Diffie-Hellman открытый ключ в CSP, вызовите функцию [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , передав указатель на большой двоичный объект открытого ключа в параметре *pbData* , длину большого двоичного объекта в параметре *двдатален* и указатель на Diffie-Hellman ключ в параметре *хпубкэй* . Это приводит к выполнению вычислений (Y ^ X) mod P, что создает общий секретный ключ и завершает [*Обмен ключами*](../secgloss/e-gly.md). Этот вызов функции возвращает маркер нового секретного ключа сеанса в параметре *hKey* .
4.  На этом этапе импортированный Diffie-Hellman имеет тип **калг \_ агридкэй \_ ANY**. Прежде чем ключ можно будет использовать, его необходимо преобразовать в тип ключа сеанса. Это достигается путем вызова функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) с параметром *двпарам* , установленным в **ключевое \_ алгид** , а *pbData* — указателем на значение [**\_ идентификатора ALG**](alg-id.md) , представляющее ключ сеанса, например **калг \_ RC4**. Перед использованием общего ключа в функции [**криптенкрипт**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) или [**криптдекрипт**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) необходимо преобразовать ключ. Вызовы любой из этих функций до преобразования типа ключа завершатся ошибкой.
5.  Секретный ключ сеанса теперь готов к использованию для шифрования или расшифровки.
6.  Если ключ больше не нужен, удалите его, вызвав функцию [**криптдестройкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .

## <a name="exporting-a-diffie-hellman-private-key"></a>Экспорт Diffie-Hellman закрытого ключа

Чтобы экспортировать Diffie-Hellman закрытый ключ, выполните следующие действия.

1.  Вызовите функцию [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft Diffie-Hellman.
2.  Создайте ключ Diffie-Hellman, вызвав функцию [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) для создания нового ключа или вызвав функцию [**криптжетусеркэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) для получения существующего ключа.
3.  Создайте Diffie-Hellman [*большой двоичный объект закрытого ключа*](../secgloss/p-gly.md) , вызвав функцию [**Криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , передав **приватекэйблоб** в параметре *двблобтипе* и маркер в ключ Diffie-Hellman в параметре *hKey* .
4.  Если маркер ключа больше не нужен, вызовите функцию [**криптдестройкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) для уничтожения маркера ключа.

## <a name="example-code"></a>Пример кода

В следующем примере показано, как создать, экспортировать, импортировать и использовать ключ Diffie-Hellman для выполнения обмена ключами.


```C++
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// The key size, in bits.
#define DHKEYSIZE 512

// Prime in little-endian format.
static const BYTE g_rgbPrime[] = 
{
    0x91, 0x02, 0xc8, 0x31, 0xee, 0x36, 0x07, 0xec, 
    0xc2, 0x24, 0x37, 0xf8, 0xfb, 0x3d, 0x69, 0x49, 
    0xac, 0x7a, 0xab, 0x32, 0xac, 0xad, 0xe9, 0xc2, 
    0xaf, 0x0e, 0x21, 0xb7, 0xc5, 0x2f, 0x76, 0xd0, 
    0xe5, 0x82, 0x78, 0x0d, 0x4f, 0x32, 0xb8, 0xcb,
    0xf7, 0x0c, 0x8d, 0xfb, 0x3a, 0xd8, 0xc0, 0xea, 
    0xcb, 0x69, 0x68, 0xb0, 0x9b, 0x75, 0x25, 0x3d,
    0xaa, 0x76, 0x22, 0x49, 0x94, 0xa4, 0xf2, 0x8d 
};

// Generator in little-endian format.
static BYTE g_rgbGenerator[] = 
{
    0x02, 0x88, 0xd7, 0xe6, 0x53, 0xaf, 0x72, 0xc5,
    0x8c, 0x08, 0x4b, 0x46, 0x6f, 0x9f, 0x2e, 0xc4,
    0x9c, 0x5c, 0x92, 0x21, 0x95, 0xb7, 0xe5, 0x58, 
    0xbf, 0xba, 0x24, 0xfa, 0xe5, 0x9d, 0xcb, 0x71, 
    0x2e, 0x2c, 0xce, 0x99, 0xf3, 0x10, 0xff, 0x3b,
    0xcb, 0xef, 0x6c, 0x95, 0x22, 0x55, 0x9d, 0x29,
    0x00, 0xb5, 0x4c, 0x5b, 0xa5, 0x63, 0x31, 0x41,
    0x13, 0x0a, 0xea, 0x39, 0x78, 0x02, 0x6d, 0x62
};

BYTE g_rgbData[] = {0x01, 0x02, 0x03, 0x04,    0x05, 0x06, 0x07, 0x08};

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    BOOL fReturn;
    HCRYPTPROV hProvParty1 = NULL; 
    HCRYPTPROV hProvParty2 = NULL; 
    DATA_BLOB P;
    DATA_BLOB G;
    HCRYPTKEY hPrivateKey1 = NULL;
    HCRYPTKEY hPrivateKey2 = NULL;
    PBYTE pbKeyBlob1 = NULL;
    PBYTE pbKeyBlob2 = NULL;
    HCRYPTKEY hSessionKey1 = NULL;
    HCRYPTKEY hSessionKey2 = NULL;
    PBYTE pbData = NULL;

    /************************
    Construct data BLOBs for the prime and generator. The P and G 
    values, represented by the g_rgbPrime and g_rgbGenerator arrays 
    respectively, are shared values that have been agreed to by both 
    parties.
    ************************/
    P.cbData = DHKEYSIZE/8;
    P.pbData = (BYTE*)(g_rgbPrime);

    G.cbData = DHKEYSIZE/8;
    G.pbData = (BYTE*)(g_rgbGenerator);

    /************************
    Create the private Diffie-Hellman key for party 1. 
    ************************/
    // Acquire a provider handle for party 1.
    fReturn = CryptAcquireContext(
        &hProvParty1, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 1.
    fReturn = CryptGenKey(
        hProvParty1, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Create the private Diffie-Hellman key for party 2. 
    ************************/
    // Acquire a provider handle for party 2.
    fReturn = CryptAcquireContext(
        &hProvParty2, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 2.
    fReturn = CryptGenKey(
        hProvParty2, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 1's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen1;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob1 = (PBYTE)malloc(dwDataLen1)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob1,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 2's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen2;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob2 = (PBYTE)malloc(dwDataLen2)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob2,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Party 1 imports party 2's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty1,
        pbKeyBlob2,
        dwDataLen2,
        hPrivateKey1,
        0,
        &hSessionKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }
    
    /************************
    Party 2 imports party 1's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty2,
        pbKeyBlob1,
        dwDataLen1,
        hPrivateKey2,
        0,
        &hSessionKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Convert the agreed keys to symmetric keys. They are currently of 
    the form CALG_AGREEDKEY_ANY. Convert them to CALG_RC4.
    ************************/
    ALG_ID Algid = CALG_RC4;

    // Enable the party 1 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey1,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Enable the party 2 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey2,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Encrypt some data with party 1's session key. 
    ************************/
    // Get the size.
    DWORD dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        NULL, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate a buffer to hold the encrypted data.
    pbData = (PBYTE)malloc(dwLength);
    if(!pbData)
    {
        goto ErrorExit;
    }

    // Copy the unencrypted data to the buffer. The data will be 
    // encrypted in place.
    memcpy(pbData, g_rgbData, sizeof(g_rgbData)); 

    // Encrypt the data.
    dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        pbData, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }
  
    /************************
    Decrypt the data with party 2's session key. 
    ************************/
    dwLength = sizeof(g_rgbData);
    fReturn = CryptDecrypt(
        hSessionKey2,
        0,
        TRUE,
        0,
        pbData,
        &dwLength);
    if(!fReturn)
    {
        goto ErrorExit;
    }


ErrorExit:
    if(pbData)
    {
        free(pbData);
        pbData = NULL;
    }

    if(hSessionKey2)
    {
        CryptDestroyKey(hSessionKey2);
        hSessionKey2 = NULL;
    }

    if(hSessionKey1)
    {
        CryptDestroyKey(hSessionKey1);
        hSessionKey1 = NULL;
    }

    if(pbKeyBlob2)
    {
        free(pbKeyBlob2);
        pbKeyBlob2 = NULL;
    }

    if(pbKeyBlob1)
    {
        free(pbKeyBlob1);
        pbKeyBlob1 = NULL;
    }

    if(hPrivateKey2)
    {
        CryptDestroyKey(hPrivateKey2);
        hPrivateKey2 = NULL;
    }

    if(hPrivateKey1)
    {
        CryptDestroyKey(hPrivateKey1);
        hPrivateKey1 = NULL;
    }

    if(hProvParty2)
    {
        CryptReleaseContext(hProvParty2, 0);
        hProvParty2 = NULL;
    }

    if(hProvParty1)
    {
        CryptReleaseContext(hProvParty1, 0);
        hProvParty1 = NULL;
    }

    return 0;
}
```



 

 
