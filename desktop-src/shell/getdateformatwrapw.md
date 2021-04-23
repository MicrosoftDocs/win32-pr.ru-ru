---
description: Форматирует дату в виде строки даты для указанного языкового стандарта.
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: Функция Жетдатеформатврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDateFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9c369584fd15a27d5e684452b2277104b5b1da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264427"
---
# <a name="getdateformatwrapw-function"></a><span data-ttu-id="339cd-103">Функция Жетдатеформатврапв</span><span class="sxs-lookup"><span data-stu-id="339cd-103">GetDateFormatWrapW function</span></span>

<span data-ttu-id="339cd-104">\[**Жетдатеформатврапв** доступен для использования в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="339cd-104">\[**GetDateFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="339cd-105">Он будет недоступен в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="339cd-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="339cd-106">На своем месте следует использовать [**жетдатеформатв**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) .\]</span><span class="sxs-lookup"><span data-stu-id="339cd-106">You should use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in its place.\]</span></span>

<span data-ttu-id="339cd-107">Форматирует дату в виде строки даты для указанного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="339cd-107">Formats a date as a date string for a specified locale.</span></span> <span data-ttu-id="339cd-108">Функция форматирует либо указанную дату, либо локальную системную дату.</span><span class="sxs-lookup"><span data-stu-id="339cd-108">The function formats either a specified date or the local system date.</span></span>

> [!Note]  
> <span data-ttu-id="339cd-109">**Жетдатеформатврапв** — это оболочка для функции **жетдатеформатв** .</span><span class="sxs-lookup"><span data-stu-id="339cd-109">**GetDateFormatWrapW** is a wrapper for the **GetDateFormatW** function.</span></span> <span data-ttu-id="339cd-110">Дополнительные сведения об использовании см. на странице [**жетдатеформат**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) .</span><span class="sxs-lookup"><span data-stu-id="339cd-110">See the [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="339cd-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="339cd-111">Syntax</span></span>


```C++
int GetDateFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpDate,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzDateStr,
  _In_        int        cchDate
);
```



## <a name="parameters"></a><span data-ttu-id="339cd-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="339cd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="339cd-113">*Языковой стандарт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="339cd-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="339cd-114">Тип: **LCID**</span><span class="sxs-lookup"><span data-stu-id="339cd-114">Type: **LCID**</span></span>

<span data-ttu-id="339cd-115">Языковой стандарт, в котором строка даты должна быть отформатирована.</span><span class="sxs-lookup"><span data-stu-id="339cd-115">The locale for which the date string is to be formatted.</span></span> <span data-ttu-id="339cd-116">Если *пвзформат* имеет **значение NULL**, функция форматирует строку в соответствии с форматом даты для этого языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="339cd-116">If *pwzFormat* is **NULL**, the function formats the string according to the date format for this locale.</span></span> <span data-ttu-id="339cd-117">Если *пвзформат* не равно **null**, функция использует языковой стандарт только для информации, которая не указана в формате строки рисунка (например, названия дня и месяца языкового стандарта).</span><span class="sxs-lookup"><span data-stu-id="339cd-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's day and month names).</span></span>

<span data-ttu-id="339cd-118">Этот параметр может быть идентификатором локали, созданным в макросе [**макелЦид**](/windows/win32/api/winnt/nf-winnt-makelcid) , или одним из следующих предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="339cd-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="339cd-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**система языкового стандарта \_ \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="339cd-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="339cd-120">Национальная настройка системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="339cd-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="339cd-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_Пользовательская Национальная настройка \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="339cd-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="339cd-122">Языковой стандарт пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="339cd-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="339cd-123">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="339cd-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="339cd-124">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="339cd-124">Type: **DWORD**</span></span>

<span data-ttu-id="339cd-125">Задает различные параметры функции.</span><span class="sxs-lookup"><span data-stu-id="339cd-125">Specifies various function options.</span></span> <span data-ttu-id="339cd-126">Если *пвзформат* не **равно NULL**, этот параметр должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="339cd-126">If *pwzFormat* is not **NULL**, this parameter must be zero.</span></span> <span data-ttu-id="339cd-127">Если *пвзформат* имеет **значение NULL**, можно указать сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="339cd-127">If *pwzFormat* is **NULL**, you can specify a combination of the following values.</span></span> <span data-ttu-id="339cd-128">Если не указать дату \_ еармонс, Date \_ ШОРТДАТЕ или Date \_ Лонгдате, а *пвзформат* имеет **значение NULL**, то \_ в качестве значения по умолчанию используется дата шортдате.</span><span class="sxs-lookup"><span data-stu-id="339cd-128">If you do not specify either DATE\_YEARMONTH, DATE\_SHORTDATE, or DATE\_LONGDATE, and *pwzFormat* is **NULL**, then DATE\_SHORTDATE is used as the default.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="339cd-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**наусероверриде ЛОКАЛи \_**</span><span class="sxs-lookup"><span data-stu-id="339cd-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="339cd-130">Если задано значение, функция форматирует строку, используя системный формат даты по умолчанию для указанного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="339cd-130">If set, the function formats the string using the system default date format for the specified locale.</span></span> <span data-ttu-id="339cd-131">Если значение не задано, функция форматирует строку с использованием любых пользовательских переопределений в формате даты по умолчанию для языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="339cd-131">If not set, the function formats the string using any user overrides to the locale's default date format.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="339cd-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**Использование языкового стандарта \_ \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="339cd-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="339cd-133">Использует системную кодовую страницу ANSI для перевода строк вместо кодовой страницы языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="339cd-133">Uses the system ANSI code page for string translation instead of the locale's code page.</span></span>

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span data-ttu-id="339cd-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**Дата \_ шортдате**</span><span class="sxs-lookup"><span data-stu-id="339cd-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**DATE\_SHORTDATE**</span></span>


</dt> <dd>

<span data-ttu-id="339cd-135">Использует краткий формат даты.</span><span class="sxs-lookup"><span data-stu-id="339cd-135">Uses the short date format.</span></span> <span data-ttu-id="339cd-136">Это значение нельзя использовать с DATE \_ лонгдате или Date \_ еармонс.</span><span class="sxs-lookup"><span data-stu-id="339cd-136">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span data-ttu-id="339cd-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**Дата \_ лонгдате**</span><span class="sxs-lookup"><span data-stu-id="339cd-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**DATE\_LONGDATE**</span></span>


</dt> <dd>

<span data-ttu-id="339cd-138">Использует длинный формат даты.</span><span class="sxs-lookup"><span data-stu-id="339cd-138">Uses the long date format.</span></span> <span data-ttu-id="339cd-139">Это значение нельзя использовать с DATE \_ шортдате или Date \_ еармонс.</span><span class="sxs-lookup"><span data-stu-id="339cd-139">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span data-ttu-id="339cd-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**Дата \_ еармонс**</span><span class="sxs-lookup"><span data-stu-id="339cd-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**DATE\_YEARMONTH**</span></span>


</dt> <dd>

<span data-ttu-id="339cd-141">Использует формат "год/месяц".</span><span class="sxs-lookup"><span data-stu-id="339cd-141">Uses the year/month format.</span></span> <span data-ttu-id="339cd-142">Это значение нельзя использовать с DATE \_ шортдате или Date \_ лонгдате.</span><span class="sxs-lookup"><span data-stu-id="339cd-142">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span>

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span data-ttu-id="339cd-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**использовать в качестве даты \_ \_ альтернативный \_ Календарь**</span><span class="sxs-lookup"><span data-stu-id="339cd-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**DATE\_USE\_ALT\_CALENDAR**</span></span>


</dt> <dd>

<span data-ttu-id="339cd-144">Использует альтернативный календарь, если он существует, для форматирования строки даты.</span><span class="sxs-lookup"><span data-stu-id="339cd-144">Uses the alternate calendar, if one exists, to format the date string.</span></span> <span data-ttu-id="339cd-145">Если этот флаг установлен, функция использует формат по умолчанию для этого альтернативного календаря вместо использования каких-либо пользовательских переопределений.</span><span class="sxs-lookup"><span data-stu-id="339cd-145">If this flag is set, the function uses the default format for that alternate calendar, rather than using any user overrides.</span></span> <span data-ttu-id="339cd-146">Пользовательские переопределения будут использоваться только в том случае, если для указанного альтернативного календаря формат по умолчанию отсутствует.</span><span class="sxs-lookup"><span data-stu-id="339cd-146">The user overrides will be used only in the event that there is no default format for the specified alternate calendar.</span></span>

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span data-ttu-id="339cd-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**Дата \_ лтрреадинг**</span><span class="sxs-lookup"><span data-stu-id="339cd-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**DATE\_LTRREADING**</span></span>


</dt> <dd>

<span data-ttu-id="339cd-148">Добавляет метки для макета чтения слева направо.</span><span class="sxs-lookup"><span data-stu-id="339cd-148">Adds marks for left-to-right reading layout.</span></span> <span data-ttu-id="339cd-149">Это значение нельзя использовать с параметром DATE \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="339cd-149">This value cannot be used with DATE\_RTLREADING.</span></span>

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span data-ttu-id="339cd-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**Дата \_ RTLREADING**</span><span class="sxs-lookup"><span data-stu-id="339cd-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**DATE\_RTLREADING**</span></span>


</dt> <dd>

<span data-ttu-id="339cd-151">Добавляет метки для макета чтения справа налево.</span><span class="sxs-lookup"><span data-stu-id="339cd-151">Adds marks for right-to-left reading layout.</span></span> <span data-ttu-id="339cd-152">Это значение нельзя использовать с параметром DATE \_ лтрреадинг.</span><span class="sxs-lookup"><span data-stu-id="339cd-152">This value cannot be used with DATE\_LTRREADING.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="339cd-153">*лпдате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="339cd-153">*lpDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="339cd-154">Тип: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="339cd-154">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="339cd-155">Указатель на структуру [_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) , содержащую сведения о датах для форматирования.</span><span class="sxs-lookup"><span data-stu-id="339cd-155">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date information to be formatted.</span></span> <span data-ttu-id="339cd-156">Если этот указатель равен **null**, функция использует текущую локальную системную дату.</span><span class="sxs-lookup"><span data-stu-id="339cd-156">If this pointer is **NULL**, the function uses the current local system date.</span></span>

</dd> <dt>

<span data-ttu-id="339cd-157">*пвзформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="339cd-157">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="339cd-158">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="339cd-158">Type: **LPCWSTR**</span></span>

<span data-ttu-id="339cd-159">Указатель на формат изображения, используемый для формирования строки даты.</span><span class="sxs-lookup"><span data-stu-id="339cd-159">A pointer to a format picture to use to form the date string.</span></span> <span data-ttu-id="339cd-160">Если *пвзформат* имеет **значение NULL**, функция использует формат даты указанного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="339cd-160">If *pwzFormat* is **NULL**, the function uses the date format of the specified locale.</span></span> <span data-ttu-id="339cd-161">Дополнительные сведения см. в разделе [**жетдатеформат**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) .</span><span class="sxs-lookup"><span data-stu-id="339cd-161">See [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="339cd-162">*пвздатестр* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="339cd-162">*pwzDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="339cd-163">Тип: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="339cd-163">Type: **LPWSTR**</span></span>

<span data-ttu-id="339cd-164">Указатель на буфер, который получает отформатированную строку даты.</span><span class="sxs-lookup"><span data-stu-id="339cd-164">A pointer to a buffer that receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="339cd-165">*кчдате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="339cd-165">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="339cd-166">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="339cd-166">Type: **int**</span></span>

<span data-ttu-id="339cd-167">Задает размер буфера *пвздатестр* в символах.</span><span class="sxs-lookup"><span data-stu-id="339cd-167">Specifies the size, in characters, of the *pwzDateStr* buffer.</span></span> <span data-ttu-id="339cd-168">Если *кчдате* равен нулю, функция возвращает количество символов, необходимых для хранения форматированной строки даты, а буфер, на который указывает *пвздатестр* , не используется.</span><span class="sxs-lookup"><span data-stu-id="339cd-168">If *cchDate* is zero, the function returns the number of characters required to hold the formatted date string, and the buffer pointed to by *pwzDateStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="339cd-169">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="339cd-169">Return value</span></span>

<span data-ttu-id="339cd-170">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="339cd-170">Type: **int**</span></span>

<span data-ttu-id="339cd-171">Если функция выполнена, возвращаемое значение — это число символов, записанных в буфер, на который указывает *пвздатестр*.</span><span class="sxs-lookup"><span data-stu-id="339cd-171">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzDateStr*.</span></span> <span data-ttu-id="339cd-172">Если параметр *кчдате* равен нулю, то возвращаемое значение представляет собой количество символов, необходимых для хранения форматированной строки даты.</span><span class="sxs-lookup"><span data-stu-id="339cd-172">If the *cchDate* parameter is zero, the return value is the number of characters required to hold the formatted date string.</span></span> <span data-ttu-id="339cd-173">Счетчик включает завершающий нуль символ.</span><span class="sxs-lookup"><span data-stu-id="339cd-173">The count includes the terminating null character.</span></span>

<span data-ttu-id="339cd-174">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="339cd-174">If the function fails, the return value is zero.</span></span> <span data-ttu-id="339cd-175">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="339cd-175">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="339cd-176">**GetLastError** может возвращать один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="339cd-176">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="339cd-177">**Ошибка \_ недостаточного \_ буфера**</span><span class="sxs-lookup"><span data-stu-id="339cd-177">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="339cd-178">**Ошибка \_ недопустимых \_ флагов**</span><span class="sxs-lookup"><span data-stu-id="339cd-178">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="339cd-179">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="339cd-179">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="339cd-180">Примечания</span><span class="sxs-lookup"><span data-stu-id="339cd-180">Remarks</span></span>

<span data-ttu-id="339cd-181">**Жетдатеформатврапв** предоставляет возможность использования строк Юникода в операционных системах, предшествующих Windows XP.</span><span class="sxs-lookup"><span data-stu-id="339cd-181">**GetDateFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="339cd-182">Предпочтительным методом является использование [**жетдатеформатв**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) в сочетании с уровнем Майкрософт для Юникода (мслу).</span><span class="sxs-lookup"><span data-stu-id="339cd-182">The preferred method is to use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="339cd-183">**Жетдатеформатврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 311.</span><span class="sxs-lookup"><span data-stu-id="339cd-183">**GetDateFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 311.</span></span>

## <a name="requirements"></a><span data-ttu-id="339cd-184">Требования</span><span class="sxs-lookup"><span data-stu-id="339cd-184">Requirements</span></span>



| <span data-ttu-id="339cd-185">Требование</span><span class="sxs-lookup"><span data-stu-id="339cd-185">Requirement</span></span> | <span data-ttu-id="339cd-186">Значение</span><span class="sxs-lookup"><span data-stu-id="339cd-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="339cd-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="339cd-187">Minimum supported client</span></span><br/> | <span data-ttu-id="339cd-188">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="339cd-188">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="339cd-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="339cd-189">Minimum supported server</span></span><br/> | <span data-ttu-id="339cd-190">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="339cd-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="339cd-191">DLL</span><span class="sxs-lookup"><span data-stu-id="339cd-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="339cd-192"><dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="339cd-192"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="339cd-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="339cd-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="339cd-194">**жетдатеформат**</span><span class="sxs-lookup"><span data-stu-id="339cd-194">**GetDateFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
