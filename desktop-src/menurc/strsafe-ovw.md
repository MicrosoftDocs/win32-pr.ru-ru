---
title: О Стрсафе. h
description: Низкая обработка буфера фрагментацией во многих проблемах безопасности, связанных с переполнением буфера.
ms.assetid: a104a260-1edb-441a-acf8-e2bd3a7d8235
keywords:
- строковые функции
- Стрсафе. h
- Функции стрсафе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9b993ccff6d085f3b1eb14c1920c4c633661df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700865"
---
# <a name="about-strsafeh"></a>О Стрсафе. h

Низкая обработка буфера фрагментацией во многих проблемах безопасности, связанных с переполнением буфера. Функции, определенные в Стрсафе. h, обеспечивают дополнительную обработку для правильной обработки буфера в коде. По этой причине они предназначены для замены встроенных аналогов C/C++, а также конкретных реализаций Windows. Стрсафе. h доступен в Windows SDK, начиная с Windows XP с пакетом обновления 2 (SP2).

К преимуществам функций Стрсафе относятся:

-   Размер буфера назначения всегда предоставляется функции, чтобы убедиться, что функция не выполняет запись после конца буфера.

-   Буферы гарантированно завершаются нулем, даже если операция усекает предполагаемый результат.

-   Все функции возвращают значение **HRESULT** с одним возможным кодом успешного выполнения (**\_ ОК**).

-   Каждая функция доступна в соответствующем количестве символов ("Кч") или количестве байт ("CB").

-   Большинство функций имеют расширенную (ex) версию, доступную для расширенной функциональности.

Дополнительные сведения см. в следующих разделах.

-   [Функции счетчика символов](#character-count-functions)
-   [Функции счетчика байтов](#byte-count-functions)
-   [Использование Стрсафе. h](#using-strsafeh)
-   [См. также](#related-topics)

## <a name="character-count-functions"></a>Функции счетчика символов

Следующие функции используют число символов, а не число байтов.



| Функция                                                                                                                                                                                                                      | Меняющей                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**Стрингкчкат**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt> [ **стрингкчкатекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ тксат](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**лстркат**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**strcat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**стркатбуфф**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                             |
| <dl> <dt>[**Стрингкчкатн**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)</dt> <dt> [ **стрингкчкатнекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **strncat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                   |
| <dl> <dt>[**Стрингкчкопи**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt> [ **стрингкчкопекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ ткскпи](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**лстркпи**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**strcpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                    |
| <dl> <dt>[**Стрингкчкопин**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)</dt> <dt> [ **стрингкчкопинекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ ткснкпи](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>[**Стрингкчжетс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)</dt> <dt> [ **стрингкчжетсекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)</dt> </dl>             | <dl> <dt>[Возвращает, \_ жетвс, \_ жеттс](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>[**Стрингкчпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt> [ **стрингкчпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ стпринтф](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**вспринтф**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**внспринтф**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ снвпринтф, \_ снтпринтф](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>          |
| <dl> <dt>[**Стрингкчвпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt> [ **стрингкчвпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ встпринтф](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ вснвпринтф, \_ вснтпринтф](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**ввспринтф**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**ввнспринтф**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl>, |
| <dl> <dt>[**стрингкчленгс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> </dl>                                                                                                         | <dl> <dt>[strlen, wcslen, \_ ткслен](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="byte-count-functions"></a>Функции счетчика байтов

Следующие функции используют число байтов, а не число символов.



| Функция                                                                                                                                                                                                                  | Меняющей                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**Стрингкбкат**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt> [ **стрингкбкатекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ тксат](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**лстркат**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**strcat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**стркатбуфф**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                            |
| <dl> <dt>[**Стрингкбкатн**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)</dt> <dt> [ **стрингкбкатнекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **strncat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                  |
| <dl> <dt>[**Стрингкбкопи**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt> [ **стрингкбкопекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ ткскпи](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**лстркпи**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**strcpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                   |
| <dl> <dt>[**Стрингкбкопин**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)</dt> <dt> [ **стрингкбкопинекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ ткснкпи](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>[**Стрингкбжетс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)</dt> <dt> [ **стрингкбжетсекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)</dt> </dl>             | <dl> <dt>[Возвращает, \_ жетвс, \_ жеттс](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>[**Стрингкбпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt> [ **стрингкбпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ стпринтф](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**вспринтф**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**внспринтф**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ снвпринтф, \_ снтпринтф](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>         |
| <dl> <dt>[**Стрингкбвпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt> [ **стрингкбвпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ встпринтф](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ вснвпринтф, \_ вснтпринтф](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**ввспринтф**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**ввнспринтф**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl> |
| <dl> <dt>[**стрингкбленгс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                       | <dl> <dt>[strlen, wcslen, \_ ткслен](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="using-strsafeh"></a>Использование Стрсафе. h

-   Чтобы использовать встроенные функции Стрсафе, включите заголовочный файл, как показано здесь, следуя инструкциям **\# include** для всех остальных файлов заголовков.

    `#include <strsafe.h>`

-   Чтобы использовать функции в форме библиотеки, включите следующую инструкцию перед включением Стрсафе. h. Однако рекомендуется использовать встроенные функции.

    `#define STRSAFE_LIB`

    > [!Note]  
    > : Следующие функции должны использоваться в качестве встроенных функций: [**стрингкбжетс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa), [**стрингкбжетсекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa), [**стрингкчжетс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)и [**стрингкчжетсекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa).

     

-   При включении Стрсафе. h в файл старые функции, замененные функциями Стрсафе. h, будут считаться устаревшими. Попытки использовать эти старые функции приведут к ошибке компилятора, сообщающей вам об использовании новых функций. Если вы хотите переопределить это поведение, включите следующую инструкцию перед включением Стрсафе. h.

    `#define STRSAFE_NO_DEPRECATE`

-   Чтобы разрешить только функции подсчета символов, перед включением Стрсафе. h следует включить следующую инструкцию.

    `#define STRSAFE_NO_CB_FUNCTIONS`

-   Чтобы разрешить только функции количества байтов, включите следующую инструкцию перед включением Стрсафе. h.

    `#define STRSAFE_NO_CCH_FUNCTIONS`

    > [!Note]  
    > Вы можете определить **стрсафе \_ без \_ функций \_ CB** или **стрсафе \_ без \_ \_ функций Кч**, но не оба.

     

-   Некоторые функции Стрсафе имеют версии, учитывающие языковой стандарт. По умолчанию эти функции не объявляются в заголовке. Чтобы включить эти объявления, перед включением Стрсафе. h включите следующую инструкцию макроса.

    `#define STRSAFE_LOCALE_FUNCTIONS`

-   Максимальная поддерживаемая длина строки — 2 147 483 647 (**стрсафе \_ Max \_ Кч**) символов: ANSI или Unicode.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Функции стрсафе](string-overviews.md)
</dt> </dl>

 

 