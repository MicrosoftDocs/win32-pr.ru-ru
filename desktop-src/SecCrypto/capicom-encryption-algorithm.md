---
description: Определяет алгоритмы, используемые при шифровании и расшифровке.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: Перечисление CAPICOM_ENCRYPTION_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668526"
---
# <a name="capicom_encryption_algorithm-enumeration"></a><span data-ttu-id="00f9f-103">\_ \_ Перечисление АЛГОРИТМа CAPICOM</span><span class="sxs-lookup"><span data-stu-id="00f9f-103">CAPICOM\_ENCRYPTION\_ALGORITHM enumeration</span></span>

<span data-ttu-id="00f9f-104">Тип перечисления для **\_ \_ алгоритма CAPICOM** определяет алгоритмы, используемые при шифровании и расшифровке.</span><span class="sxs-lookup"><span data-stu-id="00f9f-104">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type defines the algorithms to be used in encryption and decryption.</span></span>

## <a name="members"></a><span data-ttu-id="00f9f-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="00f9f-105">Members</span></span>



| <span data-ttu-id="00f9f-106">Член</span><span class="sxs-lookup"><span data-stu-id="00f9f-106">Member</span></span>                                   | <span data-ttu-id="00f9f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="00f9f-107">Description</span></span>                                                                                                                                                                                              | <span data-ttu-id="00f9f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="00f9f-108">Value</span></span>     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="00f9f-109">**\_Алгоритм шифрования \_ CAPICOM \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="00f9f-109">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</span></span>  | <span data-ttu-id="00f9f-110">Используйте шифрование RSA RC2.</span><span class="sxs-lookup"><span data-stu-id="00f9f-110">Use RSA RC2 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="00f9f-111">0</span><span class="sxs-lookup"><span data-stu-id="00f9f-111">0</span></span>         |
| <span data-ttu-id="00f9f-112">**\_Алгоритм шифрования \_ CAPICOM \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="00f9f-112">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</span></span>  | <span data-ttu-id="00f9f-113">Используйте шифрование RSA RC4.</span><span class="sxs-lookup"><span data-stu-id="00f9f-113">Use RSA RC4 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="00f9f-114">1</span><span class="sxs-lookup"><span data-stu-id="00f9f-114">1</span></span>         |
| <span data-ttu-id="00f9f-115">**\_алгоритм шифрования \_ CAPICOM \_ des**</span><span class="sxs-lookup"><span data-stu-id="00f9f-115">**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</span></span>  | <span data-ttu-id="00f9f-116">Используйте шифрование DES.</span><span class="sxs-lookup"><span data-stu-id="00f9f-116">Use DES encryption.</span></span><br/>                                                                                                                                                                           | <span data-ttu-id="00f9f-117">2</span><span class="sxs-lookup"><span data-stu-id="00f9f-117">2</span></span>         |
| <span data-ttu-id="00f9f-118">**\_Алгоритм шифрования \_ CAPICOM \_ 3DES**</span><span class="sxs-lookup"><span data-stu-id="00f9f-118">**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</span></span> | <span data-ttu-id="00f9f-119">Используйте тройное шифрование DES.</span><span class="sxs-lookup"><span data-stu-id="00f9f-119">Use triple DES encryption.</span></span><br/>                                                                                                                                                                    | <span data-ttu-id="00f9f-120">3</span><span class="sxs-lookup"><span data-stu-id="00f9f-120">3</span></span>         |
| <span data-ttu-id="00f9f-121">**\_алгоритм шифрования \_ CAPICOM \_ AES**</span><span class="sxs-lookup"><span data-stu-id="00f9f-121">**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</span></span>  | <span data-ttu-id="00f9f-122">Используйте алгоритм [*AES*](../secgloss/a-gly.md) (AES).</span><span class="sxs-lookup"><span data-stu-id="00f9f-122">Use the [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) algorithm.</span></span> <span data-ttu-id="00f9f-123">Это значение допустимо только для объекта [**EncryptedData**](encrypteddata.md) .</span><span class="sxs-lookup"><span data-stu-id="00f9f-123">This value is valid for the [**EncryptedData**](encrypteddata.md) object only.</span></span><br/> | <span data-ttu-id="00f9f-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="00f9f-124">4 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="00f9f-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00f9f-125">Remarks</span></span>

<span data-ttu-id="00f9f-126">Тип перечисления для **\_ \_ алгоритма CAPICOM-шифрования** используется свойством [**Algorithm.Name**](algorithm-name.md) .</span><span class="sxs-lookup"><span data-stu-id="00f9f-126">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type is used by the [**Algorithm.Name**](algorithm-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="00f9f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="00f9f-127">Requirements</span></span>



| <span data-ttu-id="00f9f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="00f9f-128">Requirement</span></span> | <span data-ttu-id="00f9f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="00f9f-129">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="00f9f-130">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="00f9f-130">Redistributable</span></span><br/> | <span data-ttu-id="00f9f-131">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="00f9f-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="00f9f-132">Header</span><span class="sxs-lookup"><span data-stu-id="00f9f-132">Header</span></span><br/>          | <dl> <span data-ttu-id="00f9f-133"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="00f9f-133"><dt>Capicom.h</dt></span></span> </dl> |



 

 
