---
description: Создает временный контейнер в поставщике служб шифрования (CSP) и загружает закрытый ключ из памяти в контейнер.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: Функция Пвкприватекэйаккуиреконтекстфроммемори
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348485"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a><span data-ttu-id="e038a-103">Функция Пвкприватекэйаккуиреконтекстфроммемори</span><span class="sxs-lookup"><span data-stu-id="e038a-103">PvkPrivateKeyAcquireContextFromMemory function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e038a-104">Это нерекомендуемый API.</span><span class="sxs-lookup"><span data-stu-id="e038a-104">This API is deprecated.</span></span> <span data-ttu-id="e038a-105">Корпорация Майкрософт может удалить этот API в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="e038a-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="e038a-106">Функция **пвкприватекэйаккуиреконтекстфроммемори** создает временный контейнер в [*поставщике служб шифрования*](../secgloss/c-gly.md) (CSP) и загружает [*закрытый ключ*](../secgloss/p-gly.md) из памяти в контейнер.</span><span class="sxs-lookup"><span data-stu-id="e038a-106">The **PvkPrivateKeyAcquireContextFromMemory** function creates a temporary container in the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and loads a [*private key*](../secgloss/p-gly.md) from memory into the container.</span></span>

> [!Note]  
> <span data-ttu-id="e038a-107">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="e038a-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="e038a-108">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="e038a-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e038a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e038a-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="e038a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e038a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e038a-111">*пвсзпровнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e038a-111">*pwszProvName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e038a-112">Указатель на строку, завершающуюся нулем, которая содержит имя CSP, тип которого запрашивается в *двпровтипе*.</span><span class="sxs-lookup"><span data-stu-id="e038a-112">A pointer to a null-terminated string that contains the name of the CSP whose type is requested in *dwProvType*.</span></span>

</dd> <dt>

<span data-ttu-id="e038a-113">*двпровтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e038a-113">*dwProvType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e038a-114">Значение **DWORD** для типа CSP.</span><span class="sxs-lookup"><span data-stu-id="e038a-114">A **DWORD** value for the CSP type.</span></span> <span data-ttu-id="e038a-115">Дополнительные сведения о типах CSP см. в разделе [типы поставщиков служб шифрования](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="e038a-115">For more information about CSP types, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="e038a-116">*pbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e038a-116">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e038a-117">Указатель на буфер для получения данных контекста.</span><span class="sxs-lookup"><span data-stu-id="e038a-117">A pointer to a buffer to receive the context data.</span></span> <span data-ttu-id="e038a-118">Вызывающий объект должен предоставить этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="e038a-118">The caller must provide this resource.</span></span>

</dd> <dt>

<span data-ttu-id="e038a-119">*cbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e038a-119">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e038a-120">Значение **типа DWORD** , указывающее размер буфера *pbData* в байтах.</span><span class="sxs-lookup"><span data-stu-id="e038a-120">A **DWORD** value that specifies the size, in bytes, of the *pbData* buffer.</span></span> <span data-ttu-id="e038a-121">Вызывающий объект должен предоставить это значение.</span><span class="sxs-lookup"><span data-stu-id="e038a-121">The caller must provide this value.</span></span>

</dd> <dt>

<span data-ttu-id="e038a-122">*хвндовнер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e038a-122">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e038a-123">Если требуется пароль для расшифровки контекстных данных, на которые указывает параметр *pbData* , этот параметр является обработчиком родительского элемента диалогового окна. в противном случае он имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e038a-123">If a password is required to decrypt the context data pointed to by the *pbData* parameter, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e038a-124">*пвсзкэйнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e038a-124">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e038a-125">Указатель на строку, завершающуюся нулем, которая содержит имя извлекаемого ключа.</span><span class="sxs-lookup"><span data-stu-id="e038a-125">A pointer to a null-terminated string that contains the name of the key to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e038a-126">*пдвкэйспек* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="e038a-126">*pdwKeySpec* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e038a-127">Указатель на значение **DWORD** , указывающее тип ключа.</span><span class="sxs-lookup"><span data-stu-id="e038a-127">A pointer to a **DWORD** value that specifies the type of key.</span></span> <span data-ttu-id="e038a-128">Возможные значения: **в \_ Кэйексчанже** или **в \_ сигнатуре**.</span><span class="sxs-lookup"><span data-stu-id="e038a-128">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="e038a-129">*фкриптпров* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e038a-129">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e038a-130">Указатель на маркер для CSP.</span><span class="sxs-lookup"><span data-stu-id="e038a-130">A pointer to a handle for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="e038a-131">*ппвсзтмпконтаинер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e038a-131">*ppwszTmpContainer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e038a-132">Адрес указателя на строку, завершающуюся нулем, для временного имени контейнера.</span><span class="sxs-lookup"><span data-stu-id="e038a-132">The address of a pointer to a null-terminated string for the temporary container name.</span></span> <span data-ttu-id="e038a-133">Функция **пвкприватекэйаккуиреконтекстфроммемори** предоставляет буфер для этой строки и инициализирует ее.</span><span class="sxs-lookup"><span data-stu-id="e038a-133">The **PvkPrivateKeyAcquireContextFromMemory** function provides the buffer for this string and initializes it.</span></span> <span data-ttu-id="e038a-134">При вызове **пвкприватекэйаккуиреконтекстфроммемори** адрес должен указывать на значение **null** .</span><span class="sxs-lookup"><span data-stu-id="e038a-134">When calling **PvkPrivateKeyAcquireContextFromMemory**, the address should point to a **NULL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e038a-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e038a-135">Return value</span></span>

<span data-ttu-id="e038a-136">При успешном выполнении эта функция возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="e038a-136">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="e038a-137">Функция **пвкприватекэйаккуиреконтекстфроммемори** возвращает **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="e038a-137">The **PvkPrivateKeyAcquireContextFromMemory** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="e038a-138">Требования</span><span class="sxs-lookup"><span data-stu-id="e038a-138">Requirements</span></span>



| <span data-ttu-id="e038a-139">Требование</span><span class="sxs-lookup"><span data-stu-id="e038a-139">Requirement</span></span> | <span data-ttu-id="e038a-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e038a-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e038a-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e038a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e038a-142">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e038a-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e038a-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e038a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e038a-144">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e038a-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e038a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e038a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e038a-146"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e038a-146"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
