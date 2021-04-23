---
description: Комплект шифров — это набор алгоритмов шифрования.
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: Комплекты шифров в TLS/SSL (общедоступный поставщик услуг Schannel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa8b47aed266c49ac306adfd2aef78af269a39
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105651244"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a><span data-ttu-id="7ebcf-103">Комплекты шифров в TLS/SSL (общедоступный поставщик услуг Schannel)</span><span class="sxs-lookup"><span data-stu-id="7ebcf-103">Cipher Suites in TLS/SSL (Schannel SSP)</span></span>

<span data-ttu-id="7ebcf-104">Комплект шифров — это набор алгоритмов шифрования.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-104">A cipher suite is a set of cryptographic algorithms.</span></span> <span data-ttu-id="7ebcf-105">Реализация протокола TLS/SSL в ПОСТАВЩИКе SChannel использует алгоритмы из набора шифров для создания ключей и шифрования информации.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-105">The schannel SSP implementation of the TLS/SSL protocols use algorithms from a cipher suite to create keys and encrypt information.</span></span> <span data-ttu-id="7ebcf-106">Комплект шифров указывает один алгоритм для каждой из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="7ebcf-106">A cipher suite specifies one algorithm for each of the following tasks:</span></span>

-   <span data-ttu-id="7ebcf-107">обмена ключами;</span><span class="sxs-lookup"><span data-stu-id="7ebcf-107">Key exchange</span></span>
-   <span data-ttu-id="7ebcf-108">массового шифрования;</span><span class="sxs-lookup"><span data-stu-id="7ebcf-108">Bulk encryption</span></span>
-   <span data-ttu-id="7ebcf-109">проверки подлинности сообщений.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-109">Message authentication</span></span>

<span data-ttu-id="7ebcf-110">[*Алгоритмы обмена ключами*](/windows/desktop/SecGloss/k-gly) защищают сведения, необходимые для создания общих ключей.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-110">[*Key exchange algorithms*](/windows/desktop/SecGloss/k-gly) protect information required to create shared keys.</span></span> <span data-ttu-id="7ebcf-111">Эти алгоритмы являются асимметричными ([*алгоритмы открытого ключа*](/windows/desktop/SecGloss/p-gly)) и хорошо работают для относительно небольших объемов данных.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-111">These algorithms are asymmetric ([*public key algorithms*](/windows/desktop/SecGloss/p-gly)) and perform well for relatively small amounts of data.</span></span>

<span data-ttu-id="7ebcf-112">Алгоритмы блочного шифрования шифруют сообщения, которыми обмениваются клиенты и серверы.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-112">Bulk encryption algorithms encrypt messages exchanged between clients and servers.</span></span> <span data-ttu-id="7ebcf-113">Эти алгоритмы являются [*симметричными*](/windows/desktop/SecGloss/s-gly) и хорошо работают для больших объемов данных.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-113">These algorithms are [*symmetric*](/windows/desktop/SecGloss/s-gly) and perform well for large amounts of data.</span></span>

<span data-ttu-id="7ebcf-114">Алгоритмы [проверки подлинности сообщений](message-authentication-codes-in-schannel.md) генерируют [*хэши*](/windows/desktop/SecGloss/h-gly) и подписи сообщений, гарантирующие [*целостность*](/windows/desktop/SecGloss/i-gly) сообщения.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-114">[Message authentication](message-authentication-codes-in-schannel.md) algorithms generate message [*hashes*](/windows/desktop/SecGloss/h-gly) and signatures that ensure the [*integrity*](/windows/desktop/SecGloss/i-gly) of a message.</span></span>

<span data-ttu-id="7ebcf-115">Разработчики указывают эти элементы с помощью типов данных [**\_ идентификаторов ALG**](/windows/desktop/SecCrypto/alg-id) .</span><span class="sxs-lookup"><span data-stu-id="7ebcf-115">Developers specify these elements by using [**ALG\_ID**](/windows/desktop/SecCrypto/alg-id) data types.</span></span> <span data-ttu-id="7ebcf-116">Дополнительные сведения см. в разделе [Указание шифров SChannel и стойкости шифра](specifying-schannel-ciphers-and-cipher-strengths.md).</span><span class="sxs-lookup"><span data-stu-id="7ebcf-116">For more information, see [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).</span></span>

<span data-ttu-id="7ebcf-117">В более ранних версиях Windows наборы шифров TLS и эллиптические кривые были настроены с помощью одной строки:</span><span class="sxs-lookup"><span data-stu-id="7ebcf-117">In earlier versions of Windows, TLS cipher suites and elliptical curves were configured by using a single string:</span></span>

![Схема, на которой показана одна строка для комплекта шифров.](images/tls-cipher-suite.png)

<span data-ttu-id="7ebcf-119">Разные версии Windows поддерживают разные наборы шифров TLS и порядок приоритетов.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-119">Different Windows versions support different TLS cipher suites and priority order.</span></span> <span data-ttu-id="7ebcf-120">См. соответствующий номер версии Windows по умолчанию, в котором они выбираются поставщиком Schannel (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="7ebcf-120">See the corresponding Windows version for the default order in which they are chosen by the Microsoft Schannel Provider.</span></span>

<span data-ttu-id="7ebcf-121">**Windows Server 2022:** Сведения о поддерживаемых комплектах шифров см. в разделе комплекты [шифров TLS в Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md) .</span><span class="sxs-lookup"><span data-stu-id="7ebcf-121">**Windows Server 2022:** For information about supported cipher suites, see [TLS Cipher Suites in Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md)</span></span>

<span data-ttu-id="7ebcf-122">**Windows 10, версия 1903:** Сведения о поддерживаемых комплектах шифров см. в статье комплекты [шифров TLS в Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)</span><span class="sxs-lookup"><span data-stu-id="7ebcf-122">**Windows 10, version 1903:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)</span></span>

<span data-ttu-id="7ebcf-123">**Windows 10, версия 1809:** Сведения о поддерживаемых комплектах шифров см. в статье комплекты [шифров TLS в Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)</span><span class="sxs-lookup"><span data-stu-id="7ebcf-123">**Windows 10, version 1809:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)</span></span>

<span data-ttu-id="7ebcf-124">**Windows 10, версия 1803:** Сведения о поддерживаемых комплектах шифров см. в статье комплекты [шифров TLS в Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)</span><span class="sxs-lookup"><span data-stu-id="7ebcf-124">**Windows 10, version 1803:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)</span></span>

<span data-ttu-id="7ebcf-125">**Windows 10, версия 1709:** Сведения о поддерживаемых комплектах шифров см. в статье комплекты [шифров TLS в Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)</span><span class="sxs-lookup"><span data-stu-id="7ebcf-125">**Windows 10, version 1709:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)</span></span>

<span data-ttu-id="7ebcf-126">**Windows 10, версия 1703:** Сведения о поддерживаемых комплектах шифров см. в статье комплекты [шифров TLS в Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)</span><span class="sxs-lookup"><span data-stu-id="7ebcf-126">**Windows 10, version 1703:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)</span></span>

<span data-ttu-id="7ebcf-127">**Windows Server 2016 и Windows 10, версия 1607:** Сведения о поддерживаемых комплектах шифров см. в статье комплекты [шифров TLS в Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)</span><span class="sxs-lookup"><span data-stu-id="7ebcf-127">**Windows Server 2016 and Windows 10, version 1607:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)</span></span>

<span data-ttu-id="7ebcf-128">**Windows 10, версия 1511:** Сведения о поддерживаемых комплектах шифров см. в статье комплекты [шифров TLS в Windows 10 клиенте v1511 установлен](tls-cipher-suites-in-windows-10-v1511.md)</span><span class="sxs-lookup"><span data-stu-id="7ebcf-128">**Windows 10, version 1511:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)</span></span>

<span data-ttu-id="7ebcf-129">**Windows 10, версия 1507:** Сведения о поддерживаемых комплектах шифров см. в статье комплекты [шифров TLS в Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)</span><span class="sxs-lookup"><span data-stu-id="7ebcf-129">**Windows 10, version 1507:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)</span></span>

<span data-ttu-id="7ebcf-130">**Windows Server 2012 R2 и Windows 8.1:** Сведения о поддерживаемых комплектах шифров см. [в разделе наборы шифров TLS в Windows 8.1](tls-cipher-suites-in-windows-8-1.md)</span><span class="sxs-lookup"><span data-stu-id="7ebcf-130">**Windows Server 2012 R2 and Windows 8.1:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 8.1](tls-cipher-suites-in-windows-8-1.md)</span></span>

<span data-ttu-id="7ebcf-131">**Windows Server 2012 и Windows 8:** Дополнительные сведения о поддерживаемых комплектах шифров см. в статье комплекты [шифров TLS в Windows 8](tls-cipher-suites-in-windows-8.md) .</span><span class="sxs-lookup"><span data-stu-id="7ebcf-131">**Windows Server 2012 and Windows 8:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 8](tls-cipher-suites-in-windows-8.md)</span></span>

<span data-ttu-id="7ebcf-132">**Windows Server 2008 R2 и Windows 7:** Дополнительные сведения о поддерживаемых комплектах шифров см. в статье комплекты [шифров TLS в Windows 7](tls-cipher-suites-in-windows-7.md) .</span><span class="sxs-lookup"><span data-stu-id="7ebcf-132">**Windows Server 2008 R2 and Windows 7:** For information about supported cipher suites, see [TLS Cipher Suites in Windows 7](tls-cipher-suites-in-windows-7.md)</span></span>

<span data-ttu-id="7ebcf-133">**Windows Server 2008 и Windows Vista:** Дополнительные сведения о поддерживаемых комплектах шифров см. в статье комплекты [шифров TLS в Windows Vista](schannel-cipher-suites-in-windows-vista.md) .</span><span class="sxs-lookup"><span data-stu-id="7ebcf-133">**Windows Server 2008 and Windows Vista:** For information about supported cipher suites, see [TLS Cipher Suites in Windows Vista](schannel-cipher-suites-in-windows-vista.md)</span></span>

<span data-ttu-id="7ebcf-134">**Windows Server 2003 и Windows XP:** Дополнительные сведения о поддерживаемых комплектах шифров см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-134">**Windows Server 2003 and Windows XP:** For information about supported cipher suites, see the following topics.</span></span>

| <span data-ttu-id="7ebcf-135">Раздел</span><span class="sxs-lookup"><span data-stu-id="7ebcf-135">Topic</span></span>                                                                         | <span data-ttu-id="7ebcf-136">Описание</span><span class="sxs-lookup"><span data-stu-id="7ebcf-136">Description</span></span>                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ebcf-137">Комплекты шифров TLS</span><span class="sxs-lookup"><span data-stu-id="7ebcf-137">TLS Cipher Suites</span></span>](tls-cipher-suites.md)<br/>                         | <span data-ttu-id="7ebcf-138">Сведения о комплектах шифров, доступных по протоколу TLS в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-138">Information about the cipher suites available with the TLS protocol in Windows Server 2003 and Windows XP.</span></span><br/>              |
| [<span data-ttu-id="7ebcf-139">Протокол SSL</span><span class="sxs-lookup"><span data-stu-id="7ebcf-139">Secure Sockets Layer Protocol</span></span>](secure-sockets-layer-protocol.md)<br/> | <span data-ttu-id="7ebcf-140">Общие сведения о SSL 2,0 и 3,0, включая доступные комплекты шифров в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-140">General information about SSL 2.0 and 3.0, including the available cipher suites in Windows Server 2003 and Windows XP.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="7ebcf-141">До Windows 10 строки комплекта шифров были добавлены с эллиптической кривой для определения приоритета кривой.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-141">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="7ebcf-142">Windows 10 поддерживает настройку порядка приоритетов на основе эллиптических кривых, поэтому суффикс эллиптической кривой не является обязательным и переопределяется новым порядковым приоритетом эллиптической кривой, когда он предоставляется, чтобы разрешить организациям использовать групповую политику для настройки различных версий Windows с одинаковыми комплектами шифров.</span><span class="sxs-lookup"><span data-stu-id="7ebcf-142">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>

 

