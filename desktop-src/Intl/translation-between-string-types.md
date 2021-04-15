---
description: Функции, перечисленные в следующей таблице, преобразуют символьные строки из одного строкового типа в другой.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Преобразование между строковыми типами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683516"
---
# <a name="translation-between-string-types"></a>Преобразование между строковыми типами

Функции, перечисленные в следующей таблице, преобразуют символьные строки из одного строкового типа в другой.



| Функция                                           | Описание                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [**FoldString**](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | Преобразует одну строку символов в другую.             |
| [**LCMapString завершилось ошибкой**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | Сопоставляет строку символов по языку и региональным параметрам.                      |
| [**тауникоде**](/windows/win32/api/winuser/nf-winuser-tounicode)              | Преобразует виртуальный код ключа в символ Юникода. |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | Сопоставляет многобайтовую строку со строкой в Юникоде.            |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | Сопоставляет строку Юникода с многобайтовой строкой.            |



 

Функции [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) и [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) особенно полезны для приложений, поддерживающих несколько строковых типов. В ANSI C также определяются функции преобразования **wcstombs** и **функции mbstowcs**, но они могут преобразовывать только в набор символов, поддерживаемый стандартной библиотекой C.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Юникод в Windows API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
