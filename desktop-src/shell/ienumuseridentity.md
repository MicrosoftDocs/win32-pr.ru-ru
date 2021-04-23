---
description: Иенумусеридентити не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Интерфейс Иенумусеридентити (Мсидент. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985412"
---
# <a name="ienumuseridentity-interface"></a><span data-ttu-id="3ae28-104">Интерфейс Иенумусеридентити</span><span class="sxs-lookup"><span data-stu-id="3ae28-104">IEnumUserIdentity interface</span></span>

<span data-ttu-id="3ae28-105">\[**Иенумусеридентити** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="3ae28-105">\[**IEnumUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="3ae28-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="3ae28-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="3ae28-107">Предоставляет перечисление всех удостоверений пользователей, имеющихся в системе.</span><span class="sxs-lookup"><span data-stu-id="3ae28-107">Provides enumeration of all user identities present on the system.</span></span>

## <a name="members"></a><span data-ttu-id="3ae28-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="3ae28-108">Members</span></span>

<span data-ttu-id="3ae28-109">Интерфейс **иенумусеридентити** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3ae28-109">The **IEnumUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3ae28-110">**Иенумусеридентити** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3ae28-110">**IEnumUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="3ae28-111">Методы</span><span class="sxs-lookup"><span data-stu-id="3ae28-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3ae28-112">Методы</span><span class="sxs-lookup"><span data-stu-id="3ae28-112">Methods</span></span>

<span data-ttu-id="3ae28-113">Интерфейс **иенумусеридентити** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3ae28-113">The **IEnumUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="3ae28-114">Метод</span><span class="sxs-lookup"><span data-stu-id="3ae28-114">Method</span></span>                                         | <span data-ttu-id="3ae28-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3ae28-115">Description</span></span>                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ae28-116">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="3ae28-116">**Clone**</span></span>](ienumuseridentity-clone.md)       | <span data-ttu-id="3ae28-117">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3ae28-117">Deprecated.</span></span> <span data-ttu-id="3ae28-118">Возвращает копию текущего перечисления.</span><span class="sxs-lookup"><span data-stu-id="3ae28-118">Gets a copy of the current enumeration.</span></span><br/>                                                               |
| [<span data-ttu-id="3ae28-119">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="3ae28-119">**GetCount**</span></span>](ienumuseridentity-getcount.md) | <span data-ttu-id="3ae28-120">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3ae28-120">Deprecated.</span></span> <span data-ttu-id="3ae28-121">Возвращает число удостоверений пользователей, находящихся в системе в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="3ae28-121">Gets the count of user identities currently on the system.</span></span><br/>                                            |
| [<span data-ttu-id="3ae28-122">**Далее**</span><span class="sxs-lookup"><span data-stu-id="3ae28-122">**Next**</span></span>](ienumuseridentity-next.md)         | <span data-ttu-id="3ae28-123">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3ae28-123">Deprecated.</span></span> <span data-ttu-id="3ae28-124">Извлекает из перечисления массив интерфейсов удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3ae28-124">Retrieves an array of user identity interfaces from the enumeration.</span></span><br/>                                  |
| [<span data-ttu-id="3ae28-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="3ae28-125">**Reset**</span></span>](ienumuseridentity-reset.md)       | <span data-ttu-id="3ae28-126">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3ae28-126">Deprecated.</span></span> <span data-ttu-id="3ae28-127">Сбрасывает внутреннее число извлеченных интерфейсов в перечислении.</span><span class="sxs-lookup"><span data-stu-id="3ae28-127">Resets the internal count of retrieved interfaces in the enumeration.</span></span><br/>                                 |
| [<span data-ttu-id="3ae28-128">**Сразу**</span><span class="sxs-lookup"><span data-stu-id="3ae28-128">**Skip**</span></span>](ienumuseridentity-skip.md)         | <span data-ttu-id="3ae28-129">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3ae28-129">Deprecated.</span></span> <span data-ttu-id="3ae28-130">Пропускает заданное число интерфейсов удостоверения пользователя в перечислении.</span><span class="sxs-lookup"><span data-stu-id="3ae28-130">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="3ae28-131">Используется при извлечении интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="3ae28-131">Used when retrieving interfaces.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3ae28-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="3ae28-132">Remarks</span></span>

<span data-ttu-id="3ae28-133">Для получения сведений об удостоверениях пользователей, имеющихся в системе, можно использовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="3ae28-133">To retrieve information about user identities present on the system, you can use this interface.</span></span> <span data-ttu-id="3ae28-134">Чтобы получить этот интерфейс, из интерфейса [**иусеридентитиманажер**](iuseridentitymanager.md) можно вызвать [**Иусеридентитиманажер:: енумидентитиес**](iuseridentitymanager-enumidentities.md) .</span><span class="sxs-lookup"><span data-stu-id="3ae28-134">From a [**IUserIdentityManager**](iuseridentitymanager.md) interface, you can call [**IUserIdentityManager::EnumIdentities**](iuseridentitymanager-enumidentities.md) to retrieve this interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ae28-135">Требования</span><span class="sxs-lookup"><span data-stu-id="3ae28-135">Requirements</span></span>



| <span data-ttu-id="3ae28-136">Требование</span><span class="sxs-lookup"><span data-stu-id="3ae28-136">Requirement</span></span> | <span data-ttu-id="3ae28-137">Значение</span><span class="sxs-lookup"><span data-stu-id="3ae28-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae28-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ae28-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae28-139">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3ae28-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3ae28-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ae28-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae28-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ae28-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3ae28-142">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3ae28-142">End of client support</span></span><br/>    | <span data-ttu-id="3ae28-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3ae28-143">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="3ae28-144">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="3ae28-144">End of server support</span></span><br/>    | <span data-ttu-id="3ae28-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ae28-145">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="3ae28-146">Header</span><span class="sxs-lookup"><span data-stu-id="3ae28-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ae28-147"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ae28-147"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ae28-148">IDL</span><span class="sxs-lookup"><span data-stu-id="3ae28-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ae28-149"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ae28-149"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ae28-150">DLL</span><span class="sxs-lookup"><span data-stu-id="3ae28-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ae28-151"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ae28-151"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ae28-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ae28-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ae28-153">**иусеридентитиманажер**</span><span class="sxs-lookup"><span data-stu-id="3ae28-153">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> </dl>

 

 
