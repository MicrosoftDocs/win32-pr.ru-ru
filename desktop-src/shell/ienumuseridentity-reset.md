---
description: Сбрасывает внутреннее число извлеченных интерфейсов в перечислении.
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: 'Метод Иенумусеридентити:: Reset (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 05b3c5d38575fa1b2957c28070d642ad15f846ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264413"
---
# <a name="ienumuseridentityreset-method"></a><span data-ttu-id="41845-103">Метод Иенумусеридентити:: Reset</span><span class="sxs-lookup"><span data-stu-id="41845-103">IEnumUserIdentity::Reset method</span></span>

<span data-ttu-id="41845-104">\[**Иенумусеридентити:: Reset** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="41845-104">\[**IEnumUserIdentity::Reset** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="41845-105">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="41845-105">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="41845-106">Сбрасывает внутреннее число извлеченных интерфейсов в перечислении.</span><span class="sxs-lookup"><span data-stu-id="41845-106">Resets the internal count of retrieved interfaces in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="41845-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41845-107">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="41845-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="41845-108">Parameters</span></span>

<span data-ttu-id="41845-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="41845-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41845-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41845-110">Return value</span></span>

<span data-ttu-id="41845-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="41845-111">Type: **HRESULT**</span></span>

<span data-ttu-id="41845-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="41845-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41845-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41845-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="41845-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="41845-114">Remarks</span></span>

<span data-ttu-id="41845-115">[**Иенумусеридентити**](ienumuseridentity.md) хранит внутренний счетчик, указывающий, какой интерфейс следует извлечь.</span><span class="sxs-lookup"><span data-stu-id="41845-115">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="41845-116">Вызов этого метода приведет к сбросу значения этого счетчика.</span><span class="sxs-lookup"><span data-stu-id="41845-116">Calling this method will reset the value of this count.</span></span>

## <a name="requirements"></a><span data-ttu-id="41845-117">Требования</span><span class="sxs-lookup"><span data-stu-id="41845-117">Requirements</span></span>



| <span data-ttu-id="41845-118">Требование</span><span class="sxs-lookup"><span data-stu-id="41845-118">Requirement</span></span> | <span data-ttu-id="41845-119">Значение</span><span class="sxs-lookup"><span data-stu-id="41845-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41845-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41845-120">Minimum supported client</span></span><br/> | <span data-ttu-id="41845-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="41845-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="41845-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41845-122">Minimum supported server</span></span><br/> | <span data-ttu-id="41845-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41845-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="41845-124">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="41845-124">End of client support</span></span><br/>    | <span data-ttu-id="41845-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="41845-125">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="41845-126">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="41845-126">End of server support</span></span><br/>    | <span data-ttu-id="41845-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="41845-127">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="41845-128">Header</span><span class="sxs-lookup"><span data-stu-id="41845-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="41845-129"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="41845-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="41845-130">IDL</span><span class="sxs-lookup"><span data-stu-id="41845-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41845-131"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41845-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="41845-132">DLL</span><span class="sxs-lookup"><span data-stu-id="41845-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41845-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41845-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41845-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41845-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41845-135">**иенумусеридентити**</span><span class="sxs-lookup"><span data-stu-id="41845-135">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="41845-136">**Иенумусеридентити:: Skip**</span><span class="sxs-lookup"><span data-stu-id="41845-136">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="41845-137">**Иенумусеридентити:: NOCOUNT**</span><span class="sxs-lookup"><span data-stu-id="41845-137">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> <dt>

[<span data-ttu-id="41845-138">**Иенумусеридентити:: Next**</span><span class="sxs-lookup"><span data-stu-id="41845-138">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




