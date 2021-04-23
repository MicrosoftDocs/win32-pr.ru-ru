---
description: Указывает расположение хранилища сертификатов.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: Перечисление CAPICOM_STORE_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 24b2e786e2821c39c6ff67f5919dca2ac0c6bfe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669035"
---
# <a name="capicom_store_location-enumeration"></a><span data-ttu-id="10a96-103">\_ \_ Перечисление расположения CAPICOM Store</span><span class="sxs-lookup"><span data-stu-id="10a96-103">CAPICOM\_STORE\_LOCATION enumeration</span></span>

<span data-ttu-id="10a96-104">Тип **перечисления \_ CAPICOM \_ Location** указывает расположение [*хранилища сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="10a96-104">The **CAPICOM\_STORE\_LOCATION** enumeration type indicates the location of a [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="10a96-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="10a96-105">Members</span></span>



| <span data-ttu-id="10a96-106">Член</span><span class="sxs-lookup"><span data-stu-id="10a96-106">Member</span></span>                                      | <span data-ttu-id="10a96-107">Описание</span><span class="sxs-lookup"><span data-stu-id="10a96-107">Description</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="10a96-108">Значение</span><span class="sxs-lookup"><span data-stu-id="10a96-108">Value</span></span> |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="10a96-109">**\_хранилище CAPICOM Memory \_**</span><span class="sxs-lookup"><span data-stu-id="10a96-109">**CAPICOM\_MEMORY\_STORE**</span></span>                  | <span data-ttu-id="10a96-110">Хранилище является хранилищем памяти.</span><span class="sxs-lookup"><span data-stu-id="10a96-110">The store is a memory store.</span></span> <span data-ttu-id="10a96-111">Любые изменения в содержимом хранилища не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="10a96-111">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                              | <span data-ttu-id="10a96-112">0</span><span class="sxs-lookup"><span data-stu-id="10a96-112">0</span></span>     |
| <span data-ttu-id="10a96-113">**хранилище CAPICOM на \_ локальном \_ компьютере \_**</span><span class="sxs-lookup"><span data-stu-id="10a96-113">**CAPICOM\_LOCAL\_MACHINE\_STORE**</span></span>          | <span data-ttu-id="10a96-114">Хранилище является локальным хранилищем компьютера.</span><span class="sxs-lookup"><span data-stu-id="10a96-114">The store is a local machine store.</span></span> <span data-ttu-id="10a96-115">Хранилища локальных компьютеров могут быть хранилищами для чтения и записи, только если у пользователя есть разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="10a96-115">Local machine stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="10a96-116">Если у пользователя есть разрешения на чтение и запись и если хранилище открыто для чтения и записи, то изменения в содержимом хранилища сохраняются.</span><span class="sxs-lookup"><span data-stu-id="10a96-116">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> | <span data-ttu-id="10a96-117">1</span><span class="sxs-lookup"><span data-stu-id="10a96-117">1</span></span>     |
| <span data-ttu-id="10a96-118">**\_хранилище CAPICOM текущего \_ пользователя \_**</span><span class="sxs-lookup"><span data-stu-id="10a96-118">**CAPICOM\_CURRENT\_USER\_STORE**</span></span>           | <span data-ttu-id="10a96-119">Хранилище является хранилищем текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="10a96-119">The store is a current user store.</span></span> <span data-ttu-id="10a96-120">Хранилище текущего пользователя может быть хранилищем для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="10a96-120">A current user store may be a read/write store.</span></span> <span data-ttu-id="10a96-121">Если это так, изменения в содержимом хранилища сохраняются.</span><span class="sxs-lookup"><span data-stu-id="10a96-121">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                      | <span data-ttu-id="10a96-122">2</span><span class="sxs-lookup"><span data-stu-id="10a96-122">2</span></span>     |
| <span data-ttu-id="10a96-123">**CAPICOM \_ Active \_ Directory \_ пользовательское \_ хранилище**</span><span class="sxs-lookup"><span data-stu-id="10a96-123">**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</span></span> | <span data-ttu-id="10a96-124">Магазин является хранилищем Active Directory.</span><span class="sxs-lookup"><span data-stu-id="10a96-124">The store is an Active Directory store.</span></span> <span data-ttu-id="10a96-125">Хранилища Active Directory могут быть открыты только в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="10a96-125">Active Directory stores can be opened only in read-only mode.</span></span> <span data-ttu-id="10a96-126">Сертификаты нельзя добавлять в хранилища Active Directory или удалять из них.</span><span class="sxs-lookup"><span data-stu-id="10a96-126">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                                                                                        | <span data-ttu-id="10a96-127">3</span><span class="sxs-lookup"><span data-stu-id="10a96-127">3</span></span>     |
| <span data-ttu-id="10a96-128">**\_хранилище CAPICOM смарт- \_ карты \_ пользователя \_**</span><span class="sxs-lookup"><span data-stu-id="10a96-128">**CAPICOM\_SMART\_CARD\_USER\_STORE**</span></span>       | <span data-ttu-id="10a96-129">Хранилища поддерживают хранилища сертификатов на основе смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="10a96-129">Stores support smart card–based certificate stores.</span></span> <span data-ttu-id="10a96-130">Магазин — это группа существующих смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="10a96-130">The store is the group of present smart cards.</span></span> <span data-ttu-id="10a96-131">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="10a96-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                         | <span data-ttu-id="10a96-132">4</span><span class="sxs-lookup"><span data-stu-id="10a96-132">4</span></span>     |



## <a name="remarks"></a><span data-ttu-id="10a96-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10a96-133">Remarks</span></span>

<span data-ttu-id="10a96-134">Тип **перечисления \_ CAPICOM \_ Location** используется следующими методами.</span><span class="sxs-lookup"><span data-stu-id="10a96-134">The **CAPICOM\_STORE\_LOCATION** enumeration type is used by the following methods:</span></span>

-   [<span data-ttu-id="10a96-135">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="10a96-135">**PrivateKey.Open**</span></span>](privatekey-open.md)
-   [<span data-ttu-id="10a96-136">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="10a96-136">**Store.Open**</span></span>](store-open.md)

## <a name="requirements"></a><span data-ttu-id="10a96-137">Требования</span><span class="sxs-lookup"><span data-stu-id="10a96-137">Requirements</span></span>



| <span data-ttu-id="10a96-138">Требование</span><span class="sxs-lookup"><span data-stu-id="10a96-138">Requirement</span></span> | <span data-ttu-id="10a96-139">Значение</span><span class="sxs-lookup"><span data-stu-id="10a96-139">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10a96-140">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="10a96-140">Redistributable</span></span><br/> | <span data-ttu-id="10a96-141">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="10a96-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="10a96-142">Header</span><span class="sxs-lookup"><span data-stu-id="10a96-142">Header</span></span><br/>          | <dl> <span data-ttu-id="10a96-143"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="10a96-143"><dt>Capicom.h</dt></span></span> </dl> |



 

 
