---
description: Поддерживает протоколы RSA и SChannel.
ms.assetid: f0c11a04-7931-424a-b085-0cc584ea7bb7
title: PROV_RSA_SCHANNEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a76d7f5339f2e7f60ac34705437b1ef0a773fd6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815753"
---
# <a name="prov_rsa_schannel"></a><span data-ttu-id="dd2db-103">PROV \_ RSA \_ SChannel</span><span class="sxs-lookup"><span data-stu-id="dd2db-103">PROV\_RSA\_SCHANNEL</span></span>

<span data-ttu-id="dd2db-104">\_ \_ Тип поставщика Prov RSA SChannel поддерживает протоколы RSA и [*SChannel*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="dd2db-104">The PROV\_RSA\_SCHANNEL provider type supports both RSA and [*Schannel*](../secgloss/s-gly.md) protocols.</span></span>

## <a name="algorithms-supported"></a><span data-ttu-id="dd2db-105">Поддерживаемые алгоритмы</span><span class="sxs-lookup"><span data-stu-id="dd2db-105">Algorithms Supported</span></span>

<span data-ttu-id="dd2db-106">Описание каждого из этих алгоритмов см. в глоссарии.</span><span class="sxs-lookup"><span data-stu-id="dd2db-106">For descriptions of each of these algorithms, see the glossary.</span></span>



| <span data-ttu-id="dd2db-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="dd2db-107">Purpose</span></span>      | <span data-ttu-id="dd2db-108">Поддерживаемые алгоритмы</span><span class="sxs-lookup"><span data-stu-id="dd2db-108">Supported algorithms</span></span>                                                                                                                                                                                                                                                                                                          |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2db-109">Обмен ключами</span><span class="sxs-lookup"><span data-stu-id="dd2db-109">Key Exchange</span></span> | [<span data-ttu-id="dd2db-110">*RSA*</span><span class="sxs-lookup"><span data-stu-id="dd2db-110">*RSA*</span></span>](../secgloss/r-gly.md)                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="dd2db-111">Подпись</span><span class="sxs-lookup"><span data-stu-id="dd2db-111">Signature</span></span>    | <span data-ttu-id="dd2db-112">RSA</span><span class="sxs-lookup"><span data-stu-id="dd2db-112">RSA</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="dd2db-113">Шифрование</span><span class="sxs-lookup"><span data-stu-id="dd2db-113">Encryption</span></span>   | <span data-ttu-id="dd2db-114">Любой \_ CSP Prov RSA \_ SChannel должен реализовывать один или несколько из следующих алгоритмов: [ *RC4*](../secgloss/r-gly.md)</span><span class="sxs-lookup"><span data-stu-id="dd2db-114">Any PROV\_RSA\_SCHANNEL CSP must implement one or more of the following algorithms: [*RC4*](../secgloss/r-gly.md)</span></span><br/> [<span data-ttu-id="dd2db-115">*DES*</span><span class="sxs-lookup"><span data-stu-id="dd2db-115">*DES*</span></span>](../secgloss/d-gly.md)<br/> [<span data-ttu-id="dd2db-116">*Triple DES*</span><span class="sxs-lookup"><span data-stu-id="dd2db-116">*Triple DES*</span></span>](../secgloss/t-gly.md)<br/> |
| <span data-ttu-id="dd2db-117">Хэширование</span><span class="sxs-lookup"><span data-stu-id="dd2db-117">Hashing</span></span>      | <span data-ttu-id="dd2db-118">[*MD5*](../secgloss/m-gly.md)[*SHA*](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="dd2db-118">[*MD5*](../secgloss/m-gly.md)[*SHA*](../secgloss/s-gly.md)</span></span><br/>                                                                                                                                                                                             |



 

 

 
