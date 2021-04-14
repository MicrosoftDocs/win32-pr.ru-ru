---
description: Иусеридентити не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Интерфейс Иусеридентити (Мсидент. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985401"
---
# <a name="iuseridentity-interface"></a><span data-ttu-id="e79ac-104">Интерфейс Иусеридентити</span><span class="sxs-lookup"><span data-stu-id="e79ac-104">IUserIdentity interface</span></span>

<span data-ttu-id="e79ac-105">\[**Иусеридентити** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="e79ac-105">\[**IUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="e79ac-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="e79ac-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="e79ac-107">Предоставляет методы, предоставляющие данные для идентификации, реестра и папки для конкретного удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e79ac-107">Exposes methods that provide identification, registry, and folder data for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="e79ac-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="e79ac-108">Members</span></span>

<span data-ttu-id="e79ac-109">Интерфейс **иусеридентити** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e79ac-109">The **IUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e79ac-110">**Иусеридентити** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e79ac-110">**IUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="e79ac-111">Методы</span><span class="sxs-lookup"><span data-stu-id="e79ac-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e79ac-112">Методы</span><span class="sxs-lookup"><span data-stu-id="e79ac-112">Methods</span></span>

<span data-ttu-id="e79ac-113">Интерфейс **иусеридентити** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e79ac-113">The **IUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="e79ac-114">Метод</span><span class="sxs-lookup"><span data-stu-id="e79ac-114">Method</span></span>                                                         | <span data-ttu-id="e79ac-115">Описание</span><span class="sxs-lookup"><span data-stu-id="e79ac-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e79ac-116">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="e79ac-116">**GetCookie**</span></span>](iuseridentity-getcookie.md)                   | <span data-ttu-id="e79ac-117">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e79ac-117">Deprecated.</span></span> <span data-ttu-id="e79ac-118">Возвращает файл cookie, используемый для уникальной идентификации этого удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e79ac-118">Gets the cookie used to uniquely identify this user identity.</span></span><br/>             |
| [<span data-ttu-id="e79ac-119">**жетидентитифолдер**</span><span class="sxs-lookup"><span data-stu-id="e79ac-119">**GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)   | <span data-ttu-id="e79ac-120">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e79ac-120">Deprecated.</span></span> <span data-ttu-id="e79ac-121">Возвращает файловую папку, связанную с этим удостоверением.</span><span class="sxs-lookup"><span data-stu-id="e79ac-121">Gets the file folder associated with this identity.</span></span><br/>                       |
| [<span data-ttu-id="e79ac-122">**GetName**</span><span class="sxs-lookup"><span data-stu-id="e79ac-122">**GetName**</span></span>](iuseridentity-getname.md)                       | <span data-ttu-id="e79ac-123">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e79ac-123">Deprecated.</span></span> <span data-ttu-id="e79ac-124">Возвращает имя, связанное с этим удостоверением пользователя.</span><span class="sxs-lookup"><span data-stu-id="e79ac-124">Gets the name associated with this user identity.</span></span><br/>                         |
| [<span data-ttu-id="e79ac-125">**опенидентитирегкэй**</span><span class="sxs-lookup"><span data-stu-id="e79ac-125">**OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md) | <span data-ttu-id="e79ac-126">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e79ac-126">Deprecated.</span></span> <span data-ttu-id="e79ac-127">Извлекает ключ в реестре, соответствующий этому удостоверению пользователя.</span><span class="sxs-lookup"><span data-stu-id="e79ac-127">Retrieves the key in the registry that corresponds to this user identity.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e79ac-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="e79ac-128">Remarks</span></span>

<span data-ttu-id="e79ac-129">Этот интерфейс предоставляет сведения, соответствующие конкретному удостоверению пользователя, присутствующему в системе.</span><span class="sxs-lookup"><span data-stu-id="e79ac-129">This interface provides information that corresponds to a specific user identity present on the system.</span></span> <span data-ttu-id="e79ac-130">Вы можете получить доступ к папке удостоверений этого пользователя, ключу реестра и файлу cookie для идентификации, а также получить имя, связанное с удостоверением пользователя.</span><span class="sxs-lookup"><span data-stu-id="e79ac-130">You can access this user identity's identity folder, its registry key, and its identification cookie, as well as retrieve the name associated with the user identity.</span></span>

## <a name="requirements"></a><span data-ttu-id="e79ac-131">Требования</span><span class="sxs-lookup"><span data-stu-id="e79ac-131">Requirements</span></span>



| <span data-ttu-id="e79ac-132">Требование</span><span class="sxs-lookup"><span data-stu-id="e79ac-132">Requirement</span></span> | <span data-ttu-id="e79ac-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e79ac-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e79ac-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e79ac-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e79ac-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e79ac-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e79ac-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e79ac-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e79ac-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e79ac-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e79ac-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e79ac-138">End of client support</span></span><br/>    | <span data-ttu-id="e79ac-139">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e79ac-139">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="e79ac-140">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e79ac-140">End of server support</span></span><br/>    | <span data-ttu-id="e79ac-141">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e79ac-141">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="e79ac-142">Header</span><span class="sxs-lookup"><span data-stu-id="e79ac-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e79ac-143"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="e79ac-143"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="e79ac-144">IDL</span><span class="sxs-lookup"><span data-stu-id="e79ac-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e79ac-145"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e79ac-145"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="e79ac-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e79ac-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e79ac-147"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e79ac-147"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e79ac-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e79ac-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e79ac-149">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="e79ac-149">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="e79ac-150">**иусеридентитиманажер**</span><span class="sxs-lookup"><span data-stu-id="e79ac-150">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="e79ac-151">**иенумусеридентити**</span><span class="sxs-lookup"><span data-stu-id="e79ac-151">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> </dl>

 

 
