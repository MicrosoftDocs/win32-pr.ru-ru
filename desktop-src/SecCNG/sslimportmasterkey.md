---
description: Выполняет операцию обмена ключами протокола SSL на SSL стороне сервера.
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Функция Сслимпортмастеркэй (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647360"
---
# <a name="sslimportmasterkey-function"></a><span data-ttu-id="fe93c-103">Функция Сслимпортмастеркэй</span><span class="sxs-lookup"><span data-stu-id="fe93c-103">SslImportMasterKey function</span></span>

<span data-ttu-id="fe93c-104">Функция **сслимпортмастеркэй** выполняет операцию обмена ключами протокола SSL на [*SSL*](/windows/desktop/SecGloss/s-gly) стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="fe93c-104">The **SslImportMasterKey** function performs a server-side [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) key exchange operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe93c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe93c-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fe93c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe93c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe93c-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe93c-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe93c-108">Обработчик для экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="fe93c-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="fe93c-109">*хприватекэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe93c-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe93c-110">Маркер [*закрытого ключа*](/windows/desktop/SecGloss/p-gly) , используемый в Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe93c-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="fe93c-111">*фмастеркэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fe93c-111">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe93c-112">Указатель на маркер, получающий [*главный ключ*](/windows/desktop/SecGloss/m-gly).</span><span class="sxs-lookup"><span data-stu-id="fe93c-112">A pointer to the handle to receive the [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="fe93c-113">*двпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe93c-113">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe93c-114">Одно из значений [**идентификатора протокола поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="fe93c-114">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="fe93c-115">*двЦиферсуите* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe93c-115">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe93c-116">Один из значений [**идентификаторов комплекта шифров поставщика CNG SSL**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="fe93c-116">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="fe93c-117">*ппараметерлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe93c-117">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe93c-118">Указатель на массив буферов [**нкриптбуффер**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) , содержащих сведения, используемые в рамках операции обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="fe93c-118">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="fe93c-119">Точный набор буферов зависит от используемого протокола и набора шифров.</span><span class="sxs-lookup"><span data-stu-id="fe93c-119">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="fe93c-120">По крайней мере, список будет содержать буферы, содержащие клиентские и серверные случайные значения.</span><span class="sxs-lookup"><span data-stu-id="fe93c-120">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="fe93c-121">*пбенкриптедкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe93c-121">*pbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe93c-122">Указатель на буфер, содержащий зашифрованный предварительный основной секретный ключ, зашифрованный с помощью [*открытого ключа*](/windows/desktop/SecGloss/p-gly) сервера.</span><span class="sxs-lookup"><span data-stu-id="fe93c-122">A pointer to a buffer that contains the encrypted premaster secret key encrypted with the [*public key*](/windows/desktop/SecGloss/p-gly) of the server.</span></span>

</dd> <dt>

<span data-ttu-id="fe93c-123">*кбенкриптедкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe93c-123">*cbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe93c-124">Размер (в байтах) буфера *пбенкриптедкэй* .</span><span class="sxs-lookup"><span data-stu-id="fe93c-124">The size, in bytes, of the *pbEncryptedKey* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="fe93c-125">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe93c-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe93c-126">Установите для этого параметра **\_ \_ \_ флаг NCRYPT SSL-сервера** , чтобы указать, что это вызов сервера.</span><span class="sxs-lookup"><span data-stu-id="fe93c-126">Set this parameter to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe93c-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe93c-127">Return value</span></span>

<span data-ttu-id="fe93c-128">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="fe93c-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="fe93c-129">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="fe93c-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="fe93c-130">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="fe93c-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="fe93c-131">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="fe93c-131">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="fe93c-132">Описание</span><span class="sxs-lookup"><span data-stu-id="fe93c-132">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe93c-133">Не <dt>**превышать \_ НЕТ \_**</dt> <dt>0x8009000EL</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="fe93c-133"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="fe93c-134">Недостаточно памяти для выделения необходимых буферов.</span><span class="sxs-lookup"><span data-stu-id="fe93c-134">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="fe93c-135">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fe93c-135"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="fe93c-136">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="fe93c-136">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="fe93c-137">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="fe93c-137"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="fe93c-138">Параметр *фмастеркэй* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fe93c-138">The *phMasterKey* parameter is **NULL**.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="fe93c-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe93c-139">Remarks</span></span>

<span data-ttu-id="fe93c-140">Эта функция расшифровывает предварительный основной секрет, рассчитывает главный секрет SSL и возвращает в вызывающий объект маркер этого объекта.</span><span class="sxs-lookup"><span data-stu-id="fe93c-140">This function decrypts the premaster secret, computes the SSL master secret, and returns a handle to this object to the caller.</span></span> <span data-ttu-id="fe93c-141">Затем этот главный ключ можно использовать для получения ключа сеанса SSL и завершения подтверждения SSL.</span><span class="sxs-lookup"><span data-stu-id="fe93c-141">This master key can then be used to derive the SSL session key and finish the SSL handshake.</span></span>

> [!Note]  
> <span data-ttu-id="fe93c-142">Эта функция используется при использовании алгоритма обмена ключами [*RSA*](/windows/desktop/SecGloss/r-gly) .</span><span class="sxs-lookup"><span data-stu-id="fe93c-142">This function is used when the [*RSA*](/windows/desktop/SecGloss/r-gly) key exchange algorithm is being used.</span></span> <span data-ttu-id="fe93c-143">Когда используется [*DH*](/windows/desktop/SecGloss/d-gly) , серверный код вызывает [**сслженератемастеркэй**](sslgeneratemasterkey.md) .</span><span class="sxs-lookup"><span data-stu-id="fe93c-143">When [*DH*](/windows/desktop/SecGloss/d-gly) is used, then the server code calls [**SslGenerateMasterKey**](sslgeneratemasterkey.md) instead.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe93c-144">Требования</span><span class="sxs-lookup"><span data-stu-id="fe93c-144">Requirements</span></span>



| <span data-ttu-id="fe93c-145">Требование</span><span class="sxs-lookup"><span data-stu-id="fe93c-145">Requirement</span></span> | <span data-ttu-id="fe93c-146">Значение</span><span class="sxs-lookup"><span data-stu-id="fe93c-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe93c-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe93c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="fe93c-148">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe93c-148">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fe93c-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe93c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="fe93c-150">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe93c-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fe93c-151">Header</span><span class="sxs-lookup"><span data-stu-id="fe93c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe93c-152"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe93c-152"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="fe93c-153">DLL</span><span class="sxs-lookup"><span data-stu-id="fe93c-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe93c-154"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe93c-154"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

