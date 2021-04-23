---
description: 'Иусеридентитиманажер:: logon не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'Метод Иусеридентитиманажер:: logon (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143021"
---
# <a name="iuseridentitymanagerlogon-method"></a><span data-ttu-id="db4d7-104">Метод Иусеридентитиманажер:: logon</span><span class="sxs-lookup"><span data-stu-id="db4d7-104">IUserIdentityManager::Logon method</span></span>

<span data-ttu-id="db4d7-105">\[**Иусеридентитиманажер:: logon** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="db4d7-105">\[**IUserIdentityManager::Logon** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="db4d7-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="db4d7-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="db4d7-107">Отображает пользовательский интерфейс, позволяющий пользователю выбрать удостоверение пользователя.</span><span class="sxs-lookup"><span data-stu-id="db4d7-107">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="db4d7-108">В случае успешного выполнения удостоверение пользователя будет зарегистрировано и извлечено.</span><span class="sxs-lookup"><span data-stu-id="db4d7-108">If successful, the user identity will be logged on and retrieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="db4d7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db4d7-109">Syntax</span></span>


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="db4d7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="db4d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db4d7-111">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db4d7-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db4d7-112">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="db4d7-112">Type: **HWND**</span></span>

<span data-ttu-id="db4d7-113">Значение **HWND** , определяющее окно, которое будет перенесено на передний план после закрытия пользовательского интерфейса входа.</span><span class="sxs-lookup"><span data-stu-id="db4d7-113">An **HWND** value that identifies a window that will be brought to the foreground after the logon UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="db4d7-114">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db4d7-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db4d7-115">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="db4d7-115">Type: **DWORD**</span></span>

<span data-ttu-id="db4d7-116">Необязательные флаги для определения того, как будет вести себя пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="db4d7-116">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="db4d7-117">Задайте значение Уил \_ Force \_ UI, чтобы заставить пользовательский интерфейс отображаться, даже если удостоверение уже выбрано.</span><span class="sxs-lookup"><span data-stu-id="db4d7-117">Set to UIL\_FORCE\_UI to force the UI to display, even if an identity has already been chosen.</span></span>

</dd> <dt>

<span data-ttu-id="db4d7-118">*ппидентити* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db4d7-118">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db4d7-119">Тип: **[ **иусеридентити**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="db4d7-119">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="db4d7-120">Адрес указателя, который получает выбранное удостоверение пользователя.</span><span class="sxs-lookup"><span data-stu-id="db4d7-120">The address of the pointer that receives the chosen user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db4d7-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db4d7-121">Return value</span></span>

<span data-ttu-id="db4d7-122">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="db4d7-122">Type: **HRESULT**</span></span>

<span data-ttu-id="db4d7-123">Результат операции входа в систему.</span><span class="sxs-lookup"><span data-stu-id="db4d7-123">Result of the logon operation.</span></span> <span data-ttu-id="db4d7-124">В случае успеха возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="db4d7-124">If successful, it returns S\_OK.</span></span> <span data-ttu-id="db4d7-125">В противном случае будет возвращен один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="db4d7-125">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="db4d7-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="db4d7-126">Return code</span></span>                                                                                            | <span data-ttu-id="db4d7-127">Описание</span><span class="sxs-lookup"><span data-stu-id="db4d7-127">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db4d7-128"><dt>**\_ \_ отменено пользователем**</dt></span><span class="sxs-lookup"><span data-stu-id="db4d7-128"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="db4d7-129">Пользователь отменил операцию входа из пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="db4d7-129">The user canceled the logon operation from the UI.</span></span><br/>                               |
| <dl> <span data-ttu-id="db4d7-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="db4d7-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="db4d7-131">Не удалось создать удостоверение пользователя.</span><span class="sxs-lookup"><span data-stu-id="db4d7-131">The user identity could not be created.</span></span><br/>                                          |
| <dl> <span data-ttu-id="db4d7-132"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="db4d7-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="db4d7-133">Непредвиденный сбой операции.</span><span class="sxs-lookup"><span data-stu-id="db4d7-133">The operation failed unexpectedly.</span></span><br/>                                               |
| <dl> <span data-ttu-id="db4d7-134"><dt>**Электронные \_ удостоверения \_ отключены**</dt></span><span class="sxs-lookup"><span data-stu-id="db4d7-134"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="db4d7-135">Управление удостоверениями отключено в системе.</span><span class="sxs-lookup"><span data-stu-id="db4d7-135">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="db4d7-136"><dt>**\_удостоверения \_ отключены**</dt></span><span class="sxs-lookup"><span data-stu-id="db4d7-136"><dt>**S\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="db4d7-137">Управление удостоверениями отключено в системе.</span><span class="sxs-lookup"><span data-stu-id="db4d7-137">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="db4d7-138"><dt>**\_Изменение идентификатора \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="db4d7-138"><dt>**E\_IDENTITY\_CHANGING**</dt></span></span> </dl>   | <span data-ttu-id="db4d7-139">Система в настоящее время переключает удостоверения и не может выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="db4d7-139">The system is currently switching identities, and cannot complete the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="db4d7-140">Требования</span><span class="sxs-lookup"><span data-stu-id="db4d7-140">Requirements</span></span>



| <span data-ttu-id="db4d7-141">Требование</span><span class="sxs-lookup"><span data-stu-id="db4d7-141">Requirement</span></span> | <span data-ttu-id="db4d7-142">Значение</span><span class="sxs-lookup"><span data-stu-id="db4d7-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db4d7-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db4d7-143">Minimum supported client</span></span><br/> | <span data-ttu-id="db4d7-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="db4d7-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="db4d7-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db4d7-145">Minimum supported server</span></span><br/> | <span data-ttu-id="db4d7-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="db4d7-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="db4d7-147">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="db4d7-147">End of client support</span></span><br/>    | <span data-ttu-id="db4d7-148">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="db4d7-148">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="db4d7-149">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="db4d7-149">End of server support</span></span><br/>    | <span data-ttu-id="db4d7-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="db4d7-150">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="db4d7-151">Header</span><span class="sxs-lookup"><span data-stu-id="db4d7-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="db4d7-152"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="db4d7-152"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="db4d7-153">IDL</span><span class="sxs-lookup"><span data-stu-id="db4d7-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db4d7-154"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db4d7-154"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="db4d7-155">DLL</span><span class="sxs-lookup"><span data-stu-id="db4d7-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db4d7-156"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db4d7-156"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db4d7-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db4d7-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4d7-158">**иусеридентитиманажер**</span><span class="sxs-lookup"><span data-stu-id="db4d7-158">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="db4d7-159">**Иусеридентитиманажер:: выход из системы**</span><span class="sxs-lookup"><span data-stu-id="db4d7-159">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> <dt>

[<span data-ttu-id="db4d7-160">**Иусеридентитиманажер:: Манажеидентитиес**</span><span class="sxs-lookup"><span data-stu-id="db4d7-160">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




