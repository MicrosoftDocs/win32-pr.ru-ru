---
description: Определяет длину ключа, используемую при шифровании.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: Перечисление CAPICOM_ENCRYPTION_KEY_LENGTH (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4f3e64df1e706ef20a83f4da5c81cda2a08ed331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669458"
---
# <a name="capicom_encryption_key_length-enumeration"></a><span data-ttu-id="dcf4b-103">\_ \_ Перечисление длины ключей шифрования CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="dcf4b-103">CAPICOM\_ENCRYPTION\_KEY\_LENGTH enumeration</span></span>

<span data-ttu-id="dcf4b-104">Тип перечисления " **\_ \_ \_ Длина ключа шифрования CAPICOM** " определяет [*длину ключа*](../secgloss/k-gly.md) , используемую при шифровании.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-104">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type defines the [*key length*](../secgloss/k-gly.md) to be used in encryption.</span></span>

## <a name="members"></a><span data-ttu-id="dcf4b-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="dcf4b-105">Members</span></span>



| <span data-ttu-id="dcf4b-106">Член</span><span class="sxs-lookup"><span data-stu-id="dcf4b-106">Member</span></span>                                          | <span data-ttu-id="dcf4b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="dcf4b-107">Description</span></span>                                                                               | <span data-ttu-id="dcf4b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="dcf4b-108">Value</span></span>     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="dcf4b-109">**\_ \_ \_ Максимальная длина ключа шифрования \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="dcf4b-109">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</span></span>   | <span data-ttu-id="dcf4b-110">Использует максимальную длину ключа, доступную в указанном алгоритме шифрования.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-110">Uses the maximum key length available with the indicated encryption algorithm.</span></span><br/> | <span data-ttu-id="dcf4b-111">0</span><span class="sxs-lookup"><span data-stu-id="dcf4b-111">0</span></span>         |
| <span data-ttu-id="dcf4b-112">**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 40 \_ бит**</span><span class="sxs-lookup"><span data-stu-id="dcf4b-112">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</span></span>  | <span data-ttu-id="dcf4b-113">Использует 40-разрядные ключи.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-113">Uses 40-bit keys.</span></span><br/>                                                              | <span data-ttu-id="dcf4b-114">1</span><span class="sxs-lookup"><span data-stu-id="dcf4b-114">1</span></span>         |
| <span data-ttu-id="dcf4b-115">**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 56 \_ бит**</span><span class="sxs-lookup"><span data-stu-id="dcf4b-115">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</span></span>  | <span data-ttu-id="dcf4b-116">Использует 56-разрядные ключи, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-116">Uses 56-bit keys if available.</span></span><br/>                                                 | <span data-ttu-id="dcf4b-117">2</span><span class="sxs-lookup"><span data-stu-id="dcf4b-117">2</span></span>         |
| <span data-ttu-id="dcf4b-118">**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 128 \_ бит**</span><span class="sxs-lookup"><span data-stu-id="dcf4b-118">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</span></span> | <span data-ttu-id="dcf4b-119">Использует 128-разрядные ключи, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-119">Uses 128-bit keys if available.</span></span><br/>                                                | <span data-ttu-id="dcf4b-120">3</span><span class="sxs-lookup"><span data-stu-id="dcf4b-120">3</span></span>         |
| <span data-ttu-id="dcf4b-121">**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 192 \_ бит**</span><span class="sxs-lookup"><span data-stu-id="dcf4b-121">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</span></span> | <span data-ttu-id="dcf4b-122">Использует 192-разрядные ключи.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-122">Uses 192-bit keys.</span></span> <span data-ttu-id="dcf4b-123">Эта длина ключа доступна только для алгоритма AES.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-123">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="dcf4b-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="dcf4b-124">4 // v2.0</span></span> |
| <span data-ttu-id="dcf4b-125">**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 256 \_ бит**</span><span class="sxs-lookup"><span data-stu-id="dcf4b-125">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</span></span> | <span data-ttu-id="dcf4b-126">Использует 256-разрядные ключи.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-126">Uses 256-bit keys.</span></span> <span data-ttu-id="dcf4b-127">Эта длина ключа доступна только для алгоритма AES.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-127">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="dcf4b-128">5//v 2.0</span><span class="sxs-lookup"><span data-stu-id="dcf4b-128">5 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="dcf4b-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcf4b-129">Remarks</span></span>

<span data-ttu-id="dcf4b-130">Тип перечисления " **CAPICOM" \_ \_ \_ длины ключа шифрования** используется свойством [**Algorithm. keylength**](algorithm-keylength.md) .</span><span class="sxs-lookup"><span data-stu-id="dcf4b-130">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type is used by the [**Algorithm.KeyLength**](algorithm-keylength.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcf4b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="dcf4b-131">Requirements</span></span>



| <span data-ttu-id="dcf4b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="dcf4b-132">Requirement</span></span> | <span data-ttu-id="dcf4b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="dcf4b-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf4b-134">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="dcf4b-134">Redistributable</span></span><br/> | <span data-ttu-id="dcf4b-135">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="dcf4b-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="dcf4b-136">Header</span><span class="sxs-lookup"><span data-stu-id="dcf4b-136">Header</span></span><br/>          | <dl> <span data-ttu-id="dcf4b-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcf4b-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 
