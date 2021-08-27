---
description: Международные компоненты для Юникода (ICU) — это зрелый, широко используемый набор API-интерфейсов глобализации с открытым исходным кодом.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: Международные компоненты для Юникода (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7fec661b24e352c24abddf687e6b119752e39ce80c12dc409000afa179f1f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107032"
---
# <a name="international-components-for-unicode-icu"></a>Международные компоненты для Юникода (ICU)

Международные компоненты для Юникода (ICU) — это зрелый, широко используемый набор API-интерфейсов глобализации с открытым исходным кодом. ICU использует обширный общий языковой стандарт Юникода (КЛДР) в качестве библиотеки данных, предоставляя поддержку глобализации для приложений программного обеспечения. ICU является широко переносимым и дает приложениям одинаковые результаты во всех платформах.

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a>Основные особенности служб API глобализации, предоставляемых ICU

-   **Преобразование кодовой страницы**: Преобразование текстовых данных в Юникод или из Юникода, а также практически любой другой набор символов или кодировка. Таблицы преобразования ICU основаны на данных кодировки, собираемых IBM на протяжении многих десятилетий, и являются наиболее полными доступными в любом месте.
-   **Параметры сортировки**: Сравните строки в соответствии с соглашениями и стандартами определенного языка, региона или страны. Параметры сортировки ICU основаны на алгоритме сортировки Юникода и правилах сравнения для конкретного языкового стандарта от КЛДР.
-   **Форматирование**: форматирование чисел, дат, времени и денежных сумм в соответствии с соглашениями выбранного языкового стандарта. Сюда входит преобразование названий месяцев и дней в выбранный язык, выбор соответствующих сокращений, правильное упорядочивание полей и т. д. Эти данные также поступают из репозитория данных общего языкового стандарта.
-   **Вычисления времени**. несколько типов календарей предоставляются за пределами обычного григорианского календаря. Предоставляется тщательный набор API-интерфейсов для вычисления часовых поясов.
-   **Поддержка Юникода**. ICU тесно отслеживает Стандарт Юникода, обеспечивая легкий доступ ко всем свойствам символов Юникода, нормализации Юникода, сложению регистра и другим фундаментальным операциям, указанным в [стандарте Юникода](https://www.unicode.org/).
-   **Регулярное выражение**: регулярные выражения ICU полностью поддерживают Юникод, обеспечивая очень конкурентную производительность.
-   **Bidi**: поддержка обработки текста, содержащего сочетание слева направо (английский) и справа налево (арабский или иврит).

Дополнительные сведения можно найти на веб-сайте ICU: <http://site.icu-project.org/>

## <a name="overview"></a>Обзор

в Windows 10 Creators Update ICU был интегрирован в Windows, что обеспечивает общедоступные интерфейсы api C и данные.

> [!IMPORTANT]
> версия ICU в Windows предоставляет только api C. Он не предоставляет никаких API-интерфейсов C++. К сожалению, невозможность предоставления интерфейсов API C++ из-за отсутствия стабильного интерфейса ABI в C++.

Документацию по API ICU C см. на официальной странице документации по ICU: <http://icu-project.org/apiref/icu4c/index.html#Module>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a>Журнал изменений в библиотеке ICU в Windows

### <a name="version-1703-creators-update"></a>Версия 1703 (авторское обновление)
Библиотека ICU впервые была добавлена в Windows 10ную ОС в этой версии.
Он был добавлен как:
- Две системные библиотеки DLL:
    -   **icuuc.dll** (это ICU "Common" Библиотека)
    -   **icuin.dll** (это библиотека ICU "i18n")
- два файла заголовков в пакете SDK для Windows 10:
    -   **икукоммон. h**
    -   **icui18n. h**
- две библиотеки импорта в пакете SDK для Windows 10:
    -   **икуук. lib**
    -   **икуин. lib**

### <a name="version-1709-fall-creators-update"></a>Версия 1709 (обновление источников обновлений)
Был добавлен объединенный файл заголовка **ICU. h**, который содержит содержимое обоих файлов заголовков (икукоммон. h и icui18n. h), а также изменяет тип `UCHAR` на `char16_t` .

### <a name="version-1903-may-2019-update"></a>Версия 1903 (обновление Май 2019)
Добавлена новая Объединенная библиотека DLL, **icu.dll**, которая содержит как "Common", так и "i18n" библиотеки. кроме того, в Windows 10 SDK: **icu. lib** была добавлена новая библиотека импорта.

В дальнейшем новые интерфейсы API не будут добавляться в старые заголовки (икукоммон. h и icui18n. h) или в старые библиотеки импорта (икуук. lib и икуин. lib). Новые API-интерфейсы будут добавлены только в Объединенный заголовок (ICU. h) и Объединенную lib-программу импорта (ICU. lib).

## <a name="getting-started"></a>Приступая к работе

существуют три основных шага, которые необходимо выполнить. (Windows 10 Creators Update или более поздней версии)

<dl>

1. приложение должно быть предназначено для Windows 10 версии 1703 (автор обновления) или более поздней.

2. Добавьте в заголовки:

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   в Windows 10 версии 1709 и выше следует включить объединенный заголовок.

   ``` syntax
   #include <icu.h>
   ```
  
3. Ссылка на две библиотеки:

   -   икуук. lib
   -   икуин. lib

   в Windows 10 версии 1903 и выше следует использовать объединенную библиотеку.

   -   ICU. lib

</dl>

Затем вы можете вызвать любой API ICU C из этих библиотек, которые вам нужны. (Интерфейсы API C++ не предоставляются.)

> [!IMPORTANT]
> Если вы используете устаревшие библиотеки импорта, икуук. lib и икуин. lib, убедитесь, что они перечислены перед библиотеками, такими как онекореуап. lib или Виндовсапп. lib, в параметре компоновщика дополнительные зависимости (см. изображение ниже). В противном случае компоновщик свяжется с ICU. lib, что приведет к попытке загрузить icu.dll во время выполнения. Эта библиотека DLL доступна только начиная с версии 1903. таким образом, если пользователь обновляет Windows 10 SDK на компьютере предварительной версии 1903 Windows, приложение не сможет загрузиться и запуститься. журнал библиотек ICU в Windows см. в статье [журнал изменений библиотеки ICU в Windows](#history-of-changes-to-the-icu-library-in-windows).

![Пример ICU](images/icu-example.png)

> [!Note]  
>
> - Это конфигурация для всех платформ.
> - Чтобы приложения Win32 использовали ICU, им нужно сначала вызвать [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) . в Windows 10 версии 1903 и выше, где доступна объединенная библиотека ICU (icu.dll/ику.либ), вызов CoInitializeEx можно опустить с помощью комбинированной библиотеки.
> - не все данные, возвращаемые api-интерфейсами ICU, будут согласованы с Windows OS, так как эта работа по выравниванию еще выполняется. 

## <a name="icu-example-app"></a>Пример приложения ICU

### <a name="example-code-snippet"></a>Пример фрагмента кода

Ниже приведен пример, иллюстрирующий использование API-интерфейсов ICU из приложения UWP в C++. (Он не является полноценным автономным приложением, а просто примером вызова метода ICU.)

В следующем небольшом примере предполагается, что существуют методы **ErrorMessage** и **аутпутмессаже** , которые каким бы ни был образом выводят строки пользователю.

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

 

 



