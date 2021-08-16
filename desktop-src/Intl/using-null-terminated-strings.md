---
description: При использовании строк, заканчивающихся символом NULL, приложения Юникода всегда должны приводить к типу TCHAR ноль.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Использование строк, заканчивающихся символом NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a5f27048bde2af75eca28626a562473ceffcc66f3f2f23509beca4fba06ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631784"
---
# <a name="using-null-terminated-strings"></a>Использование строк, заканчивающихся символом NULL

При использовании строк, заканчивающихся символом NULL, приложения Юникода всегда должны приводить к типу TCHAR ноль. Код Символ 0x0000 — признак конца строки Юникода для строки, завершающейся нулем. Для этого кода недостаточно одного байта, так как многие символы Юникода содержат нулевые байты как старший или младший байт. Примером является буква A, для которой код символа — 0x0041.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование специальных символов в Юникоде](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



