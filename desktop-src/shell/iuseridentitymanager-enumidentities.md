---
description: 'Иусеридентитиманажер:: Енумидентитиес не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'Метод Иусеридентитиманажер:: Енумидентитиес (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143027"
---
# <a name="iuseridentitymanagerenumidentities-method"></a><span data-ttu-id="8620c-104">Метод Иусеридентитиманажер:: Енумидентитиес</span><span class="sxs-lookup"><span data-stu-id="8620c-104">IUserIdentityManager::EnumIdentities method</span></span>

<span data-ttu-id="8620c-105">\[**Иусеридентитиманажер:: енумидентитиес** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="8620c-105">\[**IUserIdentityManager::EnumIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="8620c-106">Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="8620c-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="8620c-107">Возвращает объект [**иенумусеридентити**](ienumuseridentity.md) , который можно использовать для перечисления удостоверений пользователей, имеющихся в системе.</span><span class="sxs-lookup"><span data-stu-id="8620c-107">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8620c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8620c-108">Syntax</span></span>


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a><span data-ttu-id="8620c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8620c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8620c-110">*ппенумусер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8620c-110">*ppEnumUser* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8620c-111">Тип: **[ **иенумусеридентити**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8620c-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="8620c-112">Адрес указателя на новый объект перечисления идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="8620c-112">The address of the pointer to the new identity enumeration object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8620c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8620c-113">Return value</span></span>

<span data-ttu-id="8620c-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8620c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8620c-115">Результат операции извлечения.</span><span class="sxs-lookup"><span data-stu-id="8620c-115">The result of the retrieval operation.</span></span> <span data-ttu-id="8620c-116">В случае успеха возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8620c-116">If successful, it returns S\_OK.</span></span> <span data-ttu-id="8620c-117">Если не удалось создать объект перечисления, он возвращает E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8620c-117">If the enumeration object could not be created, it returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8620c-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="8620c-118">Remarks</span></span>

<span data-ttu-id="8620c-119">Этот метод полезен для итерации по списку удостоверений в системе.</span><span class="sxs-lookup"><span data-stu-id="8620c-119">This method is useful for iteration over the list of identities on the system.</span></span> <span data-ttu-id="8620c-120">Чтобы получить одиночное удостоверение с помощью файла cookie, не обращаясь к списку, вызовите [**иусеридентитиманажер:: жетидентитибикукие**](iuseridentitymanager-getidentitybycookie.md).</span><span class="sxs-lookup"><span data-stu-id="8620c-120">To retrieve a single identity by its cookie without accessing the list, call [**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8620c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8620c-121">Requirements</span></span>



| <span data-ttu-id="8620c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8620c-122">Requirement</span></span> | <span data-ttu-id="8620c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8620c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8620c-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8620c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8620c-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8620c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8620c-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8620c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8620c-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8620c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8620c-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8620c-128">End of client support</span></span><br/>    | <span data-ttu-id="8620c-129">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8620c-129">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="8620c-130">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8620c-130">End of server support</span></span><br/>    | <span data-ttu-id="8620c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8620c-131">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="8620c-132">Header</span><span class="sxs-lookup"><span data-stu-id="8620c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8620c-133"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="8620c-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="8620c-134">IDL</span><span class="sxs-lookup"><span data-stu-id="8620c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8620c-135"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8620c-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="8620c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8620c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8620c-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8620c-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8620c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8620c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8620c-139">**иусеридентитиманажер**</span><span class="sxs-lookup"><span data-stu-id="8620c-139">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="8620c-140">**иенумусеридентити**</span><span class="sxs-lookup"><span data-stu-id="8620c-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="8620c-141">**Иусеридентитиманажер:: Жетидентитибикукие**</span><span class="sxs-lookup"><span data-stu-id="8620c-141">**IUserIdentityManager::GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




