---
description: Получает маркер поставщика служб шифрования (CSP) на основе файла закрытого ключа или имени контейнера ключей.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: Функция Пвкжеткриптпров
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913619"
---
# <a name="pvkgetcryptprov-function"></a><span data-ttu-id="7f042-103">Функция Пвкжеткриптпров</span><span class="sxs-lookup"><span data-stu-id="7f042-103">PvkGetCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f042-104">Это нерекомендуемый API.</span><span class="sxs-lookup"><span data-stu-id="7f042-104">This API is deprecated.</span></span> <span data-ttu-id="7f042-105">Корпорация Майкрософт может удалить этот API в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="7f042-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="7f042-106">Функция **пвкжеткриптпров** получает маркер [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) на основе файла [*закрытого ключа*](../secgloss/p-gly.md) или имени контейнера ключей.</span><span class="sxs-lookup"><span data-stu-id="7f042-106">The **PvkGetCryptProv** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) based on either a [*private key*](../secgloss/p-gly.md) file or a key container name.</span></span>

> [!Note]  
> <span data-ttu-id="7f042-107">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="7f042-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="7f042-108">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="7f042-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7f042-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f042-109">Syntax</span></span>


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a><span data-ttu-id="7f042-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f042-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f042-111">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f042-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f042-112">Если для расшифровки файла закрытого ключа требуется пароль, этот параметр является маркером родительского элемента диалогового окна пароль. в противном случае он имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7f042-112">If a password is required to decrypt the private key file, this parameter is a handle to the parent of the password dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7f042-113">*пвсзкаптион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f042-113">*pwszCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f042-114">Указатель на строку, завершающуюся нулем, для заголовка диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="7f042-114">A pointer to a null-terminated string for the dialog box caption.</span></span>

</dd> <dt>

<span data-ttu-id="7f042-115">*пвсзкапипровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f042-115">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f042-116">Указатель на строку, завершающуюся нулем, для имени CSP.</span><span class="sxs-lookup"><span data-stu-id="7f042-116">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="7f042-117">*двпровидертипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f042-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f042-118">Значение типа **DWORD** , представляющее тип поставщика служб шифрования.</span><span class="sxs-lookup"><span data-stu-id="7f042-118">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="7f042-119">Дополнительные сведения см. в разделе [типы поставщиков служб шифрования](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="7f042-119">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f042-120">*пвсзпвкфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f042-120">*pwszPvkFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f042-121">Указатель на строку, завершающуюся нулем, которая содержит имя файла закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="7f042-121">A pointer to a null-terminated string that contains the name of a private key file.</span></span>

</dd> <dt>

<span data-ttu-id="7f042-122">*пвсзкэйконтаинернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f042-122">*pwszKeyContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f042-123">Указатель на строку, завершающуюся нулем, для имени контейнера закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="7f042-123">A pointer to a null-terminated string for the private key container name.</span></span>

</dd> <dt>

<span data-ttu-id="7f042-124">*пдвкэйспек* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f042-124">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f042-125">Указатель на значение **DWORD** для типа ключа контейнера, возвращаемого с помощью *фкриптпров* и *ппвсзтмпконтаинер*.</span><span class="sxs-lookup"><span data-stu-id="7f042-125">A pointer to a **DWORD** value for the type of key of the container returned with *phCryptProv* and *ppwszTmpContainer*.</span></span>

</dd> <dt>

<span data-ttu-id="7f042-126">*ппвсзтмпконтаинер* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="7f042-126">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f042-127">Адрес указателя на строку, завершающуюся нулем, для имени контейнера временного ключа.</span><span class="sxs-lookup"><span data-stu-id="7f042-127">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="7f042-128">Функция **пвкжеткриптпров** предоставляет и инициализирует Временный контейнер.</span><span class="sxs-lookup"><span data-stu-id="7f042-128">The **PvkGetCryptProv** function provides and initializes the temporary container.</span></span> <span data-ttu-id="7f042-129">При вызове **пвкжеткриптпров** адрес должен указывать на значение **null** .</span><span class="sxs-lookup"><span data-stu-id="7f042-129">When calling **PvkGetCryptProv**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="7f042-130">*фкриптпров* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f042-130">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f042-131">Указатель на маркер для CSP.</span><span class="sxs-lookup"><span data-stu-id="7f042-131">A pointer to a handle for the CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f042-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f042-132">Return value</span></span>

<span data-ttu-id="7f042-133">Если метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7f042-133">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="7f042-134">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="7f042-134">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="7f042-135">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="7f042-135">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f042-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f042-136">Remarks</span></span>

<span data-ttu-id="7f042-137">Функция **пвкжеткриптпров** сначала пытается получить маркер поставщика из имени контейнера ключей, заданного параметром *пвсзкэйконтаинернаме* .</span><span class="sxs-lookup"><span data-stu-id="7f042-137">The **PvkGetCryptProv** function first tries to get the provider handle from the key container name specified by the *pwszKeyContainerName* parameter.</span></span> <span data-ttu-id="7f042-138">Если для параметра *пвсзкэйконтаинернаме* передать **значение NULL** , **пвкжеткриптпров** пытается получить поставщик из файла закрытого ключа, указанного в параметре *пвсзпвкфиле* .</span><span class="sxs-lookup"><span data-stu-id="7f042-138">If you pass **NULL** for the *pwszKeyContainerName* parameter, **PvkGetCryptProv** tries to get the provider from the private key file specified in the *pwszPvkFile* parameter.</span></span>

<span data-ttu-id="7f042-139">Когда вы завершите использование CSP, освободите маркер поставщика и Временный контейнер ключей, вызвав функцию [**пвкфрикриптпров**](pvkfreecryptprov.md) .</span><span class="sxs-lookup"><span data-stu-id="7f042-139">When you have finished using the CSP, free the provider handle and temporary key container by calling the [**PvkFreeCryptProv**](pvkfreecryptprov.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f042-140">Требования</span><span class="sxs-lookup"><span data-stu-id="7f042-140">Requirements</span></span>



| <span data-ttu-id="7f042-141">Требование</span><span class="sxs-lookup"><span data-stu-id="7f042-141">Requirement</span></span> | <span data-ttu-id="7f042-142">Значение</span><span class="sxs-lookup"><span data-stu-id="7f042-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f042-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f042-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7f042-144">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7f042-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7f042-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f042-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7f042-146">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f042-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f042-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7f042-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f042-148"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f042-148"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
