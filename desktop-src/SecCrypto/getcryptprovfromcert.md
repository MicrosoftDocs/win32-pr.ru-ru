---
description: Получает маркер поставщика служб шифрования (CSP) и ключевую спецификацию для контекста сертификата.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: Функция Жеткриптпровфромцерт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350125"
---
# <a name="getcryptprovfromcert-function"></a><span data-ttu-id="f2dfa-103">Функция Жеткриптпровфромцерт</span><span class="sxs-lookup"><span data-stu-id="f2dfa-103">GetCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2dfa-104">Это нерекомендуемый API.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-104">This API is deprecated.</span></span> <span data-ttu-id="f2dfa-105">Корпорация Майкрософт может удалить этот API в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="f2dfa-106">Функция **жеткриптпровфромцерт** получает маркер [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) и ключевую спецификацию для контекста [*сертификата*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f2dfa-106">The **GetCryptProvFromCert** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and a key specification for a [*certificate*](../secgloss/c-gly.md) context.</span></span> <span data-ttu-id="f2dfa-107">Эта функция используется для получения доступа к [*закрытому ключу*](../secgloss/p-gly.md) издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-107">Use this function to get access to the [*private key*](../secgloss/p-gly.md) of the certificate issuer.</span></span>

> [!Note]  
> <span data-ttu-id="f2dfa-108">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="f2dfa-109">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f2dfa-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2dfa-110">Syntax</span></span>


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a><span data-ttu-id="f2dfa-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2dfa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2dfa-112">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-112">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dfa-113">Маркер окна, используемый в качестве владельца всех отображаемых диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-113">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="f2dfa-114">Этот элемент в настоящее время не используется и не учитывается.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-114">This member is not currently used and is ignored.</span></span> <span data-ttu-id="f2dfa-115">Для этого параметра можно спокойно передать **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="f2dfa-115">It is safe to pass **NULL** for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f2dfa-116">*пцерт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-116">*pCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dfa-117">Указатель на структуру [**\_ контекста**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) сертификата для сертификата.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-117">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="f2dfa-118">*фкриптпров* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-118">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dfa-119">Указатель на структуру [**хкриптпров**](hcryptprov.md) , которая является обработчиком для CSP.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-119">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure that is a handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="f2dfa-120">*пдвкэйспек* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-120">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dfa-121">Спецификация закрытого ключа для извлечения.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-121">The specification of the private key to retrieve.</span></span> <span data-ttu-id="f2dfa-122">Возможные значения: **в \_ Кэйексчанже** или **в \_ сигнатуре**.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-122">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="f2dfa-123">*пфдидкриптаккуире* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-123">*pfDidCryptAcquire* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dfa-124">Значение типа, указывающее, получил ли функция маркер поставщика на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-124">A value that specifies whether the function acquired the provider handle based on the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="f2dfa-125">*ппвсзтмпконтаинер* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-125">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dfa-126">Адрес указателя на строку, завершающуюся нулем, для имени контейнера временного ключа.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-126">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="f2dfa-127">Функция **жеткриптпровфромцерт** предоставляет и инициализирует Временный контейнер.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-127">The **GetCryptProvFromCert** function provides and initializes the temporary container.</span></span> <span data-ttu-id="f2dfa-128">При вызове **жеткриптпровфромцерт** адрес должен указывать на значение **null** .</span><span class="sxs-lookup"><span data-stu-id="f2dfa-128">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="f2dfa-129">*ппвсзпровидернаме* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-129">*ppwszProviderName* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dfa-130">Адрес указателя на строку, завершающуюся нулем, для имени поставщика.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-130">The address of a pointer to a null-terminated string for the provider name.</span></span> <span data-ttu-id="f2dfa-131">Функция **жеткриптпровфромцерт** возвращает имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-131">The **GetCryptProvFromCert** function returns the provider name.</span></span> <span data-ttu-id="f2dfa-132">При вызове **жеткриптпровфромцерт** адрес должен указывать на значение **null** .</span><span class="sxs-lookup"><span data-stu-id="f2dfa-132">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="f2dfa-133">*пдвпровидертипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-133">*pdwProviderType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dfa-134">Указывает тип CSP.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-134">Specifies the CSP type.</span></span> <span data-ttu-id="f2dfa-135">Это может быть ноль или один из [типов поставщиков служб шифрования](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="f2dfa-135">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="f2dfa-136">Если этот член равен нулю, контейнер ключей является одним из поставщиков хранилища ключей CNG.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-136">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2dfa-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2dfa-137">Return value</span></span>

<span data-ttu-id="f2dfa-138">При успешном выполнении эта функция возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-138">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="f2dfa-139">Функция **жеткриптпровфромцерт** возвращает **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-139">The **GetCryptProvFromCert** function returns **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2dfa-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2dfa-140">Remarks</span></span>

<span data-ttu-id="f2dfa-141">Средство [MakeCert](makecert.md) вызывает **жеткриптпровфромцерт** при вызове с помощью параметра командной строки **-** -.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-141">The [MakeCert](makecert.md) tool calls **GetCryptProvFromCert** when you invoke it by using the **-is** command line option.</span></span>

<span data-ttu-id="f2dfa-142">Если параметр *пфдидкриптаккуире* имеет значение **true**, функция задает для значений поставщика параметры *фкриптпров*, *пдвкэйспек* и *пдвпровидертипе* .</span><span class="sxs-lookup"><span data-stu-id="f2dfa-142">If the *pfDidCryptAcquire* parameter is set to **TRUE**, the function sets *phCryptProv*, *pdwKeySpec*, and *pdwProviderType* parameters to the provider values.</span></span>

<span data-ttu-id="f2dfa-143">Завершив использование CSP, освободите его, вызвав функцию [**фрикриптпровфромцерт**](freecryptprovfromcert.md) .</span><span class="sxs-lookup"><span data-stu-id="f2dfa-143">When you have finished using the CSP, free it by calling the [**FreeCryptProvFromCert**](freecryptprovfromcert.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2dfa-144">Требования</span><span class="sxs-lookup"><span data-stu-id="f2dfa-144">Requirements</span></span>



| <span data-ttu-id="f2dfa-145">Требование</span><span class="sxs-lookup"><span data-stu-id="f2dfa-145">Requirement</span></span> | <span data-ttu-id="f2dfa-146">Значение</span><span class="sxs-lookup"><span data-stu-id="f2dfa-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2dfa-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2dfa-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f2dfa-148">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f2dfa-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2dfa-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f2dfa-150">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2dfa-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f2dfa-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2dfa-152"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2dfa-152"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
