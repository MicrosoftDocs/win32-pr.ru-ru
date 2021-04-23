---
description: Преобразует URL-адрес файла в путь Microsoft MS-DOS.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: Функция Мфкреатепасфромурл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711275"
---
# <a name="mfcreatepathfromurl-function"></a><span data-ttu-id="f23dd-103">Функция Мфкреатепасфромурл</span><span class="sxs-lookup"><span data-stu-id="f23dd-103">MFCreatePathFromURL function</span></span>

<span data-ttu-id="f23dd-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="f23dd-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f23dd-105">Вместо этого приложения должны вызывать [**паскреатефромурл**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span><span class="sxs-lookup"><span data-stu-id="f23dd-105">Instead, applications should call [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span></span>

<span data-ttu-id="f23dd-106">Преобразует URL-адрес файла в путь Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="f23dd-106">Converts a file URL to a Microsoft MS-DOS path.</span></span>

## <a name="syntax"></a><span data-ttu-id="f23dd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f23dd-107">Syntax</span></span>


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a><span data-ttu-id="f23dd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f23dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f23dd-109">*пвсзфилеурл* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f23dd-109">*pwszFileURL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f23dd-110">Строка, завершающаяся нулем и содержащая URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f23dd-110">A null-terminated string that contains the URL.</span></span> <span data-ttu-id="f23dd-111">Максимальная длина строки — **\_ Максимальная \_ \_ Длина URL-адреса в Интернете**.</span><span class="sxs-lookup"><span data-stu-id="f23dd-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="f23dd-112">*ппвсзфилепас* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f23dd-112">*ppwszFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f23dd-113">Получает строку, завершающуюся нулем, которая содержит URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f23dd-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="f23dd-114">Вызывающий объект должен освободить строку, вызвав [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="f23dd-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f23dd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f23dd-115">Return value</span></span>

<span data-ttu-id="f23dd-116">Функция возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f23dd-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="f23dd-117">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f23dd-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f23dd-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f23dd-118">Return code</span></span>                                                                                  | <span data-ttu-id="f23dd-119">Описание</span><span class="sxs-lookup"><span data-stu-id="f23dd-119">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f23dd-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f23dd-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f23dd-121">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f23dd-121">The function succeeded.</span></span> <br/>                                                                         |
| <dl> <span data-ttu-id="f23dd-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f23dd-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f23dd-123">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="f23dd-123">Invalid argument.</span></span> <span data-ttu-id="f23dd-124">Строка, указанная в параметре *пвсзфилеурл* , не может быть преобразована в путь.</span><span class="sxs-lookup"><span data-stu-id="f23dd-124">The string given in the *pwszFileURL* parameter cannot be converted to a path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f23dd-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f23dd-125">Remarks</span></span>

<span data-ttu-id="f23dd-126">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="f23dd-126">This function has no associated import library.</span></span> <span data-ttu-id="f23dd-127">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mfplat.dll.</span><span class="sxs-lookup"><span data-stu-id="f23dd-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f23dd-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f23dd-128">Requirements</span></span>



| <span data-ttu-id="f23dd-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f23dd-129">Requirement</span></span> | <span data-ttu-id="f23dd-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f23dd-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f23dd-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f23dd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f23dd-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f23dd-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f23dd-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f23dd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f23dd-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f23dd-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f23dd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f23dd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f23dd-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f23dd-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23dd-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f23dd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23dd-138">Функции Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f23dd-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
