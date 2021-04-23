---
description: Идентитинформатиончанжед не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'Метод Иидентитичанженотифи:: Идентитинформатиончанжед (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909520"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a><span data-ttu-id="8f7b2-104">Метод Иидентитичанженотифи:: Идентитинформатиончанжед</span><span class="sxs-lookup"><span data-stu-id="8f7b2-104">IIdentityChangeNotify::IdentityInformationChanged method</span></span>

<span data-ttu-id="8f7b2-105">\[**Идентитинформатиончанжед** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="8f7b2-105">\[**IdentityInformationChanged** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="8f7b2-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="8f7b2-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="8f7b2-107">Вызывается при изменении сведений об удостоверении пользователя или при добавлении или удалении удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f7b2-107">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f7b2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f7b2-108">Syntax</span></span>


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a><span data-ttu-id="8f7b2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f7b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f7b2-110">*двтипе*</span><span class="sxs-lookup"><span data-stu-id="8f7b2-110">*dwType*</span></span> 
</dt> <dd>

<span data-ttu-id="8f7b2-111">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f7b2-111">Type: **DWORD**</span></span>

<span data-ttu-id="8f7b2-112">Значение типа, указывающее тип измененной информации или операцию, выполненную с удостоверением.</span><span class="sxs-lookup"><span data-stu-id="8f7b2-112">A value that specifies the type of information changed, or the operation performed on an identity.</span></span> <span data-ttu-id="8f7b2-113">Может быть сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8f7b2-113">Can be a combination of the following values.</span></span>

<dt>



 <span data-ttu-id="8f7b2-114">(ИИК \_ ТЕКУЩЕЕ \_ удостоверение \_ изменено)</span><span class="sxs-lookup"><span data-stu-id="8f7b2-114">(IIC\_CURRENT\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="8f7b2-115">Текущее удостоверение было изменено.</span><span class="sxs-lookup"><span data-stu-id="8f7b2-115">The current identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="8f7b2-116">(ИИК \_ Идентификатор \_ изменен)</span><span class="sxs-lookup"><span data-stu-id="8f7b2-116">(IIC\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="8f7b2-117">Удостоверение было изменено.</span><span class="sxs-lookup"><span data-stu-id="8f7b2-117">An identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="8f7b2-118">(ИИК \_ УДОСТОВЕРЕНие \_ удалено)</span><span class="sxs-lookup"><span data-stu-id="8f7b2-118">(IIC\_IDENTITY\_DELETED)</span></span>


</dt> <dd>

<span data-ttu-id="8f7b2-119">Удостоверение удалено.</span><span class="sxs-lookup"><span data-stu-id="8f7b2-119">An identity has been deleted.</span></span>

</dd> <dt>



 <span data-ttu-id="8f7b2-120">(ИИК \_ УДОСТОВЕРЕНие \_ добавлено)</span><span class="sxs-lookup"><span data-stu-id="8f7b2-120">(IIC\_IDENTITY\_ADDED)</span></span>


</dt> <dd>

<span data-ttu-id="8f7b2-121">Добавлено новое удостоверение.</span><span class="sxs-lookup"><span data-stu-id="8f7b2-121">A new identity has been added.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f7b2-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f7b2-122">Return value</span></span>

<span data-ttu-id="8f7b2-123">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8f7b2-123">Type: **HRESULT**</span></span>

<span data-ttu-id="8f7b2-124">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8f7b2-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8f7b2-125">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f7b2-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f7b2-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="8f7b2-126">Remarks</span></span>

<span data-ttu-id="8f7b2-127">Этот метод можно реализовать, чтобы обеспечить пользовательское поведение приложения при изменении списка удостоверений пользователей в системе.</span><span class="sxs-lookup"><span data-stu-id="8f7b2-127">You may implement this method to provide custom behavior for your application when the list of user identities on the system has been modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f7b2-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8f7b2-128">Requirements</span></span>



| <span data-ttu-id="8f7b2-129">Требование</span><span class="sxs-lookup"><span data-stu-id="8f7b2-129">Requirement</span></span> | <span data-ttu-id="8f7b2-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8f7b2-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f7b2-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f7b2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8f7b2-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8f7b2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8f7b2-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f7b2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8f7b2-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8f7b2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8f7b2-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8f7b2-135">End of client support</span></span><br/>    | <span data-ttu-id="8f7b2-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8f7b2-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="8f7b2-137">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8f7b2-137">End of server support</span></span><br/>    | <span data-ttu-id="8f7b2-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f7b2-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="8f7b2-139">Header</span><span class="sxs-lookup"><span data-stu-id="8f7b2-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f7b2-140"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f7b2-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f7b2-141">IDL</span><span class="sxs-lookup"><span data-stu-id="8f7b2-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8f7b2-142"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8f7b2-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="8f7b2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="8f7b2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f7b2-144"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f7b2-144"><dt>Msoe.dll</dt></span></span> </dl>    |



 

 




