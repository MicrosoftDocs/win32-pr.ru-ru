---
description: илангуаже ЛОКАЛи \_
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b68ccd270319fa00cd2e983b5f9159d454f160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682400"
---
# <a name="locale_ilanguage"></a>илангуаже ЛОКАЛи \_

[Идентификатор языка](language-identifiers.md) с шестнадцатеричным значением. Например, Английский (США) имеет значение 0409, которое указывает на шестнадцатеричное число и эквивалентно 1033 десятичному. Максимально допустимое число символов для этой строки равно пяти, включая завершающий нуль-символ.

**Windows Vista и более поздние версии:** Использование этой константы может привести к тому, что [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) возвратит недопустимый идентификатор локали. При вызове этой функции приложение должно использовать константу [ \_ SNAME локали](locale-sname.md) .

 

 



