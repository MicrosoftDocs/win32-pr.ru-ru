---
description: Международные компоненты для Юникода (ICU) — это зрелый, широко используемый набор API-интерфейсов глобализации с открытым исходным кодом.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: Международные компоненты для Юникода (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560a2f344a3024685e17df0f434f8ffa040b5c8b
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349993"
---
# <a name="international-components-for-unicode-icu"></a><span data-ttu-id="572c3-103">Международные компоненты для Юникода (ICU)</span><span class="sxs-lookup"><span data-stu-id="572c3-103">International Components for Unicode (ICU)</span></span>

<span data-ttu-id="572c3-104">Международные компоненты для Юникода (ICU) — это зрелый, широко используемый набор API-интерфейсов глобализации с открытым исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="572c3-104">International Components for Unicode (ICU) is a mature, widely used set of open-source globalization APIs.</span></span> <span data-ttu-id="572c3-105">ICU использует обширный общий языковой стандарт Юникода (КЛДР) в качестве библиотеки данных, предоставляя поддержку глобализации для приложений программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="572c3-105">ICU utilizes Unicode's vast Common Locale Data Repository (CLDR) as its data library, providing globalization support for software applications.</span></span> <span data-ttu-id="572c3-106">ICU является широко переносимым и дает приложениям одинаковые результаты во всех платформах.</span><span class="sxs-lookup"><span data-stu-id="572c3-106">ICU is widely portable and gives applications the same results across on all platforms.</span></span>

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a><span data-ttu-id="572c3-107">Основные особенности служб API глобализации, предоставляемых ICU</span><span class="sxs-lookup"><span data-stu-id="572c3-107">Highlights of the Globalization API services provided by ICU</span></span>

-   <span data-ttu-id="572c3-108">**Преобразование кодовой страницы**: Преобразование текстовых данных в Юникод или из Юникода, а также практически любой другой набор символов или кодировка.</span><span class="sxs-lookup"><span data-stu-id="572c3-108">**Code Page Conversion**: Convert text data to or from Unicode and nearly any other character set or encoding.</span></span> <span data-ttu-id="572c3-109">Таблицы преобразования ICU основаны на данных кодировки, собираемых IBM на протяжении многих десятилетий, и являются наиболее полными доступными в любом месте.</span><span class="sxs-lookup"><span data-stu-id="572c3-109">ICU's conversion tables are based on charset data collected by IBM over the course of many decades, and is the most complete available anywhere.</span></span>
-   <span data-ttu-id="572c3-110">**Параметры сортировки**: Сравните строки в соответствии с соглашениями и стандартами определенного языка, региона или страны.</span><span class="sxs-lookup"><span data-stu-id="572c3-110">**Collation**: Compare strings according to the conventions and standards of a particular language, region or country.</span></span> <span data-ttu-id="572c3-111">Параметры сортировки ICU основаны на алгоритме сортировки Юникода и правилах сравнения для конкретного языкового стандарта от КЛДР.</span><span class="sxs-lookup"><span data-stu-id="572c3-111">ICU's collation is based on the Unicode Collation Algorithm plus locale-specific comparison rules from CLDR.</span></span>
-   <span data-ttu-id="572c3-112">**Форматирование**: форматирование чисел, дат, времени и денежных сумм в соответствии с соглашениями выбранного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="572c3-112">**Formatting**: Format numbers, dates, times and currency amounts according the conventions of a chosen locale.</span></span> <span data-ttu-id="572c3-113">Сюда входит преобразование названий месяцев и дней в выбранный язык, выбор соответствующих сокращений, правильное упорядочивание полей и т. д. Эти данные также поступают из репозитория данных общего языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="572c3-113">This includes translating month and day names into the selected language, choosing appropriate abbreviations, ordering fields correctly, etc. This data also comes from the Common Locale Data Repository.</span></span>
-   <span data-ttu-id="572c3-114">**Вычисления времени**. несколько типов календарей предоставляются за пределами обычного григорианского календаря.</span><span class="sxs-lookup"><span data-stu-id="572c3-114">**Time Calculations**: Multiple types of calendars are provided beyond the traditional Gregorian.</span></span> <span data-ttu-id="572c3-115">Предоставляется тщательный набор API-интерфейсов для вычисления часовых поясов.</span><span class="sxs-lookup"><span data-stu-id="572c3-115">A thorough set of time zone calculation APIs are provided.</span></span>
-   <span data-ttu-id="572c3-116">**Поддержка Юникода**. ICU тесно отслеживает Стандарт Юникода, обеспечивая легкий доступ ко всем свойствам символов Юникода, нормализации Юникода, сложению регистра и другим фундаментальным операциям, указанным в [стандарте Юникода](https://www.unicode.org/).</span><span class="sxs-lookup"><span data-stu-id="572c3-116">**Unicode Support**: ICU closely tracks the Unicode standard, providing easy access to all of the many Unicode character properties, Unicode Normalization, Case Folding, and other fundamental operations as specified by the [Unicode Standard](https://www.unicode.org/).</span></span>
-   <span data-ttu-id="572c3-117">**Регулярное выражение**: регулярные выражения ICU полностью поддерживают Юникод, обеспечивая очень конкурентную производительность.</span><span class="sxs-lookup"><span data-stu-id="572c3-117">**Regular Expression**: ICU's regular expressions fully support Unicode while providing very competitive performance.</span></span>
-   <span data-ttu-id="572c3-118">**Bidi**: поддержка обработки текста, содержащего сочетание слева направо (английский) и справа налево (арабский или иврит).</span><span class="sxs-lookup"><span data-stu-id="572c3-118">**Bidi**: Support for handling text containing a mixture of left to right (English) and right to left (Arabic or Hebrew) data.</span></span>

<span data-ttu-id="572c3-119">Дополнительные сведения можно найти на веб-сайте ICU: <http://site.icu-project.org/></span><span class="sxs-lookup"><span data-stu-id="572c3-119">For more information, you can visit the ICU website: <http://site.icu-project.org/></span></span>

## <a name="overview"></a><span data-ttu-id="572c3-120">Обзор</span><span class="sxs-lookup"><span data-stu-id="572c3-120">Overview</span></span>

<span data-ttu-id="572c3-121">В Windows 10 Creators Update, ICU был интегрирован в Windows, делая интерфейсы API C общедоступными.</span><span class="sxs-lookup"><span data-stu-id="572c3-121">In Windows 10 Creators Update, ICU was integrated into Windows, making the C APIs and data publicly accessible.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="572c3-122">Версия ICU в Windows предоставляет только API C.</span><span class="sxs-lookup"><span data-stu-id="572c3-122">The version of ICU in Windows only exposes the C APIs.</span></span> <span data-ttu-id="572c3-123">Он не предоставляет никаких API-интерфейсов C++.</span><span class="sxs-lookup"><span data-stu-id="572c3-123">It does not expose any of the C++ APIs.</span></span> <span data-ttu-id="572c3-124">К сожалению, невозможность предоставления интерфейсов API C++ из-за отсутствия стабильного интерфейса ABI в C++.</span><span class="sxs-lookup"><span data-stu-id="572c3-124">Unfortunately, it is impossible to ever expose the C++ APIs due to the lack of a stable ABI in C++.</span></span>

<span data-ttu-id="572c3-125">Документацию по API ICU C см. на официальной странице документации по ICU: <http://icu-project.org/apiref/icu4c/index.html#Module></span><span class="sxs-lookup"><span data-stu-id="572c3-125">For documentation on the ICU C APIs, please refer to the official ICU documentation page here: <http://icu-project.org/apiref/icu4c/index.html#Module></span></span>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a><span data-ttu-id="572c3-126">Журнал изменений в библиотеке ICU в Windows</span><span class="sxs-lookup"><span data-stu-id="572c3-126">History of changes to the ICU library in Windows</span></span>

### <a name="version-1703-creators-update"></a><span data-ttu-id="572c3-127">Версия 1703 (авторское обновление)</span><span class="sxs-lookup"><span data-stu-id="572c3-127">Version 1703 (Creators Update)</span></span>
<span data-ttu-id="572c3-128">Библиотека ICU была впервые добавлена в ОС Windows 10 в этой версии.</span><span class="sxs-lookup"><span data-stu-id="572c3-128">The ICU library was first added to the Windows 10 OS in this version.</span></span>
<span data-ttu-id="572c3-129">Он был добавлен как:</span><span class="sxs-lookup"><span data-stu-id="572c3-129">It was added as:</span></span>
- <span data-ttu-id="572c3-130">Две системные библиотеки DLL:</span><span class="sxs-lookup"><span data-stu-id="572c3-130">Two system DLLs:</span></span>
    -   <span data-ttu-id="572c3-131">**icuuc.dll** (это ICU "Common" Библиотека)</span><span class="sxs-lookup"><span data-stu-id="572c3-131">**icuuc.dll** (this is the ICU "common" library)</span></span>
    -   <span data-ttu-id="572c3-132">**icuin.dll** (это библиотека ICU "i18n")</span><span class="sxs-lookup"><span data-stu-id="572c3-132">**icuin.dll** (this is the ICU "i18n" library)</span></span>
- <span data-ttu-id="572c3-133">Два файла заголовков в пакете SDK для Windows 10:</span><span class="sxs-lookup"><span data-stu-id="572c3-133">Two header files in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="572c3-134">**икукоммон. h**</span><span class="sxs-lookup"><span data-stu-id="572c3-134">**icucommon.h**</span></span>
    -   <span data-ttu-id="572c3-135">**icui18n. h**</span><span class="sxs-lookup"><span data-stu-id="572c3-135">**icui18n.h**</span></span>
- <span data-ttu-id="572c3-136">Две библиотеки импорта в пакете SDK для Windows 10:</span><span class="sxs-lookup"><span data-stu-id="572c3-136">Two import libs in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="572c3-137">**икуук. lib**</span><span class="sxs-lookup"><span data-stu-id="572c3-137">**icuuc.lib**</span></span>
    -   <span data-ttu-id="572c3-138">**икуин. lib**</span><span class="sxs-lookup"><span data-stu-id="572c3-138">**icuin.lib**</span></span>

### <a name="version-1709-fall-creators-update"></a><span data-ttu-id="572c3-139">Версия 1709 (обновление источников обновлений)</span><span class="sxs-lookup"><span data-stu-id="572c3-139">Version 1709 (Fall Creators Update)</span></span>
<span data-ttu-id="572c3-140">Был добавлен объединенный файл заголовка **ICU. h**, который содержит содержимое обоих файлов заголовков (икукоммон. h и icui18n. h), а также изменяет тип `UCHAR` на `char16_t` .</span><span class="sxs-lookup"><span data-stu-id="572c3-140">A combined header file, **icu.h**, was added, which contains the contents of both header files above (icucommon.h and icui18n.h), and also changes the type of `UCHAR` to `char16_t`.</span></span>

### <a name="version-1903-may-2019-update"></a><span data-ttu-id="572c3-141">Версия 1903 (обновление Май 2019)</span><span class="sxs-lookup"><span data-stu-id="572c3-141">Version 1903 (May 2019 Update)</span></span>
<span data-ttu-id="572c3-142">Добавлена новая Объединенная библиотека DLL, **icu.dll**, которая содержит как "Common", так и "i18n" библиотеки.</span><span class="sxs-lookup"><span data-stu-id="572c3-142">A new combined DLL, **icu.dll**, was added, which contains both the "common" and "i18n" libraries.</span></span> <span data-ttu-id="572c3-143">Кроме того, в пакет SDK для Windows 10 была добавлена новая библиотека импорта: **ICU. lib**.</span><span class="sxs-lookup"><span data-stu-id="572c3-143">Also, a new import library was added to the Windows 10 SDK: **icu.lib**.</span></span>

<span data-ttu-id="572c3-144">В дальнейшем новые интерфейсы API не будут добавляться в старые заголовки (икукоммон. h и icui18n. h) или в старые библиотеки импорта (икуук. lib и икуин. lib).</span><span class="sxs-lookup"><span data-stu-id="572c3-144">Going forward, no new APIs will be added to the old headers (icucommon.h and icui18n.h) or to the old import libs (icuuc.lib and icuin.lib).</span></span> <span data-ttu-id="572c3-145">Новые API-интерфейсы будут добавлены только в Объединенный заголовок (ICU. h) и Объединенную lib-программу импорта (ICU. lib).</span><span class="sxs-lookup"><span data-stu-id="572c3-145">New APIs will only be added to the combined header (icu.h) and the combined import lib (icu.lib).</span></span>

## <a name="getting-started"></a><span data-ttu-id="572c3-146">Приступая к работе</span><span class="sxs-lookup"><span data-stu-id="572c3-146">Getting Started</span></span>

<span data-ttu-id="572c3-147">Существует три основных шага, которые необходимо выполнить. (обновление Windows 10 для дизайнеров или более поздней версии)</span><span class="sxs-lookup"><span data-stu-id="572c3-147">There are three main steps to follow: (Windows 10 Creators Update or higher)</span></span>

<dl>

1. <span data-ttu-id="572c3-148">Ваше приложение должно быть предназначено для Windows 10 версии 1703 (создателей обновления) или более поздней.</span><span class="sxs-lookup"><span data-stu-id="572c3-148">Your application needs to target Windows 10 Version 1703 (Creators Update) or higher.</span></span>

2. <span data-ttu-id="572c3-149">Добавьте в заголовки:</span><span class="sxs-lookup"><span data-stu-id="572c3-149">Add in the headers:</span></span>

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   <span data-ttu-id="572c3-150">В Windows 10 версии 1709 и более поздних следует включить Объединенный заголовок:</span><span class="sxs-lookup"><span data-stu-id="572c3-150">On Windows 10 Version 1709 and above, you should include the combined header instead:</span></span>

   ``` syntax
   #include <icu.h>
   ```
  
3. <span data-ttu-id="572c3-151">Ссылка на две библиотеки:</span><span class="sxs-lookup"><span data-stu-id="572c3-151">Link to the two libraries:</span></span>

   -   <span data-ttu-id="572c3-152">икуук. lib</span><span class="sxs-lookup"><span data-stu-id="572c3-152">icuuc.lib</span></span>
   -   <span data-ttu-id="572c3-153">икуин. lib</span><span class="sxs-lookup"><span data-stu-id="572c3-153">icuin.lib</span></span>

   <span data-ttu-id="572c3-154">В Windows 10 версии 1903 и выше вместо нее следует использовать объединенную библиотеку:</span><span class="sxs-lookup"><span data-stu-id="572c3-154">On Windows 10 Version 1903 and above, you should use the combined library instead:</span></span>

   -   <span data-ttu-id="572c3-155">ICU. lib</span><span class="sxs-lookup"><span data-stu-id="572c3-155">icu.lib</span></span>

</dl>

<span data-ttu-id="572c3-156">Затем вы можете вызвать любой API ICU C из этих библиотек, которые вам нужны.</span><span class="sxs-lookup"><span data-stu-id="572c3-156">Then, you can call whatever ICU C API from these libraries you want.</span></span> <span data-ttu-id="572c3-157">(Интерфейсы API C++ не предоставляются.)</span><span class="sxs-lookup"><span data-stu-id="572c3-157">(No C++ APIs are exposed.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="572c3-158">Если вы используете устаревшие библиотеки импорта, икуук. lib и икуин. lib, убедитесь, что они перечислены перед библиотеками, такими как онекореуап. lib или Виндовсапп. lib, в параметре компоновщика дополнительные зависимости (см. изображение ниже).</span><span class="sxs-lookup"><span data-stu-id="572c3-158">If you are using the legacy import libraries, icuuc.lib and icuin.lib, ensure they're listed before the umbrella libraries, like onecoreuap.lib or WindowsApp.lib, in the Additional Dependencies Linker setting (see the image below).</span></span> <span data-ttu-id="572c3-159">В противном случае компоновщик свяжется с ICU. lib, что приведет к попытке загрузить icu.dll во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="572c3-159">Otherwise, the linker will link to icu.lib, which will result in an attempt to load icu.dll during run time.</span></span> <span data-ttu-id="572c3-160">Эта библиотека DLL доступна только начиная с версии 1903.</span><span class="sxs-lookup"><span data-stu-id="572c3-160">That DLL is present only starting with version 1903.</span></span> <span data-ttu-id="572c3-161">Таким образом, если пользователь обновляет пакет SDK для Windows 10 на компьютере с Windows до версии 1903, приложение не сможет загрузиться и запуститься.</span><span class="sxs-lookup"><span data-stu-id="572c3-161">So, if a user upgrades the Windows 10 SDK on a pre-version 1903 Windows machine, the app will fail to load and run.</span></span> <span data-ttu-id="572c3-162">Журнал библиотек ICU в Windows см. в статье [Хронология изменений в библиотеке ICU в Windows](#history-of-changes-to-the-icu-library-in-windows).</span><span class="sxs-lookup"><span data-stu-id="572c3-162">For a history of the ICU libraries in Windows, see [History of changes to the ICU library in Windows](#history-of-changes-to-the-icu-library-in-windows).</span></span>

![Пример ICU](images/icu-example.png)

> [!Note]  
>
> - <span data-ttu-id="572c3-164">Это конфигурация для всех платформ.</span><span class="sxs-lookup"><span data-stu-id="572c3-164">This is the configuration for “All Platforms”.</span></span>
> - <span data-ttu-id="572c3-165">Чтобы приложения Win32 использовали ICU, им нужно сначала вызвать [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) .</span><span class="sxs-lookup"><span data-stu-id="572c3-165">For Win32 apps to use ICU, they need to call [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) first.</span></span> <span data-ttu-id="572c3-166">В Windows 10 версии 1903 и более поздних, где доступна Объединенная библиотека ICU (icu.dll/Ику.либ), вызов CoInitializeEx можно опустить с помощью комбинированной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="572c3-166">On Windows 10 version 1903 and above, where the combined ICU library (icu.dll/icu.lib) is available, you can omit the CoInitializeEx call by using the combined library.</span></span>
> - <span data-ttu-id="572c3-167">Не все данные, возвращаемые API-интерфейсами ICU, будут согласованы с операционной системой Windows, так как эта работа по выравниванию еще выполняется.</span><span class="sxs-lookup"><span data-stu-id="572c3-167">Not all data returned by ICU APIs will align with the Windows OS, as this alignment work is still in progress.</span></span> 

## <a name="icu-example-app"></a><span data-ttu-id="572c3-168">Пример приложения ICU</span><span class="sxs-lookup"><span data-stu-id="572c3-168">ICU Example App</span></span>

### <a name="example-code-snippet"></a><span data-ttu-id="572c3-169">Пример фрагмента кода</span><span class="sxs-lookup"><span data-stu-id="572c3-169">Example code snippet</span></span>

<span data-ttu-id="572c3-170">Ниже приведен пример, иллюстрирующий использование API-интерфейсов ICU из приложения UWP в C++.</span><span class="sxs-lookup"><span data-stu-id="572c3-170">The following is an example illustrating the use of ICU APIs from within a C++ UWP application.</span></span> <span data-ttu-id="572c3-171">(Он не является полноценным автономным приложением, а просто примером вызова метода ICU.)</span><span class="sxs-lookup"><span data-stu-id="572c3-171">(It is not intended to be a full stand-alone application, rather it is just an example of calling an ICU method.)</span></span>

<span data-ttu-id="572c3-172">В следующем небольшом примере предполагается, что существуют методы **ErrorMessage** и **аутпутмессаже** , которые каким бы ни был образом выводят строки пользователю.</span><span class="sxs-lookup"><span data-stu-id="572c3-172">The following small example assumes that there are methods **ErrorMessage** and **OutputMessage** that output the strings to the user in some manner.</span></span>

``` syntax
// On Windows 10 Creators Update, include the following two headers. With Windows 10 Fall Creators Update and later, you can just include the single header <icu.h>.
#include <icucommon.h>
#include <icui18n.h>

void FormatDateTimeICU()
{
    UErrorCode status = U_ZERO_ERROR;

    // Create a ICU date formatter, using only the 'short date' style format.
    UDateFormat* dateFormatter = udat_open(UDAT_NONE, UDAT_SHORT, nullptr, nullptr, -1, nullptr, 0, &status);

    if (U_FAILURE(status))
    {
        ErrorMessage(L"Failed to create date formatter.");
        return;
    }

    // Get the current date and time.
    UDate currentDateTime = ucal_getNow();

    int32_t stringSize = 0;
    
    // Determine how large the formatted string from ICU would be.
    stringSize = udat_format(dateFormatter, currentDateTime, nullptr, 0, nullptr, &status);

    if (status == U_BUFFER_OVERFLOW_ERROR)
    {
        status = U_ZERO_ERROR;
        // Allocate space for the formatted string.
        auto dateString = std::make_unique<UChar[]>(stringSize + 1);

        // Format the date time into the string.
        udat_format(dateFormatter, currentDateTime, dateString.get(), stringSize + 1, nullptr, &status);

        if (U_FAILURE(status))
        {
            ErrorMessage(L"Failed to format the date time.");
            return;
        }

        // Output the formatted date time.
        OutputMessage(dateString.get());
    }
    else
    {
        ErrorMessage(L"An error occured while trying to determine the size of the formatted date time.");
        return;
    }

    // We need to close the ICU date formatter.
    udat_close(dateFormatter);
}
```

 

 



