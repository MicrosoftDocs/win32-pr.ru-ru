---
description: С каждым языковым стандартом связан тип календаря по умолчанию (тип данных КАЛТИПЕ). Языковой стандарт может также иметь альтернативный тип календаря. Дополнительные сведения о типах календарей см. в разделе сведения о типах календарей.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Дата и календарь
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a3c21965bfbf8c4215b478e5c3b4adbae579ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912555"
---
# <a name="date-and-calendar"></a><span data-ttu-id="3abce-105">Дата и календарь</span><span class="sxs-lookup"><span data-stu-id="3abce-105">Date and Calendar</span></span>

<span data-ttu-id="3abce-106">С каждым [языковым стандартом](locales-and-languages.md) связан тип календаря по умолчанию (тип данных калтипе).</span><span class="sxs-lookup"><span data-stu-id="3abce-106">Each [locale](locales-and-languages.md) has a default calendar type (data type CALTYPE) associated with it.</span></span> <span data-ttu-id="3abce-107">Языковой стандарт может также иметь альтернативный тип календаря.</span><span class="sxs-lookup"><span data-stu-id="3abce-107">A locale can also have an alternate calendar type.</span></span> <span data-ttu-id="3abce-108">Дополнительные сведения о типах календарей см. в разделе [сведения о типах календарей](calendar-type-information.md).</span><span class="sxs-lookup"><span data-stu-id="3abce-108">For details of calendar types, see [Calendar Type Information](calendar-type-information.md).</span></span>

> [!Note]  
> <span data-ttu-id="3abce-109">Чтобы использовать альтернативный тип календаря для языкового стандарта, приложение должно задать для параметра [locale \_ иоптионалкалендар](locale-ioptionalcalendar.md) константу альтернативный тип календаря для локали.</span><span class="sxs-lookup"><span data-stu-id="3abce-109">To use an alternate calendar type for a locale, your application must set the [LOCALE\_IOPTIONALCALENDAR](locale-ioptionalcalendar.md) constant to the alternate calendar type for the locale.</span></span>

 

<span data-ttu-id="3abce-110">Большинство языковых стандартов используют стандартный григорианский календарь и заданное число форматов даты.</span><span class="sxs-lookup"><span data-stu-id="3abce-110">Most locales use the standard Gregorian calendar and a set number of date formats.</span></span> <span data-ttu-id="3abce-111">Эти параметры по умолчанию для форматов даты доступны для просмотра с помощью функции [**енумдатеформатсекс**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) или [**енумдатеформатсексекс**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) .</span><span class="sxs-lookup"><span data-stu-id="3abce-111">These default choices for date formats are available for display by using the [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) or [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) function.</span></span>

<span data-ttu-id="3abce-112">При создании полного списка вариантов формата для некоторых языков требуется учитывать особые соображения.</span><span class="sxs-lookup"><span data-stu-id="3abce-112">Some locales require special considerations when creating a complete list of format choices.</span></span> <span data-ttu-id="3abce-113">Для некоторых из этих языков строки текста должны вставляться в строку формата даты, а для других требуется совершенно другой метод вычисления значений.</span><span class="sxs-lookup"><span data-stu-id="3abce-113">Some of these locales require text strings to be inserted in the date format string, while others require a completely different method of computation of the values.</span></span> <span data-ttu-id="3abce-114">Приложение решает эти особые требования, добавив определенные типы сведений о языковых стандартах и типы календарей.</span><span class="sxs-lookup"><span data-stu-id="3abce-114">An application addresses these special requirements by the addition of certain locale information types and calendar types.</span></span>

<span data-ttu-id="3abce-115">Дополнительные сведения о реализации дат и календарей в приложениях см. в разделе [Получение сведений о времени и датах](retrieving-time-and-date-information.md).</span><span class="sxs-lookup"><span data-stu-id="3abce-115">For details about implementing dates and calendars in your applications, see [Retrieving Time and Date Information](retrieving-time-and-date-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3abce-116">См. также</span><span class="sxs-lookup"><span data-stu-id="3abce-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3abce-117">Сведения о поддержке национальных языков</span><span class="sxs-lookup"><span data-stu-id="3abce-117">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="3abce-118">Сведения о типе календаря</span><span class="sxs-lookup"><span data-stu-id="3abce-118">Calendar Type Information</span></span>](calendar-type-information.md)
</dt> <dt>

[<span data-ttu-id="3abce-119">Получение сведений о времени и дате</span><span class="sxs-lookup"><span data-stu-id="3abce-119">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="3abce-120">**енумдатеформатсекс**</span><span class="sxs-lookup"><span data-stu-id="3abce-120">**EnumDateFormatsEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[<span data-ttu-id="3abce-121">**енумдатеформатсексекс**</span><span class="sxs-lookup"><span data-stu-id="3abce-121">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



