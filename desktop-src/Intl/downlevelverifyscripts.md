---
description: Сравнивает два перечисленных списка скриптов.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Функция Довнлевелверифискриптс (Идндл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664319"
---
# <a name="downlevelverifyscripts-function"></a><span data-ttu-id="114c5-103">Функция Довнлевелверифискриптс</span><span class="sxs-lookup"><span data-stu-id="114c5-103">DownlevelVerifyScripts function</span></span>

<span data-ttu-id="114c5-104">Сравнивает два перечисленных списка скриптов.</span><span class="sxs-lookup"><span data-stu-id="114c5-104">Compares two enumerated lists of scripts.</span></span>

> [!Note]  
> <span data-ttu-id="114c5-105">Эта функция используется только приложениями, работающими в операционных системах, предшествующих Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="114c5-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="114c5-106">Для его использования требуется загружаемый пакет.</span><span class="sxs-lookup"><span data-stu-id="114c5-106">Its use requires the download package.</span></span> <span data-ttu-id="114c5-107">Приложения, которые работают только в Windows Vista и более поздних версиях, должны вызывать [**верифискриптс**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span><span class="sxs-lookup"><span data-stu-id="114c5-107">Applications that only run on Windows Vista and later should call [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="114c5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="114c5-108">Syntax</span></span>


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a><span data-ttu-id="114c5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="114c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="114c5-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="114c5-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="114c5-111">Флаги, указывающие параметры проверки сценария.</span><span class="sxs-lookup"><span data-stu-id="114c5-111">Flags specifying script verification options.</span></span>



| <span data-ttu-id="114c5-112">Значение</span><span class="sxs-lookup"><span data-stu-id="114c5-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="114c5-113">Значение</span><span class="sxs-lookup"><span data-stu-id="114c5-113">Meaning</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <span data-ttu-id="114c5-114"><dt>**VS \_ Разрешить \_ латиницу**</dt></span><span class="sxs-lookup"><span data-stu-id="114c5-114"><dt>**VS\_ALLOW\_LATIN**</dt></span></span> </dl> | <span data-ttu-id="114c5-115">Разрешить "ЛАТН" (Латинский скрипт) в списке тестов, даже если он отсутствует в списке языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="114c5-115">Allow "Latn" (Latin script) in the test list, even if it is not in the locale list.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="114c5-116">*лплокалескриптс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="114c5-116">*lpLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="114c5-117">Указатель на список языковых стандартов — список сценариев для заданного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="114c5-117">Pointer to the locale list, the enumerated list of scripts for a given locale.</span></span> <span data-ttu-id="114c5-118">Этот список обычно заполняется вызовом [**довнлевелжетлокалескриптс**](downlevelgetlocalescripts.md).</span><span class="sxs-lookup"><span data-stu-id="114c5-118">This list is typically populated by calling [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="114c5-119">*кчлокалескриптс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="114c5-119">*cchLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="114c5-120">Размер строки (в символах), указанной параметром *лплокалескриптс*.</span><span class="sxs-lookup"><span data-stu-id="114c5-120">Size, in characters, of the string indicated by *lpLocaleScripts*.</span></span> <span data-ttu-id="114c5-121">Приложение задает для этого параметра значение-1, если строка завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="114c5-121">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="114c5-122">Если этот параметр имеет значение 0, функция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="114c5-122">If this parameter is set to 0, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="114c5-123">*лптестскриптс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="114c5-123">*lpTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="114c5-124">Указатель на список тестов, второй нумерованный список скриптов.</span><span class="sxs-lookup"><span data-stu-id="114c5-124">Pointer to the test list, a second enumerated list of scripts.</span></span> <span data-ttu-id="114c5-125">Этот список обычно заполняется вызовом [**довнлевелжетстрингскриптс**](downlevelgetstringscripts.md).</span><span class="sxs-lookup"><span data-stu-id="114c5-125">This list is typically populated by calling [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="114c5-126">*кчтестскриптс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="114c5-126">*cchTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="114c5-127">Размер строки (в символах), указанной параметром *лптестскриптс*.</span><span class="sxs-lookup"><span data-stu-id="114c5-127">Size, in characters, of the string indicated by *lpTestScripts*.</span></span> <span data-ttu-id="114c5-128">Приложение задает для этого параметра значение-1, если строка завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="114c5-128">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="114c5-129">Если этот параметр имеет значение 0, функция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="114c5-129">If this parameter is set to 0, the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="114c5-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="114c5-130">Return value</span></span>

<span data-ttu-id="114c5-131">Возвращает **значение true** , если список тестов не пуст и все элементы в списке также включены в список языковых стандартов.</span><span class="sxs-lookup"><span data-stu-id="114c5-131">Returns **TRUE** if the test list is non-empty and all items in the list are also included in the locale list.</span></span> <span data-ttu-id="114c5-132">В противном случае функция возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="114c5-132">Otherwise, the function returns **FALSE**.</span></span>

<span data-ttu-id="114c5-133">Возвращаемое значение **false** может означать, что список тестов содержит элемент, отсутствующий в списке языкового стандарта, или может указывать на ошибку.</span><span class="sxs-lookup"><span data-stu-id="114c5-133">A return value of **FALSE** can indicate that the test list contains an item that is not in the locale list, or it can indicate an error.</span></span> <span data-ttu-id="114c5-134">Чтобы различать эти два варианта, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="114c5-134">To distinguish between these two cases, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="114c5-135">Если **довнлевелверифискриптс** успешно определил, что в списке тестов присутствует элемент, отсутствующий в списке языкового стандарта, **GetLastError** возвращает ошибку \_ Success.</span><span class="sxs-lookup"><span data-stu-id="114c5-135">If **DownlevelVerifyScripts** has successfully determined that there is an item in the test list that is not in the locale list, **GetLastError** returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="114c5-136">В противном случае **GetLastError** может вернуть один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="114c5-136">Otherwise, **GetLastError** can return one of the following error codes:</span></span>

-   <span data-ttu-id="114c5-137">Ошибка \_ : недопустимые \_ флаги.</span><span class="sxs-lookup"><span data-stu-id="114c5-137">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="114c5-138">Указаны недопустимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="114c5-138">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="114c5-139">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="114c5-139">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="114c5-140">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="114c5-140">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="114c5-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="114c5-141">Remarks</span></span>

<span data-ttu-id="114c5-142">Эта функция сравнивает строки, например "ЛАТН; Цирл; ", который состоит из последовательности из четырех символьных имен, с каждым именем сценария, за которым следует точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="114c5-142">This function compares strings, such as "Latn;Cyrl;", that consist of a series of 4-character script names, with each script name followed by a semicolon.</span></span> <span data-ttu-id="114c5-143">Кроме того, в нем есть особый случай того, что Латинский скрипт часто используется на языках и национальных стандартах, для которых он не является машинным.</span><span class="sxs-lookup"><span data-stu-id="114c5-143">It also has a special case to account for the fact that the Latin script is often used in languages and locales for which it is not native.</span></span>

<span data-ttu-id="114c5-144">Эта функция полезна как часть стратегии по устранению проблем безопасности, связанных с [международными доменными именами (IDNs)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="114c5-144">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="114c5-145">Ниже приведены примеры возврата этой функции и последующего вызова [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) в различных сценариях.</span><span class="sxs-lookup"><span data-stu-id="114c5-145">The following are examples of the return of this function and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in various scenarios.</span></span> <span data-ttu-id="114c5-146">В двух последних примерах показано, соответственно, что в списке тестов отсутствует завершающая точка с запятой (неправильно сформированная строка) и в случае, когда список тестов пуст.</span><span class="sxs-lookup"><span data-stu-id="114c5-146">The last two examples illustrate, respectively, a case in which the test list lacks a terminating semicolon (malformed string) and a case in which the test list is empty.</span></span>



| <span data-ttu-id="114c5-147">Строка "языковой стандарт"</span><span class="sxs-lookup"><span data-stu-id="114c5-147">"Locale" string</span></span> | <span data-ttu-id="114c5-148">Строка "Test"</span><span class="sxs-lookup"><span data-stu-id="114c5-148">"Test" string</span></span> | <span data-ttu-id="114c5-149">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="114c5-149">*dwFlags*</span></span>        | <span data-ttu-id="114c5-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="114c5-150">Return value</span></span> | <span data-ttu-id="114c5-151">Обратная GetLastError</span><span class="sxs-lookup"><span data-stu-id="114c5-151">GetLastError return</span></span>       |
|-----------------|---------------|------------------|--------------|---------------------------|
| <span data-ttu-id="114c5-152">Хани; Хира; Знаков</span><span class="sxs-lookup"><span data-stu-id="114c5-152">Hani;Hira;Kana;</span></span> | <span data-ttu-id="114c5-153">Хани;</span><span class="sxs-lookup"><span data-stu-id="114c5-153">Hani;</span></span>         | <span data-ttu-id="114c5-154">Н/Д</span><span class="sxs-lookup"><span data-stu-id="114c5-154">N/A</span></span>              | <span data-ttu-id="114c5-155">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="114c5-155">**TRUE**</span></span>     | <span data-ttu-id="114c5-156">Н/Д</span><span class="sxs-lookup"><span data-stu-id="114c5-156">N/A</span></span>                       |
| <span data-ttu-id="114c5-157">Хани; Хира; Знаков</span><span class="sxs-lookup"><span data-stu-id="114c5-157">Hani;Hira;Kana;</span></span> | <span data-ttu-id="114c5-158">Хани; ЛАТН;</span><span class="sxs-lookup"><span data-stu-id="114c5-158">Hani;Latn;</span></span>    | <span data-ttu-id="114c5-159">0</span><span class="sxs-lookup"><span data-stu-id="114c5-159">0</span></span>                | <span data-ttu-id="114c5-160">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="114c5-160">**FALSE**</span></span>    | <span data-ttu-id="114c5-161">Ошибка при \_ успешном выполнении</span><span class="sxs-lookup"><span data-stu-id="114c5-161">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="114c5-162">Хани; Хира; Знаков</span><span class="sxs-lookup"><span data-stu-id="114c5-162">Hani;Hira;Kana;</span></span> | <span data-ttu-id="114c5-163">Хани; ЛАТН;</span><span class="sxs-lookup"><span data-stu-id="114c5-163">Hani;Latn;</span></span>    | <span data-ttu-id="114c5-164">VS \_ Разрешить \_ латиницу</span><span class="sxs-lookup"><span data-stu-id="114c5-164">VS\_ALLOW\_LATIN</span></span> | <span data-ttu-id="114c5-165">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="114c5-165">**TRUE**</span></span>     | <span data-ttu-id="114c5-166">Н/Д</span><span class="sxs-lookup"><span data-stu-id="114c5-166">N/A</span></span>                       |
| <span data-ttu-id="114c5-167">Хани; Хира; Знаков</span><span class="sxs-lookup"><span data-stu-id="114c5-167">Hani;Hira;Kana;</span></span> | <span data-ttu-id="114c5-168">Цирл;</span><span class="sxs-lookup"><span data-stu-id="114c5-168">Cyrl;</span></span>         | <span data-ttu-id="114c5-169">Н/Д</span><span class="sxs-lookup"><span data-stu-id="114c5-169">N/A</span></span>              | <span data-ttu-id="114c5-170">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="114c5-170">**FALSE**</span></span>    | <span data-ttu-id="114c5-171">Ошибка при \_ успешном выполнении</span><span class="sxs-lookup"><span data-stu-id="114c5-171">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="114c5-172">Хани; Хира; Знаков</span><span class="sxs-lookup"><span data-stu-id="114c5-172">Hani;Hira;Kana;</span></span> | <span data-ttu-id="114c5-173">Цирл;</span><span class="sxs-lookup"><span data-stu-id="114c5-173">Cyrl;</span></span>         | <span data-ttu-id="114c5-174">Н/Д</span><span class="sxs-lookup"><span data-stu-id="114c5-174">N/A</span></span>              | <span data-ttu-id="114c5-175">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="114c5-175">**FALSE**</span></span>    | <span data-ttu-id="114c5-176">Ошибка \_ недопустимого \_ параметра</span><span class="sxs-lookup"><span data-stu-id="114c5-176">ERROR\_INVALID\_PARAMETER</span></span> |
| <span data-ttu-id="114c5-177">Хани; Хира; Знаков</span><span class="sxs-lookup"><span data-stu-id="114c5-177">Hani;Hira;Kana;</span></span> |               | <span data-ttu-id="114c5-178">Н/Д</span><span class="sxs-lookup"><span data-stu-id="114c5-178">N/A</span></span>              | <span data-ttu-id="114c5-179">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="114c5-179">**FALSE**</span></span>    | <span data-ttu-id="114c5-180">Ошибка при \_ успешном выполнении</span><span class="sxs-lookup"><span data-stu-id="114c5-180">ERROR\_SUCCESS</span></span>            |



 

<span data-ttu-id="114c5-181">Требуемый заголовочный файл и библиотека DLL являются частью скачивания веб- [API для Межязыкового доменного имени Майкрософт (IDN)](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , доступного в [центре загрузки MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="114c5-181">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="114c5-182">Требования</span><span class="sxs-lookup"><span data-stu-id="114c5-182">Requirements</span></span>



| <span data-ttu-id="114c5-183">Требование</span><span class="sxs-lookup"><span data-stu-id="114c5-183">Requirement</span></span> | <span data-ttu-id="114c5-184">Значение</span><span class="sxs-lookup"><span data-stu-id="114c5-184">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="114c5-185">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="114c5-185">Minimum supported client</span></span><br/> | <span data-ttu-id="114c5-186">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="114c5-186">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                  |
| <span data-ttu-id="114c5-187">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="114c5-187">Minimum supported server</span></span><br/> | <span data-ttu-id="114c5-188">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="114c5-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                         |
| <span data-ttu-id="114c5-189">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="114c5-189">Redistributable</span></span><br/>          | <span data-ttu-id="114c5-190">API для межязыкового доменного имени Майкрософт (IDN) — Windows XP с пакетом обновления 2 (SP2), Windows Server 2003 с пакетом обновления SP1, Орвиндовс Vista</span><span class="sxs-lookup"><span data-stu-id="114c5-190">Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP with SP2,Windows Server 2003 with SP1, orWindows Vista</span></span><br/> |
| <span data-ttu-id="114c5-191">Header</span><span class="sxs-lookup"><span data-stu-id="114c5-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="114c5-192"><dt>Идндл. h</dt></span><span class="sxs-lookup"><span data-stu-id="114c5-192"><dt>Idndl.h</dt></span></span> </dl>                                                           |
| <span data-ttu-id="114c5-193">DLL</span><span class="sxs-lookup"><span data-stu-id="114c5-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="114c5-194"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="114c5-194"><dt>Idndl.dll</dt></span></span> </dl>                                                         |



## <a name="see-also"></a><span data-ttu-id="114c5-195">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="114c5-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="114c5-196">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="114c5-196">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="114c5-197">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="114c5-197">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="114c5-198">Обработка международных доменных имен (IDNs)</span><span class="sxs-lookup"><span data-stu-id="114c5-198">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="114c5-199">**довнлевелжетлокалескриптс**</span><span class="sxs-lookup"><span data-stu-id="114c5-199">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="114c5-200">**довнлевелжетстрингскриптс**</span><span class="sxs-lookup"><span data-stu-id="114c5-200">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="114c5-201">**верифискриптс**</span><span class="sxs-lookup"><span data-stu-id="114c5-201">**VerifyScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
