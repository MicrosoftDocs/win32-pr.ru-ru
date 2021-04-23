---
description: Форматирует время в виде строки времени для указанного языкового стандарта.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: Функция Жеттимеформатврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 53f1bb88c2b3a79b58f3025daec31a7b1340b642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985484"
---
# <a name="gettimeformatwrapw-function"></a><span data-ttu-id="73ee6-103">Функция Жеттимеформатврапв</span><span class="sxs-lookup"><span data-stu-id="73ee6-103">GetTimeFormatWrapW function</span></span>

<span data-ttu-id="73ee6-104">\[**Жеттимеформатврапв** доступен для использования в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="73ee6-104">\[**GetTimeFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="73ee6-105">Она может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="73ee6-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="73ee6-106">На своем месте следует использовать [**жеттимеформатв**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .\]</span><span class="sxs-lookup"><span data-stu-id="73ee6-106">You should use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in its place.\]</span></span>

<span data-ttu-id="73ee6-107">Форматирует время в виде строки времени для указанного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="73ee6-107">Formats time as a time string for a specified locale.</span></span> <span data-ttu-id="73ee6-108">Функция форматирует либо указанное время, либо локальное системное время.</span><span class="sxs-lookup"><span data-stu-id="73ee6-108">The function formats either a specified time or the local system time.</span></span>

> [!Note]  
> <span data-ttu-id="73ee6-109">**Жеттимеформатврапв** — это оболочка для функции **жеттимеформатв** .</span><span class="sxs-lookup"><span data-stu-id="73ee6-109">**GetTimeFormatWrapW** is a wrapper for the **GetTimeFormatW** function.</span></span> <span data-ttu-id="73ee6-110">Дополнительные сведения об использовании см. на странице [**жеттимеформат**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .</span><span class="sxs-lookup"><span data-stu-id="73ee6-110">See the [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="73ee6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73ee6-111">Syntax</span></span>


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a><span data-ttu-id="73ee6-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="73ee6-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ee6-113">*Языковой стандарт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73ee6-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ee6-114">Тип: **LCID**</span><span class="sxs-lookup"><span data-stu-id="73ee6-114">Type: **LCID**</span></span>

<span data-ttu-id="73ee6-115">Задает языковой стандарт, для которого должна быть отформатирована строка времени.</span><span class="sxs-lookup"><span data-stu-id="73ee6-115">Specifies the locale for which the time string is to be formatted.</span></span> <span data-ttu-id="73ee6-116">Если *пвзформат* имеет **значение NULL**, функция форматирует строку в соответствии с форматом времени для этого языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="73ee6-116">If *pwzFormat* is **NULL**, the function formats the string according to the time format for this locale.</span></span> <span data-ttu-id="73ee6-117">Если *пвзформат* не равно **null**, функция использует языковой стандарт только для сведений, не указанных в формате строки рисунка (например, метки времени языкового стандарта).</span><span class="sxs-lookup"><span data-stu-id="73ee6-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's time markers).</span></span>

<span data-ttu-id="73ee6-118">Этот параметр может быть идентификатором локали, созданным в макросе [**макелЦид**](/windows/win32/api/winnt/nf-winnt-makelcid) , или одним из следующих предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="73ee6-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="73ee6-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**система языкового стандарта \_ \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="73ee6-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="73ee6-120">Национальная настройка системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73ee6-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="73ee6-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_Пользовательская Национальная настройка \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="73ee6-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="73ee6-122">Языковой стандарт пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73ee6-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="73ee6-123">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73ee6-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ee6-124">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="73ee6-124">Type: **DWORD**</span></span>

<span data-ttu-id="73ee6-125">Задает различные параметры функции.</span><span class="sxs-lookup"><span data-stu-id="73ee6-125">Specifies various function options.</span></span> <span data-ttu-id="73ee6-126">Можно указать сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="73ee6-126">You can specify a combination of the following values.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="73ee6-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**наусероверриде ЛОКАЛи \_**</span><span class="sxs-lookup"><span data-stu-id="73ee6-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="73ee6-128">Если задано значение, функция форматирует строку, используя системный формат времени по умолчанию для указанного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="73ee6-128">If set, the function formats the string using the system default time format for the specified locale.</span></span> <span data-ttu-id="73ee6-129">Если значение не задано, функция форматирует строку с использованием любых пользовательских переопределений в формате времени по умолчанию для языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="73ee6-129">If not set, the function formats the string using any user overrides to the locale's default time format.</span></span> <span data-ttu-id="73ee6-130">Этот флаг можно установить, только если *пвзформат* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="73ee6-130">This flag can only be set if *pwzFormat* is **NULL**.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="73ee6-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**Использование языкового стандарта \_ \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="73ee6-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="73ee6-132">Использует системную кодовую страницу ANSI для перевода строк вместо кодовой страницы языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="73ee6-132">Uses the system ANSI code page for string translation instead of the locale code page.</span></span>

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span data-ttu-id="73ee6-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**ВРЕМЯ \_ номинутесорсекондс**</span><span class="sxs-lookup"><span data-stu-id="73ee6-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TIME\_NOMINUTESORSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="73ee6-134">Не использует минуты или секунды.</span><span class="sxs-lookup"><span data-stu-id="73ee6-134">Does not use minutes or seconds.</span></span>

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span data-ttu-id="73ee6-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**ВРЕМЯ в \_ секунду**</span><span class="sxs-lookup"><span data-stu-id="73ee6-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TIME\_NOSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="73ee6-136">Не использует секунды.</span><span class="sxs-lookup"><span data-stu-id="73ee6-136">Does not use seconds.</span></span>

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span data-ttu-id="73ee6-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**ВРЕМЯ \_ нотимемаркер**</span><span class="sxs-lookup"><span data-stu-id="73ee6-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TIME\_NOTIMEMARKER**</span></span>


</dt> <dd>

<span data-ttu-id="73ee6-138">Не использует маркер времени.</span><span class="sxs-lookup"><span data-stu-id="73ee6-138">Does not use a time marker.</span></span>

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span data-ttu-id="73ee6-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**ВРЕМЯ \_ FORCE24HOURFORMAT**</span><span class="sxs-lookup"><span data-stu-id="73ee6-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TIME\_FORCE24HOURFORMAT**</span></span>


</dt> <dd>

<span data-ttu-id="73ee6-140">Всегда использует 24-часовой формат времени.</span><span class="sxs-lookup"><span data-stu-id="73ee6-140">Always uses a 24-hour time format.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="73ee6-141">*лптиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73ee6-141">*lpTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ee6-142">Тип: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="73ee6-142">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="73ee6-143">Указатель на структуру [_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) , которая содержит сведения о времени для форматирования.</span><span class="sxs-lookup"><span data-stu-id="73ee6-143">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the time information to be formatted.</span></span> <span data-ttu-id="73ee6-144">Если этот указатель равен **null**, функция использует текущее локальное системное время.</span><span class="sxs-lookup"><span data-stu-id="73ee6-144">If this pointer is **NULL**, the function uses the current local system time.</span></span>

</dd> <dt>

<span data-ttu-id="73ee6-145">*пвзформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73ee6-145">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ee6-146">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="73ee6-146">Type: **LPCWSTR**</span></span>

<span data-ttu-id="73ee6-147">Указатель на формат, используемый для формирования строки времени.</span><span class="sxs-lookup"><span data-stu-id="73ee6-147">A pointer to a format to use to form the time string.</span></span> <span data-ttu-id="73ee6-148">Если *пвзформат* имеет **значение NULL**, функция использует формат времени для указанного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="73ee6-148">If *pwzFormat* is **NULL**, the function uses the time format of the specified locale.</span></span> <span data-ttu-id="73ee6-149">Дополнительные сведения см. в разделе [**жеттимеформат**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .</span><span class="sxs-lookup"><span data-stu-id="73ee6-149">See [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="73ee6-150">*пвзтиместр* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="73ee6-150">*pwzTimeStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73ee6-151">Тип: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="73ee6-151">Type: **LPWSTR**</span></span>

<span data-ttu-id="73ee6-152">Указатель на буфер, который получает отформатированную строку времени.</span><span class="sxs-lookup"><span data-stu-id="73ee6-152">A pointer to a buffer that receives the formatted time string.</span></span>

</dd> <dt>

<span data-ttu-id="73ee6-153">*кчтиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73ee6-153">*cchTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ee6-154">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="73ee6-154">Type: **int**</span></span>

<span data-ttu-id="73ee6-155">Размер (в символах) буфера *пвзтиместр* .</span><span class="sxs-lookup"><span data-stu-id="73ee6-155">The size, in characters, of the *pwzTimeStr* buffer.</span></span> <span data-ttu-id="73ee6-156">Если *кчтиме* равен нулю, функция возвращает количество символов, необходимых для хранения отформатированной строки времени, а буфер, на который указывает *пвзтиместр* , не используется.</span><span class="sxs-lookup"><span data-stu-id="73ee6-156">If *cchTime* is zero, the function returns the number of characters required to hold the formatted time string, and the buffer pointed to by *pwzTimeStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73ee6-157">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73ee6-157">Return value</span></span>

<span data-ttu-id="73ee6-158">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="73ee6-158">Type: **int**</span></span>

<span data-ttu-id="73ee6-159">Если функция выполнена, возвращаемое значение — это число символов, записанных в буфер, на который указывает *пвзтиместр*.</span><span class="sxs-lookup"><span data-stu-id="73ee6-159">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzTimeStr*.</span></span> <span data-ttu-id="73ee6-160">Если параметр *кчтиме* равен нулю, то возвращаемое значение является числом символов, необходимых для хранения форматируемой строки времени.</span><span class="sxs-lookup"><span data-stu-id="73ee6-160">If the *cchTime* parameter is zero, the return value is the number of characters required to hold the formatted time string.</span></span> <span data-ttu-id="73ee6-161">Счетчик включает завершающий нуль символ.</span><span class="sxs-lookup"><span data-stu-id="73ee6-161">The count includes the terminating null character.</span></span>

<span data-ttu-id="73ee6-162">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="73ee6-162">If the function fails, the return value is zero.</span></span> <span data-ttu-id="73ee6-163">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="73ee6-163">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="73ee6-164">**GetLastError** может возвращать один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="73ee6-164">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="73ee6-165">**Ошибка \_ недостаточного \_ буфера**</span><span class="sxs-lookup"><span data-stu-id="73ee6-165">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="73ee6-166">**Ошибка \_ недопустимых \_ флагов**</span><span class="sxs-lookup"><span data-stu-id="73ee6-166">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="73ee6-167">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="73ee6-167">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="73ee6-168">Примечания</span><span class="sxs-lookup"><span data-stu-id="73ee6-168">Remarks</span></span>

<span data-ttu-id="73ee6-169">**Жеттимеформатврапв** предоставляет возможность использования строк Юникода в операционных системах, предшествующих Windows XP.</span><span class="sxs-lookup"><span data-stu-id="73ee6-169">**GetTimeFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="73ee6-170">Предпочтительным методом является использование [**жеттимеформатв**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) в сочетании с уровнем Майкрософт для Юникода (мслу).</span><span class="sxs-lookup"><span data-stu-id="73ee6-170">The preferred method is to use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="73ee6-171">**Жеттимеформатврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 310.</span><span class="sxs-lookup"><span data-stu-id="73ee6-171">**GetTimeFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 310.</span></span>

## <a name="requirements"></a><span data-ttu-id="73ee6-172">Требования</span><span class="sxs-lookup"><span data-stu-id="73ee6-172">Requirements</span></span>



| <span data-ttu-id="73ee6-173">Требование</span><span class="sxs-lookup"><span data-stu-id="73ee6-173">Requirement</span></span> | <span data-ttu-id="73ee6-174">Значение</span><span class="sxs-lookup"><span data-stu-id="73ee6-174">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73ee6-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73ee6-175">Minimum supported client</span></span><br/> | <span data-ttu-id="73ee6-176">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="73ee6-176">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73ee6-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73ee6-177">Minimum supported server</span></span><br/> | <span data-ttu-id="73ee6-178">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73ee6-178">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="73ee6-179">DLL</span><span class="sxs-lookup"><span data-stu-id="73ee6-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73ee6-180"><dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="73ee6-180"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73ee6-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73ee6-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ee6-182">**жеттимеформат**</span><span class="sxs-lookup"><span data-stu-id="73ee6-182">**GetTimeFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
