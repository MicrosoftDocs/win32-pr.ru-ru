---
description: 'Windows Vista и более поздние версии: NLS определяет несколько псевдо-национальных настроек для использования в дополнение к существующим языкам Windows.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682623"
---
# <a name="pseudo-locales"></a><span data-ttu-id="0deb4-103">Pseudo-Locales</span><span class="sxs-lookup"><span data-stu-id="0deb4-103">Pseudo-Locales</span></span>

<span data-ttu-id="0deb4-104">**Windows Vista и более поздние версии:** NLS определяет несколько псевдо-национальных настроек для использования в дополнение к существующим языкам Windows.</span><span class="sxs-lookup"><span data-stu-id="0deb4-104">**Windows Vista and later:** NLS defines several pseudo-locales for use in addition to the existing Windows locales.</span></span> <span data-ttu-id="0deb4-105">Используйте эти псевдо-национальные настройки для тестирования локализации приложений.</span><span class="sxs-lookup"><span data-stu-id="0deb4-105">Use these pseudo-locales for testing the localization of your applications.</span></span> <span data-ttu-id="0deb4-106">Сведения о реализации см. [в разделе использование Pseudo-Locales для тестирования локализации](using-pseudo-locales-for-localization-testing.md).</span><span class="sxs-lookup"><span data-stu-id="0deb4-106">For implementation details, see [Using Pseudo-Locales for Localization Testing](using-pseudo-locales-for-localization-testing.md).</span></span>

## <a name="supported-pseudo-locales"></a><span data-ttu-id="0deb4-107">Поддерживаемые Pseudo-Locales</span><span class="sxs-lookup"><span data-stu-id="0deb4-107">Supported Pseudo-Locales</span></span>

<span data-ttu-id="0deb4-108">В NLS поддерживаются следующие псевдо-языковые стандарты:</span><span class="sxs-lookup"><span data-stu-id="0deb4-108">The pseudo-locales supported by NLS are:</span></span>

-   <span data-ttu-id="0deb4-109">Базовая псевдо-Национальная настройка</span><span class="sxs-lookup"><span data-stu-id="0deb4-109">Base pseudo-locale</span></span>
-   <span data-ttu-id="0deb4-110">Псевдо-locale с зеркальным отображением (справа налево)</span><span class="sxs-lookup"><span data-stu-id="0deb4-110">Mirrored (right-to-left) pseudo-locale</span></span>
-   <span data-ttu-id="0deb4-111">Восточно-Азиатский языковой стандарт</span><span class="sxs-lookup"><span data-stu-id="0deb4-111">East Asian-language pseudo-locale</span></span>

<span data-ttu-id="0deb4-112">Выберите определенный псевдо-locale для использования в соответствии с назначениями кодовых страниц и строками для локализации, например названия месяцев, названия дней.</span><span class="sxs-lookup"><span data-stu-id="0deb4-112">Choose the particular pseudo-locale to use based on its code page assignments and the strings for localization, for example, month names, day names.</span></span> <span data-ttu-id="0deb4-113">Данные для каждого псевдо-локали включают не только соответствующие кодовые страницы и строки дня и месяца для локализации, но и данные для нескольких других тестовых случаев для NLS.</span><span class="sxs-lookup"><span data-stu-id="0deb4-113">Data for each pseudo-locale includes not only relevant code pages and day and month strings for localization, but also data for several other test cases for NLS.</span></span> <span data-ttu-id="0deb4-114">Тестовые случаи проверяют следующие типы данных:</span><span class="sxs-lookup"><span data-stu-id="0deb4-114">The test cases examine the following types of data:</span></span>

-   <span data-ttu-id="0deb4-115">9-разрядные [идентификаторы языкового стандарта](locale-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="0deb4-115">9-bit [locale identifiers](locale-identifiers.md).</span></span> <span data-ttu-id="0deb4-116">Псевдо-национальные настройки дают возможность протестировать работу 9-разрядных идентификаторов языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="0deb4-116">Pseudo-locales provide a good opportunity to test the operation of 9-bit locale identifiers.</span></span>
-   <span data-ttu-id="0deb4-117">Строки из языков, которые должны использовать небольшие шрифты.</span><span class="sxs-lookup"><span data-stu-id="0deb4-117">Strings from languages that must use small fonts.</span></span> <span data-ttu-id="0deb4-118">Из-за ограничений в интерфейсе графических устройств (GDI) шрифт пользовательского интерфейса для некоторых языков меньше, чем оптимальный.</span><span class="sxs-lookup"><span data-stu-id="0deb4-118">Because of limitations in the graphics device interface (GDI), the user interface font for some languages is smaller than optimal.</span></span> <span data-ttu-id="0deb4-119">Псевдо-национальные настройки включают несколько строк из этих языков в сочетании со строками из языков с более стандартной обработкой шрифтов.</span><span class="sxs-lookup"><span data-stu-id="0deb4-119">Pseudo-locales include several strings from these languages, combined with strings from languages with more standard font handling.</span></span> <span data-ttu-id="0deb4-120">Эти строки можно использовать в тестировании для определения способа отрисовки шрифта, ограниченного GDI.</span><span class="sxs-lookup"><span data-stu-id="0deb4-120">You can use these strings in testing to determine how a GDI-limited font renders.</span></span>
-   <span data-ttu-id="0deb4-121">Нестандартные длины строк.</span><span class="sxs-lookup"><span data-stu-id="0deb4-121">Unusual string lengths.</span></span> <span data-ttu-id="0deb4-122">Некоторые константы информации о языковых стандартах, например [региональные \_ слист](locale-slist.md) и [ \_ икурренци locale](locale-icurrency.md), имеют стандартные ограничения на размер строки.</span><span class="sxs-lookup"><span data-stu-id="0deb4-122">Some locale information constants, for example, [LOCALE\_SLIST](locale-slist.md) and [LOCALE\_ICURRENCY](locale-icurrency.md), have conventional limits on string size.</span></span> <span data-ttu-id="0deb4-123">Псевдо-национальные настройки поддерживают проверку изменяемой длины строк.</span><span class="sxs-lookup"><span data-stu-id="0deb4-123">The pseudo-locales support the examination of varied string lengths.</span></span>
-   <span data-ttu-id="0deb4-124">Альтернативные сортировки.</span><span class="sxs-lookup"><span data-stu-id="0deb4-124">Alternate sorts.</span></span> <span data-ttu-id="0deb4-125">Псевдо-национальные настройки можно использовать для проверки альтернативной функции сортировки, если альтернативный [Идентификатор порядка сортировки](sort-order-identifiers.md) отличается от базового идентификатора порядка сортировки, который обычно связан с языковым стандартом.</span><span class="sxs-lookup"><span data-stu-id="0deb4-125">Pseudo-locales can be used to test alternate sort functionality when the alternate [sort order identifier](sort-order-identifiers.md) differs from the base sort order identifier that is usually associated with the locale.</span></span>

## <a name="pseudo-locale-names-and-identifiers"></a><span data-ttu-id="0deb4-126">Имена и идентификаторы псевдо-локалей</span><span class="sxs-lookup"><span data-stu-id="0deb4-126">Pseudo-locale Names and Identifiers</span></span>

<span data-ttu-id="0deb4-127">В псевдокодах используются [имена языковых стандартов](locale-names.md) , которые выбираются из пространства частного использования во избежание конфликта с возможными строками, представленными в стандартах Международная организация по стандартизации (iso) 639 и ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="0deb4-127">The pseudo-locales have [locale names](locale-names.md) that are chosen from the private use space to avoid conflict with possible strings introduced into the International Organization for Standardization (ISO) 639 and ISO 3166 standards.</span></span> <span data-ttu-id="0deb4-128">Каждый псевдо-locale также имеет свой собственный идентификатор локали.</span><span class="sxs-lookup"><span data-stu-id="0deb4-128">Each pseudo-locale also has its own locale identifier.</span></span> <span data-ttu-id="0deb4-129">В следующей таблице приведены имена и идентификаторы для определенных псевдо-языков.</span><span class="sxs-lookup"><span data-stu-id="0deb4-129">The following table provides the names and identifiers for the defined pseudo-locales.</span></span>



| <span data-ttu-id="0deb4-130">Псевдо-locale</span><span class="sxs-lookup"><span data-stu-id="0deb4-130">Pseudo-locale</span></span>       | <span data-ttu-id="0deb4-131">Имя языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="0deb4-131">Locale name</span></span> | <span data-ttu-id="0deb4-132">Идентификатор локали</span><span class="sxs-lookup"><span data-stu-id="0deb4-132">Locale identifier</span></span> |
|---------------------|-------------|-------------------|
| <span data-ttu-id="0deb4-133">Основной</span><span class="sxs-lookup"><span data-stu-id="0deb4-133">Base</span></span>                | <span data-ttu-id="0deb4-134">QPS — Плок</span><span class="sxs-lookup"><span data-stu-id="0deb4-134">qps-ploc</span></span>    | <span data-ttu-id="0deb4-135">0501</span><span class="sxs-lookup"><span data-stu-id="0deb4-135">0501</span></span>              |
| <span data-ttu-id="0deb4-136">Зеркальный том</span><span class="sxs-lookup"><span data-stu-id="0deb4-136">Mirrored</span></span>            | <span data-ttu-id="0deb4-137">QPS — плокм</span><span class="sxs-lookup"><span data-stu-id="0deb4-137">qps-plocm</span></span>   | <span data-ttu-id="0deb4-138">09ff</span><span class="sxs-lookup"><span data-stu-id="0deb4-138">09ff</span></span>              |
| <span data-ttu-id="0deb4-139">Восточно-азиатский язык</span><span class="sxs-lookup"><span data-stu-id="0deb4-139">East Asian-language</span></span> | <span data-ttu-id="0deb4-140">QPS — плока</span><span class="sxs-lookup"><span data-stu-id="0deb4-140">qps-ploca</span></span>   | <span data-ttu-id="0deb4-141">05fe</span><span class="sxs-lookup"><span data-stu-id="0deb4-141">05fe</span></span>              |



 

## <a name="example"></a><span data-ttu-id="0deb4-142">Пример</span><span class="sxs-lookup"><span data-stu-id="0deb4-142">Example</span></span>

<span data-ttu-id="0deb4-143">В следующем примере показан текст, отображаемый для базовой псевдо-локали:</span><span class="sxs-lookup"><span data-stu-id="0deb4-143">The following example shows text displayed for a base pseudo-locale:</span></span>

<span data-ttu-id="0deb4-144">\[Шěđлеśđαỳ!!! \] , 8 ōф \[ μäŕςћ!! \] ōф 2006</span><span class="sxs-lookup"><span data-stu-id="0deb4-144">\[Шěđлеśđαỳ !!!\], 8 ōf \[Μäŕςћ !!\] ōf 2006</span></span>

## <a name="related-topics"></a><span data-ttu-id="0deb4-145">См. также</span><span class="sxs-lookup"><span data-stu-id="0deb4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0deb4-146">Языковые стандарты и языки</span><span class="sxs-lookup"><span data-stu-id="0deb4-146">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="0deb4-147">Идентификаторы языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="0deb4-147">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="0deb4-148">Имена языковых стандартов</span><span class="sxs-lookup"><span data-stu-id="0deb4-148">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="0deb4-149">Идентификаторы порядка сортировки</span><span class="sxs-lookup"><span data-stu-id="0deb4-149">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="0deb4-150">Использование Pseudo-Locales для тестирования локализации</span><span class="sxs-lookup"><span data-stu-id="0deb4-150">Using Pseudo-Locales for Localization Testing</span></span>](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



