---
description: Задает или получает тип используемого алгоритма хэширования.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: Хашеддата. algorithm, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a27dc275ce900bfd6412599cb81ad14038f96405
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685224"
---
# <a name="hasheddataalgorithm-property"></a><span data-ttu-id="cbd4c-103">Хашеддата. algorithm, свойство</span><span class="sxs-lookup"><span data-stu-id="cbd4c-103">HashedData.Algorithm property</span></span>

<span data-ttu-id="cbd4c-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="cbd4c-105">Вместо этого используйте [**класс HashAlgorithm**](/previous-versions/windows/) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="cbd4c-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="cbd4c-106">Свойство **Algorithm** задает или получает тип используемого алгоритма хэширования.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-106">The **Algorithm** property sets or retrieves the type of hashing algorithm used.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd4c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbd4c-107">Syntax</span></span>


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="cbd4c-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cbd4c-108">Property value</span></span>

<span data-ttu-id="cbd4c-109">Значение перечисления хэш [**\_ - \_ алгоритма CAPICOM**](capicom-hash-algorithm.md) , определяющее хэш-алгоритм.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-109">A value of the [**CAPICOM\_HASH\_ALGORITHM**](capicom-hash-algorithm.md) enumeration that defines a hash algorithm.</span></span> <span data-ttu-id="cbd4c-110">Значение по умолчанию — \_ алгоритм ХЭША CAPICOM \_ \_ SHA1.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-110">The default value is CAPICOM\_HASH\_ALGORITHM\_SHA1.</span></span> <span data-ttu-id="cbd4c-111">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="cbd4c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="cbd4c-112">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="cbd4c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="cbd4c-113">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <span data-ttu-id="cbd4c-114"><dt>**\_Алгоритм ХЭША \_ CAPICOM \_ SHA1**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd4c-114"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA1**</dt></span></span> </dl>           | <span data-ttu-id="cbd4c-115">Алгоритм хэширования SHA1.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-115">SHA1 hashing algorithm.</span></span><br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <span data-ttu-id="cbd4c-116"><dt>**\_ \_ MD2 алгоритма CAPICOM hash \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd4c-116"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD2**</dt></span></span> </dl>              | <span data-ttu-id="cbd4c-117">Алгоритм хэширования MD2.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-117">MD2 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <span data-ttu-id="cbd4c-118"><dt>**\_Хэш- \_ алгоритмы CAPICOM \_ MD4**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd4c-118"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD4**</dt></span></span> </dl>              | <span data-ttu-id="cbd4c-119">Алгоритм хэширования MD4.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-119">MD4 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <span data-ttu-id="cbd4c-120"><dt>**\_MD5- \_ алгоритм хеширования \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd4c-120"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD5**</dt></span></span> </dl>              | <span data-ttu-id="cbd4c-121">Алгоритм хэширования MD5.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-121">MD5 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <span data-ttu-id="cbd4c-122"><dt>**\_Хэш-алгоритм "CAPICOM hash \_ \_ SHA \_ 256"**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd4c-122"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</dt></span></span> </dl> | <span data-ttu-id="cbd4c-123">Алгоритм хеширования SHA-256.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-123">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="cbd4c-124">**CAPICOM 2.0.0.3 и более ранние версии:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-124">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <span data-ttu-id="cbd4c-125"><dt>**\_Хэш-алгоритм "CAPICOM hash \_ \_ SHA \_ 384"**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd4c-125"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</dt></span></span> </dl> | <span data-ttu-id="cbd4c-126">Алгоритм хеширования SHA-384.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="cbd4c-127">**CAPICOM 2.0.0.3 и более ранние версии:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <span data-ttu-id="cbd4c-128"><dt>**\_Хэш-алгоритм "CAPICOM hash \_ \_ SHA \_ 512"**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd4c-128"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</dt></span></span> </dl> | <span data-ttu-id="cbd4c-129">Алгоритм хеширования SHA-512.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-129">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="cbd4c-130">**CAPICOM 2.0.0.3 и более ранние версии:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-130">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cbd4c-131">Требования</span><span class="sxs-lookup"><span data-stu-id="cbd4c-131">Requirements</span></span>



| <span data-ttu-id="cbd4c-132">Требование</span><span class="sxs-lookup"><span data-stu-id="cbd4c-132">Requirement</span></span> | <span data-ttu-id="cbd4c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="cbd4c-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd4c-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cbd4c-134">End of client support</span></span><br/> | <span data-ttu-id="cbd4c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbd4c-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cbd4c-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="cbd4c-136">End of server support</span></span><br/> | <span data-ttu-id="cbd4c-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbd4c-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cbd4c-138">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="cbd4c-138">Redistributable</span></span><br/>       | <span data-ttu-id="cbd4c-139">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="cbd4c-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cbd4c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="cbd4c-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="cbd4c-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbd4c-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbd4c-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbd4c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd4c-143">**хашеддата**</span><span class="sxs-lookup"><span data-stu-id="cbd4c-143">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
