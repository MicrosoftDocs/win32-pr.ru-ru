---
description: SSL Возвращает ключ сеанса SSL или открытый эфемерный ключ в сериализованный большой двоичный объект.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: Функция Сслекспорткэй (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991615"
---
# <a name="sslexportkey-function"></a><span data-ttu-id="ce94c-103">Функция Сслекспорткэй</span><span class="sxs-lookup"><span data-stu-id="ce94c-103">SslExportKey function</span></span>

<span data-ttu-id="ce94c-104">Функция **сслекспорткэй** [*SSL*](/windows/desktop/SecGloss/s-gly) возвращает [*ключ сеанса*](/windows/desktop/SecGloss/s-gly) SSL или открытый эфемерный ключ в сериализованный [*большой двоичный объект*](/windows/desktop/SecGloss/b-gly).</span><span class="sxs-lookup"><span data-stu-id="ce94c-104">The **SslExportKey** function returns an [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) [*session key*](/windows/desktop/SecGloss/s-gly) or public ephemeral key into a serialized [*BLOB*](/windows/desktop/SecGloss/b-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce94c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce94c-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ce94c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce94c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce94c-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce94c-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce94c-108">Маркер экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="ce94c-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="ce94c-109">*hKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce94c-109">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce94c-110">Маркер экспортируемого ключа.</span><span class="sxs-lookup"><span data-stu-id="ce94c-110">The handle of the key to export.</span></span>

<span data-ttu-id="ce94c-111">Если ключ не указан, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ce94c-111">When you are not specifying a key, set this parameter to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="ce94c-112">Для получения маркера *hKey* вызывается функция [**сслопенприватекэй**](sslopenprivatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="ce94c-112">A *hKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="ce94c-113">Дескрипторы, полученные от функции [**нкриптопенкэй**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) , не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="ce94c-113">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce94c-114">*псзблобтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce94c-114">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce94c-115">Строка в Юникоде, заканчивающаяся нулем и содержащая идентификатор, указывающий тип большого двоичного объекта для экспорта.</span><span class="sxs-lookup"><span data-stu-id="ce94c-115">A null-terminated Unicode string that contains an identifier that specifies the type of BLOB to export.</span></span> <span data-ttu-id="ce94c-116">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ce94c-116">This can be one of the following values.</span></span>



| <span data-ttu-id="ce94c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ce94c-117">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="ce94c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ce94c-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="ce94c-119"><dt>**\_ \_ открытый \_ большой двоичный объект BCRYPT DH**</dt></span><span class="sxs-lookup"><span data-stu-id="ce94c-119"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="ce94c-120">Экспорт Diffie-Hellman [*открытого ключа*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="ce94c-120">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="ce94c-121">Буфер *пбаутпут* сразу же получает [**структуру \_ \_ \_ больших двоичных объектов ключа Диффи-Хелмана**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) , за которой следуют данные ключа.</span><span class="sxs-lookup"><span data-stu-id="ce94c-121">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="ce94c-122"><dt>**\_BLOB- \_ объект еккпублик BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="ce94c-122"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="ce94c-123">Экспорт открытого ключа шифрования на основе [*эллиптических кривых*](/windows/desktop/SecGloss/e-gly) (ECC).</span><span class="sxs-lookup"><span data-stu-id="ce94c-123">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) public key.</span></span> <span data-ttu-id="ce94c-124">Буфер *пбаутпут* сразу же получает [**структуру \_ \_ больших двоичных объектов екккэй BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) , за которой следуют данные ключа.</span><span class="sxs-lookup"><span data-stu-id="ce94c-124">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="ce94c-125"><dt>**\_ \_ большой двоичный объект непрозрачного ключа BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce94c-125"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="ce94c-126">Экспорт симметричного ключа в формате, характерном для одного [*поставщика служб шифрования*](/windows/desktop/SecGloss/c-gly) (CSP).</span><span class="sxs-lookup"><span data-stu-id="ce94c-126">Export a symmetric key in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="ce94c-127">Непрозрачные BLOB-объекты не передаются и должны быть импортированы с помощью того же *поставщика служб шифрования* (CSP), который создал большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="ce94c-127">Opaque BLOBs are not transferable and must be imported by using the same *cryptographic service provider* (CSP) that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="ce94c-128"><dt>**\_BLOB- \_ объект рсапублик BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="ce94c-128"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="ce94c-129">Экспорт открытого ключа RSA.</span><span class="sxs-lookup"><span data-stu-id="ce94c-129">Export an RSA public key.</span></span> <span data-ttu-id="ce94c-130">Буфер *пбаутпут* сразу же получает [**структуру \_ \_ больших двоичных объектов RSAKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) , за которой следуют данные ключа.</span><span class="sxs-lookup"><span data-stu-id="ce94c-130">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="ce94c-131">*пбаутпут* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="ce94c-131">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ce94c-132">Адрес буфера, который получает [*большой двоичный объект ключа*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="ce94c-132">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="ce94c-133">Параметр *кбаутпут* содержит размер этого буфера.</span><span class="sxs-lookup"><span data-stu-id="ce94c-133">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="ce94c-134">Если этот параметр имеет **значение NULL**, эта функция поместит требуемый размер (в байтах) в **DWORD** , на который указывает параметр *пкбресулт* .</span><span class="sxs-lookup"><span data-stu-id="ce94c-134">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ce94c-135">*кбаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce94c-135">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce94c-136">Размер (в байтах) буфера *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="ce94c-136">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ce94c-137">*пкбресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ce94c-137">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce94c-138">Адрес переменной **типа DWORD** , которая получает число байтов, скопированных в буфер *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="ce94c-138">The address of a **DWORD** variable that receives the number of bytes copied to the *pbOutput* buffer.</span></span> <span data-ttu-id="ce94c-139">Если при вызове функции для параметра *пбаутпут* задано **значение NULL** , то необходимый размер буфера *пбаутпут* в байтах возвращается в **DWORD** , на который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ce94c-139">If the *pbOutput* parameter is set to **NULL** when the function is called, the required size for the *pbOutput* buffer, in bytes, is returned in the **DWORD** pointed to by this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ce94c-140">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce94c-140">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce94c-141">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="ce94c-141">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce94c-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce94c-142">Return value</span></span>

<span data-ttu-id="ce94c-143">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="ce94c-143">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="ce94c-144">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="ce94c-144">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="ce94c-145">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="ce94c-145">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="ce94c-146">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="ce94c-146">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="ce94c-147">Описание</span><span class="sxs-lookup"><span data-stu-id="ce94c-147">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="ce94c-148">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ce94c-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="ce94c-149">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="ce94c-149">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce94c-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce94c-150">Remarks</span></span>

<span data-ttu-id="ce94c-151">Функция **сслекспорткэй** упрощает перенос ключей сеанса из одного процесса в другой, а также экспорт открытой части в эфемерный ключ.</span><span class="sxs-lookup"><span data-stu-id="ce94c-151">The **SslExportKey** function facilitates transporting session keys from one process to another as well as exporting the public portion an ephemeral key.</span></span>

<span data-ttu-id="ce94c-152">При экспорте ключей сеанса тип большого двоичного объекта является непрозрачным, а это означает, что формат большого двоичного объекта не имеет значения, если только функции **сслекспорткэй** и [**сслимпорткэй**](sslimportkey.md) могут интерпретировать его.</span><span class="sxs-lookup"><span data-stu-id="ce94c-152">When exporting session keys, the BLOB type is opaque, meaning that the format of the BLOB is irrelevant as long as both the **SslExportKey** and [**SslImportKey**](sslimportkey.md) functions can interpret it.</span></span>

<span data-ttu-id="ce94c-153">При экспорте открытой части эфемерного ключа тип большого двоичного объекта должен иметь соответствующий тип, например **NCrypt \_ DH \_ Public \_ BLOB** или **NCrypt \_ еккпублик \_ BLOB**.</span><span class="sxs-lookup"><span data-stu-id="ce94c-153">When exporting the public portion of an ephemeral key the BLOB type must be the appropriate type, such as **NCRYPT\_DH\_PUBLIC\_BLOB** or **NCRYPT\_ECCPUBLIC\_BLOB**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce94c-154">Требования</span><span class="sxs-lookup"><span data-stu-id="ce94c-154">Requirements</span></span>



| <span data-ttu-id="ce94c-155">Требование</span><span class="sxs-lookup"><span data-stu-id="ce94c-155">Requirement</span></span> | <span data-ttu-id="ce94c-156">Значение</span><span class="sxs-lookup"><span data-stu-id="ce94c-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce94c-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce94c-157">Minimum supported client</span></span><br/> | <span data-ttu-id="ce94c-158">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce94c-158">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ce94c-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce94c-159">Minimum supported server</span></span><br/> | <span data-ttu-id="ce94c-160">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce94c-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ce94c-161">Header</span><span class="sxs-lookup"><span data-stu-id="ce94c-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce94c-162"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce94c-162"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="ce94c-163">DLL</span><span class="sxs-lookup"><span data-stu-id="ce94c-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce94c-164"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce94c-164"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

