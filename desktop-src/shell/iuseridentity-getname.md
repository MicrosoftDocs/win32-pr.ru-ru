---
description: 'Иусеридентити:: Name не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: 4db24dd2-d2b8-4a58-9c16-0e721bc195da
title: Метод Иусеридентити::-Name (Мсидент. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88c0a3d08ff917c2cc9fd59f15e4c23fc22fc79d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985404"
---
# <a name="iuseridentitygetname-method"></a><span data-ttu-id="d10db-104">Метод Иусеридентити:: Name</span><span class="sxs-lookup"><span data-stu-id="d10db-104">IUserIdentity::GetName method</span></span>

<span data-ttu-id="d10db-105">\[**Иусеридентити:: Name** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="d10db-105">\[**IUserIdentity::GetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="d10db-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="d10db-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="d10db-107">Возвращает имя, связанное с этим удостоверением пользователя.</span><span class="sxs-lookup"><span data-stu-id="d10db-107">Gets the name associated with this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="d10db-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d10db-108">Syntax</span></span>


```C++
HRESULT GetName(
  [in] WCHAR *pszName,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="d10db-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d10db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d10db-110">*pszName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d10db-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d10db-111">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="d10db-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="d10db-112">Указатель на строку расширенных символов, которая получает имя этого удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d10db-112">A pointer to a wide-character string that receives the name of this user identity.</span></span>

</dd> <dt>

<span data-ttu-id="d10db-113">_ulBuffSize \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d10db-113">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d10db-114">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="d10db-114">Type: **ULONG**</span></span>

<span data-ttu-id="d10db-115">Значение типа, указывающее размер *pszName*.</span><span class="sxs-lookup"><span data-stu-id="d10db-115">A value that specifies the size of *pszName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d10db-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d10db-116">Return value</span></span>

<span data-ttu-id="d10db-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d10db-117">Type: **HRESULT**</span></span>

<span data-ttu-id="d10db-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d10db-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d10db-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d10db-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10db-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d10db-120">Requirements</span></span>



| <span data-ttu-id="d10db-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d10db-121">Requirement</span></span> | <span data-ttu-id="d10db-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d10db-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d10db-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d10db-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d10db-124">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d10db-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d10db-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d10db-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d10db-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d10db-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d10db-127">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d10db-127">End of client support</span></span><br/>    | <span data-ttu-id="d10db-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d10db-128">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="d10db-129">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d10db-129">End of server support</span></span><br/>    | <span data-ttu-id="d10db-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d10db-130">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="d10db-131">Header</span><span class="sxs-lookup"><span data-stu-id="d10db-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d10db-132"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="d10db-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="d10db-133">IDL</span><span class="sxs-lookup"><span data-stu-id="d10db-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d10db-134"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d10db-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="d10db-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d10db-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d10db-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d10db-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d10db-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d10db-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10db-138">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="d10db-138">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="d10db-139">**SetName**</span><span class="sxs-lookup"><span data-stu-id="d10db-139">**SetName**</span></span>](iuseridentity2-setname.md)
</dt> </dl>

 

 




