---
description: '\_ \_ \_ Перечисление флагов хранилища CAPICOM определяет флаги хранилища ключей.'
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: Перечисление CAPICOM_KEY_STORAGE_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 9edbc3a5ac3396e528ebbb5390c4b07c24770e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648694"
---
# <a name="capicom_key_storage_flag-enumeration"></a><span data-ttu-id="0adaa-103">\_ \_ \_ Перечисление ФЛАГов хранилища CAPICOM</span><span class="sxs-lookup"><span data-stu-id="0adaa-103">CAPICOM\_KEY\_STORAGE\_FLAG enumeration</span></span>

<span data-ttu-id="0adaa-104">Перечисление **\_ \_ \_ флагов хранилища CAPICOM** определяет флаги хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0adaa-104">The **CAPICOM\_KEY\_STORAGE\_FLAG** enumeration defines key storage flags.</span></span>

## <a name="members"></a><span data-ttu-id="0adaa-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="0adaa-105">Members</span></span>



| <span data-ttu-id="0adaa-106">Член</span><span class="sxs-lookup"><span data-stu-id="0adaa-106">Member</span></span>                                     | <span data-ttu-id="0adaa-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0adaa-107">Description</span></span>                           | <span data-ttu-id="0adaa-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0adaa-108">Value</span></span> |
|--------------------------------------------|---------------------------------------|-------|
| <span data-ttu-id="0adaa-109">**\_хранилище CAPICOM \_ key \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="0adaa-109">**CAPICOM\_KEY\_STORAGE\_DEFAULT**</span></span>         | <span data-ttu-id="0adaa-110">Хранилище ключей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0adaa-110">Default key storage.</span></span><br/>       | <span data-ttu-id="0adaa-111">0</span><span class="sxs-lookup"><span data-stu-id="0adaa-111">0</span></span>     |
| <span data-ttu-id="0adaa-112">**\_хранилище CAPICOM Key, \_ \_ экспортируемое**</span><span class="sxs-lookup"><span data-stu-id="0adaa-112">**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</span></span>      | <span data-ttu-id="0adaa-113">Ключ доступен для экспорта.</span><span class="sxs-lookup"><span data-stu-id="0adaa-113">The key is exportable.</span></span><br/>     | <span data-ttu-id="0adaa-114">1</span><span class="sxs-lookup"><span data-stu-id="0adaa-114">1</span></span>     |
| <span data-ttu-id="0adaa-115">**\_ \_ \_ защищенное пользователем хранилище CAPICOM key \_**</span><span class="sxs-lookup"><span data-stu-id="0adaa-115">**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</span></span> | <span data-ttu-id="0adaa-116">Ключ защищен пользователем.</span><span class="sxs-lookup"><span data-stu-id="0adaa-116">The key is user protected.</span></span><br/> | <span data-ttu-id="0adaa-117">2</span><span class="sxs-lookup"><span data-stu-id="0adaa-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="0adaa-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0adaa-118">Remarks</span></span>

<span data-ttu-id="0adaa-119">Это перечисление используется следующим методом:</span><span class="sxs-lookup"><span data-stu-id="0adaa-119">This enumeration is used by the following method:</span></span>

-   [<span data-ttu-id="0adaa-120">**Certificate. Load**</span><span class="sxs-lookup"><span data-stu-id="0adaa-120">**Certificate.Load**</span></span>](certificate-load.md)
-   [<span data-ttu-id="0adaa-121">**Store. Load**</span><span class="sxs-lookup"><span data-stu-id="0adaa-121">**Store.Load**</span></span>](store-load.md)

## <a name="requirements"></a><span data-ttu-id="0adaa-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0adaa-122">Requirements</span></span>



| <span data-ttu-id="0adaa-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0adaa-123">Requirement</span></span> | <span data-ttu-id="0adaa-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0adaa-124">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0adaa-125">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0adaa-125">Redistributable</span></span><br/> | <span data-ttu-id="0adaa-126">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0adaa-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="0adaa-127">Header</span><span class="sxs-lookup"><span data-stu-id="0adaa-127">Header</span></span><br/>          | <dl> <span data-ttu-id="0adaa-128"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="0adaa-128"><dt>Capicom.h</dt></span></span> </dl> |



 

 




