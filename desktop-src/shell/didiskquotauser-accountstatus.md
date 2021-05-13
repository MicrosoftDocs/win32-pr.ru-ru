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
ms.openlocfilehash: e27e86fadab02616f91a4838acfc4be93e985ebd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841655"
---
# <a name="didiskquotauseraccountstatus-property"></a><span data-ttu-id="6f908-103">Дидисккуотаусер. Аккаунтстатус, свойство</span><span class="sxs-lookup"><span data-stu-id="6f908-103">DIDiskQuotaUser.AccountStatus property</span></span>

<span data-ttu-id="6f908-104">Возвращает состояние учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="6f908-104">Gets the status of the user's account.</span></span>

<span data-ttu-id="6f908-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6f908-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f908-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f908-106">Syntax</span></span>


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a><span data-ttu-id="6f908-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6f908-107">Property value</span></span>

<span data-ttu-id="6f908-108">Это свойство может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6f908-108">This property can take one of the following values.</span></span>



| <span data-ttu-id="6f908-109">Состояние</span><span class="sxs-lookup"><span data-stu-id="6f908-109">Status</span></span>            | <span data-ttu-id="6f908-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6f908-110">Value</span></span> | <span data-ttu-id="6f908-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6f908-111">Description</span></span>                         |
|-------------------|-------|-------------------------------------|
| <span data-ttu-id="6f908-112">дкакктресолвед</span><span class="sxs-lookup"><span data-stu-id="6f908-112">dqAcctResolved</span></span>    | <span data-ttu-id="6f908-113">0</span><span class="sxs-lookup"><span data-stu-id="6f908-113">0</span></span>     | <span data-ttu-id="6f908-114">Сведения об учетной записи разрешены.</span><span class="sxs-lookup"><span data-stu-id="6f908-114">Account information is resolved.</span></span>    |
| <span data-ttu-id="6f908-115">дкакктунаваилабле</span><span class="sxs-lookup"><span data-stu-id="6f908-115">dqAcctUnavailable</span></span> | <span data-ttu-id="6f908-116">1</span><span class="sxs-lookup"><span data-stu-id="6f908-116">1</span></span>     | <span data-ttu-id="6f908-117">Сведения об учетной записи недоступны.</span><span class="sxs-lookup"><span data-stu-id="6f908-117">Account information is unavailable.</span></span> |
| <span data-ttu-id="6f908-118">дкакктделетед</span><span class="sxs-lookup"><span data-stu-id="6f908-118">dqAcctDeleted</span></span>     | <span data-ttu-id="6f908-119">2</span><span class="sxs-lookup"><span data-stu-id="6f908-119">2</span></span>     | <span data-ttu-id="6f908-120">Учетная запись удалена.</span><span class="sxs-lookup"><span data-stu-id="6f908-120">Account has been deleted.</span></span>           |
| <span data-ttu-id="6f908-121">дкакктинвалид</span><span class="sxs-lookup"><span data-stu-id="6f908-121">dqAcctInvalid</span></span>     | <span data-ttu-id="6f908-122">3</span><span class="sxs-lookup"><span data-stu-id="6f908-122">3</span></span>     | <span data-ttu-id="6f908-123">Недопустимая учетная запись.</span><span class="sxs-lookup"><span data-stu-id="6f908-123">Account is invalid.</span></span>                 |
| <span data-ttu-id="6f908-124">дкакктункновн</span><span class="sxs-lookup"><span data-stu-id="6f908-124">dqAcctUnknown</span></span>     | <span data-ttu-id="6f908-125">4</span><span class="sxs-lookup"><span data-stu-id="6f908-125">4</span></span>     | <span data-ttu-id="6f908-126">Не удается найти учетную запись.</span><span class="sxs-lookup"><span data-stu-id="6f908-126">Account cannot be found.</span></span>            |
| <span data-ttu-id="6f908-127">дкакктунресолвед</span><span class="sxs-lookup"><span data-stu-id="6f908-127">dqAcctUnresolved</span></span>  | <span data-ttu-id="6f908-128">5</span><span class="sxs-lookup"><span data-stu-id="6f908-128">5</span></span>     | <span data-ttu-id="6f908-129">Сведения об учетной записи не разрешены.</span><span class="sxs-lookup"><span data-stu-id="6f908-129">Account information is unresolved.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="6f908-130">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="6f908-130">Requirements</span></span>



| <span data-ttu-id="6f908-131">Требование</span><span class="sxs-lookup"><span data-stu-id="6f908-131">Requirement</span></span> | <span data-ttu-id="6f908-132">Значение</span><span class="sxs-lookup"><span data-stu-id="6f908-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f908-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f908-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6f908-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6f908-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f908-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f908-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6f908-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6f908-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6f908-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6f908-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f908-138"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="6f908-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f908-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f908-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f908-140">**Объект Дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="6f908-140">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




