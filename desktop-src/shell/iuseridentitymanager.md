---
description: Иусеридентитиманажер не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Интерфейс Иусеридентитиманажер (Мсидент. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896550"
---
# <a name="iuseridentitymanager-interface"></a><span data-ttu-id="468cf-104">Интерфейс Иусеридентитиманажер</span><span class="sxs-lookup"><span data-stu-id="468cf-104">IUserIdentityManager interface</span></span>

<span data-ttu-id="468cf-105">\[**Иусеридентитиманажер** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="468cf-105">\[**IUserIdentityManager** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="468cf-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="468cf-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="468cf-107">Предоставляет методы для идентификации, перечисления и управления удостоверениями пользователей в системе.</span><span class="sxs-lookup"><span data-stu-id="468cf-107">Exposes methods that identify, enumerate, and manage user identities on the system.</span></span>

## <a name="members"></a><span data-ttu-id="468cf-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="468cf-108">Members</span></span>

<span data-ttu-id="468cf-109">Интерфейс **иусеридентитиманажер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="468cf-109">The **IUserIdentityManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="468cf-110">**Иусеридентитиманажер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="468cf-110">**IUserIdentityManager** also has these types of members:</span></span>

-   [<span data-ttu-id="468cf-111">Методы</span><span class="sxs-lookup"><span data-stu-id="468cf-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="468cf-112">Методы</span><span class="sxs-lookup"><span data-stu-id="468cf-112">Methods</span></span>

<span data-ttu-id="468cf-113">Интерфейс **иусеридентитиманажер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="468cf-113">The **IUserIdentityManager** interface has these methods.</span></span>



| <span data-ttu-id="468cf-114">Метод</span><span class="sxs-lookup"><span data-stu-id="468cf-114">Method</span></span>                                                                  | <span data-ttu-id="468cf-115">Описание</span><span class="sxs-lookup"><span data-stu-id="468cf-115">Description</span></span>                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="468cf-116">**енумидентитиес**</span><span class="sxs-lookup"><span data-stu-id="468cf-116">**EnumIdentities**</span></span>](iuseridentitymanager-enumidentities.md)           | <span data-ttu-id="468cf-117">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="468cf-117">Deprecated.</span></span> <span data-ttu-id="468cf-118">Возвращает объект [**иенумусеридентити**](ienumuseridentity.md) , который можно использовать для перечисления удостоверений пользователей, имеющихся в системе.</span><span class="sxs-lookup"><span data-stu-id="468cf-118">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span><br/> |
| [<span data-ttu-id="468cf-119">**жетидентитибикукие**</span><span class="sxs-lookup"><span data-stu-id="468cf-119">**GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md) | <span data-ttu-id="468cf-120">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="468cf-120">Deprecated.</span></span> <span data-ttu-id="468cf-121">Возвращает конкретное удостоверение пользователя по файлу cookie, используемому для уникальной идентификации.</span><span class="sxs-lookup"><span data-stu-id="468cf-121">Gets a specific user identity by the cookie used to uniquely identify it.</span></span><br/>                                                                        |
| [<span data-ttu-id="468cf-122">**Выполнен**</span><span class="sxs-lookup"><span data-stu-id="468cf-122">**Logoff**</span></span>](iuseridentitymanager-logoff.md)                           | <span data-ttu-id="468cf-123">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="468cf-123">Deprecated.</span></span> <span data-ttu-id="468cf-124">Выйдите из текущего удостоверения.</span><span class="sxs-lookup"><span data-stu-id="468cf-124">Log off the current identity.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="468cf-125">**Входа**</span><span class="sxs-lookup"><span data-stu-id="468cf-125">**Logon**</span></span>](iuseridentitymanager-logon.md)                             | <span data-ttu-id="468cf-126">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="468cf-126">Deprecated.</span></span> <span data-ttu-id="468cf-127">Отображает пользовательский интерфейс, позволяющий пользователю выбрать удостоверение пользователя.</span><span class="sxs-lookup"><span data-stu-id="468cf-127">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="468cf-128">В случае успешного выполнения удостоверение пользователя будет зарегистрировано и извлечено.</span><span class="sxs-lookup"><span data-stu-id="468cf-128">If successful, the user identity will be logged on and retrieved.</span></span><br/>        |
| [<span data-ttu-id="468cf-129">**манажеидентитиес**</span><span class="sxs-lookup"><span data-stu-id="468cf-129">**ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)       | <span data-ttu-id="468cf-130">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="468cf-130">Deprecated.</span></span> <span data-ttu-id="468cf-131">Отображает пользовательский интерфейс, позволяющий пользователю управлять удостоверениями пользователей.</span><span class="sxs-lookup"><span data-stu-id="468cf-131">Displays a UI to the user, allowing the user to manage user identities.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="468cf-132">Требования</span><span class="sxs-lookup"><span data-stu-id="468cf-132">Requirements</span></span>



| <span data-ttu-id="468cf-133">Требование</span><span class="sxs-lookup"><span data-stu-id="468cf-133">Requirement</span></span> | <span data-ttu-id="468cf-134">Значение</span><span class="sxs-lookup"><span data-stu-id="468cf-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="468cf-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="468cf-135">Minimum supported client</span></span><br/> | <span data-ttu-id="468cf-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="468cf-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="468cf-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="468cf-137">Minimum supported server</span></span><br/> | <span data-ttu-id="468cf-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="468cf-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="468cf-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="468cf-139">End of client support</span></span><br/>    | <span data-ttu-id="468cf-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="468cf-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="468cf-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="468cf-141">End of server support</span></span><br/>    | <span data-ttu-id="468cf-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="468cf-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="468cf-143">Header</span><span class="sxs-lookup"><span data-stu-id="468cf-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="468cf-144"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="468cf-144"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="468cf-145">IDL</span><span class="sxs-lookup"><span data-stu-id="468cf-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="468cf-146"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="468cf-146"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="468cf-147">DLL</span><span class="sxs-lookup"><span data-stu-id="468cf-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="468cf-148"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="468cf-148"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="468cf-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="468cf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="468cf-150">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="468cf-150">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="468cf-151">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="468cf-151">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="468cf-152">**иенумусеридентити**</span><span class="sxs-lookup"><span data-stu-id="468cf-152">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="468cf-153">**иидентитичанженотифи**</span><span class="sxs-lookup"><span data-stu-id="468cf-153">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> </dl>

 

 
