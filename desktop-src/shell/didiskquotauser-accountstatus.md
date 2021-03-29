---
description: Возвращает состояние учетной записи пользователя.
title: Дидисккуотаусер. Аккаунтстатус, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: 155ae627d70c5125fd0d1d501062224450fc8e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984289"
---
# <a name="didiskquotauseraccountstatus-property"></a><span data-ttu-id="9d63d-103">Дидисккуотаусер. Аккаунтстатус, свойство</span><span class="sxs-lookup"><span data-stu-id="9d63d-103">DIDiskQuotaUser.AccountStatus property</span></span>

<span data-ttu-id="9d63d-104">Возвращает состояние учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="9d63d-104">Gets the status of the user's account.</span></span>

<span data-ttu-id="9d63d-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9d63d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d63d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d63d-106">Syntax</span></span>


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a><span data-ttu-id="9d63d-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9d63d-107">Property value</span></span>

<span data-ttu-id="9d63d-108">Это свойство может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9d63d-108">This property can take one of the following values.</span></span>



| <span data-ttu-id="9d63d-109">Состояние</span><span class="sxs-lookup"><span data-stu-id="9d63d-109">Status</span></span>            | <span data-ttu-id="9d63d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="9d63d-110">Value</span></span> | <span data-ttu-id="9d63d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="9d63d-111">Description</span></span>                         |
|-------------------|-------|-------------------------------------|
| <span data-ttu-id="9d63d-112">дкакктресолвед</span><span class="sxs-lookup"><span data-stu-id="9d63d-112">dqAcctResolved</span></span>    | <span data-ttu-id="9d63d-113">0</span><span class="sxs-lookup"><span data-stu-id="9d63d-113">0</span></span>     | <span data-ttu-id="9d63d-114">Сведения об учетной записи разрешены.</span><span class="sxs-lookup"><span data-stu-id="9d63d-114">Account information is resolved.</span></span>    |
| <span data-ttu-id="9d63d-115">дкакктунаваилабле</span><span class="sxs-lookup"><span data-stu-id="9d63d-115">dqAcctUnavailable</span></span> | <span data-ttu-id="9d63d-116">1</span><span class="sxs-lookup"><span data-stu-id="9d63d-116">1</span></span>     | <span data-ttu-id="9d63d-117">Сведения об учетной записи недоступны.</span><span class="sxs-lookup"><span data-stu-id="9d63d-117">Account information is unavailable.</span></span> |
| <span data-ttu-id="9d63d-118">дкакктделетед</span><span class="sxs-lookup"><span data-stu-id="9d63d-118">dqAcctDeleted</span></span>     | <span data-ttu-id="9d63d-119">2</span><span class="sxs-lookup"><span data-stu-id="9d63d-119">2</span></span>     | <span data-ttu-id="9d63d-120">Учетная запись удалена.</span><span class="sxs-lookup"><span data-stu-id="9d63d-120">Account has been deleted.</span></span>           |
| <span data-ttu-id="9d63d-121">дкакктинвалид</span><span class="sxs-lookup"><span data-stu-id="9d63d-121">dqAcctInvalid</span></span>     | <span data-ttu-id="9d63d-122">3</span><span class="sxs-lookup"><span data-stu-id="9d63d-122">3</span></span>     | <span data-ttu-id="9d63d-123">Недопустимая учетная запись.</span><span class="sxs-lookup"><span data-stu-id="9d63d-123">Account is invalid.</span></span>                 |
| <span data-ttu-id="9d63d-124">дкакктункновн</span><span class="sxs-lookup"><span data-stu-id="9d63d-124">dqAcctUnknown</span></span>     | <span data-ttu-id="9d63d-125">4</span><span class="sxs-lookup"><span data-stu-id="9d63d-125">4</span></span>     | <span data-ttu-id="9d63d-126">Не удается найти учетную запись.</span><span class="sxs-lookup"><span data-stu-id="9d63d-126">Account cannot be found.</span></span>            |
| <span data-ttu-id="9d63d-127">дкакктунресолвед</span><span class="sxs-lookup"><span data-stu-id="9d63d-127">dqAcctUnresolved</span></span>  | <span data-ttu-id="9d63d-128">5</span><span class="sxs-lookup"><span data-stu-id="9d63d-128">5</span></span>     | <span data-ttu-id="9d63d-129">Сведения об учетной записи не разрешены.</span><span class="sxs-lookup"><span data-stu-id="9d63d-129">Account information is unresolved.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="9d63d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="9d63d-130">Requirements</span></span>



| <span data-ttu-id="9d63d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="9d63d-131">Requirement</span></span> | <span data-ttu-id="9d63d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="9d63d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d63d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d63d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9d63d-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9d63d-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d63d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d63d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9d63d-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9d63d-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9d63d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9d63d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d63d-138"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="9d63d-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d63d-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d63d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d63d-140">**Объект Дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="9d63d-140">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




