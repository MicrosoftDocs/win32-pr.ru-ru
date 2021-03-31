---
description: SChannel использует CryptoAPI для криптографических операций, таких как хранение открытых и закрытых ключей.
ms.assetid: 5ad9a171-5f69-4035-aac5-ae8d27d0abfb
title: Schannel и CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0684cd690911444b77ba27d2876e578fd71c73a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423625"
---
# <a name="schannel-and-cryptoapi"></a><span data-ttu-id="af14b-103">Schannel и CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="af14b-103">Schannel and CryptoAPI</span></span>

<span data-ttu-id="af14b-104">SChannel использует [CryptoAPI](../seccrypto/cryptography-essentials.md) для криптографических операций, таких как хранение [*открытых и закрытых ключей*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="af14b-104">Schannel uses [CryptoAPI](../seccrypto/cryptography-essentials.md) for cryptographic operations such as storing [*public/private keys*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="af14b-105">В следующих разделах содержатся подробные сведения о том, как SChannel использует CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="af14b-105">The following topics provide detailed information about how Schannel makes use of CryptoAPI.</span></span>



| <span data-ttu-id="af14b-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="af14b-106">Topic</span></span>                                                                   | <span data-ttu-id="af14b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="af14b-107">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af14b-108">Хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="af14b-108">Certificate Stores</span></span>](certificate-stores.md)<br/>                 | <span data-ttu-id="af14b-109">Сертификаты клиента и сервера должны храниться в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="af14b-109">Both client and server certificates must be stored in a certificate store.</span></span><br/>                                |
| [<span data-ttu-id="af14b-110">CryptoAPI 2.0 закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="af14b-110">CryptoAPI 2.0 Private Keys</span></span>](cryptoapi-2-0-private-keys.md)<br/> | <span data-ttu-id="af14b-111">Учетные данные SChannel представляются внутренне как структуры [**\_ контекста сертификата**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="af14b-111">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span><br/> |



 

 

 
