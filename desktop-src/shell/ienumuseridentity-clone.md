---
description: 'Иенумусеридентити:: Clone не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: 'Метод Иенумусеридентити:: Clone (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: ebdec426fe7ab591c801c00b637211e903cf5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997674"
---
# <a name="ienumuseridentityclone-method"></a><span data-ttu-id="8216e-104">Метод Иенумусеридентити:: Clone</span><span class="sxs-lookup"><span data-stu-id="8216e-104">IEnumUserIdentity::Clone method</span></span>

<span data-ttu-id="8216e-105">\[**Иенумусеридентити:: Clone** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="8216e-105">\[**IEnumUserIdentity::Clone** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="8216e-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="8216e-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="8216e-107">Возвращает копию текущего перечисления.</span><span class="sxs-lookup"><span data-stu-id="8216e-107">Gets a copy of the current enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8216e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8216e-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="8216e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8216e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8216e-110">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8216e-110">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8216e-111">Тип: **[ **иенумусеридентити**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8216e-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="8216e-112">Адрес указателя, получающего копию этого перечисления.</span><span class="sxs-lookup"><span data-stu-id="8216e-112">The address of a pointer that receives a copy of this enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8216e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8216e-113">Return value</span></span>

<span data-ttu-id="8216e-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8216e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8216e-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8216e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8216e-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8216e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8216e-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="8216e-117">Remarks</span></span>

<span data-ttu-id="8216e-118">[**Иенумусеридентити**](ienumuseridentity.md) хранит внутренний счетчик, указывающий, какой интерфейс следует извлечь.</span><span class="sxs-lookup"><span data-stu-id="8216e-118">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="8216e-119">Значение этого счетчика будет применено к интерфейсу, полученному с помощью *ппенум*.</span><span class="sxs-lookup"><span data-stu-id="8216e-119">The value of this count will be applied to the interface received by *ppenum*.</span></span> <span data-ttu-id="8216e-120">Чтобы сбросить счетчик, вызовите метод [**иенумусеридентити:: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="8216e-120">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8216e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8216e-121">Requirements</span></span>



| <span data-ttu-id="8216e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8216e-122">Requirement</span></span> | <span data-ttu-id="8216e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8216e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8216e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8216e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8216e-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8216e-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8216e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8216e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8216e-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8216e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8216e-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8216e-128">End of client support</span></span><br/>    | <span data-ttu-id="8216e-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8216e-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="8216e-130">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8216e-130">End of server support</span></span><br/>    | <span data-ttu-id="8216e-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8216e-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="8216e-132">Header</span><span class="sxs-lookup"><span data-stu-id="8216e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8216e-133"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="8216e-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="8216e-134">IDL</span><span class="sxs-lookup"><span data-stu-id="8216e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8216e-135"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8216e-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="8216e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8216e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8216e-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8216e-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8216e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8216e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8216e-139">**иенумусеридентити**</span><span class="sxs-lookup"><span data-stu-id="8216e-139">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="8216e-140">**Иенумусеридентити:: Reset**</span><span class="sxs-lookup"><span data-stu-id="8216e-140">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> </dl>

 

 




