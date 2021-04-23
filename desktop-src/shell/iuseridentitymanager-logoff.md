---
description: Выход из системы не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: 'Метод Иусеридентитиманажер:: logoff (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logoff
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 4266e6116e43b7b792c3040d7c86a60037ca4c44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984156"
---
# <a name="iuseridentitymanagerlogoff-method"></a><span data-ttu-id="63309-104">Метод Иусеридентитиманажер:: logoff</span><span class="sxs-lookup"><span data-stu-id="63309-104">IUserIdentityManager::Logoff method</span></span>

<span data-ttu-id="63309-105">\[**Выход из системы** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="63309-105">\[**Logoff** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="63309-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="63309-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="63309-107">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="63309-107">Deprecated.</span></span> <span data-ttu-id="63309-108">Выйдите из текущего удостоверения.</span><span class="sxs-lookup"><span data-stu-id="63309-108">Log off the current identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="63309-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63309-109">Syntax</span></span>


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="63309-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="63309-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63309-111">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63309-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63309-112">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="63309-112">Type: **HWND**</span></span>

<span data-ttu-id="63309-113">Значение **HWND** , определяющее окно, которое будет перенесено на передний план после завершения выхода.</span><span class="sxs-lookup"><span data-stu-id="63309-113">An **HWND** value that identifies a window that will be brought into the foreground when the logoff is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63309-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63309-114">Return value</span></span>

<span data-ttu-id="63309-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="63309-115">Type: **HRESULT**</span></span>

<span data-ttu-id="63309-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="63309-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63309-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63309-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="63309-118">Требования</span><span class="sxs-lookup"><span data-stu-id="63309-118">Requirements</span></span>



| <span data-ttu-id="63309-119">Требование</span><span class="sxs-lookup"><span data-stu-id="63309-119">Requirement</span></span> | <span data-ttu-id="63309-120">Значение</span><span class="sxs-lookup"><span data-stu-id="63309-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63309-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63309-121">Minimum supported client</span></span><br/> | <span data-ttu-id="63309-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63309-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="63309-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63309-123">Minimum supported server</span></span><br/> | <span data-ttu-id="63309-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63309-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="63309-125">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="63309-125">End of client support</span></span><br/>    | <span data-ttu-id="63309-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="63309-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="63309-127">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="63309-127">End of server support</span></span><br/>    | <span data-ttu-id="63309-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63309-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="63309-129">Header</span><span class="sxs-lookup"><span data-stu-id="63309-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="63309-130"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="63309-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="63309-131">IDL</span><span class="sxs-lookup"><span data-stu-id="63309-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63309-132"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63309-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="63309-133">DLL</span><span class="sxs-lookup"><span data-stu-id="63309-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63309-134"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63309-134"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63309-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63309-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63309-136">**иусеридентитиманажер**</span><span class="sxs-lookup"><span data-stu-id="63309-136">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="63309-137">**Иусеридентитиманажер:: logon**</span><span class="sxs-lookup"><span data-stu-id="63309-137">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="63309-138">**Иусеридентитиманажер:: Манажеидентитиес**</span><span class="sxs-lookup"><span data-stu-id="63309-138">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




