---
description: Базовый поставщик, надежный поставщик и Улучшенный поставщик используют одинаковые ключевые BLOB-объекты.
ms.assetid: f1bd347b-33bd-40bc-9a9b-c06f264f1af4
title: Большие двоичные объекты расширенного поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f693fd469a1df2e76078e61bb69c90ea5d5041d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664135"
---
# <a name="enhanced-provider-key-blobs"></a><span data-ttu-id="16800-103">Большие двоичные объекты расширенного поставщика</span><span class="sxs-lookup"><span data-stu-id="16800-103">Enhanced Provider Key BLOBs</span></span>

<span data-ttu-id="16800-104">Базовый поставщик, надежный поставщик и Улучшенный поставщик используют одинаковые [*Ключевые BLOB-объекты*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="16800-104">The Base Provider, Strong Provider, and Enhanced Provider use the same [*key BLOBs*](../secgloss/k-gly.md).</span></span>

-   [<span data-ttu-id="16800-105">BLOB-объекты открытого ключа</span><span class="sxs-lookup"><span data-stu-id="16800-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="16800-106">BLOB-объекты закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="16800-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="16800-107">Простые ключевые BLOB-объекты</span><span class="sxs-lookup"><span data-stu-id="16800-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="16800-108">BLOB-объекты открытого ключа</span><span class="sxs-lookup"><span data-stu-id="16800-108">Public Key BLOBs</span></span>

<span data-ttu-id="16800-109">[*BLOB-объекты открытого ключа*](../secgloss/p-gly.md), тип **публиккэйблоб**, используются для хранения [*открытых ключей*](../secgloss/p-gly.md) за пределами [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="16800-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md) outside a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="16800-110">Большие двоичные объекты открытого ключа поставщика имеют следующий формат.</span><span class="sxs-lookup"><span data-stu-id="16800-110">Extended provider public key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="16800-111">В следующей таблице описаны все компоненты открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="16800-111">The following table describes each public key component.</span></span> <span data-ttu-id="16800-112">Все значения представлены в формате с [*прямым порядком байтов*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="16800-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="16800-113">Поле</span><span class="sxs-lookup"><span data-stu-id="16800-113">Field</span></span>          | <span data-ttu-id="16800-114">Описание</span><span class="sxs-lookup"><span data-stu-id="16800-114">Description</span></span>                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16800-115">остатка от деления</span><span class="sxs-lookup"><span data-stu-id="16800-115">modulus</span></span>        | <span data-ttu-id="16800-116">Данные модуля открытого ключа находятся непосредственно после структуры [**рсапубкэй**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="16800-116">The public key modulus data is located directly after the [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="16800-117">Размер этих данных зависит от размера открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="16800-117">The size of this data will vary, depending on the size of the public key.</span></span> <span data-ttu-id="16800-118">Число байтов может быть определено путем деления значения поля **рсапубкэй битлен** на восемь.</span><span class="sxs-lookup"><span data-stu-id="16800-118">The number of bytes can be determined by dividing the value of the **RSAPUBKEY bitlen** field by eight.</span></span> |
| <span data-ttu-id="16800-119">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="16800-119">publickeystruc</span></span> | <span data-ttu-id="16800-120">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="16800-120">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="16800-121">рсапубкэй</span><span class="sxs-lookup"><span data-stu-id="16800-121">rsapubkey</span></span>      | <span data-ttu-id="16800-122">Структура [**рсапубкэй**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="16800-122">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="16800-123">**Фокусный** элемент должен иметь значение 0x31415352.</span><span class="sxs-lookup"><span data-stu-id="16800-123">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="16800-124">Это шестнадцатеричное значение является кодировкой [*ASCII*](../secgloss/a-gly.md) для RSA1.</span><span class="sxs-lookup"><span data-stu-id="16800-124">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="16800-125">Большие двоичные объекты с открытым ключом не шифруются.</span><span class="sxs-lookup"><span data-stu-id="16800-125">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="16800-126">Они содержат открытые ключи в виде открытого [*текста*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="16800-126">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="16800-127">BLOB-объекты закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="16800-127">Private Key BLOBs</span></span>

<span data-ttu-id="16800-128">[*BLOB-объекты с закрытыми ключами*](../secgloss/p-gly.md)типа **приватекэйблоб** используются для хранения [*закрытых ключей*](../secgloss/p-gly.md) за пределами CSP.</span><span class="sxs-lookup"><span data-stu-id="16800-128">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*private keys*](../secgloss/p-gly.md) outside a CSP.</span></span> <span data-ttu-id="16800-129">Большие двоичные объекты с закрытым ключом поставщика имеют следующий формат.</span><span class="sxs-lookup"><span data-stu-id="16800-129">Extended provider private key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="16800-130">В следующей таблице описывается компонент BLOB-объекта закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="16800-130">The following table describes the private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="16800-131">Эти поля соответствуют полям, описанным в разделе 7,2 [*стандарта криптографии с открытым ключом*](../secgloss/p-gly.md) (PKCS) \# 1 с незначительными отличиями.</span><span class="sxs-lookup"><span data-stu-id="16800-131">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="16800-132">Поле</span><span class="sxs-lookup"><span data-stu-id="16800-132">Field</span></span>           | <span data-ttu-id="16800-133">Описание</span><span class="sxs-lookup"><span data-stu-id="16800-133">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16800-134">части</span><span class="sxs-lookup"><span data-stu-id="16800-134">coefficient</span></span>     | <span data-ttu-id="16800-135">Части.</span><span class="sxs-lookup"><span data-stu-id="16800-135">Coefficient.</span></span> <span data-ttu-id="16800-136">Оно имеет числовое значение (обратная часть q) mod p.</span><span class="sxs-lookup"><span data-stu-id="16800-136">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                                                |
| <span data-ttu-id="16800-137">exponent1</span><span class="sxs-lookup"><span data-stu-id="16800-137">exponent1</span></span>       | <span data-ttu-id="16800-138">Показатель степени 1.</span><span class="sxs-lookup"><span data-stu-id="16800-138">Exponent 1.</span></span> <span data-ttu-id="16800-139">Оно имеет числовое значение d Mod (p – 1).</span><span class="sxs-lookup"><span data-stu-id="16800-139">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="16800-140">exponent2</span><span class="sxs-lookup"><span data-stu-id="16800-140">exponent2</span></span>       | <span data-ttu-id="16800-141">Экспонента 2.</span><span class="sxs-lookup"><span data-stu-id="16800-141">Exponent 2.</span></span> <span data-ttu-id="16800-142">Оно имеет числовое значение d Mod (q – 1).</span><span class="sxs-lookup"><span data-stu-id="16800-142">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="16800-143">Modulus</span><span class="sxs-lookup"><span data-stu-id="16800-143">Modulus</span></span>         | <span data-ttu-id="16800-144">Модуль.</span><span class="sxs-lookup"><span data-stu-id="16800-144">The modulus.</span></span> <span data-ttu-id="16800-145">Он имеет значение *Prime1*×*Prime2* и часто называется n.</span><span class="sxs-lookup"><span data-stu-id="16800-145">This has a value of *Prime1*×*Prime2* and is often known as n.</span></span>                                                                                                                                   |
| <span data-ttu-id="16800-146">prime1</span><span class="sxs-lookup"><span data-stu-id="16800-146">prime1</span></span>          | <span data-ttu-id="16800-147">Простое число 1, которое часто называют p.</span><span class="sxs-lookup"><span data-stu-id="16800-147">Prime number 1, often known as p.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="16800-148">prime2</span><span class="sxs-lookup"><span data-stu-id="16800-148">prime2</span></span>          | <span data-ttu-id="16800-149">Простое число 2, которое часто называют q.</span><span class="sxs-lookup"><span data-stu-id="16800-149">Prime number 2, often known as q.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="16800-150">приватикспонент</span><span class="sxs-lookup"><span data-stu-id="16800-150">privateExponent</span></span> | <span data-ttu-id="16800-151">Закрытый показатель степени, часто известный как d.</span><span class="sxs-lookup"><span data-stu-id="16800-151">Private exponent, often known as d.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="16800-152">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="16800-152">publickeystruc</span></span>  | <span data-ttu-id="16800-153">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="16800-153">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="16800-154">рсапубкэй</span><span class="sxs-lookup"><span data-stu-id="16800-154">rsapubkey</span></span>       | <span data-ttu-id="16800-155">Структура [**рсапубкэй**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="16800-155">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="16800-156">**Фокусный** элемент должен иметь значение 0x32415352.</span><span class="sxs-lookup"><span data-stu-id="16800-156">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="16800-157">Это шестнадцатеричное значение является кодировкой [*ASCII*](../secgloss/a-gly.md) для RSA2.</span><span class="sxs-lookup"><span data-stu-id="16800-157">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="16800-158">Большие двоичные объекты с закрытыми ключами не шифруются.</span><span class="sxs-lookup"><span data-stu-id="16800-158">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="16800-159">Они содержат закрытые ключи в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="16800-159">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="16800-160">При вызове [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)разработчик может выбрать, следует ли шифровать ключ.</span><span class="sxs-lookup"><span data-stu-id="16800-160">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="16800-161">**Приватекэйблоб** шифруется, если параметр *хекспкэй* содержит допустимый маркер для ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="16800-161">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="16800-162">Все, кроме [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) части большого двоичного объекта, шифруется.</span><span class="sxs-lookup"><span data-stu-id="16800-162">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="16800-163">Параметры алгоритма шифрования и ключа шифрования не сохраняются вместе с BLOB-объектом закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="16800-163">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="16800-164">Приложение должно управлять и хранить эти сведения.</span><span class="sxs-lookup"><span data-stu-id="16800-164">The application must manage and store this information.</span></span> <span data-ttu-id="16800-165">Если для *хекспкэй* передается ноль, закрытый ключ будет экспортирован без шифрования.</span><span class="sxs-lookup"><span data-stu-id="16800-165">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="16800-166">Экспортировать закрытые ключи без шифрования небезопасно, так как они уязвимы для перехвата и использования неавторизованными сущностями.</span><span class="sxs-lookup"><span data-stu-id="16800-166">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="16800-167">Простые ключевые BLOB-объекты</span><span class="sxs-lookup"><span data-stu-id="16800-167">Simple Key BLOBs</span></span>

<span data-ttu-id="16800-168">[*Простые ключевые BLOB-объекты*](../secgloss/s-gly.md)типа **симплеблоб** используются для хранения и передачи ключей сеанса за пределами CSP.</span><span class="sxs-lookup"><span data-stu-id="16800-168">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys outside a CSP.</span></span> <span data-ttu-id="16800-169">Большие двоичные объекты с простыми ключами поставщика всегда шифруются с помощью [*открытого ключа обмена ключами*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="16800-169">Extended provider simple key BLOBs are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="16800-170">Элемент **pbData** в **симплеблоб** представляет собой последовательность байтов в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="16800-170">The **pbData** member of the **SIMPLEBLOB** is a sequence of bytes in the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="16800-171">В следующей таблице описаны все компоненты элемента **pbData** в **симплеблоб**.</span><span class="sxs-lookup"><span data-stu-id="16800-171">The following table describes each component of the **pbData** member of the **SIMPLEBLOB**.</span></span>



| <span data-ttu-id="16800-172">Поле</span><span class="sxs-lookup"><span data-stu-id="16800-172">Field</span></span>          | <span data-ttu-id="16800-173">Описание</span><span class="sxs-lookup"><span data-stu-id="16800-173">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16800-174">алгид</span><span class="sxs-lookup"><span data-stu-id="16800-174">algid</span></span>          | <span data-ttu-id="16800-175">Структура [**\_ идентификаторов ALG**](alg-id.md) , указывающая алгоритм шифрования, используемый для шифрования данных ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="16800-175">An [**ALG\_ID**](alg-id.md) structure that specifies the encryption algorithm used to encrypt the session key data.</span></span> <span data-ttu-id="16800-176">Обычно это имеет значение КАЛГ \_ RSA \_ KEYX, которое указывает на то, что данные ключа сеанса были зашифрованы с помощью открытого ключа шифрования [*RSA*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="16800-176">This typically has a value of CALG\_RSA\_KEYX, which indicates that the session key data was encrypted with a key exchange public key using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span>                                                                                                                           |
| <span data-ttu-id="16800-177">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="16800-177">encryptedkey</span></span>   | <span data-ttu-id="16800-178">Последовательность **байтов** , представляющая зашифрованные данные ключа сеанса в форме \# блока шифрования PKCS 1, типа 2.</span><span class="sxs-lookup"><span data-stu-id="16800-178">A **BYTE** sequence that represents the encrypted session key data in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="16800-179">Сведения об этом формате данных см. в разделе стандарты криптографии с открытым ключом (PKCS) \# 1, опубликованные RSA Data Security, Inc. Эти данные всегда имеют тот же размер, что и модуль открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="16800-179">For information about this data format, see the Public Key Cryptography Standards (PKCS) \#1, published by RSA Data Security, Inc. This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="16800-180">Например, открытые ключи, создаваемые базовым поставщиком Microsoft RSA, могут иметь длину 512 бит (64 байт), поэтому зашифрованные данные ключа сеанса также всегда имеют значение 512 бит (64 байт).</span><span class="sxs-lookup"><span data-stu-id="16800-180">For example, public keys generated by the Microsoft RSA Base Provider can be 512 bits (64 bytes) in length, so the encrypted session key data is also always 512 bits (64 bytes).</span></span><br/> |
| <span data-ttu-id="16800-181">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="16800-181">publickeystruc</span></span> | <span data-ttu-id="16800-182">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="16800-182">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

<span data-ttu-id="16800-183">Дополнительные сведения о базовом поставщике и BLOB-объектах расширенного поставщика см. в [статье основные двоичные объекты базового поставщика](base-provider-key-blobs.md).</span><span class="sxs-lookup"><span data-stu-id="16800-183">For information about the Base Provider and Extended Provider key BLOBs, see [Base Provider Key BLOBs](base-provider-key-blobs.md).</span></span>

 

 
