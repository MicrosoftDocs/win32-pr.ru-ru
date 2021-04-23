---
description: Импортирует ключ SSL в поставщик протокола SSL.
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: Функция Сслимпорткэй (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8bf1b03fd5d51974db3676dcdbccc2a2b0fa4323
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662862"
---
# <a name="sslimportkey-function"></a><span data-ttu-id="8cef5-103">Функция Сслимпорткэй</span><span class="sxs-lookup"><span data-stu-id="8cef5-103">SslImportKey function</span></span>

<span data-ttu-id="8cef5-104">Функция **сслимпорткэй** импортирует ключ [*SSL*](/windows/desktop/SecGloss/s-gly) в поставщик протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="8cef5-104">The **SslImportKey** function imports a key into the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cef5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cef5-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8cef5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cef5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cef5-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cef5-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cef5-108">Обработчик для экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="8cef5-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="8cef5-109">*фкэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8cef5-109">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cef5-110">Указатель на маркер [*криптографического ключа*](/windows/desktop/SecGloss/c-gly) для получения импортируемого ключа.</span><span class="sxs-lookup"><span data-stu-id="8cef5-110">A pointer to the handle of the [*cryptographic key*](/windows/desktop/SecGloss/c-gly) to receive the imported key.</span></span>

</dd> <dt>

<span data-ttu-id="8cef5-111">*псзблобтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cef5-111">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cef5-112">Строка в Юникоде, заканчивающаяся нулем и содержащая идентификатор, указывающий тип [*большого двоичного объекта*](/windows/desktop/SecGloss/b-gly) , который содержится в буфере *пбинпут* .</span><span class="sxs-lookup"><span data-stu-id="8cef5-112">A null-terminated Unicode string that contains an identifier that specifies the type of [*BLOB*](/windows/desktop/SecGloss/b-gly) that is contained in the *pbInput* buffer.</span></span> <span data-ttu-id="8cef5-113">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8cef5-113">This can be one of the following values.</span></span>



| <span data-ttu-id="8cef5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8cef5-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="8cef5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8cef5-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="8cef5-116"><dt>**\_ \_ открытый \_ большой двоичный объект BCRYPT DH**</dt></span><span class="sxs-lookup"><span data-stu-id="8cef5-116"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="8cef5-117">Экспорт Diffie-Hellman [*открытого ключа*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="8cef5-117">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="8cef5-118">Буфер *пбаутпут* сразу же получает [**структуру \_ \_ \_ больших двоичных объектов ключа Диффи-Хелмана**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) , за которой следуют данные ключа.</span><span class="sxs-lookup"><span data-stu-id="8cef5-118">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="8cef5-119"><dt>**\_BLOB- \_ объект еккпублик BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="8cef5-119"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="8cef5-120">Экспорт [*открытого ключа*](/windows/desktop/SecGloss/p-gly)шифрования на основе [*эллиптических кривых*](/windows/desktop/SecGloss/e-gly) (ECC).</span><span class="sxs-lookup"><span data-stu-id="8cef5-120">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="8cef5-121">Буфер *пбаутпут* сразу же получает [**структуру \_ \_ больших двоичных объектов екккэй BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) , за которой следуют данные ключа.</span><span class="sxs-lookup"><span data-stu-id="8cef5-121">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="8cef5-122"><dt>**\_ \_ большой двоичный объект непрозрачного ключа BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8cef5-122"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="8cef5-123">Экспорт [*симметричного ключа*](/windows/desktop/SecGloss/s-gly) в формате, характерном для одного [*поставщика служб шифрования*](/windows/desktop/SecGloss/c-gly) (CSP).</span><span class="sxs-lookup"><span data-stu-id="8cef5-123">Export a [*symmetric key*](/windows/desktop/SecGloss/s-gly) in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="8cef5-124">Непрозрачные BLOB-объекты не передаются и должны быть импортированы с помощью того же CSP, который создал большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="8cef5-124">Opaque BLOBs are not transferable and must be imported by using the same CSP that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="8cef5-125"><dt>**\_BLOB- \_ объект рсапублик BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="8cef5-125"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="8cef5-126">Экспорт открытого ключа [*RSA*](/windows/desktop/SecGloss/r-gly) .</span><span class="sxs-lookup"><span data-stu-id="8cef5-126">Export an [*RSA*](/windows/desktop/SecGloss/r-gly) public key.</span></span> <span data-ttu-id="8cef5-127">Буфер *пбаутпут* сразу же получает [**структуру \_ \_ больших двоичных объектов RSAKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) , за которой следуют данные ключа.</span><span class="sxs-lookup"><span data-stu-id="8cef5-127">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="8cef5-128">*пбкэйблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cef5-128">*pbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cef5-129">Указатель на буфер, содержащий [*большой двоичный объект ключа*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="8cef5-129">A pointer to the buffer that contains the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span>

</dd> <dt>

<span data-ttu-id="8cef5-130">*кбкэйблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cef5-130">*cbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cef5-131">Размер (в байтах) буфера *пбкэйблоб* .</span><span class="sxs-lookup"><span data-stu-id="8cef5-131">The size, in bytes, of the *pbKeyBlob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8cef5-132">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cef5-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cef5-133">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="8cef5-133">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cef5-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cef5-134">Return value</span></span>

<span data-ttu-id="8cef5-135">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8cef5-135">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="8cef5-136">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="8cef5-136">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="8cef5-137">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="8cef5-137">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="8cef5-138">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="8cef5-138">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="8cef5-139">Описание</span><span class="sxs-lookup"><span data-stu-id="8cef5-139">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8cef5-140">Не <dt>**превышать \_ НЕТ \_**</dt> <dt>0x8009000EL</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="8cef5-140"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="8cef5-141">Недостаточно памяти для выделения необходимых буферов.</span><span class="sxs-lookup"><span data-stu-id="8cef5-141">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="8cef5-142">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8cef5-142"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="8cef5-143">Недопустимый маркер *хсслпровидер* .</span><span class="sxs-lookup"><span data-stu-id="8cef5-143">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="8cef5-144">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="8cef5-144"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="8cef5-145">Параметр *фкэй* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8cef5-145">The *phKey* parameter is **NULL**.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="8cef5-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8cef5-146">Remarks</span></span>

<span data-ttu-id="8cef5-147">Функцию **сслимпорткэй** можно использовать для импорта ключей сеанса в рамках процесса передачи ключей сеанса из одного процесса в другой.</span><span class="sxs-lookup"><span data-stu-id="8cef5-147">You can use the **SslImportKey** function to import session keys as a part of the process of transferring session keys from one process to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cef5-148">Требования</span><span class="sxs-lookup"><span data-stu-id="8cef5-148">Requirements</span></span>



| <span data-ttu-id="8cef5-149">Требование</span><span class="sxs-lookup"><span data-stu-id="8cef5-149">Requirement</span></span> | <span data-ttu-id="8cef5-150">Значение</span><span class="sxs-lookup"><span data-stu-id="8cef5-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cef5-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8cef5-151">Minimum supported client</span></span><br/> | <span data-ttu-id="8cef5-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8cef5-152">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8cef5-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8cef5-153">Minimum supported server</span></span><br/> | <span data-ttu-id="8cef5-154">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8cef5-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8cef5-155">Header</span><span class="sxs-lookup"><span data-stu-id="8cef5-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cef5-156"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cef5-156"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="8cef5-157">DLL</span><span class="sxs-lookup"><span data-stu-id="8cef5-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cef5-158"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cef5-158"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

