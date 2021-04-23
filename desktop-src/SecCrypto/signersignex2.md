---
description: Метки и отметки времени задаются в указанном файле, что позволяет использовать несколько вложенных подписей.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: Функция SignerSignEx2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266097"
---
# <a name="signersignex2-function"></a><span data-ttu-id="9f6b4-103">Функция SignerSignEx2</span><span class="sxs-lookup"><span data-stu-id="9f6b4-103">SignerSignEx2 function</span></span>

<span data-ttu-id="9f6b4-104">Функция **SignerSignEx2** подписывает и помечает заметку времени для указанного файла, что позволяет использовать несколько вложенных подписей.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-104">The **SignerSignEx2** function signs and time stamps the specified file, allowing multiple nested signatures.</span></span>

> [!Note]  
> <span data-ttu-id="9f6b4-105">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="9f6b4-106">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9f6b4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f6b4-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="9f6b4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f6b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f6b4-109">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-110">Изменяет поведение этой функции.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="9f6b4-111">Если файл, который должен быть подписан, является переносимым исполняемым файлом (PE), это может быть ноль или сочетание одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="9f6b4-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9f6b4-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="9f6b4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9f6b4-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="9f6b4-114"><dt>**SPC \_ \_ \_ \_ \_ Флаг хэшей страниц исключенного PE**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="9f6b4-114"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="9f6b4-115">Исключение хэшей страниц при создании косвенных данных SIP для PE-файла.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-115">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="9f6b4-116">Этот флаг имеет приоритет над флагом **\_ \_ \_ \_ \_ флага "хэш-значения" хэша SPC Inc** .</span><span class="sxs-lookup"><span data-stu-id="9f6b4-116">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="9f6b4-117">Если не указано **ни \_ \_ \_ \_ \_ флага хэшей страниц исключенного PE** , ни флаг "хэши" для **\_ \_ \_ \_ хэшей \_ страницы** PE, то для этого параметра используется значение, заданное с помощью функции [**винтрустсетдефаултинклудепепажехашес**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) .</span><span class="sxs-lookup"><span data-stu-id="9f6b4-117">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="9f6b4-118">По умолчанию для этого параметра необходимо исключить хэши страниц при создании косвенных данных SIP для PE-файлов.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-118">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="9f6b4-119">Это значение определено в файле заголовка Мссип. h.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-119">This value is defined in the Mssip.h header file.</span></span><br/> <span data-ttu-id="9f6b4-120">**Windows Server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="9f6b4-121"><dt>**SPC \_ \_Флаг " \_ Импорт \_ \_ таблицы адреса \_**</dt> " ("Inc PE") <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9f6b4-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="9f6b4-122">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="9f6b4-123"><dt>**SPC \_ \_ \_ \_ \_ Флаг сведений об отладке Inc PE**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="9f6b4-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="9f6b4-124">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="9f6b4-125"><dt>**SPC \_ \_ \_ \_ Флаг ресурсов PE в среде Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9f6b4-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="9f6b4-126">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="9f6b4-127"><dt>**SPC \_ \_ \_ \_ \_ Флаги ХЭШЕЙ страниц PE "Inc**</dt> " <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9f6b4-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="9f6b4-128">Включайте хэши страниц при создании косвенных данных SIP для PE-файла.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="9f6b4-129">**Windows Server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> <span data-ttu-id="9f6b4-130">Это значение определено в файле заголовка Мссип. h.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-130">This value is defined in the Mssip.h header file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <span data-ttu-id="9f6b4-131"><dt>**Подпись \_ Добавить**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="9f6b4-131"><dt>**SIG\_APPEND**</dt> <dt>0x1000</dt></span></span> </dl>                                                                         | <span data-ttu-id="9f6b4-132">Подпись будет вложенной.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-132">The signature will be nested.</span></span> <span data-ttu-id="9f6b4-133">Если установить этот флаг перед добавлением подписи, то созданная подпись будет добавлена в качестве внешней подписи.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-133">If you set this flag before any signature has been added, the generated signature will be added as the outer signature.</span></span> <span data-ttu-id="9f6b4-134">Если этот флаг не установлен, созданная сигнатура заменит внешнюю подпись, удаляя все внутренние подписи.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-134">If you do not set this flag, the generated signature replaces the outer signature, deleting all inner signatures.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="9f6b4-135">*псубжектинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-135">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-136">Указатель на структуру [**\_ \_ сведений о субъекте-подписавшем**](signer-subject-info.md) , указывающий тему для подписывания.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-136">Pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b4-137">*псигнерцерт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-137">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-138">Указатель на структуру [**\_ сертификатов подписи**](signer-cert.md) , указывающую сертификат, используемый для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-138">Pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b4-139">*псигнатуреинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-139">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-140">Указатель на структуру [**\_ \_ сведений о сигнатуре**](signer-signature-info.md) для подписи, которая содержит сведения о цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-140">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b4-141">*ппровидеринфо* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-141">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-142">Указатель на структуру [**\_ \_ сведений о поставщике подписи**](signer-provider-info.md) , указывающий [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) и сведения о закрытом ключе, используемые для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-142">Pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="9f6b4-143">Если значение этого параметра равно **null**, параметр *псигнерцерт* должен указывать сертификат, связанный с CSP.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-143">If the value of this parameter is **NULL**, the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b4-144">*двтиместампфлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-144">*dwTimestampFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-145">Флаги, которые будут переданы в [**SignerTimeStampEx3**](signertimestampex3.md) , если параметр *пвсзттптиместамп* имеет значение, отличное от **null**.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-145">Flags that will be passed to [**SignerTimeStampEx3**](signertimestampex3.md) if the *pwszHttpTimeStamp* parameter is not **NULL**.</span></span> <span data-ttu-id="9f6b4-146">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-146">This can be one of the following values.</span></span>



| <span data-ttu-id="9f6b4-147">Значение</span><span class="sxs-lookup"><span data-stu-id="9f6b4-147">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="9f6b4-148">Значение</span><span class="sxs-lookup"><span data-stu-id="9f6b4-148">Meaning</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="9f6b4-149"><dt>**\_Метка времени подписи \_ AUTHENTICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6b4-149"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="9f6b4-150">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-150">Default value.</span></span> <span data-ttu-id="9f6b4-151">Указывает отметку времени Authenticode.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-151">Specifies an Authenticode timestamp.</span></span><br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="9f6b4-152"><dt>**\_Метка времени подписи \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6b4-152"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="9f6b4-153">Задает отметку времени RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-153">Specifies an RFC 3161 timestamp.</span></span><br/>                    |



 

<span data-ttu-id="9f6b4-154">Этот параметр пропускается, если параметр *пвсзттптиместамп* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-154">This parameter is ignored if the *pwszHttpTimeStamp* parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b4-155">*псзтиместампалгорисмоид* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-155">*pszTimestampAlgorithmOid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-156">Идентификатор объекта алгоритма, используемого для создания метки времени RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-156">Object identifier of the algorithm to be used for creating an RFC 3161 timestamp.</span></span> <span data-ttu-id="9f6b4-157">Этот параметр не учитывается для меток времени Authenticode.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-157">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b4-158">*пвсзттптиместамп* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-158">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-159">URL-адрес сервера отметок времени.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-159">URL of the time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b4-160">*псрекуест* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-160">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-161">Указатель на массив [**понятных структур \_ атрибутов**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) , которые добавляются в запрос на подписывание.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-161">Pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="9f6b4-162">Этот параметр пропускается, если параметр *пвсзттптиместамп* не содержит допустимого значения или имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-162">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value or is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b4-163">*псипдата* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-163">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-164">32-разрядное значение, передаваемое в функции SIP в качестве дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-164">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="9f6b4-165">Формат и содержимое этого объекта определяется поставщиком SIP.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-165">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b4-166">*ппсигнерконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-166">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-167">Адрес указателя на структуру [**\_ контекста подписавшего**](signer-context.md) , который содержит подписанный [*большой двоичный объект*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9f6b4-167">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="9f6b4-168">По завершении использования структуры **\_ контекста подписания** Освободите структуру **\_ контекста подписи** , вызвав функцию [**сигнерфрисигнерконтекст**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="9f6b4-168">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b4-169">*пкриптополици* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-169">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6b4-170">При наличии указателя на структуру [**\_ \_ \_ абзаца со строгой подписью сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) , содержащую параметры, используемые для проверки наличия строгих подписей.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-170">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="9f6b4-171">Если сертификат или его цепочка не проходят, файл не изменяется каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-171">If either a certificate or its chain does not pass, the file is not altered in any way.</span></span> <span data-ttu-id="9f6b4-172">Если URL-адрес передается в для указания центра меток времени (TSA), эта политика также применяется к метке времени.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-172">If a URL is passed in to specify a Time Stamping Authority (TSA), this policy is also applied to the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b4-173">*Сохраняется*</span><span class="sxs-lookup"><span data-stu-id="9f6b4-173">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6b4-174">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-174">Reserved.</span></span> <span data-ttu-id="9f6b4-175">Это значение должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-175">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f6b4-176">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f6b4-176">Return value</span></span>

<span data-ttu-id="9f6b4-177">Если функция завершается успешно, функция возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-177">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="9f6b4-178">Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-178">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="9f6b4-179">Возможные коды ошибок, возвращаемые этой функцией, включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="9f6b4-179">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="9f6b4-180">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="9f6b4-180">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



| <span data-ttu-id="9f6b4-181">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9f6b4-181">Return code</span></span>                                                                                  | <span data-ttu-id="9f6b4-182">Описание</span><span class="sxs-lookup"><span data-stu-id="9f6b4-182">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f6b4-183"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6b4-183"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9f6b4-184">Если для параметра *двтиместампфлагс* задана **\_ Метка времени \_ AUTHENTICODE**, нельзя присвоить параметру *dwFlags* значение « **\_ Добавление подписи**».</span><span class="sxs-lookup"><span data-stu-id="9f6b4-184">If you set the *dwTimestampFlags* parameter to **SIGNER\_TIMESTAMP\_AUTHENTICODE**, you cannot set the *dwFlags* parameter to **SIG\_APPEND**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9f6b4-185">Требования</span><span class="sxs-lookup"><span data-stu-id="9f6b4-185">Requirements</span></span>



| <span data-ttu-id="9f6b4-186">Требование</span><span class="sxs-lookup"><span data-stu-id="9f6b4-186">Requirement</span></span> | <span data-ttu-id="9f6b4-187">Значение</span><span class="sxs-lookup"><span data-stu-id="9f6b4-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6b4-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f6b4-188">Minimum supported client</span></span><br/> | <span data-ttu-id="9f6b4-189">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="9f6b4-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f6b4-190">Minimum supported server</span></span><br/> | <span data-ttu-id="9f6b4-191">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9f6b4-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9f6b4-192">DLL</span><span class="sxs-lookup"><span data-stu-id="9f6b4-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f6b4-193"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f6b4-193"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f6b4-194">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f6b4-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6b4-195">**сигнерсигн**</span><span class="sxs-lookup"><span data-stu-id="9f6b4-195">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="9f6b4-196">**сигнерсигнекс**</span><span class="sxs-lookup"><span data-stu-id="9f6b4-196">**SignerSignEx**</span></span>](signersignex.md)
</dt> <dt>

[<span data-ttu-id="9f6b4-197">**сигнерфрисигнерконтекст**</span><span class="sxs-lookup"><span data-stu-id="9f6b4-197">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
