---
description: Подписывает хэш с помощью указанного закрытого ключа.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: Функция Сслсигнхаш (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497223"
---
# <a name="sslsignhash-function"></a><span data-ttu-id="911ed-103">Функция Сслсигнхаш</span><span class="sxs-lookup"><span data-stu-id="911ed-103">SslSignHash function</span></span>

<span data-ttu-id="911ed-104">Функция **сслсигнхаш** подписывает [*хэш*](/windows/desktop/SecGloss/h-gly) с помощью указанного [*закрытого ключа*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="911ed-104">The **SslSignHash** function signs a [*hash*](/windows/desktop/SecGloss/h-gly) by using the specified [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="911ed-105">Процесс подписывания выполняется на сервере.</span><span class="sxs-lookup"><span data-stu-id="911ed-105">The signing process is performed on the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="911ed-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="911ed-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="911ed-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="911ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="911ed-108">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="911ed-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="911ed-109">Обработчик для экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="911ed-109">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="911ed-110">*хприватекэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="911ed-110">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="911ed-111">Маркер закрытого ключа, используемый для подписи хэша.</span><span class="sxs-lookup"><span data-stu-id="911ed-111">The handle to the private key to use to sign the hash.</span></span>

</dd> <dt>

<span data-ttu-id="911ed-112">*пбхашвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="911ed-112">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="911ed-113">Указатель на буфер, содержащий хэш для подписи.</span><span class="sxs-lookup"><span data-stu-id="911ed-113">A pointer to a buffer that contains the hash to sign.</span></span>

</dd> <dt>

<span data-ttu-id="911ed-114">*кбхашвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="911ed-114">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="911ed-115">Размер (в байтах) буфера *пбхашвалуе* .</span><span class="sxs-lookup"><span data-stu-id="911ed-115">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="911ed-116">*пбсигнатуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="911ed-116">*pbSignature* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="911ed-117">Адрес буфера, который получает сигнатуру хэша.</span><span class="sxs-lookup"><span data-stu-id="911ed-117">The address of a buffer that receives the signature of the hash.</span></span> <span data-ttu-id="911ed-118">Параметр *кбсигнатуре* содержит размер этого буфера.</span><span class="sxs-lookup"><span data-stu-id="911ed-118">The *cbSignature* parameter contains the size of this buffer.</span></span> <span data-ttu-id="911ed-119">Чтобы определить требуемый размер буфера, присвойте параметру *Пбсигнатуре* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="911ed-119">To determine the required sized size of the buffer, set the *pbSignature* parameter to **NULL**.</span></span> <span data-ttu-id="911ed-120">Требуемый размер буфера будет возвращен в параметре *пкбресулт* .</span><span class="sxs-lookup"><span data-stu-id="911ed-120">The required size of the buffer will be returned in the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="911ed-121">*кбсигнатуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="911ed-121">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="911ed-122">Размер (в байтах) буфера *пбсигнатуре* .</span><span class="sxs-lookup"><span data-stu-id="911ed-122">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="911ed-123">*пкбресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="911ed-123">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="911ed-124">Указатель на значение, которое после завершения содержит фактическое число байтов, записанных в буфер *пбсигнатуре* .</span><span class="sxs-lookup"><span data-stu-id="911ed-124">A pointer to a value that, upon completion, contains the actual number of bytes written to the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="911ed-125">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="911ed-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="911ed-126">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="911ed-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="911ed-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="911ed-127">Return value</span></span>

<span data-ttu-id="911ed-128">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="911ed-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="911ed-129">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="911ed-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="911ed-130">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="911ed-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="911ed-131">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="911ed-131">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="911ed-132">Описание</span><span class="sxs-lookup"><span data-stu-id="911ed-132">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="911ed-133">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="911ed-133"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="911ed-134">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="911ed-134">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="911ed-135">Требования</span><span class="sxs-lookup"><span data-stu-id="911ed-135">Requirements</span></span>



| <span data-ttu-id="911ed-136">Требование</span><span class="sxs-lookup"><span data-stu-id="911ed-136">Requirement</span></span> | <span data-ttu-id="911ed-137">Значение</span><span class="sxs-lookup"><span data-stu-id="911ed-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="911ed-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="911ed-138">Minimum supported client</span></span><br/> | <span data-ttu-id="911ed-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="911ed-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="911ed-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="911ed-140">Minimum supported server</span></span><br/> | <span data-ttu-id="911ed-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="911ed-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="911ed-142">Header</span><span class="sxs-lookup"><span data-stu-id="911ed-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="911ed-143"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="911ed-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="911ed-144">DLL</span><span class="sxs-lookup"><span data-stu-id="911ed-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="911ed-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="911ed-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

