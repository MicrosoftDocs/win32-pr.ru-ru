---
description: 'Иусеридентитиманажер:: Манажеидентитиес не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'Метод Иусеридентитиманажер:: Манажеидентитиес (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342435"
---
# <a name="iuseridentitymanagermanageidentities-method"></a><span data-ttu-id="52b60-104">Метод Иусеридентитиманажер:: Манажеидентитиес</span><span class="sxs-lookup"><span data-stu-id="52b60-104">IUserIdentityManager::ManageIdentities method</span></span>

<span data-ttu-id="52b60-105">\[**Иусеридентитиманажер:: манажеидентитиес** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="52b60-105">\[**IUserIdentityManager::ManageIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="52b60-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="52b60-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="52b60-107">Отображает пользовательский интерфейс, позволяющий пользователю управлять удостоверениями пользователей.</span><span class="sxs-lookup"><span data-stu-id="52b60-107">Displays a UI to the user, allowing the user to manage user identities.</span></span>

## <a name="syntax"></a><span data-ttu-id="52b60-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52b60-108">Syntax</span></span>


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="52b60-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="52b60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52b60-110">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="52b60-110">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52b60-111">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="52b60-111">Type: **HWND**</span></span>

<span data-ttu-id="52b60-112">Значение **HWND** , определяющее окно, которое будет перенесено на передний план после закрытия пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="52b60-112">An **HWND** value that identifies a window that will be brought to the foreground after the UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="52b60-113">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="52b60-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52b60-114">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="52b60-114">Type: **DWORD**</span></span>

<span data-ttu-id="52b60-115">Необязательные флаги для определения того, как будет вести себя пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="52b60-115">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="52b60-116">Задайте значение УИМИ \_ создать \_ новое \_ удостоверение, чтобы предложить пользователю создать новое удостоверение.</span><span class="sxs-lookup"><span data-stu-id="52b60-116">Set to UIMI\_CREATE\_NEW\_IDENTITY to prompt the user to create a new identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52b60-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52b60-117">Return value</span></span>

<span data-ttu-id="52b60-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="52b60-118">Type: **HRESULT**</span></span>

<span data-ttu-id="52b60-119">Результат операции управления.</span><span class="sxs-lookup"><span data-stu-id="52b60-119">The result of the management operation.</span></span> <span data-ttu-id="52b60-120">В случае успеха возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="52b60-120">If successful, it returns S\_OK.</span></span> <span data-ttu-id="52b60-121">В противном случае будет возвращен один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="52b60-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="52b60-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="52b60-122">Return code</span></span>                                                                                            | <span data-ttu-id="52b60-123">Описание</span><span class="sxs-lookup"><span data-stu-id="52b60-123">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="52b60-124"><dt>**Электронные \_ удостоверения \_ отключены**</dt></span><span class="sxs-lookup"><span data-stu-id="52b60-124"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="52b60-125">Управление удостоверениями отключено в системе.</span><span class="sxs-lookup"><span data-stu-id="52b60-125">Identity management is disabled on the system.</span></span><br/> |
| <dl> <span data-ttu-id="52b60-126"><dt>**\_ \_ отменено пользователем**</dt></span><span class="sxs-lookup"><span data-stu-id="52b60-126"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="52b60-127">Пользователь отменил диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="52b60-127">The user canceled the dialog.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="52b60-128">Требования</span><span class="sxs-lookup"><span data-stu-id="52b60-128">Requirements</span></span>



| <span data-ttu-id="52b60-129">Требование</span><span class="sxs-lookup"><span data-stu-id="52b60-129">Requirement</span></span> | <span data-ttu-id="52b60-130">Значение</span><span class="sxs-lookup"><span data-stu-id="52b60-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52b60-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52b60-131">Minimum supported client</span></span><br/> | <span data-ttu-id="52b60-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52b60-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="52b60-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52b60-133">Minimum supported server</span></span><br/> | <span data-ttu-id="52b60-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52b60-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="52b60-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="52b60-135">End of client support</span></span><br/>    | <span data-ttu-id="52b60-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="52b60-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="52b60-137">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="52b60-137">End of server support</span></span><br/>    | <span data-ttu-id="52b60-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="52b60-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="52b60-139">Header</span><span class="sxs-lookup"><span data-stu-id="52b60-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="52b60-140"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="52b60-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="52b60-141">IDL</span><span class="sxs-lookup"><span data-stu-id="52b60-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="52b60-142"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="52b60-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="52b60-143">DLL</span><span class="sxs-lookup"><span data-stu-id="52b60-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52b60-144"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52b60-144"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52b60-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52b60-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52b60-146">**иусеридентитиманажер**</span><span class="sxs-lookup"><span data-stu-id="52b60-146">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="52b60-147">**Иусеридентитиманажер:: logon**</span><span class="sxs-lookup"><span data-stu-id="52b60-147">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="52b60-148">**Иусеридентитиманажер:: выход из системы**</span><span class="sxs-lookup"><span data-stu-id="52b60-148">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




