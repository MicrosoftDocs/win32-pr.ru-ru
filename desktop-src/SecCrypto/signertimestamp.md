---
description: Помечает время указанной темой. Эта функция поддерживает отметку времени Authenticode. Чтобы выполнить отметку времени X. 509 для инфраструктуры открытых ключей (RFC 3161), используйте функцию SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: Функция Сигнертиместамп
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999213"
---
# <a name="signertimestamp-function"></a><span data-ttu-id="5d62d-105">Функция Сигнертиместамп</span><span class="sxs-lookup"><span data-stu-id="5d62d-105">SignerTimeStamp function</span></span>

<span data-ttu-id="5d62d-106">Время функции **сигнертиместамп** помечает указанную тему.</span><span class="sxs-lookup"><span data-stu-id="5d62d-106">The **SignerTimeStamp** function time stamps the specified subject.</span></span> <span data-ttu-id="5d62d-107">Эта функция поддерживает отметку времени Authenticode.</span><span class="sxs-lookup"><span data-stu-id="5d62d-107">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="5d62d-108">Чтобы выполнить отметку времени X. 509 для инфраструктуры открытых ключей (RFC 3161), используйте функцию [**SignerTimeStampEx2**](signertimestampex2.md) .</span><span class="sxs-lookup"><span data-stu-id="5d62d-108">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="5d62d-109">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="5d62d-109">This function has no associated header file or import library.</span></span> <span data-ttu-id="5d62d-110">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="5d62d-110">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5d62d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d62d-111">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="5d62d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d62d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d62d-113">*псубжектинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d62d-113">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d62d-114">Адрес структуры [**\_ \_ сведений о субъекте-подписывания**](signer-subject-info.md) , которая представляет субъект для отметки времени.</span><span class="sxs-lookup"><span data-stu-id="5d62d-114">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="5d62d-115">*пвсзттптиместамп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d62d-115">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d62d-116">Адрес строки в Юникоде, завершающейся нулем, которая содержит URL-адрес сервера отметок времени.</span><span class="sxs-lookup"><span data-stu-id="5d62d-116">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="5d62d-117">*псрекуест* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5d62d-117">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d62d-118">Адрес структуры [**\_ атрибутов шифрования**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) , которая содержит дополнительные атрибуты, добавляемые в запрос метки времени.</span><span class="sxs-lookup"><span data-stu-id="5d62d-118">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="5d62d-119">Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.</span><span class="sxs-lookup"><span data-stu-id="5d62d-119">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="5d62d-120">*псипдата* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5d62d-120">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d62d-121">32-разрядное значение, передаваемое в функции SIP в качестве дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="5d62d-121">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="5d62d-122">Формат и содержимое этого объекта определяется поставщиком SIP.</span><span class="sxs-lookup"><span data-stu-id="5d62d-122">The format and content of this is defined by the SIP provider.</span></span>

<span data-ttu-id="5d62d-123">Этот параметр является необязательным и может иметь **значение NULL** , если он не включен.</span><span class="sxs-lookup"><span data-stu-id="5d62d-123">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d62d-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d62d-124">Return value</span></span>

<span data-ttu-id="5d62d-125">Если функция завершается успешно, функция возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5d62d-125">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="5d62d-126">Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="5d62d-126">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="5d62d-127">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="5d62d-127">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d62d-128">Требования</span><span class="sxs-lookup"><span data-stu-id="5d62d-128">Requirements</span></span>



| <span data-ttu-id="5d62d-129">Требование</span><span class="sxs-lookup"><span data-stu-id="5d62d-129">Requirement</span></span> | <span data-ttu-id="5d62d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="5d62d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d62d-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d62d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5d62d-132">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5d62d-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5d62d-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d62d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5d62d-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5d62d-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d62d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5d62d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d62d-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d62d-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
