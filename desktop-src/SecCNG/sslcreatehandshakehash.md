---
description: Получает хэш-маркер, используемый для хэширования сообщений подтверждения.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Функция Сслкреатехандшакехаш (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662864"
---
# <a name="sslcreatehandshakehash-function"></a><span data-ttu-id="dbd1d-103">Функция Сслкреатехандшакехаш</span><span class="sxs-lookup"><span data-stu-id="dbd1d-103">SslCreateHandshakeHash function</span></span>

<span data-ttu-id="dbd1d-104">Функция **сслкреатехандшакехаш** Получает хэш-маркер, используемый для хэширования сообщений подтверждения.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-104">The **SslCreateHandshakeHash** function obtains a hash handle that is used to hash handshake messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbd1d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbd1d-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="dbd1d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbd1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbd1d-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbd1d-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd1d-108">Маркер экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="dbd1d-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="dbd1d-109">*фхандшакехаш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dbd1d-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd1d-110">Хэш-маркер, который может быть передан другим функциям поставщика SSL.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-110">A hash handle that can be passed to other SSL provider functions.</span></span>

</dd> <dt>

<span data-ttu-id="dbd1d-111">*двпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbd1d-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd1d-112">Одно из значений [**идентификатора протокола поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="dbd1d-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

> [!Note]  
> <span data-ttu-id="dbd1d-113">Эта функция не используется с протоколом SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-113">This function is not used with the SSL 2.0 protocol.</span></span>

 

</dd> <dt>

<span data-ttu-id="dbd1d-114">*двЦиферсуите* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbd1d-114">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd1d-115">Один из значений [**идентификатора комплекта шифров поставщика CNG SSL**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="dbd1d-115">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="dbd1d-116">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbd1d-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd1d-117">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-117">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbd1d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbd1d-118">Return value</span></span>

<span data-ttu-id="dbd1d-119">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-119">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="dbd1d-120">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-120">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="dbd1d-121">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-121">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="dbd1d-122">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="dbd1d-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="dbd1d-123">Описание</span><span class="sxs-lookup"><span data-stu-id="dbd1d-123">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="dbd1d-124">Не <dt>**превышать \_ НЕТ \_**</dt> <dt>0x8009000EL</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="dbd1d-124"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="dbd1d-125">Недостаточно памяти для выделения буфера хэша.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-125">There is insufficient memory to allocate the hash buffer.</span></span><br/> |
| <dl> <span data-ttu-id="dbd1d-126">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dbd1d-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="dbd1d-127">Недопустимый маркер *хсслпровидер* .</span><span class="sxs-lookup"><span data-stu-id="dbd1d-127">The *hSslProvider* handle is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="dbd1d-128">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="dbd1d-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="dbd1d-129">*Фхандшакехаш* имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-129">The *phHandshakeHash* is null.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="dbd1d-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbd1d-130">Remarks</span></span>

<span data-ttu-id="dbd1d-131">Функция **сслкреатехандшакехаш** является одной из трех функций, используемых для создания хэша, используемого во время подтверждения SSL.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-131">The **SslCreateHandshakeHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="dbd1d-132">Для получения обработчика хэша вызывается функция **сслкреатехандшакехаш** .</span><span class="sxs-lookup"><span data-stu-id="dbd1d-132">The **SslCreateHandshakeHash** function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="dbd1d-133">Функция [**сслхашхандшаке**](sslhashhandshake.md) вызывается любое количество раз с обработчиком хэша для добавления данных в хэш.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-133">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="dbd1d-134">Функция [**сслкомпутефинишедхаш**](sslcomputefinishedhash.md) вызывается с хэш-маркером для получения дайджеста хэшированных данных.</span><span class="sxs-lookup"><span data-stu-id="dbd1d-134">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbd1d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="dbd1d-135">Requirements</span></span>



| <span data-ttu-id="dbd1d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="dbd1d-136">Requirement</span></span> | <span data-ttu-id="dbd1d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="dbd1d-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbd1d-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbd1d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dbd1d-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbd1d-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dbd1d-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbd1d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dbd1d-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dbd1d-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dbd1d-142">Header</span><span class="sxs-lookup"><span data-stu-id="dbd1d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbd1d-143"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbd1d-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="dbd1d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dbd1d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbd1d-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbd1d-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

