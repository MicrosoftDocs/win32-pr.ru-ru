---
description: Возвращает маркер для хеша подтверждения, используемого для проверки подлинности клиента.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: Функция Сслкреатеклиентаусхаш (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662866"
---
# <a name="sslcreateclientauthhash-function"></a><span data-ttu-id="7b2a3-103">Функция Сслкреатеклиентаусхаш</span><span class="sxs-lookup"><span data-stu-id="7b2a3-103">SslCreateClientAuthHash function</span></span>

<span data-ttu-id="7b2a3-104">Функция **сслкреатеклиентаусхаш** Извлекает маркер для [*хеша*](/windows/desktop/SecGloss/h-gly) подтверждения, который используется для проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-104">The **SslCreateClientAuthHash** function retrieves a handle to the handshake [*hash*](/windows/desktop/SecGloss/h-gly) that is used for client authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b2a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b2a3-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7b2a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b2a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b2a3-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b2a3-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2a3-108">Маркер экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="7b2a3-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="7b2a3-109">*фхандшакехаш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7b2a3-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2a3-110">Указатель на переменную **\_ хэш- \_ обработчика NCRYPT** для получения обработчика хэша.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-110">A pointer to an **NCRYPT\_HASH\_HANDLE** variable to receive the hash handle.</span></span>

</dd> <dt>

<span data-ttu-id="7b2a3-111">*двпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b2a3-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2a3-112">Одно из значений [**идентификатора протокола поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="7b2a3-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="7b2a3-113">*двЦиферсуите* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b2a3-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2a3-114">Один из значений [**идентификатора комплекта шифров поставщика CNG SSL**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="7b2a3-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="7b2a3-115">*псзашалгид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b2a3-115">*pszHashAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2a3-116">Одно из значений [**идентификаторов алгоритма CNG**](cng-algorithm-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="7b2a3-116">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) values.</span></span>

</dd> <dt>

<span data-ttu-id="7b2a3-117">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b2a3-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2a3-118">Этот параметр зарезервирован для будущего использования и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-118">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b2a3-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b2a3-119">Return value</span></span>

<span data-ttu-id="7b2a3-120">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="7b2a3-121">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="7b2a3-122">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="7b2a3-123">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="7b2a3-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="7b2a3-124">Описание</span><span class="sxs-lookup"><span data-stu-id="7b2a3-124">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b2a3-125">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7b2a3-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="7b2a3-126">Параметр *хсслпровидер* содержит недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-126">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="7b2a3-127">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="7b2a3-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="7b2a3-128">Параметр *фхандшакехаш* имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-128">The *phHandshakeHash* parameter is set to **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="7b2a3-129">Не <dt>**превышать \_ НЕ \_ поддерживается**</dt> <dt>0x80090029L</dt></span><span class="sxs-lookup"><span data-stu-id="7b2a3-129"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="7b2a3-130">Выбранная функция не поддерживается в указанной версии интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-130">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="7b2a3-131">Не <dt>**превышать \_ НЕТ \_**</dt> <dt>0x8009000EL</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="7b2a3-131"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="7b2a3-132">Недостаточно памяти для выделения буферов.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-132">Insufficient memory to allocate buffers.</span></span><br/>                                          |
| <dl> <span data-ttu-id="7b2a3-133">Не <dt>**превышать \_ Неправильные \_ Флаги**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="7b2a3-133"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="7b2a3-134">Параметр *dwFlags* должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-134">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="7b2a3-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b2a3-135">Remarks</span></span>

<span data-ttu-id="7b2a3-136">Функция **сслкреатеклиентаусхаш** вызывается для [*протокола*](/windows/desktop/SecGloss/t-gly) TLS 1,2 или более поздней версии для создания хэш-объектов, используемых для хэширования сообщений подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-136">The **SslCreateClientAuthHash** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.2 or later conversations to create hash objects that are used to hash handshake messages.</span></span> <span data-ttu-id="7b2a3-137">Он вызывается один раз для каждого возможного [*алгоритма хэширования*](/windows/desktop/SecGloss/h-gly) , который может использоваться в сигнатуре проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="7b2a3-137">It is called once for each possible [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that can be used in the client authentication signature.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b2a3-138">Требования</span><span class="sxs-lookup"><span data-stu-id="7b2a3-138">Requirements</span></span>



| <span data-ttu-id="7b2a3-139">Требование</span><span class="sxs-lookup"><span data-stu-id="7b2a3-139">Requirement</span></span> | <span data-ttu-id="7b2a3-140">Значение</span><span class="sxs-lookup"><span data-stu-id="7b2a3-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b2a3-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b2a3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7b2a3-142">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7b2a3-142">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7b2a3-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b2a3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7b2a3-144">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b2a3-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b2a3-145">Header</span><span class="sxs-lookup"><span data-stu-id="7b2a3-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b2a3-146"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b2a3-146"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="7b2a3-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7b2a3-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b2a3-148"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b2a3-148"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

