---
description: Каждый языковой стандарт имеет уникальный идентификатор, 32-разрядное значение, состоящее из идентификатора языка и идентификатора порядка сортировки.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Идентификаторы языкового стандарта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682402"
---
# <a name="locale-identifiers"></a><span data-ttu-id="433c0-103">Идентификаторы языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="433c0-103">Locale Identifiers</span></span>

<span data-ttu-id="433c0-104">Каждый [языковой стандарт](locales-and-languages.md) имеет уникальный идентификатор, 32-разрядное значение, состоящее из [идентификатора языка](language-identifiers.md) и [идентификатора порядка сортировки](sort-order-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="433c0-104">Each [locale](locales-and-languages.md) has a unique identifier, a 32-bit value that consists of a [language identifier](language-identifiers.md) and a [sort order identifier](sort-order-identifiers.md).</span></span> <span data-ttu-id="433c0-105">Идентификатор локали является стандартным международным числовым сокращением и содержит компоненты, необходимые для уникальной идентификации одного из установленных языковых стандартов, определенных операционной системой.</span><span class="sxs-lookup"><span data-stu-id="433c0-105">The locale identifier is a standard international numeric abbreviation and has the components necessary to uniquely identify one of the installed operating system-defined locales.</span></span> <span data-ttu-id="433c0-106">NLS поддерживает как предопределенные идентификаторы локали, так и пользовательские идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="433c0-106">NLS supports both predefined locale identifiers and custom identifiers.</span></span>

> [!Note]  
> <span data-ttu-id="433c0-107">Имена языковых стандартов можно использовать с функциями, появившимися в Windows Vista, которые принимают в качестве параметра [имя локали](locale-names.md) вместо идентификатора локали.</span><span class="sxs-lookup"><span data-stu-id="433c0-107">Locale names can be used with functions introduced in Windows Vista that take a [locale name](locale-names.md) as a parameter, instead of a locale identifier.</span></span> <span data-ttu-id="433c0-108">Дополнительные сведения см. [в разделе вызов функций locale Name](calling-the--locale-name--functions.md).</span><span class="sxs-lookup"><span data-stu-id="433c0-108">For more information, see [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md).</span></span> <span data-ttu-id="433c0-109">Использование имен языковых стандартов вместо идентификаторов языкового стандарта всегда является предпочтительным.</span><span class="sxs-lookup"><span data-stu-id="433c0-109">Use of locale names instead of locale identifiers is always preferable.</span></span>

 

<span data-ttu-id="433c0-110">На следующем рисунке показан формат битов в идентификаторе локали.</span><span class="sxs-lookup"><span data-stu-id="433c0-110">The following illustration shows the format of the bits in a locale identifier.</span></span>

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a><span data-ttu-id="433c0-111">Предопределенные идентификаторы языковых стандартов</span><span class="sxs-lookup"><span data-stu-id="433c0-111">Predefined Locale Identifiers</span></span>

<span data-ttu-id="433c0-112">Стандартные идентификаторы языкового стандарта, поддерживаемые NLS, определяются в [справочнике по API поддержки национальных языков (NLS)](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span><span class="sxs-lookup"><span data-stu-id="433c0-112">The predefined locale identifiers supported by NLS are defined in the [National Language Support (NLS) API Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span></span>

<span data-ttu-id="433c0-113">NLS использует следующие сведения о языковых стандартах для представления идентификаторов языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="433c0-113">NLS uses the following locale information constants to represent locale identifiers.</span></span>

-   <span data-ttu-id="433c0-114">[Языковой стандарт \_ СЛАНГУАЖЕ](locale-slanguage.md) или [ \_ слокализедлангуаженаме locale](locale-slocalized-constants.md)</span><span class="sxs-lookup"><span data-stu-id="433c0-114">[LOCALE\_SLANGUAGE](locale-slanguage.md) or [LOCALE\_SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span></span>
-   [<span data-ttu-id="433c0-115">SNAME ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="433c0-115">LOCALE\_SNAME</span></span>](locale-sname.md)
-   [<span data-ttu-id="433c0-116">сскриптс ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="433c0-116">LOCALE\_SSCRIPTS</span></span>](locale-sscripts.md)
-   [<span data-ttu-id="433c0-117">идефаултансикодепаже ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="433c0-117">LOCALE\_IDEFAULTANSICODEPAGE</span></span>](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a><span data-ttu-id="433c0-118">Пользовательские идентификаторы языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="433c0-118">Custom Locale Identifiers</span></span>

<span data-ttu-id="433c0-119">**Windows Vista:** NLS поддерживает пользовательские идентификаторы языкового стандарта, представленные следующими константами сведений о языковых стандартах.</span><span class="sxs-lookup"><span data-stu-id="433c0-119">**Windows Vista:** NLS supports the custom locale identifiers represented by the following locale information constants.</span></span>

-   [<span data-ttu-id="433c0-120">Пользовательский ЯЗЫКовой стандарт \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="433c0-120">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="433c0-121">Пользовательский пользовательский интерфейс языкового стандарта \_ \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="433c0-121">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="433c0-122">Пользовательский ЯЗЫКовой стандарт не \_ \_ указан</span><span class="sxs-lookup"><span data-stu-id="433c0-122">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

## <a name="building-a-locale"></a><span data-ttu-id="433c0-123">Создание языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="433c0-123">Building a Locale</span></span>

<span data-ttu-id="433c0-124">Для сборки языковых стандартов можно использовать программу, предоставляемую NLS.</span><span class="sxs-lookup"><span data-stu-id="433c0-124">You can use the Locale Builder utility provided by NLS to build locales.</span></span> <span data-ttu-id="433c0-125">Дополнительные сведения см. в разделе [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).</span><span class="sxs-lookup"><span data-stu-id="433c0-125">For more information, see [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).</span></span>

<span data-ttu-id="433c0-126">Приложение может создать код локали с помощью макроса [**макелЦид**](/windows/desktop/api/Winnt/nf-winnt-makelcid) .</span><span class="sxs-lookup"><span data-stu-id="433c0-126">Your application can construct a locale identifier using the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro.</span></span> <span data-ttu-id="433c0-127">Кроме того, можно использовать один из идентификаторов по умолчанию, соответствующий константам, перечисленным ниже.</span><span class="sxs-lookup"><span data-stu-id="433c0-127">Alternatively it can use one of the default identifiers corresponding to the constants listed below.</span></span>

-   [<span data-ttu-id="433c0-128">ИНВАРИАНТный ЯЗЫКовой стандарт \_</span><span class="sxs-lookup"><span data-stu-id="433c0-128">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="433c0-129">система языкового стандарта \_ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="433c0-129">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="433c0-130">\_Пользовательская Национальная настройка \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="433c0-130">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a><span data-ttu-id="433c0-131">Получение идентификаторов языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="433c0-131">Retrieval of Locale Identifiers</span></span>

<span data-ttu-id="433c0-132">Приложение может извлекать текущие идентификаторы языковых стандартов с помощью функций [**жетсистемдефаултлЦид**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) и [**жетусердефаултлЦид**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) .</span><span class="sxs-lookup"><span data-stu-id="433c0-132">An application can retrieve the current locale identifiers by using the [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) and [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) functions.</span></span> <span data-ttu-id="433c0-133">Каждый поток может устанавливать и получать собственный языковой стандарт с помощью [**сетсреадлокале**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) и [**жетсреадлокале**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span><span class="sxs-lookup"><span data-stu-id="433c0-133">Each thread can set and retrieve its own locale with [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) and [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="433c0-134">См. также</span><span class="sxs-lookup"><span data-stu-id="433c0-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="433c0-135">Языковые стандарты и языки</span><span class="sxs-lookup"><span data-stu-id="433c0-135">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="433c0-136">Идентификаторы языка</span><span class="sxs-lookup"><span data-stu-id="433c0-136">Language Identifiers</span></span>](language-identifiers.md)
</dt> <dt>

[<span data-ttu-id="433c0-137">Имена языковых стандартов</span><span class="sxs-lookup"><span data-stu-id="433c0-137">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="433c0-138">Идентификаторы порядка сортировки</span><span class="sxs-lookup"><span data-stu-id="433c0-138">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="433c0-139">**макелЦид**</span><span class="sxs-lookup"><span data-stu-id="433c0-139">**MAKELCID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
