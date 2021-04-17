---
description: Объясняется, как создать КАЛГ \_ SSL3 \_ SHAMD5 hash.
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Создание CALG_SSL3_SHAMD5ного хэша
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663622"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a><span data-ttu-id="05a5e-103">Создание КАЛГ \_ SSL3 \_ SHAMD5 hash</span><span class="sxs-lookup"><span data-stu-id="05a5e-103">Creating a CALG\_SSL3\_SHAMD5 Hash</span></span>

<span data-ttu-id="05a5e-104">**Создание КАЛГ \_ SSL3 \_ SHAMD5 hash**</span><span class="sxs-lookup"><span data-stu-id="05a5e-104">**To create a CALG\_SSL3\_SHAMD5 hash**</span></span>

1.  <span data-ttu-id="05a5e-105">Используя стандартную методологию CryptoAPI, создайте MD5 и хэш [*SHA*](../secgloss/s-gly.md) [](../secgloss/h-gly.md) для целевых данных.</span><span class="sxs-lookup"><span data-stu-id="05a5e-105">Using standard CryptoAPI methodology, create both a MD5 and a [*SHA*](../secgloss/s-gly.md) [*hash*](../secgloss/h-gly.md) of the target data.</span></span>
2.  <span data-ttu-id="05a5e-106">Объедините два хэша со значением MD5, крайним левым и самым правым SHA.</span><span class="sxs-lookup"><span data-stu-id="05a5e-106">Concatenate the two hashes, with the MD5 value leftmost and the SHA value rightmost.</span></span> <span data-ttu-id="05a5e-107">Это приводит к 36-байтному значению (16 байт + 20 байт).</span><span class="sxs-lookup"><span data-stu-id="05a5e-107">This results in a 36-byte value (16 bytes + 20 bytes).</span></span>
3.  <span data-ttu-id="05a5e-108">Получите маркер для [*объекта хэша*](../secgloss/h-gly.md) , вызвав [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) с калг \_ SSL3 \_ SHAMD5, переданным в параметр *алгид* .</span><span class="sxs-lookup"><span data-stu-id="05a5e-108">Get a handle to a [*hash object*](../secgloss/h-gly.md) by calling [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with CALG\_SSL3\_SHAMD5 passed in the *Algid* parameter.</span></span>
4.  <span data-ttu-id="05a5e-109">Задайте хэш-значение с помощью вызова [**криптсесашпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span><span class="sxs-lookup"><span data-stu-id="05a5e-109">Set the hash value with a call to [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span></span> <span data-ttu-id="05a5e-110">Объединенные хэш-значения передаются в виде **байта** \* в параметре *PBDATA* , и \_ значение HP хашвал должно быть передано в параметр *двпарам* .</span><span class="sxs-lookup"><span data-stu-id="05a5e-110">The concatenated hash values are passed as a **BYTE**\* in the *pbData* parameter, and the HP\_HASHVAL value must be passed in the *dwParam* parameter.</span></span> <span data-ttu-id="05a5e-111">Вызов [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) с помощью маркера, возвращенного [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) на шаге 3, завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="05a5e-111">Calling [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) using the handle returned by [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) in step 3 will fail.</span></span>
5.  <span data-ttu-id="05a5e-112">Вызовите [**криптсигнхаш**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) , чтобы создать сигнатуру.</span><span class="sxs-lookup"><span data-stu-id="05a5e-112">Call [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) to generate the signature.</span></span>
6.  <span data-ttu-id="05a5e-113">Вызовите [**криптдестройхаш**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) , чтобы уничтожить хэш-объект.</span><span class="sxs-lookup"><span data-stu-id="05a5e-113">Call [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) to destroy the hash object.</span></span>

 

 
