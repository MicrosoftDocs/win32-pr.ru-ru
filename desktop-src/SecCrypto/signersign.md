---
description: Подписывает указанный файл.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: Функция Сигнерсигн
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683814"
---
# <a name="signersign-function"></a><span data-ttu-id="36387-103">Функция Сигнерсигн</span><span class="sxs-lookup"><span data-stu-id="36387-103">SignerSign function</span></span>

<span data-ttu-id="36387-104">Функция **сигнерсигн** подписывает указанный файл.</span><span class="sxs-lookup"><span data-stu-id="36387-104">The **SignerSign** function signs the specified file.</span></span>

> [!Note]  
> <span data-ttu-id="36387-105">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="36387-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="36387-106">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="36387-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="36387-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36387-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="36387-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="36387-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36387-109">*псубжектинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36387-109">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36387-110">Указатель на структуру [**\_ \_ сведений о субъекте-подписавшем**](signer-subject-info.md) , указывающий тему для подписывания.</span><span class="sxs-lookup"><span data-stu-id="36387-110">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="36387-111">*псигнерцерт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36387-111">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36387-112">Указатель на структуру [**\_ сертификата подписи**](signer-cert.md) , указывающий сертификат, используемый для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="36387-112">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="36387-113">*псигнатуреинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36387-113">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36387-114">Указатель на структуру [**\_ \_ сведений о сигнатуре**](signer-signature-info.md) для подписи, которая содержит сведения о цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="36387-114">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="36387-115">*ппровидеринфо* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="36387-115">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="36387-116">Указатель на структуру [**\_ \_ сведений о поставщике подписи**](signer-provider-info.md) , указывающий [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) и сведения о [*закрытом ключе*](../secgloss/p-gly.md) , используемые для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="36387-116">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and [*private key*](../secgloss/p-gly.md) information used to create the digital signature.</span></span>

<span data-ttu-id="36387-117">Если значение этого параметра равно **null**, то значение параметра *псигнерцерт* должно указывать сертификат, связанный с CSP.</span><span class="sxs-lookup"><span data-stu-id="36387-117">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="36387-118">*пвсзттптиместамп* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="36387-118">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="36387-119">URL-адрес сервера отметок времени.</span><span class="sxs-lookup"><span data-stu-id="36387-119">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="36387-120">*псрекуест* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="36387-120">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="36387-121">Указатель на массив [**понятных структур \_ атрибутов**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) , которые добавляются в запрос на подписывание.</span><span class="sxs-lookup"><span data-stu-id="36387-121">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="36387-122">Этот параметр пропускается, если параметр *пвсзттптиместамп* не содержит допустимого значения, отличного от **null**.</span><span class="sxs-lookup"><span data-stu-id="36387-122">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="36387-123">*псипдата* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="36387-123">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="36387-124">32-разрядное значение, передаваемое в функции SIP в качестве дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="36387-124">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="36387-125">Формат и содержимое этого объекта определяется поставщиком SIP.</span><span class="sxs-lookup"><span data-stu-id="36387-125">The format and content of this is defined by the SIP provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36387-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36387-126">Return value</span></span>

<span data-ttu-id="36387-127">Если функция завершается успешно, функция возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="36387-127">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="36387-128">Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="36387-128">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="36387-129">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="36387-129">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36387-130">Требования</span><span class="sxs-lookup"><span data-stu-id="36387-130">Requirements</span></span>



| <span data-ttu-id="36387-131">Требование</span><span class="sxs-lookup"><span data-stu-id="36387-131">Requirement</span></span> | <span data-ttu-id="36387-132">Значение</span><span class="sxs-lookup"><span data-stu-id="36387-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36387-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36387-133">Minimum supported client</span></span><br/> | <span data-ttu-id="36387-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="36387-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="36387-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36387-135">Minimum supported server</span></span><br/> | <span data-ttu-id="36387-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36387-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36387-137">DLL</span><span class="sxs-lookup"><span data-stu-id="36387-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36387-138"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36387-138"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36387-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36387-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36387-140">**сигнерсигнекс**</span><span class="sxs-lookup"><span data-stu-id="36387-140">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
