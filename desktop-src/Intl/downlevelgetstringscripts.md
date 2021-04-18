---
description: Предоставляет список скриптов, используемых в указанной строке Юникода.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: Функция Довнлевелжетстрингскриптс (Идндл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684252"
---
# <a name="downlevelgetstringscripts-function"></a><span data-ttu-id="36761-103">Функция Довнлевелжетстрингскриптс</span><span class="sxs-lookup"><span data-stu-id="36761-103">DownlevelGetStringScripts function</span></span>

<span data-ttu-id="36761-104">Предоставляет список скриптов, используемых в указанной строке Юникода.</span><span class="sxs-lookup"><span data-stu-id="36761-104">Provides a list of scripts used in the specified Unicode string.</span></span>

> [!Note]  
> <span data-ttu-id="36761-105">Эта функция используется только приложениями, работающими в операционных системах, предшествующих Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="36761-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="36761-106">Для его использования требуется загружаемый пакет.</span><span class="sxs-lookup"><span data-stu-id="36761-106">Its use requires the download package.</span></span> <span data-ttu-id="36761-107">Приложения, которые работают только в Windows Vista и более поздних версиях, должны вызывать [**жетстрингскриптс**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span><span class="sxs-lookup"><span data-stu-id="36761-107">Applications that only run on Windows Vista and later should call [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="36761-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36761-108">Syntax</span></span>


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="36761-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="36761-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36761-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36761-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36761-111">Флаги, указывающие параметры для получения скрипта.</span><span class="sxs-lookup"><span data-stu-id="36761-111">Flags specifying options for script retrieval.</span></span>



| <span data-ttu-id="36761-112">Значение</span><span class="sxs-lookup"><span data-stu-id="36761-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="36761-113">Значение</span><span class="sxs-lookup"><span data-stu-id="36761-113">Meaning</span></span>                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <span data-ttu-id="36761-114"><dt>**GSS \_ допускает \_ унаследованные \_ Общие**</dt></span><span class="sxs-lookup"><span data-stu-id="36761-114"><dt>**GSS\_ALLOW\_INHERITED\_COMMON**</dt></span></span> </dl> | <span data-ttu-id="36761-115">Получение сведений о скрипте "Каии" (УНАСЛЕДОВАНном) и "Зиии" (COMMON).</span><span class="sxs-lookup"><span data-stu-id="36761-115">Retrieve "Qaii" (INHERITED) and "Zyyy" (COMMON) script information.</span></span> <span data-ttu-id="36761-116">Это значение не влияет на обработку неназначенных символов.</span><span class="sxs-lookup"><span data-stu-id="36761-116">This value does not affect the processing of unassigned characters.</span></span> <span data-ttu-id="36761-117">Эти символы во входной строке всегда приводят к тому, что "ZZZZ" (неназначенный скрипт) будет отображаться в строке скрипта.</span><span class="sxs-lookup"><span data-stu-id="36761-117">These characters in the input string always cause a "Zzzz" (UNASSIGNED script) to appear in the script string.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="36761-118">По умолчанию эта функция игнорирует все наследуемые или общие символы во входной строке Юникода.</span><span class="sxs-lookup"><span data-stu-id="36761-118">By default, this function ignores any inherited or common characters in the input Unicode string.</span></span> <span data-ttu-id="36761-119">Если GSS \_ допускает \_ наследование унаследованных \_ типов, то ни "Каии", ни "зиии" не будут отображаться в строке скрипта, даже если входная строка содержит такие символы.</span><span class="sxs-lookup"><span data-stu-id="36761-119">If GSS\_ALLOW\_INHERITED\_COMMON is not set, neither "Qaii" nor "Zyyy" will appear in the script string, even if the input string contains such characters.</span></span> <span data-ttu-id="36761-120">Если \_ параметр GSS допускает \_ наследование наследуемых \_ типов, и если входная строка содержит унаследованные и (или) общие символы, в строке скрипта появятся "Каии" и/или "зиии".</span><span class="sxs-lookup"><span data-stu-id="36761-120">If GSS\_ALLOW\_INHERITED\_COMMON is set, and if the input string contains inherited and/or common characters, "Qaii" and/or "Zyyy" appear in the script string.</span></span> <span data-ttu-id="36761-121">См. раздел «Примечания».</span><span class="sxs-lookup"><span data-stu-id="36761-121">See the Remarks section.</span></span>

 

</dd> <dt>

<span data-ttu-id="36761-122">*лпстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36761-122">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36761-123">Указатель на строку в Юникоде для анализа.</span><span class="sxs-lookup"><span data-stu-id="36761-123">Pointer to the Unicode string to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="36761-124">*кчстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36761-124">*cchString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36761-125">Размер (в символах) строки Юникода, указанной параметром *лпстринг*.</span><span class="sxs-lookup"><span data-stu-id="36761-125">Size, in characters, of the Unicode string indicated by *lpString*.</span></span> <span data-ttu-id="36761-126">Приложение задает для этого параметра значение-1, если строка завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="36761-126">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="36761-127">Если приложение устанавливает для этого параметра значение 0, функция получает строку в Юникоде null (L " \\ 0") в *лпскриптс* и возвращает значение 1.</span><span class="sxs-lookup"><span data-stu-id="36761-127">If the application sets this parameter to 0, the function retrieves a null Unicode string (L"\\0") in *lpScripts* and returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="36761-128">*лпскриптс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="36761-128">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36761-129">Указатель на буфер, в котором эта функция получает строку, завершающуюся нулем, представляющую список скриптов, с использованием 4-символьной нотации, используемой в [стандарте ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="36761-129">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="36761-130">Имя каждого сценария состоит из четырех латинских символов, а имена извлекаются в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="36761-130">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="36761-131">За каждым именем, включая Последнее, следует точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="36761-131">Each name, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="36761-132">Кроме того, этот параметр может содержать **значение NULL** , если *кчскриптс* имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="36761-132">Alternatively, this parameter can contain **NULL** if *cchScripts* set to 0.</span></span> <span data-ttu-id="36761-133">В этом случае функция возвращает необходимый размер буфера скрипта.</span><span class="sxs-lookup"><span data-stu-id="36761-133">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="36761-134">*кчскриптс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36761-134">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36761-135">Размер в символах для буфера скрипта, указанного параметром *лпскриптс*.</span><span class="sxs-lookup"><span data-stu-id="36761-135">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="36761-136">Кроме того, приложение может установить этот параметр в значение 0.</span><span class="sxs-lookup"><span data-stu-id="36761-136">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="36761-137">В этом случае функция получает **значение NULL** в *лпскриптс* и возвращает необходимый размер буфера скрипта.</span><span class="sxs-lookup"><span data-stu-id="36761-137">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36761-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36761-138">Return value</span></span>

<span data-ttu-id="36761-139">Возвращает число символов, полученных в выходном буфере, включая завершающий нуль-символ, если для параметра *кчскриптс* задано ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="36761-139">Returns the number of characters retrieved in the output buffer, including a terminating null character, if successful and *cchScripts* is set to a nonzero value.</span></span> <span data-ttu-id="36761-140">Функция возвращает 1, чтобы указать, что ни один скрипт не найден, например, если входная строка содержит только общие или УНАСЛЕДОВАНные символы, а GSS \_ разрешает \_ унаследованные \_ Общие, не задано.</span><span class="sxs-lookup"><span data-stu-id="36761-140">The function returns 1 to indicate that no script has been found, for example, when the input string only contains COMMON or INHERITED characters and GSS\_ALLOW\_INHERITED\_COMMON is not set.</span></span> <span data-ttu-id="36761-141">Учитывая, что каждый найденный скрипт добавляет пять символов (четыре символа + разделитель), простая математическая операция предоставляет количество сценариев ( \_ код возврата 1)/5.</span><span class="sxs-lookup"><span data-stu-id="36761-141">Given that each found script adds five characters (four characters + delimiter), a simple mathematical operation provides the script count as (return\_code - 1) / 5.</span></span>

<span data-ttu-id="36761-142">Если функция завершается удачно и значение *кчскриптс* равно 0, то возвращаемое значение имеет необходимый размер (в символах, включая завершающий нуль-символ) для буфера скрипта.</span><span class="sxs-lookup"><span data-stu-id="36761-142">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span> <span data-ttu-id="36761-143">Счетчик скриптов описан выше.</span><span class="sxs-lookup"><span data-stu-id="36761-143">The script count is as described above.</span></span>

<span data-ttu-id="36761-144">Функция возвращает 0, если она не выполнена.</span><span class="sxs-lookup"><span data-stu-id="36761-144">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="36761-145">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="36761-145">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="36761-146">Ошибка \_ баддб.</span><span class="sxs-lookup"><span data-stu-id="36761-146">ERROR\_BADDB.</span></span> <span data-ttu-id="36761-147">Функция не может получить доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="36761-147">The function could not access the data.</span></span> <span data-ttu-id="36761-148">Такая ситуация обычно не возникает, и обычно указывает на неправильную установку, на диск или на проблему.</span><span class="sxs-lookup"><span data-stu-id="36761-148">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="36761-149">Ошибка \_ : недостаточный \_ Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="36761-149">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="36761-150">Указанный размер буфера не достаточен или имеет неправильное значение **null**.</span><span class="sxs-lookup"><span data-stu-id="36761-150">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="36761-151">Ошибка \_ : недопустимые \_ флаги.</span><span class="sxs-lookup"><span data-stu-id="36761-151">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="36761-152">Указаны недопустимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="36761-152">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="36761-153">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="36761-153">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="36761-154">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="36761-154">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="36761-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36761-155">Remarks</span></span>

<span data-ttu-id="36761-156">Эта функция полезна как часть стратегии по устранению проблем безопасности, связанных с [международными доменными именами (IDNs)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="36761-156">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="36761-157">Определение скрипта основано на значениях скриптов, опубликованных консорциумом Unicode в <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> , за исключением того, что неназначенные символы имеют значение «ZZZZ» (не назначено) вместо «зиии» (Common).</span><span class="sxs-lookup"><span data-stu-id="36761-157">The script determination is based on the script values published by the Unicode Consortium in <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt>, except that the unassigned characters have the value "Zzzz" (UNASSIGNED) instead of "Zyyy" (COMMON).</span></span>

<span data-ttu-id="36761-158">Ниже приведены некоторые примеры поведения этой функции.</span><span class="sxs-lookup"><span data-stu-id="36761-158">Here are some examples of the behavior of this function:</span></span>



<span data-ttu-id="36761-159">Входная строка</span><span class="sxs-lookup"><span data-stu-id="36761-159">Input string</span></span>

<span data-ttu-id="36761-160">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="36761-160">*dwFlags*</span></span>

<span data-ttu-id="36761-161">*лпскриптс*</span><span class="sxs-lookup"><span data-stu-id="36761-161">*lpScripts*</span></span>

<span data-ttu-id="36761-162">Скрипты</span><span class="sxs-lookup"><span data-stu-id="36761-162">Scripts</span></span>

<span data-ttu-id="36761-163">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="36761-163">Microsoft.com</span></span>

<span data-ttu-id="36761-164">0</span><span class="sxs-lookup"><span data-stu-id="36761-164">0</span></span>

<span data-ttu-id="36761-165">ЛАТН;</span><span class="sxs-lookup"><span data-stu-id="36761-165">Latn;</span></span>

<span data-ttu-id="36761-166">Латиница</span><span class="sxs-lookup"><span data-stu-id="36761-166">Latin</span></span>

<span data-ttu-id="36761-167">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="36761-167">Microsoft.com</span></span>

<span data-ttu-id="36761-168">GSS \_ допускает \_ унаследованные \_ Общие</span><span class="sxs-lookup"><span data-stu-id="36761-168">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="36761-169">ЛАТН; Зиии;</span><span class="sxs-lookup"><span data-stu-id="36761-169">Latn;Zyyy;</span></span>

<span data-ttu-id="36761-170">Латиница + общие</span><span class="sxs-lookup"><span data-stu-id="36761-170">Latin + Common</span></span>

<span data-ttu-id="36761-171">$ {ROWSPAN2} $Ni Ñо $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="36761-171">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="36761-172">004E 0069 0241 006F</span><span class="sxs-lookup"><span data-stu-id="36761-172">004E 0069 0241 006F</span></span>

<span data-ttu-id="36761-173">$ {ROWSPAN2} $GSS \_ Разрешить \_ унаследованные \_ Общие $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="36761-173">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="36761-174">$ {ROWSPAN2} $Latn; $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="36761-174">${ROWSPAN2}$Latn;${REMOVE}$</span></span>  

<span data-ttu-id="36761-175">$ {ROWSPAN2} $Latin $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="36761-175">${ROWSPAN2}$Latin${REMOVE}$</span></span>  

<span data-ttu-id="36761-176">Использует Латинская СТРОЧная БУКВа N с ТИЛЬДой</span><span class="sxs-lookup"><span data-stu-id="36761-176">Uses LATIN SMALL LETTER N WITH TILDE</span></span>

<span data-ttu-id="36761-177">$ {ROWSPAN2} $Ni Ñо $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="36761-177">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="36761-178">004E 0069 006E 0303 006F</span><span class="sxs-lookup"><span data-stu-id="36761-178">004E 0069 006E 0303 006F</span></span>

<span data-ttu-id="36761-179">$ {ROWSPAN2} $GSS \_ Разрешить \_ унаследованные \_ Общие $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="36761-179">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="36761-180">$ {ROWSPAN2} $Latn; Каии; $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="36761-180">${ROWSPAN2}$Latn;Qaii;${REMOVE}$</span></span>  

<span data-ttu-id="36761-181">$ {ROWSPAN2} $Latin + унаследовано $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="36761-181">${ROWSPAN2}$Latin + Inherited${REMOVE}$</span></span>  

<span data-ttu-id="36761-182">Использует сочетание ТИЛЬДы</span><span class="sxs-lookup"><span data-stu-id="36761-182">Uses COMBINING TILDE</span></span>

<span data-ttu-id="36761-183">$ {ROWSPAN2} $Sp ООФ $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="36761-183">${ROWSPAN2}$Spооf${REMOVE}$</span></span>  

<span data-ttu-id="36761-184">0053 0070 043e 043e 0066</span><span class="sxs-lookup"><span data-stu-id="36761-184">0053 0070 043e 043e 0066</span></span>

<span data-ttu-id="36761-185">$ {ROWSPAN2} $0 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="36761-185">${ROWSPAN2}$0${REMOVE}$</span></span>  

<span data-ttu-id="36761-186">$ {ROWSPAN2} $Latn; Цирл; $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="36761-186">${ROWSPAN2}$Latn;Cyrl;${REMOVE}$</span></span>  

<span data-ttu-id="36761-187">$ {ROWSPAN2} $Latin + кириллица $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="36761-187">${ROWSPAN2}$Latin + Cyrillic${REMOVE}$</span></span>  

<span data-ttu-id="36761-188">Используется КИРИЛЛическая СТРОЧная БУКВа O</span><span class="sxs-lookup"><span data-stu-id="36761-188">Uses CYRILLIC SMALL LETTER O</span></span>

<span data-ttu-id="36761-189"></span><span class="sxs-lookup"><span data-stu-id="36761-189"></span></span>

<span data-ttu-id="36761-190">U + F000</span><span class="sxs-lookup"><span data-stu-id="36761-190">U+f000</span></span>

<span data-ttu-id="36761-191">0</span><span class="sxs-lookup"><span data-stu-id="36761-191">0</span></span>

<span data-ttu-id="36761-192">ZZZZ</span><span class="sxs-lookup"><span data-stu-id="36761-192">Zzzz;</span></span>

<span data-ttu-id="36761-193">"Не присвоено"</span><span class="sxs-lookup"><span data-stu-id="36761-193">Unassigned</span></span>

<span data-ttu-id="36761-194"></span><span class="sxs-lookup"><span data-stu-id="36761-194"></span></span>

<span data-ttu-id="36761-195">U + F000</span><span class="sxs-lookup"><span data-stu-id="36761-195">U+f000</span></span>

<span data-ttu-id="36761-196">GSS \_ допускает \_ унаследованные \_ Общие</span><span class="sxs-lookup"><span data-stu-id="36761-196">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="36761-197">ZZZZ</span><span class="sxs-lookup"><span data-stu-id="36761-197">Zzzz;</span></span>

<span data-ttu-id="36761-198">"Не присвоено"</span><span class="sxs-lookup"><span data-stu-id="36761-198">Unassigned</span></span>



 

<span data-ttu-id="36761-199">Требуемый заголовочный файл и библиотека DLL являются частью скачивания веб- [API для Межязыкового доменного имени Майкрософт (IDN)](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) , доступного в [центре загрузки MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="36761-199">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="36761-200">Требования</span><span class="sxs-lookup"><span data-stu-id="36761-200">Requirements</span></span>



| <span data-ttu-id="36761-201">Требование</span><span class="sxs-lookup"><span data-stu-id="36761-201">Requirement</span></span> | <span data-ttu-id="36761-202">Значение</span><span class="sxs-lookup"><span data-stu-id="36761-202">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36761-203">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36761-203">Minimum supported client</span></span><br/> | <span data-ttu-id="36761-204">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="36761-204">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="36761-205">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36761-205">Minimum supported server</span></span><br/> | <span data-ttu-id="36761-206">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36761-206">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="36761-207">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="36761-207">Redistributable</span></span><br/>          | <span data-ttu-id="36761-208">API для межязыкового доменного имени Майкрософт (IDN) в Windows XP (SP2 или более поздней версии), Windows Server 2003 (с пакетом обновления 1 (SP1) или более поздней версии) или Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36761-208">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="36761-209">Header</span><span class="sxs-lookup"><span data-stu-id="36761-209">Header</span></span><br/>                   | <dl> <span data-ttu-id="36761-210"><dt>Идндл. h</dt></span><span class="sxs-lookup"><span data-stu-id="36761-210"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="36761-211">DLL</span><span class="sxs-lookup"><span data-stu-id="36761-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36761-212"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36761-212"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="36761-213">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36761-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36761-214">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="36761-214">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="36761-215">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="36761-215">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="36761-216">Обработка международных доменных имен (IDNs)</span><span class="sxs-lookup"><span data-stu-id="36761-216">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="36761-217">**довнлевелжетлокалескриптс**</span><span class="sxs-lookup"><span data-stu-id="36761-217">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="36761-218">**довнлевелверифискриптс**</span><span class="sxs-lookup"><span data-stu-id="36761-218">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="36761-219">**жетстрингскриптс**</span><span class="sxs-lookup"><span data-stu-id="36761-219">**GetStringScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 
