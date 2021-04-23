---
description: Жетидентитифолдер не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: 'Метод Иусеридентити:: Жетидентитифолдер (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 9f2644570bb7ccc2ae5bee8a37d4471ffb65861a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984612"
---
# <a name="iuseridentitygetidentityfolder-method"></a><span data-ttu-id="26486-104">Метод Иусеридентити:: Жетидентитифолдер</span><span class="sxs-lookup"><span data-stu-id="26486-104">IUserIdentity::GetIdentityFolder method</span></span>

<span data-ttu-id="26486-105">\[**Жетидентитифолдер** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="26486-105">\[**GetIdentityFolder** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="26486-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="26486-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="26486-107">Возвращает файловую папку, связанную с этим удостоверением.</span><span class="sxs-lookup"><span data-stu-id="26486-107">Gets the file folder associated with this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="26486-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26486-108">Syntax</span></span>


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="26486-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="26486-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26486-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26486-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26486-111">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="26486-111">Type: **DWORD**</span></span>

<span data-ttu-id="26486-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="26486-112">Required.</span></span> <span data-ttu-id="26486-113">Значение типа, указывающее, является ли папка, связанная с этим удостоверением, перемещаемой.</span><span class="sxs-lookup"><span data-stu-id="26486-113">A value that specifies whether the folder associated with this identity is roaming.</span></span> <span data-ttu-id="26486-114">Должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="26486-114">Must be one of the following values.</span></span>

<dt>



 <span data-ttu-id="26486-115">(GIF \_ ПЕРЕМЕЩАЕМая \_ Папка)</span><span class="sxs-lookup"><span data-stu-id="26486-115">(GIF\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="26486-116">Папка является перемещаемой.</span><span class="sxs-lookup"><span data-stu-id="26486-116">The folder is roaming.</span></span>

</dd> <dt>



 <span data-ttu-id="26486-117">(GIF \_ НЕ \_ перемещаемая \_ Папка)</span><span class="sxs-lookup"><span data-stu-id="26486-117">(GIF\_NON\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="26486-118">Папка является локальной.</span><span class="sxs-lookup"><span data-stu-id="26486-118">The folder is local.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="26486-119">*псзпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26486-119">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26486-120">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="26486-120">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="26486-121">Указатель на строку расширенных символов, которая получает путь к папке.</span><span class="sxs-lookup"><span data-stu-id="26486-121">A pointer to a wide-character string that receives the folder path.</span></span>

</dd> <dt>

<span data-ttu-id="26486-122">_ulBuffSize \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="26486-122">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26486-123">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="26486-123">Type: **ULONG**</span></span>

<span data-ttu-id="26486-124">Значение типа, указывающее размер *псзпас*.</span><span class="sxs-lookup"><span data-stu-id="26486-124">A value that specifies the size of *pszPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26486-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26486-125">Return value</span></span>

<span data-ttu-id="26486-126">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="26486-126">Type: **HRESULT**</span></span>

<span data-ttu-id="26486-127">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="26486-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26486-128">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26486-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="26486-129">Требования</span><span class="sxs-lookup"><span data-stu-id="26486-129">Requirements</span></span>



| <span data-ttu-id="26486-130">Требование</span><span class="sxs-lookup"><span data-stu-id="26486-130">Requirement</span></span> | <span data-ttu-id="26486-131">Значение</span><span class="sxs-lookup"><span data-stu-id="26486-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26486-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26486-132">Minimum supported client</span></span><br/> | <span data-ttu-id="26486-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26486-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="26486-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26486-134">Minimum supported server</span></span><br/> | <span data-ttu-id="26486-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26486-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="26486-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="26486-136">End of client support</span></span><br/>    | <span data-ttu-id="26486-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="26486-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="26486-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="26486-138">End of server support</span></span><br/>    | <span data-ttu-id="26486-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="26486-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="26486-140">Header</span><span class="sxs-lookup"><span data-stu-id="26486-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="26486-141"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="26486-141"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="26486-142">IDL</span><span class="sxs-lookup"><span data-stu-id="26486-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26486-143"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26486-143"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="26486-144">DLL</span><span class="sxs-lookup"><span data-stu-id="26486-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26486-145"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26486-145"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26486-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26486-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26486-147">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="26486-147">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="26486-148">**Иусеридентити:: Опенидентитирегкэй**</span><span class="sxs-lookup"><span data-stu-id="26486-148">**IUserIdentity::OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




