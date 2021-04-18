---
description: Параметр ordinal не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: 'Метод IUserIdentity2:: метода ordinal (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f5a7e875e92342363722858b3ac714171cb547b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985684"
---
# <a name="iuseridentity2getordinal-method"></a><span data-ttu-id="dfb0e-104">Метод IUserIdentity2:: метода Ordinal</span><span class="sxs-lookup"><span data-stu-id="dfb0e-104">IUserIdentity2::GetOrdinal method</span></span>

<span data-ttu-id="dfb0e-105">\[Параметр **Ordinal** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="dfb0e-105">\[**GetOrdinal** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="dfb0e-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="dfb0e-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="dfb0e-107">Возвращает порядковый номер этого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="dfb0e-107">Gets the ordinal number for this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb0e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfb0e-108">Syntax</span></span>


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a><span data-ttu-id="dfb0e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfb0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfb0e-110">*двординал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfb0e-110">*dwOrdinal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb0e-111">Введите: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="dfb0e-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="dfb0e-112">Указатель на значение _ \*DWORD\*\*, которое получает порядковый номер для этого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="dfb0e-112">A pointer to a _ *DWORD*\* value that receives the ordinal number for this identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfb0e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfb0e-113">Return value</span></span>

<span data-ttu-id="dfb0e-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dfb0e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="dfb0e-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="dfb0e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dfb0e-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dfb0e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfb0e-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="dfb0e-117">Remarks</span></span>

<span data-ttu-id="dfb0e-118">Порядковый номер определяет порядок удостоверений в списке удостоверений, но может не сохраняться во всех операциях с удостоверениями.</span><span class="sxs-lookup"><span data-stu-id="dfb0e-118">The ordinal determines the order of the identities in the identity list, but may not persist throughout operations on the identities.</span></span> <span data-ttu-id="dfb0e-119">Чтобы получить уникальное значение для удостоверения, вызовите метод [**Кука**](iuseridentity-getcookie.md).</span><span class="sxs-lookup"><span data-stu-id="dfb0e-119">To get a unique value for an identity, call [**GetCookie**](iuseridentity-getcookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb0e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="dfb0e-120">Requirements</span></span>



| <span data-ttu-id="dfb0e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="dfb0e-121">Requirement</span></span> | <span data-ttu-id="dfb0e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="dfb0e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb0e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfb0e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb0e-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dfb0e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dfb0e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfb0e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb0e-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dfb0e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dfb0e-127">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dfb0e-127">End of client support</span></span><br/>    | <span data-ttu-id="dfb0e-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dfb0e-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="dfb0e-129">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="dfb0e-129">End of server support</span></span><br/>    | <span data-ttu-id="dfb0e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dfb0e-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="dfb0e-131">Header</span><span class="sxs-lookup"><span data-stu-id="dfb0e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfb0e-132"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb0e-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfb0e-133">IDL</span><span class="sxs-lookup"><span data-stu-id="dfb0e-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dfb0e-134"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dfb0e-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="dfb0e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="dfb0e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfb0e-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfb0e-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb0e-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfb0e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb0e-138">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="dfb0e-138">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="dfb0e-139">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="dfb0e-139">**GetCookie**</span></span>](iuseridentity-getcookie.md)
</dt> </dl>

 

 




