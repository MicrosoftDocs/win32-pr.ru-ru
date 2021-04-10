---
description: Для наборов символов используются следующие функции.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Функции Юникода и кодировка символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081331"
---
# <a name="unicode-and-character-set-functions"></a>Функции Юникода и кодировка символов

Для наборов символов используются следующие функции.



| Функция                                                       | Описание                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**жеттекстчарсет**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | Извлекает идентификатор кодировки для шрифта, выбранного в данный момент в указанном контексте устройства.         |
| [**жеттекстчарсетинфо**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | Извлекает сведения о кодировке шрифта, выбранного в данный момент в указанном контексте устройства. |
| [**исдбкслеадбите**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | Определяет, является ли указанный символ старшим байтом для системной кодовой страницы Windows ANSI по умолчанию (CP \_ ACP).           |
| [**исдбкслеадбитикс**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | Определяет, является ли указанный символ потенциально старшим байтом.                                                       |
| [**истекстуникоде**](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | Определяет, может ли буфер содержать форму текста в Юникоде.                                                   |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | Сопоставляет символьную строку со строкой UTF-16 (расширенная символьная).                                                          |
| [**транслатечарсетинфо**](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | Преобразует сведения о кодировке и задает соответствующие значения для всех элементов целевой структуры.           |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | Сопоставляет строку UTF-16 (расширенных символов) с новой символьной строкой.                                                      |
| [**битестауникоде**](/previous-versions/dd317724(v=vs.85))                       | Не используйте.                                                                                                           |
| [**нлсдллкодепажетранслатион**](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | Не используйте.                                                                                                           |
| [**уникодетобитес**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))                       | Не используется.                                                                                                           |



 

 

 
