---
description: Преобразует путь Microsoft MS-DOS в канонический URL-адрес.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: Функция Мфкреатеурлфромпас
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711276"
---
# <a name="mfcreateurlfrompath-function"></a><span data-ttu-id="148e4-103">Функция Мфкреатеурлфромпас</span><span class="sxs-lookup"><span data-stu-id="148e4-103">MFCreateURLFromPath function</span></span>

<span data-ttu-id="148e4-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="148e4-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="148e4-105">Вместо этого приложения должны вызывать [урлкреатефромпас](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span><span class="sxs-lookup"><span data-stu-id="148e4-105">Instead, Applications should call [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span></span>

<span data-ttu-id="148e4-106">Преобразует путь Microsoft MS-DOS в канонический URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="148e4-106">Converts a Microsoft MS-DOS path to a canonicalized URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="148e4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="148e4-107">Syntax</span></span>


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a><span data-ttu-id="148e4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="148e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="148e4-109">*пвсзфилепас* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="148e4-109">*pwszFilePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="148e4-110">Строка, завершающаяся нулем, которая содержит путь.</span><span class="sxs-lookup"><span data-stu-id="148e4-110">A null-terminated string that contains the path.</span></span> <span data-ttu-id="148e4-111">Максимальная длина строки — **\_ Максимальная \_ \_ Длина URL-адреса в Интернете**.</span><span class="sxs-lookup"><span data-stu-id="148e4-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="148e4-112">*ппвсзфилеурл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="148e4-112">*ppwszFileURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="148e4-113">Получает строку, завершающуюся нулем, которая содержит URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="148e4-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="148e4-114">Вызывающий объект должен освободить строку, вызвав [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="148e4-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="148e4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="148e4-115">Return value</span></span>

<span data-ttu-id="148e4-116">Функция возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="148e4-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="148e4-117">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="148e4-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="148e4-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="148e4-118">Return code</span></span>                                                                             | <span data-ttu-id="148e4-119">Описание</span><span class="sxs-lookup"><span data-stu-id="148e4-119">Description</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="148e4-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="148e4-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="148e4-121">Строка, заданная в параметре *пвсзфилепас* , уже имеет формат URL.</span><span class="sxs-lookup"><span data-stu-id="148e4-121">The string given in the *pwszFilePath* parameter is already in URL format.</span></span> <span data-ttu-id="148e4-122">В этом случае *псзфилепас* просто копируется в *ппсзфилеурл* без изменения.</span><span class="sxs-lookup"><span data-stu-id="148e4-122">In this case, *pszFilePath* is simply copied to *ppszFileURL* without modification.</span></span><br/> |
| <dl> <span data-ttu-id="148e4-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="148e4-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="148e4-124">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="148e4-124">The function succeeded.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="148e4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="148e4-125">Remarks</span></span>

<span data-ttu-id="148e4-126">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="148e4-126">This function has no associated import library.</span></span> <span data-ttu-id="148e4-127">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mfplat.dll.</span><span class="sxs-lookup"><span data-stu-id="148e4-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="148e4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="148e4-128">Requirements</span></span>



| <span data-ttu-id="148e4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="148e4-129">Requirement</span></span> | <span data-ttu-id="148e4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="148e4-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="148e4-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="148e4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="148e4-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="148e4-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="148e4-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="148e4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="148e4-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="148e4-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="148e4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="148e4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="148e4-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="148e4-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="148e4-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="148e4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="148e4-138">Функции Media Foundation</span><span class="sxs-lookup"><span data-stu-id="148e4-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
