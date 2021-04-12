---
description: Предоставляет список скриптов для указанного языкового стандарта.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: Функция Довнлевелжетлокалескриптс (Идндл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272070"
---
# <a name="downlevelgetlocalescripts-function"></a><span data-ttu-id="befe4-103">Функция Довнлевелжетлокалескриптс</span><span class="sxs-lookup"><span data-stu-id="befe4-103">DownlevelGetLocaleScripts function</span></span>

<span data-ttu-id="befe4-104">Предоставляет список скриптов для указанного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="befe4-104">Provides a list of scripts for the specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="befe4-105">Эта функция используется только приложениями, работающими в операционных системах, предшествующих Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="befe4-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="befe4-106">Для его использования требуется загружаемый пакет.</span><span class="sxs-lookup"><span data-stu-id="befe4-106">Its use requires the download package.</span></span> <span data-ttu-id="befe4-107">Приложения, которые работают только в Windows Vista и более поздних версиях, должны вызывать [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) с *LCType* , установленным в [locale \_ сскриптс](locale-sscripts.md).</span><span class="sxs-lookup"><span data-stu-id="befe4-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SSCRIPTS](locale-sscripts.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="befe4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="befe4-108">Syntax</span></span>


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="befe4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="befe4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="befe4-110">*лплокаленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="befe4-110">*lpLocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="befe4-111">Указатель на [имя локали](locale-names.md), заканчивающееся нулем.</span><span class="sxs-lookup"><span data-stu-id="befe4-111">Pointer to a null-terminated [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="befe4-112">*лпскриптс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="befe4-112">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="befe4-113">Указатель на буфер, в котором эта функция получает строку, завершающуюся нулем, представляющую список скриптов, с использованием 4-символьной нотации, используемой в [стандарте ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="befe4-113">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="befe4-114">Имя каждого сценария состоит из четырех латинских символов, а имена извлекаются в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="befe4-114">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="befe4-115">За каждым из них, включая последний, следует точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="befe4-115">Each of them, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="befe4-116">Кроме того, этот параметр может содержать **значение NULL** , если *кчскриптс* имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="befe4-116">Alternatively, this parameter can contain **NULL** if *cchScripts* is set to 0.</span></span> <span data-ttu-id="befe4-117">В этом случае функция возвращает необходимый размер буфера скрипта.</span><span class="sxs-lookup"><span data-stu-id="befe4-117">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="befe4-118">*кчскриптс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="befe4-118">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="befe4-119">Размер в символах для буфера скрипта, указанного параметром *лпскриптс*.</span><span class="sxs-lookup"><span data-stu-id="befe4-119">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="befe4-120">Кроме того, приложение может установить этот параметр в значение 0.</span><span class="sxs-lookup"><span data-stu-id="befe4-120">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="befe4-121">В этом случае функция получает **значение NULL** в *лпскриптс* и возвращает необходимый размер буфера скрипта.</span><span class="sxs-lookup"><span data-stu-id="befe4-121">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="befe4-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="befe4-122">Return value</span></span>

<span data-ttu-id="befe4-123">Возвращает число символов, полученных в буфере скрипта, включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="befe4-123">Returns the number of characters retrieved in the script buffer, including the terminating null character.</span></span> <span data-ttu-id="befe4-124">Если функция завершается удачно и значение *кчскриптс* равно 0, то возвращаемое значение имеет необходимый размер (в символах, включая завершающий нуль-символ) для буфера скрипта.</span><span class="sxs-lookup"><span data-stu-id="befe4-124">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span>

<span data-ttu-id="befe4-125">Эта функция возвращает 0, если она не выполнена.</span><span class="sxs-lookup"><span data-stu-id="befe4-125">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="befe4-126">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="befe4-126">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="befe4-127">Ошибка \_ баддб.</span><span class="sxs-lookup"><span data-stu-id="befe4-127">ERROR\_BADDB.</span></span> <span data-ttu-id="befe4-128">Функция не может получить доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="befe4-128">The function could not access the data.</span></span> <span data-ttu-id="befe4-129">Такая ситуация обычно не возникает, и обычно указывает на неправильную установку, на диск или на проблему.</span><span class="sxs-lookup"><span data-stu-id="befe4-129">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="befe4-130">Ошибка \_ : недостаточный \_ Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="befe4-130">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="befe4-131">Указанный размер буфера не достаточен или имеет неправильное значение **null**.</span><span class="sxs-lookup"><span data-stu-id="befe4-131">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="befe4-132">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="befe4-132">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="befe4-133">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="befe4-133">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="befe4-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="befe4-134">Remarks</span></span>

<span data-ttu-id="befe4-135">Эта функция полезна как часть стратегии по устранению проблем безопасности, связанных с [международными доменными именами (IDNs)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="befe4-135">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="befe4-136">Ниже приведены некоторые примеры входных и выходных данных для этой функции, при условии, что размер буфера достаточен.</span><span class="sxs-lookup"><span data-stu-id="befe4-136">Here are some examples of inputs and outputs for this function, assuming a sufficient buffer size:</span></span>



| <span data-ttu-id="befe4-137">Locale</span><span class="sxs-lookup"><span data-stu-id="befe4-137">Locale</span></span>                  | <span data-ttu-id="befe4-138">*лплокаленаме*</span><span class="sxs-lookup"><span data-stu-id="befe4-138">*lpLocaleName*</span></span> | <span data-ttu-id="befe4-139">*лпскриптс*</span><span class="sxs-lookup"><span data-stu-id="befe4-139">*lpScripts*</span></span>     |
|-------------------------|----------------|-----------------|
| <span data-ttu-id="befe4-140">Английский (США)</span><span class="sxs-lookup"><span data-stu-id="befe4-140">English (United States)</span></span> | <span data-ttu-id="befe4-141">ru-RU</span><span class="sxs-lookup"><span data-stu-id="befe4-141">en-US</span></span>          | <span data-ttu-id="befe4-142">ЛАТН;</span><span class="sxs-lookup"><span data-stu-id="befe4-142">Latn;</span></span>           |
| <span data-ttu-id="befe4-143">Хинди (Индия)</span><span class="sxs-lookup"><span data-stu-id="befe4-143">Hindi (India)</span></span>           | <span data-ttu-id="befe4-144">hi-IN</span><span class="sxs-lookup"><span data-stu-id="befe4-144">hi-IN</span></span>          | <span data-ttu-id="befe4-145">Дева;</span><span class="sxs-lookup"><span data-stu-id="befe4-145">Deva;</span></span>           |
| <span data-ttu-id="befe4-146">Японский (Япония)</span><span class="sxs-lookup"><span data-stu-id="befe4-146">Japanese (Japan)</span></span>        | <span data-ttu-id="befe4-147">ja-JP</span><span class="sxs-lookup"><span data-stu-id="befe4-147">ja-JP</span></span>          | <span data-ttu-id="befe4-148">Хани; Хира; Знаков</span><span class="sxs-lookup"><span data-stu-id="befe4-148">Hani;Hira;Kana;</span></span> |



 

<span data-ttu-id="befe4-149">Список не содержит латинский сценарий, если он не является важнейшей частью системы записи, используемой для языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="befe4-149">The list does not contain the Latin script unless it is an essential part of the writing system used for a locale.</span></span> <span data-ttu-id="befe4-150">Однако символы латиницы часто используются в контексте национальных настроек, для которых они не являются собственными, например для внешнего имени компании.</span><span class="sxs-lookup"><span data-stu-id="befe4-150">However, Latin characters are often used in the context of locales for which they are not native, as for a foreign business name.</span></span> <span data-ttu-id="befe4-151">В приведенном выше примере для языка хинди в Индии единственным извлеченным сценарием является "Дева" (для деванагари), хотя Латинский символ также может отображаться в тексте на языке хинди.</span><span class="sxs-lookup"><span data-stu-id="befe4-151">In the example above for Hindi in India, the only script retrieved is "Deva" (for Devanagari), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="befe4-152">Функция [**довнлевелверифискриптс**](downlevelverifyscripts.md) имеет специальный флаг для обращения к этому варианту.</span><span class="sxs-lookup"><span data-stu-id="befe4-152">The [**DownlevelVerifyScripts**](downlevelverifyscripts.md) function has a special flag to address that case.</span></span>

<span data-ttu-id="befe4-153">Требуемый заголовочный файл и библиотека DLL являются частью скачивания веб- [API для Межязыкового доменного имени Майкрософт (IDN)](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , доступного в [центре загрузки MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="befe4-153">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="befe4-154">Требования</span><span class="sxs-lookup"><span data-stu-id="befe4-154">Requirements</span></span>



| <span data-ttu-id="befe4-155">Требование</span><span class="sxs-lookup"><span data-stu-id="befe4-155">Requirement</span></span> | <span data-ttu-id="befe4-156">Значение</span><span class="sxs-lookup"><span data-stu-id="befe4-156">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="befe4-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="befe4-157">Minimum supported client</span></span><br/> | <span data-ttu-id="befe4-158">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="befe4-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="befe4-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="befe4-159">Minimum supported server</span></span><br/> | <span data-ttu-id="befe4-160">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="befe4-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="befe4-161">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="befe4-161">Redistributable</span></span><br/>          | <span data-ttu-id="befe4-162">API для межязыкового доменного имени Майкрософт (IDN) в Windows XP (SP2 или более поздней версии), Windows Server 2003 (с пакетом обновления 1 (SP1) или более поздней версии) или Windows Vista</span><span class="sxs-lookup"><span data-stu-id="befe4-162">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="befe4-163">Header</span><span class="sxs-lookup"><span data-stu-id="befe4-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="befe4-164"><dt>Идндл. h</dt></span><span class="sxs-lookup"><span data-stu-id="befe4-164"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="befe4-165">DLL</span><span class="sxs-lookup"><span data-stu-id="befe4-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="befe4-166"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="befe4-166"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="befe4-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="befe4-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="befe4-168">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="befe4-168">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="befe4-169">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="befe4-169">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="befe4-170">Обработка международных доменных имен (IDNs)</span><span class="sxs-lookup"><span data-stu-id="befe4-170">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="befe4-171">**довнлевелжетстрингскриптс**</span><span class="sxs-lookup"><span data-stu-id="befe4-171">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="befe4-172">**довнлевелверифискриптс**</span><span class="sxs-lookup"><span data-stu-id="befe4-172">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="befe4-173">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="befe4-173">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
