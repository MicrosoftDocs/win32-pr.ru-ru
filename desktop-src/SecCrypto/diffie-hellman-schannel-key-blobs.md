---
description: Большие двоичные объекты используются с поставщиком Диффи-Хелмана или SChannel для экспорта ключей из, а также для импорта ключей в поставщик служб шифрования (CSP).
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: Большие двоичные объекты Диффи-Хелмана и ключа SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813737"
---
# <a name="diffie-hellmanschannel-key-blobs"></a><span data-ttu-id="7899a-103">Большие двоичные объекты Диффи-Хелмана и ключа SChannel</span><span class="sxs-lookup"><span data-stu-id="7899a-103">Diffie-Hellman/Schannel Key BLOBs</span></span>

<span data-ttu-id="7899a-104">[*Большие двоичные объекты*](../secgloss/b-gly.md) используются с поставщиком SChannel [*Диффи-Хелмана*](../secgloss/d-gly.md) / [](../secgloss/s-gly.md) для экспорта ключей из и импорта ключей в [*поставщик служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="7899a-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="7899a-105">BLOB-объекты открытого ключа</span><span class="sxs-lookup"><span data-stu-id="7899a-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="7899a-106">BLOB-объекты закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="7899a-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="7899a-107">BLOB-объекты открытого ключа</span><span class="sxs-lookup"><span data-stu-id="7899a-107">Public Key BLOBs</span></span>

<span data-ttu-id="7899a-108">Diffie-Hellman [*большие двоичные объекты с открытым ключом*](../secgloss/p-gly.md)используются для обмена значения (G ^ X) mod P в Diffie-Hellman обмена ключами. </span><span class="sxs-lookup"><span data-stu-id="7899a-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="7899a-109">Эти ключи экспортируются и импортируются в виде последовательности байтов в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="7899a-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="7899a-110">В следующей таблице описаны все компоненты [*большого двоичного объекта ключа*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7899a-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="7899a-111">Поле</span><span class="sxs-lookup"><span data-stu-id="7899a-111">Field</span></span>          | <span data-ttu-id="7899a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7899a-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7899a-113">дхпубкэй</span><span class="sxs-lookup"><span data-stu-id="7899a-113">dhpubkey</span></span>       | <span data-ttu-id="7899a-114">Структура [**дхпубкэй**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="7899a-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="7899a-115">**Фокусный** элемент должен иметь значение 0x31484400.</span><span class="sxs-lookup"><span data-stu-id="7899a-115">The **magic** member must be set to 0x31484400.</span></span> <span data-ttu-id="7899a-116">Это шестнадцатеричное значение является кодировкой [*ASCII*](../secgloss/a-gly.md) для DH1.</span><span class="sxs-lookup"><span data-stu-id="7899a-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH1.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7899a-117">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="7899a-117">publickeystruc</span></span> | <span data-ttu-id="7899a-118">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="7899a-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7899a-119">да</span><span class="sxs-lookup"><span data-stu-id="7899a-119">y</span></span>              | <span data-ttu-id="7899a-120">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="7899a-120">A **BYTE** sequence.</span></span> <span data-ttu-id="7899a-121">Значение y (G ^ X) mod P находится непосредственно после структуры [**дхпубкэй**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="7899a-121">The y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="7899a-122">Длина последовательности в байтах равна **битлен** элементу **дхпубкэй** , разделенному на восемь.</span><span class="sxs-lookup"><span data-stu-id="7899a-122">The length, in bytes, of the sequence is the **bitlen** member of **DHPUBKEY** divided by eight.</span></span> <span data-ttu-id="7899a-123">Если длина данных, полученная в результате вычисления (G ^ X) mod P, равна одному или нескольким байтам, меньшим, чем P, то данные должны быть дополнены необходимыми байтами (нулевого значения), чтобы данные были требуемой длины (формат с [*прямым порядком байтов*](../secgloss/l-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="7899a-123">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="7899a-124">BLOB-объекты закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="7899a-124">Private Key BLOBs</span></span>

<span data-ttu-id="7899a-125">[*Большие двоичные объекты с закрытым ключом*](../secgloss/p-gly.md)d-h используются для экспорта и импорта конфиденциальных сведений о ключе d-h. </span><span class="sxs-lookup"><span data-stu-id="7899a-125">D-H [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to export and import private information of a D-H key.</span></span> <span data-ttu-id="7899a-126">Эти ключи экспортируются и импортируются в виде последовательности байтов в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="7899a-126">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="7899a-127">В следующей таблице описаны все компоненты большого двоичного объекта ключа.</span><span class="sxs-lookup"><span data-stu-id="7899a-127">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="7899a-128">Поле</span><span class="sxs-lookup"><span data-stu-id="7899a-128">Field</span></span>          | <span data-ttu-id="7899a-129">Описание</span><span class="sxs-lookup"><span data-stu-id="7899a-129">Description</span></span>                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7899a-130">дхпубкэй</span><span class="sxs-lookup"><span data-stu-id="7899a-130">dhpubkey</span></span>       | <span data-ttu-id="7899a-131">Структура [**дхпубкэй**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="7899a-131">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="7899a-132">**Фокусный** элемент должен иметь значение 0x32484400.</span><span class="sxs-lookup"><span data-stu-id="7899a-132">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="7899a-133">Это шестнадцатеричное значение является кодировкой [*ASCII*](../secgloss/a-gly.md) для DH2.</span><span class="sxs-lookup"><span data-stu-id="7899a-133">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH2.</span></span> |
| <span data-ttu-id="7899a-134">генератор</span><span class="sxs-lookup"><span data-stu-id="7899a-134">generator</span></span>      | <span data-ttu-id="7899a-135">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="7899a-135">A **BYTE** sequence.</span></span> <span data-ttu-id="7899a-136">Генератор G.</span><span class="sxs-lookup"><span data-stu-id="7899a-136">The generator G.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="7899a-137">публиккэйструк</span><span class="sxs-lookup"><span data-stu-id="7899a-137">publickeystruc</span></span> | <span data-ttu-id="7899a-138">Структура [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="7899a-138">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                      |
| <span data-ttu-id="7899a-139">простых</span><span class="sxs-lookup"><span data-stu-id="7899a-139">prime</span></span>          | <span data-ttu-id="7899a-140">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="7899a-140">A **BYTE** sequence.</span></span> <span data-ttu-id="7899a-141">Основной модуль, P. Эти данные всегда должны иметь наиболее значимый бит наиболее значимого байта, равный одному.</span><span class="sxs-lookup"><span data-stu-id="7899a-141">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                    |
| <span data-ttu-id="7899a-142">secret</span><span class="sxs-lookup"><span data-stu-id="7899a-142">secret</span></span>         | <span data-ttu-id="7899a-143">Последовательность **байтов** .</span><span class="sxs-lookup"><span data-stu-id="7899a-143">A **BYTE** sequence.</span></span> <span data-ttu-id="7899a-144">Секретный показатель X.</span><span class="sxs-lookup"><span data-stu-id="7899a-144">The secret exponent X.</span></span>                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="7899a-145">Значения "основной", "Генератор" и "секрет" должны всегда иметь одинаковую длину в байтах.</span><span class="sxs-lookup"><span data-stu-id="7899a-145">The prime, generator, and secret values must always have the same length, in bytes.</span></span> <span data-ttu-id="7899a-146">Если какое-либо значение является одним байтом или более коротким, оно должно быть дополнено необходимым числом нулевых байтов, чтобы сделать их одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="7899a-146">If any value is one byte or more shorter than the others, it must be padded with the necessary number of zero bytes to make them the same.</span></span> <span data-ttu-id="7899a-147">Простой, генератор и секретный код имеют формат с [*прямым порядком байтов*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="7899a-147">The prime, generator, and secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
