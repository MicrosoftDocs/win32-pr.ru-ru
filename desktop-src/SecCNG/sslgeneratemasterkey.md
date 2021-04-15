---
description: Вычисление главного секретного ключа (SSL) SSL.
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: Функция Сслженератемастеркэй (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424074"
---
# <a name="sslgeneratemasterkey-function"></a><span data-ttu-id="b7eb6-103">Функция Сслженератемастеркэй</span><span class="sxs-lookup"><span data-stu-id="b7eb6-103">SslGenerateMasterKey function</span></span>

<span data-ttu-id="b7eb6-104">Функция **сслженератемастеркэй** [*выSSL*](/windows/desktop/SecGloss/s-gly) числит главный секретный ключ протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-104">The **SslGenerateMasterKey** function computes the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) master secret key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7eb6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7eb6-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b7eb6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7eb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7eb6-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb6-108">Обработчик для экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="b7eb6-109">*хприватекэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb6-110">Маркер [*закрытого ключа*](/windows/desktop/SecGloss/p-gly) , используемый в Exchange.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="b7eb6-111">*хпубликкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-111">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb6-112">Маркер [*открытого ключа*](/windows/desktop/SecGloss/p-gly) , используемый в обмене.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-112">The handle to the [*public key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="b7eb6-113">*фмастеркэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-113">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb6-114">Указатель на маркер созданного [*главного ключа*](/windows/desktop/SecGloss/m-gly).</span><span class="sxs-lookup"><span data-stu-id="b7eb6-114">A pointer to the handle to the generated [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="b7eb6-115">*двпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-115">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb6-116">Одно из значений [**идентификатора протокола поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="b7eb6-116">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="b7eb6-117">*двЦиферсуите* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-117">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb6-118">Один из значений [**идентификатора комплекта шифров поставщика CNG SSL**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="b7eb6-118">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="b7eb6-119">*ппараметерлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-119">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb6-120">Указатель на массив буферов [**нкриптбуффер**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) , содержащих сведения, используемые в рамках операции обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-120">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="b7eb6-121">Точный набор буферов зависит от используемого протокола и набора шифров.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-121">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="b7eb6-122">По крайней мере, список будет содержать буферы, содержащие клиентские и серверные случайные значения.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-122">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="b7eb6-123">*пбаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-123">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb6-124">Адрес буфера, который получает предварительный основной секрет, зашифрованный с помощью открытого ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-124">The address of a buffer that receives the premaster secret encrypted with the public key of the server.</span></span> <span data-ttu-id="b7eb6-125">Параметр *кбаутпут* содержит размер этого буфера.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-125">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="b7eb6-126">Если этот параметр имеет **значение NULL**, эта функция возвращает необходимый размер (в байтах) в **DWORD** , на который указывает параметр *пкбресулт* .</span><span class="sxs-lookup"><span data-stu-id="b7eb6-126">If this parameter is **NULL**, this function returns the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="b7eb6-127">Этот буфер используется при выполнении обмена ключами RSA.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-127">This buffer is used when performing a RSA key exchange.</span></span>

 

</dd> <dt>

<span data-ttu-id="b7eb6-128">*кбаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-128">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb6-129">Размер (в байтах) буфера *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="b7eb6-129">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b7eb6-130">*пкбресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-130">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb6-131">Указатель на значение **DWORD** , в котором будет помещено число байтов, записанных в буфер *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="b7eb6-131">A pointer to a **DWORD** value in which to place number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b7eb6-132">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb6-133">Указывает, используется ли эта функция для обмена ключами на стороне клиента или на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-133">Specifies whether this function is being used for client-side or server-side key exchange.</span></span>



| <span data-ttu-id="b7eb6-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b7eb6-134">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="b7eb6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b7eb6-135">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="b7eb6-136"><dt>**NCRYPT \_ \_ \_ Флаг клиента SSL**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b7eb6-136"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="b7eb6-137">Задает обмен ключами на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-137">Specifies a client-side key exchange.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="b7eb6-138"><dt>**NCRYPT \_ \_ \_ Флаг сервера SSL**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b7eb6-138"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="b7eb6-139">Задает обмен ключами на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-139">Specifies a server-side key exchange.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7eb6-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7eb6-140">Return value</span></span>

<span data-ttu-id="b7eb6-141">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-141">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="b7eb6-142">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-142">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="b7eb6-143">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-143">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="b7eb6-144">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b7eb6-144">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="b7eb6-145">Описание</span><span class="sxs-lookup"><span data-stu-id="b7eb6-145">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7eb6-146">Не <dt>**превышать \_ НЕТ \_**</dt> <dt>0x8009000EL</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="b7eb6-146"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="b7eb6-147">Недостаточно памяти для выделения необходимых буферов.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-147">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="b7eb6-148">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b7eb6-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="b7eb6-149">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="b7eb6-149">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="b7eb6-150">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="b7eb6-150"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="b7eb6-151">Недопустимый параметр *фмастеркэй* или *хпубликкэй* .</span><span class="sxs-lookup"><span data-stu-id="b7eb6-151">The *phMasterKey* or *hPublicKey* parameter is not valid.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="b7eb6-152">Требования</span><span class="sxs-lookup"><span data-stu-id="b7eb6-152">Requirements</span></span>



| <span data-ttu-id="b7eb6-153">Требование</span><span class="sxs-lookup"><span data-stu-id="b7eb6-153">Requirement</span></span> | <span data-ttu-id="b7eb6-154">Значение</span><span class="sxs-lookup"><span data-stu-id="b7eb6-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7eb6-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7eb6-155">Minimum supported client</span></span><br/> | <span data-ttu-id="b7eb6-156">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-156">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b7eb6-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7eb6-157">Minimum supported server</span></span><br/> | <span data-ttu-id="b7eb6-158">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7eb6-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b7eb6-159">Header</span><span class="sxs-lookup"><span data-stu-id="b7eb6-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7eb6-160"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7eb6-160"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="b7eb6-161">DLL</span><span class="sxs-lookup"><span data-stu-id="b7eb6-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7eb6-162"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7eb6-162"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

