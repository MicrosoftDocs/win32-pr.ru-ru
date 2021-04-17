---
title: Перечисление DRM_CRYPTO_TYPE (Вмдрмсдк. h)
description: '\_ \_ Перечисление типа шифрования DRM определяет типы криптографических алгоритмов, которые могут использоваться для шифрования содержимого.'
ms.assetid: e04d22cd-04fe-4b80-9644-7cd24dc99f04
keywords:
- Формат Windows Media DRM_CRYPTO_TYPE перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_CRYPTO_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2560429d074e23025fae22822ccae90d432fb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717925"
---
# <a name="drm_crypto_type-enumeration"></a><span data-ttu-id="a7058-105">\_ \_ Перечисление типов шифрования DRM</span><span class="sxs-lookup"><span data-stu-id="a7058-105">DRM\_CRYPTO\_TYPE enumeration</span></span>

<span data-ttu-id="a7058-106">Перечисление **\_ \_ типа шифрования DRM** определяет типы криптографических алгоритмов, которые могут использоваться для шифрования содержимого.</span><span class="sxs-lookup"><span data-stu-id="a7058-106">The **DRM\_CRYPTO\_TYPE** enumeration defines the cryptographic algorithm types that can be used to encrypt content.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7058-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7058-107">Syntax</span></span>


```C++
typedef enum DRM_CRYPTO_TYPE { 
  CRYPTO_TYPE_MCE  = 0
} ;
```



## <a name="constants"></a><span data-ttu-id="a7058-108">Константы</span><span class="sxs-lookup"><span data-stu-id="a7058-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a7058-109"><span id="CRYPTO_TYPE_MCE"></span><span id="crypto_type_mce"></span>**\_тип шифрования \_ MCE**</span><span class="sxs-lookup"><span data-stu-id="a7058-109"><span id="CRYPTO_TYPE_MCE"></span><span id="crypto_type_mce"></span>**CRYPTO\_TYPE\_MCE**</span></span>
</dt> <dd>

<span data-ttu-id="a7058-110">Задает 128-разрядное шифрование в режиме счетчика AES (AES).</span><span class="sxs-lookup"><span data-stu-id="a7058-110">Specifies 128-bit counter mode Advanced Encryption Standard (AES) encryption.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7058-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7058-111">Remarks</span></span>

<span data-ttu-id="a7058-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="a7058-112">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7058-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a7058-113">Requirements</span></span>



| <span data-ttu-id="a7058-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a7058-114">Requirement</span></span> | <span data-ttu-id="a7058-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a7058-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7058-116">Header</span><span class="sxs-lookup"><span data-stu-id="a7058-116">Header</span></span><br/> | <dl> <span data-ttu-id="a7058-117"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7058-117"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7058-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7058-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7058-119">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="a7058-119">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





