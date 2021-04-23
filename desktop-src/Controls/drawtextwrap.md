---
title: Функция Дравтекстврап
description: Рисует форматированный текст в указанном прямоугольнике. Текст форматируется в соответствии с заданным методом (расширяя вкладки, выполняя, выполняя и т. д.). Эта функция заключает в оболочку вызов DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- Элементы управления Windows для функций Дравтекстврап
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988246"
---
# <a name="drawtextwrap-function"></a><span data-ttu-id="fe8c1-106">Функция Дравтекстврап</span><span class="sxs-lookup"><span data-stu-id="fe8c1-106">DrawTextWrap function</span></span>

<span data-ttu-id="fe8c1-107">\[**Дравтекстврап** доступен в Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="fe8c1-107">\[**DrawTextWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="fe8c1-108">Он может быть изменен или недоступен в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="fe8c1-109">Вместо этого рекомендуется использовать [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="fe8c1-109">It is recommended to use [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) directly instead.\]</span></span>

<span data-ttu-id="fe8c1-110">Рисует форматированный текст в указанном прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-110">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="fe8c1-111">Текст форматируется в соответствии с заданным методом (расширяя вкладки, выполняя, выполняя и т. д.).</span><span class="sxs-lookup"><span data-stu-id="fe8c1-111">It formats the text according to the specified method (expanding tabs, justifying characters, breaking lines, and so on).</span></span> <span data-ttu-id="fe8c1-112">Эта функция заключает в оболочку вызов [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="fe8c1-112">This function wraps a call to [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe8c1-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe8c1-113">Syntax</span></span>


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="fe8c1-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe8c1-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe8c1-115">*HDC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe8c1-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8c1-116">Тип: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe8c1-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe8c1-117">Маркер контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="fe8c1-118">*лпстринг* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fe8c1-118">*lpString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8c1-119">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe8c1-119">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe8c1-120">Указатель на буфер, содержащий текст для рисования.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-120">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="fe8c1-121">Если параметр *нкаунт* имеет значение-1, строка должна завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-121">If the *nCount* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="fe8c1-122">Если *UFormat* включает DT \_ модифистринг, функция может добавить в эту строку до четырех дополнительных символов.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-122">If *uFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="fe8c1-123">Буфер, содержащий строку, должен быть достаточно большим, чтобы разместить эти дополнительные символы.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-123">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="fe8c1-124">*нкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe8c1-124">*nCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8c1-125">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="fe8c1-125">Type: **int**</span></span>

<span data-ttu-id="fe8c1-126">Длина строки, на которую указывает *лпстринг*.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-126">The length of the string pointed to by *lpString*.</span></span> <span data-ttu-id="fe8c1-127">Если *нкаунт* имеет значение-1, то предполагается, что параметр *лпстринг* является указателем на строку, завершающимся нулем, а [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) автоматически вычислит число символов.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-127">If *nCount* is -1, then the *lpString* parameter is assumed to be a pointer to a null-terminated string and [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="fe8c1-128">*лпрект* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fe8c1-128">*lpRect* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8c1-129">Тип: **лпрект**</span><span class="sxs-lookup"><span data-stu-id="fe8c1-129">Type: **LPRECT**</span></span>

<span data-ttu-id="fe8c1-130">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую прямоугольник в логических координатах, в котором должен быть отформатирован текст.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-130">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="fe8c1-131">*UFormat* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe8c1-131">*uFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8c1-132">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe8c1-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe8c1-133">Параметры форматирования.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-133">The formatting options.</span></span> <span data-ttu-id="fe8c1-134">Полный список параметров см. в документации по [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .</span><span class="sxs-lookup"><span data-stu-id="fe8c1-134">See the documentation for [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="fe8c1-135">*лпдтпарамс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe8c1-135">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8c1-136">Тип: **лпдравтекстпарамс**</span><span class="sxs-lookup"><span data-stu-id="fe8c1-136">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="fe8c1-137">Указатель на структуру [**дравтекстпарамс**](/windows/win32/api/winuser/ns-winuser-drawtextparams) , указывающую дополнительные параметры форматирования.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-137">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="fe8c1-138">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-138">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe8c1-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe8c1-139">Return value</span></span>

<span data-ttu-id="fe8c1-140">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="fe8c1-140">Type: **int**</span></span>

<span data-ttu-id="fe8c1-141">Если функция выполняется удачно, возвращаемое значение — это высота текста в логических единицах.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-141">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="fe8c1-142">Если указан параметр **DT \_ vCenter** или **DT \_ Bottom** , возвращаемое значение является смещением от **верхнего** элемента *ЛПРК* до конца рисуемого текста, если функция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-142">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text If the function fails, the return value is zero.</span></span>

<span data-ttu-id="fe8c1-143">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-143">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="fe8c1-144">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="fe8c1-144">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe8c1-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe8c1-145">Remarks</span></span>

<span data-ttu-id="fe8c1-146">**Дравтекстврап** не экспортируется по имени или объявлено в общедоступном заголовке.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-146">**DrawTextWrap** is not exported by name or declared in a public header.</span></span> <span data-ttu-id="fe8c1-147">Чтобы использовать его, необходимо использовать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 415 из ComCtl32.dll для получения указателя на функцию.</span><span class="sxs-lookup"><span data-stu-id="fe8c1-147">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 415 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="fe8c1-148">Дополнительные замечания см. в разделе [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="fe8c1-148">For additional remarks, please see [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe8c1-149">Требования</span><span class="sxs-lookup"><span data-stu-id="fe8c1-149">Requirements</span></span>



| <span data-ttu-id="fe8c1-150">Требование</span><span class="sxs-lookup"><span data-stu-id="fe8c1-150">Requirement</span></span> | <span data-ttu-id="fe8c1-151">Значение</span><span class="sxs-lookup"><span data-stu-id="fe8c1-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8c1-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe8c1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8c1-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe8c1-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="fe8c1-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe8c1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8c1-155">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe8c1-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fe8c1-156">DLL</span><span class="sxs-lookup"><span data-stu-id="fe8c1-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe8c1-157"><dt>Comctl32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="fe8c1-157"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

