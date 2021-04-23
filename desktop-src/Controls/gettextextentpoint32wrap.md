---
title: Функция GetTextExtentPoint32Wrap
description: Вычисление ширины и высоты указанной строки текста. Эта функция заключает в оболочку вызов Жеттекстекстентпоинт.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- Элементы управления Windows для функций GetTextExtentPoint32Wrap
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801234"
---
# <a name="gettextextentpoint32wrap-function"></a><span data-ttu-id="59daf-105">Функция GetTextExtentPoint32Wrap</span><span class="sxs-lookup"><span data-stu-id="59daf-105">GetTextExtentPoint32Wrap function</span></span>

<span data-ttu-id="59daf-106">\[**GetTextExtentPoint32Wrap** доступен в Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="59daf-106">\[**GetTextExtentPoint32Wrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="59daf-107">Он может быть изменен или недоступен в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="59daf-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="59daf-108">Вместо этого рекомендуется использовать [**жеттекстекстентпоинт**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="59daf-108">It is recommended to use [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) directly instead.\]</span></span>

<span data-ttu-id="59daf-109">Вычисление ширины и высоты указанной строки текста.</span><span class="sxs-lookup"><span data-stu-id="59daf-109">Computes the width and height of the specified string of text.</span></span> <span data-ttu-id="59daf-110">Эта функция заключает в оболочку вызов [**жеттекстекстентпоинт**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="59daf-110">This function wraps a call to [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="syntax"></a><span data-ttu-id="59daf-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59daf-111">Syntax</span></span>


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a><span data-ttu-id="59daf-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="59daf-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59daf-113">*HDC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59daf-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59daf-114">Тип: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="59daf-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="59daf-115">Маркер контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="59daf-115">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="59daf-116">*лпстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59daf-116">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59daf-117">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="59daf-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="59daf-118">Указатель на буфер, содержащий текст для рисования.</span><span class="sxs-lookup"><span data-stu-id="59daf-118">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="59daf-119">Строка не должна завершаться нулем, так как *кбкаунт* указывает длину строки.</span><span class="sxs-lookup"><span data-stu-id="59daf-119">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="59daf-120">*кбкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59daf-120">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59daf-121">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="59daf-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="59daf-122">Длина строки в байтах, на которую указывает параметр *лпстринг*.</span><span class="sxs-lookup"><span data-stu-id="59daf-122">The length, in bytes, of the string pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="59daf-123">*лпсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="59daf-123">*lpSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59daf-124">Тип: **лпсизе**</span><span class="sxs-lookup"><span data-stu-id="59daf-124">Type: **LPSIZE**</span></span>

<span data-ttu-id="59daf-125">При возврате из этого метода содержит указатель на структуру [**размера**](/previous-versions//dd145106(v=vs.85)) , содержащую измерения строки в логических единицах.</span><span class="sxs-lookup"><span data-stu-id="59daf-125">When this method returns, contains a pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure containing the dimensions of the string, in logical units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59daf-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59daf-126">Return value</span></span>

<span data-ttu-id="59daf-127">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="59daf-127">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="59daf-128">При успешном выполнении возвращает ненулевое значение. в противном случае — значение 0.</span><span class="sxs-lookup"><span data-stu-id="59daf-128">Returns a nonzero value if successful; otherwise, 0.</span></span>

<span data-ttu-id="59daf-129">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="59daf-129">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="59daf-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59daf-130">Remarks</span></span>

<span data-ttu-id="59daf-131">**GetTextExtentPoint32Wrap** не экспортируется по имени или объявлено в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="59daf-131">**GetTextExtentPoint32Wrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="59daf-132">Чтобы использовать его, необходимо использовать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 420 из ComCtl32.dll для получения указателя на функцию.</span><span class="sxs-lookup"><span data-stu-id="59daf-132">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 420 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="59daf-133">Дополнительные замечания см. в разделе [**жеттекстекстентпоинт**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="59daf-133">For additional remarks, please see [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="requirements"></a><span data-ttu-id="59daf-134">Требования</span><span class="sxs-lookup"><span data-stu-id="59daf-134">Requirements</span></span>



| <span data-ttu-id="59daf-135">Требование</span><span class="sxs-lookup"><span data-stu-id="59daf-135">Requirement</span></span> | <span data-ttu-id="59daf-136">Значение</span><span class="sxs-lookup"><span data-stu-id="59daf-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59daf-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59daf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="59daf-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59daf-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="59daf-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59daf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="59daf-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59daf-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="59daf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="59daf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59daf-142"><dt>Comctl32.dll (версия 5,81 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="59daf-142"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

