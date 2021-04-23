---
description: Не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: 4a743d64-9af3-43cf-9a9f-d808676ab337
title: 'Метод Иусеридентити:: (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 96cafb13f2c90c41e4aa6dcaaa72cf052757d0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984617"
---
# <a name="iuseridentitygetcookie-method"></a><span data-ttu-id="c08b3-104">Метод Иусеридентити:: Кука</span><span class="sxs-lookup"><span data-stu-id="c08b3-104">IUserIdentity::GetCookie method</span></span>

<span data-ttu-id="c08b3-105">\[**Не поддерживается** и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="c08b3-105">\[**GetCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="c08b3-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="c08b3-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="c08b3-107">Возвращает файл cookie, используемый для уникальной идентификации этого удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c08b3-107">Gets the cookie used to uniquely identify this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="c08b3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c08b3-108">Syntax</span></span>


```C++
HRESULT GetCookie(
  [out] GUID *puidCookie
);
```



## <a name="parameters"></a><span data-ttu-id="c08b3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c08b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c08b3-110">*пуидкукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c08b3-110">*puidCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c08b3-111">Тип: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="c08b3-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="c08b3-112">Указатель на значение _ \*GUID\*\*, которое получает файл cookie, используемый для уникальной идентификации этого удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c08b3-112">A pointer to a _ *GUID*\* value that receives the cookie used to uniquely identify this user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c08b3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c08b3-113">Return value</span></span>

<span data-ttu-id="c08b3-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c08b3-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c08b3-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c08b3-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c08b3-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c08b3-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c08b3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c08b3-117">Requirements</span></span>



| <span data-ttu-id="c08b3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c08b3-118">Requirement</span></span> | <span data-ttu-id="c08b3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c08b3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c08b3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c08b3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c08b3-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c08b3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c08b3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c08b3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c08b3-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c08b3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c08b3-124">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c08b3-124">End of client support</span></span><br/>    | <span data-ttu-id="c08b3-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c08b3-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="c08b3-126">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c08b3-126">End of server support</span></span><br/>    | <span data-ttu-id="c08b3-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c08b3-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="c08b3-128">Header</span><span class="sxs-lookup"><span data-stu-id="c08b3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c08b3-129"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="c08b3-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="c08b3-130">IDL</span><span class="sxs-lookup"><span data-stu-id="c08b3-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c08b3-131"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c08b3-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="c08b3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c08b3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c08b3-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c08b3-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c08b3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c08b3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c08b3-135">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="c08b3-135">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="c08b3-136">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="c08b3-136">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)
</dt> </dl>

 

 




