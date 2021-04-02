---
description: Следующий материал допустим только в том случае, если в качестве механизма SASL используется дайджест. Шифры и шифрование недоступны для проверки подлинности HTTP с помощью Microsoft Digest.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Ciphers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263838"
---
# <a name="ciphers"></a><span data-ttu-id="7c1d1-104">Ciphers</span><span class="sxs-lookup"><span data-stu-id="7c1d1-104">Ciphers</span></span>

<span data-ttu-id="7c1d1-105">Следующий материал допустим только в том случае, если в качестве механизма SASL используется дайджест.</span><span class="sxs-lookup"><span data-stu-id="7c1d1-105">The following material is valid only when Digest is used as a SASL mechanism.</span></span> <span data-ttu-id="7c1d1-106">Шифры и шифрование недоступны для проверки подлинности HTTP с помощью Microsoft Digest.</span><span class="sxs-lookup"><span data-stu-id="7c1d1-106">Ciphers and encryption are not available for HTTP authentication using Microsoft Digest.</span></span>

<span data-ttu-id="7c1d1-107">Директива шифра дайджеста SASL содержит список шифров, поддерживаемых сервером, для которого требуется конфиденциальная связь.</span><span class="sxs-lookup"><span data-stu-id="7c1d1-107">A Digest SASL challenge's cipher directive contains a list of the ciphers supported by a server that requires confidential communications.</span></span> <span data-ttu-id="7c1d1-108">Директиву Cipher можно добавить, только если для директивы КОП задано значение "auth-conf".</span><span class="sxs-lookup"><span data-stu-id="7c1d1-108">The cipher directive can only be included if the qop directive is set to "auth-conf".</span></span> <span data-ttu-id="7c1d1-109">Шифры, распознаваемые Microsoft Digest, перечислены в следующей таблице в порядке от самого надежного к слабому.</span><span class="sxs-lookup"><span data-stu-id="7c1d1-109">The ciphers recognized by Microsoft Digest are listed in the following table, in order from strongest to weakest.</span></span>



| <span data-ttu-id="7c1d1-110">Значение шифра</span><span class="sxs-lookup"><span data-stu-id="7c1d1-110">Cipher value</span></span> | <span data-ttu-id="7c1d1-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7c1d1-111">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c1d1-112">RC4</span><span class="sxs-lookup"><span data-stu-id="7c1d1-112">"rc4"</span></span>        | <span data-ttu-id="7c1d1-113">Шифр RC4 с 128-битным ключом.</span><span class="sxs-lookup"><span data-stu-id="7c1d1-113">The RC4 cipher with a 128-bit key.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="7c1d1-114">3DES</span><span class="sxs-lookup"><span data-stu-id="7c1d1-114">"3des"</span></span>       | <span data-ttu-id="7c1d1-115">Шифр [*Triple DES*](/windows/desktop/SecGloss/t-gly) в режиме [*CBC*](/windows/desktop/SecGloss/c-gly) с еде с одним и тем же ключом для каждого этапа E (режим с двумя ключами).</span><span class="sxs-lookup"><span data-stu-id="7c1d1-115">The [*triple DES*](/windows/desktop/SecGloss/t-gly) cipher in [*CBC*](/windows/desktop/SecGloss/c-gly) mode with EDE with the same key for each E stage (two keys mode).</span></span> <span data-ttu-id="7c1d1-116">Общая длина ключа составляет 112 бит.</span><span class="sxs-lookup"><span data-stu-id="7c1d1-116">Total key length is 112 bits.</span></span> |
| <span data-ttu-id="7c1d1-117">RC4-56</span><span class="sxs-lookup"><span data-stu-id="7c1d1-117">"rc4-56"</span></span>     | <span data-ttu-id="7c1d1-118">Шифр RC4 с 56-битным ключом.</span><span class="sxs-lookup"><span data-stu-id="7c1d1-118">The RC4 cipher with a 56-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="7c1d1-119">RC4-40</span><span class="sxs-lookup"><span data-stu-id="7c1d1-119">"rc4-40"</span></span>     | <span data-ttu-id="7c1d1-120">Шифр RC4 с 40-битным ключом.</span><span class="sxs-lookup"><span data-stu-id="7c1d1-120">The RC4 cipher with a 40-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="7c1d1-121">3DES</span><span class="sxs-lookup"><span data-stu-id="7c1d1-121">"des"</span></span>        | <span data-ttu-id="7c1d1-122">Шифр [*стандарта шифрования данных*](/windows/desktop/SecGloss/d-gly) (DES) в режиме [*сцепления блоков*](/windows/desktop/SecGloss/c-gly) шифрования (CBC) с 56-битным ключом.</span><span class="sxs-lookup"><span data-stu-id="7c1d1-122">The [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) (DES) cipher in [*cipher block chaining*](/windows/desktop/SecGloss/c-gly) (CBC) mode with a 56-bit key.</span></span> |



 

<span data-ttu-id="7c1d1-123">Когда серверное приложение запрашивает конфиденциальность (КОП = "auth-conf"), Microsoft Digest создаст запрос, предлагающий клиенту все шифры, установленные на сервере и поддерживаемые дайджестом.</span><span class="sxs-lookup"><span data-stu-id="7c1d1-123">When a server application requests confidentiality (qop="auth-conf") Microsoft Digest will generate a challenge that offers the client all of the ciphers installed on the server and supported by Digest.</span></span> <span data-ttu-id="7c1d1-124">Клиент дайджеста выберет наиболее надежный доступный шифр.</span><span class="sxs-lookup"><span data-stu-id="7c1d1-124">The Digest client will select the strongest available cipher.</span></span> <span data-ttu-id="7c1d1-125">Дополнительные сведения об указании конфиденциальности см. [в разделе Создание дайджест-запроса](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="7c1d1-125">For details on specifying confidentiality, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 
