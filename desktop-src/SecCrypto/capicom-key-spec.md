---
description: Перечисление ключевых спецификаций CAPICOM \_ \_ определяет ключевые спецификации.
ms.assetid: e4aaaf69-ab28-4e8c-8a8a-6dc662299865
title: Перечисление CAPICOM_KEY_SPEC (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_SPEC
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 153f0431d78ff595b4d568fd7a677abea0d28be7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648695"
---
# <a name="capicom_key_spec-enumeration"></a><span data-ttu-id="3a6db-103">\_ \_ Перечисление СПЕЦИФИКАЦИй CAPICOM</span><span class="sxs-lookup"><span data-stu-id="3a6db-103">CAPICOM\_KEY\_SPEC enumeration</span></span>

<span data-ttu-id="3a6db-104">Перечисление **\_ ключевых \_** спецификаций CAPICOM определяет ключевые спецификации.</span><span class="sxs-lookup"><span data-stu-id="3a6db-104">The **CAPICOM\_KEY\_SPEC** enumeration defines key specifications.</span></span>

## <a name="members"></a><span data-ttu-id="3a6db-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="3a6db-105">Members</span></span>



| <span data-ttu-id="3a6db-106">Член</span><span class="sxs-lookup"><span data-stu-id="3a6db-106">Member</span></span>                              | <span data-ttu-id="3a6db-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3a6db-107">Description</span></span>                                                | <span data-ttu-id="3a6db-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3a6db-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|-------|
| <span data-ttu-id="3a6db-109">**\_ \_ КЭЙЕКСЧАНЖЕ спецификация CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="3a6db-109">**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</span></span> | <span data-ttu-id="3a6db-110">Ключ можно использовать для шифрования и подписывания.</span><span class="sxs-lookup"><span data-stu-id="3a6db-110">The key can be used for encryption and signing.</span></span><br/> | <span data-ttu-id="3a6db-111">1</span><span class="sxs-lookup"><span data-stu-id="3a6db-111">1</span></span>     |
| <span data-ttu-id="3a6db-112">**\_ \_ подпись спецификации CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="3a6db-112">**CAPICOM\_KEY\_SPEC\_SIGNATURE**</span></span>   | <span data-ttu-id="3a6db-113">Ключ можно использовать только для подписывания.</span><span class="sxs-lookup"><span data-stu-id="3a6db-113">The key can be used only for signing.</span></span><br/>           | <span data-ttu-id="3a6db-114">2</span><span class="sxs-lookup"><span data-stu-id="3a6db-114">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="3a6db-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a6db-115">Remarks</span></span>

<span data-ttu-id="3a6db-116">Перечисление **\_ ключевых \_ спецификаций CAPICOM** используется следующими методами и свойствами:</span><span class="sxs-lookup"><span data-stu-id="3a6db-116">The **CAPICOM\_KEY\_SPEC** enumeration is used by the following methods and properties:</span></span>

-   <span data-ttu-id="3a6db-117">[**PrivateKey. keySpec**](privatekey-keyspec.md) , свойство.</span><span class="sxs-lookup"><span data-stu-id="3a6db-117">[**PrivateKey.KeySpec**](privatekey-keyspec.md) property.</span></span>
-   <span data-ttu-id="3a6db-118">Метод [**PrivateKey. Open**](privatekey-open.md) .</span><span class="sxs-lookup"><span data-stu-id="3a6db-118">[**PrivateKey.Open**](privatekey-open.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a6db-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3a6db-119">Requirements</span></span>



| <span data-ttu-id="3a6db-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3a6db-120">Requirement</span></span> | <span data-ttu-id="3a6db-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3a6db-121">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3a6db-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="3a6db-122">Redistributable</span></span><br/> | <span data-ttu-id="3a6db-123">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="3a6db-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="3a6db-124">Header</span><span class="sxs-lookup"><span data-stu-id="3a6db-124">Header</span></span><br/>          | <dl> <span data-ttu-id="3a6db-125"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a6db-125"><dt>Capicom.h</dt></span></span> </dl> |



 

 




