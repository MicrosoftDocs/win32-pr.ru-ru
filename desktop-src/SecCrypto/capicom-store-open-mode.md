---
description: Используется с методом Store. Open для указания способа открытия хранилища сертификатов.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: Перечисление CAPICOM_STORE_OPEN_MODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648920"
---
# <a name="capicom_store_open_mode-enumeration"></a><span data-ttu-id="65700-103">\_ \_ Перечисление в открытом режиме CAPICOM Store \_</span><span class="sxs-lookup"><span data-stu-id="65700-103">CAPICOM\_STORE\_OPEN\_MODE enumeration</span></span>

<span data-ttu-id="65700-104">\_ \_ Тип перечисления CAPICOM Store Open \_ mode используется с методом [**Store. Open**](store-open.md) для указания способа открытия хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="65700-104">The CAPICOM\_STORE\_OPEN\_MODE enumeration type is used with the [**Store.Open**](store-open.md) method to indicate how a certificate store is to be opened.</span></span>

## <a name="members"></a><span data-ttu-id="65700-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="65700-105">Members</span></span>



| <span data-ttu-id="65700-106">Член</span><span class="sxs-lookup"><span data-stu-id="65700-106">Member</span></span>                                      | <span data-ttu-id="65700-107">Описание</span><span class="sxs-lookup"><span data-stu-id="65700-107">Description</span></span>                                                                                                                                                              | <span data-ttu-id="65700-108">Значение</span><span class="sxs-lookup"><span data-stu-id="65700-108">Value</span></span> |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="65700-109">**CAPICOM \_ Store \_ открыт \_ только для чтения \_**</span><span class="sxs-lookup"><span data-stu-id="65700-109">**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</span></span>        | <span data-ttu-id="65700-110">Откройте хранилище в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="65700-110">Open the store in read-only mode.</span></span><br/>                                                                                                                             | <span data-ttu-id="65700-111">0</span><span class="sxs-lookup"><span data-stu-id="65700-111">0</span></span>     |
| <span data-ttu-id="65700-112">**CAPICOM \_ Store \_ открыть \_ чтение и \_ запись**</span><span class="sxs-lookup"><span data-stu-id="65700-112">**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</span></span>       | <span data-ttu-id="65700-113">Откройте хранилище в режиме чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="65700-113">Open the store in read/write mode.</span></span><br/>                                                                                                                            | <span data-ttu-id="65700-114">1</span><span class="sxs-lookup"><span data-stu-id="65700-114">1</span></span>     |
| <span data-ttu-id="65700-115">**\_ \_ \_ Максимальное \_ допустимое число открытых в CAPICOM Store**</span><span class="sxs-lookup"><span data-stu-id="65700-115">**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</span></span>  | <span data-ttu-id="65700-116">Откройте хранилище в режиме чтения и записи, если у пользователя есть разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="65700-116">Open the store in read/write mode if the user has read/write permissions.</span></span> <span data-ttu-id="65700-117">Если у пользователя нет разрешений на чтение и запись, откройте хранилище в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="65700-117">If the user does not have read/write permissions, open the store in read-only mode.</span></span><br/> | <span data-ttu-id="65700-118">2</span><span class="sxs-lookup"><span data-stu-id="65700-118">2</span></span>     |
| <span data-ttu-id="65700-119">**в \_ CAPICOM \_ Store \_ открыто \_ только существующее**</span><span class="sxs-lookup"><span data-stu-id="65700-119">**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</span></span>    | <span data-ttu-id="65700-120">Открывать только существующие магазины; не создавать новое хранилище.</span><span class="sxs-lookup"><span data-stu-id="65700-120">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="65700-121">Представлено CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="65700-121">Introduced by CAPICOM 2.0.</span></span><br/>                                                                              | <span data-ttu-id="65700-122">128</span><span class="sxs-lookup"><span data-stu-id="65700-122">128</span></span>   |
| <span data-ttu-id="65700-123">**\_открыто хранилище CAPICOM, \_ \_ включая \_ архивированные**</span><span class="sxs-lookup"><span data-stu-id="65700-123">**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</span></span> | <span data-ttu-id="65700-124">Включать архивные сертификаты при использовании хранилища.</span><span class="sxs-lookup"><span data-stu-id="65700-124">Include archived certificates when using the store.</span></span> <span data-ttu-id="65700-125">Представлено CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="65700-125">Introduced by CAPICOM 2.0.</span></span><br/>                                                                                | <span data-ttu-id="65700-126">256</span><span class="sxs-lookup"><span data-stu-id="65700-126">256</span></span>   |



## <a name="remarks"></a><span data-ttu-id="65700-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65700-127">Remarks</span></span>

<span data-ttu-id="65700-128">При использовании \_ \_ \_ перечислений в режиме открытого хранилища CAPICOM можно использовать только один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="65700-128">When using the CAPICOM\_STORE\_OPEN\_MODE enumeration, only one of the following settings can be used.</span></span>

-   <span data-ttu-id="65700-129">CAPICOM \_ Store \_ открыт \_ только для чтения \_</span><span class="sxs-lookup"><span data-stu-id="65700-129">CAPICOM\_STORE\_OPEN\_READ\_ONLY</span></span>
-   <span data-ttu-id="65700-130">CAPICOM \_ Store \_ открыть \_ чтение и \_ запись</span><span class="sxs-lookup"><span data-stu-id="65700-130">CAPICOM\_STORE\_OPEN\_READ\_WRITE</span></span>
-   <span data-ttu-id="65700-131">\_ \_ \_ Максимальное \_ допустимое число открытых в CAPICOM Store</span><span class="sxs-lookup"><span data-stu-id="65700-131">CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED</span></span>

## <a name="requirements"></a><span data-ttu-id="65700-132">Требования</span><span class="sxs-lookup"><span data-stu-id="65700-132">Requirements</span></span>



| <span data-ttu-id="65700-133">Требование</span><span class="sxs-lookup"><span data-stu-id="65700-133">Requirement</span></span> | <span data-ttu-id="65700-134">Значение</span><span class="sxs-lookup"><span data-stu-id="65700-134">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65700-135">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="65700-135">Redistributable</span></span><br/> | <span data-ttu-id="65700-136">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="65700-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="65700-137">Header</span><span class="sxs-lookup"><span data-stu-id="65700-137">Header</span></span><br/>          | <dl> <span data-ttu-id="65700-138"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="65700-138"><dt>Capicom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65700-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65700-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65700-140">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="65700-140">**Store.Open**</span></span>](store-open.md)
</dt> </dl>

 

 




