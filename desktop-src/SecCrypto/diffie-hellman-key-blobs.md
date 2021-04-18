---
description: BLOB-объекты используются с поставщиком Diffie-Hellman для экспорта ключей из, а также для импорта ключей в поставщик служб шифрования (CSP).
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Diffie-Hellmanные BLOB-объекты ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663096"
---
# <a name="diffie-hellman-key-blobs"></a><span data-ttu-id="9398e-103">Diffie-Hellmanные BLOB-объекты ключей</span><span class="sxs-lookup"><span data-stu-id="9398e-103">Diffie-Hellman Key BLOBs</span></span>

<span data-ttu-id="9398e-104">[*Большие двоичные объекты*](../secgloss/b-gly.md) используются с поставщиком [*Диффи-Хелмана*](../secgloss/d-gly.md) для экспорта ключей из и импорта ключей в [*поставщик служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="9398e-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="9398e-105">BLOB-объекты открытого ключа</span><span class="sxs-lookup"><span data-stu-id="9398e-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="9398e-106">BLOB-объекты закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="9398e-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="9398e-107">BLOB-объекты открытого ключа</span><span class="sxs-lookup"><span data-stu-id="9398e-107">Public Key BLOBs</span></span>

<span data-ttu-id="9398e-108">Diffie-Hellman [*большие двоичные объекты с открытым ключом*](../secgloss/p-gly.md)используются для обмена значения (G ^ X) mod P в Diffie-Hellman обмена ключами. </span><span class="sxs-lookup"><span data-stu-id="9398e-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="9398e-109">Эти ключи экспортируются и импортируются в виде последовательности байтов в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="9398e-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="9398e-110">В следующей таблице описаны все компоненты [*большого двоичного объекта ключа*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9398e-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="9398e-111">Поле</span><span class="sxs-lookup"><span data-stu-id="9398e-111">Field</span></span>          | <span data-ttu-id="9398e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9398e-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9398e-113">дхпубкэй</span><span class="sxs-lookup"><span data-stu-id="9398e-113">dhpubkey</span></span>       | <span data-ttu-id="9398e-114">Структура [**дхпубкэй**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="9398e-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="9398e-115">**Фокусный** элемент должен иметь значение 0x31484400.</span><span class="sxs-lookup"><span data-stu-id="9398e-115">The **magic** member should be set to 0x31484400.</span></span> <span data-ttu-id="9398e-116">Это шестнадцатеричное значение — кодировка [*ASCII*](../secgloss/a-gly.md) "DH1".</span><span class="sxs-lookup"><span data-stu-id="9398e-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH1".</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9398e-117">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="9398e-117">publickeystruc</span></span> | <span data-ttu-id="9398e-118">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="9398e-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9398e-119">да</span><span class="sxs-lookup"><span data-stu-id="9398e-119">y</span></span>              | <span data-ttu-id="9398e-120">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="9398e-120">A **BYTE** sequence.</span></span> <span data-ttu-id="9398e-121">Значение Y (G ^ X) mod P находится непосредственно после структуры [**дхпубкэй**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) и всегда должно быть длиной (в байтах) поля **дхпубкэй битлен** (разрядная длина P), деленная на восемь.</span><span class="sxs-lookup"><span data-stu-id="9398e-121">The Y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure, and should always be the length, in bytes, of the **DHPUBKEY bitlen** field (bit length of P) divided by eight.</span></span> <span data-ttu-id="9398e-122">Если длина данных, полученная в результате вычисления (G ^ X) mod P, равна одному или нескольким байтам, меньшим, чем P, то данные должны быть дополнены необходимыми байтами (нулевого значения), чтобы данные были требуемой длины (формат с [*прямым порядком байтов*](../secgloss/l-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="9398e-122">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="9398e-123">BLOB-объекты закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="9398e-123">Private Key BLOBs</span></span>

<span data-ttu-id="9398e-124">Diffie-Hellman [*BLOB-объекты с закрытыми ключами*](../secgloss/p-gly.md)введите **приватекэйблоб**, чтобы сохранить сведения об общедоступных и закрытых данных ключа Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="9398e-124">Diffie-Hellman [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store the public/private information of a Diffie-Hellman key.</span></span> <span data-ttu-id="9398e-125">Эти ключи экспортируются и импортируются в виде последовательности байтов в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="9398e-125">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="9398e-126">В следующей таблице описаны все компоненты большого двоичного объекта ключа.</span><span class="sxs-lookup"><span data-stu-id="9398e-126">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="9398e-127">Поле</span><span class="sxs-lookup"><span data-stu-id="9398e-127">Field</span></span>          | <span data-ttu-id="9398e-128">Описание</span><span class="sxs-lookup"><span data-stu-id="9398e-128">Description</span></span>                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9398e-129">дхпубкэй</span><span class="sxs-lookup"><span data-stu-id="9398e-129">dhpubkey</span></span>       | <span data-ttu-id="9398e-130">Структура [**дхпубкэй**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="9398e-130">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="9398e-131">**Фокусный** элемент должен иметь значение 0x32484400.</span><span class="sxs-lookup"><span data-stu-id="9398e-131">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="9398e-132">Это шестнадцатеричное значение — кодировка [*ASCII*](../secgloss/a-gly.md) "DH2".</span><span class="sxs-lookup"><span data-stu-id="9398e-132">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH2".</span></span> |
| <span data-ttu-id="9398e-133">генератор</span><span class="sxs-lookup"><span data-stu-id="9398e-133">generator</span></span>      | <span data-ttu-id="9398e-134">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="9398e-134">A **BYTE** sequence.</span></span> <span data-ttu-id="9398e-135">Генератор, G.</span><span class="sxs-lookup"><span data-stu-id="9398e-135">The generator, G.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="9398e-136">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="9398e-136">publickeystruc</span></span> | <span data-ttu-id="9398e-137">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="9398e-137">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                        |
| <span data-ttu-id="9398e-138">простых</span><span class="sxs-lookup"><span data-stu-id="9398e-138">prime</span></span>          | <span data-ttu-id="9398e-139">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="9398e-139">A **BYTE** sequence.</span></span> <span data-ttu-id="9398e-140">Основной модуль, P. Эти данные всегда должны иметь наиболее значимый бит наиболее значимого байта, равный одному.</span><span class="sxs-lookup"><span data-stu-id="9398e-140">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                      |
| <span data-ttu-id="9398e-141">secret</span><span class="sxs-lookup"><span data-stu-id="9398e-141">secret</span></span>         | <span data-ttu-id="9398e-142">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="9398e-142">A **BYTE** sequence.</span></span> <span data-ttu-id="9398e-143">Экспонента секрета, X.</span><span class="sxs-lookup"><span data-stu-id="9398e-143">The secret exponent, X.</span></span>                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="9398e-144">Генератор и секрет должны всегда иметь одинаковую длину в байтах.</span><span class="sxs-lookup"><span data-stu-id="9398e-144">The generator and secret must always have the same length, in bytes.</span></span> <span data-ttu-id="9398e-145">Если один байт или более короткий, то он должен быть дополнен требуемым числом нулевых байтов, чтобы сделать их одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="9398e-145">If either is one byte or more shorter than the other, it must be padded with the necessary number of zero value bytes to make them the same.</span></span> <span data-ttu-id="9398e-146">И генератор, и секрет имеют формат с [*прямым порядком байтов*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9398e-146">Both the generator and the secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
