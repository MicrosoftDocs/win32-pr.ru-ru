---
description: Выполняет вычисление хэша, отправленного в сообщении SSL о завершении подтверждения протокола SSL.
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Функция Сслкомпутефинишедхаш (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991620"
---
# <a name="sslcomputefinishedhash-function"></a><span data-ttu-id="b0dd9-103">Функция Сслкомпутефинишедхаш</span><span class="sxs-lookup"><span data-stu-id="b0dd9-103">SslComputeFinishedHash function</span></span>

<span data-ttu-id="b0dd9-104">Функция **сслкомпутефинишедхаш** выполняет вычисление [*хэша*](/windows/desktop/SecGloss/h-gly) , отправленного в сообщении SSL о завершении подтверждения [*протокола*](/windows/desktop/SecGloss/s-gly) SSL.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-104">The **SslComputeFinishedHash** function computes the [*hash*](/windows/desktop/SecGloss/h-gly) sent in the finished message of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span> <span data-ttu-id="b0dd9-105">Дополнительные сведения о последовательности подтверждения SSL см. [в разделе Описание подтверждения SSL (SSL)](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="b0dd9-105">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0dd9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0dd9-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b0dd9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0dd9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0dd9-108">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0dd9-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0dd9-109">Маркер экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-109">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="b0dd9-110">*хмастеркэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0dd9-110">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0dd9-111">Маркер объекта [*главного ключа*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="b0dd9-111">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="b0dd9-112">*ххандшакехаш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0dd9-112">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0dd9-113">Маркер хэша сообщений подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-113">The handle of the hash of the handshake messages.</span></span>

</dd> <dt>

<span data-ttu-id="b0dd9-114">*пбаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b0dd9-114">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0dd9-115">Указатель на буфер, который получает хэш для сообщения о завершении.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-115">A pointer to a buffer that receives the hash for the finish message.</span></span>

</dd> <dt>

<span data-ttu-id="b0dd9-116">*кбаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0dd9-116">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0dd9-117">Длина буфера *пбаутпут* в байтах.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-117">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b0dd9-118">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0dd9-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0dd9-119">Одна из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-119">One of the following constants.</span></span>



| <span data-ttu-id="b0dd9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b0dd9-120">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="b0dd9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b0dd9-121">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="b0dd9-122"><dt>**NCRYPT \_ \_ \_ Флаг клиента SSL**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b0dd9-122"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="b0dd9-123">Указывает, что это вызов клиента.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-123">Specifies that this is a client call.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="b0dd9-124"><dt>**NCRYPT \_ \_ \_ Флаг сервера SSL**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b0dd9-124"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="b0dd9-125">Указывает, что это вызов сервера.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-125">Specifies that this is a server call.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0dd9-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0dd9-126">Return value</span></span>

<span data-ttu-id="b0dd9-127">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="b0dd9-128">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-128">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="b0dd9-129">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b0dd9-129">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="b0dd9-130">Описание</span><span class="sxs-lookup"><span data-stu-id="b0dd9-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="b0dd9-131">Не <dt>**превышать \_ Недопустимый \_ HANDLE**</dt> <dt>2148073510 (0x80090026)</dt></span><span class="sxs-lookup"><span data-stu-id="b0dd9-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>2148073510 (0x80090026)</dt></span></span> </dl> | <span data-ttu-id="b0dd9-132">Один из представленных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-132">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0dd9-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0dd9-133">Remarks</span></span>

<span data-ttu-id="b0dd9-134">Функция **сслкомпутефинишедхаш** является одной из трех функций, используемых для создания хэша, используемого во время подтверждения SSL.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-134">The **SslComputeFinishedHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="b0dd9-135">Для получения обработчика хэша вызывается функция [**сслкреатехандшакехаш**](sslcreatehandshakehash.md) .</span><span class="sxs-lookup"><span data-stu-id="b0dd9-135">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="b0dd9-136">Функция [**сслхашхандшаке**](sslhashhandshake.md) вызывается любое количество раз с обработчиком хэша для добавления данных в хэш.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-136">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="b0dd9-137">Функция **сслкомпутефинишедхаш** вызывается с хэш-маркером для получения дайджеста хэшированных данных.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-137">The **SslComputeFinishedHash** function is called with the hash handle to obtain the digest of the hashed data.</span></span>

<span data-ttu-id="b0dd9-138">Хэш-значение вычисляются путем хэширования главного секрета с использованием хэша всех отправленных или полученных сообщений предыдущего подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-138">The hash value is computed by hashing the master secret with a hash of all previous handshake messages sent or received.</span></span>

<span data-ttu-id="b0dd9-139">Значение *кбаутпут* определяет длину хэш-данных.</span><span class="sxs-lookup"><span data-stu-id="b0dd9-139">The value of *cbOutput* determines the length of the hash data.</span></span> <span data-ttu-id="b0dd9-140">Если используется [*протокол tls*](/windows/desktop/SecGloss/t-gly) 1,0, это значение всегда должно быть равно 12 (байт).</span><span class="sxs-lookup"><span data-stu-id="b0dd9-140">When the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.0 protocol is used, this should always be 12 (bytes).</span></span> <span data-ttu-id="b0dd9-141">Дополнительные сведения см. в описании [протокола TLS версии 1,0](https://www.ietf.org/rfc/rfc2246.txt).</span><span class="sxs-lookup"><span data-stu-id="b0dd9-141">For more information, see [The TLS Protocol Version 1.0](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0dd9-142">Требования</span><span class="sxs-lookup"><span data-stu-id="b0dd9-142">Requirements</span></span>



| <span data-ttu-id="b0dd9-143">Требование</span><span class="sxs-lookup"><span data-stu-id="b0dd9-143">Requirement</span></span> | <span data-ttu-id="b0dd9-144">Значение</span><span class="sxs-lookup"><span data-stu-id="b0dd9-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0dd9-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0dd9-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b0dd9-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0dd9-146">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b0dd9-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0dd9-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b0dd9-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b0dd9-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b0dd9-149">Header</span><span class="sxs-lookup"><span data-stu-id="b0dd9-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0dd9-150"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0dd9-150"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="b0dd9-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b0dd9-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0dd9-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0dd9-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

