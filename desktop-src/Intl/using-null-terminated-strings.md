---
description: При использовании строк, заканчивающихся символом NULL, приложения Юникода всегда должны приводить к типу TCHAR ноль.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Использование строк, заканчивающихся символом NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce12079fa3d0c5a88af369a347f1cd655136ee09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272951"
---
# <a name="using-null-terminated-strings"></a>Использование строк, заканчивающихся символом NULL

При использовании строк, заканчивающихся символом NULL, приложения Юникода всегда должны приводить к типу TCHAR ноль. Код Символ 0x0000 — признак конца строки Юникода для строки, завершающейся нулем. Для этого кода недостаточно одного байта, так как многие символы Юникода содержат нулевые байты как старший или младший байт. Примером является буква A, для которой код символа — 0x0041.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование специальных символов в Юникоде](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



