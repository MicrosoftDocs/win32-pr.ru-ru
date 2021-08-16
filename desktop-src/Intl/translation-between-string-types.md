---
description: Функции, перечисленные в следующей таблице, преобразуют символьные строки из одного строкового типа в другой.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Преобразование между строковыми типами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b62ae39307e92c203441ea8ddb9dc61b394a02622e3c86a8949b59539588585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631924"
---
# <a name="translation-between-string-types"></a>Преобразование между строковыми типами

Функции, перечисленные в следующей таблице, преобразуют символьные строки из одного строкового типа в другой.



| Функция                                           | Описание                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [**FoldString**](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | Преобразует одну строку символов в другую.             |
| [**LCMapString завершилось ошибкой**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | Карты строку символов по языку и региональным параметрам.                      |
| [**тауникоде**](/windows/win32/api/winuser/nf-winuser-tounicode)              | Преобразует виртуальный код ключа в символ Юникода. |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | Карты многобайтовую строку в строку юникода.            |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | Карты строку юникода в многобайтовую строку.            |



 

Функции [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) и [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) особенно полезны для приложений, поддерживающих несколько строковых типов. В ANSI C также определяются функции преобразования **wcstombs** и **функции mbstowcs**, но они могут преобразовывать только в набор символов, поддерживаемый стандартной библиотекой C.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Юникод в Windows API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
