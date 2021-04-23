---
description: Задает или получает длину ключа.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Свойство Algorithm. KeyLength
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685103"
---
# <a name="algorithmkeylength-property"></a><span data-ttu-id="7b4a8-103">Свойство Algorithm. KeyLength</span><span class="sxs-lookup"><span data-stu-id="7b4a8-103">Algorithm.KeyLength property</span></span>

<span data-ttu-id="7b4a8-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="7b4a8-105">Вместо этого используйте [**класс алгорисмидентифиер**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="7b4a8-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7b4a8-106">Свойство **keylength** задает или получает длину ключа.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-106">The **KeyLength** property sets or retrieves the length of the key.</span></span>

<span data-ttu-id="7b4a8-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4a8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b4a8-108">Syntax</span></span>


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a><span data-ttu-id="7b4a8-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7b4a8-109">Property value</span></span>

<span data-ttu-id="7b4a8-110">Значение перечисления [**\_ \_ \_ длины ключа шифрования CAPICOM**](capicom-encryption-key-length.md) , указывающее длину ключа.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-110">A value of the [**CAPICOM\_ENCRYPTION\_KEY\_LENGTH**](capicom-encryption-key-length.md) enumeration that specifies the key length.</span></span> <span data-ttu-id="7b4a8-111">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="7b4a8-112">Значение</span><span class="sxs-lookup"><span data-stu-id="7b4a8-112">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="7b4a8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7b4a8-113">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <span data-ttu-id="7b4a8-114"><dt>**\_ \_ \_ Максимальная длина ключа шифрования \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4a8-114"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</dt></span></span> </dl>     | <span data-ttu-id="7b4a8-115">Используйте максимальную длину ключа, доступную в указанном алгоритме шифрования.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-115">Use the maximum key length available with the indicated encryption algorithm.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <span data-ttu-id="7b4a8-116"><dt>**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 40 \_ бит**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4a8-116"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="7b4a8-117">Используйте 40-разрядные ключи.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-117">Use 40-bit keys.</span></span><br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <span data-ttu-id="7b4a8-118"><dt>**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 56 \_ бит**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4a8-118"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="7b4a8-119">Используйте 56-разрядные ключи, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-119">Use 56-bit keys if available.</span></span><br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <span data-ttu-id="7b4a8-120"><dt>**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 128 \_ бит**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4a8-120"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</dt></span></span> </dl> | <span data-ttu-id="7b4a8-121">Используйте 128-разрядные ключи, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-121">Use 128-bit keys if available.</span></span><br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <span data-ttu-id="7b4a8-122"><dt>**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 192 \_ бит**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4a8-122"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</dt></span></span> </dl> | <span data-ttu-id="7b4a8-123">Используйте 192-разрядные ключи.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-123">Use 192-bit keys.</span></span> <span data-ttu-id="7b4a8-124">Эта длина ключа доступна только для алгоритма AES.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-124">This key length is available only for AES.</span></span><br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <span data-ttu-id="7b4a8-125"><dt>**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 256 \_ бит**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4a8-125"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</dt></span></span> </dl> | <span data-ttu-id="7b4a8-126">Используйте 256-разрядные ключи.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-126">Use 256-bit keys.</span></span> <span data-ttu-id="7b4a8-127">Эта длина ключа доступна только для алгоритма AES.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-127">This key length is available only for AES.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="7b4a8-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b4a8-128">Remarks</span></span>

<span data-ttu-id="7b4a8-129">При использовании алгоритмов шифрования DES и 3DES Длина ключей составляет Standard, а свойство **keylength** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="7b4a8-129">When DES and 3DES encryption algorithms are used, the key lengths are standard and the **KeyLength** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4a8-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7b4a8-130">Requirements</span></span>



| <span data-ttu-id="7b4a8-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7b4a8-131">Requirement</span></span> | <span data-ttu-id="7b4a8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7b4a8-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4a8-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7b4a8-133">End of client support</span></span><br/> | <span data-ttu-id="7b4a8-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b4a8-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7b4a8-135">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7b4a8-135">End of server support</span></span><br/> | <span data-ttu-id="7b4a8-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b4a8-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7b4a8-137">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7b4a8-137">Redistributable</span></span><br/>       | <span data-ttu-id="7b4a8-138">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="7b4a8-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7b4a8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7b4a8-139">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7b4a8-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b4a8-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b4a8-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b4a8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4a8-142">**Алгоритм**</span><span class="sxs-lookup"><span data-stu-id="7b4a8-142">**Algorithm**</span></span>](algorithm.md)
</dt> </dl>

 

 
