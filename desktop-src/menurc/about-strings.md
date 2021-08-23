---
title: Сведения о строках
description: В этом разделе обсуждаются строковые функции.
ms.assetid: f1799fbf-4619-4b19-998e-b1d2f4c19a35
keywords:
- ресурсы, строки
- строки;
- строковые функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50f47205ec021bffaa4cb6e24aa4825177a3fc0d8546f3a14b1d4b0e0ca4271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034392"
---
# <a name="about-strings"></a>Сведения о строках

Строковые функции предоставляют приложениям средства копирования, сравнения, сортировки, форматирования и преобразования символьных строк, а также средства для определения символьного типа каждого символа в строке. Все строковые функции поддерживают однобайтовые, двухбайтовые и Юникод наборы символов, если эти наборы символов поддерживаются операционной системой, в которой выполняется приложение.

**Предупреждение системы безопасности:** Неправильное использование строковых функций может вызвать проблемы безопасности приложения. Обычно это включает переполнение буфера, которое может привести к атаке типа "отказ в обслуживании" для вашего приложения или к внедрению исполняемого кода от злоумышленника. Функции Стрсафе обеспечивают более безопасную обработку строк и рекомендуются для повышения безопасности приложения. Дополнительные сведения об этих функциях см. в разделе [Использование функций стрсафе. h](strsafe-ovw.md).

В этом разделе рассматриваются следующие темы.

-   [Сравнение с строковыми функциями C Run-Time](#comparison-with-c-run-time-string-functions)
-   [Строковые ресурсы](#string-resources)

## <a name="comparison-with-c-run-time-string-functions"></a>Сравнение с строковыми функциями C Run-Time

Многие строковые функции дублируют или расширяют привычные строковые функции из стандартной библиотеки времени выполнения C (CRT). Многие из улучшений позволяют строковым функциям работать с Юникодом или расширенными наборами символов. в следующей таблице показаны функции CRT, функции Windows (поддерживающие юникод, в отличие от функций CRT) и функции стрсафе.



| Строковая функция CRT                                       | Windows String, функция    | Функция Стрсафе                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [strcat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019) | [**лстркат**](/windows/desktop/api/Winbase/nf-winbase-lstrcata) | <dl> <dt>[**Стрингкчкат**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt>[**стрингкчкатекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> <dt>[**стрингкбкат**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt>[**стрингкбкатекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>         |
| [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp?view=vs-2019) | [**лстркмп**](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa) | (нет эквивалентной функции)                                                                                                                                                                                                                                                                                                                                                                                  |
| [strcpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019) | [**лстркпи**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya) | <dl> <dt>[**Стрингкчкопи**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt>[**стрингкчкопекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> <dt>[**стрингкбкопи**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt>[**стрингкбкопекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl> |
| [strlen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019) | [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) | <dl> <dt>[**Стрингкчленгс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> <dt> [ **стрингкбленгс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                                                                                                       |



 

Функция **strlen** , например, всегда возвращает число байтов в строке, но функция [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) возвращает число значений **TCHAR** , которые ссылаются на байты для версий функции или значения **WCHAR** ANSI для версий функций или значений типа данных в Юникоде.

Следующие строковые функции отличаются от стандартных функций C, таких как **ToLower** и **ToUpper** в том, что они работают с любым символом в кодировке. Например, с помощью функции [**чарловер**](/windows/desktop/api/Winuser/nf-winuser-charlowera) приложение может преобразовать прописную букву U с умляут (u) в нижний регистр (u). Дополнительные сведения о кодировках см. в разделе [Однобайтовые кодировки](/windows/desktop/Intl/single-byte-character-sets).



| Функция                               | Описание                                   |
|----------------------------------------|-----------------------------------------------|
| [**чарловер**](/windows/desktop/api/Winuser/nf-winuser-charlowera)         | Преобразует символ или строку в нижний регистр.  |
| [**чарловербуфф**](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa) | Преобразует строку символов в нижний регистр.     |
| [**чарнекст**](/windows/desktop/api/Winuser/nf-winuser-charnexta)           | Переходит к следующему символу в строке.      |
| [**чарпрев**](/windows/desktop/api/Winuser/nf-winuser-charpreva)           | Перемещает к предыдущему символу в строке. |
| [**чаруппер**](/windows/desktop/api/Winuser/nf-winuser-charuppera)         | Преобразует символ или строку в верхний регистр.  |
| [**чаруппербуфф**](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa) | Преобразует строку в верхний регистр.               |



 

Следующие строковые функции делают определение символа на основе семантики языка, выбранного пользователем. Эти функции включены в Юникоде.



| Функция                                         | Описание                                     |
|--------------------------------------------------|-------------------------------------------------|
| [**исчаралфа**](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)               | Определяет, является ли символ буквой.   |
| [**исчаралфанумерик**](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica) | Определяет, является ли символ буквенно-цифровым. |
| [**исчарловер**](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)               | Определяет, является ли символ строчным.    |
| [**исчаруппер**](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)               | Определяет, является ли символ прописным.    |



 

В следующей таблице приведены расширения Юникода для стандартных функций среды выполнения C (CRT). Как упоминалось ранее, функции Стрсафе обеспечивают более безопасную обработку строк и рекомендуются для повышения безопасности приложения.



| Стандартная функция CRT                                       | String, функция                | Функция Стрсафе                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)  | [**вспринтф**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)   | <dl> <dt>[**Стрингкчпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt>[**стрингкчпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> <dt>[**стрингкбпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt>[**стрингкбпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>         |
| [vsprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019) | [**ввспринтф**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa) | <dl> <dt>[**Стрингкчвпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt>[**стрингкчвпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> <dt>[**стрингкбвпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt>[**стрингкбвпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> |



 

## <a name="string-resources"></a>Строковые ресурсы

Приложение, которое поддерживает символьные строки в ресурсах, может быть переведено на новые языки с минимальными усилиями. Вместо поиска строк в исходных модулях можно просто перевести строки в файл ресурсов и повторно связать приложение. Кроме того, использование строковых ресурсов упрощает создание версий приложения в Юникоде и в формате, отличном от Юникода, из тех же исходных файлов.

Функция [**лоадстринг**](/windows/desktop/api/Winuser/nf-winuser-loadstringa) загружает строковый ресурс из исполняемого файла приложения. Функция [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) загружает строковый ресурс и интерпретирует параметры форматирования, которые могут быть внедрены в строку.

Ресурсы в двоичной форме хранятся в формате Юникода. При загрузке ресурсов приложения могут использовать версию Юникода функций ресурсов (например,[**лоадстрингв**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)) для получения ресурсов в виде данных в Юникоде.

Для 16-разрядных строковых ресурсов длина 255 символов равна максимальной. Для 32-разрядных строковых ресурсов длина 65535 символов равна максимальной.

 

 