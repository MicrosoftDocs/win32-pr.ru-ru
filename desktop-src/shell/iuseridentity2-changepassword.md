---
description: ChangePassword не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'Метод IUserIdentity2:: ChangePassword (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984605"
---
# <a name="iuseridentity2changepassword-method"></a><span data-ttu-id="e08ae-104">Метод IUserIdentity2:: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="e08ae-104">IUserIdentity2::ChangePassword method</span></span>

<span data-ttu-id="e08ae-105">\[**ChangePassword** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="e08ae-105">\[**ChangePassword** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="e08ae-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="e08ae-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="e08ae-107">Задает новый пароль для удостоверения.</span><span class="sxs-lookup"><span data-stu-id="e08ae-107">Sets a new password for the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="e08ae-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e08ae-108">Syntax</span></span>


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a><span data-ttu-id="e08ae-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e08ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e08ae-110">*сзолдпасс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e08ae-110">*szOldPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e08ae-111">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="e08ae-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="e08ae-112">Строка расширенных символов, содержащая пароль, который в настоящее время связан с удостоверением.</span><span class="sxs-lookup"><span data-stu-id="e08ae-112">The wide-character string that contains the password currently associated with the identity.</span></span>

</dd> <dt>

<span data-ttu-id="e08ae-113">_szNewPass \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e08ae-113">_szNewPass\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e08ae-114">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="e08ae-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="e08ae-115">Строка расширенных символов, содержащая новый пароль, который должен быть связан с удостоверением.</span><span class="sxs-lookup"><span data-stu-id="e08ae-115">The wide-character string that contains the new password to be associated with the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e08ae-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e08ae-116">Return value</span></span>

<span data-ttu-id="e08ae-117">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e08ae-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e08ae-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e08ae-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e08ae-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e08ae-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e08ae-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="e08ae-120">Remarks</span></span>

<span data-ttu-id="e08ae-121">Значение параметра *сзолдпасс* должно соответствовать текущему паролю удостоверения, применяемого для *сзневпасс* .</span><span class="sxs-lookup"><span data-stu-id="e08ae-121">The value of *szOldPass* must match the current password of the identity for *szNewPass* to be applied.</span></span> <span data-ttu-id="e08ae-122">Неправильное значение *сзолдпасс* приведет к возвращению значения E с \_ ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e08ae-122">An incorrect value of *szOldPass* will result in a return value of E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e08ae-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e08ae-123">Requirements</span></span>



| <span data-ttu-id="e08ae-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e08ae-124">Requirement</span></span> | <span data-ttu-id="e08ae-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e08ae-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e08ae-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e08ae-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e08ae-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e08ae-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e08ae-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e08ae-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e08ae-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e08ae-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e08ae-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e08ae-130">End of client support</span></span><br/>    | <span data-ttu-id="e08ae-131">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e08ae-131">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="e08ae-132">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e08ae-132">End of server support</span></span><br/>    | <span data-ttu-id="e08ae-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e08ae-133">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="e08ae-134">Header</span><span class="sxs-lookup"><span data-stu-id="e08ae-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e08ae-135"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="e08ae-135"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="e08ae-136">IDL</span><span class="sxs-lookup"><span data-stu-id="e08ae-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e08ae-137"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e08ae-137"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="e08ae-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e08ae-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e08ae-139"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e08ae-139"><dt>Msident.dll</dt></span></span> </dl> |



 

 




