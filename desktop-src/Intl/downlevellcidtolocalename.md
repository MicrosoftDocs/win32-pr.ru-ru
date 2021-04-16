---
description: Преобразует идентификатор локали в имя языкового стандарта.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: Функция ДовнлевеллЦидтолокаленаме (Нлсдл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 2f8e4ce9763348cf765522ebbd624a6e82f1071a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664320"
---
# <a name="downlevellcidtolocalename-function"></a><span data-ttu-id="a9650-103">Функция ДовнлевеллЦидтолокаленаме</span><span class="sxs-lookup"><span data-stu-id="a9650-103">DownlevelLCIDToLocaleName function</span></span>

<span data-ttu-id="a9650-104">Преобразует [идентификатор локали](locale-identifiers.md) в [имя языкового стандарта](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="a9650-104">Converts a [locale identifier](locale-identifiers.md) to a [locale name](locale-names.md).</span></span>

> [!Note]  
> <span data-ttu-id="a9650-105">Эта функция используется только приложениями, работающими в операционных системах, предшествующих Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a9650-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="a9650-106">Для его использования требуется загружаемый пакет.</span><span class="sxs-lookup"><span data-stu-id="a9650-106">Its use requires a download package.</span></span> <span data-ttu-id="a9650-107">Приложения, работающие только в Windows Vista и более поздних версиях, должны вызывать [**лЦидтолокаленаме**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) для получения имени языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="a9650-107">Applications that run only on Windows Vista and later should call [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to retrieve a locale name.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a9650-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9650-108">Syntax</span></span>


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a9650-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9650-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9650-110">*Языковой стандарт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9650-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9650-111">Идентификатор локали для преобразования.</span><span class="sxs-lookup"><span data-stu-id="a9650-111">The locale identifier to translate.</span></span> <span data-ttu-id="a9650-112">Для создания идентификатора языкового стандарта можно использовать макрос [**макелЦид**](/windows/desktop/api/Winnt/nf-winnt-makelcid) .</span><span class="sxs-lookup"><span data-stu-id="a9650-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier.</span></span> <span data-ttu-id="a9650-113">Эта функция не поддерживает нейтральные национальные настройки или следующие конкретные значения идентификатора локали.</span><span class="sxs-lookup"><span data-stu-id="a9650-113">This function does not support neutral locales or the following specific locale identifier values.</span></span>

-   [<span data-ttu-id="a9650-114">система языкового стандарта \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a9650-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="a9650-115">\_Пользовательская Национальная настройка \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a9650-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)
-   [<span data-ttu-id="a9650-116">Пользовательский ЯЗЫКовой стандарт \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a9650-116">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="a9650-117">Пользовательский пользовательский интерфейс языкового стандарта \_ \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a9650-117">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="a9650-118">Пользовательский ЯЗЫКовой стандарт не \_ \_ указан</span><span class="sxs-lookup"><span data-stu-id="a9650-118">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="a9650-119">*лпнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a9650-119">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9650-120">Указатель на буфер, в котором эта функция получает имя локали.</span><span class="sxs-lookup"><span data-stu-id="a9650-120">Pointer to a buffer in which this function retrieves the locale name.</span></span> <span data-ttu-id="a9650-121">Функция получает **значение NULL** , если *кчнаме* имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="a9650-121">The function retrieves **NULL** if *cchName* is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="a9650-122">*кчнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9650-122">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9650-123">Размер (в кодовых позициях UTF-16) в буфере имени языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="a9650-123">Size, in UTF-16 code points, of the locale name buffer.</span></span> <span data-ttu-id="a9650-124">Приложение задает для этого параметра значение 0, чтобы получить требуемый размер в буфере имен языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="a9650-124">The application sets this parameter to 0 to return the required size of the locale name buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a9650-125">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9650-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9650-126">Флаги, указывающие тип получаемого имени.</span><span class="sxs-lookup"><span data-stu-id="a9650-126">Flags specifying the type of name to retrieve.</span></span> <span data-ttu-id="a9650-127">Значение по умолчанию — \_ имя локали нижнего уровня \_ .</span><span class="sxs-lookup"><span data-stu-id="a9650-127">The default value is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9650-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9650-128">Return value</span></span>

<span data-ttu-id="a9650-129">Возвращает количество кодовых точек UTF-16 в имени языкового стандарта, включая завершающий нуль-символ, в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="a9650-129">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span> <span data-ttu-id="a9650-130">Если функция выполнена удачно и значение *кчнаме* равно 0, то возвращаемое значение будет иметь необходимый размер в символах (включая символы NULL) для буфера имен языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="a9650-130">If the function succeeds and the value of *cchName* is 0, the return value is the required size, in characters (including null characters), for the locale name buffer.</span></span>

<span data-ttu-id="a9650-131">Функция возвращает 0, если она не выполнена.</span><span class="sxs-lookup"><span data-stu-id="a9650-131">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="a9650-132">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="a9650-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="a9650-133">Ошибка \_ : недостаточный \_ Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="a9650-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="a9650-134">Указанный размер буфера не достаточен или имеет неправильное значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a9650-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="a9650-135">Ошибка \_ : недопустимые \_ флаги.</span><span class="sxs-lookup"><span data-stu-id="a9650-135">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="a9650-136">Недопустимое значение *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a9650-136">The value of *dwFlags* is not valid.</span></span>
-   <span data-ttu-id="a9650-137">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="a9650-137">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="a9650-138">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="a9650-138">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9650-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9650-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a9650-140">Эта функция не поддерживает [пользовательские языковые стандарты](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="a9650-140">This function does not support [custom locales](custom-locales.md).</span></span>

 

<span data-ttu-id="a9650-141">Требуемый заголовочный файл и библиотека DLL являются частью скачивания "API сопоставления данных нижнего уровня Microsoft NLS", доступного в [центре загрузки Майкрософт](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="a9650-141">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9650-142">Требования</span><span class="sxs-lookup"><span data-stu-id="a9650-142">Requirements</span></span>



| <span data-ttu-id="a9650-143">Требование</span><span class="sxs-lookup"><span data-stu-id="a9650-143">Requirement</span></span> | <span data-ttu-id="a9650-144">Значение</span><span class="sxs-lookup"><span data-stu-id="a9650-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9650-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9650-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a9650-146">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a9650-146">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="a9650-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9650-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a9650-148">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a9650-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a9650-149">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a9650-149">Redistributable</span></span><br/>          | <span data-ttu-id="a9650-150">Интерфейсы API сопоставления данных нижнего уровня Microsoft NLS в Windows XP с пакетом обновления 2 (SP2) и Латерорвиндовс Vista</span><span class="sxs-lookup"><span data-stu-id="a9650-150">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="a9650-151">Header</span><span class="sxs-lookup"><span data-stu-id="a9650-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9650-152"><dt>Нлсдл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9650-152"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="a9650-153">DLL</span><span class="sxs-lookup"><span data-stu-id="a9650-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9650-154"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9650-154"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a9650-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9650-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9650-156">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="a9650-156">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="a9650-157">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="a9650-157">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="a9650-158">Сопоставление данных локали</span><span class="sxs-lookup"><span data-stu-id="a9650-158">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="a9650-159">**лЦидтолокаленаме**</span><span class="sxs-lookup"><span data-stu-id="a9650-159">**LCIDToLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
