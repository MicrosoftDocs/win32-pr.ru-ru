---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Вложенные экземпляры Скоредпроперти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1bfed09c48bc0ac6e93e09f96dc8116e8b0a91
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105684807"
---
# <a name="nested-scoredproperty-instances"></a>Вложенные экземпляры Скоредпроперти

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Обратите внимание, что добавление экземпляров Скоредпроперти в качестве дочерних элементов экземпляра параметра не разрешено. Экземпляры Скоредпроперти также могут быть вложенными в другие экземпляры Скоредпроперти. Это полезно, когда свойство устройства является сложным и лучше представлено несколькими подсвойствами. Добавление вложенных свойств в существующее (или открытое) свойство или Скоредпроперти является хорошим способом улучшения параметра, сохраняя при этом переносимость с существующими экземплярами параметров. Например, экземпляры стандартных параметров для функции MediaType содержат Скоредпроперти, описывающий вес носителя как «Light», «средний», «высокий» или «Екстрахеави». Если требуется более точное описание веса, можно добавить подсвойство (GramsPer100Sheets в следующем примере), содержащее фактический вес (в граммах) 100 листов мультимедиа. Расширенный параметр может выглядеть, как в следующем примере.

``` syntax
<!-- Note: The following ScoredProperty is not a Public Print Schema ScoredProperty -->
<!-- This example shows a nested ScoredProperty defined by a Private namespace-->
<!-- It is included for illustration purposes. -->

<psf:ScoredProperty name="FabrikamES500:PaperWeight">
  <psf:Value xsi:type="xs:string">Medium</psf:Value>
  <psf:ScoredProperty name="FabrikamES500:GramsPerSheet">
    <Value xsi:type="decimal">109.5</Value>
  </psf:ScoredProperty>
</psf:ScoredProperty>
```

Сравнение исходного и расширенного параметров обеспечивает близкое к идеальному совпадению, так как расширенный параметр является надмножеством исходного, а расположения и значения каждого из исходных экземпляров Скоредпроперти сохраняются.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



