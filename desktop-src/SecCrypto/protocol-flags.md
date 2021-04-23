---
description: Стандартные константы для протоколов шифрования. Эти значения определены в Винкрипт. h.
ms.assetid: 61dc0eff-2033-464a-a558-1798a92d48a2
title: Флаги протокола (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25804763e407ff2a12e5657878e343f483d353e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999133"
---
# <a name="protocol-flags"></a><span data-ttu-id="efa12-104">Флаги протокола</span><span class="sxs-lookup"><span data-stu-id="efa12-104">Protocol Flags</span></span>

<span data-ttu-id="efa12-105">Ниже приведены стандартные константы для протоколов шифрования.</span><span class="sxs-lookup"><span data-stu-id="efa12-105">The following are predefined constants for cryptography protocols.</span></span> <span data-ttu-id="efa12-106">Эти значения определены в Винкрипт. h.</span><span class="sxs-lookup"><span data-stu-id="efa12-106">These values are defined in Wincrypt.h.</span></span>



| <span data-ttu-id="efa12-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="efa12-107">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="efa12-108">Описание</span><span class="sxs-lookup"><span data-stu-id="efa12-108">Description</span></span>                                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="CRYPT_FLAG_IPSEC"></span><span id="crypt_flag_ipsec"></span><dl> <span data-ttu-id="efa12-109"><dt>**Шифрования \_ ФЛАГ \_ IPSec**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="efa12-109"><dt>**CRYPT\_FLAG\_IPSEC**</dt> <dt>0x0010</dt></span></span> </dl>       | <span data-ttu-id="efa12-110">Протокол IPsec.</span><span class="sxs-lookup"><span data-stu-id="efa12-110">Internet protocol security (IPsec) protocol.</span></span><br/>               |
| <span id="CRYPT_FLAG_PCT1"></span><span id="crypt_flag_pct1"></span><dl> <span data-ttu-id="efa12-111"><dt>**Шифрования \_ ФЛАГ \_ PCT1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="efa12-111"><dt>**CRYPT\_FLAG\_PCT1**</dt> <dt>0x0001</dt></span></span> </dl>          | <span data-ttu-id="efa12-112">Протокол передачи частных соединений (PCT) версии 1.</span><span class="sxs-lookup"><span data-stu-id="efa12-112">Private communications transport (PCT) version 1 protocol.</span></span><br/> |
| <span id="CRYPT_FLAG_SIGNING"></span><span id="crypt_flag_signing"></span><dl> <span data-ttu-id="efa12-113"><dt>**Шифрования \_ ФЛАГ \_ подписи**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="efa12-113"><dt>**CRYPT\_FLAG\_SIGNING**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="efa12-114">Протокол подписывания.</span><span class="sxs-lookup"><span data-stu-id="efa12-114">Signing protocol.</span></span><br/>                                          |
| <span id="CRYPT_FLAG_SSL2"></span><span id="crypt_flag_ssl2"></span><dl> <span data-ttu-id="efa12-115"><dt>**Шифрования \_ ФЛАГ \_ SSL2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="efa12-115"><dt>**CRYPT\_FLAG\_SSL2**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="efa12-116">Протокол SSL версии 2.</span><span class="sxs-lookup"><span data-stu-id="efa12-116">Secure sockets layer (SSL) version 2 protocol.</span></span><br/>             |
| <span id="CRYPT_FLAG_SSL3"></span><span id="crypt_flag_ssl3"></span><dl> <span data-ttu-id="efa12-117"><dt>**Шифрования \_ ФЛАГ \_ SSL3**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="efa12-117"><dt>**CRYPT\_FLAG\_SSL3**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="efa12-118">Протокол SSL версии 3.</span><span class="sxs-lookup"><span data-stu-id="efa12-118">SSL version 3 protocol.</span></span><br/>                                    |
| <span id="CRYPT_FLAG_TLS1"></span><span id="crypt_flag_tls1"></span><dl> <span data-ttu-id="efa12-119"><dt>**Шифрования \_ ФЛАГ \_ TLS1**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="efa12-119"><dt>**CRYPT\_FLAG\_TLS1**</dt> <dt>0x0008</dt></span></span> </dl>          | <span data-ttu-id="efa12-120">Протокол TLS версии 1.</span><span class="sxs-lookup"><span data-stu-id="efa12-120">Transport layer security (TLS) version 1 protocol.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="efa12-121">Требования</span><span class="sxs-lookup"><span data-stu-id="efa12-121">Requirements</span></span>



| <span data-ttu-id="efa12-122">Требование</span><span class="sxs-lookup"><span data-stu-id="efa12-122">Requirement</span></span> | <span data-ttu-id="efa12-123">Значение</span><span class="sxs-lookup"><span data-stu-id="efa12-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efa12-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efa12-124">Minimum supported client</span></span><br/> | <span data-ttu-id="efa12-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="efa12-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="efa12-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efa12-126">Minimum supported server</span></span><br/> | <span data-ttu-id="efa12-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="efa12-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="efa12-128">Header</span><span class="sxs-lookup"><span data-stu-id="efa12-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="efa12-129"><dt>Винкрипт. h</dt></span><span class="sxs-lookup"><span data-stu-id="efa12-129"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efa12-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efa12-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efa12-131">**PROV \_ енумалгс \_ ex**</span><span class="sxs-lookup"><span data-stu-id="efa12-131">**PROV\_ENUMALGS\_EX**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex)
</dt> </dl>

 

 




