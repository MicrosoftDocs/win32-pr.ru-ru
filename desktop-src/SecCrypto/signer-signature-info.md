---
description: Содержит сведения о цифровой подписи.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: Структура SIGNER_SIGNATURE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8e2b1fa68da51a649a01d4356ebfb1519ceeffb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264682"
---
# <a name="signer_signature_info-structure"></a><span data-ttu-id="b07f3-103">\_ \_ Структура сведений о подписи подписывания</span><span class="sxs-lookup"><span data-stu-id="b07f3-103">SIGNER\_SIGNATURE\_INFO structure</span></span>

<span data-ttu-id="b07f3-104">Структура **сведений о \_ подписи \_ подписывания** содержит сведения о цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="b07f3-104">The **SIGNER\_SIGNATURE\_INFO** structure contains information about a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="b07f3-105">Эта структура не определена ни в одном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="b07f3-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="b07f3-106">Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="b07f3-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b07f3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b07f3-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a><span data-ttu-id="b07f3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b07f3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b07f3-109">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="b07f3-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="b07f3-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="b07f3-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="b07f3-111">**алгидхаш**</span><span class="sxs-lookup"><span data-stu-id="b07f3-111">**algidHash**</span></span>
</dt> <dd>

<span data-ttu-id="b07f3-112">Хэш-алгоритм, используемый для цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="b07f3-112">The hash algorithm used for the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="b07f3-113">**дваттрчоице**</span><span class="sxs-lookup"><span data-stu-id="b07f3-113">**dwAttrChoice**</span></span>
</dt> <dd>

<span data-ttu-id="b07f3-114">Указывает, содержит ли подпись атрибуты [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b07f3-114">Specifies whether the signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span> <span data-ttu-id="b07f3-115">Этот элемент может иметь одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b07f3-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="b07f3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b07f3-116">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="b07f3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b07f3-117">Meaning</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <span data-ttu-id="b07f3-118"><dt>**\_ Подписавший ДВУХФАКТОРНОЙ \_ attr**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b07f3-118"><dt>**SIGNER\_AUTHCODE\_ATTR**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="b07f3-119">Сигнатура содержит атрибуты [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b07f3-119">The signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <span data-ttu-id="b07f3-120"><dt>**\_ Подписавший НЕТ \_ attr**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b07f3-120"><dt>**SIGNER\_NO\_ATTR**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="b07f3-121">Подпись не имеет атрибутов [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b07f3-121">The signature does not have [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b07f3-122">**паттраускоде**</span><span class="sxs-lookup"><span data-stu-id="b07f3-122">**pAttrAuthcode**</span></span>
</dt> <dd>

<span data-ttu-id="b07f3-123">Задает атрибуты для подписи [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b07f3-123">Specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span> <span data-ttu-id="b07f3-124">Этот элемент необходим, если значение элемента **дваттрчоице** — **подписывающий \_ двухфакторной \_ attr**.</span><span class="sxs-lookup"><span data-stu-id="b07f3-124">This member is required if the value of the **dwAttrChoice** member is **SIGNER\_AUTHCODE\_ATTR**.</span></span>

</dd> <dt>

<span data-ttu-id="b07f3-125">**псаусентикатед**</span><span class="sxs-lookup"><span data-stu-id="b07f3-125">**psAuthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="b07f3-126">Указанные пользователем атрибуты, добавленные в цифровую подпись.</span><span class="sxs-lookup"><span data-stu-id="b07f3-126">Authenticated user-supplied attributes added to the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="b07f3-127">**псунаусентикатед**</span><span class="sxs-lookup"><span data-stu-id="b07f3-127">**psUnauthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="b07f3-128">Пользовательские атрибуты, не прошедшие проверку подлинности, добавлены в цифровую подпись.</span><span class="sxs-lookup"><span data-stu-id="b07f3-128">Unauthenticated user-supplied attributes added to the digital signature.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b07f3-129">Требования</span><span class="sxs-lookup"><span data-stu-id="b07f3-129">Requirements</span></span>



| <span data-ttu-id="b07f3-130">Требование</span><span class="sxs-lookup"><span data-stu-id="b07f3-130">Requirement</span></span> | <span data-ttu-id="b07f3-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b07f3-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b07f3-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b07f3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b07f3-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b07f3-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b07f3-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b07f3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b07f3-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b07f3-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b07f3-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b07f3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b07f3-137">**сигнерсигн**</span><span class="sxs-lookup"><span data-stu-id="b07f3-137">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="b07f3-138">**сигнерсигнекс**</span><span class="sxs-lookup"><span data-stu-id="b07f3-138">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
