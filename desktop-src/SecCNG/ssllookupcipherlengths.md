---
description: Возвращает \_ \_ структуру длины шифра NCRYPT SSL \_ , которая содержит заголовок и длину трейлеров входного протокола, набора шифров и типа ключа.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: Функция СсллукупЦиферленгсс (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991568"
---
# <a name="ssllookupcipherlengths-function"></a><span data-ttu-id="c1dfd-103">Функция СсллукупЦиферленгсс</span><span class="sxs-lookup"><span data-stu-id="c1dfd-103">SslLookupCipherLengths function</span></span>

<span data-ttu-id="c1dfd-104">Функция **ссллукупЦиферленгсс** возвращает структуру [**\_ \_ \_ длины шифра NCRYPT SSL**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) , которая содержит заголовок и длину трейлеров входного протокола, набора шифров и типа ключа.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-104">The **SslLookupCipherLengths** function returns an [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure that contains the header and trailer lengths of the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1dfd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1dfd-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c1dfd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1dfd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1dfd-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1dfd-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dfd-108">Маркер экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="c1dfd-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="c1dfd-109">*двпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1dfd-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dfd-110">Одно из значений [**идентификатора протокола поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c1dfd-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="c1dfd-111">*двЦиферсуите* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1dfd-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dfd-112">Один из значений [**идентификатора комплекта шифров поставщика CNG SSL**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c1dfd-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="c1dfd-113">*двкэйтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1dfd-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dfd-114">Одно из значений [**идентификатора типа ключа поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c1dfd-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="c1dfd-115">Для типов ключей, не являющихся [*шифрованием на основе эллиптических кривых*](/windows/desktop/SecGloss/e-gly) (ECC), установите этот параметр в ноль.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1dfd-116">*пЦиферленгсс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c1dfd-116">*pCipherLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dfd-117">Указатель на буфер для получения структуры [**\_ \_ \_ длины шифра SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) .</span><span class="sxs-lookup"><span data-stu-id="c1dfd-117">A pointer to a buffer to receive the [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c1dfd-118">*кбЦиферленгсс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1dfd-118">*cbCipherLengths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dfd-119">Длина буфера в байтах, на которую указывает параметр *пЦиферленгсс* .</span><span class="sxs-lookup"><span data-stu-id="c1dfd-119">The length, in bytes, of the buffer pointed to by the *pCipherLengths* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c1dfd-120">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1dfd-120">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dfd-121">Этот параметр зарезервирован для будущего использования и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-121">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1dfd-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1dfd-122">Return value</span></span>

<span data-ttu-id="c1dfd-123">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-123">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="c1dfd-124">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-124">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="c1dfd-125">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-125">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="c1dfd-126">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c1dfd-126">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="c1dfd-127">Описание</span><span class="sxs-lookup"><span data-stu-id="c1dfd-127">Description</span></span>                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1dfd-128">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c1dfd-128"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="c1dfd-129">Параметр *хсслпровидер* содержит недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-129">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="c1dfd-130">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="c1dfd-130"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="c1dfd-131">Параметр *пЦиферленгсс* имеет значение **null** , или длина буфера, заданная параметром *кбЦиферленгсс* , слишком мала.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-131">The *pCipherLengths* parameter is set to **NULL** or the buffer length specified by the *cbCipherLengths* is too short.</span></span><br/> |
| <dl> <span data-ttu-id="c1dfd-132">Не <dt>**превышать \_ Неправильные \_ Флаги**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="c1dfd-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="c1dfd-133">Параметр *dwFlags* должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="c1dfd-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1dfd-134">Remarks</span></span>

<span data-ttu-id="c1dfd-135">Функция **ссллукупЦиферленгсс** вызывается для протокола TLS 1,1 или более поздних диалоговых [*окон*](/windows/desktop/SecGloss/t-gly) , чтобы запросить заголовок и длину трейлеров для запрошенного протокола, набора шифров и типа ключа.</span><span class="sxs-lookup"><span data-stu-id="c1dfd-135">The **SslLookupCipherLengths** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.1 or later conversations to query the header and trailer lengths for the requested protocol, cipher suite, and key type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1dfd-136">Требования</span><span class="sxs-lookup"><span data-stu-id="c1dfd-136">Requirements</span></span>



| <span data-ttu-id="c1dfd-137">Требование</span><span class="sxs-lookup"><span data-stu-id="c1dfd-137">Requirement</span></span> | <span data-ttu-id="c1dfd-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c1dfd-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1dfd-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1dfd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c1dfd-140">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c1dfd-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c1dfd-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1dfd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c1dfd-142">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1dfd-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1dfd-143">Header</span><span class="sxs-lookup"><span data-stu-id="c1dfd-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1dfd-144"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1dfd-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="c1dfd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c1dfd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1dfd-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1dfd-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

