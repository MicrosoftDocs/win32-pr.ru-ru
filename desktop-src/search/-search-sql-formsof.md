---
description: Термин FORMSOF выполняет поиск совпадений с другими лингвистическими формами слова.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: FORMSOF термин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701391"
---
# <a name="formsof-term"></a>FORMSOF термин

Термин FORMSOF выполняет поиск совпадений с другими лингвистическими формами слова. Ниже приведен синтаксис термина FORMSOF:


```
FORMSOF (<generation_type>,<match_words>)
```



Тип поколения указывает, как Microsoft Windows Search выбирает альтернативные формы. Значение **перегиба** выбирает альтернативные формы перегиба для слов Match. Если слово является глаголом, используются альтернативные времена. Если слово является существительным, для обнаружения совпадений используются единственные, множественные и многочисловые формы.

Слово Match \_ — это одно или несколько слов, разделенных запятыми.

## <a name="examples"></a>Примеры

В следующем примере выполняется поиск совпадений для слова «Run». Этот пример соответствует документам, содержащим "Run", "выполняющемуся" или "Run".


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Предикат FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Предложения WHERE](-search-sql-where.md)
</dt> </dl>

 

 



