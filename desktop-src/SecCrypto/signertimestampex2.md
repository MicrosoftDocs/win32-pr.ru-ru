---
description: Время помечает указанную тему и при необходимости возвращает указатель на \_ структуру контекста подписи, содержащую указатель на большой двоичный объект. Эта функция может использоваться для выполнения инфраструктуры открытого ключа X. 509, RFC 3161&\# 8211; совместимые метки времени.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: Функция SignerTimeStampEx2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664231"
---
# <a name="signertimestampex2-function"></a><span data-ttu-id="e59f0-104">Функция SignerTimeStampEx2</span><span class="sxs-lookup"><span data-stu-id="e59f0-104">SignerTimeStampEx2 function</span></span>

<span data-ttu-id="e59f0-105">Функция **SignerTimeStampEx2** помечает указанную тему и при необходимости возвращает указатель на структуру [**\_ контекста подписи**](signer-context.md) , содержащую указатель на [*большой двоичный объект*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e59f0-105">The **SignerTimeStampEx2** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="e59f0-106">Эта функция может использоваться для выполнения 509 инфраструктуры открытого ключа X., совместимой с RFC 3161, меток времени.</span><span class="sxs-lookup"><span data-stu-id="e59f0-106">This function can be used to perform X.509 Public Key Infrastructure, RFC 3161–compliant, time stamps.</span></span>

> [!Note]  
> <span data-ttu-id="e59f0-107">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="e59f0-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="e59f0-108">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="e59f0-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e59f0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e59f0-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="e59f0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e59f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e59f0-111">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e59f0-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59f0-112">Значение, указывающее тип создаваемой метки времени.</span><span class="sxs-lookup"><span data-stu-id="e59f0-112">Value that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="e59f0-113">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="e59f0-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="e59f0-114">Значения являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="e59f0-114">The values are mutually exclusive.</span></span>



| <span data-ttu-id="e59f0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e59f0-115">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="e59f0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e59f0-116">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="e59f0-117"><dt>**\_Метка времени подписи \_ AUTHENTICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="e59f0-117"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="e59f0-118">Задает отметку времени Authenticode.</span><span class="sxs-lookup"><span data-stu-id="e59f0-118">Specifies an Authenticode time stamp.</span></span><br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="e59f0-119"><dt>**\_Метка времени подписи \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="e59f0-119"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="e59f0-120">Задает отметку времени, совместимую с RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="e59f0-120">Specifies an RFC 3161–compliant time stamp.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e59f0-121">*псубжектинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e59f0-121">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59f0-122">Адрес структуры [**\_ \_ сведений о субъекте-подписывания**](signer-subject-info.md) , которая представляет субъект для отметки времени.</span><span class="sxs-lookup"><span data-stu-id="e59f0-122">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="e59f0-123">*пвсзттптиместамп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e59f0-123">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59f0-124">Адрес строки в Юникоде, завершающейся нулем, которая содержит URL-адрес сервера отметок времени.</span><span class="sxs-lookup"><span data-stu-id="e59f0-124">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="e59f0-125">*двалгид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e59f0-125">*dwAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59f0-126">Задает хэш-алгоритм, используемый для выполнения отметок времени, соответствующих RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="e59f0-126">Specifies a hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="e59f0-127">Этот параметр не учитывается для меток времени Authenticode.</span><span class="sxs-lookup"><span data-stu-id="e59f0-127">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="e59f0-128">*псрекуест* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e59f0-128">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59f0-129">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e59f0-129">Optional.</span></span> <span data-ttu-id="e59f0-130">Адрес структуры [**\_ атрибутов шифрования**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) , которая содержит дополнительные атрибуты, добавляемые в запрос метки времени.</span><span class="sxs-lookup"><span data-stu-id="e59f0-130">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="e59f0-131">Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.</span><span class="sxs-lookup"><span data-stu-id="e59f0-131">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="e59f0-132">*псипдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e59f0-132">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e59f0-133">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e59f0-133">Optional.</span></span> <span data-ttu-id="e59f0-134">32-разрядное значение, передаваемое в качестве дополнительных данных в функции [*пакета интерфейса субъекта*](../secgloss/s-gly.md) (SIP).</span><span class="sxs-lookup"><span data-stu-id="e59f0-134">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="e59f0-135">Формат и содержимое этого параметра определяется поставщиком SIP.</span><span class="sxs-lookup"><span data-stu-id="e59f0-135">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="e59f0-136">Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.</span><span class="sxs-lookup"><span data-stu-id="e59f0-136">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="e59f0-137">*ппсигнерконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e59f0-137">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e59f0-138">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e59f0-138">Optional.</span></span> <span data-ttu-id="e59f0-139">Адрес указателя на структуру [**\_ контекста подписавшего**](signer-context.md) , который содержит подписанный большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="e59f0-139">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="e59f0-140">По завершении использования структуры **\_ контекста подписывающий** освободите ее, вызвав функцию [**сигнерфрисигнерконтекст**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="e59f0-140">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e59f0-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e59f0-141">Return value</span></span>

<span data-ttu-id="e59f0-142">Если функция завершается успешно, функция возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e59f0-142">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="e59f0-143">Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="e59f0-143">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="e59f0-144">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="e59f0-144">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e59f0-145">Требования</span><span class="sxs-lookup"><span data-stu-id="e59f0-145">Requirements</span></span>



| <span data-ttu-id="e59f0-146">Требование</span><span class="sxs-lookup"><span data-stu-id="e59f0-146">Requirement</span></span> | <span data-ttu-id="e59f0-147">Значение</span><span class="sxs-lookup"><span data-stu-id="e59f0-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e59f0-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e59f0-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e59f0-149">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e59f0-149">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e59f0-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e59f0-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e59f0-151">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e59f0-151">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e59f0-152">DLL</span><span class="sxs-lookup"><span data-stu-id="e59f0-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e59f0-153"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e59f0-153"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e59f0-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e59f0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e59f0-155">**сигнертиместамп**</span><span class="sxs-lookup"><span data-stu-id="e59f0-155">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="e59f0-156">**сигнертиместампекс**</span><span class="sxs-lookup"><span data-stu-id="e59f0-156">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> </dl>

 

 
