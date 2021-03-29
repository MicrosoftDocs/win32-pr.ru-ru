---
description: Возвращает сертификат из учетных данных пользователя.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: Функция Жетцертификатефромкред (Лсаидпров. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647281"
---
# <a name="getcertificatefromcred-function"></a><span data-ttu-id="771b8-103">Функция Жетцертификатефромкред</span><span class="sxs-lookup"><span data-stu-id="771b8-103">GetCertificateFromCred function</span></span>

<span data-ttu-id="771b8-104">Возвращает сертификат из учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="771b8-104">Gets the certificate from the user credential.</span></span>

## <a name="syntax"></a><span data-ttu-id="771b8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="771b8-105">Syntax</span></span>


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a><span data-ttu-id="771b8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="771b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="771b8-107">*Провидерхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="771b8-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771b8-108">Маркер поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="771b8-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="771b8-109">*Клиенттокен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="771b8-109">*ClientToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771b8-110">Маркер вызывающего объекта, который получает сертификат.</span><span class="sxs-lookup"><span data-stu-id="771b8-110">Token of the caller who is retrieving the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="771b8-111">*Супплиедкред* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="771b8-111">*SuppliedCred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771b8-112">Указатель на SECPKG структуру [**\_ \_ учетных данных**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) , содержащую учетные данные для идентификатора в сети, сертификат которого запрашивается.</span><span class="sxs-lookup"><span data-stu-id="771b8-112">A pointer to a [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure that contains the credential of an online ID whose certificate is requested.</span></span> <span data-ttu-id="771b8-113">Поставщик удостоверений должен проверить входные данные так, как если бы они поступили из ненадежного источника.</span><span class="sxs-lookup"><span data-stu-id="771b8-113">The identity provider must validate the input data as if it is coming from an untrusted source.</span></span>

</dd> <dt>

<span data-ttu-id="771b8-114">*Супплиедкредсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="771b8-114">*SuppliedCredSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771b8-115">Размер (в байтах) буфера *супплиедкред* .</span><span class="sxs-lookup"><span data-stu-id="771b8-115">The size, in bytes, of the *SuppliedCred* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="771b8-116">*Цертконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="771b8-116">*CertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="771b8-117">Если функция выполнена, этот параметр является указателем на возвращаемый \_ указатель контекста кцерт.</span><span class="sxs-lookup"><span data-stu-id="771b8-117">If the function succeeds, this parameter is a pointer to the returned CCERT\_CONTEXT pointer.</span></span> <span data-ttu-id="771b8-118">Завершив использование контекста сертификата, освободите его, вызвав функцию [**цертфрицертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="771b8-118">When you have finished using the certificate context, release it by calling the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="771b8-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="771b8-119">Return value</span></span>

<span data-ttu-id="771b8-120">Если функция завершается успешно, функция возвращает состояние \_ Success.</span><span class="sxs-lookup"><span data-stu-id="771b8-120">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="771b8-121">Если функция завершается ошибкой, функция может вернуть один из следующих кодов ошибок NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="771b8-121">If the function fails, the function may return one of the following NTSTATUS error codes.</span></span>



| <span data-ttu-id="771b8-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="771b8-122">Return value</span></span>                                                                                            | <span data-ttu-id="771b8-123">Описание</span><span class="sxs-lookup"><span data-stu-id="771b8-123">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="771b8-124"><dt>СОСТОЯНИЕ \_ не \_ поддерживается</dt></span><span class="sxs-lookup"><span data-stu-id="771b8-124"><dt>STATUS\_NOT\_SUPPORTED</dt></span></span> </dl>       | <span data-ttu-id="771b8-125">Поставщик удостоверений не распознает тип учетных данных предоставляемых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="771b8-125">The identity provider does not recognize the credential type of the supplied credential.</span></span> <span data-ttu-id="771b8-126">LSA попытается обратиться к следующему поставщику удостоверений.</span><span class="sxs-lookup"><span data-stu-id="771b8-126">LSA will try the next identity provider.</span></span><br/>                                           |
| <dl> <span data-ttu-id="771b8-127"><dt>\_Ошибка входа в состояние \_</dt></span><span class="sxs-lookup"><span data-stu-id="771b8-127"><dt>STATUS\_LOGON\_FAILURE</dt></span></span> </dl>       | <span data-ttu-id="771b8-128">Неверные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="771b8-128">The credential is incorrect.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="771b8-129"><dt>\_Недопустимый \_ параметр Status</dt></span><span class="sxs-lookup"><span data-stu-id="771b8-129"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>   | <span data-ttu-id="771b8-130">Недействительный параметр.</span><span class="sxs-lookup"><span data-stu-id="771b8-130">A parameter is not valid.</span></span> <span data-ttu-id="771b8-131">Учетные данные могут быть в неправильном формате, а не в определенной структуре [**\_ \_ учетных данных SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) .</span><span class="sxs-lookup"><span data-stu-id="771b8-131">The credential may be in an incorrect format and not in the defined [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure.</span></span><br/> |
| <dl> <span data-ttu-id="771b8-132"><dt>СОСТОЯНИЕ " \_ сеть \_ недоступна"</dt></span><span class="sxs-lookup"><span data-stu-id="771b8-132"><dt>STATUS\_NETWORK\_UNREACHABLE</dt></span></span> </dl> | <span data-ttu-id="771b8-133">Поставщик удостоверений не может связаться с облаком для получения сертификата.</span><span class="sxs-lookup"><span data-stu-id="771b8-133">The identity provider cannot contact the cloud to obtain the certificate.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="771b8-134"><dt>\_ \_ срок действия пароля истек</dt></span><span class="sxs-lookup"><span data-stu-id="771b8-134"><dt>STATUS\_PASSWORD\_EXPIRED</dt></span></span> </dl>    | <span data-ttu-id="771b8-135">Срок действия пароля учетной записи истек.</span><span class="sxs-lookup"><span data-stu-id="771b8-135">The account password has expired.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="771b8-136"><dt>\_учетная запись состояния \_ заблокирована \_</dt></span><span class="sxs-lookup"><span data-stu-id="771b8-136"><dt>STATUS\_ACCOUNT\_LOCKED\_OUT</dt></span></span> </dl> | <span data-ttu-id="771b8-137">Учетная запись заблокирована.</span><span class="sxs-lookup"><span data-stu-id="771b8-137">The account has been locked out.</span></span> <br/>                                                                                                                                           |
| <dl> <span data-ttu-id="771b8-138"><dt>Прочие</dt></span><span class="sxs-lookup"><span data-stu-id="771b8-138"><dt>Others</dt></span></span> </dl>                       | <span data-ttu-id="771b8-139">Другие коды ошибок, относящиеся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="771b8-139">Other provider-specific error codes.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="771b8-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="771b8-140">Remarks</span></span>

<span data-ttu-id="771b8-141">Перед получением сертификата из облака поставщик удостоверений должен проверить наличие действительного сертификата для этого пользователя в хранилище сертификатов пользователя "MY".</span><span class="sxs-lookup"><span data-stu-id="771b8-141">Before fetching the certificate from the cloud, the identity provider should check that there is a valid certificate for this user in the user's "MY" certificate store.</span></span> <span data-ttu-id="771b8-142">Если существует действительный сертификат, поставщик должен вернуть этот сертификат, чтобы избежать ненужного сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="771b8-142">If a valid certificate exists, the provider should return this certificate to avoid unnecessary network traffic.</span></span>

<span data-ttu-id="771b8-143">Поставщик удостоверений также может кэшировать сертификат локально, если он защищен от текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="771b8-143">The identity provider can also cache the certificate locally as long as it is protected from the current user.</span></span>

## <a name="requirements"></a><span data-ttu-id="771b8-144">Требования</span><span class="sxs-lookup"><span data-stu-id="771b8-144">Requirements</span></span>



| <span data-ttu-id="771b8-145">Требование</span><span class="sxs-lookup"><span data-stu-id="771b8-145">Requirement</span></span> | <span data-ttu-id="771b8-146">Значение</span><span class="sxs-lookup"><span data-stu-id="771b8-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="771b8-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="771b8-147">Minimum supported client</span></span><br/> | <span data-ttu-id="771b8-148">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="771b8-148">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="771b8-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="771b8-149">Minimum supported server</span></span><br/> | <span data-ttu-id="771b8-150">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="771b8-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="771b8-151">Header</span><span class="sxs-lookup"><span data-stu-id="771b8-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="771b8-152"><dt>Лсаидпров. h</dt></span><span class="sxs-lookup"><span data-stu-id="771b8-152"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

