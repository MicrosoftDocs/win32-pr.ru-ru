---
description: Определяет имена расширенного использования ключа в зависимости от того, где их можно использовать.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: Перечисление CAPICOM_EKU (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668522"
---
# <a name="capicom_eku-enumeration"></a><span data-ttu-id="a7be7-103">\_Перечисление EKU в CAPICOM</span><span class="sxs-lookup"><span data-stu-id="a7be7-103">CAPICOM\_EKU enumeration</span></span>

<span data-ttu-id="a7be7-104">Тип перечисления **CAPICOM \_ EKU** определяет имена расширенного использования ключа в зависимости от того, где их можно использовать.</span><span class="sxs-lookup"><span data-stu-id="a7be7-104">The **CAPICOM\_EKU** enumeration type defines the extended key usage names based on where they can be used.</span></span>

## <a name="members"></a><span data-ttu-id="a7be7-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="a7be7-105">Members</span></span>



| <span data-ttu-id="a7be7-106">Член</span><span class="sxs-lookup"><span data-stu-id="a7be7-106">Member</span></span>                                     | <span data-ttu-id="a7be7-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a7be7-107">Description</span></span>                                                                                                                                                 | <span data-ttu-id="a7be7-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a7be7-108">Value</span></span> |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="a7be7-109">**\_другое расширенное EKU \_**</span><span class="sxs-lookup"><span data-stu-id="a7be7-109">**CAPICOM\_EKU\_OTHER**</span></span>                    | <span data-ttu-id="a7be7-110">В сертификате используются определенные в локальной политике.</span><span class="sxs-lookup"><span data-stu-id="a7be7-110">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="a7be7-111">Используется, если требуемое EKU не определено и значение OID должно быть задано приложением.</span><span class="sxs-lookup"><span data-stu-id="a7be7-111">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> | <span data-ttu-id="a7be7-112">0</span><span class="sxs-lookup"><span data-stu-id="a7be7-112">0</span></span>     |
| <span data-ttu-id="a7be7-113">**\_ \_ \_ Проверка подлинности сервера CAPICOM EKU**</span><span class="sxs-lookup"><span data-stu-id="a7be7-113">**CAPICOM\_EKU\_SERVER\_AUTH**</span></span>             | <span data-ttu-id="a7be7-114">Сертификат можно использовать для проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="a7be7-114">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                | <span data-ttu-id="a7be7-115">1</span><span class="sxs-lookup"><span data-stu-id="a7be7-115">1</span></span>     |
| <span data-ttu-id="a7be7-116">**\_ \_ \_ Проверка подлинности клиента CAPICOM EKU**</span><span class="sxs-lookup"><span data-stu-id="a7be7-116">**CAPICOM\_EKU\_CLIENT\_AUTH**</span></span>             | <span data-ttu-id="a7be7-117">Сертификат можно использовать для проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="a7be7-117">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                | <span data-ttu-id="a7be7-118">2</span><span class="sxs-lookup"><span data-stu-id="a7be7-118">2</span></span>     |
| <span data-ttu-id="a7be7-119">**\_Подписывание \_ кода CAPICOM EKU \_**</span><span class="sxs-lookup"><span data-stu-id="a7be7-119">**CAPICOM\_EKU\_CODE\_SIGNING**</span></span>            | <span data-ttu-id="a7be7-120">Сертификат можно использовать для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="a7be7-120">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           | <span data-ttu-id="a7be7-121">3</span><span class="sxs-lookup"><span data-stu-id="a7be7-121">3</span></span>     |
| <span data-ttu-id="a7be7-122">**\_ \_ Защита электронной почты CAPICOM EKU \_**</span><span class="sxs-lookup"><span data-stu-id="a7be7-122">**CAPICOM\_EKU\_EMAIL\_PROTECTION**</span></span>        | <span data-ttu-id="a7be7-123">Сертификат можно использовать для защиты электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a7be7-123">Certificate can be used for email protection.</span></span><br/>                                                                                                    | <span data-ttu-id="a7be7-124">4</span><span class="sxs-lookup"><span data-stu-id="a7be7-124">4</span></span>     |
| <span data-ttu-id="a7be7-125">**\_Вход в \_ смарт-карту CAPICOM EKU \_**</span><span class="sxs-lookup"><span data-stu-id="a7be7-125">**CAPICOM\_EKU\_SMARTCARD\_LOGON**</span></span>         | <span data-ttu-id="a7be7-126">Сертификат можно использовать для входа с использованием смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="a7be7-126">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="a7be7-127">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a7be7-127">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         | <span data-ttu-id="a7be7-128">5</span><span class="sxs-lookup"><span data-stu-id="a7be7-128">5</span></span>     |
| <span data-ttu-id="a7be7-129">**\_ \_ \_ Файловая система с шифрованием CAPICOM EKU \_**</span><span class="sxs-lookup"><span data-stu-id="a7be7-129">**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</span></span> | <span data-ttu-id="a7be7-130">Сертификат можно использовать для EFS.</span><span class="sxs-lookup"><span data-stu-id="a7be7-130">Certificate can be used for EFS.</span></span> <span data-ttu-id="a7be7-131">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a7be7-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      | <span data-ttu-id="a7be7-132">6</span><span class="sxs-lookup"><span data-stu-id="a7be7-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="a7be7-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7be7-133">Remarks</span></span>

<span data-ttu-id="a7be7-134">Тип перечисления **CAPICOM \_ EKU** используется в [**EKU. Имя**](eku-name.md) свойства.</span><span class="sxs-lookup"><span data-stu-id="a7be7-134">The **CAPICOM\_EKU** enumeration type is used by the [**EKU.Name**](eku-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7be7-135">Требования</span><span class="sxs-lookup"><span data-stu-id="a7be7-135">Requirements</span></span>



| <span data-ttu-id="a7be7-136">Требование</span><span class="sxs-lookup"><span data-stu-id="a7be7-136">Requirement</span></span> | <span data-ttu-id="a7be7-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a7be7-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a7be7-138">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a7be7-138">Redistributable</span></span><br/> | <span data-ttu-id="a7be7-139">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="a7be7-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="a7be7-140">Header</span><span class="sxs-lookup"><span data-stu-id="a7be7-140">Header</span></span><br/>          | <dl> <span data-ttu-id="a7be7-141"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7be7-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 




