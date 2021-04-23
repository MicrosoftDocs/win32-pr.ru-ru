---
description: BLOB-объекты используются с поставщиком RSA/SChannel для экспорта ключей из и импорта ключей в поставщик служб шифрования (CSP).
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: BLOB-объекты ключей RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea26a98e9c2925442166eb28245ebc471b1749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897598"
---
# <a name="rsaschannel-key-blobs"></a><span data-ttu-id="e8289-103">BLOB-объекты ключей RSA/SChannel</span><span class="sxs-lookup"><span data-stu-id="e8289-103">RSA/Schannel Key BLOBs</span></span>

<span data-ttu-id="e8289-104">[*BLOB-объекты*](../secgloss/b-gly.md) используются с поставщиком [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) для экспорта ключей из и импорта ключей в [*поставщик служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="e8289-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="e8289-105">BLOB-объекты открытого ключа</span><span class="sxs-lookup"><span data-stu-id="e8289-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="e8289-106">BLOB-объекты закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="e8289-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="e8289-107">Простые ключевые BLOB-объекты</span><span class="sxs-lookup"><span data-stu-id="e8289-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="e8289-108">BLOB-объекты открытого ключа</span><span class="sxs-lookup"><span data-stu-id="e8289-108">Public Key BLOBs</span></span>

<span data-ttu-id="e8289-109">Для хранения [*открытых ключей*](../secgloss/p-gly.md)используются [*большие двоичные объекты с открытым ключом*](../secgloss/p-gly.md), тип **публиккэйблоб**.</span><span class="sxs-lookup"><span data-stu-id="e8289-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="e8289-110">Эти ключи экспортируются и импортируются в виде последовательности байтов в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="e8289-110">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="e8289-111">В следующей таблице описаны все компоненты открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="e8289-111">The following table describes each public key component.</span></span> <span data-ttu-id="e8289-112">Все значения представлены в формате с [*прямым порядком байтов*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e8289-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="e8289-113">Поле</span><span class="sxs-lookup"><span data-stu-id="e8289-113">Field</span></span>          | <span data-ttu-id="e8289-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e8289-114">Description</span></span>                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8289-115">остатка от деления</span><span class="sxs-lookup"><span data-stu-id="e8289-115">modulus</span></span>        | <span data-ttu-id="e8289-116">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="e8289-116">A **BYTE** sequence.</span></span> <span data-ttu-id="e8289-117">Данные модуля открытого ключа находятся непосредственно после структуры **рсапубкэй** .</span><span class="sxs-lookup"><span data-stu-id="e8289-117">The public key modulus data is located directly after the **RSAPUBKEY** structure.</span></span> <span data-ttu-id="e8289-118">Длина этих данных зависит от длины открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="e8289-118">The length of this data varies, depending on the length of the public key.</span></span> <span data-ttu-id="e8289-119">Число байтов может быть определено путем деления значения элемента **Битлен** **рсапубкэй** на восемь.</span><span class="sxs-lookup"><span data-stu-id="e8289-119">The number of bytes can be determined by dividing the value of the **bitlen** member of **RSAPUBKEY** by eight.</span></span> |
| <span data-ttu-id="e8289-120">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="e8289-120">publickeystruc</span></span> | <span data-ttu-id="e8289-121">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="e8289-121">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="e8289-122">рсапубкэй</span><span class="sxs-lookup"><span data-stu-id="e8289-122">rsapubkey</span></span>      | <span data-ttu-id="e8289-123">Структура [**рсапубкэй**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="e8289-123">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="e8289-124">**Фокусный** элемент должен иметь значение 0x31415352.</span><span class="sxs-lookup"><span data-stu-id="e8289-124">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="e8289-125">Это шестнадцатеричное значение является кодировкой [*ASCII*](../secgloss/a-gly.md) для RSA1.</span><span class="sxs-lookup"><span data-stu-id="e8289-125">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                                      |



 

> [!Note]  
> <span data-ttu-id="e8289-126">Большие двоичные объекты с открытым ключом не шифруются.</span><span class="sxs-lookup"><span data-stu-id="e8289-126">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="e8289-127">Они содержат открытые ключи в виде открытого [*текста*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e8289-127">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="e8289-128">BLOB-объекты закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="e8289-128">Private Key BLOBs</span></span>

<span data-ttu-id="e8289-129">[*BLOB-объекты с закрытыми ключами*](../secgloss/p-gly.md)типа **приватекэйблоб** используются для хранения [*пар открытого и закрытого ключей*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e8289-129">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="e8289-130">Эти ключи экспортируются и импортируются в виде последовательности байтов в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="e8289-130">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="e8289-131">Если [*большой двоичный объект ключа*](../secgloss/k-gly.md) зашифрован, то все, кроме [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) части большого двоичного объекта, шифруются.</span><span class="sxs-lookup"><span data-stu-id="e8289-131">If the [*key BLOB*](../secgloss/k-gly.md) is encrypted, then everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="e8289-132">Параметры алгоритма шифрования и ключа шифрования не сохраняются вместе с BLOB-объектом закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="e8289-132">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="e8289-133">Для управления этими сведениями отвечает приложение.</span><span class="sxs-lookup"><span data-stu-id="e8289-133">It is the responsibility of the application to manage this information.</span></span>

 

<span data-ttu-id="e8289-134">В следующей таблице описывается каждый компонент BLOB-объекта закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="e8289-134">The following table describes each private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="e8289-135">Эти поля соответствуют полям, описанным в разделе 7,2 [*стандарта криптографии с открытым ключом*](../secgloss/p-gly.md) (PKCS) \# 1 с незначительными отличиями.</span><span class="sxs-lookup"><span data-stu-id="e8289-135">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="e8289-136">Поле</span><span class="sxs-lookup"><span data-stu-id="e8289-136">Field</span></span>           | <span data-ttu-id="e8289-137">Описание</span><span class="sxs-lookup"><span data-stu-id="e8289-137">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8289-138">exponent1</span><span class="sxs-lookup"><span data-stu-id="e8289-138">exponent1</span></span>       | <span data-ttu-id="e8289-139">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="e8289-139">A **BYTE** sequence.</span></span> <span data-ttu-id="e8289-140">Первый показатель степени.</span><span class="sxs-lookup"><span data-stu-id="e8289-140">The first exponent.</span></span> <span data-ttu-id="e8289-141">Оно имеет числовое значение d Mod (p – 1).</span><span class="sxs-lookup"><span data-stu-id="e8289-141">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                           |
| <span data-ttu-id="e8289-142">exponent2</span><span class="sxs-lookup"><span data-stu-id="e8289-142">exponent2</span></span>       | <span data-ttu-id="e8289-143">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="e8289-143">A **BYTE** sequence.</span></span> <span data-ttu-id="e8289-144">Второй показатель степени.</span><span class="sxs-lookup"><span data-stu-id="e8289-144">The second exponent.</span></span> <span data-ttu-id="e8289-145">Оно имеет числовое значение d Mod (q – 1).</span><span class="sxs-lookup"><span data-stu-id="e8289-145">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                          |
| <span data-ttu-id="e8289-146">части</span><span class="sxs-lookup"><span data-stu-id="e8289-146">coefficient</span></span>     | <span data-ttu-id="e8289-147">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="e8289-147">A **BYTE** sequence.</span></span> <span data-ttu-id="e8289-148">Части.</span><span class="sxs-lookup"><span data-stu-id="e8289-148">Coefficient.</span></span> <span data-ttu-id="e8289-149">Оно имеет числовое значение (обратная часть q) mod p.</span><span class="sxs-lookup"><span data-stu-id="e8289-149">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                           |
| <span data-ttu-id="e8289-150">Modulus</span><span class="sxs-lookup"><span data-stu-id="e8289-150">Modulus</span></span>         | <span data-ttu-id="e8289-151">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="e8289-151">A **BYTE** sequence.</span></span> <span data-ttu-id="e8289-152">Модуль.</span><span class="sxs-lookup"><span data-stu-id="e8289-152">The modulus.</span></span> <span data-ttu-id="e8289-153">Он содержит строку, содержащую *Prime1* \* *Prime2*.</span><span class="sxs-lookup"><span data-stu-id="e8289-153">This has a string that contains *Prime1* \* *Prime2*.</span></span> <span data-ttu-id="e8289-154">Он часто называется n.</span><span class="sxs-lookup"><span data-stu-id="e8289-154">It is often known as n.</span></span>                                                                                               |
| <span data-ttu-id="e8289-155">prime1</span><span class="sxs-lookup"><span data-stu-id="e8289-155">prime1</span></span>          | <span data-ttu-id="e8289-156">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="e8289-156">A **BYTE** sequence.</span></span> <span data-ttu-id="e8289-157">Простое число 1, которое часто называют p.</span><span class="sxs-lookup"><span data-stu-id="e8289-157">Prime number 1, often known as p.</span></span>                                                                                                                                                        |
| <span data-ttu-id="e8289-158">prime2</span><span class="sxs-lookup"><span data-stu-id="e8289-158">prime2</span></span>          | <span data-ttu-id="e8289-159">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="e8289-159">A **BYTE** sequence.</span></span> <span data-ttu-id="e8289-160">Простое число 2, которое часто называют q.</span><span class="sxs-lookup"><span data-stu-id="e8289-160">Prime number 2, often known as q.</span></span>                                                                                                                                                        |
| <span data-ttu-id="e8289-161">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="e8289-161">publickeystruc</span></span>  | <span data-ttu-id="e8289-162">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="e8289-162">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="e8289-163">приватикспонент</span><span class="sxs-lookup"><span data-stu-id="e8289-163">privateExponent</span></span> | <span data-ttu-id="e8289-164">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="e8289-164">A **BYTE** sequence.</span></span> <span data-ttu-id="e8289-165">Закрытый показатель степени, часто известный как d.</span><span class="sxs-lookup"><span data-stu-id="e8289-165">The private exponent, often known as d.</span></span>                                                                                                                                                  |
| <span data-ttu-id="e8289-166">рсапубкэй</span><span class="sxs-lookup"><span data-stu-id="e8289-166">rsapubkey</span></span>       | <span data-ttu-id="e8289-167">Структура [**рсапубкэй**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="e8289-167">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="e8289-168">**Фокусный** элемент должен иметь значение 0x32415352.</span><span class="sxs-lookup"><span data-stu-id="e8289-168">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="e8289-169">Это шестнадцатеричное значение является кодировкой [*ASCII*](../secgloss/a-gly.md) для RSA2.</span><span class="sxs-lookup"><span data-stu-id="e8289-169">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="e8289-170">Большие двоичные объекты с закрытыми ключами не шифруются.</span><span class="sxs-lookup"><span data-stu-id="e8289-170">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="e8289-171">Они содержат закрытые ключи в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="e8289-171">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="e8289-172">При вызове [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)разработчик может выбрать, следует ли шифровать ключ.</span><span class="sxs-lookup"><span data-stu-id="e8289-172">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="e8289-173">**Приватекэйблоб** шифруется, если параметр *хекспкэй* содержит допустимый маркер для ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="e8289-173">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="e8289-174">Все, кроме [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) части большого двоичного объекта, шифруется.</span><span class="sxs-lookup"><span data-stu-id="e8289-174">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="e8289-175">Параметры алгоритма шифрования и ключа шифрования не сохраняются вместе с BLOB-объектом закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="e8289-175">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="e8289-176">Приложение должно управлять и хранить эти сведения.</span><span class="sxs-lookup"><span data-stu-id="e8289-176">The application must manage and store this information.</span></span> <span data-ttu-id="e8289-177">Если для *хекспкэй* передается ноль, закрытый ключ будет экспортирован без шифрования.</span><span class="sxs-lookup"><span data-stu-id="e8289-177">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="e8289-178">Экспортировать закрытые ключи без шифрования небезопасно, так как они уязвимы для перехвата и использования неавторизованными сущностями.</span><span class="sxs-lookup"><span data-stu-id="e8289-178">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="e8289-179">Простые ключевые BLOB-объекты</span><span class="sxs-lookup"><span data-stu-id="e8289-179">Simple Key BLOBs</span></span>

<span data-ttu-id="e8289-180">[*Простые ключевые BLOB-объекты*](../secgloss/s-gly.md)типа **симплеблоб** используются для хранения и передачи ключей сеанса.</span><span class="sxs-lookup"><span data-stu-id="e8289-180">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys.</span></span> <span data-ttu-id="e8289-181">Они всегда шифруются с помощью [*открытого ключа обмена ключами*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e8289-181">These are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="e8289-182">Эти ключи экспортируются и импортируются в виде последовательности байтов в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="e8289-182">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="e8289-183">В следующей таблице описаны все простые компоненты больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="e8289-183">The following table describes each simple BLOB component.</span></span>



| <span data-ttu-id="e8289-184">Поле</span><span class="sxs-lookup"><span data-stu-id="e8289-184">Field</span></span>          | <span data-ttu-id="e8289-185">Описание</span><span class="sxs-lookup"><span data-stu-id="e8289-185">Description</span></span>                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8289-186">алгид</span><span class="sxs-lookup"><span data-stu-id="e8289-186">algid</span></span>          | <span data-ttu-id="e8289-187">Структура [**\_ идентификаторов ALG**](alg-id.md) .</span><span class="sxs-lookup"><span data-stu-id="e8289-187">An [**ALG\_ID**](alg-id.md) structure.</span></span> <span data-ttu-id="e8289-188">Обычно это указывает алгоритм КАЛГ \_ RSA \_ KEYX, который указывает, что данные ключа сеанса были зашифрованы с помощью открытого ключа обмена ключами, используя [*алгоритм открытого ключа RSA*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e8289-188">This typically specifies the CALG\_RSA\_KEYX algorithm, which indicates that the session key data was encrypted with a key exchange public key, using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span> |
| <span data-ttu-id="e8289-189">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="e8289-189">encryptedkey</span></span>   | <span data-ttu-id="e8289-190">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="e8289-190">A **BYTE** sequence.</span></span> <span data-ttu-id="e8289-191">Зашифрованные данные ключа сеанса имеют вид \# блока шифрования PKCS 1, тип 2.</span><span class="sxs-lookup"><span data-stu-id="e8289-191">The encrypted session key data is in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="e8289-192">Сведения об этом формате данных см. в разделе стандарты криптографии с открытым ключом (PKCS), опубликованные RSA Data Security, Inc.</span><span class="sxs-lookup"><span data-stu-id="e8289-192">For information about this data format, see the Public Key Cryptography Standards (PKCS), published by RSA Data Security, Inc.</span></span>                                                                                     |
| <span data-ttu-id="e8289-193">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="e8289-193">publickeystruc</span></span> | <span data-ttu-id="e8289-194">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="e8289-194">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="e8289-195">Эти данные всегда имеют тот же размер, что и модуль открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="e8289-195">This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="e8289-196">Например, открытые ключи, создаваемые базовым поставщиком служб шифрования Майкрософт, всегда имеют 512 бит (64 байт), поэтому зашифрованные данные ключа сеанса также всегда имеют размер 64 байт.</span><span class="sxs-lookup"><span data-stu-id="e8289-196">For example, public keys generated by the Microsoft Base Cryptographic Provider are always 512 bits (64 bytes) in length, so the encrypted session key data is also always 64 bytes.</span></span>

 

 
