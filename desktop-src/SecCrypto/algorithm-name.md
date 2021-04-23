---
description: Задает или получает алгоритм, используемый для подписывания, запечатывание и шифрования операций. Это свойство по умолчанию.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Algorithm.Name, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 35ff147d8db7fb409787fa938a951dfc0a2320e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665134"
---
# <a name="algorithmname-property"></a><span data-ttu-id="f4ab1-104">Algorithm.Name, свойство</span><span class="sxs-lookup"><span data-stu-id="f4ab1-104">Algorithm.Name property</span></span>

<span data-ttu-id="f4ab1-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="f4ab1-106">Вместо этого используйте [**класс алгорисмидентифиер**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="f4ab1-106">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f4ab1-107">Свойство **Name** задает или получает алгоритм, используемый для подписывания, запечатывание и шифрования операций.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-107">The **Name** property sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="f4ab1-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-108">This is the default property.</span></span>

<span data-ttu-id="f4ab1-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ab1-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4ab1-110">Syntax</span></span>


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="f4ab1-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f4ab1-111">Property value</span></span>

<span data-ttu-id="f4ab1-112">Значение перечисления [**\_ \_ алгоритма CAPICOM**](capicom-encryption-algorithm.md) , указывающее используемый алгоритм.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-112">A value of the [**CAPICOM\_ENCRYPTION\_ALGORITHM**](capicom-encryption-algorithm.md) enumeration that specifies which algorithm to use.</span></span> <span data-ttu-id="f4ab1-113">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="f4ab1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f4ab1-114">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="f4ab1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f4ab1-115">Meaning</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <span data-ttu-id="f4ab1-116"><dt>**\_Алгоритм шифрования \_ CAPICOM \_ RC2**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ab1-116"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</dt></span></span> </dl>    | <span data-ttu-id="f4ab1-117">Используйте шифрование RC2.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-117">Use RC2 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <span data-ttu-id="f4ab1-118"><dt>**\_Алгоритм шифрования \_ CAPICOM \_ RC4**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ab1-118"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</dt></span></span> </dl>    | <span data-ttu-id="f4ab1-119">Используйте алгоритм шифрования RC4.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-119">Use RC4 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <span data-ttu-id="f4ab1-120"><dt>**\_алгоритм шифрования \_ CAPICOM \_ des**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ab1-120"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</dt></span></span> </dl>    | <span data-ttu-id="f4ab1-121">Используйте шифрование DES.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-121">Use DES encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <span data-ttu-id="f4ab1-122"><dt>**\_Алгоритм шифрования \_ CAPICOM \_ 3DES**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ab1-122"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</dt></span></span> </dl> | <span data-ttu-id="f4ab1-123">Используйте тройное шифрование DES.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-123">Use triple DES encryption.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <span data-ttu-id="f4ab1-124"><dt>**\_алгоритм шифрования \_ CAPICOM \_ AES**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ab1-124"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</dt></span></span> </dl>    | <span data-ttu-id="f4ab1-125">Используйте алгоритм AES.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-125">Use the AES algorithm.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="f4ab1-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4ab1-126">Remarks</span></span>

<span data-ttu-id="f4ab1-127">Когда значение этого свойства сбрасывается прямо или косвенно, полное состояние объекта сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="f4ab1-127">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ab1-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f4ab1-128">Requirements</span></span>



| <span data-ttu-id="f4ab1-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f4ab1-129">Requirement</span></span> | <span data-ttu-id="f4ab1-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f4ab1-130">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ab1-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f4ab1-131">End of client support</span></span><br/> | <span data-ttu-id="f4ab1-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4ab1-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f4ab1-133">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f4ab1-133">End of server support</span></span><br/> | <span data-ttu-id="f4ab1-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4ab1-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f4ab1-135">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f4ab1-135">Redistributable</span></span><br/>       | <span data-ttu-id="f4ab1-136">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4ab1-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f4ab1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f4ab1-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f4ab1-138"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4ab1-138"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
