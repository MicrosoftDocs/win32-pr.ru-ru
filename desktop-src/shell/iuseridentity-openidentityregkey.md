---
description: Не рекомендуется. Извлекает ключ в реестре, соответствующий этому удостоверению пользователя.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'Метод Иусеридентити:: Опенидентитирегкэй (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984608"
---
# <a name="iuseridentityopenidentityregkey-method"></a><span data-ttu-id="216fe-104">Метод Иусеридентити:: Опенидентитирегкэй</span><span class="sxs-lookup"><span data-stu-id="216fe-104">IUserIdentity::OpenIdentityRegKey method</span></span>

<span data-ttu-id="216fe-105">\[Метод **иусеридентити:: опенидентитирегкэй** можно использовать в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="216fe-105">\[The **IUserIdentity::OpenIdentityRegKey** method is available for use in Windows 2000.</span></span> <span data-ttu-id="216fe-106">В Windows XP эта функция заменена [учетными записями пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md)и может быть изменена или недоступна в последующих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="216fe-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="216fe-107">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="216fe-107">Deprecated.</span></span> <span data-ttu-id="216fe-108">Извлекает ключ в реестре, соответствующий этому удостоверению пользователя.</span><span class="sxs-lookup"><span data-stu-id="216fe-108">Retrieves the key in the registry that corresponds to this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="216fe-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="216fe-109">Syntax</span></span>


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a><span data-ttu-id="216fe-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="216fe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="216fe-111">*двдесиредакцесс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="216fe-111">*dwDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216fe-112">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="216fe-112">Type: **DWORD**</span></span>

<span data-ttu-id="216fe-113">Значение, описывающее уровень доступа, запрошенный для раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="216fe-113">A value that describes the access level requested of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="216fe-114">*фкэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="216fe-114">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="216fe-115">Тип: \**hKey \** _</span><span class="sxs-lookup"><span data-stu-id="216fe-115">Type: \**HKEY\** _</span></span>

<span data-ttu-id="216fe-116">Указатель, получающий раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="216fe-116">A pointer that receives the registry key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="216fe-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="216fe-117">Return value</span></span>

<span data-ttu-id="216fe-118">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="216fe-118">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="216fe-119">Результат запроса реестра.</span><span class="sxs-lookup"><span data-stu-id="216fe-119">The result of the registry request.</span></span> <span data-ttu-id="216fe-120">В случае успеха возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="216fe-120">If successful, it returns **S\_OK**.</span></span> <span data-ttu-id="216fe-121">В противном случае будет возвращен один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="216fe-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="216fe-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="216fe-122">Return code</span></span>                                                                                            | <span data-ttu-id="216fe-123">Описание</span><span class="sxs-lookup"><span data-stu-id="216fe-123">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="216fe-124"><dt>**\_ \_ не найдено удостоверение E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="216fe-124"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="216fe-125">С этим удостоверением не связан раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="216fe-125">This identity does not have an associated registry key.</span></span><br/> |
| <dl> <span data-ttu-id="216fe-126"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="216fe-126"><dt>**E\_FAIL**</dt></span></span> </dl>                 | <span data-ttu-id="216fe-127">Не удалось получить доступ к разделу реестра.</span><span class="sxs-lookup"><span data-stu-id="216fe-127">The registry key was unable to be accessed.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="216fe-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="216fe-128">Remarks</span></span>

<span data-ttu-id="216fe-129">Параметр *двдесиредакцесс* — это стандартный дескриптор безопасности доступа к реестру, описывающий доступ к разделу реестра.</span><span class="sxs-lookup"><span data-stu-id="216fe-129">The *dwDesiredAccess* parameter is a standard registry access security descriptor that describes the access you want to gain to the registry key.</span></span> <span data-ttu-id="216fe-130">Дополнительные сведения о безопасности реестра, включая список допустимых значений для этого параметра, см. в разделе [раздел реестра Security and Access Rights](../sysinfo/registry-key-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="216fe-130">For more information on registry security, including a list of acceptable values for this parameter, see [Registry Key Security and Access Rights](../sysinfo/registry-key-security-and-access-rights.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="216fe-131">Требования</span><span class="sxs-lookup"><span data-stu-id="216fe-131">Requirements</span></span>



| <span data-ttu-id="216fe-132">Требование</span><span class="sxs-lookup"><span data-stu-id="216fe-132">Requirement</span></span> | <span data-ttu-id="216fe-133">Значение</span><span class="sxs-lookup"><span data-stu-id="216fe-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="216fe-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="216fe-134">Minimum supported client</span></span><br/> | <span data-ttu-id="216fe-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="216fe-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="216fe-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="216fe-136">Minimum supported server</span></span><br/> | <span data-ttu-id="216fe-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="216fe-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="216fe-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="216fe-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="216fe-139"><dt>Мсидент. h</dt></span><span class="sxs-lookup"><span data-stu-id="216fe-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="216fe-140">IDL</span><span class="sxs-lookup"><span data-stu-id="216fe-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="216fe-141"><dt>Мсидент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="216fe-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="216fe-142">DLL</span><span class="sxs-lookup"><span data-stu-id="216fe-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="216fe-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="216fe-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="216fe-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="216fe-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="216fe-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="216fe-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="216fe-146">**Иусеридентити:: Жетидентитифолдер**</span><span class="sxs-lookup"><span data-stu-id="216fe-146">**IUserIdentity::GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
