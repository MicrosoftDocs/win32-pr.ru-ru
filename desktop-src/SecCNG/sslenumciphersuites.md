---
description: Перечисляет комплекты шифров, поддерживаемые поставщиком протокола протокола SSL (SSL).
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: Функция СсленумЦиферсуитес (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345042"
---
# <a name="sslenumciphersuites-function"></a><span data-ttu-id="86a0d-103">Функция СсленумЦиферсуитес</span><span class="sxs-lookup"><span data-stu-id="86a0d-103">SslEnumCipherSuites function</span></span>

<span data-ttu-id="86a0d-104">Функция **ссленумЦиферсуитес** перечисляет комплекты шифров, [*SSL*](/windows/desktop/SecGloss/s-gly) поддерживаемые поставщиком протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="86a0d-104">The **SslEnumCipherSuites** function enumerates the cipher suites supported by a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="86a0d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86a0d-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="86a0d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86a0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86a0d-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86a0d-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86a0d-108">Маркер экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="86a0d-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="86a0d-109">*хприватекэй* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="86a0d-109">*hPrivateKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86a0d-110">Маркер [*закрытого ключа*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="86a0d-110">The handle of a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="86a0d-111">Если указан закрытый ключ, **ссленумЦиферсуитес** перечисляет комплекты шифров, совместимые с закрытым ключом.</span><span class="sxs-lookup"><span data-stu-id="86a0d-111">When a private key is specified, **SslEnumCipherSuites** enumerates the cipher suites that are compatible with the private key.</span></span> <span data-ttu-id="86a0d-112">Например, если закрытый ключ является ключом DSS, \_ возвращаются только комплекты шифров DSS дхе.</span><span class="sxs-lookup"><span data-stu-id="86a0d-112">For example, if the private key is a DSS key, then only the DSS\_DHE cipher suites are returned.</span></span> <span data-ttu-id="86a0d-113">Если закрытый ключ является ключом RSA, но не поддерживает операции расшифровки RAW, комплекты шифров SSL2 не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="86a0d-113">If the private key is an RSA key, but it does not support raw decryption operations, then the SSL2 cipher suites are not returned.</span></span>

<span data-ttu-id="86a0d-114">Присвойте этому параметру **значение NULL** , если не указан закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="86a0d-114">Set this parameter to **NULL** when you are not specifying a private key.</span></span>

> [!Note]  
> <span data-ttu-id="86a0d-115">Для получения маркера *хприватекэй* вызывается функция [**сслопенприватекэй**](sslopenprivatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="86a0d-115">A *hPrivateKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="86a0d-116">Дескрипторы, полученные от функции [**нкриптопенкэй**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) , не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="86a0d-116">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="86a0d-117">*ппЦиферсуите* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="86a0d-117">*ppCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86a0d-118">Указатель на структуру [**\_ \_ \_ набора шифров NCRYPT SSL**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) для получения адреса следующего комплекта шифров в списке.</span><span class="sxs-lookup"><span data-stu-id="86a0d-118">A pointer to a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure to receive the address of the next cipher suite in the list.</span></span>

</dd> <dt>

<span data-ttu-id="86a0d-119">*ппенумстате* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="86a0d-119">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86a0d-120">Указатель на буфер, указывающий текущую позиции в списке комплектов шифров.</span><span class="sxs-lookup"><span data-stu-id="86a0d-120">A pointer to a buffer that indicates the current position in the list of cipher suites.</span></span>

<span data-ttu-id="86a0d-121">Установите указатель на **null** при первом вызове **ссленумЦиферсуитес**.</span><span class="sxs-lookup"><span data-stu-id="86a0d-121">Set the pointer to **NULL** on the first call to **SslEnumCipherSuites**.</span></span> <span data-ttu-id="86a0d-122">При каждом последующем вызове передайте неизмененное значение обратно в **ссленумЦиферсуитес**.</span><span class="sxs-lookup"><span data-stu-id="86a0d-122">On each subsequent call, pass the unmodified value back to **SslEnumCipherSuites**.</span></span>

<span data-ttu-id="86a0d-123">Если больше нет доступных наборов шифров, следует освободить *ппенумстате* , вызвав функцию [**сслфрибуффер**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="86a0d-123">When there are no more cipher suites available, you should free *ppEnumState* by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="86a0d-124">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86a0d-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86a0d-125">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="86a0d-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86a0d-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86a0d-126">Return value</span></span>

<span data-ttu-id="86a0d-127">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="86a0d-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="86a0d-128">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="86a0d-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="86a0d-129">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="86a0d-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="86a0d-130">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="86a0d-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="86a0d-131">Описание</span><span class="sxs-lookup"><span data-stu-id="86a0d-131">Description</span></span>                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86a0d-132">Не <dt>**превышать \_ НЕТ \_**</dt> <dt>0x8009000EL</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="86a0d-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>      | <span data-ttu-id="86a0d-133">Недостаточно памяти для выделения необходимых буферов.</span><span class="sxs-lookup"><span data-stu-id="86a0d-133">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="86a0d-134">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="86a0d-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="86a0d-135">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="86a0d-135">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="86a0d-136">Не <dt>**превышать \_ Больше \_ нет \_ элементов**</dt> <dt>0x8009002AL</dt></span><span class="sxs-lookup"><span data-stu-id="86a0d-136"><dt>**NTE\_NO\_MORE\_ITEMS**</dt> <dt>0x8009002AL</dt></span></span> </dl> | <span data-ttu-id="86a0d-137">Дополнительные комплекты шифров не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="86a0d-137">No additional cipher suites are supported.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="86a0d-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86a0d-138">Remarks</span></span>

<span data-ttu-id="86a0d-139">Чтобы перечислить все комплекты шифров, поддерживаемые поставщиком SSL, вызовите функцию **ссленумЦиферсуитес** в цикле до тех пор, пока не будет возвращено **\_ \_ больше \_ элементов** .</span><span class="sxs-lookup"><span data-stu-id="86a0d-139">To enumerate all cipher suites supported by the SSL provider, call the **SslEnumCipherSuites** function in a loop until **NTE\_NO\_MORE\_ITEMS** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="86a0d-140">Требования</span><span class="sxs-lookup"><span data-stu-id="86a0d-140">Requirements</span></span>



| <span data-ttu-id="86a0d-141">Требование</span><span class="sxs-lookup"><span data-stu-id="86a0d-141">Requirement</span></span> | <span data-ttu-id="86a0d-142">Значение</span><span class="sxs-lookup"><span data-stu-id="86a0d-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86a0d-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86a0d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="86a0d-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86a0d-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="86a0d-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86a0d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="86a0d-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86a0d-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="86a0d-147">Header</span><span class="sxs-lookup"><span data-stu-id="86a0d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="86a0d-148"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="86a0d-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="86a0d-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="86a0d-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="86a0d-150"><dt>NCrypt. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86a0d-150"><dt>Ncrypt.lib</dt></span></span> </dl>    |
| <span data-ttu-id="86a0d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="86a0d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86a0d-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86a0d-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="86a0d-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86a0d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86a0d-154">**NCRYPT \_ для \_ набора шифров SSL \_**</span><span class="sxs-lookup"><span data-stu-id="86a0d-154">**NCRYPT\_SSL\_CIPHER\_SUITE**</span></span>](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

