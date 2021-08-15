---
description: Термин FORMSOF выполняет поиск совпадений с другими лингвистическими формами слова.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: FORMSOF термин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ffcbd832833a506db99236bf26921a4b0145ffe5bfccaed8fff59103370291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863447"
---
# <a name="formsof-term"></a>FORMSOF термин

Термин FORMSOF выполняет поиск совпадений с другими лингвистическими формами слова. Ниже приведен синтаксис термина FORMSOF:


```
FORMSOF (<generation_type>,<match_words>)
```



тип поколения указывает, как Microsoft Windows Search выбирает альтернативные формы word. Значение **перегиба** выбирает альтернативные формы перегиба для слов Match. Если слово является глаголом, используются альтернативные времена. Если слово является существительным, для обнаружения совпадений используются единственные, множественные и многочисловые формы.

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

 

 



