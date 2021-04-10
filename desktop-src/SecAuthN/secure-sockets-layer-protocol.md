---
description: Сведения в этом разделе относятся к Windows Server 2003 и Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Протокол SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998394"
---
# <a name="secure-sockets-layer-protocol"></a><span data-ttu-id="afa6b-103">Протокол SSL</span><span class="sxs-lookup"><span data-stu-id="afa6b-103">Secure Sockets Layer Protocol</span></span>

<span data-ttu-id="afa6b-104">Сведения в этом разделе относятся к Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="afa6b-104">The information in this topic applies to Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="afa6b-105">Сведения о комплектах шифров для Windows Server 2008 и Windows Vista см. в разделе комплекты [шифров в SChannel](cipher-suites-in-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="afa6b-105">For cipher suites for Windows Server 2008 and Windows Vista, see [Cipher Suites in Schannel](cipher-suites-in-schannel.md).</span></span>

<span data-ttu-id="afa6b-106">Schannel поддерживает версии 2,0 и 3,0 [*протокола SSL (SSL)*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="afa6b-106">Schannel supports versions 2.0 and 3.0 of the [*Secure Sockets Layer (SSL) protocol*](../secgloss/s-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="afa6b-107">Начиная с Windows 10 версии 1607 и Windows Server 2016, протокол SSL 2,0 был удален и больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="afa6b-107">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

 

## <a name="ssl-30"></a><span data-ttu-id="afa6b-108">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="afa6b-108">SSL 3.0</span></span>

<span data-ttu-id="afa6b-109">SSL 3,0 является предшественником [протокола](transport-layer-security-protocol.md)TLS.</span><span class="sxs-lookup"><span data-stu-id="afa6b-109">SSL 3.0 is the predecessor of the [Transport Layer Security Protocol](transport-layer-security-protocol.md).</span></span>

<span data-ttu-id="afa6b-110">Schannel поддерживает комплекты шифров, перечисленные в разделе комплекты [шифров TLS](tls-cipher-suites.md) для SSL 3,0.</span><span class="sxs-lookup"><span data-stu-id="afa6b-110">Schannel supports the cipher suites listed under [TLS Cipher Suites](tls-cipher-suites.md) for SSL 3.0.</span></span> <span data-ttu-id="afa6b-111">SSL 3,0 поддерживает все комплекты шифров, перечисленные в разделе комплекты шифров TLS, а также SSL \_ Fortezza \_ Кеа \_ с помощью технологии \_ Fortezza \_ CBC \_ SHA.</span><span class="sxs-lookup"><span data-stu-id="afa6b-111">SSL 3.0 supports all of the cipher suites listed under TLS Cipher Suites as well as SSL\_FORTEZZA\_KEA\_WITH\_FORTEZZA\_CBC\_SHA.</span></span>

## <a name="ssl-20"></a><span data-ttu-id="afa6b-112">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="afa6b-112">SSL 2.0</span></span>

<span data-ttu-id="afa6b-113">Протокол SSL 2,0 был заменен протоколом TLS и не должен использоваться для новой разработки.</span><span class="sxs-lookup"><span data-stu-id="afa6b-113">SSL 2.0 has been superseded by TLS and should not be used for new development.</span></span>

<span data-ttu-id="afa6b-114">Schannel поддерживает следующие комплекты шифров для SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="afa6b-114">Schannel supports the following cipher suites for SSL 2.0.</span></span> <span data-ttu-id="afa6b-115">Эти наборы перечислены в порядке от наиболее безопасного до наименьшего уровня безопасности.</span><span class="sxs-lookup"><span data-stu-id="afa6b-115">The suites are listed in order from most secure to least secure.</span></span>

-   <span data-ttu-id="afa6b-116">SSL \_ RC4 \_ 128 \_ с \_ MD5</span><span class="sxs-lookup"><span data-stu-id="afa6b-116">SSL\_RC4\_128\_WITH\_MD5</span></span>
-   <span data-ttu-id="afa6b-117">SSL \_ DES \_ 192 \_ EDE3 \_ CBC \_ с \_ MD5</span><span class="sxs-lookup"><span data-stu-id="afa6b-117">SSL\_DES\_192\_EDE3\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="afa6b-118">SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ с \_ MD5</span><span class="sxs-lookup"><span data-stu-id="afa6b-118">SSL\_RC2\_CBC\_128\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="afa6b-119">SSL \_ DES \_ 64 \_ CBC \_ с \_ MD5</span><span class="sxs-lookup"><span data-stu-id="afa6b-119">SSL\_DES\_64\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="afa6b-120">SSL \_ RC4 \_ 128 \_ EXPORT40 \_ с \_ MD5</span><span class="sxs-lookup"><span data-stu-id="afa6b-120">SSL\_RC4\_128\_EXPORT40\_WITH\_MD5</span></span>

 

 
