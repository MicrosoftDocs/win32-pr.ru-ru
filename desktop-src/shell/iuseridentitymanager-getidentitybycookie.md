---
description: Жетидентитибикукие не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'Метод Иусеридентитиманажер:: Жетидентитибикукие (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb4e5ad5bda349a5b1650b090abc44a9fd1e6332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539482"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a><span data-ttu-id="f728f-104">Метод Иусеридентитиманажер:: Жетидентитибикукие</span><span class="sxs-lookup"><span data-stu-id="f728f-104">IUserIdentityManager::GetIdentityByCookie method</span></span>

<span data-ttu-id="f728f-105">\[**Жетидентитибикукие** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="f728f-105">\[**GetIdentityByCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f728f-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="f728f-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="f728f-107">Возвращает конкретное удостоверение пользователя по файлу cookie, используемому для уникальной идентификации.</span><span class="sxs-lookup"><span data-stu-id="f728f-107">Gets a specific user identity by the cookie used to uniquely identify it.</span></span>

## <a name="syntax"></a><span data-ttu-id="f728f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f728f-108">Syntax</span></span>


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="f728f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f728f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f728f-110">*уидкукие* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f728f-110">*uidCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f728f-111">Тип: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="f728f-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="f728f-112">Адрес значения _ \*GUID\*\*, представляющего файл cookie для удостоверения, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="f728f-112">The address of a _ *GUID*\* value that represents the cookie for the identity you want to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f728f-113">*ппидентити* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f728f-113">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f728f-114">Тип: **[ **иусеридентити**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f728f-114">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="f728f-115">Адрес указателя, который получит объект удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f728f-115">The address of the pointer that will receive the user identity object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f728f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f728f-116">Return value</span></span>

<span data-ttu-id="f728f-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f728f-117">Type: **HRESULT**</span></span>

<span data-ttu-id="f728f-118">Результат запроса получения.</span><span class="sxs-lookup"><span data-stu-id="f728f-118">The result of the retrieval request.</span></span> <span data-ttu-id="f728f-119">В случае успеха возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f728f-119">If successful, it returns S\_OK.</span></span> <span data-ttu-id="f728f-120">В противном случае будет возвращен один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="f728f-120">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="f728f-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f728f-121">Return code</span></span>                                                                                            | <span data-ttu-id="f728f-122">Описание</span><span class="sxs-lookup"><span data-stu-id="f728f-122">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="f728f-123"><dt>**\_ \_ не найдено удостоверение E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f728f-123"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="f728f-124">Не удалось найти запрошенное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="f728f-124">The identity requested could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="f728f-125"><dt>**Электронные \_ удостоверения \_ отключены**</dt></span><span class="sxs-lookup"><span data-stu-id="f728f-125"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="f728f-126">Управление удостоверениями отключено в системе.</span><span class="sxs-lookup"><span data-stu-id="f728f-126">Identity management is disabled on the system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f728f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f728f-127">Requirements</span></span>



| <span data-ttu-id="f728f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f728f-128">Requirement</span></span> | <span data-ttu-id="f728f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f728f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f728f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f728f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f728f-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f728f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f728f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f728f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f728f-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f728f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f728f-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f728f-134">End of client support</span></span><br/>    | <span data-ttu-id="f728f-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f728f-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="f728f-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f728f-136">End of server support</span></span><br/>    | <span data-ttu-id="f728f-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f728f-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="f728f-138">Header</span><span class="sxs-lookup"><span data-stu-id="f728f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f728f-139"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="f728f-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="f728f-140">IDL</span><span class="sxs-lookup"><span data-stu-id="f728f-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f728f-141"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f728f-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="f728f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f728f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f728f-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f728f-143"><dt>Msident.dll</dt></span></span> </dl> |



 

 




