---
description: Поддерживаемые протоколы и комплекты шифров могут быть перечислены вызовами Криптжетпровпарам с PP \_ енумалгс или PP \_ енумалгс \_ ex.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Перечисление поддерживаемых протоколов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662856"
---
# <a name="enumerating-supported-protocols"></a><span data-ttu-id="bb8cc-103">Перечисление поддерживаемых протоколов</span><span class="sxs-lookup"><span data-stu-id="bb8cc-103">Enumerating Supported Protocols</span></span>

<span data-ttu-id="bb8cc-104">Поддерживаемые протоколы и комплекты шифров могут быть перечислены вызовами [**криптжетпровпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) с PP \_ енумалгс или PP \_ енумалгс \_ ex.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-104">Supported protocols and cipher suites can be listed by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with PP\_ENUMALGS or PP\_ENUMALGS\_EX.</span></span> <span data-ttu-id="bb8cc-105">Значение PP \_ енумалгс \_ ex работает так же, как PP \_ енумалгс, но возвращает структуру [**Prov \_ енумалгс \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) , содержащую более обширную информацию о алгоритмах, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-105">The PP\_ENUMALGS\_EX value works like PP\_ENUMALGS but returns a [**PROV\_ENUMALGS\_EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) structure that holds more extensive information on the algorithms supported by the provider.</span></span>

<span data-ttu-id="bb8cc-106">Дополнительные сведения об определенных флагах протокола и их значениях см. в разделе [флаги протокола](protocol-flags.md).</span><span class="sxs-lookup"><span data-stu-id="bb8cc-106">For more information about defined protocol flags and their values, see [Protocol Flags](protocol-flags.md).</span></span>

<span data-ttu-id="bb8cc-107">Учитывая, что элемент **хкриптпров** является [*маркером*](../secgloss/h-gly.md) открытого криптографического [*контекста*](../secgloss/c-gly.md) , полученного с помощью [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) с параметром *двпровтипе* , имеющим значение Prov \_ RSA \_ SChannel, в следующем примере перечисляются имена всех алгоритмов, доступных в CSP.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-107">Given that the **hCryptProv** member is the [*handle*](../secgloss/h-gly.md) of an open cryptographic [*context*](../secgloss/c-gly.md) acquired by using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) with its *dwProvType* parameter set to PROV\_RSA\_SCHANNEL, the following example lists the names of all algorithms available in the CSP.</span></span>


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



<span data-ttu-id="bb8cc-108">В следующей таблице перечислены некоторые алгоритмы, возвращаемые обычным внутренним \_ CSP Prov RSA \_ SChannel.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-108">The following table lists some algorithms returned by a typical domestic PROV\_RSA\_SCHANNEL CSP.</span></span> <span data-ttu-id="bb8cc-109">Обратите внимание, что в этом примере CSP не поддерживает шифрование SHA Макинтош и SSL2 DES.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-109">Notice that neither SSL2 SHA MACs nor SSL2 DES encryption is supported by the CSP in this example.</span></span>



| <span data-ttu-id="bb8cc-110">Идентификатор алгоритма</span><span class="sxs-lookup"><span data-stu-id="bb8cc-110">Algorithm identifier</span></span>                                                                        | <span data-ttu-id="bb8cc-111">Минимальная длина ключа</span><span class="sxs-lookup"><span data-stu-id="bb8cc-111">Minimum key length</span></span> | <span data-ttu-id="bb8cc-112">Максимальная длина ключа</span><span class="sxs-lookup"><span data-stu-id="bb8cc-112">Maximum key length</span></span> | <span data-ttu-id="bb8cc-113">Протоколы</span><span class="sxs-lookup"><span data-stu-id="bb8cc-113">Protocols</span></span> | <span data-ttu-id="bb8cc-114">Имя алгоритма</span><span class="sxs-lookup"><span data-stu-id="bb8cc-114">Algorithm name</span></span> |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [<span data-ttu-id="bb8cc-115">*КАЛГ \_ RSA \_ KEYX*</span><span class="sxs-lookup"><span data-stu-id="bb8cc-115">*CALG\_RSA\_KEYX*</span></span>](../secgloss/c-gly.md) | <span data-ttu-id="bb8cc-116">512</span><span class="sxs-lookup"><span data-stu-id="bb8cc-116">512</span></span>                | <span data-ttu-id="bb8cc-117">2048</span><span class="sxs-lookup"><span data-stu-id="bb8cc-117">2048</span></span>               | <span data-ttu-id="bb8cc-118">0x0007</span><span class="sxs-lookup"><span data-stu-id="bb8cc-118">0x0007</span></span>    | <span data-ttu-id="bb8cc-119">"RSA \_ KEYX"</span><span class="sxs-lookup"><span data-stu-id="bb8cc-119">"RSA\_KEYX"</span></span>    |
| [<span data-ttu-id="bb8cc-120">*\_MD5 калг*</span><span class="sxs-lookup"><span data-stu-id="bb8cc-120">*CALG\_MD5*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="bb8cc-121">128</span><span class="sxs-lookup"><span data-stu-id="bb8cc-121">128</span></span>                | <span data-ttu-id="bb8cc-122">128</span><span class="sxs-lookup"><span data-stu-id="bb8cc-122">128</span></span>                | <span data-ttu-id="bb8cc-123">0x0007</span><span class="sxs-lookup"><span data-stu-id="bb8cc-123">0x0007</span></span>    | <span data-ttu-id="bb8cc-124">MD5</span><span class="sxs-lookup"><span data-stu-id="bb8cc-124">"MD5"</span></span>          |
| [<span data-ttu-id="bb8cc-125">*\_SHA калг*</span><span class="sxs-lookup"><span data-stu-id="bb8cc-125">*CALG\_SHA*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="bb8cc-126">160</span><span class="sxs-lookup"><span data-stu-id="bb8cc-126">160</span></span>                | <span data-ttu-id="bb8cc-127">160</span><span class="sxs-lookup"><span data-stu-id="bb8cc-127">160</span></span>                | <span data-ttu-id="bb8cc-128">0x0005</span><span class="sxs-lookup"><span data-stu-id="bb8cc-128">0x0005</span></span>    | <span data-ttu-id="bb8cc-129">ХЭШ</span><span class="sxs-lookup"><span data-stu-id="bb8cc-129">"SHA"</span></span>          |
| [<span data-ttu-id="bb8cc-130">*КАЛГ \_ RC4*</span><span class="sxs-lookup"><span data-stu-id="bb8cc-130">*CALG\_RC4*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="bb8cc-131">40</span><span class="sxs-lookup"><span data-stu-id="bb8cc-131">40</span></span>                 | <span data-ttu-id="bb8cc-132">128</span><span class="sxs-lookup"><span data-stu-id="bb8cc-132">128</span></span>                | <span data-ttu-id="bb8cc-133">0x0007</span><span class="sxs-lookup"><span data-stu-id="bb8cc-133">0x0007</span></span>    | <span data-ttu-id="bb8cc-134">RC4</span><span class="sxs-lookup"><span data-stu-id="bb8cc-134">"RC4"</span></span>          |
| <span data-ttu-id="bb8cc-135">КАЛГ \_ des</span><span class="sxs-lookup"><span data-stu-id="bb8cc-135">CALG\_DES</span></span>                                                                                   | <span data-ttu-id="bb8cc-136">56</span><span class="sxs-lookup"><span data-stu-id="bb8cc-136">56</span></span>                 | <span data-ttu-id="bb8cc-137">56</span><span class="sxs-lookup"><span data-stu-id="bb8cc-137">56</span></span>                 | <span data-ttu-id="bb8cc-138">0x0005</span><span class="sxs-lookup"><span data-stu-id="bb8cc-138">0x0005</span></span>    | <span data-ttu-id="bb8cc-139">3DES</span><span class="sxs-lookup"><span data-stu-id="bb8cc-139">"DES"</span></span>          |



 

<span data-ttu-id="bb8cc-140">Чтобы подготовиться к отправке сообщений Клиенселло или Серверхелло, механизм протокола [*SChannel*](../secgloss/s-gly.md) перечисляет алгоритмы и размеры ключей, поддерживаемые CSP, и создает список, который является внутренним набором поддерживаемых комплектов шифров.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-140">To prepare to send ClientHello or ServerHello messages, the [*Schannel*](../secgloss/s-gly.md) protocol engine enumerates the algorithms and key sizes supported by the CSP and builds a list internally of supported cipher suites.</span></span>

 

 
