---
description: Возвращает имя языкового стандарта для родительского элемента поддерживаемого языкового стандарта.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Функция Довнлевелжетпарентлокаленаме (Нлсдл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: d3a556d68c33249d2e6b49c48035cc58d8bac8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999328"
---
# <a name="downlevelgetparentlocalename-function"></a><span data-ttu-id="49d31-103">Функция Довнлевелжетпарентлокаленаме</span><span class="sxs-lookup"><span data-stu-id="49d31-103">DownlevelGetParentLocaleName function</span></span>

<span data-ttu-id="49d31-104">Возвращает [имя языкового стандарта](locale-names.md) для родительского элемента поддерживаемого языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="49d31-104">Retrieves the [locale name](locale-names.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="49d31-105">Эта функция используется только приложениями, работающими в операционных системах, предшествующих Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="49d31-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="49d31-106">Для его использования требуется загружаемый пакет.</span><span class="sxs-lookup"><span data-stu-id="49d31-106">Its use requires the download package.</span></span> <span data-ttu-id="49d31-107">Приложения, которые работают только в Windows Vista и более поздних версиях, должны вызывать [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) с *LCType* , установленным в [locale \_ спарент](locale-sparent.md).</span><span class="sxs-lookup"><span data-stu-id="49d31-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="49d31-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49d31-108">Syntax</span></span>


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a><span data-ttu-id="49d31-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="49d31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49d31-110">*Языковой стандарт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49d31-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49d31-111">[Идентификатор](locale-identifiers.md) локали языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="49d31-111">[Locale identifier](locale-identifiers.md) of the locale.</span></span> <span data-ttu-id="49d31-112">С помощью макроса [**макелЦид**](/windows/desktop/api/Winnt/nf-winnt-makelcid) можно создать идентификатор языкового стандарта или использовать одно из следующих предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="49d31-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="49d31-113">ИНВАРИАНТный ЯЗЫКовой стандарт \_</span><span class="sxs-lookup"><span data-stu-id="49d31-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="49d31-114">система языкового стандарта \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="49d31-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="49d31-115">\_Пользовательская Национальная настройка \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="49d31-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="49d31-116">**Windows Vista и более поздние версии:** Также поддерживаются следующие пользовательские идентификаторы языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="49d31-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="49d31-117">Пользовательский ЯЗЫКовой стандарт \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="49d31-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="49d31-118">Пользовательский пользовательский интерфейс языкового стандарта \_ \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="49d31-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="49d31-119">Пользовательский ЯЗЫКовой стандарт не \_ \_ указан</span><span class="sxs-lookup"><span data-stu-id="49d31-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="49d31-120">*лпнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="49d31-120">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49d31-121">Указатель на буфер, в котором функция получает имя родительского языкового стандарта или одно из следующих предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="49d31-121">Pointer to a buffer in which the function retrieves the parent locale name, or one of the following predefined values.</span></span> <span data-ttu-id="49d31-122">Этот параметр имеет значение **null** , если *кчнаме* имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="49d31-122">This parameter is set to **NULL** if *cchName* is set to 0.</span></span>

-   [<span data-ttu-id="49d31-123">\_инвариантное имя локали \_</span><span class="sxs-lookup"><span data-stu-id="49d31-123">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="49d31-124">имя языкового стандарта \_ \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="49d31-124">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="49d31-125">имя языкового стандарта \_ \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="49d31-125">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="49d31-126">*кчнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49d31-126">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49d31-127">Размер буфера, обозначенного *лпнаме*, в кодовых позициях UTF-16.</span><span class="sxs-lookup"><span data-stu-id="49d31-127">Size of the buffer indicated by *lpName*, in UTF-16 code points.</span></span> <span data-ttu-id="49d31-128">Значение 0 для этого параметра приводит к тому, что функция игнорирует буфер *лпнаме* и возвращает размер буфера в символах (включая пустые символы), необходимых для хранения имени родительского языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="49d31-128">A value of 0 for this parameter causes the function to ignore the *lpName* buffer and return the size of the buffer, in characters (null characters included), required to contain the parent locale name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49d31-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49d31-129">Return value</span></span>

<span data-ttu-id="49d31-130">Возвращает количество кодовых точек UTF-16 в имени языкового стандарта, включая завершающий нуль-символ, в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="49d31-130">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span>

<span data-ttu-id="49d31-131">Эта функция возвращает 0, если она не выполнена.</span><span class="sxs-lookup"><span data-stu-id="49d31-131">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="49d31-132">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="49d31-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="49d31-133">Ошибка \_ : недостаточный \_ Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="49d31-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="49d31-134">Указанный размер буфера не достаточен или имеет неправильное значение **null**.</span><span class="sxs-lookup"><span data-stu-id="49d31-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="49d31-135">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="49d31-135">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="49d31-136">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="49d31-136">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="49d31-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49d31-137">Remarks</span></span>

<span data-ttu-id="49d31-138">Требуемый заголовочный файл и библиотека DLL являются частью скачивания "API сопоставления данных нижнего уровня Microsoft NLS", доступного в [центре загрузки Майкрософт](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="49d31-138">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="49d31-139">Требования</span><span class="sxs-lookup"><span data-stu-id="49d31-139">Requirements</span></span>



| <span data-ttu-id="49d31-140">Требование</span><span class="sxs-lookup"><span data-stu-id="49d31-140">Requirement</span></span> | <span data-ttu-id="49d31-141">Значение</span><span class="sxs-lookup"><span data-stu-id="49d31-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49d31-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49d31-142">Minimum supported client</span></span><br/> | <span data-ttu-id="49d31-143">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="49d31-143">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="49d31-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49d31-144">Minimum supported server</span></span><br/> | <span data-ttu-id="49d31-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49d31-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49d31-146">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="49d31-146">Redistributable</span></span><br/>          | <span data-ttu-id="49d31-147">API-интерфейсы сопоставления данных нижнего уровня Microsoft NLS в Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="49d31-147">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and later</span></span><br/>  |
| <span data-ttu-id="49d31-148">Header</span><span class="sxs-lookup"><span data-stu-id="49d31-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="49d31-149"><dt>Нлсдл. h</dt></span><span class="sxs-lookup"><span data-stu-id="49d31-149"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="49d31-150">DLL</span><span class="sxs-lookup"><span data-stu-id="49d31-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49d31-151"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49d31-151"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49d31-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49d31-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d31-153">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="49d31-153">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="49d31-154">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="49d31-154">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="49d31-155">Сопоставление данных локали</span><span class="sxs-lookup"><span data-stu-id="49d31-155">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="49d31-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="49d31-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
