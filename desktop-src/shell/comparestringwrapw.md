---
description: Сравнивает две строки символов Юникода с использованием заданного языкового стандарта.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: Функция Компарестрингврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 0731182f5c01ad56db722972628d2cbe39373835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984352"
---
# <a name="comparestringwrapw-function"></a><span data-ttu-id="d6d9d-103">Функция Компарестрингврапв</span><span class="sxs-lookup"><span data-stu-id="d6d9d-103">CompareStringWrapW function</span></span>

<span data-ttu-id="d6d9d-104">\[**Компарестрингврапв** доступен для использования в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-104">\[**CompareStringWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="d6d9d-105">Он будет недоступен в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="d6d9d-106">На своем месте следует использовать [**компарестрингв**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) .\]</span><span class="sxs-lookup"><span data-stu-id="d6d9d-106">You should use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in its place.\]</span></span>

<span data-ttu-id="d6d9d-107">Сравнивает две строки символов Юникода с использованием заданного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-107">Compares two Unicode character strings, using a specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="d6d9d-108">**Компарестрингврапв** — это оболочка для функции **компарестрингв** .</span><span class="sxs-lookup"><span data-stu-id="d6d9d-108">**CompareStringWrapW** is a wrapper for the **CompareStringW** function.</span></span> <span data-ttu-id="d6d9d-109">Дополнительные замечания об использовании см. на странице [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) .</span><span class="sxs-lookup"><span data-stu-id="d6d9d-109">See the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d6d9d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6d9d-110">Syntax</span></span>


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a><span data-ttu-id="d6d9d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6d9d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6d9d-112">*Языковой стандарт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6d9d-112">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d9d-113">Тип: **LCID**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-113">Type: **LCID**</span></span>

<span data-ttu-id="d6d9d-114">Идентификатор локали, используемый для сравнения.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-114">A locale identifier used for the comparison.</span></span> <span data-ttu-id="d6d9d-115">Этот параметр может быть одним из следующих заранее определенных идентификаторов языкового стандарта или идентификатором локали, созданным в макросе [**макелЦид**](/windows/win32/api/winnt/nf-winnt-makelcid) .</span><span class="sxs-lookup"><span data-stu-id="d6d9d-115">This parameter can be one of the following predefined locale identifiers or a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="d6d9d-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**система языкового стандарта \_ \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="d6d9d-117">Язык системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-117">The system's default locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="d6d9d-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_Пользовательская Национальная настройка \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="d6d9d-119">Языковой стандарт текущего пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-119">The current user's default locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d6d9d-120">*двкмпфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6d9d-120">*dwCmpFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d9d-121">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-121">Type: **DWORD**</span></span>

<span data-ttu-id="d6d9d-122">Флаги, указывающие, как функция сравнивает две строки.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-122">The flags that indicate how the function compares the two strings.</span></span> <span data-ttu-id="d6d9d-123">По умолчанию эти флаги не заданы.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-123">By default, these flags are not set.</span></span> <span data-ttu-id="d6d9d-124">Задайте значение 0, чтобы получить поведение по умолчанию или любое сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-124">Set to zero to get the default behavior or to any combination of the following values.</span></span>

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span data-ttu-id="d6d9d-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**НОРМа \_ IGNORECASE**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORM\_IGNORECASE**</span></span>


</dt> <dd>

<span data-ttu-id="d6d9d-126">Не учитывать регистр.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-126">Ignore case.</span></span>

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span data-ttu-id="d6d9d-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**НОРМа \_ игнореканатипе**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORM\_IGNOREKANATYPE**</span></span>


</dt> <dd>

<span data-ttu-id="d6d9d-128">Не различать символы хирагана и катакана.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-128">Do not differentiate between Hiragana and Katakana characters.</span></span> <span data-ttu-id="d6d9d-129">Соответствующие символы хирагана и катакана сравниваются как равные.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-129">Corresponding Hiragana and Katakana characters compare as equal.</span></span>

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span data-ttu-id="d6d9d-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**НОРМа \_ игноренонспаце**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORM\_IGNORENONSPACE**</span></span>


</dt> <dd>

<span data-ttu-id="d6d9d-131">Пропускать несамостоятельные символы.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-131">Ignore nonspacing characters.</span></span>

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span data-ttu-id="d6d9d-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**НОРМа \_ игноресимболс**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORM\_IGNORESYMBOLS**</span></span>


</dt> <dd>

<span data-ttu-id="d6d9d-133">Игнорировать символы.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-133">Ignore symbols.</span></span>

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span data-ttu-id="d6d9d-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**НОРМа \_ игноревидс**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORM\_IGNOREWIDTH**</span></span>


</dt> <dd>

<span data-ttu-id="d6d9d-135">Не следует различать однобайтовые символы и один и тот же символ в виде двухбайтовых символов.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-135">Do not differentiate between a single-byte character and the same character as a double-byte character.</span></span>

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span data-ttu-id="d6d9d-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**Сортировать \_ стрингсорт**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**SORT\_STRINGSORT**</span></span>


</dt> <dd>

<span data-ttu-id="d6d9d-137">Считать знаки препинания такими же, как символы.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-137">Treat punctuation the same as symbols.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d6d9d-138">*lpString1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6d9d-138">*lpString1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d9d-139">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-139">Type: **LPCWSTR**</span></span>

<span data-ttu-id="d6d9d-140">Указатель на первую строку Юникода для сравнения.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-140">A pointer to the first Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="d6d9d-141">*cchCount1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6d9d-141">*cchCount1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d9d-142">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-142">Type: **int**</span></span>

<span data-ttu-id="d6d9d-143">Число символов в строке, на которое указывает параметр *lpString1* .</span><span class="sxs-lookup"><span data-stu-id="d6d9d-143">The number of characters in the string pointed to by the *lpString1* parameter.</span></span> <span data-ttu-id="d6d9d-144">Число не содержит завершающего нуль символа.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-144">The count does not include the terminating null character.</span></span> <span data-ttu-id="d6d9d-145">Если этот параметр имеет отрицательное значение, предполагается, что строка завершается нулем, а длина вычисляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-145">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="d6d9d-146">*lpString2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6d9d-146">*lpString2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d9d-147">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-147">Type: **LPCWSTR**</span></span>

<span data-ttu-id="d6d9d-148">Указатель на вторую сравниваемую строку Юникода.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-148">A pointer to the second Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="d6d9d-149">*cchCount2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6d9d-149">*cchCount2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d9d-150">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-150">Type: **int**</span></span>

<span data-ttu-id="d6d9d-151">Число символов в строке, на которое указывает параметр *lpString2* .</span><span class="sxs-lookup"><span data-stu-id="d6d9d-151">The number of characters in the string pointed to by the *lpString2* parameter.</span></span> <span data-ttu-id="d6d9d-152">Число не содержит завершающего нуль символа.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-152">The count does not include the terminating null character.</span></span> <span data-ttu-id="d6d9d-153">Если этот параметр имеет отрицательное значение, предполагается, что строка завершается нулем, а длина вычисляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-153">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6d9d-154">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6d9d-154">Return value</span></span>

<span data-ttu-id="d6d9d-155">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-155">Type: **int**</span></span>

<span data-ttu-id="d6d9d-156">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-156">If the function fails, the return value is zero.</span></span> <span data-ttu-id="d6d9d-157">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="d6d9d-157">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="d6d9d-158">**GetLastError** может возвращать один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-158">**GetLastError** may return one of the following error codes.</span></span>

-   <span data-ttu-id="d6d9d-159">Ошибка \_ недопустимых \_ флагов</span><span class="sxs-lookup"><span data-stu-id="d6d9d-159">ERROR\_INVALID\_FLAGS</span></span>
-   <span data-ttu-id="d6d9d-160">Ошибка \_ недопустимого \_ параметра</span><span class="sxs-lookup"><span data-stu-id="d6d9d-160">ERROR\_INVALID\_PARAMETER</span></span>

<span data-ttu-id="d6d9d-161">Если функция выполнена, возвращаемое значение является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-161">If the function succeeds, the return value is one of the following values.</span></span> 

| <span data-ttu-id="d6d9d-162">Требование</span><span class="sxs-lookup"><span data-stu-id="d6d9d-162">Requirement</span></span> | <span data-ttu-id="d6d9d-163">Значение</span><span class="sxs-lookup"><span data-stu-id="d6d9d-163">Value</span></span> |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d9d-164">CSTR \_ меньше \_</span><span class="sxs-lookup"><span data-stu-id="d6d9d-164">CSTR\_LESS\_THAN</span></span>    | <span data-ttu-id="d6d9d-165">Строка, на которую указывает параметр *lpString1* , меньше в лексической величине, чем строка, на которую указывает параметр *lpString2* .</span><span class="sxs-lookup"><span data-stu-id="d6d9d-165">The string pointed to by the *lpString1* parameter is less in lexical value than the string pointed to by the *lpString2* parameter.</span></span> |
| <span data-ttu-id="d6d9d-166">CSTR \_ равно</span><span class="sxs-lookup"><span data-stu-id="d6d9d-166">CSTR\_EQUAL</span></span>         | <span data-ttu-id="d6d9d-167">Строка, на которую указывает *lpString1* , равна значению в лексической строке, на которую указывает *lpString2*.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-167">The string pointed to by *lpString1* is equal in lexical value to the string pointed to by *lpString2*.</span></span>                              |
| <span data-ttu-id="d6d9d-168">CSTR \_ больше \_</span><span class="sxs-lookup"><span data-stu-id="d6d9d-168">CSTR\_GREATER\_THAN</span></span> | <span data-ttu-id="d6d9d-169">Строка, на которую указывает *lpString1* , больше в лексической величине, чем строка, на которую указывает *lpString2*</span><span class="sxs-lookup"><span data-stu-id="d6d9d-169">The string pointed to by *lpString1* is greater in lexical value than the string pointed to by *lpString2*</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="d6d9d-170">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6d9d-170">Remarks</span></span>

<span data-ttu-id="d6d9d-171">**Предупреждение системы безопасности:** Неправильное использование этой функции может привести к нарушению безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-171">**Security Warning:** Using this function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="d6d9d-172">Строки, которые не сравниваются правильно, могут формировать недопустимые входные данные.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-172">Strings that are not compared correctly can produce invalid input.</span></span> <span data-ttu-id="d6d9d-173">Тестовые строки, чтобы убедиться, что они действительны, прежде чем использовать их и предоставить обработчики ошибок.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-173">Test strings to make sure they are valid before using them and provide error handlers.</span></span> <span data-ttu-id="d6d9d-174">Дополнительные сведения см. в разделе [вопросы безопасности: международные функции.](../intl/security-considerations--international-features.md)</span><span class="sxs-lookup"><span data-stu-id="d6d9d-174">For more information, see [Security Considerations: International Features](../intl/security-considerations--international-features.md)</span></span>

<span data-ttu-id="d6d9d-175">Предпочтительным методом является использование [**компарестрингв**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) в сочетании с уровнем Майкрософт для Юникода (мслу).</span><span class="sxs-lookup"><span data-stu-id="d6d9d-175">The preferred method is to use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="d6d9d-176">**Компарестрингврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 45.</span><span class="sxs-lookup"><span data-stu-id="d6d9d-176">**CompareStringWrapW** must be called directly from Shlwapi.dll, using ordinal 45.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d9d-177">Требования</span><span class="sxs-lookup"><span data-stu-id="d6d9d-177">Requirements</span></span>



| <span data-ttu-id="d6d9d-178">Требование</span><span class="sxs-lookup"><span data-stu-id="d6d9d-178">Requirement</span></span> | <span data-ttu-id="d6d9d-179">Значение</span><span class="sxs-lookup"><span data-stu-id="d6d9d-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d9d-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6d9d-180">Minimum supported client</span></span><br/> | <span data-ttu-id="d6d9d-181">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d6d9d-181">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d6d9d-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6d9d-182">Minimum supported server</span></span><br/> | <span data-ttu-id="d6d9d-183">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d6d9d-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d6d9d-184">Header</span><span class="sxs-lookup"><span data-stu-id="d6d9d-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6d9d-185"><dt>Нет</dt></span><span class="sxs-lookup"><span data-stu-id="d6d9d-185"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="d6d9d-186">DLL</span><span class="sxs-lookup"><span data-stu-id="d6d9d-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6d9d-187"><dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="d6d9d-187"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6d9d-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6d9d-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d9d-189">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="d6d9d-189">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
