---
description: Не рекомендуется.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: Функция Жеткалендардатеформатекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarDateFormatEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: b0130bf62c742d0565b1c98c138ac8c71ddf7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683525"
---
# <a name="getcalendardateformatex-function"></a><span data-ttu-id="43a8e-103">Функция Жеткалендардатеформатекс</span><span class="sxs-lookup"><span data-stu-id="43a8e-103">GetCalendarDateFormatEx function</span></span>

<span data-ttu-id="43a8e-104">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="43a8e-104">Deprecated.</span></span> <span data-ttu-id="43a8e-105">Извлекает правильно отформатированную строку даты для указанного языкового стандарта, используя указанные дату и календарь.</span><span class="sxs-lookup"><span data-stu-id="43a8e-105">Retrieves a properly formatted date string for the specified locale using the specified date and calendar.</span></span> <span data-ttu-id="43a8e-106">Пользователь может указать краткий формат даты, длинный формат даты, год в формате месяца или шаблон пользовательского формата.</span><span class="sxs-lookup"><span data-stu-id="43a8e-106">The user can specify the short date format, the long date format, the year month format, or a custom format pattern.</span></span>

> [!Note]  
> <span data-ttu-id="43a8e-107">Эта функция может извлекать данные, которые изменяются между выпусками, например из-за пользовательского языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="43a8e-107">This function can retrieve data that changes between releases, for example, due to a custom locale.</span></span> <span data-ttu-id="43a8e-108">Если приложение должно сохранять или передавать данные, см. раздел [использование постоянных данных языкового стандарта](using-persistent-locale-data.md).</span><span class="sxs-lookup"><span data-stu-id="43a8e-108">If your application must persist or transmit data, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="43a8e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43a8e-109">Syntax</span></span>


```C++
BOOL GetCalendarDateFormatEx(
  _In_        LPCWSTR       lpszLocale,
  _In_        DWORD         dwFlags,
  _In_  const LPCALDATETIME lpCalDateTime,
  _In_        LPCWSTR       lpFormat,
  _Out_       LPWSTR        lpDateStr,
  _In_        int           cchDate
);
```



## <a name="parameters"></a><span data-ttu-id="43a8e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="43a8e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a8e-111">*лпсзлокале* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43a8e-111">*lpszLocale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a8e-112">Указатель на имя языкового стандарта или одно из следующих предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="43a8e-112">Pointer to a locale name, or one of the following predefined values.</span></span>

-   [<span data-ttu-id="43a8e-113">\_инвариантное имя локали \_</span><span class="sxs-lookup"><span data-stu-id="43a8e-113">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="43a8e-114">имя языкового стандарта \_ \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="43a8e-114">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="43a8e-115">имя языкового стандарта \_ \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="43a8e-115">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="43a8e-116">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43a8e-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a8e-117">Флаги, задающие параметры формата даты.</span><span class="sxs-lookup"><span data-stu-id="43a8e-117">Flags specifying date format options.</span></span> <span data-ttu-id="43a8e-118">Если *лпформат* не имеет значение **null**, этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="43a8e-118">If *lpFormat* is not set to **NULL**, this parameter must be set to 0.</span></span> <span data-ttu-id="43a8e-119">Если *лпформат* имеет значение **null**, приложение может указать сочетание следующих значений и [ \_ наусероверриде локали](locale-nouseroverride.md).</span><span class="sxs-lookup"><span data-stu-id="43a8e-119">If *lpFormat* is set to **NULL**, the application can specify a combination of the following values and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md).</span></span>



| <span data-ttu-id="43a8e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="43a8e-120">Value</span></span>                                                                                                                                                               | <span data-ttu-id="43a8e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="43a8e-121">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <span data-ttu-id="43a8e-122"><dt>**Дата \_ шортдате**</dt></span><span class="sxs-lookup"><span data-stu-id="43a8e-122"><dt>**DATE\_SHORTDATE**</dt></span></span> </dl>    | <span data-ttu-id="43a8e-123">Используйте краткий формат даты.</span><span class="sxs-lookup"><span data-stu-id="43a8e-123">Use the short date format.</span></span> <span data-ttu-id="43a8e-124">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43a8e-124">This is the default.</span></span> <span data-ttu-id="43a8e-125">Это значение нельзя использовать с DATE \_ лонгдате или Date \_ еармонс.</span><span class="sxs-lookup"><span data-stu-id="43a8e-125">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span> <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <span data-ttu-id="43a8e-126"><dt>**Дата \_ лонгдате**</dt></span><span class="sxs-lookup"><span data-stu-id="43a8e-126"><dt>**DATE\_LONGDATE**</dt></span></span> </dl>       | <span data-ttu-id="43a8e-127">Используйте длинный формат даты.</span><span class="sxs-lookup"><span data-stu-id="43a8e-127">Use the long date format.</span></span> <span data-ttu-id="43a8e-128">Это значение нельзя использовать с DATE \_ шортдате или Date \_ еармонс.</span><span class="sxs-lookup"><span data-stu-id="43a8e-128">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span> <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <span data-ttu-id="43a8e-129"><dt>**Дата \_ еармонс**</dt></span><span class="sxs-lookup"><span data-stu-id="43a8e-129"><dt>**DATE\_YEARMONTH**</dt></span></span> </dl>    | <span data-ttu-id="43a8e-130">Используйте формат "год/месяц".</span><span class="sxs-lookup"><span data-stu-id="43a8e-130">Use the year/month format.</span></span> <span data-ttu-id="43a8e-131">Это значение нельзя использовать с DATE \_ шортдате или Date \_ лонгдате.</span><span class="sxs-lookup"><span data-stu-id="43a8e-131">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span><br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <span data-ttu-id="43a8e-132"><dt>**Дата \_ лтрреадинг**</dt></span><span class="sxs-lookup"><span data-stu-id="43a8e-132"><dt>**DATE\_LTRREADING**</dt></span></span> </dl> | <span data-ttu-id="43a8e-133">Добавьте метки для макета чтения слева направо.</span><span class="sxs-lookup"><span data-stu-id="43a8e-133">Add marks for left-to-right reading layout.</span></span> <span data-ttu-id="43a8e-134">Это значение нельзя использовать с параметром DATE \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="43a8e-134">This value cannot be used with DATE\_RTLREADING.</span></span><br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <span data-ttu-id="43a8e-135"><dt>**Дата \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="43a8e-135"><dt>**DATE\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="43a8e-136">Добавьте метки для макета чтения справа налево.</span><span class="sxs-lookup"><span data-stu-id="43a8e-136">Add marks for right-to-left reading layout.</span></span> <span data-ttu-id="43a8e-137">Это значение нельзя использовать с DATE \_ лтрреадинг</span><span class="sxs-lookup"><span data-stu-id="43a8e-137">This value cannot be used with DATE\_LTRREADING</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="43a8e-138">*лпкалдатетиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43a8e-138">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a8e-139">Указатель на структуру [**калдатетиме**](caldatetime.md) , которая содержит дату и сведения календаря для форматирования.</span><span class="sxs-lookup"><span data-stu-id="43a8e-139">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to format.</span></span>

</dd> <dt>

<span data-ttu-id="43a8e-140">*лпформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43a8e-140">*lpFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a8e-141">Указатель на строку формата Picture, используемую для формирования строки даты.</span><span class="sxs-lookup"><span data-stu-id="43a8e-141">Pointer to a format picture string that is used to form the date string.</span></span> <span data-ttu-id="43a8e-142">Возможные значения для строки формата изображения определены в формате " [день", "месяц", "год" и "формат эры](day--month--year--and-era-format-pictures.md)".</span><span class="sxs-lookup"><span data-stu-id="43a8e-142">Possible values for the format picture string are defined in [Day, Month, Year, and Era Format Pictures](day--month--year--and-era-format-pictures.md).</span></span>

<span data-ttu-id="43a8e-143">Строка формата рисунка должна завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="43a8e-143">The format picture string must be null-terminated.</span></span> <span data-ttu-id="43a8e-144">Функция использует языковой стандарт только для сведений, не указанных в строке формата Picture, например названия дня и месяца для языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="43a8e-144">The function uses the locale only for information not specified in the format picture string, for example, the day and month names for the locale.</span></span> <span data-ttu-id="43a8e-145">Приложение задает для этого параметра **значение NULL** , если функция должна использовать формат даты указанного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="43a8e-145">The application sets this parameter to **NULL** if the function is to use the date format of the specified locale.</span></span>

</dd> <dt>

<span data-ttu-id="43a8e-146">*лпдатестр* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="43a8e-146">*lpDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43a8e-147">Указатель на буфер, в котором эта функция получает форматированную строку даты.</span><span class="sxs-lookup"><span data-stu-id="43a8e-147">Pointer to a buffer in which this function receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="43a8e-148">*кчдате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43a8e-148">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a8e-149">Размер (в символах) буфера *лпдатестр* .</span><span class="sxs-lookup"><span data-stu-id="43a8e-149">Size, in characters, of the *lpDateStr* buffer.</span></span> <span data-ttu-id="43a8e-150">Кроме того, приложение может установить этот параметр в значение 0.</span><span class="sxs-lookup"><span data-stu-id="43a8e-150">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="43a8e-151">В этом случае функция возвращает количество символов, необходимых для хранения форматированной строки даты, а параметр *лпдатестр* не используется.</span><span class="sxs-lookup"><span data-stu-id="43a8e-151">In this case, the function returns the number of characters required to hold the formatted date string, and the *lpDateStr* parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a8e-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43a8e-152">Return value</span></span>

<span data-ttu-id="43a8e-153">Возвращает число символов, записанных в буфер *лпдатестр* в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="43a8e-153">Returns the number of characters written to the *lpDateStr* buffer if successful.</span></span> <span data-ttu-id="43a8e-154">Если параметр *кчдате* имеет значение 0, функция возвращает количество символов, необходимых для хранения форматированной строки даты, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="43a8e-154">If the *cchDate* parameter is set to 0, the function returns the number of characters required to hold the formatted date string, including the terminating null character.</span></span>

<span data-ttu-id="43a8e-155">Эта функция возвращает 0, если она не выполнена.</span><span class="sxs-lookup"><span data-stu-id="43a8e-155">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="43a8e-156">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="43a8e-156">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="43a8e-157">\_Дата ошибки \_ за пределами \_ \_ диапазона.</span><span class="sxs-lookup"><span data-stu-id="43a8e-157">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="43a8e-158">Указанная дата находится за пределами диапазона.</span><span class="sxs-lookup"><span data-stu-id="43a8e-158">The specified date was out of range.</span></span>
-   <span data-ttu-id="43a8e-159">Ошибка \_ : недостаточный \_ Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="43a8e-159">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="43a8e-160">Указанный размер буфера не достаточен или имеет неправильное значение **null**.</span><span class="sxs-lookup"><span data-stu-id="43a8e-160">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="43a8e-161">Ошибка \_ : недопустимые \_ флаги.</span><span class="sxs-lookup"><span data-stu-id="43a8e-161">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="43a8e-162">Указаны недопустимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="43a8e-162">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="43a8e-163">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="43a8e-163">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="43a8e-164">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="43a8e-164">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a8e-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43a8e-165">Remarks</span></span>

<span data-ttu-id="43a8e-166">Самая ранняя дата, поддерживаемая этой функцией, — 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="43a8e-166">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="43a8e-167">Эта функция не имеет связанного файла заголовка или файла библиотеки.</span><span class="sxs-lookup"><span data-stu-id="43a8e-167">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="43a8e-168">Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля.</span><span class="sxs-lookup"><span data-stu-id="43a8e-168">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="43a8e-169">Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с этим обработчиком модуля и именем этой функции, чтобы получить адрес функции.</span><span class="sxs-lookup"><span data-stu-id="43a8e-169">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a8e-170">Требования</span><span class="sxs-lookup"><span data-stu-id="43a8e-170">Requirements</span></span>



| <span data-ttu-id="43a8e-171">Требование</span><span class="sxs-lookup"><span data-stu-id="43a8e-171">Requirement</span></span> | <span data-ttu-id="43a8e-172">Значение</span><span class="sxs-lookup"><span data-stu-id="43a8e-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43a8e-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43a8e-173">Minimum supported client</span></span><br/> | <span data-ttu-id="43a8e-174">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43a8e-174">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="43a8e-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43a8e-175">Minimum supported server</span></span><br/> | <span data-ttu-id="43a8e-176">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43a8e-176">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="43a8e-177">DLL</span><span class="sxs-lookup"><span data-stu-id="43a8e-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43a8e-178"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43a8e-178"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a8e-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43a8e-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a8e-180">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="43a8e-180">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="43a8e-181">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="43a8e-181">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="43a8e-182">Изображения дня, месяца, года и эры</span><span class="sxs-lookup"><span data-stu-id="43a8e-182">Day, Month, Year, and Era Format Pictures</span></span>](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[<span data-ttu-id="43a8e-183">NLS: пример API-интерфейсов на основе имен</span><span class="sxs-lookup"><span data-stu-id="43a8e-183">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> <dt>

[<span data-ttu-id="43a8e-184">**енумдатеформатсексекс**</span><span class="sxs-lookup"><span data-stu-id="43a8e-184">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[<span data-ttu-id="43a8e-185">**жетдатеформат**</span><span class="sxs-lookup"><span data-stu-id="43a8e-185">**GetDateFormat**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[<span data-ttu-id="43a8e-186">**жетдатеформатекс**</span><span class="sxs-lookup"><span data-stu-id="43a8e-186">**GetDateFormatEx**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[<span data-ttu-id="43a8e-187">**калдатетиме**</span><span class="sxs-lookup"><span data-stu-id="43a8e-187">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
