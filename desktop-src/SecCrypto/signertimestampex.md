---
description: Время помечает указанную тему и при необходимости возвращает указатель на \_ структуру контекста подписи, содержащую указатель на большой двоичный объект.
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: Функция Сигнертиместампекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816720"
---
# <a name="signertimestampex-function"></a><span data-ttu-id="4ad1f-103">Функция Сигнертиместампекс</span><span class="sxs-lookup"><span data-stu-id="4ad1f-103">SignerTimeStampEx function</span></span>

<span data-ttu-id="4ad1f-104">Функция **сигнертиместампекс** помечает указанную тему и при необходимости возвращает указатель на структуру [**\_ контекста подписи**](signer-context.md) , содержащую указатель на [*большой двоичный объект*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4ad1f-104">The **SignerTimeStampEx** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="4ad1f-105">Эта функция поддерживает отметку времени Authenticode.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-105">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="4ad1f-106">Чтобы выполнить отметку времени X. 509 для инфраструктуры открытых ключей (RFC 3161), используйте функцию [**SignerTimeStampEx2**](signertimestampex2.md) .</span><span class="sxs-lookup"><span data-stu-id="4ad1f-106">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="4ad1f-107">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="4ad1f-108">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4ad1f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ad1f-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="4ad1f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ad1f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ad1f-111">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ad1f-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ad1f-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-112">Reserved.</span></span> <span data-ttu-id="4ad1f-113">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-113">This parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="4ad1f-114">*псубжектинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ad1f-114">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ad1f-115">Адрес структуры [**\_ \_ сведений о субъекте-подписывания**](signer-subject-info.md) , которая представляет субъект для отметки времени.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-115">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="4ad1f-116">*пвсзттптиместамп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ad1f-116">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ad1f-117">Адрес строки в Юникоде, завершающейся нулем, которая содержит URL-адрес сервера отметок времени.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-117">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="4ad1f-118">*псрекуест* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ad1f-118">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ad1f-119">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-119">Optional.</span></span> <span data-ttu-id="4ad1f-120">Адрес структуры [**\_ атрибутов шифрования**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) , которая содержит дополнительные атрибуты, добавляемые в запрос метки времени.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-120">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="4ad1f-121">Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-121">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="4ad1f-122">*псипдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ad1f-122">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ad1f-123">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-123">Optional.</span></span> <span data-ttu-id="4ad1f-124">32-разрядное значение, передаваемое в качестве дополнительных данных в функции [*пакета интерфейса субъекта*](../secgloss/s-gly.md) (SIP).</span><span class="sxs-lookup"><span data-stu-id="4ad1f-124">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="4ad1f-125">Формат и содержимое этого параметра определяется поставщиком SIP.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-125">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="4ad1f-126">Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-126">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="4ad1f-127">*ппсигнерконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4ad1f-127">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ad1f-128">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-128">Optional.</span></span> <span data-ttu-id="4ad1f-129">Адрес указателя на структуру [**\_ контекста подписавшего**](signer-context.md) , который содержит подписанный большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-129">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="4ad1f-130">По завершении использования структуры **\_ контекста подписывающий** освободите ее, вызвав функцию [**сигнерфрисигнерконтекст**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="4ad1f-130">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ad1f-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ad1f-131">Return value</span></span>

<span data-ttu-id="4ad1f-132">Если функция завершается успешно, функция возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-132">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="4ad1f-133">Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="4ad1f-133">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="4ad1f-134">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="4ad1f-134">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ad1f-135">Требования</span><span class="sxs-lookup"><span data-stu-id="4ad1f-135">Requirements</span></span>



| <span data-ttu-id="4ad1f-136">Требование</span><span class="sxs-lookup"><span data-stu-id="4ad1f-136">Requirement</span></span> | <span data-ttu-id="4ad1f-137">Значение</span><span class="sxs-lookup"><span data-stu-id="4ad1f-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad1f-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ad1f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4ad1f-139">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4ad1f-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4ad1f-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ad1f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4ad1f-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4ad1f-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4ad1f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4ad1f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ad1f-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ad1f-143"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ad1f-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ad1f-144">See also</span></span>

<dl> <span data-ttu-id="4ad1f-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="4ad1f-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="4ad1f-146">**сигнертиместамп**</span><span class="sxs-lookup"><span data-stu-id="4ad1f-146">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> </dl>

 

 
