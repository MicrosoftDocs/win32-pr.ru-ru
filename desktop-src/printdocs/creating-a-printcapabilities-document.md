---
description: После проверки PrintTicket можно использовать для создания моментального снимка PrintCapabilities.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Создание документа PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1a01395df674b683349bd4a5f42fe1bd57ef2768ef4d967ba3aeda7734f5e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950204"
---
# <a name="creating-a-printcapabilities-document"></a>Создание документа PrintCapabilities

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

После проверки PrintTicket можно использовать для создания моментального снимка PrintCapabilities. Поставщик должен иметь внутреннее представление для любого свойства, значение которого зависит от конфигурации устройства. Например, если Спотдиаметер является свойством, которое зависит от функций разрешения и MediaType, внутреннее представление Спотдиаметер, связанное с различными значениями для разрешения, и параметр MediaType может выглядеть так, как показано в следующей таблице.



| Решение      | MediaType         | спотдиаметер   |
|-----------------|-------------------|----------------|
| 300<br/>  | Bond<br/>   | 520<br/> |
| 300<br/>  | Глянцевое<br/> | 350<br/> |
| 600<br/>  | Bond<br/>   | 330<br/> |
| 600<br/>  | Глянцевое<br/> | 180<br/> |
| 1200<br/> | Bond<br/>   | 250<br/> |
| 1200<br/> | Глянцевое<br/> | 100<br/> |



 

В этом примере поставщик PrintCapabilities должен использовать предоставленный PrintTicket, чтобы выбрать соответствующую запись из внутренней таблицы и сообщить о том, что в качестве значения свойства Спотдиаметер. Этот процесс повторяется для каждого свойства с несколькими значениями (для каждого свойства, значение которого зависит от конфигурации). В разделе [схема и построение документа PrintCapabilities](printcapabilities-schema-and-document-construction.md) описаны другие шаги, связанные с созданием моментального снимка PrintCapabilities.

Чтобы создать моментальный снимок документа PrintCapabilities по умолчанию, укажите PrintTicket по умолчанию (а не произвольный PrintTicket) для метода, который создает документы PrintCapabilities.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




