---
description: Проверяет указанную сигнатуру с помощью предоставленного хэша и открытого ключа.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: Функция Сслверифисигнатуре (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cb2a50a7f16062f271a89b6061e3f2fa2dd16685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897090"
---
# <a name="sslverifysignature-function"></a><span data-ttu-id="55dfb-103">Функция Сслверифисигнатуре</span><span class="sxs-lookup"><span data-stu-id="55dfb-103">SslVerifySignature function</span></span>

<span data-ttu-id="55dfb-104">Функция **сслверифисигнатуре** проверяет указанную сигнатуру с помощью предоставленного [*хэша*](/windows/desktop/SecGloss/h-gly) и [*открытого ключа*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="55dfb-104">The **SslVerifySignature** function verifies the specified signature by using the supplied [*hash*](/windows/desktop/SecGloss/h-gly) and the [*public key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="55dfb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55dfb-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="55dfb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55dfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55dfb-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55dfb-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55dfb-108">Обработчик для экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="55dfb-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="55dfb-109">*хпубликкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55dfb-109">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55dfb-110">Маркер открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="55dfb-110">The handle to the public key.</span></span>

</dd> <dt>

<span data-ttu-id="55dfb-111">*пбхашвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55dfb-111">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55dfb-112">Указатель на буфер, содержащий хэш, используемый для проверки подписи.</span><span class="sxs-lookup"><span data-stu-id="55dfb-112">A pointer to a buffer that contains the hash to use to verify the signature.</span></span>

</dd> <dt>

<span data-ttu-id="55dfb-113">*кбхашвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55dfb-113">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55dfb-114">Размер (в байтах) буфера *пбхашвалуе* .</span><span class="sxs-lookup"><span data-stu-id="55dfb-114">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="55dfb-115">*пбсигнатуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55dfb-115">*pbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55dfb-116">Указатель на буфер, содержащий сигнатура для проверки.</span><span class="sxs-lookup"><span data-stu-id="55dfb-116">A pointer to a buffer that contains the signature to verify.</span></span>

</dd> <dt>

<span data-ttu-id="55dfb-117">*кбсигнатуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55dfb-117">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55dfb-118">Размер (в байтах) буфера *пбсигнатуре* .</span><span class="sxs-lookup"><span data-stu-id="55dfb-118">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="55dfb-119">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55dfb-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55dfb-120">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="55dfb-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55dfb-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55dfb-121">Return value</span></span>

<span data-ttu-id="55dfb-122">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="55dfb-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="55dfb-123">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="55dfb-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="55dfb-124">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="55dfb-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="55dfb-125">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="55dfb-125">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="55dfb-126">Описание</span><span class="sxs-lookup"><span data-stu-id="55dfb-126">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="55dfb-127">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="55dfb-127"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="55dfb-128">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="55dfb-128">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55dfb-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55dfb-129">Remarks</span></span>

<span data-ttu-id="55dfb-130">Функция **сслверифисигнатуре** в данный момент не вызывается Windows.</span><span class="sxs-lookup"><span data-stu-id="55dfb-130">The **SslVerifySignature** function is not currently called by Windows.</span></span> <span data-ttu-id="55dfb-131">Эта функция является обязательной частью интерфейса поставщика SSL и должна быть полностью реализована для обеспечения прямой совместимости.</span><span class="sxs-lookup"><span data-stu-id="55dfb-131">This function is a required part of the SSL Provider interface and should be fully implemented to ensure forward compatibility.</span></span>

<span data-ttu-id="55dfb-132">Текущая реализация серверной части подключения [*протокола*](/windows/desktop/SecGloss/t-gly) TLS вызывает функцию [**нкриптверифисигнатуре**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) во время проверки подлинности клиента для обработки сообщения проверки сертификата.</span><span class="sxs-lookup"><span data-stu-id="55dfb-132">Current implementations of the server side of the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) connection call the [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) function during the client authentication to process the certificate verify message.</span></span>

## <a name="requirements"></a><span data-ttu-id="55dfb-133">Требования</span><span class="sxs-lookup"><span data-stu-id="55dfb-133">Requirements</span></span>



| <span data-ttu-id="55dfb-134">Требование</span><span class="sxs-lookup"><span data-stu-id="55dfb-134">Requirement</span></span> | <span data-ttu-id="55dfb-135">Значение</span><span class="sxs-lookup"><span data-stu-id="55dfb-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="55dfb-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55dfb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="55dfb-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55dfb-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="55dfb-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55dfb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="55dfb-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55dfb-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="55dfb-140">Header</span><span class="sxs-lookup"><span data-stu-id="55dfb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="55dfb-141"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="55dfb-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="55dfb-142">DLL</span><span class="sxs-lookup"><span data-stu-id="55dfb-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55dfb-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55dfb-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

