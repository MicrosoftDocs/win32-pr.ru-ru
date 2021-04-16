---
description: 'Возвращает идентификатор алгоритма шифрования API: следующего поколения (CNG) алгоритма хэширования, который используется для функции "псевдо-Random" протокола TLS (PRF) для входного протокола, набора шифров и типа ключа.'
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: Функция СслжетЦиферсуитепрфхашалгорисм (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664726"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a><span data-ttu-id="b45b8-103">Функция СслжетЦиферсуитепрфхашалгорисм</span><span class="sxs-lookup"><span data-stu-id="b45b8-103">SslGetCipherSuitePRFHashAlgorithm function</span></span>

<span data-ttu-id="b45b8-104">Функция **сслжетЦиферсуитепрфхашалгорисм** возвращает идентификатор алгоритма шифрования API: следующего поколения (CNG) [*алгоритма хэширования*](/windows/desktop/SecGloss/h-gly) , который используется для [*функции псевдо-Random*](/windows/desktop/SecGloss/p-gly) (PRF) [*для протокола ввода*](/windows/desktop/SecGloss/t-gly) , набора шифров и типа ключа.</span><span class="sxs-lookup"><span data-stu-id="b45b8-104">The **SslGetCipherSuitePRFHashAlgorithm** function returns the Cryptography API: Next Generation (CNG) Algorithm Identifier of the [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that is used for the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) [*pseudo-random function*](/windows/desktop/SecGloss/p-gly) (PRF) for the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b45b8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b45b8-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b45b8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b45b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b45b8-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b45b8-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b45b8-108">Маркер экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="b45b8-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="b45b8-109">*двпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b45b8-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b45b8-110">Одно из значений [**идентификатора протокола поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="b45b8-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="b45b8-111">*двЦиферсуите* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b45b8-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b45b8-112">Один из значений [**идентификатора комплекта шифров поставщика CNG SSL**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="b45b8-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="b45b8-113">*двкэйтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b45b8-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b45b8-114">Одно из значений [**идентификатора типа ключа поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="b45b8-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="b45b8-115">Для типов ключей, не являющихся [*шифрованием на основе эллиптических кривых*](/windows/desktop/SecGloss/e-gly) (ECC), установите этот параметр в ноль.</span><span class="sxs-lookup"><span data-stu-id="b45b8-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b45b8-116">*сзпрфхаш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b45b8-116">*szPRFHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b45b8-117">Один из [**идентификаторов алгоритма CNG**](cng-algorithm-identifiers.md) для хэша, который будет использоваться для протокола TLS PRF.</span><span class="sxs-lookup"><span data-stu-id="b45b8-117">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) for the hash that will be used for the TLS PRF.</span></span>

</dd> <dt>

<span data-ttu-id="b45b8-118">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b45b8-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b45b8-119">Этот параметр зарезервирован для будущего использования и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="b45b8-119">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b45b8-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b45b8-120">Return value</span></span>

<span data-ttu-id="b45b8-121">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b45b8-121">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="b45b8-122">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="b45b8-122">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="b45b8-123">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="b45b8-123">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="b45b8-124">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b45b8-124">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="b45b8-125">Описание</span><span class="sxs-lookup"><span data-stu-id="b45b8-125">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b45b8-126">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b45b8-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="b45b8-127">Параметр *хсслпровидер* содержит недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="b45b8-127">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="b45b8-128">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="b45b8-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="b45b8-129">Параметр *сзпрфхаш* имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="b45b8-129">The *szPRFHash* parameter is set to **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="b45b8-130">Не <dt>**превышать \_ НЕ \_ поддерживается**</dt> <dt>0x80090029L</dt></span><span class="sxs-lookup"><span data-stu-id="b45b8-130"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="b45b8-131">Выбранная функция не поддерживается в указанной версии интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b45b8-131">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="b45b8-132">Не <dt>**превышать \_ Неправильные \_ Флаги**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="b45b8-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="b45b8-133">Параметр *dwFlags* должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="b45b8-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="b45b8-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b45b8-134">Remarks</span></span>

<span data-ttu-id="b45b8-135">Эта функция **сслжетЦиферсуитепрфхашалгорисм** вызывается для запросов TLS 1,2 или более поздних версий для запроса алгоритма хэширования, который будет использоваться в протоколе TLS PRF.</span><span class="sxs-lookup"><span data-stu-id="b45b8-135">This **SslGetCipherSuitePRFHashAlgorithm** function is called for TLS 1.2 or later conversations to query the hashing algorithm that will be used in the TLS PRF.</span></span>

## <a name="requirements"></a><span data-ttu-id="b45b8-136">Требования</span><span class="sxs-lookup"><span data-stu-id="b45b8-136">Requirements</span></span>



| <span data-ttu-id="b45b8-137">Требование</span><span class="sxs-lookup"><span data-stu-id="b45b8-137">Requirement</span></span> | <span data-ttu-id="b45b8-138">Значение</span><span class="sxs-lookup"><span data-stu-id="b45b8-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45b8-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b45b8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b45b8-140">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b45b8-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b45b8-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b45b8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b45b8-142">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b45b8-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b45b8-143">Header</span><span class="sxs-lookup"><span data-stu-id="b45b8-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b45b8-144"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="b45b8-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="b45b8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b45b8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b45b8-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b45b8-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

