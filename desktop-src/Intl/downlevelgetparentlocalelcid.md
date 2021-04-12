---
description: Получает идентификатор локали для родительского элемента поддерживаемого языкового стандарта.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Функция ДовнлевелжетпарентлокалелЦид (Нлсдл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348145"
---
# <a name="downlevelgetparentlocalelcid-function"></a><span data-ttu-id="afd7b-103">Функция ДовнлевелжетпарентлокалелЦид</span><span class="sxs-lookup"><span data-stu-id="afd7b-103">DownlevelGetParentLocaleLCID function</span></span>

<span data-ttu-id="afd7b-104">Получает [идентификатор локали](locale-identifiers.md) для родительского элемента поддерживаемого языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="afd7b-104">Retrieves the [locale identifier](locale-identifiers.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="afd7b-105">Эта функция используется только приложениями, работающими в операционных системах, предшествующих Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="afd7b-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="afd7b-106">Для его использования требуется загружаемый пакет.</span><span class="sxs-lookup"><span data-stu-id="afd7b-106">Its use requires the download package.</span></span> <span data-ttu-id="afd7b-107">Приложения, которые работают только в Windows Vista и более поздних версиях, должны вызывать [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) с *LCType* , установленным в [locale \_ спарент](locale-sparent.md).</span><span class="sxs-lookup"><span data-stu-id="afd7b-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="afd7b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afd7b-108">Syntax</span></span>


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a><span data-ttu-id="afd7b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="afd7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afd7b-110">*Языковой стандарт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afd7b-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd7b-111">Идентификатор локали языкового стандарта, для которого необходимо получить родительский идентификатор локали.</span><span class="sxs-lookup"><span data-stu-id="afd7b-111">Locale identifier of the locale for which to retrieve the parent locale identifier.</span></span> <span data-ttu-id="afd7b-112">С помощью макроса [**макелЦид**](/windows/desktop/api/Winnt/nf-winnt-makelcid) можно создать идентификатор языкового стандарта или использовать одно из следующих предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="afd7b-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="afd7b-113">ИНВАРИАНТный ЯЗЫКовой стандарт \_</span><span class="sxs-lookup"><span data-stu-id="afd7b-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="afd7b-114">система языкового стандарта \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="afd7b-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="afd7b-115">\_Пользовательская Национальная настройка \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="afd7b-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="afd7b-116">**Windows Vista и более поздние версии:** Также поддерживаются следующие пользовательские идентификаторы языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="afd7b-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="afd7b-117">Пользовательский ЯЗЫКовой стандарт \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="afd7b-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="afd7b-118">Пользовательский пользовательский интерфейс языкового стандарта \_ \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="afd7b-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="afd7b-119">Пользовательский ЯЗЫКовой стандарт не \_ \_ указан</span><span class="sxs-lookup"><span data-stu-id="afd7b-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afd7b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afd7b-120">Return value</span></span>

<span data-ttu-id="afd7b-121">Возвращает родительский идентификатор локали в случае успеха или 0 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="afd7b-121">Returns the parent locale identifier if successful, or 0 otherwise.</span></span> <span data-ttu-id="afd7b-122">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="afd7b-122">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="afd7b-123">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="afd7b-123">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="afd7b-124">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="afd7b-124">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="afd7b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afd7b-125">Remarks</span></span>

<span data-ttu-id="afd7b-126">Требуемый заголовочный файл и библиотека DLL являются частью скачивания "API сопоставления данных нижнего уровня Microsoft NLS", доступного в [центре загрузки Майкрософт](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="afd7b-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="afd7b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="afd7b-127">Requirements</span></span>



| <span data-ttu-id="afd7b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="afd7b-128">Requirement</span></span> | <span data-ttu-id="afd7b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="afd7b-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afd7b-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afd7b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="afd7b-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="afd7b-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="afd7b-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afd7b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="afd7b-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="afd7b-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afd7b-134">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="afd7b-134">Redistributable</span></span><br/>          | <span data-ttu-id="afd7b-135">Интерфейсы API сопоставления данных нижнего уровня Microsoft NLS в Windows Кспор Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afd7b-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XPor Windows Vista</span></span><br/>     |
| <span data-ttu-id="afd7b-136">Header</span><span class="sxs-lookup"><span data-stu-id="afd7b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="afd7b-137"><dt>Нлсдл. h</dt></span><span class="sxs-lookup"><span data-stu-id="afd7b-137"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="afd7b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="afd7b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afd7b-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afd7b-139"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afd7b-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afd7b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afd7b-141">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="afd7b-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="afd7b-142">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="afd7b-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="afd7b-143">Сопоставление данных локали</span><span class="sxs-lookup"><span data-stu-id="afd7b-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="afd7b-144">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="afd7b-144">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
