---
description: Преобразует имя языкового стандарта в идентификатор локали, который может использоваться для получения сведений из операционной системы.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Функция ДовнлевеллокаленаметолЦид (Нлсдл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651118"
---
# <a name="downlevellocalenametolcid-function"></a><span data-ttu-id="4c3fa-103">Функция ДовнлевеллокаленаметолЦид</span><span class="sxs-lookup"><span data-stu-id="4c3fa-103">DownlevelLocaleNameToLCID function</span></span>

<span data-ttu-id="4c3fa-104">Преобразует [имя языкового](locale-names.md) стандарта в [идентификатор локали](locale-identifiers.md) , который может использоваться для получения сведений из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-104">Converts a [locale name](locale-names.md) to a [locale identifier](locale-identifiers.md) that can be used to get information from the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="4c3fa-105">Эта функция используется только приложениями, работающими в операционных системах, предшествующих Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="4c3fa-106">Для его использования требуется загружаемый пакет.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-106">Its use requires a download package.</span></span> <span data-ttu-id="4c3fa-107">Приложения, которые работают только в Windows Vista и более поздних версиях, должны вызывать [**локаленаметолЦид**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) для получения идентификатора локали.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-107">Applications that only run on Windows Vista and later should call [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) to retrieve a locale identifier.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4c3fa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c3fa-108">Syntax</span></span>


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4c3fa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c3fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c3fa-110">*лпнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c3fa-110">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c3fa-111">Указатель на строку, завершающуюся нулем и представляющую [имя локали](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="4c3fa-111">Pointer to a null-terminated string representing a [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c3fa-112">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c3fa-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c3fa-113">Флаги, указывающие тип имени.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-113">Flags specifying the type of name.</span></span> <span data-ttu-id="4c3fa-114">По умолчанию используется \_ имя локали нижнего уровня \_ .</span><span class="sxs-lookup"><span data-stu-id="4c3fa-114">The default is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c3fa-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c3fa-115">Return value</span></span>

<span data-ttu-id="4c3fa-116">Возвращает идентификатор локали, соответствующий имени локали в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-116">Returns the locale identifier that corresponds to the locale name if successful.</span></span>

<span data-ttu-id="4c3fa-117">Функция возвращает 0, если она не выполнена.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-117">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="4c3fa-118">Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="4c3fa-118">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="4c3fa-119">Ошибка \_ : недопустимые \_ флаги.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-119">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="4c3fa-120">Указаны недопустимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-120">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="4c3fa-121">Ошибка \_ : недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-121">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="4c3fa-122">Любое из значений параметров было недопустимым.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-122">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c3fa-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c3fa-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c3fa-124">Эта функция не поддерживает Нейтральные языковые стандарты.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-124">This function does not support neutral locales.</span></span> <span data-ttu-id="4c3fa-125">Эквивалентная функция [**локаленаметолЦид**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) поддерживает [пользовательские языковые стандарты](custom-locales.md), но только для Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="4c3fa-125">The equivalent [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function supports [custom locales](custom-locales.md), but only for Windows Vista and later.</span></span>

 

<span data-ttu-id="4c3fa-126">Требуемый заголовочный файл и библиотека DLL являются частью скачивания "API сопоставления данных нижнего уровня Microsoft NLS", доступного в [центре загрузки Майкрософт](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="4c3fa-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c3fa-127">Требования</span><span class="sxs-lookup"><span data-stu-id="4c3fa-127">Requirements</span></span>



| <span data-ttu-id="4c3fa-128">Требование</span><span class="sxs-lookup"><span data-stu-id="4c3fa-128">Requirement</span></span> | <span data-ttu-id="4c3fa-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4c3fa-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c3fa-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c3fa-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4c3fa-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4c3fa-131">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="4c3fa-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c3fa-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4c3fa-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4c3fa-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4c3fa-134">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="4c3fa-134">Redistributable</span></span><br/>          | <span data-ttu-id="4c3fa-135">Интерфейсы API сопоставления данных нижнего уровня Microsoft NLS в Windows XP с пакетом обновления 2 (SP2) и Латерорвиндовс Vista</span><span class="sxs-lookup"><span data-stu-id="4c3fa-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="4c3fa-136">Header</span><span class="sxs-lookup"><span data-stu-id="4c3fa-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c3fa-137"><dt>Нлсдл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c3fa-137"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="4c3fa-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4c3fa-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c3fa-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c3fa-139"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4c3fa-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c3fa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c3fa-141">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="4c3fa-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="4c3fa-142">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="4c3fa-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="4c3fa-143">Сопоставление данных локали</span><span class="sxs-lookup"><span data-stu-id="4c3fa-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="4c3fa-144">**локаленаметолЦид**</span><span class="sxs-lookup"><span data-stu-id="4c3fa-144">**LocaleNameToLCID**</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
