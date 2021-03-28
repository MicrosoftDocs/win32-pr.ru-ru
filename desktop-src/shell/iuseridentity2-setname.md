---
description: 'IUserIdentity2:: SetName не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: 1c9c3beb-fa1c-4b4d-9cfd-656b97949036
title: 'Метод IUserIdentity2:: SetName (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.SetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 0b0fd06ef4b582987e41c2343f2d4596db6b8528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985680"
---
# <a name="iuseridentity2setname-method"></a><span data-ttu-id="13388-104">Метод IUserIdentity2:: SetName</span><span class="sxs-lookup"><span data-stu-id="13388-104">IUserIdentity2::SetName method</span></span>

<span data-ttu-id="13388-105">\[**IUserIdentity2:: SetName** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="13388-105">\[**IUserIdentity2::SetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="13388-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="13388-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="13388-107">Задает отображаемое имя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="13388-107">Sets the display name of the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="13388-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13388-108">Syntax</span></span>


```C++
HRESULT SetName(
  [in] WCHAR *pszName
);
```



## <a name="parameters"></a><span data-ttu-id="13388-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="13388-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13388-110">*pszName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13388-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13388-111">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="13388-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="13388-112">Строка расширенных символов, содержащая новое имя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="13388-112">The wide-character string that contains the new name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13388-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13388-113">Return value</span></span>

<span data-ttu-id="13388-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="13388-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="13388-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="13388-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13388-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="13388-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="13388-117">Требования</span><span class="sxs-lookup"><span data-stu-id="13388-117">Requirements</span></span>



| <span data-ttu-id="13388-118">Требование</span><span class="sxs-lookup"><span data-stu-id="13388-118">Requirement</span></span> | <span data-ttu-id="13388-119">Значение</span><span class="sxs-lookup"><span data-stu-id="13388-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13388-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13388-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13388-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="13388-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="13388-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13388-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13388-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="13388-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13388-124">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="13388-124">End of client support</span></span><br/>    | <span data-ttu-id="13388-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="13388-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="13388-126">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="13388-126">End of server support</span></span><br/>    | <span data-ttu-id="13388-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13388-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="13388-128">Header</span><span class="sxs-lookup"><span data-stu-id="13388-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="13388-129"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="13388-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="13388-130">IDL</span><span class="sxs-lookup"><span data-stu-id="13388-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13388-131"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13388-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="13388-132">DLL</span><span class="sxs-lookup"><span data-stu-id="13388-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13388-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13388-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13388-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13388-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13388-135">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="13388-135">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="13388-136">**GetName**</span><span class="sxs-lookup"><span data-stu-id="13388-136">**GetName**</span></span>](iuseridentity-getname.md)
</dt> </dl>

 

 




