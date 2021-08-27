---
description: илангуаже ЛОКАЛи \_
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3159fe26ce1af7291c5990a07297e7513144b5187b55c00086bf46e452ef188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106654"
---
# <a name="locale_ilanguage"></a>илангуаже ЛОКАЛи \_

[Идентификатор языка](language-identifiers.md) с шестнадцатеричным значением. Например, Английский (США) имеет значение 0409, которое указывает на шестнадцатеричное число и эквивалентно 1033 десятичному. Максимально допустимое число символов для этой строки равно пяти, включая завершающий нуль-символ.

**Windows Vista и более поздних версий:** Использование этой константы может привести к тому, что [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) возвратит недопустимый идентификатор локали. При вызове этой функции приложение должно использовать константу [ \_ SNAME локали](locale-sname.md) .

 

 



