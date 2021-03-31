---
description: Подписывает указанный файл и возвращает указатель на подписанные данные.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: Функция Сигнерсигнекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9944a09459219ccac74f5fafc9424e9f85a01112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812821"
---
# <a name="signersignex-function"></a><span data-ttu-id="29798-103">Функция Сигнерсигнекс</span><span class="sxs-lookup"><span data-stu-id="29798-103">SignerSignEx function</span></span>

<span data-ttu-id="29798-104">Функция **сигнерсигнекс** подписывает указанный файл и возвращает указатель на подписанные данные.</span><span class="sxs-lookup"><span data-stu-id="29798-104">The **SignerSignEx** function signs the specified file and returns a pointer to the signed data.</span></span>

> [!Note]  
> <span data-ttu-id="29798-105">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="29798-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="29798-106">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="29798-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="29798-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29798-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="29798-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="29798-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29798-109">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29798-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29798-110">Изменяет поведение этой функции.</span><span class="sxs-lookup"><span data-stu-id="29798-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="29798-111">Если файл, который должен быть подписан, является переносимым исполняемым файлом (PE), это может быть ноль или сочетание одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="29798-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="29798-112">Эти идентификаторы определены в Мссип. h.</span><span class="sxs-lookup"><span data-stu-id="29798-112">These identifiers are defined in Mssip.h.</span></span>



| <span data-ttu-id="29798-113">Значение</span><span class="sxs-lookup"><span data-stu-id="29798-113">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="29798-114">Значение</span><span class="sxs-lookup"><span data-stu-id="29798-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="29798-115"><dt>**SPC \_ \_ \_ \_ \_ Флаг хэшей страниц исключенного PE**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="29798-115"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="29798-116">Исключение хэшей страниц при создании косвенных данных SIP для PE-файла.</span><span class="sxs-lookup"><span data-stu-id="29798-116">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="29798-117">Этот флаг имеет приоритет над флагом **\_ \_ \_ \_ \_ флага "хэш-значения" хэша SPC Inc** .</span><span class="sxs-lookup"><span data-stu-id="29798-117">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="29798-118">Если не указано **ни \_ \_ \_ \_ \_ флага хэшей страниц исключенного PE** , ни флаг "хэши" для **\_ \_ \_ \_ хэшей \_ страницы** PE, то для этого параметра используется значение, заданное с помощью функции [**винтрустсетдефаултинклудепепажехашес**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) .</span><span class="sxs-lookup"><span data-stu-id="29798-118">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="29798-119">По умолчанию для этого параметра необходимо исключить хэши страниц при создании косвенных данных SIP для PE-файлов.</span><span class="sxs-lookup"><span data-stu-id="29798-119">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="29798-120">**Windows Server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="29798-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="29798-121"><dt>**SPC \_ \_Флаг " \_ Импорт \_ \_ таблицы адреса \_**</dt> " ("Inc PE") <dt></dt></span><span class="sxs-lookup"><span data-stu-id="29798-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="29798-122">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="29798-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="29798-123"><dt>**SPC \_ \_ \_ \_ \_ Флаг сведений об отладке Inc PE**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="29798-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="29798-124">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="29798-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="29798-125"><dt>**SPC \_ \_ \_ \_ Флаг ресурсов PE в среде Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="29798-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="29798-126">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="29798-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="29798-127"><dt>**SPC \_ \_ \_ \_ \_ Флаги ХЭШЕЙ страниц PE "Inc**</dt> " <dt></dt></span><span class="sxs-lookup"><span data-stu-id="29798-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="29798-128">Включайте хэши страниц при создании косвенных данных SIP для PE-файла.</span><span class="sxs-lookup"><span data-stu-id="29798-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="29798-129">**Windows Server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="29798-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="29798-130">*псубжектинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29798-130">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29798-131">Указатель на структуру [**\_ \_ сведений о субъекте-подписавшем**](signer-subject-info.md) , указывающий тему для подписывания.</span><span class="sxs-lookup"><span data-stu-id="29798-131">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="29798-132">*псигнерцерт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29798-132">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29798-133">Указатель на структуру [**\_ сертификата подписи**](signer-cert.md) , указывающий сертификат, используемый для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="29798-133">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="29798-134">*псигнатуреинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29798-134">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29798-135">Указатель на структуру [**\_ \_ сведений о сигнатуре**](signer-signature-info.md) для подписи, которая содержит сведения о цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="29798-135">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="29798-136">*ппровидеринфо* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="29798-136">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29798-137">Указатель на структуру [**\_ \_ сведений о поставщике подписи**](signer-provider-info.md) , указывающий [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) и сведения о закрытом ключе, используемые для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="29798-137">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="29798-138">Если значение этого параметра равно **null**, то значение параметра *псигнерцерт* должно указывать сертификат, связанный с CSP.</span><span class="sxs-lookup"><span data-stu-id="29798-138">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="29798-139">*пвсзттптиместамп* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="29798-139">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29798-140">URL-адрес сервера отметок времени.</span><span class="sxs-lookup"><span data-stu-id="29798-140">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="29798-141">*псрекуест* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="29798-141">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29798-142">Указатель на массив [**понятных структур \_ атрибутов**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) , которые добавляются в запрос на подписывание.</span><span class="sxs-lookup"><span data-stu-id="29798-142">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="29798-143">Этот параметр пропускается, если параметр *пвсзттптиместамп* не содержит допустимого значения, отличного от **null**.</span><span class="sxs-lookup"><span data-stu-id="29798-143">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="29798-144">*псипдата* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="29798-144">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29798-145">32-разрядное значение, передаваемое в функции SIP в качестве дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="29798-145">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="29798-146">Формат и содержимое этого объекта определяется поставщиком SIP.</span><span class="sxs-lookup"><span data-stu-id="29798-146">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="29798-147">*ппсигнерконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="29798-147">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29798-148">Адрес указателя на структуру [**\_ контекста подписавшего**](signer-context.md) , который содержит подписанный [*большой двоичный объект*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="29798-148">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="29798-149">По завершении использования структуры **\_ контекста подписания** Освободите структуру **\_ контекста подписи** , вызвав функцию [**сигнерфрисигнерконтекст**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="29798-149">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29798-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29798-150">Return value</span></span>

<span data-ttu-id="29798-151">Если функция завершается успешно, функция возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="29798-151">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="29798-152">Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="29798-152">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="29798-153">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="29798-153">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29798-154">Требования</span><span class="sxs-lookup"><span data-stu-id="29798-154">Requirements</span></span>



| <span data-ttu-id="29798-155">Требование</span><span class="sxs-lookup"><span data-stu-id="29798-155">Requirement</span></span> | <span data-ttu-id="29798-156">Значение</span><span class="sxs-lookup"><span data-stu-id="29798-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29798-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29798-157">Minimum supported client</span></span><br/> | <span data-ttu-id="29798-158">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="29798-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="29798-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29798-159">Minimum supported server</span></span><br/> | <span data-ttu-id="29798-160">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="29798-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="29798-161">DLL</span><span class="sxs-lookup"><span data-stu-id="29798-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29798-162"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29798-162"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29798-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29798-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29798-164">**сигнерсигн**</span><span class="sxs-lookup"><span data-stu-id="29798-164">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="29798-165">**сигнерфрисигнерконтекст**</span><span class="sxs-lookup"><span data-stu-id="29798-165">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
