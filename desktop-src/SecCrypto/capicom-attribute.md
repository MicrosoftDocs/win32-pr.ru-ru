---
description: Определяет тип атрибута, связанного с сигнатурой.
ms.assetid: 94f0dce4-0b32-4c39-ab2e-b01795432acd
title: Перечисление CAPICOM_ATTRIBUTE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ATTRIBUTE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: b03f91d0737b29b98adeb7e6a56bf9eccd35cc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669141"
---
# <a name="capicom_attribute-enumeration"></a><span data-ttu-id="e959b-103">\_Перечисление АТРИБУТОВ CAPICOM</span><span class="sxs-lookup"><span data-stu-id="e959b-103">CAPICOM\_ATTRIBUTE enumeration</span></span>

<span data-ttu-id="e959b-104">Тип **перечисления \_ атрибутов CAPICOM** определяет тип атрибута, связанного с [*сигнатурой*](../secgloss/d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e959b-104">The **CAPICOM\_ATTRIBUTE** enumeration type defines the kind of attribute associated with a [*signature*](../secgloss/d-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="e959b-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="e959b-105">Members</span></span>



| <span data-ttu-id="e959b-106">Член</span><span class="sxs-lookup"><span data-stu-id="e959b-106">Member</span></span>                                                       | <span data-ttu-id="e959b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e959b-107">Description</span></span>                                                                | <span data-ttu-id="e959b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e959b-108">Value</span></span> |
|--------------------------------------------------------------|----------------------------------------------------------------------------|-------|
| <span data-ttu-id="e959b-109">**\_время подписи CAPICOM проверенного \_ атрибута \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e959b-109">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</span></span>         | <span data-ttu-id="e959b-110">Атрибут содержит время создания подписи.</span><span class="sxs-lookup"><span data-stu-id="e959b-110">The attribute contains the time that the signature was created.</span></span><br/> | <span data-ttu-id="e959b-111">0</span><span class="sxs-lookup"><span data-stu-id="e959b-111">0</span></span>     |
| <span data-ttu-id="e959b-112">**\_ \_ \_ имя документа атрибута CAPICOM, прошедшего проверку подлинности \_**</span><span class="sxs-lookup"><span data-stu-id="e959b-112">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</span></span>        | <span data-ttu-id="e959b-113">Атрибут содержит имя подписанного документа.</span><span class="sxs-lookup"><span data-stu-id="e959b-113">The attribute contains the name of the signed document.</span></span><br/>         | <span data-ttu-id="e959b-114">1</span><span class="sxs-lookup"><span data-stu-id="e959b-114">1</span></span>     |
| <span data-ttu-id="e959b-115">**\_ \_ \_ описание документа атрибута CAPICOM, прошедшего проверку подлинности \_**</span><span class="sxs-lookup"><span data-stu-id="e959b-115">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</span></span> | <span data-ttu-id="e959b-116">Атрибут содержит описание подписанного документа.</span><span class="sxs-lookup"><span data-stu-id="e959b-116">The attribute contains a description of the signed document.</span></span><br/>    | <span data-ttu-id="e959b-117">2</span><span class="sxs-lookup"><span data-stu-id="e959b-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="e959b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e959b-118">Remarks</span></span>

<span data-ttu-id="e959b-119">Тип **перечисления \_ атрибутов CAPICOM** используется свойством [**Attribute.Name**](attribute-name.md) .</span><span class="sxs-lookup"><span data-stu-id="e959b-119">The **CAPICOM\_ATTRIBUTE** enumeration type is used by the [**Attribute.Name**](attribute-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e959b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e959b-120">Requirements</span></span>



| <span data-ttu-id="e959b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e959b-121">Requirement</span></span> | <span data-ttu-id="e959b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e959b-122">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e959b-123">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e959b-123">Redistributable</span></span><br/> | <span data-ttu-id="e959b-124">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="e959b-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="e959b-125">Header</span><span class="sxs-lookup"><span data-stu-id="e959b-125">Header</span></span><br/>          | <dl> <span data-ttu-id="e959b-126"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e959b-126"><dt>Capicom.h</dt></span></span> </dl> |



 

 
