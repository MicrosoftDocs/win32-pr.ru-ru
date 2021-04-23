---
description: 'Иенумусеридентити:: Next не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'Метод Иенумусеридентити:: Next (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 763b2b4a612596c5f02a9826ad2e9c09ab8e4b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997671"
---
# <a name="ienumuseridentitynext-method"></a><span data-ttu-id="b4579-104">Метод Иенумусеридентити:: Next</span><span class="sxs-lookup"><span data-stu-id="b4579-104">IEnumUserIdentity::Next method</span></span>

<span data-ttu-id="b4579-105">\[**Иенумусеридентити:: Next** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="b4579-105">\[**IEnumUserIdentity::Next** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="b4579-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="b4579-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="b4579-107">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b4579-107">Deprecated.</span></span> <span data-ttu-id="b4579-108">Извлекает из перечисления массив интерфейсов удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b4579-108">Retrieves an array of user identity interfaces from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4579-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4579-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="b4579-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4579-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4579-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4579-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4579-112">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="b4579-112">Type: **ULONG**</span></span>

<span data-ttu-id="b4579-113">Значение типа **ulong** , представляющее число получаемых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="b4579-113">A **ULONG** value that represents the number of interfaces to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b4579-114">*rgelt* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4579-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4579-115">Тип: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="b4579-115">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="b4579-116">Адрес указателя, получающего интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="b4579-116">The address of a pointer that receives the interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="b4579-117">*пцелтфетчед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4579-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4579-118">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="b4579-118">Type: \**ULONG\** _</span></span>

<span data-ttu-id="b4579-119">Адрес указателя, который получает число успешно извлеченных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="b4579-119">The address of a pointer that receives the number of interfaces successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4579-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4579-120">Return value</span></span>

<span data-ttu-id="b4579-121">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b4579-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b4579-122">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b4579-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b4579-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4579-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4579-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4579-124">Remarks</span></span>

<span data-ttu-id="b4579-125">[**Иенумусеридентити**](ienumuseridentity.md) хранит внутренний счетчик, указывающий, какой интерфейс следует извлечь.</span><span class="sxs-lookup"><span data-stu-id="b4579-125">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="b4579-126">Несколько вызовов этого метода не будут сбрасывать это число.</span><span class="sxs-lookup"><span data-stu-id="b4579-126">Multiple calls to this method will not reset this count.</span></span> <span data-ttu-id="b4579-127">Чтобы сбросить счетчик, вызовите метод [**иенумусеридентити:: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="b4579-127">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span> <span data-ttu-id="b4579-128">Чтобы увеличить число без извлечения интерфейсов, вызовите [**иенумусеридентити:: Skip**](ienumuseridentity-skip.md).</span><span class="sxs-lookup"><span data-stu-id="b4579-128">To increment the count without retrieving interfaces, call [**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md).</span></span>

<span data-ttu-id="b4579-129">Значение параметра *celt* не должно превышать значение, возвращенное [**Иенумусеридентити:: NOCOUNT**](ienumuseridentity-getcount.md).</span><span class="sxs-lookup"><span data-stu-id="b4579-129">The value of *celt* should not exceed the value returned by [**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4579-130">Требования</span><span class="sxs-lookup"><span data-stu-id="b4579-130">Requirements</span></span>



| <span data-ttu-id="b4579-131">Требование</span><span class="sxs-lookup"><span data-stu-id="b4579-131">Requirement</span></span> | <span data-ttu-id="b4579-132">Значение</span><span class="sxs-lookup"><span data-stu-id="b4579-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4579-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4579-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b4579-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b4579-134">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b4579-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4579-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b4579-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4579-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b4579-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b4579-137">End of client support</span></span><br/>    | <span data-ttu-id="b4579-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4579-138">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="b4579-139">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="b4579-139">End of server support</span></span><br/>    | <span data-ttu-id="b4579-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4579-140">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="b4579-141">Header</span><span class="sxs-lookup"><span data-stu-id="b4579-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4579-142"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4579-142"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4579-143">IDL</span><span class="sxs-lookup"><span data-stu-id="b4579-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4579-144"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4579-144"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="b4579-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b4579-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4579-146"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4579-146"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4579-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4579-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4579-148">**иенумусеридентити**</span><span class="sxs-lookup"><span data-stu-id="b4579-148">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="b4579-149">**Иенумусеридентити:: Skip**</span><span class="sxs-lookup"><span data-stu-id="b4579-149">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="b4579-150">**Иенумусеридентити:: Reset**</span><span class="sxs-lookup"><span data-stu-id="b4579-150">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="b4579-151">**Иенумусеридентити:: NOCOUNT**</span><span class="sxs-lookup"><span data-stu-id="b4579-151">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
