---
title: Перечисление MP_HASH_TYPE (Мпклиент. h)
description: Возможные типы хэширования.
ms.assetid: 46432C40-6DE1-4FB8-B7C1-C2712CCEB208
keywords:
- MP_HASH_TYPE перечисления устаревшие функции среды Windows
- PMP_HASH_TYPE указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MP_HASH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c36e709d165845b729673df4aaea1042a7ee49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492639"
---
# <a name="mp_hash_type-enumeration"></a><span data-ttu-id="f014d-105">\_ \_ Перечисление типов хэша MP</span><span class="sxs-lookup"><span data-stu-id="f014d-105">MP\_HASH\_TYPE enumeration</span></span>

<span data-ttu-id="f014d-106">Возможные типы хэширования.</span><span class="sxs-lookup"><span data-stu-id="f014d-106">Possible hash types.</span></span>

## <a name="syntax"></a><span data-ttu-id="f014d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f014d-107">Syntax</span></span>


```C++
typedef enum tagMP_HASH_TYPE { 
  MP_HASH_TYPE_NONE    = 0,
  MP_HASH_TYPE_CRC32   = 2,
  MP_HASH_TYPE_MD5     = 4,
  MP_HASH_TYPE_SHA1    = 8,
  MP_HASH_TYPE_SHA256  = 16
} MP_HASH_TYPE, *PMP_HASH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="f014d-108">Константы</span><span class="sxs-lookup"><span data-stu-id="f014d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f014d-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**\_тип ХЭША \_ MP \_ None**</span><span class="sxs-lookup"><span data-stu-id="f014d-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**MP\_HASH\_TYPE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="f014d-110">Нет хэша.</span><span class="sxs-lookup"><span data-stu-id="f014d-110">No hash.</span></span>

</dd> <dt>

<span data-ttu-id="f014d-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**\_ \_ CRC32 тип хэша пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="f014d-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**MP\_HASH\_TYPE\_CRC32**</span></span>
</dt> <dd>

<span data-ttu-id="f014d-112">CRC32</span><span class="sxs-lookup"><span data-stu-id="f014d-112">CRC32</span></span>

</dd> <dt>

<span data-ttu-id="f014d-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**\_ \_ MD5 тип хэша \_**</span><span class="sxs-lookup"><span data-stu-id="f014d-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**MP\_HASH\_TYPE\_MD5**</span></span>
</dt> <dd>

<span data-ttu-id="f014d-114">MD5</span><span class="sxs-lookup"><span data-stu-id="f014d-114">MD5</span></span>

</dd> <dt>

<span data-ttu-id="f014d-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**\_SHA1- \_ тип \_ хэша пакета управления**</span><span class="sxs-lookup"><span data-stu-id="f014d-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**MP\_HASH\_TYPE\_SHA1**</span></span>
</dt> <dd>

<span data-ttu-id="f014d-116">SHA1</span><span class="sxs-lookup"><span data-stu-id="f014d-116">SHA1</span></span>

</dd> <dt>

<span data-ttu-id="f014d-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**\_Тип хэша пакета управления \_ \_ SHA256**</span><span class="sxs-lookup"><span data-stu-id="f014d-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**MP\_HASH\_TYPE\_SHA256**</span></span>
</dt> <dd>

<span data-ttu-id="f014d-118">SHA 256</span><span class="sxs-lookup"><span data-stu-id="f014d-118">SHA 256</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f014d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f014d-119">Requirements</span></span>



| <span data-ttu-id="f014d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f014d-120">Requirement</span></span> | <span data-ttu-id="f014d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f014d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f014d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f014d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f014d-123">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f014d-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f014d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f014d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f014d-125">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f014d-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f014d-126">Header</span><span class="sxs-lookup"><span data-stu-id="f014d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f014d-127"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="f014d-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





