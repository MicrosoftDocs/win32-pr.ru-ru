---
description: Функция NOCOUNT не поддерживается и может быть изменена или недоступна в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: 'Метод Иенумусеридентити:: NOCOUNT (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 43355a9585fc4099c8649f7df506ff3495a53944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345385"
---
# <a name="ienumuseridentitygetcount-method"></a><span data-ttu-id="bca08-104">Метод Иенумусеридентити:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="bca08-104">IEnumUserIdentity::GetCount method</span></span>

<span data-ttu-id="bca08-105">\[Функция **NOCOUNT** не поддерживается и может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="bca08-105">\[**GetCount** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bca08-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="bca08-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="bca08-107">Возвращает число удостоверений пользователей, находящихся в системе в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="bca08-107">Gets the count of user identities currently on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="bca08-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bca08-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a><span data-ttu-id="bca08-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bca08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bca08-110">*пнкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bca08-110">*pnCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bca08-111">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="bca08-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="bca08-112">Указатель на _ \*ulong\*\*, получающий счетчик.</span><span class="sxs-lookup"><span data-stu-id="bca08-112">Pointer to a _ *ULONG*\* that receives the count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bca08-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bca08-113">Return value</span></span>

<span data-ttu-id="bca08-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bca08-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bca08-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="bca08-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bca08-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bca08-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bca08-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="bca08-117">Remarks</span></span>

<span data-ttu-id="bca08-118">Если поддержка нескольких удостоверений пользователей отключена, *пнкаунт* получит значение 1.</span><span class="sxs-lookup"><span data-stu-id="bca08-118">If support for multiple user identities is disabled, *pnCount* will receive a value of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="bca08-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bca08-119">Requirements</span></span>



| <span data-ttu-id="bca08-120">Требование</span><span class="sxs-lookup"><span data-stu-id="bca08-120">Requirement</span></span> | <span data-ttu-id="bca08-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bca08-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bca08-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bca08-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bca08-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bca08-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bca08-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bca08-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bca08-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bca08-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bca08-126">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="bca08-126">End of client support</span></span><br/>    | <span data-ttu-id="bca08-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bca08-127">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="bca08-128">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="bca08-128">End of server support</span></span><br/>    | <span data-ttu-id="bca08-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bca08-129">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="bca08-130">Header</span><span class="sxs-lookup"><span data-stu-id="bca08-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bca08-131"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="bca08-131"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="bca08-132">IDL</span><span class="sxs-lookup"><span data-stu-id="bca08-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bca08-133"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bca08-133"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="bca08-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bca08-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bca08-135"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bca08-135"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bca08-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bca08-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bca08-137">**иенумусеридентити**</span><span class="sxs-lookup"><span data-stu-id="bca08-137">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="bca08-138">**Иенумусеридентити:: Skip**</span><span class="sxs-lookup"><span data-stu-id="bca08-138">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="bca08-139">**Иенумусеридентити:: Reset**</span><span class="sxs-lookup"><span data-stu-id="bca08-139">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="bca08-140">**Иенумусеридентити:: Next**</span><span class="sxs-lookup"><span data-stu-id="bca08-140">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




