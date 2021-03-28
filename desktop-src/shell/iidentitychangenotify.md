---
description: Не рекомендуется. Предоставляет уведомления об изменениях в удостоверениях пользователей в системе, а также запросы пользователей на переключение текущего удостоверения пользователя.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Интерфейс Иидентитичанженотифи (Мсидент. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4a217b2cfb046bfb9ae5546e015264f74d00b1d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264410"
---
# <a name="iidentitychangenotify-interface"></a><span data-ttu-id="97e21-104">Интерфейс Иидентитичанженотифи</span><span class="sxs-lookup"><span data-stu-id="97e21-104">IIdentityChangeNotify interface</span></span>

<span data-ttu-id="97e21-105">\[Интерфейс **иидентитичанженотифи** доступен для использования в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="97e21-105">\[The **IIdentityChangeNotify** interface is available for use in Windows 2000.</span></span> <span data-ttu-id="97e21-106">В Windows XP эта функция заменена [учетными записями пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md)и может быть изменена или недоступна в последующих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="97e21-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="97e21-107">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="97e21-107">Deprecated.</span></span> <span data-ttu-id="97e21-108">Предоставляет уведомления об изменениях в удостоверениях пользователей в системе, а также запросы пользователей на переключение текущего удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="97e21-108">Provides notification of modifications to user identities on the system, as well as user requests to switch the current user identity.</span></span>

## <a name="members"></a><span data-ttu-id="97e21-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="97e21-109">Members</span></span>

<span data-ttu-id="97e21-110">Интерфейс **иидентитичанженотифи** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="97e21-110">The **IIdentityChangeNotify** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="97e21-111">**Иидентитичанженотифи** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="97e21-111">**IIdentityChangeNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="97e21-112">Методы</span><span class="sxs-lookup"><span data-stu-id="97e21-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97e21-113">Методы</span><span class="sxs-lookup"><span data-stu-id="97e21-113">Methods</span></span>

<span data-ttu-id="97e21-114">Интерфейс **иидентитичанженотифи** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="97e21-114">The **IIdentityChangeNotify** interface has these methods.</span></span>



| <span data-ttu-id="97e21-115">Метод</span><span class="sxs-lookup"><span data-stu-id="97e21-115">Method</span></span>                                                                                 | <span data-ttu-id="97e21-116">Описание</span><span class="sxs-lookup"><span data-stu-id="97e21-116">Description</span></span>                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97e21-117">**идентитинформатиончанжед**</span><span class="sxs-lookup"><span data-stu-id="97e21-117">**IdentityInformationChanged**</span></span>](iidentitychangenotify-identityinformationchanged.md) | <span data-ttu-id="97e21-118">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="97e21-118">Deprecated.</span></span> <span data-ttu-id="97e21-119">Вызывается при изменении сведений об удостоверении пользователя или при добавлении или удалении удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="97e21-119">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span><br/>  |
| [<span data-ttu-id="97e21-120">**куерисвитчидентитиес**</span><span class="sxs-lookup"><span data-stu-id="97e21-120">**QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)           | <span data-ttu-id="97e21-121">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="97e21-121">Deprecated.</span></span> <span data-ttu-id="97e21-122">Вызывается, когда текущий пользователь запросил переключить удостоверение пользователя, но перед тем, как произойдет переключение.</span><span class="sxs-lookup"><span data-stu-id="97e21-122">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span><br/> |
| [<span data-ttu-id="97e21-123">**свитчидентитиес**</span><span class="sxs-lookup"><span data-stu-id="97e21-123">**SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)                     | <span data-ttu-id="97e21-124">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="97e21-124">Deprecated.</span></span> <span data-ttu-id="97e21-125">Вызывается при переключении удостоверений пользователя.</span><span class="sxs-lookup"><span data-stu-id="97e21-125">Called when user identities are switched.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="97e21-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="97e21-126">Remarks</span></span>

<span data-ttu-id="97e21-127">Чтобы реализовать уведомления, производный интерфейс должен подключаться к [**иусеридентитиманажер**](iuseridentitymanager.md) путем вызова метода [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) и передачи указателя на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="97e21-127">To implement notifications, a derived interface must connect to the [**IUserIdentityManager**](iuseridentitymanager.md) by calling [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) and by passing a pointer to the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e21-128">Требования</span><span class="sxs-lookup"><span data-stu-id="97e21-128">Requirements</span></span>



| <span data-ttu-id="97e21-129">Требование</span><span class="sxs-lookup"><span data-stu-id="97e21-129">Requirement</span></span> | <span data-ttu-id="97e21-130">Значение</span><span class="sxs-lookup"><span data-stu-id="97e21-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97e21-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97e21-131">Minimum supported client</span></span><br/> | <span data-ttu-id="97e21-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="97e21-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="97e21-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97e21-133">Minimum supported server</span></span><br/> | <span data-ttu-id="97e21-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="97e21-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="97e21-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="97e21-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="97e21-136"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="97e21-136"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="97e21-137">IDL</span><span class="sxs-lookup"><span data-stu-id="97e21-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97e21-138"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97e21-138"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="97e21-139">DLL</span><span class="sxs-lookup"><span data-stu-id="97e21-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97e21-140"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97e21-140"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="97e21-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97e21-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e21-142">**иусеридентитиманажер**</span><span class="sxs-lookup"><span data-stu-id="97e21-142">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="97e21-143">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="97e21-143">**IConnectionPoint**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
