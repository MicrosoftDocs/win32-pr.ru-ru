---
description: Помечает время указанной темой и поддерживает задание меток времени для нескольких подписей.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: Функция SignerTimeStampEx3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143411"
---
# <a name="signertimestampex3-function"></a><span data-ttu-id="dbaad-103">Функция SignerTimeStampEx3</span><span class="sxs-lookup"><span data-stu-id="dbaad-103">SignerTimeStampEx3 function</span></span>

<span data-ttu-id="dbaad-104">Функция **SignerTimeStampEx3** помечает указанную тему и поддерживает задание меток времени для нескольких подписей.</span><span class="sxs-lookup"><span data-stu-id="dbaad-104">The **SignerTimeStampEx3** function time stamps the specified subject and supports setting time stamps on multiple signatures.</span></span>

> [!Note]  
> <span data-ttu-id="dbaad-105">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="dbaad-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="dbaad-106">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="dbaad-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="dbaad-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbaad-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="dbaad-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbaad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbaad-109">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbaad-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbaad-110">Флаг, указывающий тип создаваемой метки времени.</span><span class="sxs-lookup"><span data-stu-id="dbaad-110">Flag that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="dbaad-111">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="dbaad-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="dbaad-112">Значения являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="dbaad-112">The values are mutually exclusive.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dbaad-113">Значение</span><span class="sxs-lookup"><span data-stu-id="dbaad-113">Value</span></span></th>
<th><span data-ttu-id="dbaad-114">Значение</span><span class="sxs-lookup"><span data-stu-id="dbaad-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="dbaad-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dbaad-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="dbaad-116">Задает отметку времени Authenticode.</span><span class="sxs-lookup"><span data-stu-id="dbaad-116">Specifies an Authenticode time stamp.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dbaad-117">Authenticode больше не является предпочтительным типом метки времени.</span><span class="sxs-lookup"><span data-stu-id="dbaad-117">Authenticode is no longer the preferred type of time stamp.</span></span> <span data-ttu-id="dbaad-118">Поддержка меток времени Authenticode может быть удалена в будущем.</span><span class="sxs-lookup"><span data-stu-id="dbaad-118">Support for Authenticode time stamps may be removed in the future.</span></span> <span data-ttu-id="dbaad-119">Вместо этого рекомендуется использовать RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="dbaad-119">We recommend that you use RFC 3161 instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="dbaad-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dbaad-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="dbaad-121">Задает отметку времени, совместимую с RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="dbaad-121">Specifies an RFC 3161–compliant time stamp.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="dbaad-122">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbaad-122">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbaad-123">Указывает порядковый номер подписи, в которую будет добавлена метка времени.</span><span class="sxs-lookup"><span data-stu-id="dbaad-123">Specifies the sequence number of the signature to which the timestamp will be added.</span></span> <span data-ttu-id="dbaad-124">Если это значение равно нулю (0), внешняя подпись будет отметкой времени.</span><span class="sxs-lookup"><span data-stu-id="dbaad-124">If this value is zero (0), the outer signature will be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="dbaad-125">*псубжектинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbaad-125">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbaad-126">Адрес структуры [**\_ \_ сведений о субъекте-подписывания**](signer-subject-info.md) , которая представляет субъект для отметки времени.</span><span class="sxs-lookup"><span data-stu-id="dbaad-126">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="dbaad-127">*пвсзттптиместамп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbaad-127">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbaad-128">Адрес строки в Юникоде, завершающейся нулем, которая содержит URL-адрес сервера отметок времени.</span><span class="sxs-lookup"><span data-stu-id="dbaad-128">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="dbaad-129">*псзалгорисмоид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbaad-129">*pszAlgorithmOid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbaad-130">Хэш-алгоритм, используемый для выполнения отметок времени, соответствующих RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="dbaad-130">A hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="dbaad-131">Этот параметр не учитывается для меток времени Authenticode.</span><span class="sxs-lookup"><span data-stu-id="dbaad-131">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="dbaad-132">*псрекуест* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="dbaad-132">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dbaad-133">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="dbaad-133">Optional.</span></span> <span data-ttu-id="dbaad-134">Адрес структуры [**\_ атрибутов шифрования**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) , которая содержит дополнительные атрибуты, добавляемые в запрос метки времени.</span><span class="sxs-lookup"><span data-stu-id="dbaad-134">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="dbaad-135">Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.</span><span class="sxs-lookup"><span data-stu-id="dbaad-135">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="dbaad-136">*псипдата* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="dbaad-136">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dbaad-137">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="dbaad-137">Optional.</span></span> <span data-ttu-id="dbaad-138">32-разрядное значение, передаваемое в качестве дополнительных данных в функции [*пакета интерфейса субъекта*](../secgloss/s-gly.md) (SIP).</span><span class="sxs-lookup"><span data-stu-id="dbaad-138">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="dbaad-139">Формат и содержимое этого параметра определяется поставщиком SIP.</span><span class="sxs-lookup"><span data-stu-id="dbaad-139">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="dbaad-140">Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.</span><span class="sxs-lookup"><span data-stu-id="dbaad-140">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="dbaad-141">*ппсигнерконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dbaad-141">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbaad-142">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="dbaad-142">Optional.</span></span> <span data-ttu-id="dbaad-143">Адрес указателя на структуру [**\_ контекста подписавшего**](signer-context.md) , который содержит подписанный большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="dbaad-143">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="dbaad-144">По завершении использования структуры **\_ контекста подписывающий** освободите ее, вызвав функцию [**сигнерфрисигнерконтекст**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="dbaad-144">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="dbaad-145">*пкриптополици* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="dbaad-145">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dbaad-146">При наличии указателя на структуру [**\_ \_ \_ абзаца со строгой подписью сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) , содержащую параметры, используемые для проверки наличия строгих подписей.</span><span class="sxs-lookup"><span data-stu-id="dbaad-146">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="dbaad-147">Метка времени должна пройти эту политику шифрования.</span><span class="sxs-lookup"><span data-stu-id="dbaad-147">The time stamp must pass this cryptographic policy.</span></span>

</dd> <dt>

<span data-ttu-id="dbaad-148">*Сохраняется*</span><span class="sxs-lookup"><span data-stu-id="dbaad-148">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="dbaad-149">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="dbaad-149">Reserved.</span></span> <span data-ttu-id="dbaad-150">Это значение должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="dbaad-150">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbaad-151">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbaad-151">Return value</span></span>

<span data-ttu-id="dbaad-152">Если функция завершается успешно, функция возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="dbaad-152">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="dbaad-153">Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="dbaad-153">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="dbaad-154">Возможные коды ошибок, возвращаемые этой функцией, включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="dbaad-154">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="dbaad-155">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="dbaad-155">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dbaad-156">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dbaad-156">Return code</span></span></th>
<th><span data-ttu-id="dbaad-157">Описание</span><span class="sxs-lookup"><span data-stu-id="dbaad-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="dbaad-158"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dbaad-158"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="dbaad-159">Эта ошибка может возвращать следующие условия.</span><span class="sxs-lookup"><span data-stu-id="dbaad-159">This error can be returned for the following conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="dbaad-160">Для параметра <em>dwFlags</em> необходимо задать либо <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> , либо <strong>SIGNER_TIMESTAMP_RFC3161</strong> .</span><span class="sxs-lookup"><span data-stu-id="dbaad-160">You must set either <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> or <strong>SIGNER_TIMESTAMP_RFC3161</strong> for the <em>dwFlags</em> parameter.</span></span></li>
<li><span data-ttu-id="dbaad-161"><em>Сохраненный</em> параметр должен иметь <strong>значение NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="dbaad-161">The <em>pReserved</em> parameter must be <strong>NULL</strong>.</span></span></li>
<li><span data-ttu-id="dbaad-162">Если установить флаг <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> в параметре <em>dwFlags</em> , то необходимо присвоить параметру <em>двиндекс</em> значение 0.</span><span class="sxs-lookup"><span data-stu-id="dbaad-162">If you set the <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> flag in the <em>dwFlags</em> parameter, you must set the <em>dwIndex</em> parameter to zero.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="dbaad-163">Требования</span><span class="sxs-lookup"><span data-stu-id="dbaad-163">Requirements</span></span>



| <span data-ttu-id="dbaad-164">Требование</span><span class="sxs-lookup"><span data-stu-id="dbaad-164">Requirement</span></span> | <span data-ttu-id="dbaad-165">Значение</span><span class="sxs-lookup"><span data-stu-id="dbaad-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbaad-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbaad-166">Minimum supported client</span></span><br/> | <span data-ttu-id="dbaad-167">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dbaad-167">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="dbaad-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbaad-168">Minimum supported server</span></span><br/> | <span data-ttu-id="dbaad-169">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dbaad-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dbaad-170">DLL</span><span class="sxs-lookup"><span data-stu-id="dbaad-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbaad-171"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbaad-171"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbaad-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbaad-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbaad-173">**сигнертиместамп**</span><span class="sxs-lookup"><span data-stu-id="dbaad-173">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="dbaad-174">**сигнертиместампекс**</span><span class="sxs-lookup"><span data-stu-id="dbaad-174">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> <dt>

[<span data-ttu-id="dbaad-175">**SignerTimeStampEx2**</span><span class="sxs-lookup"><span data-stu-id="dbaad-175">**SignerTimeStampEx2**</span></span>](signertimestampex2.md)
</dt> </dl>

 

 
