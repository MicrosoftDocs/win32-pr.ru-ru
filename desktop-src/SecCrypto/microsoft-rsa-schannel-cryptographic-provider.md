---
description: Поставщик служб шифрования Microsoft RSA/SChannel поддерживает хеширование, подписывание данных и проверку подписей.
ms.assetid: 34ede85a-579f-400f-a53e-e40711fcaaf3
title: Поставщик служб шифрования Microsoft RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9420849d62c0b728d8f3dbccc4210de3a1394308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991186"
---
# <a name="microsoft-rsaschannel-cryptographic-provider"></a><span data-ttu-id="761d1-103">Поставщик служб шифрования Microsoft RSA/SChannel</span><span class="sxs-lookup"><span data-stu-id="761d1-103">Microsoft RSA/Schannel Cryptographic Provider</span></span>

<span data-ttu-id="761d1-104">Поставщик криптографии Microsoft [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) поддерживает хеширование, подписывание данных и проверку подписей.</span><span class="sxs-lookup"><span data-stu-id="761d1-104">The Microsoft [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) Cryptographic Provider supports hashing, data signing, and signature verification.</span></span> <span data-ttu-id="761d1-105">Идентификатор алгоритма КАЛГ \_ SSL3 \_ SHAMD5 используется для проверки подлинности клиента SSL 3,0 и TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="761d1-105">The algorithm identifier CALG\_SSL3\_SHAMD5 is used for SSL 3.0 and TLS 1.0 client authentication.</span></span> <span data-ttu-id="761d1-106">Этот CSP поддерживает получение ключей для протоколов SSL2, PCT1, SSL3 и TLS1.</span><span class="sxs-lookup"><span data-stu-id="761d1-106">This CSP supports key derivation for the SSL2, PCT1, SSL3, and TLS1 protocols.</span></span> <span data-ttu-id="761d1-107">[*Хэш*](../secgloss/h-gly.md) состоит из объединения хэша MD5 с хэшем SHA и подписанного [*закрытым ключом*](../secgloss/p-gly.md)RSA.</span><span class="sxs-lookup"><span data-stu-id="761d1-107">The [*hash*](../secgloss/h-gly.md) consists of a concatenation of a MD5 hash with a SHA hash and signed with a RSA [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="761d1-108">Его можно экспортировать в другие страны и регионы.</span><span class="sxs-lookup"><span data-stu-id="761d1-108">It can be exported to other countries/regions.</span></span>



|                |                                  |
|----------------|----------------------------------|
| <span data-ttu-id="761d1-109">Тип поставщика:</span><span class="sxs-lookup"><span data-stu-id="761d1-109">Provider type:</span></span> | <span data-ttu-id="761d1-110">**PROV \_ RSA \_ SChannel**</span><span class="sxs-lookup"><span data-stu-id="761d1-110">**PROV\_RSA\_SCHANNEL**</span></span>          |
| <span data-ttu-id="761d1-111">Имя поставщика:</span><span class="sxs-lookup"><span data-stu-id="761d1-111">Provider name:</span></span> | <span data-ttu-id="761d1-112">**MS \_ DEF \_ RSA \_ SChannel \_ Prov**</span><span class="sxs-lookup"><span data-stu-id="761d1-112">**MS\_DEF\_RSA\_SCHANNEL\_PROV**</span></span> |



 

<span data-ttu-id="761d1-113">Дополнительные сведения о поставщиках RSA/SChannel см. в разделе [функции CSP](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="761d1-113">For more information about RSA/Schannel providers, see [CSP Functions](cryptography-functions.md).</span></span>

 

 
