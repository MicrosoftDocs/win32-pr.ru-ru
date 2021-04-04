---
title: Функция Дравтекстекспривврап
description: Рисует форматированный текст в указанном прямоугольнике. Эта функция заключает в оболочку вызов Дравтекстекс.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- Элементы управления Windows для функций Дравтекстекспривврап
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989376"
---
# <a name="drawtextexprivwrap-function"></a><span data-ttu-id="c0487-105">Функция Дравтекстекспривврап</span><span class="sxs-lookup"><span data-stu-id="c0487-105">DrawTextExPrivWrap function</span></span>

<span data-ttu-id="c0487-106">\[**Дравтекстекспривврап** доступен в Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="c0487-106">\[**DrawTextExPrivWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="c0487-107">Он может быть изменен или недоступен в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="c0487-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c0487-108">Вместо этого рекомендуется использовать [**дравтекстекс**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="c0487-108">It is recommended to use [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) directly instead.\]</span></span>

<span data-ttu-id="c0487-109">Рисует форматированный текст в указанном прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="c0487-109">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="c0487-110">Эта функция заключает в оболочку вызов [**дравтекстекс**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span><span class="sxs-lookup"><span data-stu-id="c0487-110">This function wraps a call to [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0487-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0487-111">Syntax</span></span>


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="c0487-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0487-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0487-113">*HDC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0487-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0487-114">Тип: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0487-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c0487-115">Маркер контекста устройства, в котором выполняется рисование.</span><span class="sxs-lookup"><span data-stu-id="c0487-115">A handle to the device context in which to draw.</span></span>

</dd> <dt>

<span data-ttu-id="c0487-116">*лпчтекст* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c0487-116">*lpchText* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0487-117">Тип: **[ **LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0487-117">Type: **[**LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c0487-118">Указатель на буфер, содержащий текст для рисования.</span><span class="sxs-lookup"><span data-stu-id="c0487-118">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="c0487-119">Если параметр *кчтекст* имеет значение-1, строка должна завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="c0487-119">If the *cchText* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="c0487-120">Если *двдтформат* включает DT \_ модифистринг, функция может добавить в эту строку до четырех дополнительных символов.</span><span class="sxs-lookup"><span data-stu-id="c0487-120">If *dwDTFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="c0487-121">Буфер, содержащий строку, должен быть достаточно большим, чтобы разместить эти дополнительные символы.</span><span class="sxs-lookup"><span data-stu-id="c0487-121">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="c0487-122">*кчтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0487-122">*cchText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0487-123">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="c0487-123">Type: **int**</span></span>

<span data-ttu-id="c0487-124">Длина строки, на которую указывает *лпчтекст*.</span><span class="sxs-lookup"><span data-stu-id="c0487-124">The length of the string pointed to by *lpchText*.</span></span> <span data-ttu-id="c0487-125">Если *кчтекст* имеет значение-1, то предполагается, что параметр *лпчтекст* является указателем на строку, завершающимся нулем, а [**дравтекстекс**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) автоматически вычислит число символов.</span><span class="sxs-lookup"><span data-stu-id="c0487-125">If *cchText* is -1, then the *lpchText* parameter is assumed to be a pointer to a null-terminated string and [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="c0487-126">*ЛПРК* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c0487-126">*lprc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0487-127">Тип: **лпрект**</span><span class="sxs-lookup"><span data-stu-id="c0487-127">Type: **LPRECT**</span></span>

<span data-ttu-id="c0487-128">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую прямоугольник в логических координатах, в котором должен быть отформатирован текст.</span><span class="sxs-lookup"><span data-stu-id="c0487-128">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="c0487-129">*двдтформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0487-129">*dwDTFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0487-130">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0487-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c0487-131">Параметры форматирования.</span><span class="sxs-lookup"><span data-stu-id="c0487-131">The formatting options.</span></span> <span data-ttu-id="c0487-132">Полный список параметров см. в документации по [**дравтекстекс**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) .</span><span class="sxs-lookup"><span data-stu-id="c0487-132">See the documentation for [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="c0487-133">*лпдтпарамс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0487-133">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0487-134">Тип: **лпдравтекстпарамс**</span><span class="sxs-lookup"><span data-stu-id="c0487-134">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="c0487-135">Указатель на структуру [**дравтекстпарамс**](/windows/win32/api/winuser/ns-winuser-drawtextparams) , указывающую дополнительные параметры форматирования.</span><span class="sxs-lookup"><span data-stu-id="c0487-135">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="c0487-136">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c0487-136">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0487-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0487-137">Return value</span></span>

<span data-ttu-id="c0487-138">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="c0487-138">Type: **int**</span></span>

<span data-ttu-id="c0487-139">Если функция выполняется удачно, возвращаемое значение — это высота текста в логических единицах.</span><span class="sxs-lookup"><span data-stu-id="c0487-139">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="c0487-140">Если указан параметр **DT \_ vCenter** или **DT \_ Bottom** , возвращаемое значение является смещением от **верхнего** элемента *ЛПРК* до конца отображаемого текста.</span><span class="sxs-lookup"><span data-stu-id="c0487-140">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text.</span></span>

<span data-ttu-id="c0487-141">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="c0487-141">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="c0487-142">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c0487-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="c0487-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0487-143">Remarks</span></span>

<span data-ttu-id="c0487-144">**Дравтекстекспривврап** не экспортируется по имени или объявлено в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="c0487-144">**DrawTextExPrivWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="c0487-145">Чтобы использовать его, необходимо использовать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 416 из ComCtl32.dll для получения указателя на функцию.</span><span class="sxs-lookup"><span data-stu-id="c0487-145">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 416 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="c0487-146">Дополнительные замечания см. в разделе [**дравтекстекс**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span><span class="sxs-lookup"><span data-stu-id="c0487-146">For additional remarks, please see [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0487-147">Требования</span><span class="sxs-lookup"><span data-stu-id="c0487-147">Requirements</span></span>



| <span data-ttu-id="c0487-148">Требование</span><span class="sxs-lookup"><span data-stu-id="c0487-148">Requirement</span></span> | <span data-ttu-id="c0487-149">Значение</span><span class="sxs-lookup"><span data-stu-id="c0487-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0487-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0487-150">Minimum supported client</span></span><br/> | <span data-ttu-id="c0487-151">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0487-151">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="c0487-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0487-152">Minimum supported server</span></span><br/> | <span data-ttu-id="c0487-153">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0487-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c0487-154">DLL</span><span class="sxs-lookup"><span data-stu-id="c0487-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0487-155"><dt>Comctl32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c0487-155"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

