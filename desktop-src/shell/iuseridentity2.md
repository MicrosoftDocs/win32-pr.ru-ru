---
description: IUserIdentity2 не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: Интерфейс IUserIdentity2 (Мсидент. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88142e462566a6afaf299096744a0b8f9ea83dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539485"
---
# <a name="iuseridentity2-interface"></a><span data-ttu-id="a1909-104">Интерфейс IUserIdentity2</span><span class="sxs-lookup"><span data-stu-id="a1909-104">IUserIdentity2 interface</span></span>

<span data-ttu-id="a1909-105">\[**IUserIdentity2** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="a1909-105">\[**IUserIdentity2** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="a1909-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="a1909-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="a1909-107">Предоставляет методы, предоставляющие имена, пароли и порядковые номера для конкретного удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a1909-107">Exposes methods that provide naming, password, and ordinal control for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="a1909-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="a1909-108">Members</span></span>

<span data-ttu-id="a1909-109">Интерфейс **IUserIdentity2** наследует от [**иусеридентити**](iuseridentity.md).</span><span class="sxs-lookup"><span data-stu-id="a1909-109">The **IUserIdentity2** interface inherits from [**IUserIdentity**](iuseridentity.md).</span></span> <span data-ttu-id="a1909-110">**IUserIdentity2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a1909-110">**IUserIdentity2** also has these types of members:</span></span>

-   [<span data-ttu-id="a1909-111">Методы</span><span class="sxs-lookup"><span data-stu-id="a1909-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a1909-112">Методы</span><span class="sxs-lookup"><span data-stu-id="a1909-112">Methods</span></span>

<span data-ttu-id="a1909-113">Интерфейс **IUserIdentity2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a1909-113">The **IUserIdentity2** interface has these methods.</span></span>



| <span data-ttu-id="a1909-114">Метод</span><span class="sxs-lookup"><span data-stu-id="a1909-114">Method</span></span>                                                  | <span data-ttu-id="a1909-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a1909-115">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="a1909-116">**ChangePassword;**</span><span class="sxs-lookup"><span data-stu-id="a1909-116">**ChangePassword**</span></span>](iuseridentity2-changepassword.md) | <span data-ttu-id="a1909-117">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a1909-117">Deprecated.</span></span> <span data-ttu-id="a1909-118">Задает новый пароль для удостоверения.</span><span class="sxs-lookup"><span data-stu-id="a1909-118">Sets a new password for the identity.</span></span><br/>      |
| [<span data-ttu-id="a1909-119">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="a1909-119">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)         | <span data-ttu-id="a1909-120">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a1909-120">Deprecated.</span></span> <span data-ttu-id="a1909-121">Возвращает порядковый номер этого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="a1909-121">Gets the ordinal number for this identity.</span></span><br/> |
| [<span data-ttu-id="a1909-122">**SetName**</span><span class="sxs-lookup"><span data-stu-id="a1909-122">**SetName**</span></span>](iuseridentity2-setname.md)               | <span data-ttu-id="a1909-123">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a1909-123">Deprecated.</span></span> <span data-ttu-id="a1909-124">Задает отображаемое имя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="a1909-124">Sets the display name of the identity.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="a1909-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1909-125">Remarks</span></span>

<span data-ttu-id="a1909-126">Этот интерфейс также предоставляет методы интерфейса [**иусеридентити**](iuseridentity.md) , от которых он наследуется.</span><span class="sxs-lookup"><span data-stu-id="a1909-126">This interface also provides the methods of the [**IUserIdentity**](iuseridentity.md) interface, from which it inherits.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1909-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a1909-127">Requirements</span></span>



| <span data-ttu-id="a1909-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a1909-128">Requirement</span></span> | <span data-ttu-id="a1909-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a1909-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1909-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1909-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a1909-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a1909-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a1909-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1909-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a1909-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a1909-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a1909-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a1909-134">End of client support</span></span><br/>    | <span data-ttu-id="a1909-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a1909-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a1909-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a1909-136">End of server support</span></span><br/>    | <span data-ttu-id="a1909-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1909-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a1909-138">Header</span><span class="sxs-lookup"><span data-stu-id="a1909-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1909-139"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1909-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1909-140">IDL</span><span class="sxs-lookup"><span data-stu-id="a1909-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a1909-141"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a1909-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="a1909-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a1909-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1909-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1909-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1909-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1909-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1909-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="a1909-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> </dl>

 

 




