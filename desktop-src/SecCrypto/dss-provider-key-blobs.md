---
description: Используется с поставщиком услуг стандарта цифровой подписи (DSS) для экспорта ключей из и импорта ключей в поставщик служб шифрования (CSP).
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: BLOB-объекты ключа поставщика DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991025"
---
# <a name="dss-provider-key-blobs"></a><span data-ttu-id="bc66b-103">BLOB-объекты ключа поставщика DSS</span><span class="sxs-lookup"><span data-stu-id="bc66b-103">DSS Provider Key BLOBs</span></span>

<span data-ttu-id="bc66b-104">[*BLOB-объекты*](../secgloss/b-gly.md) используются с поставщиком услуг [*стандарта цифровой подписи*](../secgloss/d-gly.md) (DSS) для экспорта ключей из и импорта ключей в [*поставщик служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="bc66b-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Digital Signature Standard*](../secgloss/d-gly.md) (DSS) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="bc66b-105">BLOB-объекты открытого ключа</span><span class="sxs-lookup"><span data-stu-id="bc66b-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="bc66b-106">BLOB-объекты закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="bc66b-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="bc66b-107">BLOB-объекты открытого ключа</span><span class="sxs-lookup"><span data-stu-id="bc66b-107">Public Key BLOBs</span></span>

<span data-ttu-id="bc66b-108">[*Открытый ключ*](../secgloss/p-gly.md) DSS экспортируется и импортируется как большой двоичный объект, последовательность байтов, структурированная следующим образом.</span><span class="sxs-lookup"><span data-stu-id="bc66b-108">A DSS [*public key*](../secgloss/p-gly.md) is exported and imported as a BLOB, a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

<span data-ttu-id="bc66b-109">Эти компоненты описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bc66b-109">The following table describes these components.</span></span> <span data-ttu-id="bc66b-110">Все значения представлены в формате с [*прямым порядком байтов*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bc66b-110">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="bc66b-111">Поле</span><span class="sxs-lookup"><span data-stu-id="bc66b-111">Field</span></span>          | <span data-ttu-id="bc66b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="bc66b-112">Description</span></span>                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc66b-113">дсспубкэй</span><span class="sxs-lookup"><span data-stu-id="bc66b-113">dsspubkey</span></span>      | <span data-ttu-id="bc66b-114">Структура [**дсспубкэй**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bc66b-114">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="bc66b-115">Элемент **Magic** должен иметь значение 0x31535344.</span><span class="sxs-lookup"><span data-stu-id="bc66b-115">The **magic** member must have a value of 0x31535344.</span></span> <span data-ttu-id="bc66b-116">Это шестнадцатеричное число — кодировка [*ASCII*](../secgloss/a-gly.md) DSS1.</span><span class="sxs-lookup"><span data-stu-id="bc66b-116">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS1.</span></span> |
| <span data-ttu-id="bc66b-117">н</span><span class="sxs-lookup"><span data-stu-id="bc66b-117">g</span></span>              | <span data-ttu-id="bc66b-118">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="bc66b-118">A **BYTE** sequence.</span></span> <span data-ttu-id="bc66b-119">Генератор, g.</span><span class="sxs-lookup"><span data-stu-id="bc66b-119">The generator, g.</span></span> <span data-ttu-id="bc66b-120">Длина должна быть такой же, как и у p.</span><span class="sxs-lookup"><span data-stu-id="bc66b-120">Must be the same length as p.</span></span> <span data-ttu-id="bc66b-121">Если длина не совпадает с длиной p, то она должна быть дополнена 0x00 байтами.</span><span class="sxs-lookup"><span data-stu-id="bc66b-121">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                      |
| <span data-ttu-id="bc66b-122">p</span><span class="sxs-lookup"><span data-stu-id="bc66b-122">p</span></span>              | <span data-ttu-id="bc66b-123">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="bc66b-123">A **BYTE** sequence.</span></span> <span data-ttu-id="bc66b-124">Основной модуль, p.</span><span class="sxs-lookup"><span data-stu-id="bc66b-124">The prime modulus, p.</span></span> <span data-ttu-id="bc66b-125">Для наиболее значимого бита наиболее значимого байта должно быть задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="bc66b-125">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                                 |
| <span data-ttu-id="bc66b-126">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="bc66b-126">publickeystruc</span></span> | <span data-ttu-id="bc66b-127">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="bc66b-127">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                |
| <span data-ttu-id="bc66b-128">q</span><span class="sxs-lookup"><span data-stu-id="bc66b-128">q</span></span>              | <span data-ttu-id="bc66b-129">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="bc66b-129">A **BYTE** sequence.</span></span> <span data-ttu-id="bc66b-130">Простой, q, 20 байт.</span><span class="sxs-lookup"><span data-stu-id="bc66b-130">The prime, q, 20 bytes in length.</span></span> <span data-ttu-id="bc66b-131">Для наиболее значимого бита наиболее значимого байта должно быть задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="bc66b-131">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                     |
| <span data-ttu-id="bc66b-132">сидструкт</span><span class="sxs-lookup"><span data-stu-id="bc66b-132">seedstruct</span></span>     | <span data-ttu-id="bc66b-133">Структура [**дсссид**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) .</span><span class="sxs-lookup"><span data-stu-id="bc66b-133">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="bc66b-134">Начальные значения и счетчики для проверки простых значений.</span><span class="sxs-lookup"><span data-stu-id="bc66b-134">Seed and counter values for verifying primes.</span></span>                                                                                                                                |
| <span data-ttu-id="bc66b-135">да</span><span class="sxs-lookup"><span data-stu-id="bc66b-135">y</span></span>              | <span data-ttu-id="bc66b-136">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="bc66b-136">A **BYTE** sequence.</span></span> <span data-ttu-id="bc66b-137">Открытый ключ, y.</span><span class="sxs-lookup"><span data-stu-id="bc66b-137">The public key, y.</span></span> <span data-ttu-id="bc66b-138">Длина должна быть такой же, как и у p.</span><span class="sxs-lookup"><span data-stu-id="bc66b-138">Must be same length as p.</span></span> <span data-ttu-id="bc66b-139">Если длина не совпадает с длиной p, то она должна быть дополнена 0x00 байтами.</span><span class="sxs-lookup"><span data-stu-id="bc66b-139">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="bc66b-140">[*Большие двоичные объекты с открытым ключом*](../secgloss/p-gly.md) не шифруются.</span><span class="sxs-lookup"><span data-stu-id="bc66b-140">[*Public key BLOBs*](../secgloss/p-gly.md) are not encrypted.</span></span> <span data-ttu-id="bc66b-141">Они содержат открытые ключи в виде открытого [*текста*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bc66b-141">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="bc66b-142">BLOB-объекты закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="bc66b-142">Private Key BLOBs</span></span>

<span data-ttu-id="bc66b-143">[*Закрытый ключ*](../secgloss/p-gly.md) DSS экспортируется и импортируется в виде последовательности байтов, структурированной следующим образом.</span><span class="sxs-lookup"><span data-stu-id="bc66b-143">A DSS [*private key*](../secgloss/p-gly.md) is exported and imported as a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

<span data-ttu-id="bc66b-144">В следующей таблице описаны все компоненты.</span><span class="sxs-lookup"><span data-stu-id="bc66b-144">The following table describes each component.</span></span> <span data-ttu-id="bc66b-145">Все значения представлены в формате с [*прямым порядком байтов*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bc66b-145">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="bc66b-146">Поле</span><span class="sxs-lookup"><span data-stu-id="bc66b-146">Field</span></span>          | <span data-ttu-id="bc66b-147">Описание</span><span class="sxs-lookup"><span data-stu-id="bc66b-147">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc66b-148">дсспубкэй</span><span class="sxs-lookup"><span data-stu-id="bc66b-148">dsspubkey</span></span>      | <span data-ttu-id="bc66b-149">Структура [**дсспубкэй**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bc66b-149">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="bc66b-150">**Фокусный** элемент должен иметь значение 0x32535344.</span><span class="sxs-lookup"><span data-stu-id="bc66b-150">The **magic** member must be set to 0x32535344.</span></span> <span data-ttu-id="bc66b-151">Это шестнадцатеричное число — кодировка [*ASCII*](../secgloss/a-gly.md) DSS2.</span><span class="sxs-lookup"><span data-stu-id="bc66b-151">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS2.</span></span> |
| <span data-ttu-id="bc66b-152">н</span><span class="sxs-lookup"><span data-stu-id="bc66b-152">g</span></span>              | <span data-ttu-id="bc66b-153">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="bc66b-153">A **BYTE** sequence.</span></span> <span data-ttu-id="bc66b-154">Генератор, g.</span><span class="sxs-lookup"><span data-stu-id="bc66b-154">The generator, g.</span></span> <span data-ttu-id="bc66b-155">Длина должна быть такой же, как и у p.</span><span class="sxs-lookup"><span data-stu-id="bc66b-155">Must be the same length as p.</span></span> <span data-ttu-id="bc66b-156">Если длина не совпадает с длиной p, то она должна быть дополнена 0x00 байтами.</span><span class="sxs-lookup"><span data-stu-id="bc66b-156">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                |
| <span data-ttu-id="bc66b-157">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="bc66b-157">publickeystruc</span></span> | <span data-ttu-id="bc66b-158">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="bc66b-158">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                          |
| <span data-ttu-id="bc66b-159">p</span><span class="sxs-lookup"><span data-stu-id="bc66b-159">p</span></span>              | <span data-ttu-id="bc66b-160">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="bc66b-160">A **BYTE** sequence.</span></span> <span data-ttu-id="bc66b-161">Основной модуль, p.</span><span class="sxs-lookup"><span data-stu-id="bc66b-161">The prime modulus, p.</span></span> <span data-ttu-id="bc66b-162">Для наиболее значимого бита наиболее значимого байта должно быть задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="bc66b-162">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                           |
| <span data-ttu-id="bc66b-163">q</span><span class="sxs-lookup"><span data-stu-id="bc66b-163">q</span></span>              | <span data-ttu-id="bc66b-164">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="bc66b-164">A **BYTE** sequence.</span></span> <span data-ttu-id="bc66b-165">Простое, q.</span><span class="sxs-lookup"><span data-stu-id="bc66b-165">The prime, q.</span></span> <span data-ttu-id="bc66b-166">q имеет длину 20 байт.</span><span class="sxs-lookup"><span data-stu-id="bc66b-166">q is 20 bytes in length.</span></span> <span data-ttu-id="bc66b-167">Для наиболее значимого бита наиболее значимого байта должно быть задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="bc66b-167">The most significant bit of the most significant byte must be set to one.</span></span>                                                                          |
| <span data-ttu-id="bc66b-168">сидструкт</span><span class="sxs-lookup"><span data-stu-id="bc66b-168">seedstruct</span></span>     | <span data-ttu-id="bc66b-169">Структура [**дсссид**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) .</span><span class="sxs-lookup"><span data-stu-id="bc66b-169">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="bc66b-170">Начальные значения и счетчики для проверки простых значений.</span><span class="sxs-lookup"><span data-stu-id="bc66b-170">Seed and counter values for verifying primes.</span></span>                                                                                                                          |
| <span data-ttu-id="bc66b-171">x</span><span class="sxs-lookup"><span data-stu-id="bc66b-171">x</span></span>              | <span data-ttu-id="bc66b-172">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="bc66b-172">A **BYTE** sequence.</span></span> <span data-ttu-id="bc66b-173">Экспонента секрета, x.</span><span class="sxs-lookup"><span data-stu-id="bc66b-173">The secret exponent, x.</span></span> <span data-ttu-id="bc66b-174">Всегда должно иметь длину 20 байт.</span><span class="sxs-lookup"><span data-stu-id="bc66b-174">Must always be 20 bytes in length.</span></span> <span data-ttu-id="bc66b-175">Если длина x меньше 20 байт, то она должна быть дополнена 0x00.</span><span class="sxs-lookup"><span data-stu-id="bc66b-175">If x is smaller than 20 bytes in length, then it must be padded with 0x00.</span></span>                                                     |



 

<span data-ttu-id="bc66b-176">При вызове [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)разработчик может выбрать, следует ли шифровать ключ.</span><span class="sxs-lookup"><span data-stu-id="bc66b-176">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="bc66b-177">**Приватекэйблоб** шифруется, если параметр *хекспкэй* содержит допустимый маркер для ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="bc66b-177">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="bc66b-178">Все, кроме [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) части большого двоичного объекта, шифруется.</span><span class="sxs-lookup"><span data-stu-id="bc66b-178">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="bc66b-179">Параметры алгоритма шифрования и ключа шифрования не сохраняются вместе с BLOB-объектом закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="bc66b-179">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="bc66b-180">Приложение должно управлять и хранить эти сведения.</span><span class="sxs-lookup"><span data-stu-id="bc66b-180">The application must manage and store this information.</span></span> <span data-ttu-id="bc66b-181">Если для *хекспкэй* передается ноль, закрытый ключ будет экспортирован без шифрования.</span><span class="sxs-lookup"><span data-stu-id="bc66b-181">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="bc66b-182">Экспортировать закрытые ключи без шифрования небезопасно, так как они уязвимы для перехвата и использования неавторизованными сущностями.</span><span class="sxs-lookup"><span data-stu-id="bc66b-182">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

 

 
