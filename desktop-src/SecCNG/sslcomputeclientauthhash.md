---
description: Вычисление хэша, используемого во время проверки подлинности сертификата.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: Функция Сслкомпутеклиентаусхаш (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: faea1699657efd92049068e48ff361c48242e9c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264034"
---
# <a name="sslcomputeclientauthhash-function"></a><span data-ttu-id="54931-103">Функция Сслкомпутеклиентаусхаш</span><span class="sxs-lookup"><span data-stu-id="54931-103">SslComputeClientAuthHash function</span></span>

<span data-ttu-id="54931-104">Функция **сслкомпутеклиентаусхаш** вычислит [*хэш*](/windows/desktop/SecGloss/h-gly) , используемый во время проверки подлинности [*сертификата*](/windows/desktop/SecGloss/c-gly) .</span><span class="sxs-lookup"><span data-stu-id="54931-104">The **SslComputeClientAuthHash** function computes a [*hash*](/windows/desktop/SecGloss/h-gly) to use during [*certificate*](/windows/desktop/SecGloss/c-gly) authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="54931-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54931-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="54931-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="54931-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54931-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54931-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54931-108">Маркер экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="54931-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="54931-109">*хмастеркэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54931-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54931-110">Маркер объекта [*главного ключа*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="54931-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="54931-111">*ххандшакехаш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54931-111">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54931-112">Маркер хэширования, вычисленный до сих пор.</span><span class="sxs-lookup"><span data-stu-id="54931-112">The handle of the hash of the handshake computed so far.</span></span>

</dd> <dt>

<span data-ttu-id="54931-113">*псзалгид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54931-113">*pszAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54931-114">Указатель на строку в Юникоде, завершающуюся нулем, которая определяет запрошенный [*алгоритм шифрования*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="54931-114">A pointer to a null-terminated Unicode string that identifies the requested [*cryptographic algorithm*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="54931-115">Это может быть один из стандартных [**идентификаторов алгоритма CNG**](cng-algorithm-identifiers.md) или идентификатор другого зарегистрированного алгоритма.</span><span class="sxs-lookup"><span data-stu-id="54931-115">This can be one of the standard [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or the identifier for another registered algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="54931-116">*пбаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="54931-116">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54931-117">Адрес буфера, который получает [*большой двоичный объект ключа*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="54931-117">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="54931-118">Параметр *кбаутпут* содержит размер этого буфера.</span><span class="sxs-lookup"><span data-stu-id="54931-118">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="54931-119">Если этот параметр имеет **значение NULL**, эта функция поместит требуемый размер (в байтах) в **DWORD** , на который указывает параметр *пкбресулт* .</span><span class="sxs-lookup"><span data-stu-id="54931-119">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="54931-120">*кбаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54931-120">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54931-121">Длина буфера *пбаутпут* в байтах.</span><span class="sxs-lookup"><span data-stu-id="54931-121">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="54931-122">*пкбресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="54931-122">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54931-123">Указатель на значение **DWORD** , определяющее длину хэша в байтах, записанных в буфер *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="54931-123">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="54931-124">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54931-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54931-125">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="54931-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54931-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54931-126">Return value</span></span>

<span data-ttu-id="54931-127">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="54931-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="54931-128">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="54931-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="54931-129">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="54931-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="54931-130">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="54931-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="54931-131">Описание</span><span class="sxs-lookup"><span data-stu-id="54931-131">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="54931-132">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="54931-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="54931-133">Один из представленных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="54931-133">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54931-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54931-134">Remarks</span></span>

<span data-ttu-id="54931-135">Функция **сслкомпутеклиентаусхаш** вычислит хэш, который отправляется в сообщении о проверке сертификата SSL-подтверждения.</span><span class="sxs-lookup"><span data-stu-id="54931-135">The **SslComputeClientAuthHash** function computes the hash that is sent in the certificate verification message of the SSL handshake.</span></span> <span data-ttu-id="54931-136">Хэш-значение выдается путем создания хэша, содержащего главный секрет с хэш-кодом всех отправленных или полученных сообщений о подтверждении предыдущего подтверждения.</span><span class="sxs-lookup"><span data-stu-id="54931-136">The hash value is computed by creating a hash that contains the master secret with a hash of all previous handshake messages sent or received.</span></span> <span data-ttu-id="54931-137">Дополнительные сведения о последовательности подтверждения SSL см. [в разделе Описание подтверждения SSL (SSL)](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="54931-137">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

<span data-ttu-id="54931-138">Способ вычисления хэша зависит от используемого протокола и набора шифров.</span><span class="sxs-lookup"><span data-stu-id="54931-138">The manner in which the hash is computed depends on the protocol and cipher suite used.</span></span> <span data-ttu-id="54931-139">Кроме того, хэш зависит от типа используемого ключа проверки подлинности клиента. параметр *псзалгид* указывает тип ключа, используемого для проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="54931-139">In addition, the hash depends on the type of client authentication key used; the *pszAlgId* parameter indicates the type of key used for client authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="54931-140">Требования</span><span class="sxs-lookup"><span data-stu-id="54931-140">Requirements</span></span>



| <span data-ttu-id="54931-141">Требование</span><span class="sxs-lookup"><span data-stu-id="54931-141">Requirement</span></span> | <span data-ttu-id="54931-142">Значение</span><span class="sxs-lookup"><span data-stu-id="54931-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54931-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54931-143">Minimum supported client</span></span><br/> | <span data-ttu-id="54931-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54931-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="54931-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54931-145">Minimum supported server</span></span><br/> | <span data-ttu-id="54931-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54931-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="54931-147">Header</span><span class="sxs-lookup"><span data-stu-id="54931-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="54931-148"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="54931-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="54931-149">DLL</span><span class="sxs-lookup"><span data-stu-id="54931-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54931-150"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54931-150"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

