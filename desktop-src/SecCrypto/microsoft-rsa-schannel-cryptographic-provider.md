---
description: Поставщик служб шифрования Microsoft RSA/SChannel поддерживает хеширование, подписывание данных и проверку подписей.
ms.assetid: 34ede85a-579f-400f-a53e-e40711fcaaf3
title: Поставщик служб шифрования Microsoft RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e1971f59911b36c3812a4508530a5e1801194
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581972"
---
# <a name="microsoft-rsaschannel-cryptographic-provider"></a><span data-ttu-id="be904-103">Поставщик служб шифрования Microsoft RSA/SChannel</span><span class="sxs-lookup"><span data-stu-id="be904-103">Microsoft RSA/Schannel Cryptographic Provider</span></span>

<span data-ttu-id="be904-104">Поставщик криптографии Microsoft [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) поддерживает хеширование, подписывание данных и проверку подписей.</span><span class="sxs-lookup"><span data-stu-id="be904-104">The Microsoft [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) Cryptographic Provider supports hashing, data signing, and signature verification.</span></span> <span data-ttu-id="be904-105">Идентификатор алгоритма КАЛГ \_ SSL3 \_ SHAMD5 используется для проверки подлинности клиента SSL 3,0 и TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="be904-105">The algorithm identifier CALG\_SSL3\_SHAMD5 is used for SSL 3.0 and TLS 1.0 client authentication.</span></span> <span data-ttu-id="be904-106">Этот CSP поддерживает получение ключей для протоколов SSL2, PCT1, SSL3 и TLS1.</span><span class="sxs-lookup"><span data-stu-id="be904-106">This CSP supports key derivation for the SSL2, PCT1, SSL3, and TLS1 protocols.</span></span> <span data-ttu-id="be904-107">[*Хэш*](../secgloss/h-gly.md) состоит из объединения хэша MD5 с хэшем SHA и подписанного [*закрытым ключом*](../secgloss/p-gly.md)RSA.</span><span class="sxs-lookup"><span data-stu-id="be904-107">The [*hash*](../secgloss/h-gly.md) consists of a concatenation of a MD5 hash with a SHA hash and signed with a RSA [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="be904-108">Его можно экспортировать в другие страны и регионы.</span><span class="sxs-lookup"><span data-stu-id="be904-108">It can be exported to other countries/regions.</span></span>



|                   | <span data-ttu-id="be904-109">Значение</span><span class="sxs-lookup"><span data-stu-id="be904-109">Value</span></span>                         |
|-------------------|-------------------------------|
| <span data-ttu-id="be904-110">**Тип поставщика**</span><span class="sxs-lookup"><span data-stu-id="be904-110">**Provider type**</span></span> | <span data-ttu-id="be904-111">PROV \_ RSA \_ SChannel</span><span class="sxs-lookup"><span data-stu-id="be904-111">PROV\_RSA\_SCHANNEL</span></span>           |
| <span data-ttu-id="be904-112">**Имя поставщика**</span><span class="sxs-lookup"><span data-stu-id="be904-112">**Provider name**</span></span> | <span data-ttu-id="be904-113">MS \_ DEF \_ RSA \_ SChannel \_ Prov</span><span class="sxs-lookup"><span data-stu-id="be904-113">MS\_DEF\_RSA\_SCHANNEL\_PROV</span></span>  |



 

<span data-ttu-id="be904-114">Дополнительные сведения о поставщиках RSA/SChannel см. в разделе [функции CSP](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="be904-114">For more information about RSA/Schannel providers, see [CSP Functions](cryptography-functions.md).</span></span>

 

 
