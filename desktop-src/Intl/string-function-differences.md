---
description: В этом разделе описываются различия между строковыми функциями, используемыми для обработки сведений о кодировке Юникод и кодировке. эти функции имеют как юникод, так Windows реализации кодовых страниц для поддержки юникода и Windows параметров кодовой страницы.
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: Различия строковых функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60a6208e858eceac65ac8826ffbff6303b970969cae6f635d0bcc027dd6d9f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146997"
---
# <a name="string-function-differences"></a>Различия строковых функций

В этом разделе описываются различия между строковыми функциями, используемыми для обработки сведений о кодировке Юникод и кодировке. эти функции имеют как [юникод](unicode.md) , так [Windows реализации кодовых страниц](code-pages.md) для поддержки юникода и Windows параметров кодовой страницы.

Для следующих строковых функций не требуется специальный комментарий. их юникод и Windows реализации кодовых страниц работают одинаково.

-   [**чарнекст**](/windows/win32/api/winuser/nf-winuser-charnexta)
-   [**чарпрев**](/windows/win32/api/winuser/nf-winuser-charpreva)
-   [**Стрингкчкат**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [ **стрингкчкатекс**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)
-   [**Стрингкчкопи**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [ **стрингкчкопекс**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)
-   [**Стркбленгс**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha), [ **стркчленгс**](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)

значение длины, полученное одной из функций длины строки, всегда основано на обычной ширине символов: 8 бит для Windows кодовых страниц, 16 бит для юникода. Это значение часто называют "количеством символов". этот термин является строго верным, поскольку Windows кодовые страницы, использующие [двухбайтовые](double-byte-character-sets.md) кодировки (dbcs), имеют некоторые полноширинные символы, которые фактически представлены двумя последовательными байтами. Аналогичная ситуация возникает для [суррогатов](surrogates-and-supplementary-characters.md) в Юникоде.

Следующие строковые функции чувствительны к языковому стандарту текущего потока, производному от выбранного пользователем языка на панели управления. Функции [**лстркмп**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) и [**лстркмпи**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) не выполняют сравнения БАЙТОВ, такие как ANSI намесакес, например [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp). Вместо этого они сравнивают строки в соответствии с правилами языкового стандарта.

-   [**чарловер**](/windows/win32/api/winuser/nf-winuser-charlowera)
-   [**чарловербуфф**](/windows/win32/api/winuser/nf-winuser-charlowerbuffa)
-   [**чаруппер**](/windows/win32/api/winuser/nf-winuser-charuppera)
-   [**чаруппербуфф**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
-   [**лстркмп**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)
-   [**лстркмпи**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

приведенные ниже функции преобразуются между набором символов OEM и текущей Windows кодовой страницей или юникодом в зависимости от используемой версии.

-   [**чартуем**](/windows/win32/api/winuser/nf-winuser-chartooema)
-   [**чартуембуфф**](/windows/win32/api/winuser/nf-winuser-chartooembuffa)
-   [**оемточарбуфф**](/windows/win32/api/winuser/nf-winuser-oemtocharbuffa)

Функции печати, например [**стрингкбпринтф**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), поддерживают Юникод, предоставляя следующие новые и измененные типы данных в спецификациях формата. Эти спецификации формата влияют на способ интерпретации соответствующего входного параметра функциями.



| Спецификация формата | тип данных для версии кодовой страницы Windows | Тип данных для версии Юникода |
|----------------------|-----------------------------------------|-------------------------------|
| с                    | CHAR                                    | WCHAR                         |
| C                    | WCHAR                                   | CHAR                          |
| HC, hC               | CHAR                                    | CHAR                          |
| HS, hS               | LPSTR                                   | LPSTR                         |
| LC, lC               | WCHAR                                   | WCHAR                         |
| Ls, lS               | LPWSTR                                  | LPWSTR                        |
| s                    | LPSTR                                   | LPWSTR                        |
| S                    | LPWSTR                                  | LPSTR                         |



 

Тип данных для выходного текста всегда зависит от версии функции. если тип данных входного параметра и тип данных выходного текста не согласуются, функция print выполняет преобразование из юникода в текущую Windows кодовую страницу или наоборот по мере необходимости.

Для версии функции печати, поддерживающей Юникод, строка форматирования имеет формат Юникод, а является выходным текстом.

> [!Caution]  
> Низкая обработка буфера фрагментацией во многих проблемах безопасности, связанных с переполнением буфера. См. раздел [Справочник по стрсафе. h](../menurc/strsafe-ovw.md). Функции, определенные в Стрсафе. h, обеспечивают дополнительную обработку для правильной обработки буфера в коде. по этой причине они предназначены для замены встроенных аналогов C/C++, а также конкретных реализаций Microsoft Windows. Дополнительные сведения см. в разделе [вопросы безопасности: международные функции](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Юникод в Windows API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
