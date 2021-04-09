---
title: Функция Ексттекстаутврап
description: Рисует текст с использованием текущего выбранного шрифта, цвета фона и цвета текста. При необходимости можно указать измерения, которые будут использоваться для обрезки, непрозрачности или и того, и другого. Эта функция заключает в оболочку вызов ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- Элементы управления Windows для функций Ексттекстаутврап
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135211"
---
# <a name="exttextoutwrap-function"></a><span data-ttu-id="889ad-106">Функция Ексттекстаутврап</span><span class="sxs-lookup"><span data-stu-id="889ad-106">ExtTextOutWrap function</span></span>

<span data-ttu-id="889ad-107">\[**Ексттекстаутврап** доступен в Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="889ad-107">\[**ExtTextOutWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="889ad-108">Он может быть изменен или недоступен в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="889ad-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="889ad-109">Вместо этого рекомендуется использовать [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="889ad-109">It is recommended to use [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) directly instead.\]</span></span>

<span data-ttu-id="889ad-110">Рисует текст с использованием текущего выбранного шрифта, цвета фона и цвета текста.</span><span class="sxs-lookup"><span data-stu-id="889ad-110">Draws text using the currently selected font, background color, and text color.</span></span> <span data-ttu-id="889ad-111">При необходимости можно указать измерения, которые будут использоваться для обрезки, непрозрачности или и того, и другого.</span><span class="sxs-lookup"><span data-stu-id="889ad-111">You can optionally provide dimensions to be used for clipping, opacity, or both.</span></span> <span data-ttu-id="889ad-112">Эта функция заключает в оболочку вызов [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span><span class="sxs-lookup"><span data-stu-id="889ad-112">This function wraps a call to [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="syntax"></a><span data-ttu-id="889ad-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="889ad-113">Syntax</span></span>


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a><span data-ttu-id="889ad-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="889ad-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="889ad-115">*HDC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="889ad-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="889ad-116">Тип: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="889ad-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="889ad-117">Маркер контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="889ad-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="889ad-118">*X* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="889ad-118">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="889ad-119">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="889ad-119">Type: **int**</span></span>

<span data-ttu-id="889ad-120">Координата x (в логических координатах) точки ссылки, используемой для размещения строки.</span><span class="sxs-lookup"><span data-stu-id="889ad-120">The x-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="889ad-121">*Y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="889ad-121">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="889ad-122">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="889ad-122">Type: **int**</span></span>

<span data-ttu-id="889ad-123">Координата по оси y (в логических координатах) точки ссылки, используемой для размещения строки.</span><span class="sxs-lookup"><span data-stu-id="889ad-123">The y-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="889ad-124">*уоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="889ad-124">*uOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="889ad-125">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="889ad-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="889ad-126">Значения, указывающие, как использовать определяемый приложением прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="889ad-126">Values that specify how to use the application-defined rectangle.</span></span> <span data-ttu-id="889ad-127">Полный список параметров см. в разделе [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) .</span><span class="sxs-lookup"><span data-stu-id="889ad-127">See [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="889ad-128">*ЛПРК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="889ad-128">*lprc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="889ad-129">Тип: \**const [**Rect**](/previous-versions//dd162897(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="889ad-129">Type: \**const [**RECT**](/previous-versions//dd162897(v=vs.85))\** _</span></span>

<span data-ttu-id="889ad-130">Указатель на необязательную структуру [_ *Rect* \*](/previous-versions//dd162897(v=vs.85)) , указывающую размеры (в логических координатах) прямоугольника, используемого для обрезки, непрозрачности или и того и другого.</span><span class="sxs-lookup"><span data-stu-id="889ad-130">A pointer to an optional [_ *RECT*\*](/previous-versions//dd162897(v=vs.85)) structure that specifies the dimensions, in logical coordinates, of a rectangle that is used for clipping, opacity, or both.</span></span>

</dd> <dt>

<span data-ttu-id="889ad-131">*лпстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="889ad-131">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="889ad-132">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="889ad-132">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="889ad-133">Указатель на буфер, содержащий текст для рисования.</span><span class="sxs-lookup"><span data-stu-id="889ad-133">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="889ad-134">Строка не должна завершаться нулем, так как *кбкаунт* указывает длину строки.</span><span class="sxs-lookup"><span data-stu-id="889ad-134">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="889ad-135">*кбкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="889ad-135">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="889ad-136">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="889ad-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="889ad-137">Длина строки в байтах, на которую указывает *лпстринг*.</span><span class="sxs-lookup"><span data-stu-id="889ad-137">The length of the string, in bytes, pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="889ad-138">*лпдкс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="889ad-138">*lpDx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="889ad-139">Тип: \**const [**int**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="889ad-139">Type: \**const [**INT**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="889ad-140">Указатель на необязательный массив значений, указывающий расстояние между источниками смежных ячеек символов.</span><span class="sxs-lookup"><span data-stu-id="889ad-140">A pointer to an optional array of values that indicate the distance between origins of adjacent character cells.</span></span> <span data-ttu-id="889ad-141">Например, \[ логические устройства _lpDx \* x \] разделяют источники ячейки символа x и символьной ячейки (x + 1).</span><span class="sxs-lookup"><span data-stu-id="889ad-141">For example, _lpDx\*\[x\] logical units separate the origins of character cell x and character cell (x + 1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="889ad-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="889ad-142">Return value</span></span>

<span data-ttu-id="889ad-143">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="889ad-143">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="889ad-144">Возвращает ненулевое значение, если строка успешно рисуется.</span><span class="sxs-lookup"><span data-stu-id="889ad-144">Returns a nonzero value if the string is drawn successfully.</span></span> <span data-ttu-id="889ad-145">Однако если версия [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) с кодировкой ANSI вызывается с \_ индексом глифа ето \_ , функция возвращает **значение true** , даже если функция ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="889ad-145">However, if the ANSI version of [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) is called with ETO\_GLYPH\_INDEX, the function returns **TRUE** even though the function does nothing.</span></span>

<span data-ttu-id="889ad-146">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="889ad-146">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="889ad-147">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="889ad-147">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="889ad-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="889ad-148">Remarks</span></span>

<span data-ttu-id="889ad-149">**Ексттекстаутврап** не экспортируется по имени или объявлено в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="889ad-149">**ExtTextOutWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="889ad-150">Чтобы использовать его, необходимо использовать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 417 из ComCtl32.dll для получения указателя на функцию.</span><span class="sxs-lookup"><span data-stu-id="889ad-150">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 417 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="889ad-151">Дополнительные замечания см. в разделе [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span><span class="sxs-lookup"><span data-stu-id="889ad-151">For additional remarks, please see [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="requirements"></a><span data-ttu-id="889ad-152">Требования</span><span class="sxs-lookup"><span data-stu-id="889ad-152">Requirements</span></span>



| <span data-ttu-id="889ad-153">Требование</span><span class="sxs-lookup"><span data-stu-id="889ad-153">Requirement</span></span> | <span data-ttu-id="889ad-154">Значение</span><span class="sxs-lookup"><span data-stu-id="889ad-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="889ad-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="889ad-155">Minimum supported client</span></span><br/> | <span data-ttu-id="889ad-156">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="889ad-156">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="889ad-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="889ad-157">Minimum supported server</span></span><br/> | <span data-ttu-id="889ad-158">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="889ad-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="889ad-159">DLL</span><span class="sxs-lookup"><span data-stu-id="889ad-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="889ad-160"><dt>Comctl32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="889ad-160"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

