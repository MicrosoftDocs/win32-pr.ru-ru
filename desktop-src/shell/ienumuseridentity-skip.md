---
description: 'Иенумусеридентити:: Skip не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: 'Метод Иенумусеридентити:: Skip (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: cedd4f3c6e9736e26cbf8d58f27f805f0f5d33a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997667"
---
# <a name="ienumuseridentityskip-method"></a><span data-ttu-id="68bd3-104">Метод Иенумусеридентити:: Skip</span><span class="sxs-lookup"><span data-stu-id="68bd3-104">IEnumUserIdentity::Skip method</span></span>

<span data-ttu-id="68bd3-105">\[**Иенумусеридентити:: Skip** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="68bd3-105">\[**IEnumUserIdentity::Skip** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="68bd3-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="68bd3-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="68bd3-107">Пропускает заданное число интерфейсов удостоверения пользователя в перечислении.</span><span class="sxs-lookup"><span data-stu-id="68bd3-107">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="68bd3-108">Используется при извлечении интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="68bd3-108">Used when retrieving interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="68bd3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68bd3-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="68bd3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="68bd3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68bd3-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68bd3-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68bd3-112">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="68bd3-112">Type: **ULONG**</span></span>

<span data-ttu-id="68bd3-113">Число интерфейсов, которые нужно пропустить.</span><span class="sxs-lookup"><span data-stu-id="68bd3-113">The number of interfaces to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68bd3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68bd3-114">Return value</span></span>

<span data-ttu-id="68bd3-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="68bd3-115">Type: **HRESULT**</span></span>

<span data-ttu-id="68bd3-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="68bd3-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68bd3-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68bd3-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="68bd3-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="68bd3-118">Remarks</span></span>

<span data-ttu-id="68bd3-119">[**Иенумусеридентити**](ienumuseridentity.md) хранит внутренний счетчик, указывающий, какой интерфейс следует извлечь.</span><span class="sxs-lookup"><span data-stu-id="68bd3-119">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="68bd3-120">Чтобы увеличить это число без извлечения интерфейсов, вызовите этот метод.</span><span class="sxs-lookup"><span data-stu-id="68bd3-120">To increment this count without retrieving interfaces, call this method.</span></span> <span data-ttu-id="68bd3-121">Чтобы сбросить счетчик, вызовите метод [**иенумусеридентити:: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="68bd3-121">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68bd3-122">Требования</span><span class="sxs-lookup"><span data-stu-id="68bd3-122">Requirements</span></span>



| <span data-ttu-id="68bd3-123">Требование</span><span class="sxs-lookup"><span data-stu-id="68bd3-123">Requirement</span></span> | <span data-ttu-id="68bd3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="68bd3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68bd3-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68bd3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="68bd3-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="68bd3-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="68bd3-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68bd3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="68bd3-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="68bd3-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="68bd3-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="68bd3-129">End of client support</span></span><br/>    | <span data-ttu-id="68bd3-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="68bd3-130">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="68bd3-131">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="68bd3-131">End of server support</span></span><br/>    | <span data-ttu-id="68bd3-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="68bd3-132">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="68bd3-133">Header</span><span class="sxs-lookup"><span data-stu-id="68bd3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="68bd3-134"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="68bd3-134"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="68bd3-135">IDL</span><span class="sxs-lookup"><span data-stu-id="68bd3-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68bd3-136"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68bd3-136"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="68bd3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="68bd3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68bd3-138"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68bd3-138"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68bd3-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68bd3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68bd3-140">**иенумусеридентити**</span><span class="sxs-lookup"><span data-stu-id="68bd3-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="68bd3-141">**Иенумусеридентити:: Reset**</span><span class="sxs-lookup"><span data-stu-id="68bd3-141">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="68bd3-142">**Иенумусеридентити:: Next**</span><span class="sxs-lookup"><span data-stu-id="68bd3-142">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> <dt>

[<span data-ttu-id="68bd3-143">**Иенумусеридентити:: NOCOUNT**</span><span class="sxs-lookup"><span data-stu-id="68bd3-143">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 




